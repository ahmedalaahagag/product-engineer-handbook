# Execution Handover

## Purpose

Execution should not begin from a messy planning chat.

It should begin from a focused handover.

## Handover Contents

A good handover includes:

- target repository
- task objective
- scope rules
- files to inspect first
- relevant plan or spec reference
- acceptance criteria
- verification steps
- stop conditions

## Stop Conditions

The execution agent should stop if:

- the required files do not exist
- the task crosses unexpected boundaries
- the plan is ambiguous
- tests fail for unclear reasons
- security or data-loss risk appears

## Benefit

The executor receives a bounded task instead of the full reasoning history.

This reduces cost and improves output quality.
