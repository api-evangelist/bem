---
name: Infer a schema and build an extractor
description: Generate a JSON schema from a sample document, then create a function that extracts against it.
api: openapi/bem-openapi-original.yml
operations: [v3-infer-schema, v3-create-function, v3-get-function, v3-create-workflow]
---

# Infer a schema and build an extractor

Bootstrap a new extractor when you do not yet have a schema.

## Auth
- `x-api-key: $BEM_API_KEY`. Base URL `https://api.bem.ai/v3`.

## Steps
1. **Infer a schema** — `v3-infer-schema` (`POST /v3/infer-schema`) with a representative sample file. bem returns a JSON schema with inferred fields and types.
2. **Review & tighten** the inferred schema (strict type enforcement is a bem feature — narrow types where you can).
3. **Create the function** — `v3-create-function` (`POST /v3/functions`) using the schema as the extraction target.
4. **Verify** — `v3-get-function` (`GET /v3/functions/{functionName}`) to confirm the stored definition/version.
5. **Wire into a workflow** — `v3-create-workflow` (`POST /v3/workflows`) to chain the extractor with any downstream Classify/Parse/Enrich/Send functions.

## Conventions
- Versioning is URI-path (`/v3`); functions and workflows are versioned — pin `versionNum` for reproducibility.
- See `conventions/bem-conventions.yml` for pagination, polling cadence, and the error envelope.
