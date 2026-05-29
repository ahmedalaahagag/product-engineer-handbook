# What Worked

These are the patterns that consistently improved AI-assisted product delivery.

## Separate planning from execution

Use reasoning-heavy sessions for thinking, planning, architecture, and specification.

Use focused execution sessions for implementation.

This keeps expensive reasoning where it matters and prevents implementers from redesigning the whole product.

## Small tickets

Small tickets produce better AI output.

A good ticket is narrow, scoped, and independently verifiable.

## Explicit handovers

Do not rely on chat memory.

A handover should contain the target repo, task, constraints, files to inspect first, verification steps, and stop conditions.

## Verification passes

Generated work should be checked before it is trusted.

Verification can include tests, type checks, linting, manual smoke checks, or product-behavior review.

## Repository memory

Important lessons should be written down and reused.

If a lesson changes future behavior, promote it into a standing rule.

## Context resets

Fresh context often outperforms massive historical context.

The goal is not to keep one session alive forever.

The goal is to make the next session easy to restart.
