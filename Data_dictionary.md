# Data Dictionary

This document explains the fields used in the Customer Support Intent Classification dataset.

| Field | Description | Example |
|---|---|---|
| ID | Unique identifier assigned to each customer message | 1 |
| CUSTOMER MESSAGE | The original customer support message being classified | "I forgot my password and can't log into my account" |
| INTENT | The primary reason for the customer's contact | Password Reset |
| CONFIDENCE | Confidence level assigned to the annotation | High |
| REASON | Brief explanation supporting the selected intent | "The customer has password issues logging into account" |

## Annotation Notes

- Each customer message receives one primary intent.
- Intent labels are selected from the predefined annotation categories.
- Confidence reflects how clearly the message matches the selected intent.
- The reason field documents the logic behind the annotation decision.
