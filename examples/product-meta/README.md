# Product Meta Workspace Example

This is a generic example of a meta repository for AI-assisted product engineering.

It mirrors the workflow described in the handbook without depending on any specific product.

## Purpose

Use this repository shape to keep planning, specifications, tickets, handovers, lessons, and archives outside the implementation repositories.

Implementation stays in product repos.

Planning and coordination live here.

## Example Structure

```text
product-meta/
  AGENTS.md
  README.md
  session-log.md
  product/
    brainstorming/
    plans/
    specs/
    tickets/
    archive/
  coding/
    plans/
    specs/
    tickets/
    handovers/
    verification/
    archive/
  ui-ux/
    brainstorming/
    specs/
    tickets/
    archive/
  marketing/
    brainstorming/
    plans/
    archive/
  release/
    checklists/
    notes/
    archive/
  lessons/
    lessons-learned.md
    rules.md
  templates/
    ticket.md
    handover.md
    verification.md
```

## Rule

The meta repository coordinates work.

It does not implement product code.

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
