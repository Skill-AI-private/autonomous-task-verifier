<div align="center">

# Autonomous Task Verifier (`autonomous-task-verifier`)

**Automated TDD Loops, 5-Axis Code Review & Pre-Completion Quality Gates**  
*The Deterministic Quality Assurance & Verification Standard for AI Coding Agents.*

[![Version](https://img.shields.io/badge/version-1.0.0-18181B.svg?style=flat-square&labelColor=09090B)](https://github.com/Skill-AI-private/autonomous-task-verifier)
[![Verification](https://img.shields.io/badge/quality%20gate-zero%20assumptions-18181B.svg?style=flat-square&labelColor=09090B)](https://github.com/Skill-AI-private/autonomous-task-verifier)
[![Harnesses](https://img.shields.io/badge/compatibility-Antigravity%20|%20Claude%20Code%20|%20Cursor%20|%20Copilot-18181B.svg?style=flat-square&labelColor=09090B)](https://github.com/Skill-AI-private/autonomous-task-verifier)
[![License](https://img.shields.io/badge/license-MIT-18181B.svg?style=flat-square&labelColor=09090B)](LICENSE)

<br/>

```text
==========================================================================================
                 AUTONOMOUS TASK VERIFIER ARCHITECTURE MATRIX
==========================================================================================

  [01] THE IRON LAW OF VERIFICATION
       +-- Prohibition of unverified completion claims ("seems right" is not done)
       +-- Mandatory stack discovery: auto-identifies Vitest, Jest, Pytest, Playwright
       +-- Bounded command execution: targeted test suites with zero hanging processes

  [02] TEST-DRIVEN DEVELOPMENT (TDD) LOOP
       +-- Red Phase: Reproduce bug or assert new feature via failing test first
       +-- Green Phase: Write minimal implementation to satisfy failing test
       +-- Refactor Phase: Eliminate duplication while keeping suite green

  [03] 5-AXIS CODE REVIEW AUDIT
       +-- Correctness: Edge cases, null/empty checks, error boundaries
       +-- Simplicity: Flat control flow, clear naming, zero dead code
       +-- Architecture: Module boundary respect & dependency locality
       +-- Security: Input sanitization, OWASP checks, zero leaked secrets
       +-- Performance: No unbounded loops, memory leaks, or N+1 queries

  [04] PRE-COMPLETION DIFF & CLEANLINESS GATES
       +-- Typecheck verification (tsc --noEmit / mypy)
       +-- Scoped git diff audit (zero leftover debug logs or unintended changes)
       +-- Client-First Verification Summary (proof of test pass + 1-step manual check)
==========================================================================================
```

</div>

---

## Technical Specifications

`autonomous-task-verifier` eliminates the "Verification Gap" across autonomous coding sessions. It prevents coding agents from reporting tasks as finished without proving correctness through live compiler checks, test runner executions, and diff audits.

### Core Disciplines

* **Evidence Over Assumptions:** Forbids declaring victory based on speculative hope. Every code modification must be verified via deterministic compiler checks and test assertions.
* **Surgical TDD Protocol:** Enforces behavioral testing against public module interfaces, ensuring tests validate business logic rather than private implementation details.
* **Deterministic Diff Audit:** Scrutinizes `git diff` outputs before completion to guarantee zero accidental modifications, commented-out dead code, or exposed credentials.

---

## Installation

### Windows (PowerShell)
```powershell
git clone https://github.com/Skill-AI-private/autonomous-task-verifier.git "$HOME\.gemini\config\skills\autonomous-task-verifier"
```

### macOS & Linux (Bash)
```bash
git clone https://github.com/Skill-AI-private/autonomous-task-verifier.git ~/.gemini/config/skills/autonomous-task-verifier
```

---

## Directory Structure

```text
autonomous-task-verifier/
|-- SKILL.md                                           # Core Verification & Quality Gate Rules
|-- README.md                                          # Technical specification
`-- references/                                        # Progressive disclosure playbooks
    |-- 01-tdd-red-green-loop.md                      # TDD vertical slice cycles & anti-patterns
    |-- 02-five-axis-code-review.md                   # 5-Axis engineering & security audit
    `-- 03-pre-completion-verification-gates.md       # Typecheck, diff audit & summary format
```

---

<div align="center">

*Engineered for autonomous software agents within the Skill-AI-private suite.*

</div>
