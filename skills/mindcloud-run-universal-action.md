---
name: mindcloud-run-universal-action
description: Execute a Universal API action by discovering the app, its actions, retrieving the action schema, and then running the action.
api: openapi/connect-mindcloud-openapi.json
operations:
- v2-list-universal-apps
- v2-list-universal-actions
- v2-get-universal-action
- v2-run-universal-action
generated: '2026-10-20'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/connect-mindcloud-openapi.json ; every operationId checked against the contract
---

# mindcloud-run-universal-action

Execute a Universal API action by discovering the app, its actions, retrieving the action schema, and then running the action.

## Steps

1. 1. `v2-list-universal-apps` – no parameters; returns available app slugs.
2. 2. `v2-list-universal-actions` – path parameter `appSlug`; returns action slugs for the chosen app.
3. 3. `v2-get-universal-action` – path parameters `appSlug`, `actionSlug`; returns argument schema needed for the run.
4. 4. `v2-run-universal-action` – path parameters `appSlug`, `actionSlug`; request body contains the action arguments as defined by the schema.

## Rules

- Include an `X-API-Key` header with your API key for authentication (apiKey scheme, http).
- The POST `/run` operation is not idempotent; do not automatically retry without handling the response.
