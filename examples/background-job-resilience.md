# Example: Background Job Resilience

```text
Use the modular-robust-systems-architect skill.

Harden the import worker. It currently fails unpredictably when records are duplicated, provider responses are partial, or the job is retried. Ask about acceptable duplicate behavior, retry limits, data consistency, and operator visibility. Then inspect the worker, queue configuration, persistence layer, provider adapter, and tests. Design and implement a robust modular solution after approval.
```

Expected agent focus:

- define idempotency key and duplicate handling
- separate provider adapter mapping from import domain logic
- define retry-safe and non-retry-safe errors
- add structured failure states
- add tests for retries, partial failures, and repeated inputs
- add observability where operators need it
