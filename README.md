# Bem

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

Bem is the production layer for unstructured data. Its API turns inbound documents — PDFs, images, video, audio, and email — into structured JSON against a schema you define, using versioned, LLM-powered functions (extract, classify, parse, split, join, enrich, payload-shaping, and send) composed into reusable workflows. Bem automates document-heavy tasks such as invoice handling, claims adjudication, and data onboarding, with automatic schema inference, strict type enforcement, confidence scoring and drift detection, human-in-the-loop review, webhooks, and a knowledge graph. It offers US and EU regional endpoints, official SDKs, a CLI, a Terraform provider, and an MCP server, and is SOC 2 Type II, HIPAA, and GDPR compliant.

**Areas:** Company · Document Processing · Unstructured Data · Data Extraction · Artificial Intelligence · LLM · ETL · Schema Inference · Webhook

## Bem on APIs.io

Everything profiled for Bem is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bem/](https://apis.io/providers/bem/)** — or go straight to one of the APIs or properties below.

### APIs (22)

- [Bem Buckets API](https://apis.io/apis/bem/bem-buckets-api/) — Buckets are named partitions of the knowledge graph within an account+environment. Entities, mentions, and relations are scoped to a bucket so a single…
- [Bem Calls API](https://apis.io/apis/bem/bem-calls-api/) — The Calls API provides a unified interface for invoking both **Workflows** and **Functions**. Use this API when you want to: - Execute a complete workflow…
- [Bem Collections API](https://apis.io/apis/bem/bem-collections-api/) — Collections are named groups of embedded items used by Enrich functions for semantic search. Each collection is referenced by a `collectionName`, which…
- [Bem Connectors API](https://apis.io/apis/bem/bem-connectors-api/) — Connectors are integrations that trigger a Bem workflow from an external system. A connector binds an inbound source — currently Box or a Paragon-managed…
- [Bem Entity Bulk Seed API](https://apis.io/apis/bem/bem-entity-bulk-seed-api/) — Seed the knowledge graph with a batch of customer-authored canonical entities in one request — their types, descriptions, synonyms, and per-entity…
- [Bem Entity Curation API](https://apis.io/apis/bem/bem-entity-curation-api/) — Curate the knowledge graph by transitioning entities through their review lifecycle and editing their metadata. - **`PATCH /v3/entities/{id}`** updates a…
- [Bem Entity Synonyms API](https://apis.io/apis/bem/bem-entity-synonyms-api/) — Manage the human-readable surface forms (synonyms) attached to a canonical entity. Synonyms feed the matcher's exact-match path, so adding the right…
- [Bem Entity Type Reviewers API](https://apis.io/apis/bem/bem-entity-type-reviewers-api/) — Reviewer assignments link users to the entity types they are responsible for reviewing, scoped to an account+environment. These are dashboard-only…
- [Bem Entity Types API](https://apis.io/apis/bem/bem-entity-types-api/) — Entity Types are the customer-defined taxonomy for the knowledge graph, scoped to an account+environment. Each type has a unique, immutable name and can be…
- [Bem Errors API](https://apis.io/apis/bem/bem-errors-api/) — Retrieve terminal error events from workflow calls. Errors are events produced by function steps that failed during processing. A single workflow call may…
- [Bem Feedback API](https://apis.io/apis/bem/bem-feedback-api/) — Submit training corrections for `extract`, `classify`, and `join` events. Feedback is event-centric — each correction is attached to an event by its…
- [Bem Function Accuracy API](https://apis.io/apis/bem/bem-function-accuracy-api/) — Monitor, evaluate, and iterate on the quality of every function in your environment. Function Accuracy bundles two complementary loops: ## Evaluations…
- [Bem Functions API](https://apis.io/apis/bem/bem-functions-api/) — Functions are the core building blocks of data transformation in Bem. Each function type serves a specific purpose: - **Extract**: Extract structured JSON…
- [Bem Knowledge Graph API](https://apis.io/apis/bem/bem-knowledge-graph-api/) — Read the cross-document knowledge graph — the canonical entities and the directed relations between them that the Parse pipeline populates when…
- [Bem Outputs API](https://apis.io/apis/bem/bem-outputs-api/) — Retrieve terminal non-error output events from workflow calls. Outputs are events produced by successful terminal function steps — steps that completed…
- [Bem Review Queue API](https://apis.io/apis/bem/bem-review-queue-api/) — The reviewer-facing read surface for entity curation, available on the dashboard (JWT) only. - **`GET /v3/review-queue`** returns a cursor-paginated set of…
- [Bem Schema Inference API](https://apis.io/apis/bem/bem-schema-inference-api/) — Infer JSON Schemas from uploaded documents using AI. Upload a file (PDF, image, spreadsheet, email, etc.) and receive a general-purpose JSON Schema that…
- [Bem Subscriptions API](https://apis.io/apis/bem/bem-subscriptions-api/) — Subscriptions wire up notifications for the events your functions and collections produce. Most subscriptions target a single function (by `functionName` or…
- [Bem Views API](https://apis.io/apis/bem/bem-views-api/) — Views are tabular projections over the `transformations` your functions produce — a saved query that turns raw extracted JSON into a filterable,…
- [Bem Webhooks API](https://apis.io/apis/bem/bem-webhooks-api/) — bem POSTs a JSON event to your configured webhook URL each time a subscribed function call, workflow output, or collection-processing job fires. This…
- [Bem Workflows API](https://apis.io/apis/bem/bem-workflows-api/) — Workflows orchestrate one or more functions into a directed acyclic graph (DAG) for document processing. Use these endpoints to create, update, list, and…
- [Bem Filesystem API](https://apis.io/apis/bem/bem-filesystem-api/) — Unix-shell-style nav over parsed documents and the cross-doc memory store.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Bem Webhooks](https://apis.io/asyncapis/bem/bem-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [bem](https://apis.io/servers/bem/bem/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Bem Agentic Access](https://apis.io/agentic-access/bem/bem-agentic-access/)

#### Collections (20)

Postman and Open Collection request collections.

- [Bem Buckets API](https://apis.io/collections/bem/open-bem-buckets-api/)
- [Bem Buckets Calls API](https://apis.io/collections/bem/open-bem-calls-api/)
- [Bem Buckets Collections API](https://apis.io/collections/bem/open-bem-collections-api/)
- [Bem Buckets Connectors API](https://apis.io/collections/bem/open-bem-connectors-api/)
- [Bem Buckets Entity Bulk Seed API](https://apis.io/collections/bem/open-bem-entity-bulk-seed-api/)
- [Bem Buckets Entity Curation API](https://apis.io/collections/bem/open-bem-entity-curation-api/)
- [Bem Buckets Entity Synonyms API](https://apis.io/collections/bem/open-bem-entity-synonyms-api/)
- [Bem Buckets Entity Types API](https://apis.io/collections/bem/open-bem-entity-types-api/)
- [Bem Buckets Errors API](https://apis.io/collections/bem/open-bem-errors-api/)
- [Bem Buckets Feedback API](https://apis.io/collections/bem/open-bem-feedback-api/)
- [Bem Buckets File System API](https://apis.io/collections/bem/open-bem-file-system-api/)
- [Bem Buckets Function Accuracy API](https://apis.io/collections/bem/open-bem-function-accuracy-api/)
- [Bem Buckets Functions API](https://apis.io/collections/bem/open-bem-functions-api/)
- [Bem Buckets Knowledge Graph API](https://apis.io/collections/bem/open-bem-knowledge-graph-api/)
- [Bem Buckets Outputs API](https://apis.io/collections/bem/open-bem-outputs-api/)
- [Bem Buckets Schema Inference API](https://apis.io/collections/bem/open-bem-schema-inference-api/)
- [Bem Buckets Subscriptions API](https://apis.io/collections/bem/open-bem-subscriptions-api/)
- [Bem Buckets Views API](https://apis.io/collections/bem/open-bem-views-api/)
- [Bem Buckets Webhooks API](https://apis.io/collections/bem/open-bem-webhooks-api/)
- [Bem Buckets Workflows API](https://apis.io/collections/bem/open-bem-workflows-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Bem Openapi Overlay](https://apis.io/overlays/bem/bem-openapi-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Bem Authentication](https://apis.io/security/bem/bem-authentication/)
- [Bem Domain Security](https://apis.io/security/bem/bem-domain-security/)
- [Bem Trust Center](https://apis.io/security/bem/bem-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Bem Plans Pricing](https://apis.io/plans/bem/bem-plans-pricing/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://bem.ai)
- [Documentation](https://docs.bem.ai)
- [Getting started](https://docs.bem.ai/guide/quickstart)
- [API reference](https://docs.bem.ai/api/v3/authentication)
- [Pricing](https://www.bem.ai/pricing)
- [Sign up](https://app.bem.ai/auth/sign-up)
- [Blog](https://www.bem.ai/log)
- [Compliance](https://www.bem.ai/security)
- [Trust centre](https://trust.bem.ai)
- [Terms of service](https://www.bem.ai/terms)
- [Privacy policy](https://www.bem.ai/privacy)
- [GitHub](https://github.com/bem-team)
- [Status](https://status.bem.ai)

## API Evangelist rating

**Kin Score 66.7** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 71.7 |
| Contract quality | 57.2 |
| Contract governance | 18.2 |
| Operational transparency | 34.2 |
| Developer ergonomics | 69.6 |
| Access clarity | 78.9 |

**Agent readiness 40.8** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bem/](https://apis.io/providers/bem/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Bem: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bem/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
