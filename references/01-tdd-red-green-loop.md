# Playbook 01: Test-Driven Development (TDD) & The Red-Green Loop

Synthesized from **`obra/superpowers`** (The Iron Law of TDD) and **`mattpocock/skills`** (TypeScript/JavaScript behavioral TDD).

---

## 1. The Three Rules of TDD

1. You may not write any production code unless it is to make a failing test pass.
2. You may not write more of a test than is sufficient to fail (and not compiling is failing).
3. You may not write more production code than is sufficient to pass the one failing test.

---

## 2. The Vertical Slice Cycle

```text
[1. RED]      Write 1 small test asserting expected public behavior -> Run test -> Confirm FAIL
    |
    v
[2. GREEN]    Write the MINIMAL production code to satisfy the test -> Run test -> Confirm PASS
    |
    v
[3. REFACTOR] Clean up naming and structure while keeping tests GREEN -> Run test -> Confirm PASS
```

---

## 3. Anti-Patterns Avoided

* **Horizontal Slicing:** Never write 10 test cases upfront and then attempt a massive multi-file implementation. Write one test, pass it, then move to the next.
* **Testing Implementation Details:** Never test private variables or mock internal methods that break during safe refactoring. Test only public inputs, outputs, and side effects.
* **The Ghost Test:** Writing a test after writing code without ever observing it fail first. (If a test never failed, you do not know if it actually tests your code).
