# RAP Architecture

## Scope

This document defines the MVP1 RAP model.

## Persistence Objects

Recommended MVP1 persistence:
- ZFQ_APP
- ZFQ_APP_CTXMAP
- ZFQ_ISSUE_H
- ZFQ_ISSUE_CTX
- ZFQ_EVID_H
- ZFQ_EVID_C
- ZFQ_UAT_CASE_H
- ZFQ_UAT_CASE_S
- ZFQ_UAT_ASGN
- ZFQ_UAT_EXEC_H
- ZFQ_EXPORT_LOG
- ZFQ_JIRA_LINK

## RAP Business Objects

### App Registry
- register consuming apps
- enable or disable features
- control Jira integration mode

### Issue
- create issue
- submit issue
- attach evidence
- generate AI export
- create Jira ticket

### UAT Case
- maintain case header
- maintain case steps

### UAT Assignment
- assign users to cases
- track due date and assignment status

### UAT Execution
- start execution
- mark passed
- mark failed
- mark blocked
- complete execution
- create linked issue
- create Jira ticket

## Recommended Actions

### Issue
- Submit
- Assign
- Close
- Reopen
- GenerateAIExport
- GenerateJiraPayload
- CreateJiraCase

### UAT Execution
- StartExecution
- MarkPassed
- MarkFailed
- MarkBlocked
- CompleteExecution
- CreateIssueFromExecution
- GenerateJiraPayload
- CreateJiraCase

## Services

- Service Definition: ZUI_FQ_SRVDEF
- Service Binding: ZUI_FQ_SRVBND
- Protocol: OData V4

## Supporting Classes

- ZCL_FQ_CTX_COLLECTOR
- ZCL_FQ_ISSUE_SERVICE
- ZCL_FQ_UAT_SERVICE
- ZCL_FQ_EVID_SERVICE
- ZCL_FQ_EXPORT_SERVICE
- ZCL_FQ_AUTH_SERVICE
- ZCL_FQ_JIRA_SERVICE

## Implementation Notes

- Prefer managed RAP non-draft for MVP1.
- Keep binary evidence handling behind a service class.
- Keep Jira request generation and HTTP posting on the backend.
- Expose only MVP1 entities and actions.
