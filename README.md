# Rabobank Australia (rabobank-australia)

Rabobank Australia is the Australian arm of Rabobank Group, the Netherlands-headquartered cooperative bank and one of the world's leading food and agribusiness specialist lenders. In Australia it operates as an Authorised Deposit-taking Institution (ADI), offering rural and agribusiness finance alongside consumer online savings accounts and term deposits, including SMSF products. As a member-focused, cooperatively owned institution, its Australian retail and business deposit products fall under the Consumer Data Right (CDR / Open Banking), so Rabobank exposes a public, unauthenticated Product Reference Data (PRD) API conforming to the Data Standards Body (DSB) Consumer Data Standards, while authenticated consumer data sharing follows the CDR accredited data recipient (ADR) model.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/rabobank-australia/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/rabobank-australia/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Agribusiness
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Rabobank Australia CDR Product Reference Data API

Public, unauthenticated Consumer Data Right Product Reference Data (PRD) API listing Rabobank Australia's openly available banking products (transaction and savings accounts, term deposits including SMSF). Confirmed live at `GET /banking/products` (HTTP 200, `x-v` 4, 34 products) conforming to the DSB Consumer Data Standards Banking API.

- **Human URL:** [https://www.rabobank.com.au/support/open-banking](https://www.rabobank.com.au/support/open-banking)
- **Base URL:** `https://openbanking.api.rabobank.com.au/public/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Products

#### Properties

- [Documentation](https://www.rabobank.com.au/support/open-banking)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-products)
- [OpenAPI](openapi/rabobank-australia-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Rabobank Australia CDR Product Detail API

Public, unauthenticated Consumer Data Right endpoint returning the full detail for a single Rabobank Australia banking product (rates, fees, features, eligibility, constraints) at `GET /banking/products/{productId}`, conforming to the DSB Consumer Data Standards Banking API.

- **Human URL:** [https://www.rabobank.com.au/support/open-banking](https://www.rabobank.com.au/support/open-banking)
- **Base URL:** `https://openbanking.api.rabobank.com.au/public/cds-au/v1`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking
- Product Detail

#### Properties

- [Documentation](https://www.rabobank.com.au/support/open-banking)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/#get-product-detail)
- [OpenAPI](openapi/rabobank-australia-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.rabobank.com.au/)
- [Developer Portal](https://openbanking.api.rabobank.com.au/ob/)
- [Documentation](https://www.rabobank.com.au/support/open-banking)
- [Support](https://www.rabobank.com.au/support/faqs/open-banking)
- [LinkedIn](https://au.linkedin.com/company/rabobankaustralia)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
