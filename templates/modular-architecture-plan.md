# Modular Architecture Plan Template

## 1. Scope

Target: `[feature/module/service/workflow/API/integration/data model/tool]`

Goal: `[user/operator/developer outcome]`

Non-scope:

- `[explicit exclusion]`

Assumptions:

- `[assumption and why it is safe]`

## 2. Evidence Scanned

Files and folders:

- `[path]`

Symbols or contracts:

- `[function/class/interface/schema/route/event/config]`

Commands or tests:

- `[command]`

Not found:

- `[missing evidence]`

## 3. Current Lifecycle

```text
[input/source]
  -> [boundary validation]
  -> [orchestration/application service]
  -> [domain rule]
  -> [adapter/persistence/provider]
  -> [output/side effect]
  -> [observability]
```

Current source of truth: `[file/schema/model/service/config/database/event]`

Current boundary issues:

- `[issue tied to evidence]`

## 4. Target Modular Architecture

Recommended architecture:

```text
[entry point]
  -> [contract/schema]
  -> [application/use-case service]
  -> [domain model/rules]
  -> [ports]
  -> [adapters]
  -> [storage/provider/output]
```

Module owns:

- `[responsibility]`

Module must not own:

- `[responsibility]`

Public contracts:

- `[contract]`

Private internals:

- `[internal detail]`

Dependency direction:

- `[rule]`

Composition root or wiring location:

- `[path]`

## 5. Robustness Design

Validation:

- `[boundary validation]`

Errors and failure modes:

- `[error/failure behavior]`

Idempotency and retries:

- `[retry-safe design]`

Consistency and migration:

- `[compatibility/migration plan]`

Security and permissions:

- `[trust boundary]`

Observability:

- `[logs/metrics/traces/audit/health checks]`

## 6. Implementation Phases

1. `[phase name]`
   - Change: `[files]`
   - Verify: `[command/test/check]`
   - Stop if: `[risk condition]`

2. `[phase name]`
   - Change: `[files]`
   - Verify: `[command/test/check]`
   - Stop if: `[risk condition]`

3. `[phase name]`
   - Change: `[files]`
   - Verify: `[command/test/check]`
   - Stop if: `[risk condition]`

## 7. Acceptance Criteria

- `[observable success condition]`
- `[test or contract condition]`
- `[compatibility condition]`
- `[operational condition]`
