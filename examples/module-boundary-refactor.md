# Example: Module Boundary Refactor

```text
Use the modular-robust-systems-architect skill.

Refactor the notifications module. It currently mixes templates, user preferences, delivery orchestration, provider adapters, retries, and audit logging. Ask purpose and compatibility questions first, then inspect the module lifecycle and tests. Recommend a boundary-first architecture and a safe implementation sequence.
```

Expected agent focus:

- define what the notifications module owns
- define what provider adapters own
- keep external provider SDK details out of domain rules
- preserve existing public calls until migration is complete
- add tests around current behavior before moving responsibilities
- add retry, idempotency, and audit behavior only where needed
