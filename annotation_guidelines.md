annotation_guidelines.md
# Annotation Guidelines

## Project: Customer Support Intent Classification

### Purpose

These guidelines define how customer support messages should be classified into predefined intent categories.

The goal is to assign one primary intent to each customer message based on the customer's main reason for contacting support.

---

## General Annotation Rules

1. Read the entire customer message before assigning a label.
2. Identify the customer's primary reason for contacting support.
3. Assign only one primary intent per message.
4. Do not classify based solely on individual keywords.
5. Consider the context and meaning of the complete message.
6. When two categories appear possible, choose the category that best represents the customer's main request.
7. Use the confidence rating to indicate how certain the annotation decision is.

---

## Intent Categories

### 1. Billing

Use when the customer is asking about or reporting:

- Charges
- Payments
- Duplicate charges
- Fees
- Payment methods
- Billing-related issues

**Example:**

"I was charged twice for the same order."

**Label:** Billing

---

### 2. Account Access

Use when the customer cannot access, log into, or manage their account and no more specific category applies.

**Example:**

"My account is locked and I can't access it."

**Label:** Account Access

---

### 3. Password Reset

Use when the customer specifically needs to reset, recover, or change a forgotten password.

**Example:**

"I forgot my password and can't log into my account."

**Label:** Password Reset

---

### 4. Cancellation

Use when the customer wants to cancel an order, service, or subscription.

**Example:**

"I want to cancel my order before it ships."

**Label:** Cancellation

---

### 5. Delivery

Use when the customer is asking about delivery, shipping, package arrival, or delivery time.

**Example:**

"How long will it take for my package to arrive?"

**Label:** Delivery

---

### 6. Refund

Use when the customer is asking about money being returned after a purchase, return, or cancellation.

**Example:**

"I returned my order two weeks ago. When will I receive my money back?"

**Label:** Refund

---

### 7. Technical Issue

Use when the customer reports a technical problem involving an application, website, device, or system.

**Example:**

"The app keeps crashing whenever I try to open it."

**Label:** Technical Issue

---

### 8. General Question

Use when the customer is requesting general information and the message does not clearly fit another category.

**Example:**

"I need help understanding how your subscription works."

**Label:** General Question

---

## Confidence Guidelines

### High

Use when the customer's intent is clear and there is little or no reasonable ambiguity.

### Medium

Use when the intended category is likely but another category could reasonably apply.

### Low

Use when the message is ambiguous or there is insufficient information to confidently determine the primary intent.

---

## Handling Ambiguous Cases

### Account Management

If a customer asks about changing information associated with their account and there is no specific account-management category available, use **Account Access**.

Example:

"Can I change the email address associated with my account?"

**Label:** Account Access

**Confidence:** High

---

### Payment Information vs Billing Problem

Questions about accepted payment methods may be classified as **Billing**, even when the customer is not reporting a billing problem.

Example:

"What payment methods do you accept?"

**Label:** Billing

**Confidence:** Medium

If the message is purely informational and does not relate to payment, consider **General Question**.

---

## Quality Control

After completing the annotations, the dataset should be reviewed for:

- Incorrect labels
- Missing labels
- Missing confidence ratings
- Inconsistent reasoning
- Duplicate records
- Ambiguous cases
- Typographical errors

The final dataset should contain one consistent primary intent for each customer message.
