# Frontend Architecture

## Scope

This document defines the frontend design for MVP1.

## Frontend Deliverables

### 1. Reusable Embedded Library

Suggested package name: `zfq-lib`

Capabilities:
- launcher
- issue dialog
- UAT panel
- copy box
- evidence capture
- export preview
- context provider interface

### 2. Central Admin App

Suggested package name: `zfq-admin`

Capabilities:
- My Assigned Cases
- My Open Issues
- Failed Executions
- Issue details
- Execution details
- Case maintenance
- Assignment review
- Jira trace display

### 3. Consuming App Adapter

Suggested package name: `zfq-paymentrequest-adapter`

Purpose:
- map app-specific context into the shared payload
- inject launch entry point
- keep source app changes minimal

## Frontend Rules

- Keep service access behind a dedicated data layer.
- Do not hardcode app-specific field names in shared components.
- Keep Jira creation as a backend-triggered action.
- Show user-friendly status, technical IDs, and links where available.
- Keep UX centered on MVP1 flows only.

## Suggested Structure

```text
frontend/
  packages/
    zfq-lib/
    zfq-admin/
    zfq-paymentrequest-adapter/
```

## Required Shared Models

- App context payload model
- Issue creation model
- UAT execution model
- Evidence upload model
- Jira result model

## Error Handling

Frontend should show:
- friendly user message
- technical reference if returned by backend
- retry guidance when the action is safe to retry
