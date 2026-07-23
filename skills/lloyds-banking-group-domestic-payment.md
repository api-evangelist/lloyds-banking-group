---
name: Initiate a domestic payment (PIS)
description: >-
  Create a Lloyds Banking Group OBIE domestic-payment consent, confirm funds, have
  the customer authorise it, then submit the payment idempotently.
api: openapi/obie-payment-initiation-openapi.yaml
operations:
  - CreateDomesticPaymentConsents
  - GetDomesticPaymentConsentsConsentId
  - GetDomesticPaymentConsentsConsentIdFundsConfirmation
  - CreateDomesticPayments
  - GetDomesticPaymentsDomesticPaymentId
---

# Initiate a domestic payment (PIS)

Use the OBIE Read/Write Payment Initiation API to make a single domestic payment
with the customer's authorisation. FAPI security applies (OAuth2/OIDC token, mTLS,
and a detached JWS in `x-jws-signature` on the payment request).

## Steps

1. **Create the payment consent** — `CreateDomesticPaymentConsents`
   (`POST /domestic-payment-consents`) with a client-credentials token
   (`TPPOAuth2Security`, scope `payments`). Include the `Data.Initiation` block
   (creditor account, `InstructedAmount`), the `x-idempotency-key` header, and the
   `x-jws-signature`. Store the `ConsentId`.
2. **Redirect the customer for SCA** — send the PSU through the authorization-code
   flow (`PSUOAuth2Security`) for this `ConsentId`; they complete Strong Customer
   Authentication and you exchange the code for a PSU access token.
3. **Confirm consent + funds** — `GetDomesticPaymentConsentsConsentId` to verify
   status is `Authorised`, then
   `GetDomesticPaymentConsentsConsentIdFundsConfirmation`
   (`GET /domestic-payment-consents/{ConsentId}/funds-confirmation`) to check funds
   are available.
4. **Submit the payment** — `CreateDomesticPayments`
   (`POST /domestic-payments`) referencing the authorised `ConsentId`, with a **fresh
   `x-idempotency-key`** and the `x-jws-signature`. The `Data.Initiation` must match
   the consent exactly or you get `UK.OBIE.Resource.ConsentMismatch`.
5. **Track status** — `GetDomesticPaymentsDomesticPaymentId`
   (`GET /domestic-payments/{DomesticPaymentId}`) until the payment reaches a final
   status.

## Rules

- **Idempotency is mandatory on writes.** Replaying the same `x-idempotency-key`
  (max 40 chars, ~24h retention) returns the original payment instead of creating a
  duplicate - always retry with the same key, never a new one.
- The `Data.Initiation` in step 4 must be byte-for-byte consistent with step 1.
- Sign payment requests with a detached JWS (`x-jws-signature`, `b64=false`).
- Handle `429` with back-off; read `OBErrorResponse1.Errors[].ErrorCode`
  (`UK.OBIE.*`) on 4xx.
