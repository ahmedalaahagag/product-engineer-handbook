# Cheap Model Delegation

## Principle

Do not spend premium reasoning tokens on mechanical work.

Use strong reasoning models for:

- planning
- architecture
- specification writing
- decomposition
- risk analysis
- review

Use cheaper or coding-focused models for:

- bounded implementation
- mechanical refactoring
- test scaffolding
- summarization
- documentation cleanup

## Execution Boundary

Cheap or coding-focused execution models should start from the target implementation repository, not from the meta repository.

The meta repository provides the handover.

The target repository provides the code context.

A good delegation gives the execution model:

- one task
- one target repo
- exact files or surfaces to inspect first
- scope rules
- verification steps
- stop conditions

## Benefit

The expensive model clarifies the work.

The cheaper model executes a bounded task in the correct repo.

This reduces cost without lowering engineering control.
