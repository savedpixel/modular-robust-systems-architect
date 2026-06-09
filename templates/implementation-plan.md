# Implementation Plan Template

## Implementation Objective

Implement `[target]` with modular boundaries and scoped robustness while preserving `[compatibility requirement]`.

## Ordered Tasks

### Task 1: Add safety harness

Change:

- `[test/schema/contract file]`

Verify:

- `[command]`

Stop if:

- `[current behavior cannot be characterized]`

### Task 2: Introduce or strengthen the contract

Change:

- `[interface/schema/type/route/event/config]`

Verify:

- `[contract/schema/typecheck command]`

Stop if:

- `[consumer compatibility breaks]`

### Task 3: Create the module seam

Change:

- `[application service/domain service/port/adapter]`

Verify:

- `[unit/integration command]`

Stop if:

- `[dependency direction becomes worse]`

### Task 4: Move behavior behind the seam

Change:

- `[implementation files]`

Verify:

- `[regression command]`

Stop if:

- `[parity fails]`

### Task 5: Add robustness behavior

Change:

- `[validation/error/idempotency/retry/observability files]`

Verify:

- `[failure-mode tests]`

Stop if:

- `[failure behavior is ambiguous]`

### Task 6: Clean up and document

Change:

- `[docs/exports/deprecated path cleanup]`

Verify:

- `[full relevant check]`

Stop if:

- `[transitional compatibility still needed]`

## Rollback Plan

- `[rollback step]`
- `[feature flag/compatibility path/backout instruction]`

## Final Verification

- `[unit tests]`
- `[integration tests]`
- `[contract/schema tests]`
- `[migration/parity tests]`
- `[manual smoke check]`
