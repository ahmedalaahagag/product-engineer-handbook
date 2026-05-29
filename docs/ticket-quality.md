# Ticket Quality

Ticket quality is one of the strongest predictors of AI execution quality.

A vague ticket produces a vague implementation.

A focused ticket produces a focused implementation.

## Bad Ticket

```text
Build onboarding.
```

Why this fails:

- scope is too large
- affected files are unknown
- acceptance criteria are unclear
- verification is undefined
- the executor may redesign the product

## Good Ticket

```text
Persist onboarding progress after app restart.

Affected files:
- app/onboarding/index.tsx
- lib/onboarding-store.ts

Acceptance criteria:
- progress survives app restart
- user resumes from the last completed step
- existing onboarding flow still works

Verification:
- restart the app during onboarding
- confirm the user returns to the correct step
```

## Good tickets are

- small
- scoped
- verifiable
- easy to review
- connected to a plan or specification

## Multi-Ticket Plans

A plan may produce multiple tickets.

Each ticket should land in the correct lane's `tickets/` directory.

For example:

```text
product/plans/P1-onboarding-improvements.md
product/tickets/T-001-activation-copy.md
ui-ux/tickets/T-002-onboarding-flow-polish.md
coding/tickets/T-003-persist-onboarding-progress.md
release/tickets/T-004-beta-rollout-checklist.md
```

Do not keep generated tickets beside the plan unless the plan and every ticket belong to the same lane.

The lane owns the execution context for the ticket.

## Rule

Do not ask the execution agent to infer the whole product.

Give it a clear slice of work.
