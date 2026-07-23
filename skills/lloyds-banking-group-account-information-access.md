---
name: Access account and transaction information (AIS)
description: >-
  Set up a Lloyds Banking Group OBIE account-access consent, have the customer
  authorise it, then read accounts, balances, and transactions.
api: openapi/obie-account-info-openapi.yaml
operations:
  - CreateAccountAccessConsents
  - GetAccountAccessConsentsConsentId
  - GetAccounts
  - GetAccountsAccountId
  - GetAccountsAccountIdBalances
  - GetAccountsAccountIdTransactions
---

# Access account and transaction information (AIS)

Use the OBIE Read/Write Account and Transaction Information API to read a customer's
account data with their consent. All calls require FAPI security: OAuth2/OIDC access
token, mutual-TLS client certificate, and the `x-fapi-*` headers.

## Prerequisites

- Registered as a TPP in the Open Banking directory with valid OBIE/eIDAS certificates.
- Onboarded on the Lloyds developer portal; client credentials issued.
- mTLS transport established on every request.

## Steps

1. **Create the account-access consent** — `CreateAccountAccessConsents`
   (`POST /account-access-consents`) with a client-credentials token
   (`TPPOAuth2Security`, scope `accounts`). Supply the `Data.Permissions` you need
   (e.g. `ReadAccountsDetail`, `ReadBalances`, `ReadTransactionsDetail`) and set the
   `x-fapi-interaction-id` header. Store the returned `ConsentId`.
2. **Redirect the customer for SCA** — send the PSU to the authorization endpoint
   (`PSUOAuth2Security`, authorization-code flow) referencing the `ConsentId`. The
   customer completes Strong Customer Authentication; you receive an authorization
   code and exchange it for a PSU access token.
3. **Confirm consent status** — `GetAccountAccessConsentsConsentId`
   (`GET /account-access-consents/{ConsentId}`); proceed only when status is
   `Authorised`.
4. **List accounts** — `GetAccounts` (`GET /accounts`) with the PSU token.
5. **Read detail** — `GetAccountsAccountId`, `GetAccountsAccountIdBalances`, and
   `GetAccountsAccountIdTransactions` for each `AccountId`. Follow `Links.Next` to
   page through transactions.

## Rules

- Echo/log `x-fapi-interaction-id` on every request for correlation.
- Respect a `429` response by backing off before retry.
- On error, read the `OBErrorResponse1` envelope: each `Errors[].ErrorCode` is a
  `UK.OBIE.*` code with a `Path` to the offending field.
- A revoked consent surfaces via the Event Notifications API
  (`consent-authorization-revoked`) - stop using the token when received.
