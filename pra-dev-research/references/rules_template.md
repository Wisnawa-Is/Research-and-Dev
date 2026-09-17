# Project Development & Contributor Rules Template
<!-- Load JIT only when authoring or updating rules.md -->

```markdown
# Project Rules & Contributor Guidelines

## 1. Architectural Guardrails
- **Boundaries**: Strictly respect domain layers. UI components must never make direct database queries; all interactions go through service/controller abstractions.
- **Dependency Inversion**: High-level modules must not import low-level implementations directly; use interfaces and dependency injection where applicable.
- **State Management**: Local state should remain inside components; shared state must reside strictly within defined global stores.

---

## 2. Code Quality & Style Standards
- **Naming Conventions**:
  - Files: `kebab-case` for components and utilities (e.g., `user-card.tsx`, `auth-service.ts`).
  - Variables & Functions: `camelCase`.
  - Types, Interfaces & Classes: `PascalCase`.
  - Constants & Environment Variables: `UPPER_SNAKE_CASE`.
- **Type Safety**:
  - Strict typing enabled; `any` is strictly prohibited. Use `unknown` with runtime type narrowing.
  - All API payload responses must match defined DTO interfaces.
- **Linting & Formatting**:
  - Run linter checks prior to every commit (`npm run lint` / `cargo clippy` / `ruff check`).
  - Keep functions focused (Single Responsibility Principle, under 40 lines where feasible).

---

## 3. AI Coding Agent Execution Protocol
- **No Unsolicited File Deletion**: Never delete or rename existing files without explicit user confirmation.
- **Preserve Documentation**: Maintain all docstrings, comments, and license headers.
- **Incremental Changes**: Make targeted diffs rather than entire file rewrites when updating existing logic.
- **Verification First**: Verify changes by executing tests or build commands before marking tasks complete.

---

## 4. Git & Branching Strategy
- **Branch Naming**: `feat/description`, `fix/issue-key`, `refactor/scope`.
- **Commit Messages**: Conventional Commits standard:
  - `feat(scope): concise description of feature`
  - `fix(scope): concise description of bug fix`
  - `docs(scope): documentation change only`
  - `refactor(scope): internal logic change without external behavior shift`
```
