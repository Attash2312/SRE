# Chapter 1 — Foundations (Exam-Ready)

## Key stats + recurring problems (very exam-friendly)
- ~**40–50%** of defects originate in the **requirements** phase.
- Common problems: informal gathering, implied functionality, miscommunicated assumptions, poor specs, casual change process.

## 1) What is a “requirement”?
A requirement is a **capability**, **condition**, or **quality** needed by a stakeholder and that the system must satisfy.

### Requirement levels (memorize)
| Level | Also called | Example (Online Shopping) |
|---|---|---|
| **Business** | Business goals | “Increase online sales by 20% in 6 months.” |
| **User** | User needs | “As a customer, I want to track my shipment.” |
| **System** | Functional + non-functional | “System shall show tracking status within 2 seconds.” |

**Mnemonic:** **B-U-S** = **B**usiness, **U**ser, **S**ystem.

## 1.1) Seven types of requirements (you must memorize)
| Type | Keyword | Example |
|---|---|---|
| Business requirements | **WHY** | “Reduce airport staff costs by 25%.” |
| System requirements | system-of-systems | “POS workstation includes scanner + printer + software.” |
| User requirements | user goals/tasks | “As a passenger, I want to check in.” |
| Business rules | policies/algorithms | “Refund only within 7 days.” |
| Functional requirements | **shall** behaviors | “System shall allow users to print boarding passes.” |
| Features | grouped capability | “Spelling checker” / “Bookmarks” |
| Non-functional requirements | **-ilities** | “Checkout page loads ≤ 2s for 95% requests.” |

## 2) Functional vs Non-Functional
- **Functional requirement (FR):** what the system **does** (features/behaviors).
- **Non-functional requirement (NFR):** how well / under what constraints (quality attributes, constraints).

### Product vs Project requirements (often confused)
- **Product requirements:** implemented in the software (belongs in SRS/backlog).
- **Project requirements:** needed to deliver project but not software behavior (training, docs, migration, beta, legal).

### Quick examples
| Type | Good example | Why it’s good |
|---|---|---|
| FR | “System shall allow registered users to add items to a cart.” | Clear actor + action + condition |
| NFR (Performance) | “Search results shall be returned in ≤ 2s for 95% requests.” | Measurable + testable |

## 3) Characteristics of good requirements (often asked)
**Mnemonic:** **C-U-V-C** (plus T)
- **C**orrect
- **U**nambiguous
- **V**erifiable (testable)
- **C**omplete
- **T**raceable

### 7 characteristics of a *single requirement statement* (memorize)
**C C F N P U V**
1) Complete 2) Correct 3) Feasible 4) Necessary 5) Prioritized 6) Unambiguous 7) Verifiable

## 4) Common requirement problems (exam critique)
| Problem | Signal words | Fix pattern |
|---|---|---|
| Ambiguous | “good”, “fast”, “user-friendly” | add metric: time, error rate, SUS score |
| Not verifiable | “secure”, “easy” | convert to measurable acceptance criteria |
| Incomplete | missing actor/trigger/exception | add preconditions + alternate flows |
| Inconsistent | conflicting statements | identify source + reconcile in review |
| Design/implementation bias | “use Oracle DB” | move to constraint or remove unless mandated |
| Amalgamation | “validate and accept credit cards and cashier’s checks” | split into atomic requirements |

## 5) Stakeholders
- **Internal** (within organization): product owner, support, finance, ops, dev team.
- **External**: customers, payment gateway, courier/shipping partners, regulators.

## 6) SRE lifecycle (high-level)
Typical flow: **Elicit → Analyze/Model → Specify (SRS) → Validate → Manage/Trace**

```mermaid
flowchart LR
BR[Business Requirements] --> UR[User Requirements]
UR --> FE[Features]
FE --> FR[Functional Requirements]
FR --> D[Design]
D --> I[Implementation]
I --> T[Testing]
```

```mermaid
flowchart LR
A[Elicitation] --> B[Analysis & Negotiation]
B --> C[Specification (SRS)]
C --> D[Validation]
D --> E[Management & Traceability]
E --> A
```

## 7) Scenario mini-practice (like your exam)
**Scenario:** Online shopping system.
- Write 2 User requirements, 2 FRs, 2 NFRs.

**Model answer (concise):**
- User req: “As a registered user, I want to checkout using a preferred payment method.”
- User req: “As a registered user, I want to cancel my order before dispatch.”
- FR: “System shall allow a user to register with name, address, phone number.”
- FR: “System shall allow a registered user to place an order from items in cart.”
- NFR (Security): “All payment requests shall use TLS 1.2+ and store no CVV.”
- NFR (Availability): “Checkout service shall be available 99.5% monthly.”

## 8) What to memorize from Chapter 1
- Definitions: requirement, FR vs NFR, stakeholder.
- Quality criteria: **Correct, Unambiguous, Verifiable, Complete, Traceable**.
- Lifecycle: **Elicit → Analyze → Specify → Validate → Manage/Trace**.

## 9) Exam-style questions (solved)
### Q1 (Classification — 7 types)
Classify each statement:
1) “Reduce airport staff costs by 25%.” → **Business requirement** (WHY)
2) “As a passenger, I want to check in for a flight.” → **User requirement**
3) “System shall allow users to print boarding passes.” → **Functional requirement**
4) “Refund only within 7 days.” → **Business rule** (policy; drives requirements)
5) “Checkout page loads ≤ 2s for 95% requests.” → **NFR (performance)**
6) “Spelling checker.” → **Feature**
7) “POS workstation includes scanner + printer + software.” → **System requirement**

### Q2 (Product vs Project requirements)
Classify:
- “System shall encrypt passwords using salted hashing.” → **Product requirement** (software behavior/quality)
- “Create user training manual and conduct 2 training sessions.” → **Project requirement** (delivery activity)
