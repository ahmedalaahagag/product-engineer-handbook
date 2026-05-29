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

| Problem | Common AI Workflow | Product Engineer Handbook |
|---|---|---|
| Context growth | One chat grows forever | Context is externalized into artifacts |
| Cost | Premium models used for everything | Expensive models are reserved for reasoning-heavy work |
| Continuity | Important knowledge is trapped in chat history | Plans, specs, tickets, handovers, and lessons preserve state |
| Execution quality | Vague prompts produce vague changes | Tickets become small, scoped, and verifiable |
| Review discipline | AI output is trusted too early | Human review and manual merge remain mandatory |
| Scaling | One overloaded session handles everything | Work is split across lanes, tickets, and focused sessions |
| Tool dependence | Workflow depends on one model or vendor | Artifacts can be used by Claude, Codex, Cursor, Gemini, local models, or future tools |
| Product delivery | AI helps with isolated tasks | The workflow connects idea, planning, implementation, review, and shipping |

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

Start here if you want to copy the workflow into your own project.

1. [Context Management](docs/context-management.md) — why sessions should be disposable and knowledge should live in files.
2. [What Worked](docs/what-worked.md) — the patterns that consistently improved AI-assisted delivery.
3. [What Failed](docs/what-failed.md) — the traps that wasted time or created risk.
4. [Delivery Loop](docs/delivery-loop.md) — the full operating loop from idea to shipped change.
5. [Meta Repository Pattern](docs/meta-repo-pattern.md) — how to separate planning and coordination from implementation repos.
6. [Surface Mapping](docs/surface-mapping.md) — how to avoid backend-only or frontend-only thinking by mapping affected product surfaces.
7. [Ticket Quality](docs/ticket-quality.md) — why small, scoped, verifiable tickets improve AI execution.
8. [Execution Handover](docs/execution-handover.md) — how to pass focused work from planning to implementation.
9. [Cheap Model Delegation](docs/cheap-model-delegation.md) — how to reserve expensive models for reasoning and use cheaper models for bounded execution.
10. [Worktree Isolation](docs/worktree-isolation.md) — how to keep agent work isolated and safe.
11. [Human Review and Manual Merge](docs/human-review-and-manual-merge.md) — why humans remain the final approval gate.
12. [Session Log](docs/session-log.md) — how to preserve cross-session and cross-agent continuity.
13. [Lessons To Rules](docs/lessons-to-rules.md) — how to turn repeated lessons into standing rules.
14. [Ticket Template](templates/ticket.md) — reusable structure for AI-executable work.
15. [Handover Template](templates/handover.md) — reusable structure for execution handoffs.
16. [Verification Template](templates/verification.md) — reusable structure for proving a change is done.

## Core Principle

AI systems generate work.

Humans own decisions.

The final responsibility always belongs to the engineer.

## Mission

Make context disposable, knowledge persistent, token usage efficient, and engineering ownership explicit.
