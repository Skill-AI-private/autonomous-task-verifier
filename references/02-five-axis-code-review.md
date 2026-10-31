# Playbook 02: 5-Axis Code Review & Security Audit

Synthesized from **`addyosmani/agent-skills`** (`code-review-and-quality`).

Every completed task must pass these 5 review axes:

---

## Axis 1: Correctness & Edge-Case Resilience
- [ ] Are null, undefined, empty strings, and empty arrays explicitly handled?
- [ ] Are error boundaries and try-catch blocks scoped tightly around fallible operations?
- [ ] Does asynchronous logic handle timeouts or network rejections without crashing?

## Axis 2: Readability & Simplicity (Anti-Complexity)
- [ ] Can a junior engineer understand this function in under 60 seconds?
- [ ] Are function names verb-led (`calculateTax`, `validateSession`) and variables descriptive?
- [ ] Is control flow flat? (Use early returns / guard clauses instead of 4-level nested `if/else`).

## Axis 3: Architecture & Dependency Locality
- [ ] Does this file import from unauthorized layers (e.g., UI component importing direct database drivers)?
- [ ] Are shared types centralized, while domain-specific types remain local?

## Axis 4: Security (OWASP Top 10 Core)
- [ ] Zero hardcoded secrets, API tokens, or private keys in source code.
- [ ] All external user inputs sanitized and validated via schema validators (e.g., Zod).
- [ ] Database queries parameterized (no raw string interpolation into SQL queries).

## Axis 5: Performance & Memory
- [ ] No unbounded loops or recursion without exit conditions.
- [ ] No un-memoized expensive computations inside frequently rendering React components.
- [ ] Event listeners, intervals, and WebSocket subscriptions properly cleaned up on unmount.
