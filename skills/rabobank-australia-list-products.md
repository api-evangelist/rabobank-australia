---
name: Discover Rabobank Australia banking products
description: List Rabobank Australia's openly available banking products and fetch full detail for one, via the public unauthenticated CDR Product Reference Data API.
api: openapi/rabobank-australia-cds-banking-products-openapi.yml
operations: [listBankingProducts, getBankingProductDetail]
auth: none
base_url: https://openbanking.api.rabobank.com.au/public/cds-au/v1
---

# Discover Rabobank Australia banking products

Rabobank Australia exposes its product catalogue through the Consumer Data Right
(CDR) Product Reference Data API. It is **public and unauthenticated** — no API
key or token is needed. You MUST send the `x-v` version header.

## Rules
- Always send request header `x-v: 4`. Omitting it returns HTTP 400
  `urn:au-cds:error:cds-all:Header/Missing`; sending `x-v: 1/2/3` returns HTTP 406
  `urn:au-cds:error:cds-all:Header/UnsupportedVersion`.
- Errors come back as `{ "errors": [ { "code", "title", "detail" } ] }` (CDS
  format, not RFC 9457). See `errors/rabobank-australia-problem-types.yml`.
- Paginate with `page` and `page-size`; read `meta.totalRecords` / `meta.totalPages`
  and follow `links.next` (confirmed live: 34 products across 34 pages at page-size 1).
- Correlate requests via the `x-fapi-interaction-id` response header.

## Steps

1. **List products** — `listBankingProducts`
   `GET /banking/products` with header `x-v: 4`.
   Optional query filters: `effective` (CURRENT|FUTURE|ALL), `updated-since`,
   `brand`, `product-category`, `page`, `page-size`.
   Read `data.products[]` (each has `productId`, `productCategory`, `name`,
   `description`, `brand`, `applicationUri`).

2. **Get product detail** — `getBankingProductDetail`
   For a chosen `productId`, `GET /banking/products/{productId}` with header
   `x-v: 4`. Returns full `rates`, `fees`, `features`, `eligibility`,
   `constraints`, and `additionalInformation` for that product.

## Notes
This is the only public surface. Authenticated CDR data sharing (accounts,
balances, transactions) requires CDR accreditation as a data recipient and is
not callable with this skill.
