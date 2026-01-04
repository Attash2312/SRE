# SRE Final — 1-Page Cheat Sheet (Memorize)

## Must-memorize lists (exam tip)
- **7 types** of requirements
- **4** requirements development activities
- **7** quality characteristics of requirement statements
- **4** quality characteristics of an SRS document
- **6** common RE problems
- **Hierarchy**: Business → User → Feature → Functional → Design → Code → Test

---

## Key stats + recurring problems
- ~**40–50%** defects originate in **requirements**.
- Common causes: informal gathering, implied functionality, hidden assumptions, poor specs, casual change control.

---

## Requirements Engineering (definition)
RE = identifying, eliciting, analyzing, specifying, validating, and managing stakeholder needs.

---

## 7 Types of requirements (with keyword + example)
| Type | Keyword | Example |
|---|---|---|
| Business requirements | **WHY** | “Reduce staff cost by 25%.” |
| System requirements | system-of-systems | “Cashier workstation includes scanner + POS software + printer.” |
| User requirements | user goals | “As passenger, I want to check in.” |
| Business rules | policies/algorithms | “Refund only within 7 days.” |
| Functional requirements | **shall** behaviors | “System shall print boarding pass.” |
| Features | grouped capability | “Spelling checker” / “Bookmarks” |
| Non-functional requirements | **-ilities** | “Page loads ≤ 2s for 90% requests.” |

---

## Requirement writing rules (exam-scoring)
1) Use **“shall”** for mandatory requirements (FRs and testable NFR targets).
2) One statement = **one requirement** (atomic). Split “and/or” requirements.
3) Make it **verifiable**: add metric + threshold + conditions (load, device, time window).
4) Avoid ambiguous words: *fast, good, user-friendly, etc.* Replace with a measurable criterion.
5) If it’s mandated (law/standard/tech choice), write it as a **constraint/compliance requirement**.

### Quick templates + examples (memorize)
| Kind | Template | Good example |
|---|---|---|
| User requirement | As a `<role>`, I want `<goal>` so that `<benefit>`. | “As a customer, I want to track my order so I can plan delivery.” |
| Functional requirement (FR) | The system **shall** `<behavior>` [when `<condition>`]. | “The system shall allow a registered user to cancel an order before dispatch.” |
| Non-functional requirement (NFR) | The system **shall** `<quality>` `<metric>` [under `<load>`]. | “The system shall return search results in ≤2s for 95% requests under 100 users.” |
| Constraint / compliance | The system **shall comply with** `<standard>` / **shall** `<restriction>`. | “The system shall comply with PCI-DSS for card payments.” |
| Business rule | Policy: `<rule>` (then derive FRs). | “Refund only within 7 days.” |

---

## Product vs Project requirements
- **Product requirements**: built into the software (go in SRS/backlog).
- **Project requirements**: needed to deliver project (training, docs, migration, beta, legal).

---

## Requirements development (4 activities)
**E → A → S → V** (iterative)
- Elicitation
- Analysis
- Specification
- Validation

---

## Requirements management (8 core activities)
1) Baseline 2) Evaluate changes 3) Incorporate approved changes 4) Update plans 5) Negotiate commitments 6) Define dependencies 7) Trace to design/code/tests 8) Track status

---

## 6 common problems
1) Insufficient user involvement
2) Inaccurate planning
3) Creeping requirements (scope creep)
4) Ambiguous requirements
5) Gold plating
6) Overlooked stakeholders

---

## 7 characteristics of good requirement statements
**C C F N P U V**
- Complete
- Correct
- Feasible
- Necessary
- Prioritized
- Unambiguous
- Verifiable

---

## 4 characteristics of a good SRS
**C C M T**
- Complete
- Consistent
- Modifiable
- Traceable

---

## Business requirements fundamentals
Business requirements must define:
1) Opportunities 2) Objectives 3) Success metrics 4) Vision statement

Vision statement template (7 parts):
**For / Who / The / Is / That / Unlike / Our product**

---

## Scope techniques (4)
1) Context diagram
2) Ecosystem map
3) Feature tree
4) Event list (user/time/signal)

---

## Elicitation sources (7)
Interviews, documents, existing SRS, problem reports, surveys, observation, events/responses.

---

## Analysis checking (3)
- Necessity
- Consistency & completeness
- Feasibility

---

## Validation vs Analysis (quick)
- **Analysis:** works with raw elicited reqs; finds gaps/conflicts.
- **Validation:** checks final draft is acceptable and testable.

---

## V-Model mapping (remember)
- User requirements → Acceptance testing
- Functional requirements → System testing
- Architecture → Integration testing
- Module design → Unit testing

---

## Rapid recall (5-minute drill)
Answer these without looking:
1) List the **7 types** of requirements.
2) Write the **hierarchy** from business → test.
3) Difference between `<<include>>` and `<<extend>>` (1 line each).
4) 4 activities of requirements development.
5) 8 activities of requirements management (keywords).
6) 3 analysis checking activities.
7) 5 validation roles.
8) 3 traceability analyses.
9) Give 2 examples each: FR and NFR.
10) Convert “good usability” into a measurable requirement.
