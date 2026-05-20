# SentinelX — User Stories

## Epic: Authentication

### SNT-AUTH-001 — Register Customer User

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to register an account,  
So that I can access the platform.

#### Acceptance Criteria

- User can register with valid details
- Duplicate email registration is rejected
- Password validation is enforced
- Success response is returned

---

### SNT-AUTH-002 — Login User

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to login,  
So that I can access protected features.

#### Acceptance Criteria

- Valid credentials generate JWT
- Invalid credentials return error
- Protected routes require authentication

---

### SNT-AUTH-003 — Reset Password

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to reset my password,  
So that I can regain account access.

#### Acceptance Criteria

- Reset token can be requested
- Password can be updated with valid token
- Invalid token returns error

---

## Epic: Product Management

### SNT-PROD-001 — View Products

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to browse products,  
So that I can purchase items.

#### Acceptance Criteria

- Products are paginated
- Products support filtering/search
- Product details are viewable

---

### SNT-PROD-002 — Manage Products

#### Type

Backend + Frontend

#### User Story

As an admin,  
I want to manage products,  
So that inventory remains accurate.

#### Acceptance Criteria

- Admin can create product
- Admin can update product
- Admin can delete product

---

## Epic: Cart Management

### SNT-CART-001 — Add Item to Cart

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to add products to my cart,  
So that I can purchase them later.

#### Acceptance Criteria

- Cart item can be added
- Cart quantity updates correctly
- Cart persists for authenticated users

---

### SNT-CART-002 — Update Cart Quantity

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to update cart quantities,  
So that my order reflects my intended purchase.

#### Acceptance Criteria

- Quantity can be updated
- Invalid quantities are rejected

---

## Epic: Order Management

### SNT-ORDER-001 — Checkout Order

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to checkout my cart,  
So that I can place an order.

#### Acceptance Criteria

- Order is created successfully
- Cart converts into order
- Order status is tracked

---

### SNT-ORDER-002 — Update Order Status

#### Type

Backend

#### User Story

As an admin,  
I want to update order statuses,  
So that order processing can be tracked.

#### Acceptance Criteria

- Admin can update order status
- Invalid statuses are rejected

---

## Epic: Payment Processing

### SNT-PAY-001 — Simulate Payments

#### Type

Backend

#### User Story

As a QA engineer,  
I want deterministic payment scenarios,  
So that automated testing remains reliable.

#### Acceptance Criteria

- Successful payments supported
- Failed payments supported
- Pending payments supported
- Timeout payments supported

---

### SNT-PAY-002 — View Payments

#### Type

Backend + Frontend

#### User Story

As an admin,  
I want to view payment records,  
So that I can monitor transactions.

#### Acceptance Criteria

- Payments are searchable
- Payments are filterable
- Payment details are retrievable

---

## Epic: Transaction Management

### SNT-TRX-001 — View Transactions

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to view my transactions,  
So that I can track payment history.

#### Acceptance Criteria

- Transactions are listed
- Transactions support filtering/sorting
- Transaction details are viewable

---

### SNT-TRX-002 — Manage Transactions

#### Type

Backend

#### User Story

As an admin,  
I want to manage transactions,  
So that financial records remain accurate.

#### Acceptance Criteria

- Admin can create transaction
- Admin can update transaction
- Admin can delete transaction

---

## Epic: Support Ticketing

### SNT-SUP-001 — Create Support Ticket

#### Type

Backend + Frontend

#### User Story

As a customer,  
I want to create a support ticket,  
So that I can request assistance.

#### Acceptance Criteria

- Ticket can be created
- Ticket defaults to open status
- Ticket appears in support dashboard

---

### SNT-SUP-002 — Respond to Support Ticket

#### Type

Backend + Frontend

#### User Story

As a support user,  
I want to respond to tickets,  
So that customer issues can be resolved.

#### Acceptance Criteria

- Support users can add responses
- Internal/public visibility supported
- Responses persist correctly

---

### SNT-SUP-003 — Manage Ticket Status

#### Type

Backend + Frontend

#### User Story

As a support user,  
I want to update ticket statuses,  
So that issue progress can be tracked.

#### Acceptance Criteria

- Ticket status can be updated
- Ticket can be assigned
- Invalid statuses are rejected

---

## Epic: User Administration

### SNT-USER-001 — Manage Users

#### Type

Backend + Frontend

#### User Story

As an admin,  
I want to manage platform users,  
So that platform access remains controlled.

#### Acceptance Criteria

- Admin can create users
- Admin can update users
- Admin can disable users
- Role assignment is supported

---

## Epic: Dashboard & Reporting

### SNT-DASH-001 — View Admin Dashboard Statistics

#### Type

Backend + Frontend

#### User Story

As an admin,  
I want to view dashboard statistics,  
So that I can monitor platform activity.

#### Acceptance Criteria

- Dashboard statistics endpoint returns data
- Metrics load successfully
- Unauthorized users cannot access dashboard