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

- one task
- small
- scoped
- verifiable
- easy to review
- connected to a plan or specification
- explicit about the files or surfaces to inspect first

## One Ticket, One Task

A ticket should describe one bounded task.

If the work has multiple independent outcomes, split it into multiple tickets.

A good execution ticket should be simple enough that the task can be understood without rediscovering the whole repository.

## Exact Files First

Every coding ticket should list the exact files or surfaces the execution session should inspect first.

Prefer this:

```text
Affected files:
- app/onboarding/index.tsx
- lib/onboarding-store.ts
```

Avoid this:

```text
Find the onboarding files and fix persistence.
```

Exact files reduce token usage, reduce broad repository exploration, and prevent unrelated changes.

If the exact files are not known yet, create a discovery ticket first instead of making the implementation ticket open-ended.

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

Give it one clear, verifiable slice of work with the exact files or surfaces to inspect first.
