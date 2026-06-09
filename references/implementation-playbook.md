# Implementation Playbook

## Step 1: Characterize current behavior

Before moving responsibilities, prove what the system currently does. Add tests or document existing commands when behavior is risky or under-tested.

## Step 2: Strengthen or create the contract

Define the boundary shape before changing internals. This can be a type, interface, schema, route contract, event, package export, config format, or adapter protocol.

## Step 3: Introduce the seam

Create the module seam where behavior will live. Keep the first seam small. It should be easy to test and easy to remove if the assumption is wrong.

## Step 4: Move one vertical slice

Move enough behavior to prove the boundary works end to end. Avoid moving everything at once.

## Step 5: Add targeted robustness

Add validation, typed errors, idempotency, retries, timeouts, transactions, permissions, observability, or migration support only where the target needs it.

## Step 6: Verify parity and compatibility

Run tests and compare outputs. For generated or normalized systems, use snapshots or golden-output diffs. For migrations, run dry runs or compatibility tests.

## Step 7: Clean up transitional paths

Remove duplicate code, deprecated exports, flags, adapters, or compatibility layers only after parity and rollout are proven.

## Stop conditions

Pause implementation when:

- the source of truth is unclear
- public contract compatibility is unknown
- current behavior cannot be characterized
- generated files might be edited incorrectly
- migration risk is higher than expected
- tests reveal behavior the plan did not account for
- the implementation requires unrelated rewrites
