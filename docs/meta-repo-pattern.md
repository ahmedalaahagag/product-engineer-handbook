# Meta Repository Pattern

## Problem

Planning, implementation, review, and architecture often get mixed together.

That creates noisy context, weak boundaries, broad repository scans, and expensive execution.

In multi-repo products, this gets worse because backend, mobile, web, and infrastructure work may all move independently.

## Pattern

Use a dedicated meta repository for:

- plans
- specs
- tickets
- handovers
- lessons
- architecture notes
- verification notes
- project memory

Keep implementation in the actual product repositories.

The meta repository coordinates the work.

The execution repositories contain the code.

## Workspace Shape

A typical workspace keeps the meta repository beside the implementation repositories.

```text
workspace/
  product-meta/       # planning, tickets, handovers, memory
  product-server/     # backend implementation
  product-mobile/     # mobile implementation
  product-web/        # web app, landing page, or marketing site
```

## Execution Boundary

Planning and review can happen in the meta repository.

Execution should start in the target implementation repository.

The execution model should receive a focused handover, not the full planning history.

A good handover names:

- the target repository
- the task objective
- exact files or surfaces to inspect first
- scope rules
- acceptance criteria
- verification steps
- stop conditions

## Benefits

- smaller execution context
- clearer ownership
- better cross-repo coordination
- reusable planning artifacts
- lower token cost
- fewer unrelated code changes
- easier human review
