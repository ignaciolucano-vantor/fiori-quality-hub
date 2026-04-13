# Fiori Quality Hub

Reusable UAT, issue reporting, evidence capture, AI-ready export, and optional Jira ticket creation for SAP Fiori apps.

## Repository Purpose

This repository organizes the MVP1 implementation of Fiori Quality Hub as an agent-first project.

The repository is designed for:
- SAP S/4HANA backend work in Eclipse and ADT
- UI5 frontend work in VS Code
- agent-assisted development with Augment and ChatGPT/Codex
- reusable integration across multiple Fiori apps

## MVP1 Scope

In scope:
- App registry
- Issue reporting
- Evidence attachment
- UAT Mode Lite
- UAT case maintenance
- User assignment
- Execution status update
- Copy and paste data boxes
- Create issue from failed test
- AI export v1
- Optional Jira ticket creation extension

Out of scope:
- Advanced step-level analytics
- Full retest workflow
- Complex approval workflow
- Bi-directional sync from Jira back to SAP
- Heavy executive dashboards

## Repository Structure

```text
.
├── AGENTS.md
├── README.md
├── .augment/
│   └── rules/
├── docs/
│   ├── architecture/
│   ├── product/
│   ├── contracts/
│   └── agents/
├── backend/
└── frontend/
```

## Working Model

- GitHub repository is the technical source of truth.
- Markdown files are the living documentation.
- GitHub Project is used for execution and tracking.
- Confluence is used for overview, onboarding, and stakeholder visibility.

## Recommended Branch Model

- `main` for reviewed code and approved documentation
- `feature/<capability-name>` for focused implementation work
- `docs/<topic>` for documentation-only updates when needed

## Initial Capability Order

1. Documentation and agent setup
2. RAP persistence and contracts
3. RAP service exposure
4. Reusable frontend library
5. Admin app
6. Consuming app adapter
7. Jira extension
8. Demo hardening

## Suggested Labels

- `scope:mvp1`
- `area:backend`
- `area:frontend`
- `area:docs`
- `area:jira`
- `area:agent-ops`
- `priority:high`
- `priority:medium`
- `priority:low`
- `demo-blocker`

## Done Criteria

A change is only complete when:
- code is committed
- documentation is updated
- contract changes are reflected in docs/contracts
- test notes are added
- demo impact is stated if applicable
