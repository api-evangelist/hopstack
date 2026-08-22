# Hopstack (hopstack)

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
