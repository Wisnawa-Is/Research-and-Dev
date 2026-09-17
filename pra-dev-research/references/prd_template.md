# Product Requirements Document (PRD) Template
<!-- Load JIT only when authoring or updating PRD.md -->

```markdown
# Product Requirements Document (PRD)

## 1. Executive Summary & Vision
- **Product Name**: [Name]
- **Vision Statement**: [1-2 sentence core purpose]
- **Target Personas**:
  - Persona A: [Role, core pain points, goal]
  - Persona B: [Role, core pain points, goal]
- **Core Value Proposition**: [Differentiator vs alternatives]

## 2. Goals & Success Metrics (KPIs)
- **Business Goals**: [Goal 1], [Goal 2]
- **Key Performance Indicators (KPIs)**:
  | Metric | Baseline / Target | Measurement Method |
  | :--- | :--- | :--- |
  | Time-to-First-Action | < 60 seconds | Analytics Event |
  | Core Workflow Completion | > 85% | Funnel Analysis |
  | System Error Rate | < 0.5% | Logging / Sentry |

## 3. Product Scope & MVP Definition
- **In-Scope (MVP Phase 1)**: [Core feature list]
- **Out-of-Scope (Post-MVP)**: [Future phase items]

## 4. User Journeys & Core Epics

### Epic 1: [Feature Group Name]
- **User Story 1.1**: As a [role], I want to [action] so that [benefit].
  - **Acceptance Criteria**:
    - Given [precondition], when [action], then [expected outcome].
    - Edge Case: [Failure handling / empty state].

## 5. Non-Functional Requirements (NFRs)
- **Performance**: P95 < 250ms on critical paths.
- **Security**: OWASP Top 10, TLS 1.3, AES-256 at rest, RBAC.
- **Scalability**: Horizontal scale target, 99.9% uptime SLA.
- **Accessibility**: WCAG 2.1 AA compliance.

## 6. Assumptions & Risk Matrix
| Risk / Assumption | Impact | Likelihood | Mitigation Strategy |
| :--- | :--- | :--- | :--- |
| [Risk 1] | High | Low | [Mitigation] |

---

## 7. Document Revision Log & Feature Extensions

### In-Place Revisions:
| Date | Section Modified | Description of Change | Trigger |
| :--- | :--- | :--- | :--- |
| [YYYY-MM-DD] | [Section #] | [Summary of in-place update] | [User Request] |

### Appended Feature Extensions:
---

## Feature Extension: [Name of New Sub-Plan]
- **Motivation & Persona**: [Why added]
- **Acceptance Criteria**: [Requirements]
- **Integration Points**: [Connection to core MVP]
```
