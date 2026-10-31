# Playbook 03: Pre-Completion Verification Gates

Use this playbook as the definitive checklist before claiming any coding task is finished.

---

## 1. The 4 Deterministic Gates

### Gate A: Static Type & Syntax Check
Run the project's static type checker to verify zero syntax or type mismatches:
```bash
# TypeScript / Next.js
npx tsc --noEmit

# Python
mypy .
```

### Gate B: Bounded Test Suite Execution
Run the focused test runner for modified files:
```bash
# Vitest / Jest (Single File)
npx vitest run path/to/tested-file.test.ts

# Pytest (Single Test)
pytest tests/test_feature.py -k "test_specific_behavior"
```

### Gate C: Diff Audit (`git diff`)
Run a scoped diff check to audit changes:
```bash
git diff --stat
```
Verify:
1. Only intended files are present.
2. No temporary debug comments, `console.log("here")`, or `.env` credential leaks exist.

---

## 2. Client-First Verification Summary Format

When reporting task completion, structure your response as follows:

```markdown
### Verification Summary
- **Typecheck:** [e.g., 0 errors found via `tsc --noEmit`]
- **Automated Tests:** [e.g., 8/8 tests passed in 1.4s]
- **Scope Audit:** [e.g., Exactly 2 files modified (`src/auth.ts`, `tests/auth.test.ts`)]
- **How to verify manually:** [1 concise step for the user to confirm in browser/app]
```
