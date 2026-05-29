# Product Engineer Handbook

From idea to full product with efficient tokens, controlled context, and strong engineering ownership.

This repository documents a practical product engineering operating model for using AI without turning the project into one giant chat session.

The goal is simple:

> Take an idea from rough concept to shipped product using plans, specs, tickets, handovers, verification, human review, and persistent project memory.

AI is used as leverage. The engineer remains accountable.

## Product Engineering Loop

```text
Idea
-> Goal
-> Lane
-> Plan
-> Plan Review
-> Specification
-> Specification Review
-> Ticket Decomposition
-> Ticket Review
-> Execution Handover
-> Execution Model Selection
-> Execution
-> Verification
-> AI Review
-> Human Review
-> Manual Merge
-> Memory Update
-> Next Ticket
```

## What You Gain

- smaller AI contexts
- lower model costs
- clearer handoffs
- better ticket quality
- stronger review discipline
- tool-agnostic project memory
- less dependency on one long-running chat session
- a repeatable path from idea to product

## Why Token and Context Efficiency Matter

AI work gets expensive and unreliable when every session carries the entire project history.

This handbook pushes context into durable artifacts:

- plans
- specifications
- tickets
- handovers
- session logs
- lessons learned
- agent instructions

The result is a workflow where expensive reasoning models clarify the work, and cheaper or focused models execute bounded tasks.

## Recommended Reading Order

1. `docs/context-management.md`
2. `docs/meta-repo-pattern.md`
3. `docs/surface-mapping.md`
4. `docs/execution-handover.md`
5. `docs/cheap-model-delegation.md`
6. `docs/worktree-isolation.md`
7. `docs/human-review-and-manual-merge.md`
8. `docs/session-log.md`
9. `docs/lessons-to-rules.md`
10. `templates/ticket.md`
11. `templates/handover.md`
12. `templates/verification.md`

## Core Principle

AI systems generate work.

Humans own decisions.

The final responsibility always belongs to the engineer.

## Mission

Make context disposable, knowledge persistent, token usage efficient, and engineering ownership explicit.
