# Product Engineer Handbook

A field manual from building Suvo: from idea to shipped product with efficient tokens, controlled context, and strong engineering ownership.

This handbook documents a practical operating model for AI-assisted product engineering. It is designed for builders who want to use AI for planning, specification, implementation, review, and delivery without turning the project into one giant chat session.

The goal:

> Move from rough idea to real product through lanes, brainstorming, plans, specs, tickets, handovers, verification, human review, and persistent project memory.

AI is leverage. The engineer remains accountable.

## Origin

This handbook is based on my experience building [Suvo](https://getsuvo.com), a real supplement tracking product, as a solo product engineer using AI-assisted workflows.

Suvo forced this workflow into existence.

The project involved multiple repos, mobile and backend work, product decisions, app-store review, marketing, release planning, verification, and limited time. A single long-running AI chat was not enough. I needed lanes, specs, tickets, handovers, deterministic verification, archives, and persistent project memory.

This repository is the cleaned-up version of that system.

It is not theory. It is a field manual from building a real product while trying to control cost, context, quality, and execution.

## What You Gain

| Problem | Common AI Workflow | Product Engineer Handbook |
|---|---|---|
| Context growth | One chat grows forever | Context is externalized into artifacts |
| Cost | Premium models are used for everything | Expensive models are reserved for reasoning-heavy work |
| Continuity | Knowledge is trapped in chat history | Plans, specs, tickets, handovers, and lessons preserve state |
| Execution quality | Vague prompts produce vague changes | Tickets are small, scoped, and verifiable |
| Review discipline | AI output is trusted too early | Human review and manual merge stay mandatory |
| Scaling | One overloaded session handles everything | Work is split across lanes, tickets, and focused sessions |
| Tool dependence | Workflow depends on one model or vendor | Artifacts work across Claude, Codex, Cursor, Gemini, local models, or future tools |
| Product delivery | AI helps with isolated tasks | The workflow connects idea, planning, implementation, review, and shipping |

## Product Engineering Loop

```text
Idea
-> Goal
-> Lane
-> Brainstorming
-> Plan
-> Plan Review
-> Specification
-> Specification Review
-> Ticket Decomposition
-> Human Ticket Review
-> Execution Handover
-> Execution Model Selection
-> Execution
-> Verification
-> AI Review
-> Human Review
-> Manual Merge
-> Memory Update
-> Archive Completed Context
-> Next Ticket
```

## Lanes

A lane gives the AI its working mode: role, priorities, tone, and expected output.

Examples:

- `product` focuses on user value, scope, tradeoffs, and release shape.
- `coding` focuses on implementation, tests, maintainability, and verification.
- `ui-ux` focuses on flows, screens, copy, and usability.
- `marketing` focuses on positioning, messaging, and distribution.
- `release` focuses on rollout, risk, checklists, and launch coordination.

Lanes stop every task from becoming a coding task.

## Context and Token Efficiency

AI work gets expensive and unreliable when every session carries the entire project history.

This workflow keeps durable context in files:

- plans
- specifications
- tickets
- handovers
- session logs
- lessons learned
- agent instructions
- archive folders

Expensive reasoning models clarify the work. Focused execution models receive bounded tasks.

## Planning and Specification Support

Planning and specification work benefit from structured reasoning.

In my own workflow, I use the Superpowers skill system for brainstorming, plan writing, specification drafting, and specification review.

Execution should receive a refined handover, not the entire brainstorming history.

## Example Meta Workspace

See [examples/product-meta](examples/product-meta) for a generic meta repository structure that mirrors this workflow.

The canonical shape is:

```text
product-meta/
  product/{plans,specs,tickets,archive}/
  coding/{plans,specs,tickets,archive}/
  ui-ux/{plans,specs,tickets,archive}/
  marketing/{plans,specs,tickets,archive}/
  release/{plans,specs,tickets,archive}/
  handovers/
  verification/
  lessons/
  templates/
```

Use it as a starting point for your own product meta workspace.

## Recommended Reading Order

Start here if you want to copy the workflow.

1. [Context Management](docs/context-management.md) — make sessions disposable and knowledge durable.
2. [What Worked](docs/what-worked.md) — patterns that improved AI-assisted delivery.
3. [What Failed](docs/what-failed.md) — traps that wasted time or created risk.
4. [Delivery Loop](docs/delivery-loop.md) — the full loop from idea to shipped change.
5. [Meta Repository Pattern](docs/meta-repo-pattern.md) — separate planning from implementation repos.
6. [Surface Mapping](docs/surface-mapping.md) — map affected product surfaces before execution.
7. [Ticket Quality](docs/ticket-quality.md) — make tickets small, scoped, and verifiable.
8. [Execution Handover](docs/execution-handover.md) — pass focused work into implementation.
9. [Cheap Model Delegation](docs/cheap-model-delegation.md) — reserve expensive models for reasoning.
10. [Worktree Isolation](docs/worktree-isolation.md) — isolate agent work safely.
11. [Deterministic Verification](docs/deterministic-verification.md) — use pre-push gates for format, vet, lint, and tests.
12. [Human Review and Manual Merge](docs/human-review-and-manual-merge.md) — keep humans as the final approval gate.
13. [Session Log](docs/session-log.md) — preserve continuity across sessions.
14. [Lessons To Rules](docs/lessons-to-rules.md) — turn repeated lessons into standing rules.
15. [Archive Strategy](docs/archive-strategy.md) — keep active context small as artifacts grow.
16. [Ticket Template](templates/ticket.md) — structure executable work.
17. [Handover Template](templates/handover.md) — structure execution handoffs.
18. [Verification Template](templates/verification.md) — prove that work is done.

## Core Principle

AI systems generate work.

Humans own decisions.

The final responsibility always belongs to the engineer.

## Mission

Make context disposable, knowledge persistent, token usage efficient, and engineering ownership explicit.
