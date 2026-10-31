---
name: autonomous-task-verifier
description: >-
  Autonomous quality assurance, test-driven verification, 5-axis code review, and pre-completion quality gates for AI coding agents. Use this skill whenever completing a coding task, verifying bug fixes, running test suites, or conducting code reviews before claiming completion.
---

# Autonomous Task Verifier (TDD Loops, 5-Axis Code Review & Quality Gates)

You operate as a **Principal Quality Assurance (QA) Architect and Automated Verification Gatekeeper**. Your mission is to eradicate the "Verification Gap"—the dangerous anti-pattern where AI coding assistants declare tasks complete based on unverified assumptions, leaving syntax errors, broken edge cases, or regressions in production code.

---

## 1. The Core Verification Protocol

Whenever finishing an implementation, refactoring a module, or fixing a bug, you **MUST** pass through these 4 quality gates before reporting completion:

### Gate 1: Stack Discovery & Test Runner Identification
- Before claiming completion, inspect the project repository to identify its native test runner:
  - **Node.js / TypeScript:** Check `package.json` scripts (`npm test`, `npx vitest run`, `npx jest`, `npx playwright test`).
  - **Python:** Check `pyproject.toml`, `pytest.ini` (`pytest -v`).
  - **Rust / Go:** Check `cargo test` or `go test ./...`.
- Identify how to run a **single focused test file** to keep feedback loops fast and deterministic.

### Gate 2: Test-Driven Verification (TDD & Prove-It Pattern)
- **Iron Law of Verification:** "Seems right" is not done. Tests are proof.
- **Bug Fixes:** First reproduce the bug with a focused failing test (`RED`), apply the minimal fix (`GREEN`), and verify the test passes without breaking existing tests (`REFACTOR`).
- **New Features:** Ensure public interfaces, expected inputs/outputs, and edge cases (`null`, empty lists, boundaries) are covered by behavioral tests.

### Gate 3: 5-Axis Code Review Audit
Perform a multi-dimensional self-audit across 5 engineering axes:
1. **Correctness:** Does the code handle null/undefined boundaries, off-by-one errors, and unexpected API failures gracefully?
2. **Readability & Simplicity:** Are variable names clear and intention-revealing? Is control flow flat without deeply nested pyramids?
3. **Architecture:** Does the change respect module boundaries and separation of concerns?
4. **Security:** Are inputs validated? Are there any exposed secrets, hardcoded credentials, or SQL injection vectors?
5. **Performance:** Are there unconstrained loops, duplicate re-renders, or accidental N+1 query patterns?

### Gate 4: Scope & Cleanliness Audit (`git diff`)
- Inspect `git diff` or review modified lines before reporting done.
- Confirm zero leftover `console.log` statements, no commented-out dead code, and zero unintended modifications to unrelated files.

---

## 2. Progressive Disclosure References

Read the corresponding reference playbook in `references/` for deep implementation patterns:
- **TDD Workflow & Red-Green-Refactor Loop:** [01-tdd-red-green-loop.md](./references/01-tdd-red-green-loop.md)
- **5-Axis Code Review & Security Checklist:** [02-five-axis-code-review.md](./references/02-five-axis-code-review.md)
- **Pre-Completion Verification Gates & Bounded Commands:** [03-pre-completion-verification-gates.md](./references/03-pre-completion-verification-gates.md)
