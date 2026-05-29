# Deterministic Verification

## Problem

AI-generated work can look correct while still breaking the product.

Human review helps, but it should not be the first line of defense.

## Pattern

Use a deterministic verification script that runs the same checks every time.

Then connect it to a pre-push git hook.

```text
git push
-> pre-push hook
-> ./scripts/verify.sh
-> format
-> type check
-> lint
-> build
-> tests
-> push allowed only if checks pass
```

## What The Script Should Check

A typical verification script includes:

- formatting
- type checking
- linting
- build
- unit tests
- integration tests where practical
- generated-code consistency
- documentation or schema checks when relevant

## Why Deterministic Matters

The script should not depend on model judgment.

It should produce a clear pass or fail.

AI can explain failures, but the gate itself should be deterministic.

## Why Pre-Push

Pre-push is late enough that local iteration stays fast.

It is early enough to stop broken work before it reaches the remote branch.

## Benefits

### Lower review cost

Reviewers spend less time finding basic failures.

### Better AI feedback loops

Failed checks create concrete error output that an agent can fix.

### Safer delegation

You can delegate implementation more confidently when every change must pass the same gate.

### Less CI waste

Broken work is stopped locally before remote CI spends time and money.

### Stronger ownership

The engineer defines the quality gate instead of trusting model confidence.

## Rule

Every execution ticket should say which verification command proves the work is done.

For example:

```bash
./scripts/verify.sh
```

The command becomes part of the contract between planning, execution, review, and merge.
