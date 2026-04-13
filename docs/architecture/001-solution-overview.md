# Solution Overview

## Objective

Fiori Quality Hub is a reusable framework for SAP Fiori apps that centralizes:
- issue reporting
- UAT execution support
- evidence collection
- AI-ready remediation export
- optional Jira ticket creation

## Core Components

### 1. Central RAP Backend

The backend owns framework persistence, business rules, service exposure, export generation, and optional Jira posting.

### 2. Reusable Embedded Frontend Library

The embedded library provides:
- launch entry point
- issue dialog
- UAT panel
- copy and paste boxes
- evidence capture hooks
- export preview

### 3. Central Admin App

The admin app provides:
- worklists
- issue review
- execution review
- case maintenance
- assignment monitoring
- Jira trace visibility

## Design Principles

- Separate framework data from source app business data.
- Keep integration lightweight for consuming apps.
- Capture controlled diagnostics only.
- Preserve auditability and traceability.
- Keep MVP1 demoable and focused.

## Consuming App Contract

Every consuming app should provide a compact context payload with:
- appId
- appName
- route
- sourceObjectType
- sourceObjectId
- client
- selected business attributes relevant to the object

## Payment Request Integration Rule

Payment Request remains the owner of Payment Request business logic and process data.
Fiori Quality Hub only consumes Payment Request context.
