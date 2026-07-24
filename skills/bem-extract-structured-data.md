---
name: Extract structured data from a document
description: Define an extraction function and workflow, call it against a file, and read the structured JSON output.
api: openapi/bem-openapi-original.yml
operations: [v3-create-function, v3-create-workflow, v3-call-workflow, v3-get-call, v3-get-output]
---

# Extract structured data from a document with bem

Turn an inbound document into structured JSON against a schema you define.

## Auth
- Send `x-api-key: $BEM_API_KEY` on every request (SDKs/CLI read `BEM_API_KEY` from the environment).
- Base URL: `https://api.bem.ai` (US) or `https://api.eu1.bem.ai` (EU). All endpoints live under `/v3`.

## Steps
1. **Create an extract function** — `v3-create-function` (`POST /v3/functions`). Provide the output JSON schema you want extracted. Use `v3-infer-schema` first if you need a schema from a sample document.
2. **Create a workflow** — `v3-create-workflow` (`POST /v3/workflows`) that chains the function(s) into a DAG.
3. **Call the workflow** — `v3-call-workflow` (`POST /v3/workflows/{workflowName}/call`) with the file. Set `wait=true` to hold up to 30s for a synchronous `200`; otherwise you get `202` and poll or use webhooks.
4. **Fetch results** — poll `v3-get-call` (`GET /v3/calls/{callID}`) until terminal, then read outputs via `v3-get-output` (`GET /v3/outputs/{eventID}`). Note `call.outputs` and `call.errors` are not mutually exclusive.

## Idempotency & retries
- Pass a deterministic `callReferenceID` (e.g. the document UUID) so retried calls dedupe instead of duplicating.
- Retry `408/429/5xx` with exponential backoff; do not retry `400/401/404/422`.

## Errors
- Error envelope is custom JSON `{ message, code, details }` (not RFC 9457). See `errors/bem-problem-types.yml`.
