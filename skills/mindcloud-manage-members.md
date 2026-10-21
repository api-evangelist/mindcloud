---
name: mindcloud-manage-members
description: Invite, list, update, and remove company members.
api: openapi/connect-mindcloud-openapi.json
operations:
- v2-invite-member
- v2-list-members
- v2-update-member
- v2-delete-member
generated: '2026-10-20'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/connect-mindcloud-openapi.json ; every operationId checked against the contract
---

# mindcloud-manage-members

Invite, list, update, and remove company members.

## Steps

1. 1. Call `v2-invite-member` with the required `Authorization` header (apiKey) and a JSON body containing `email` (or list of emails).
2. 2. Call `v2-list-members` with the required `Authorization` header to retrieve the current members.
3. 3. Call `v2-update-member` with the required `Authorization` header, the path parameter `userId`, and a JSON body containing the new `role`.
4. 4. Call `v2-delete-member` with the required `Authorization` header and the path parameter `userId` to remove a member.

## Rules

- All requests must include the `Authorization` header using the apiKey scheme.
- The API uses standard HTTP status codes for errors (e.g., 4xx for client errors, 5xx for server errors).
