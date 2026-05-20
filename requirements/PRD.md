# SentinelX — Product Requirements Document (PRD)

## 1. Product Overview

### Product Name

SentinelX

### Product Type

Deterministic Fintech/E-commerce Platform

### Purpose

SentinelX is an enterprise-style fintech/e-commerce platform designed as a System Under Test (SUT) for advanced QA automation, API testing, CI/CD validation, and distributed-system testing demonstrations.

---

## 2. Business Objectives

- Provide realistic e-commerce and fintech workflows
- Support deterministic automation testing
- Support role-based business operations
- Simulate real-world payment scenarios
- Support CI/CD and containerized deployments
- Enable scalable API and UI automation

---

## 3. User Roles

| Role | Description |
|---|---|
| CUSTOMER | Purchases products/services and creates support tickets |
| ADMIN | Manages platform operations |
| SUPPORT | Handles customer support tickets |

---

## 4. Core Functionalities

### Customer Features

- Register account
- Login/logout
- Reset password
- Browse/search products
- Manage shopping cart
- Checkout orders
- Simulate payments
- View orders and transactions
- Create support tickets
- Track ticket status

### Admin Features

- Manage users
- Manage products
- Manage payments
- Manage transactions
- Manage support tickets
- Manage order statuses
- View dashboard statistics

### Support Features

- View support tickets
- Assign tickets
- Update ticket statuses
- Respond to customers

---

## 5. Payment Scenarios

The platform must support deterministic payment outcomes:

- successful
- failed
- declined
- pending
- timeout

---

## 6. Ticket States

- open
- in_progress
- resolved
- closed

---

## 7. Non-Functional Requirements

### Security

- JWT authentication
- Role-based authorization
- Protected APIs and routes

### Reliability

- Deterministic seed data
- Stable API contracts
- Predictable responses

### Observability

- Correlation IDs
- Structured logging
- Request tracing

### Accessibility

- Semantic HTML
- Accessible forms and controls

### Scalability

- Dockerized deployment
- CI/CD compatible architecture