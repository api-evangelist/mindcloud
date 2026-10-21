---
name: mindcloud-manage-connection
description: Manage a connection by listing, retrieving, testing, and optionally deleting it.
api: openapi/connect-mindcloud-openapi.json
operations:
- v2-list-connections
- v2-get-connection
- v2-test-connection
- v2-delete-connection
generated: '2026-10-20'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/connect-mindcloud-openapi.json ; every operationId checked against the contract
---

# mindcloud-manage-connection

Manage a connection by listing, retrieving, testing, and optionally deleting it.

## Steps

1. 1. Use `v2-list-connections` – no parameters, returns an array of connection objects.
2. 2. Use `v2-get-connection` – path parameter `connectionId` to retrieve details of a specific connection.
3. 3. Use `v2-test-connection` – path parameter `connectionId`; request body may contain test options as defined in the contract.
4. 4. Use `v2-delete-connection` – path parameter `connectionId`; optionally include a `revoke` action in the request body as required by the contract.

## Rules

- Authentication: Include the API key in the `Authorization` header as required by the `apiKey` scheme.
- Idempotency: The `v2-delete-connection` operation is idempotent – repeated calls with the same `connectionId` have no additional effect.
- Errors: The API returns standard HTTP error codes (e.g., 404 for not‑found, 401 for unauthorized) as defined in the contract.
