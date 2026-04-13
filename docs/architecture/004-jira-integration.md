# Jira Integration

## Objective

Allow Fiori Quality Hub to create Jira records automatically from an Issue or a failed UAT Execution.

## Supported Modes

### Mode A: Normal Jira Issue
Use Jira Platform issue creation for standard Jira projects.

### Mode B: JSM Request
Use Jira Service Management request creation for support portal flows.

## MVP1 Design Rules

- Jira posting is optional and controlled per consuming app.
- Payload generation happens on the backend.
- Secrets must not be stored in application tables.
- No bi-directional synchronization in MVP1.
- SAP remains the source for framework status.

## Configuration Model

Recommended app-level settings:
- JIRA_MODE
- JIRA_BASE_URL
- JIRA_PROJECT_KEY
- JIRA_ISSUE_TYPE
- JIRA_PRIORITY_DEFAULT
- JSM_SERVICE_DESK_ID
- JSM_REQUEST_TYPE_ID
- AUTO_CREATE_ON_SUBMIT
- AUTO_CREATE_ON_FAIL

## Backend Responsibilities

- build normalized Jira payload from issue or execution context
- validate required fields
- call the configured Jira endpoint
- store ticket key and response status in ZFQ_JIRA_LINK
- return link data to the frontend

## Frontend Responsibilities

- trigger backend action
- show posting status
- show Jira key and URL after success
- show clear error if creation fails

## Required Audit Fields

Store at least:
- source type
- source UUID
- Jira mode
- Jira key
- Jira URL
- request timestamp
- created by
- creation status
- response summary

## Security Notes

- Use technical configuration outside application persistence for secrets.
- Mask sensitive technical details in user-facing messages.
- Log enough detail for support review without exposing secrets.
