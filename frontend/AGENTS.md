# Frontend AGENTS.md

## Scope

This area contains the reusable frontend library, the admin app, and consuming app adapters.

## Build Order

1. Shared models and service layer
2. Reusable library shell
3. Issue dialog
4. UAT panel
5. Evidence upload flow
6. Export preview
7. Admin app worklists
8. Consuming app adapter
9. Jira result handling

## Rules

- Keep shared UI app-agnostic.
- Use adapters for app-specific context mapping.
- Do not hardcode business app logic into shared components.
- Trigger Jira creation through backend actions only.
- Update contracts when request or response shapes change.
