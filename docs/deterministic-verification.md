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
-> vet
-> lint
-> test
-> push allowed only if checks pass
```

## Core Checks

A minimal deterministic gate should run:

- format
- vet
- lint
- tests

For example:

```bash
./scripts/verify.sh
```

The exact commands depend on the stack, but the contract should stay stable.

For a Go service, that might mean:

```bash
gofmt/goimports check
go vet ./...
golangci-lint run
go test ./...
```

For a web or mobile repo, the same idea applies with the repo's own formatter, type checker, linter, and test runner.

## Why Deterministic Matters

The gate should not depend on model judgment.

It should produce a clear pass or fail.

AI can explain failures and propose fixes, but the verification gate itself should be deterministic.

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

The command becomes part of the contract between planning, execution, review, and merge.
