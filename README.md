# Lloyds Banking Group (lloyds-banking-group)

Lloyds Banking Group plc is the United Kingdom's largest retail and commercial banking group, serving personal, business, and corporate customers through the Lloyds Bank, Halifax, Bank of Scotland, MBNA, and Scottish Widows brands. Formed in 2009 through the acquisition of HBOS by Lloyds TSB, it is a publicly listed company on the London Stock Exchange (LLOY) and a FTSE 100 constituent - not a mutual or building society. It is authorised by the Prudential Regulation Authority and regulated by the Financial Conduct Authority and the PRA. As one of the nine CMA-mandated banks (CMA9), Lloyds operates a public developer platform that publishes UK Open Banking (OBIE / PSD2) APIs.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lloyds-banking-group/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lloyds-banking-group/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Banking
- Open Banking
- PSD2
- OBIE
- CMA9
- United Kingdom
- Payments
- Account Information
- Open Data
- FAPI

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

### Lloyds Banking Group Open Data API

Public, unauthenticated UK Open Banking Open Data API exposing reference data - ATMs, branches, personal current accounts, business current accounts, unsecured SME loans, and commercial credit cards - conformant to the OBIE Open Data standard. Confirmed live on 2026-07-23 (HTTP 200).

- **Human URL:** [https://developer.lloydsbanking.com/prod01/lbg/opendata_lloyds](https://developer.lloydsbanking.com/prod01/lbg/opendata_lloyds)
- **Base URL:** `https://api.lloydsbank.com/open-banking/v2.2`

#### Properties

- [OpenAPI](openapi/obie-opendata-swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lloydsbanking.com/prod01/lbg/opendata_lloyds)
- [API Reference](https://developer.lloydsbanking.com/prod01/lbg/products)

### Lloyds Banking Group Account and Transaction Information API

OBIE Read/Write Account and Transaction Information (AIS) API for accessing account, balance, transaction, beneficiary, standing order, direct debit, and statement data with customer consent. FAPI-secured (OAuth2/OIDC, mTLS, PSD2 SCA); requires developer-portal onboarding.

- **Human URL:** [https://developer.lloydsbanking.com/prod01/lbg/products](https://developer.lloydsbanking.com/prod01/lbg/products)
- **Base URL:** `https://api.lloydsbank.com/open-banking/v3.1`

#### Properties

- [OpenAPI](openapi/obie-account-info-openapi.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lloydsbanking.com/prod01/lbg/get-started)

### Lloyds Banking Group Payment Initiation API

OBIE Read/Write Payment Initiation (PIS) API for initiating domestic, scheduled, standing-order, international, and business bulk/batch payments with customer authorisation. FAPI-secured; requires developer-portal onboarding.

- **Human URL:** [https://developer.lloydsbanking.com/prod01/lbg/products](https://developer.lloydsbanking.com/prod01/lbg/products)
- **Base URL:** `https://api.lloydsbank.com/open-banking/v3.1`

#### Properties

- [OpenAPI](openapi/obie-payment-initiation-openapi.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lloydsbanking.com/prod01/lbg/get-started)

### Lloyds Banking Group Confirmation of Funds API

OBIE Read/Write Confirmation of Funds (CBPII) API allowing an authorised card-based payment instrument issuer to check whether funds are available on a customer account. FAPI-secured; requires developer-portal onboarding.

- **Human URL:** [https://developer.lloydsbanking.com/prod01/lbg/products](https://developer.lloydsbanking.com/prod01/lbg/products)
- **Base URL:** `https://api.lloydsbank.com/open-banking/v3.1`

#### Properties

- [OpenAPI](openapi/obie-confirmation-funds-openapi.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lloydsbanking.com/prod01/lbg/get-started)

### Lloyds Banking Group Variable Recurring Payments API

OBIE Variable Recurring Payments (VRP) profile API enabling consent-based recurring payments under a customer-agreed mandate, including sweeping between a customer's own accounts. FAPI-secured; requires developer-portal onboarding.

- **Human URL:** [https://developer.lloydsbanking.com/prod01/lbg/products](https://developer.lloydsbanking.com/prod01/lbg/products)
- **Base URL:** `https://api.lloydsbank.com/open-banking/v3.1`

#### Properties

- [OpenAPI](openapi/obie-vrp-openapi.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://developer.lloydsbanking.com/prod01/lbg/get-started)

### Lloyds Banking Group Event Notifications API

OBIE Event Notifications API delivering aggregated and real-time event signals to registered TPPs. FAPI-secured; requires developer-portal onboarding. Documented as a product on the developer portal.

- **Human URL:** [https://developer.lloydsbanking.com/prod01/lbg/products](https://developer.lloydsbanking.com/prod01/lbg/products)
- **Base URL:** `https://api.lloydsbank.com/open-banking/v3.1`

#### Properties

- [Documentation](https://developer.lloydsbanking.com/prod01/lbg/get-started)

## Common Properties

- [Website](https://www.lloydsbankinggroup.com/)
- [Developer Portal](https://developer.lloydsbanking.com/prod01/lbg/home)
- [Getting Started](https://developer.lloydsbanking.com/prod01/lbg/get-started)
- [Documentation](https://developer.lloydsbanking.com/prod01/lbg/products)
- [GitHub Organization](https://github.com/LloydsBanking)
- [LinkedIn](https://www.linkedin.com/company/lloyds-banking-group)
- [Blog](https://www.lloydsbankinggroup.com/insights.html)
- [Support](https://developer.lloydsbanking.com/prod01/lbg/support)
- [Privacy Policy](https://www.lloydsbankinggroup.com/privacy.html)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
