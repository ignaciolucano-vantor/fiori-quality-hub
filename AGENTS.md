# AGENTS.md

## Project Mission

Build MVP1 of Fiori Quality Hub as a reusable SAP Fiori framework for:
- issue reporting
- UAT Mode Lite
- evidence capture
- AI-ready export
- optional Jira ticket creation

## Architecture Rules

- Keep one central RAP service domain.
- Keep one reusable embedded frontend library.
- Keep one central admin frontend app.
- Treat business app data as external context, not owned persistence.
- Do not duplicate Payment Request business logic.
- Do not implement MVP2 or MVP3 objects unless explicitly approved.

## SAP Scope

The implementation is restricted to:
- SAP_BASIS 756 SP02
- SAP_ABA 75G SP02
- SAP_GWFND 756 SP02
- SAP_UI 756 SP03

Functional scope is restricted to:
- BASIS
- ABAP
- Fiori
- CDS
- FI
- MM
- GTS

## Delivery Rules

- Prefer small, reviewable pull requests.
- Update documentation when changing contracts, payloads, or architecture.
- Keep naming consistent across RAP and frontend.
- Keep security-sensitive values out of application tables.
- Treat Jira integration as a controlled extension of MVP1.

## MVP1 In Scope

- App registry
- Issue reporting
- Evidence attachment
- UAT Mode Lite
- UAT case maintenance
- Assignment
- Execution header persistence
- Copy and paste data boxes
- AI export v1
- Jira ticket creation extension

## MVP1 Out of Scope

- Full campaign analytics
- Advanced step result analytics
- Complex workflow approvals
- Cross-system synchronization from Jira back to SAP
- Heavy dashboarding

## Build Sequence

1. Create docs and agent rules
2. Define contracts and payloads
3. Implement RAP persistence
4. Implement RAP CDS and behavior
5. Expose RAP service
6. Build reusable frontend library
7. Build admin app
8. Build consuming app adapter
9. Add Jira integration
10. Prepare demo assets

## Quality Gates

Do not mark work as done unless:
- documentation is updated
- field names are aligned across backend and frontend
- error handling is explicit
- security assumptions are documented
- a demo path exists for the implemented capability
