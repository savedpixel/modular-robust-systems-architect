# Example: Modular Feature Build

```text
Use the modular-robust-systems-architect skill.

We need to implement organization-level usage limits. Before touching code, ask me what limit types exist, where enforcement should happen, which consumers depend on usage state, and what behavior must remain compatible. Then inspect the relevant usage tracking, permissions, API, storage, and tests. Give me one modular architecture and implementation plan with verification gates before coding.
```

Expected agent focus:

- clarify limit semantics and failure behavior
- locate current usage tracking and enforcement points
- define the source of truth for plans, limits, and usage state
- separate public API, application service, domain rules, persistence, and reporting concerns
- design validation and compatibility behavior
- implement in small slices after approval
- verify with unit, integration, and regression tests
