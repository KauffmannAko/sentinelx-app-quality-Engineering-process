# SentinelX — Technical Requirements Document (TRD)

## 1. Architecture

| Layer | Technology |
|---|---|
| Frontend | React + TypeScript |
| Backend | Symfony REST API |
| Database | PostgreSQL |
| Containerization | Docker + Docker Compose |
| CI/CD | Jenkins |
| Registry | Docker Hub |

---

## 2. Authentication & Authorization

### Authentication

- JWT-based authentication
- Login/logout endpoints
- Password reset flow

### Authorization

Supported roles:

- CUSTOMER
- ADMIN
- SUPPORT

---

## 3. Backend Requirements

### API Standards

- RESTful APIs
- JSON request/response
- OpenAPI documentation
- Structured API envelopes
- Global error handling

### Backend Functional Domains

#### Authentication

Endpoints:

- `/auth/register`
- `/auth/login`
- `/auth/logout`
- `/auth/me`
- `/auth/password-reset/request`
- `/auth/password-reset/confirm`

#### Products

Endpoints:

- `/products`
- `/products/{id}`

#### Cart

Endpoints:

- `/cart`
- `/cart/items`

#### Orders

Endpoints:

- `/orders`
- `/orders/checkout`
- `/orders/{id}`
- `/orders/{id}/status`

#### Payments

Endpoints:

- `/payments`
- `/payments/simulate`
- `/payments/{id}`

#### Transactions

Endpoints:

- `/transactions`
- `/transactions/{id}`

#### Support Tickets

Endpoints:

- `/support/tickets`
- `/support/tickets/{id}`
- `/support/tickets/{id}/messages`

#### Users

Endpoints:

- `/users`
- `/users/{id}`

---

## 4. API Validation Rules

### Request Validation

- Required fields validation
- Enum validation
- Length validation
- UUID validation
- Email format validation

### Structured Error Handling

All APIs must return standardized response envelopes containing:

- success
- data
- meta
- error
- correlationId

---

## 5. Testability Requirements

### Deterministic Test Helpers

Endpoints:

- `/test-helpers/seed`
- `/test-helpers/reset`
- `/test-helpers/users`
- `/test-helpers/payment-scenarios`

Purpose:

- automated test setup
- deterministic environments

---

## 6. Observability Requirements

### Logging

- Structured request logging
- Error logging
- Correlation ID support

### Header

```txt
X-Correlation-ID