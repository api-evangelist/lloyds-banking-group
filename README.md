# Lloyds Banking Group (lloyds-banking-group)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
