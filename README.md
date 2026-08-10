# AI Customer Support Workflow

A small AI-assisted customer support workflow demonstrating practical automation, structured problem solving, escalation, and documentation.

## Project Goal

This project demonstrates how AI can assist a customer support team with repetitive tasks while keeping a human in control of decisions that require judgment, additional information, or escalation.

## Workflow

Customer Request
↓
Capture & Normalize Request
↓
Classify Request + Detect Urgency
↓
Check Available Knowledge
↓
AI Drafts Response
↓
Confidence / Risk Check
↓
High Confidence → Response Review → Customer
↓
Low Confidence / Sensitive → Human Escalation
↓
Document Outcome
↓
Create Follow-Up Task if Needed

## Example Categories

- Billing and payments
- Account access
- Product questions
- Technical issues
- Order or request status
- Complaints and escalations

## Example

**Customer request:**

"I submitted my request three days ago and haven't received an update. Can you tell me what's happening?"

**Category:** Request status

**Priority:** Normal

**AI action:** Review the available status information and prepare a concise customer-facing response.

**Human review:** Required if the information is incomplete, contradictory, or involves a sensitive case.

**Documentation:** Record the customer request, action taken, response, and any follow-up date.

## AI Prompt

```text
You are a customer support assistant.

Analyze the customer request and return:

1. Category
2. Urgency: Low, Normal, High, or Critical
3. Key issue
4. Recommended next action
5. Draft customer response
6. Whether human review is required

Rules:

- Do not invent account, order, billing, or case information.
- If required information is missing, identify what is missing.
- Escalate sensitive, high-risk, or unclear cases.
- Keep the customer response professional, clear, and concise.
Category: Request status
Urgency: Normal

Key issue:
Customer is requesting an update on a previously submitted request.

Recommended action:
Verify the current request status before responding.

Human review:
No, unless the status information is unavailable or contradictory.

Draft response:
Thank you for reaching out. I understand you're looking for an update on your request. I'll review the current status and make sure you receive the most accurate information. If anything further is needed from you, I'll let you know.
