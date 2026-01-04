# Requirement Elicitation (Exam-Ready)

## 1) Goal
Discover stakeholder needs and constraints **before** you write the SRS.

## 1.1) Six key elicitation actions (easy marks)
Knowledge acquisition, reading, interviewing, listening, asking, observing.

## 1.2) Seven sources for requirements (asked)
1. Interviews/discussions with users
2. Documents for current/competing products
3. Existing SRS/specs
4. Problem reports + enhancement requests
5. Marketing surveys/questionnaires
6. Observing users at work
7. Events and responses (triggers)

## 2) Techniques (know definitions + pros/cons)
### A) Interviews
- **Best when:** domain experts available; need deep understanding.
- **Benefits:** rich detail; clarify instantly.
- **Limitations:** bias; time-consuming; inconsistent answers.

### B) Workshops (JAD)
- **Best when:** many stakeholders; need alignment/negotiation.
- **Benefits:** fast consensus; resolves conflicts early.
- **Limitations:** scheduling hard; strong personalities dominate.

### C) Observation / Contextual inquiry
- **Best when:** real workflow matters.
- **Benefits:** reveals tacit requirements; exposes exceptions.
- **Limitations:** Hawthorne effect; may be slow.

### D) Surveys
- **Best when:** large user base.
- **Benefits:** cheap, wide coverage.
- **Limitations:** shallow answers; low response rate.

### E) Document analysis
- **Best when:** legacy system exists or policies exist.
- **Benefits:** quick baseline; compliance.
- **Limitations:** docs outdated.

### F) Prototyping
- **Best when:** UI/interaction unclear.
- **Benefits:** reduces ambiguity; early validation.
- **Limitations:** stakeholders confuse prototype with final system.

**Mnemonic (common set):** **I-W-O-S-D-P**
Interviews, Workshops, Observation, Surveys, Documents, Prototypes.

## 2.1) Four technique categories (name-only is enough)
1) Traditional 2) Collaborative 3) Knowledge elicitation 4) Contextual

## 3) Elicitation challenges (often asked)
| Challenge | Example | Mitigation |
|---|---|---|
| Stakeholder conflict | marketing vs ops priorities | workshops + negotiation + priorities |
| Tacit knowledge | “everyone knows this” rules | observation + examples |
| Scope creep | new features every week | baseline + change control |
| Ambiguity | “fast” “secure” | define metrics/acceptance criteria |
| Communication gaps | dev vs business language | models + glossary |

## 4) Choosing techniques for a 20-week short project (like your paper)
**Recommended pair (strong answer):**
1) **Interviews** with key roles (customer, admin, payment/shipping partner)
2) **Prototyping** (low-fidelity UI + checkout flow)

**Why:** interviews capture needs quickly; prototypes validate UI-intensive shopping flows fast.

## 5) Elicitation outputs
- Stakeholder list
- Goals and constraints
- Use cases / user stories
- Business rules
- Glossary
- Initial backlog

## 6) Scenario mini-questions (practice)
1) Pick 2 techniques for FastKart and justify.
2) List 5 questions you ask in interview for “loyalty rewards”.

## 3.1) Five major elicitation problem groups (asked)
| Group | What it means |
|---|---|
| Scope | system boundary unclear (IN/OUT) |
| Understanding | users/analysts don’t fully understand domain/needs |
| Conflicting requirements | stakeholders disagree |
| Difficult to express | tacit knowledge, hard to articulate |
| Volatility | requirements change over time |

## 7) Exam-style questions (solved)
### Q1 (Pick techniques + justify — FastKart)
Choose 2 techniques and justify for recommendations + tracking + loyalty:
- **Interviews** (power users + delivery staff): uncover pain points and “why” behind behaviors.
- **Workshops/JAD** (management + marketing + ops + dev): align business goals, define loyalty rules, resolve conflicts.

Limitations (write 1 line each in exam):
- Interviews: slow + biased answers.
- Workshops: scheduling + dominant stakeholders.

### Q2 (Write 5 interview questions — loyalty)
1) What actions earn points (orders, referrals, reviews)?
2) What actions should not earn points (canceled orders, refunds)?
3) Do points expire? If yes, after how long?
4) What redemption options matter most (discount, free delivery, gifts)?
5) What is the biggest reason you stop using a loyalty program?
