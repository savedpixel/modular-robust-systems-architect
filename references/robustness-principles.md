# Robustness Principles

## Robustness starts at boundaries

Validate untrusted or cross-boundary input before it enters core logic. This includes API requests, events, config, files, CLI arguments, provider responses, database records, generated artifacts, and user-supplied data.

## Failure behavior must be designed

For each side effect or state transition, define what happens when the operation fails before, during, or after the side effect. Decide whether the system retries, compensates, records a repairable state, fails fast, or alerts an operator.

## Idempotency is required for repeatable side effects

Retries, webhooks, imports, external writes, email sends, payment-like flows, provisioning, background jobs, and deployment automation should have idempotency or deduplication where repeat execution can occur.

## Retrying is not always safe

Retry only operations that are safe or made safe. Bound retries. Add timeouts. Preserve context. Make repeated failure visible.

## Consistency must match the domain

Some systems require transactions and immediate consistency. Others can tolerate eventual consistency. The implementation should make the selected consistency model explicit and test it.

## Observability should help operators act

Logs, metrics, traces, audit records, health checks, and status fields should make failures diagnosable. Avoid noisy logging. Never log secrets.

## Robustness must be testable

A robustness mechanism that cannot be verified is not complete. Add tests for invalid input, failure modes, repeated execution, migrations, permission checks, and compatibility where relevant.
