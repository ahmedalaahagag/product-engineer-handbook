# Surface Mapping

## Problem

AI plans often treat changes as isolated.

A backend change may affect mobile, web, ops, analytics, docs, or release flows.

## Rule

Before writing a serious plan or ticket, map the affected surfaces by literal filename.

Avoid vague labels like:

- dashboard
- onboarding
- API layer

Prefer concrete references like:

- `app/onboarding/index.tsx`
- `server/handler/dashboard.go`
- `app/catalog/[id]/page.tsx`

## Benefit

Surface mapping prevents correct-in-isolation changes that break the product end to end.

It also gives execution agents a smaller and more accurate file set.
