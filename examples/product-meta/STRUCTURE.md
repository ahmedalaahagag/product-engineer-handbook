# Canonical Example Structure

The example meta workspace follows this shape:

```text
product-meta/
  product/
    plans/
    specs/
    tickets/
    archive/

  coding/
    plans/
    specs/
    tickets/
    archive/

  ui-ux/
    plans/
    specs/
    tickets/
    archive/

  marketing/
    plans/
    specs/
    tickets/
    archive/

  release/
    plans/
    specs/
    tickets/
    archive/

  handovers/
  verification/
  lessons/
  templates/
```

## Rule

Every lane has the same core folders:

```text
plans/
specs/
tickets/
archive/
```

Brainstorming happens before planning, but it does not need to be a permanent top-level folder in every lane.

Keep active lane folders small.

Move completed or stale work into `archive/`.
