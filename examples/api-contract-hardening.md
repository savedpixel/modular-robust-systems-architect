# Example: API Contract Hardening

```text
Use the modular-robust-systems-architect skill.

Harden the public API for project invitations. Ask what clients depend on today, what error formats must remain stable, and what validation should change. Then inspect routes, request schemas, service methods, permissions, tests, and docs. Produce a modular contract-first implementation plan.
```

Expected agent focus:

- separate route/controller concerns from application service behavior
- validate request shape at the boundary
- keep permission checks explicit
- preserve stable response and error contracts
- add contract and integration tests
- avoid changing unrelated API routes
