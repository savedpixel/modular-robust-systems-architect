# Validation and Verification Checklist

Use only the checks relevant to the target.

## Boundary checks

- The public contract is explicit.
- Private internals are not consumed directly.
- Dependency direction is clear.
- Cross-module calls go through the approved seam.
- External providers or legacy formats are behind adapters where needed.

## Contract checks

- Request, response, event, config, file, or generated-output shape is validated.
- Unknown or unsupported fields are handled deliberately.
- Backward compatibility is tested when existing consumers depend on the contract.
- Error responses or failure states are stable where clients depend on them.

## Robustness checks

- Invalid input fails early.
- Side effects are idempotent where retries are possible.
- Retry behavior is bounded and observable.
- Timeouts exist for external calls where relevant.
- Partial failure states are recoverable or visible.
- Permissions are checked before side effects.
- Sensitive values are not logged.
- Migration path has a rollback or stop condition.

## Test checks

- Unit tests prove domain behavior.
- Integration tests prove the boundary.
- Contract or schema tests prove compatibility.
- Migration or parity tests prove safe transition.
- Failure-mode tests cover risky paths.
- Smoke checks cover the runtime path.

## Agent checks

- No unrelated files were refactored.
- No new dependency was added without justification.
- No generated file was manually edited unless confirmed safe.
- Every changed behavior has a verification step.
