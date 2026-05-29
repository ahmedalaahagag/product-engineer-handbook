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

## Rule

Do not ask the execution agent to infer the whole product.

Give it a clear slice of work.
