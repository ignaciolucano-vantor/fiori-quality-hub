# Backend AGENTS.md

## Scope

This area contains RAP backend artifacts for Fiori Quality Hub.

## Build Order

1. Dictionary objects
2. CDS interface views
3. CDS projection views
4. Behavior definitions
5. Behavior implementations
6. Service definition and binding
7. Supporting ABAP classes
8. Test data and validation notes

## Rules

- Keep RAP implementation compatible with the target SAP release.
- Prefer managed RAP non-draft for MVP1.
- Expose only MVP1 entities and actions.
- Keep Jira HTTP integration server-side.
- Do not store secrets in application persistence.
- Document field mappings when entity shapes change.
