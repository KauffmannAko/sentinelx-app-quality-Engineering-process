# SentinelX — Prioritized Risk Matrix

**Scoring:** Risk Score = Likelihood × Impact

## Priority Classification

| Risk Score | Priority |
|---:|---|
| 20–25 | P0 — Critical |
| 15–19 | P1 — High |
| 8–14 | P2 — Medium |
| 1–7 | P3 — Low |

---

## Risk Matrix

| Feature/Area | Source of Risk | Likelihood (1–5) | Impact (1–5) | Risk Score | Testing Priority |
|---|---|---:|---:|---:|---|
| Customer Login / Protected Access | PRD Customer Features / SNT-AUTH-002 | 5 | 5 | 25 | P0 — Critical |
| Customer Checkout | PRD Customer Features / SNT-ORDER-001 | 5 | 5 | 25 | P0 — Critical |
| Customer Payment Simulation | PRD Payment Scenarios / SNT-PAY-001 | 5 | 5 | 25 | P0 — Critical |
| Customer Cart Management | PRD Customer Features / SNT-CART-001 / SNT-CART-002 | 5 | 5 | 25 | P0 — Critical |
| Customer Registration | PRD Customer Features / SNT-AUTH-001 | 4 | 5 | 20 | P0 — Critical |
| Customer Password Reset | PRD Customer Features / SNT-AUTH-003 | 4 | 5 | 20 | P0 — Critical |
| Customer Product Browsing | PRD Customer Features / SNT-PROD-001 | 4 | 5 | 20 | P0 — Critical |
| Customer Order History | PRD Customer Features / SNT-ORDER-001 | 4 | 5 | 20 | P0 — Critical |
| Customer Transaction History | PRD Customer Features / SNT-TRX-001 | 4 | 5 | 20 | P0 — Critical |
| Customer Support Ticket Creation | PRD Customer Features / SNT-SUP-001 | 4 | 5 | 20 | P0 — Critical |
| Customer Ticket Status Tracking | PRD Customer Features / Ticket States / SNT-SUP-003 | 4 | 5 | 20 | P0 — Critical |
| Support Ticket Visibility | PRD Support Features / SNT-SUP-002 / SNT-SUP-003 | 4 | 4 | 16 | P1 — High |
| Support Ticket Assignment | PRD Support Features / SNT-SUP-003 | 4 | 4 | 16 | P1 — High |
| Support Ticket Status Update | PRD Support Features / Ticket States / SNT-SUP-003 | 4 | 4 | 16 | P1 — High |
| Support Ticket Response | PRD Support Features / SNT-SUP-002 | 4 | 4 | 16 | P1 — High |
| Support Internal/Public Message Visibility | PRD Support Features / SNT-SUP-002 | 3 | 5 | 15 | P1 — High |
| Admin User Management | PRD Admin Features / SNT-USER-001 | 3 | 5 | 15 | P1 — High |
| Admin Role-Based Access Control | PRD User Roles / SNT-USER-001 / SNT-DASH-001 | 3 | 5 | 15 | P1 — High |
| Admin Product Management | PRD Admin Features / SNT-PROD-002 | 3 | 4 | 12 | P2 — Medium |
| Admin Payment Management | PRD Admin Features / SNT-PAY-002 | 3 | 4 | 12 | P2 — Medium |
| Admin Transaction Management | PRD Admin Features / SNT-TRX-002 | 3 | 4 | 12 | P2 — Medium |
| Admin Support Ticket Management | PRD Admin Features / SNT-SUP-003 | 3 | 4 | 12 | P2 — Medium |
| Admin Order Status Management | PRD Admin Features / SNT-ORDER-002 | 3 | 4 | 12 | P2 — Medium |
| Admin Dashboard Statistics | PRD Admin Features / SNT-DASH-001 | 3 | 3 | 9 | P2 — Medium |