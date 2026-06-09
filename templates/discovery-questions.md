# Discovery Questions Template

Use this before scanning or editing. Select only questions that materially affect the architecture or implementation.

## First response pattern

I need to narrow the implementation target before touching the project:

1. What exact feature, module, service, workflow, API, integration, data model, or tool should be built or changed?
2. What outcome matters most: cleaner boundaries, safer implementation, easier extension, stronger validation, better failure handling, lower coupling, or lower migration risk?
3. What current behavior, public contract, data shape, API, config, workflow, or deployment path must remain compatible?
4. Which consumers use this path today: UI, API, worker, CLI, automation, provider, data pipeline, tests, or operators?
5. What robustness risks matter most: invalid input, partial failure, retries, concurrency, permissions, observability, performance, migration, or rollback?
6. Do you want an implementation-ready plan first, or should code changes follow after the plan is approved?

## Evidence-based follow-up patterns

Ask follow-up questions after scanning only when the answer changes the implementation.

### Competing ownership found

I found two places that appear to own the same responsibility:

- `[path or symbol 1]`
- `[path or symbol 2]`

Which one is authoritative, or is one legacy?

### Public contract risk found

The target touches `[API/event/config/database/package export]`. What level of backward compatibility is required for existing consumers?

### Generated/manual boundary unclear

`[file or folder]` looks generated or derived. Should it be treated as generated output, human-maintained source, or temporary migration output?

### Robustness decision needed

The workflow can fail after `[side effect]` but before `[state update]`. Should the implementation prioritize idempotent retry, compensation, manual repair state, or fail-fast behavior?

### Missing safety harness found

I did not find tests around `[behavior]`. Should the implementation add a characterization test before refactoring, or is a direct change acceptable?

### External dependency found

This touches `[provider/API/tool]`. Are there constraints for authentication, rate limits, timeouts, retries, idempotency, audit logs, or operator alerts?
