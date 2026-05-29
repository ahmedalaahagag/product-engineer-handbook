# Worktree Isolation

## Problem

Multiple AI sessions working in the same checkout can collide.

Common failures:

- unrelated modified files
- accidental commits
- dirty working tree confusion
- duplicate implementation work
- branch contamination

## Rule

One ticket.

One branch.

One worktree.

## Benefits

- safer execution
- cleaner reviews
- easier rollback
- better parallel work
- less risk from agent mistakes
