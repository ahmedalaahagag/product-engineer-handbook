# Delivery Loop

The delivery loop is the operating model for taking an idea to a shipped product change.

It is not fully autonomous.

The human engineer owns direction, architecture, quality, and final approval.

## Loop

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
-> Execution
-> Verification
-> Human Review
-> Manual Merge
-> Memory Update
```

## Start with the outcome

Do not start with a prompt.

Start with the outcome.

A good goal defines:

- user value
- product boundary
- technical boundary
- success condition

## Route work into a lane

Lanes prevent every task from becoming a coding task.

Common lanes:

- product
- coding
- ui-ux
- marketing
- operations
- release

## Use specs for reasoning

The specification explains what should happen and why.

It includes context, decisions, scope, non-goals, affected systems, risks, and acceptance criteria.

This is where expensive reasoning belongs.

## Use tickets for execution

The spec is broken into small execution units.

The execution agent should not redesign the whole product.

It should execute a bounded ticket.

## Verify before trust

Every ticket needs an explicit verification path.

The point is not that everything is automated.

The point is that correctness must be checked.

## Keep the loop honest

The loop exists to ship.

If maintaining the loop becomes more important than shipping product, simplify it.
