# UAT Runbook — Product-5 (Customer Notifications & Messaging)

## Feature
Notification queuing and template dispatch

## Preconditions
- Service is configured with valid environment (`.env.local` or `.env.example`).
- Database migrations have been applied via `make migrate`.
- Required port is free and accessible.

## Steps
1. Start Product-5 on port 8085
2. Submit notification request via POST /api/v1/notifications
3. Retrieve notification status via GET /api/v1/notifications

## Expected Results
- Notification is queued with recipient, subject, and message content
- Notification record status is recorded as 'queued' or 'sent'

---
*Author: QA & Primary Owner (MasterSpec Section 31.1, Section 33.1)*
*Verification Contract: `verification/contract.yaml`*
