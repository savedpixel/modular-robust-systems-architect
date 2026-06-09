# Example: Robust Service Integration

```text
Use the modular-robust-systems-architect skill.

Integrate a new deployment verification service into our release workflow. Ask about failure ownership, blocking versus reporting behavior, credentials, retries, audit logs, rollout, and rollback. Then inspect the release scripts, CI workflow, deployment docs, and tests. Produce one modular integration design and implementation plan.
```

Expected agent focus:

- keep release orchestration separate from provider-specific client code
- define service contract and adapter behavior
- make timeouts, retries, and failure states explicit
- preserve the existing release path during rollout
- avoid leaking credentials in logs
- provide smoke checks and rollback conditions
