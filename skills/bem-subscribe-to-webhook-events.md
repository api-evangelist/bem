---
name: Subscribe to webhook events and verify signatures
description: Generate a webhook secret, create a subscription binding a function to your URL, and verify delivery signatures.
api: openapi/bem-openapi-original.yml
operations: [v3-generate-webhook-secret, v3-get-webhook-secret, v3-create-subscription, v3-get-subscription]
---

# Subscribe to bem webhook events

Receive terminal function events (extract, classify, parse, split, join, enrich, payload-shaping, send, error) at your endpoint instead of polling.

## Auth
- `x-api-key: $BEM_API_KEY`. Base URL `https://api.bem.ai/v3`.

## Steps
1. **Generate a signing secret** — `v3-generate-webhook-secret` (`POST /v3/webhook-secret`). Retrieve later with `v3-get-webhook-secret` (`GET /v3/webhook-secret`); rotate/revoke with `DELETE /v3/webhook-secret`.
2. **Create a subscription** — `v3-create-subscription` (`POST /v3/subscriptions`) with `name`, `type`, `functionName`, and `webhookURL`. bem POSTs each terminal event JSON to that URL.
3. **Verify each delivery** — read the `bem-signature` header (`t=<timestamp>,v1=<hex>`). Compute HMAC-SHA256 of `"{timestamp}.{raw_body}"` with your secret and constant-time compare against `v1`. Reject if the timestamp is older than ~5 minutes.
4. **Discriminate events** — the HTTP body is the event itself (no envelope); switch on `eventType`. Bodies mirror `GET /v3/outputs/{eventID}` and `GET /v3/errors/{eventID}`.
5. **Confirm the subscription** — `v3-get-subscription` (`GET /v3/subscriptions/{subscriptionID}`).

## Reference
- Full webhook surface: `asyncapi/bem-webhooks.yml`.
