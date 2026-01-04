# Sample SRS (Mini, Original) — FastKart (Exam-Style Reference)

This is an **original** mini SRS-style document written as a reference for structure + wording. It is **not copied** from any proprietary SRS.

Use it as a template to answer questions like:
- “Write SRS characteristics / sections”
- “Write FRs + NFRs for increment 1”
- “Write constraints / assumptions”

---

## 1. Introduction
### 1.1 Purpose
This document specifies requirements for **FastKart**, an online shopping platform with ordering, payments, and delivery tracking.

### 1.2 Scope
FastKart shall allow customers to browse products, place orders, pay securely, and track deliveries. The system shall provide admin capabilities to manage products and orders.

### 1.3 Definitions
- **Customer**: end user who browses and purchases products.
- **Delivery partner**: external logistics system that provides delivery status updates.
- **PII**: personally identifiable information.

## 2. Overall Description
### 2.1 Product perspective
FastKart integrates with:
- Payment gateway (external)
- Delivery partner tracking system (external)
- Warehouse/inventory system (internal or external)

### 2.2 User classes
- Customer (registered)
- Customer (guest)
- Admin (operations)
- Support agent

### 2.3 Operating environment
- Web application (latest Chrome/Edge)
- Mobile web (Android/iOS browsers)

### 2.4 Constraints (examples)
- The system **shall comply with** applicable privacy regulations for PII processing.
- The system **shall comply with** PCI-DSS requirements for card payments.

### 2.5 Assumptions & dependencies
- Payment authorization is performed by a third-party payment gateway.
- Delivery tracking updates are provided by the delivery partner system.

---

## 3. External Interface Requirements
### 3.1 User interface (UI)
- The system shall provide a checkout flow that includes: cart review, address selection, shipment selection, payment, and confirmation.

### 3.2 External system interfaces
- The system shall send a payment authorization request to the payment gateway for each order payment attempt.
- The system shall receive delivery status update events (e.g., packed, dispatched, delivered) from the delivery partner system.

---

## 4. Functional Requirements (FRs)
Wording rule: **FRs are mandatory behaviors** and should use **“shall”**.

### 4.1 Account & authentication
- **FR-01**: The system shall allow a customer to register using email and password.
- **FR-02**: The system shall allow a registered customer to log in using email and password.

### 4.2 Catalog & cart
- **FR-03**: The system shall display a searchable product catalog including product name, price, and availability.
- **FR-04**: The system shall allow a customer to add a selected product and quantity to the cart.
- **FR-05**: The system shall allow a customer to update the quantity of an item in the cart.

### 4.3 Checkout & order
- **FR-06**: The system shall allow a customer to select a shipment method during checkout.
- **FR-07**: The system shall compute and display an order total including item subtotal, taxes (if applicable), discounts (if applicable), and shipment charges.
- **FR-08**: The system shall create an order only after receiving a successful payment authorization from the payment gateway.

### 4.4 Tracking
- **FR-09**: The system shall display the latest delivery status for an active order.
- **FR-10**: The system shall append each received delivery status update to the order’s tracking timeline.

---

## 5. Non-Functional Requirements (NFRs)
Wording rule: NFRs must be **measurable** (metric + threshold + conditions).

### 5.1 Performance
- **NFR-PERF-01**: The system shall load the product catalog page within 2 seconds for 90% of requests under 100 concurrent users.
- **NFR-PERF-02**: The system shall display a tracking status update within 5 seconds of receiving the corresponding delivery partner update for 95% of events.

### 5.2 Availability & reliability
- **NFR-AVAIL-01**: The checkout service shall achieve 99.5% uptime per calendar month (excluding scheduled maintenance).

### 5.3 Security & privacy
- **NFR-SEC-01**: The system shall use TLS 1.2 or higher for all authentication and payment-related communications.
- **NFR-SEC-02**: The system shall restrict access to a customer’s order history and tracking details to the authenticated customer account.

### 5.4 Usability
- **NFR-USAB-01**: In a usability test (n=10), new users shall complete checkout within 3 minutes on average with no more than 1 critical error per user.

---

## 6. Data Requirements
- The system shall store order records including order ID, items, totals, payment status, and shipment method.
- The system shall retain audit logs of login attempts and payment events for at least 90 days.

---

## 7. Acceptance Criteria (Exam-Friendly)
Examples (you can convert directly to test cases):
- Given a customer has items in cart, when the customer confirms payment and authorization succeeds, then an order is created and an order confirmation number is displayed.
- Given the delivery partner sends status “Out for delivery”, when the system receives the update, then the update appears in the tracking timeline within 5 seconds.

---

## 8. SRS Structure References (Non-copied)
Commonly used structures come from standards/templates such as:
- **ISO/IEC/IEEE 29148** (requirements engineering and specification guidance)
- **IEEE 830** (legacy SRS guidance; often referenced in courses)
- **Volere** requirements template

In exam answers, it is usually enough to write the section headings and 1–2 lines per section (purpose, scope, overall description, interfaces, FRs, NFRs, constraints, assumptions, acceptance criteria).
