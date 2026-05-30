# Delivery Loop

The delivery loop is the operating model for taking an idea to a shipped product change.

It is not fully autonomous.

The human engineer owns direction, architecture, quality, and final approval.

## Loop

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
-> Execution in target repo
-> Verification
-> AI Review
-> Human Review
-> Manual Merge
-> Memory Update
-> Archive Completed Context
-> Next Ticket
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

Core lanes:

- product
- coding
- ui-ux
- marketing
- release

Additional lanes can be added when a product needs them, but the default workflow should stay small.

## Use specs for reasoning

The specification explains what should happen and why.

It includes context, decisions, scope, non-goals, affected systems, risks, and acceptance criteria.

This is where expensive reasoning belongs.

## Use tickets for execution

The spec is broken into small execution units.

One ticket should describe one bounded task.

The execution agent should not redesign the whole product.

It should execute a bounded ticket in the target implementation repository.

## Use handovers to cross the boundary

Planning can happen in the meta repository.

Implementation should start in the target execution repository.

The handover tells the execution model:

- what to do
- which repo to open
- which files or surfaces to inspect first
- what not to touch
- how to verify the result

## Verify before trust

Every ticket needs an explicit verification path.

The point is not that everything is automated.

The point is that correctness must be checked.

## Keep the loop honest

The loop exists to ship.

If maintaining the loop becomes more important than shipping product, simplify it.
