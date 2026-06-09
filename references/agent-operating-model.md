# Agent Operating Model

This skill uses a conversation-first, evidence-backed, implementation-focused operating model.

## 1. Ask before work begins

The agent must ask targeted questions before scanning or editing. The purpose is not to slow the user down; it is to prevent the agent from implementing the wrong architecture.

Good questions are specific to the user's target. They clarify goal, compatibility, consumers, risk, robustness expectations, and desired output.

## 2. Scan after initial answers

The agent should inspect only the relevant project evidence. It should map the lifecycle, contracts, module boundaries, dependency direction, tests, commands, and consumers.

The scan should be narrow first. Widen only when dependencies require it.

## 3. Ask evidence-based follow-ups

After scanning, the agent may ask more questions. These should come from evidence: competing implementations, unclear source of truth, generated files, missing tests, risky migrations, hidden consumers, or external provider constraints.

Do not ask follow-up questions that can be answered by reading the project.

## 4. Design the boundary

The agent should define the module boundary before implementation. It should identify ownership, public contracts, private internals, dependency direction, source of truth, adapters, and composition root.

## 5. Design robustness where failure exists

The agent should add robustness mechanisms only where they address an observed or likely failure mode. Robustness should include validation, error handling, idempotency, retries, consistency, permissions, observability, and migration safety when relevant.

## 6. Implement in slices

Once implementation is approved, the agent should change the system in small, verifiable phases. A good phase introduces a safety harness, a contract, a seam, a vertical behavior slice, or a cleanup step.

## 7. Verify and stop safely

Every phase should have a verification command or explicit check. If a stop condition is triggered, the agent should pause and report the risk instead of forcing changes through.
