# Hopstack (hopstack)

Hopstack is an AI-native, cloud-based warehouse management system (WMS) and fulfillment operations platform for warehouses, third-party logistics providers (3PLs), and e-commerce operators. It covers inbound logistics and receiving, inventory management, omnichannel order management, picking/packing/shipping, and returns, with analytics on top. Hopstack also ships pre-built integrations for ERPs (NetSuite, SAP, Odoo), e-commerce platforms (Shopify, Amazon, Magento, BigCommerce), and shipping carriers/software (FedEx, UPS, DHL, EasyPost, Shippo).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hopstack/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hopstack/refs/heads/main/apis.yml)

## Access Model (Read This First)

Hopstack **does** expose a documented, RESTful API. Its public API reference lives at [apidocs.hopstack.io/reference](https://apidocs.hopstack.io/reference) and describes programmatic access to core resources, explicitly including **orders** and **consignments**, with request parameters, response schemas, and example payloads.

However, access is **gated**, not fully open:

- **Authentication is a per-user `X-API-Key`**, generated from the Hopstack Dashboard (Username → API Keys → Create API-KEY). The key is shown once and must be stored securely (e.g., an environment variable).
- **A customer must contact Hopstack Support to enable API-key generation** in the UI before keys can be created. API access is therefore an existing-customer / partner capability rather than an open, self-service developer program.
- The **base URL, complete endpoint list, and any machine-readable OpenAPI specification** are served behind the account/partner reference and are not published as an open, scrapeable catalog. The reference site is bot-protected (returns HTTP 403 to automated fetches).

Because of this, the APIs below are documented **honestly**: **Orders** and **Consignments** are confirmed as documented API resources; **Inventory**, **Shipments**, **Products**, and **Warehouses** are modeled from Hopstack's documented WMS modules and are marked as `endpointsModeled` (their exact API paths are not confirmed in the public reference). No OpenAPI, Postman collection, or GraphQL schema is included, because none could be sourced from public material.

## Tags

- Warehouse Management
- WMS
- Fulfillment
- Logistics
- Supply Chain
- Inventory
- 3PL
- E-commerce

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Hopstack Orders API

Programmatic access to sales/fulfillment orders that flow into Hopstack's omnichannel order management and picking, packing, and shipping workflows. Confirmed as a core resource of the Hopstack REST API. Exact endpoint paths and base URL are in the account-gated reference.

- **API Reference:** [https://apidocs.hopstack.io/reference](https://apidocs.hopstack.io/reference)

### Hopstack Consignments API

Programmatic access to consignments — the inbound/receiving records that bring stock into a Hopstack-managed warehouse. Confirmed alongside orders as a core resource of the Hopstack REST API.

- **API Reference:** [https://apidocs.hopstack.io/reference](https://apidocs.hopstack.io/reference)

### Hopstack Inventory API

Inventory and stock-ledger operations across warehouses. Modeled from Hopstack's inventory management module (endpoints modeled — not confirmed in the public reference).

- **API Reference:** [https://apidocs.hopstack.io/reference](https://apidocs.hopstack.io/reference)

### Hopstack Shipments API

Shipment creation and management tied to fulfillment workflows and multi-carrier integrations. Modeled from Hopstack's shipping module (endpoints modeled — not confirmed in the public reference).

- **API Reference:** [https://apidocs.hopstack.io/reference](https://apidocs.hopstack.io/reference)

### Hopstack Products API

Product and SKU catalog management underpinning inventory and orders. Modeled from Hopstack's WMS data model (endpoints modeled — not confirmed in the public reference).

- **API Reference:** [https://apidocs.hopstack.io/reference](https://apidocs.hopstack.io/reference)

### Hopstack Warehouses API

Warehouse and location configuration for multi-warehouse, multi-client (3PL) operations. Modeled from Hopstack's warehouse management module (endpoints modeled — not confirmed in the public reference).

- **API Reference:** [https://apidocs.hopstack.io/reference](https://apidocs.hopstack.io/reference)

## Common Properties

- [Website](https://www.hopstack.io/)
- [LinkedIn](https://www.linkedin.com/company/hopstack)
- [API Docs](https://apidocs.hopstack.io/)
- [API Reference](https://apidocs.hopstack.io/reference)
- [Knowledge Base](https://help.hopstack.io/)
- [Integrations](https://www.hopstack.io/integrations)
- [Plans](plans/hopstack-plans-pricing.yml)
- [Rate Limits](rate-limits/hopstack-rate-limits.yml)
- [Fin Ops](finops/hopstack-finops.yml)

## Pricing

Hopstack does not publish list pricing. Plans are quote-based / contact-sales, typically scoped to warehouse count, order/throughput volume, modules, and 3PL client count. See `plans/hopstack-plans-pricing.yml`.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
