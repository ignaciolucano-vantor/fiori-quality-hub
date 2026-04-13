# App Context Payload

## Purpose

Define the shared payload that consuming apps send into the framework.

## Mandatory Fields

```json
{
  "appId": "PAYMENT_REQUEST",
  "appName": "Payment Request",
  "route": "ObjectPage/12345",
  "sourceObjectType": "PaymentRequest",
  "sourceObjectId": "12345",
  "client": "100"
}
```

## Recommended Optional Fields

```json
{
  "semanticObject": "PaymentRequest",
  "action": "display",
  "section": "Coding",
  "processStatus": "IN_PROGRESS",
  "filterValues": {
    "CompanyCode": "1000"
  },
  "businessAttributes": {
    "PR_ID": "12345",
    "VIM_DOCID": "90001234",
    "BUKRS": "1000",
    "LIFNR": "100234",
    "REQUESTER": "IGNACIO",
    "REQUESTER_STATUS": "CONFIRMED",
    "COD_COMPLETE_FLG": true
  },
  "lastAppError": {
    "message": "Sample controlled error text",
    "code": "FQH_DEMO_001"
  }
}
```

## Rules

- Consuming apps should send only controlled, relevant context.
- Source apps remain owners of their business logic and persistence.
- Sensitive values must be reviewed before inclusion.
