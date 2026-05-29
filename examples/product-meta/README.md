# Product Meta Workspace Example

This is a generic example of a meta repository for AI-assisted product engineering.

It mirrors the workflow described in the handbook without depending on any specific product.

## Purpose

Use this repository shape to keep planning, specifications, tickets, handovers, lessons, and archives outside the implementation repositories.

Implementation stays in product repos.

Planning and coordination live here.

## Correct Structure

Lanes are the top-level work modes.

Each lane owns its own plans, specs, and tickets.

```text
product-meta/
  AGENTS.md
  README.md
  session-log.md

  product/
    plans/
    specs/
    tickets/
    archive/

  coding/
    plans/
    specs/
    tickets/
    archive/

  ui-ux/
    plans/
    specs/
    tickets/
    archive/

  marketing/
    plans/
    specs/
    tickets/
    archive/

  release/
    plans/
    specs/
    tickets/
    archive/

  handovers/
    coding/
    ui-ux/
    release/
    archive/

  verification/
    scripts/
    reports/
    archive/

  lessons/
    lessons-learned.md
    rules.md

  templates/
    ticket.md
    handover.md
    verification.md
```

## Lane Rule

A lane gives the AI its role, personality, and output shape.

The lane decides how the work should be approached before planning starts.

Examples:

- `product/` is for user value, scope, tradeoffs, and product decisions.
- `coding/` is for implementation plans, technical specs, and executable coding tickets.
- `ui-ux/` is for flows, screens, copy, and usability work.
- `marketing/` is for positioning, content, launch messaging, and distribution.
- `release/` is for rollout plans, release risk, checklists, and launch coordination.

## Flow

```text
Lane
-> Brainstorming
-> Plan
-> Spec
-> Ticket
-> Human Ticket Review
-> Handover
-> Execution in implementation repo
-> Verification
-> Human Review
-> Merge
-> Memory Update
-> Archive
```

## Rule

The meta repository coordinates work.

It does not implement product code.

Keep active lane folders small.

Move completed, stale, or superseded work into that lane's `archive/` folder.
