# Archive Strategy

## Problem

Planning repositories grow quickly.

Plans, specs, tickets, handovers, session logs, and lessons are useful, but they can become noisy if everything stays active forever.

Large active folders create problems:

- slower navigation
- more irrelevant context
- higher token usage
- harder retrieval
- more stale instructions
- confusing active state

## Pattern

Keep active work small.

Move completed or stale artifacts into an archive.

## What To Archive

Archive artifacts when they are:

- shipped
- superseded
- abandoned
- no longer relevant to active execution
- useful historically but not needed in daily context

Common archive candidates:

- old plans
- shipped specs
- completed tickets
- stale handovers
- old session logs
- deprecated decisions

## What Should Stay Active

Keep active folders limited to work that can influence the next session.

Active files should answer:

- what are we doing now?
- what is blocked?
- what is next?
- what rules affect current execution?

## Why This Helps AI

AI agents should not scan months of dead planning history.

Archiving reduces irrelevant context and makes the current project state easier to reconstruct.

## Rule

If an artifact is useful for history but harmful to current focus, archive it.

The active workspace should represent the current product state, not the entire archaeology of the project.
