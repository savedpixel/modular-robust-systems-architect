# Modular Robust Systems Architect

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Skill](https://img.shields.io/badge/Codex%20Skill-modular--architecture-0F766E)](SKILL.md)
[![AI Agent Workflow](https://img.shields.io/badge/AI%20Agent-robust%20systems-blue)](README.md)

**Modular Robust Systems Architect** is an AI agent skill for building and implementing modular, robust software architecture in real projects.

It is designed for developers who want an agent to slow down before coding, understand the purpose of a change, inspect the relevant codebase evidence, ask better questions, design clean module boundaries, implement incrementally, and verify the result with tests and operational checks.

The skill is intentionally scoped. It should not be applied globally across a project. It activates around a concrete feature, module, service, workflow, data model, integration, API, tool, package, or system boundary.

## What it helps with

Use this skill when you need to:

- build a feature into an existing system without creating tangled dependencies
- implement a new module with clear ownership and stable contracts
- refactor a subsystem into cleaner boundaries without breaking behavior
- integrate a provider, SDK, internal service, CLI, worker, webhook, or automation tool
- harden a fragile workflow with validation, idempotency, error handling, and observability
- design source-of-truth, schema, contract, configuration, or generated-output flows
- migrate legacy behavior behind adapters or compatibility layers
- create an implementation plan another coding agent can execute safely
- turn an architectural idea into small, verifiable code changes

## Why this skill exists

AI coding agents often move too quickly from prompt to code. That can work for small edits, but it fails when the task needs durable architecture. Large changes need a different loop: understand the goal, ask questions, inspect evidence, design the boundary, implement in slices, and verify each step.

This skill gives the agent that loop. It focuses on practical architecture that can be implemented, tested, reviewed, and rolled out.

## Core behavior

The skill makes the agent follow this workflow:

```text
user request
  -> targeted purpose questions
  -> relevant project scan
  -> evidence-based follow-up questions
  -> modular architecture design
  -> robustness design
  -> implementation plan
  -> approved incremental implementation
  -> verification and handoff
```

The agent is instructed to ask before scanning or editing begins, then ask again only when the project scan reveals decisions that would change the implementation.

## What “modular and robust” means here

A modular system has:

- clear ownership boundaries
- stable public contracts
- private internals that are not consumed directly
- explicit dependency direction
- adapters around external systems and legacy formats where needed
- a named source of truth for core concepts
- tests that prove the boundary works

A robust system has:

- early validation
- deliberate error handling
- safe retry and timeout behavior where relevant
- idempotency for repeatable side effects
- consistency and migration safety
- permission and trust-boundary checks
- useful logs, metrics, traces, or audit records where needed
- verification commands and acceptance criteria

The skill does not force every architecture pattern onto every task. It selects only the mechanisms that the target and evidence justify.

## Installation

Clone or copy the skill folder into a supported skills location.

From GitHub:

```bash
git clone https://github.com/savedpixel/modular-robust-systems-architect.git
mkdir -p ~/.agents/skills
cp -R modular-robust-systems-architect ~/.agents/skills/modular-robust-systems-architect
```

User-level install:

```bash
mkdir -p ~/.agents/skills
cp -R modular-robust-systems-architect ~/.agents/skills/modular-robust-systems-architect
```

Repository-level install:

```bash
mkdir -p .agents/skills
cp -R modular-robust-systems-architect .agents/skills/modular-robust-systems-architect
```

Invoke it explicitly:

```text
Use the modular-robust-systems-architect skill.
```

The included `agents/openai.yaml` disables implicit invocation so the skill is used deliberately instead of being applied to every coding task.

## Compatibility

- Runtime dependencies: none
- Skill format: Codex/OpenAI-style `SKILL.md` with optional `agents/openai.yaml`
- Invocation model: explicit invocation recommended
- License: MIT

## Quick prompt

```text
Use the modular-robust-systems-architect skill.

I want to implement [feature/module/integration/refactor] in [project/repository/system]. Before touching code, ask me the questions needed to understand the goal, constraints, consumers, and robustness requirements. Then inspect the relevant code and give me one modular architecture and implementation plan with tests, stop conditions, and acceptance criteria.
```

## Example prompts

### Build a modular feature

```text
Use the modular-robust-systems-architect skill.

Implement organization-level usage limits. Start by asking what limits must exist, who consumes them, what must remain compatible, and what failure behavior is acceptable. Then inspect the relevant usage tracking, permissions, billing, API, and tests. Produce one modular architecture and an implementation sequence before coding.
```

### Refactor a module boundary

```text
Use the modular-robust-systems-architect skill.

Refactor the notifications module so templates, preferences, provider adapters, retries, and audit logging have clear boundaries. Ask targeted questions first, inspect the current lifecycle, then propose and implement a safe migration plan after approval.
```

### Harden an integration

```text
Use the modular-robust-systems-architect skill.

Harden the webhook ingestion workflow. I want explicit contracts, idempotency, validation, retry-safe processing, useful observability, and tests. Ask what behavior must remain compatible before scanning the code.
```

### Design a configuration or contract system

```text
Use the modular-robust-systems-architect skill.

Redesign our integration manifest flow. The goal is a compact human-owned source, strict validation, normalized generated output, compatibility checks, and runtime consumers that do not read raw config directly. Ask questions first, then inspect the loader, schemas, tests, docs, and consumers.
```

## Expected output

For planning work, the agent should return:

- target scope and non-scope
- initial questions and answered assumptions
- files, symbols, commands, schemas, docs, and tests inspected
- current lifecycle map
- current module boundaries and dependency direction
- observed issues tied to evidence
- one target modular architecture
- robustness design for validation, failures, idempotency, security, observability, and migration where relevant
- ordered implementation phases
- files to change first and files to avoid
- verification commands for each phase
- stop conditions and rollback points
- acceptance criteria

For implementation work, the agent should return:

- files changed
- what boundary or contract was introduced or improved
- what robustness behavior was added or preserved
- tests and checks run
- checks not run and why
- rollout, migration, or compatibility notes
- remaining risks

## Repository structure

```text
modular-robust-systems-architect/
  SKILL.md                         Main skill instructions and metadata
  README.md                        Public documentation and usage guide
  LICENSE                          MIT license
  CONTRIBUTING.md                  Contribution guide
  SECURITY.md                      Security reporting guidance
  CODE_OF_CONDUCT.md               Community conduct standard
  AGENTS.md                        Repository guidance for AI coding agents
  repository-metadata.json         GitHub repository metadata
  agents/openai.yaml               Optional Codex/OpenAI skill metadata
  examples/                        Ready-to-paste prompts
  templates/                       Reusable planning and review templates
  references/                      Architecture and implementation guidance
  .github/                         Issue and pull request templates
```

## GitHub description

AI agent skill for implementing modular, robust software architecture with scoped codebase discovery, clean boundaries, contracts, validation, migration safety, and verification.

## GitHub topics

`ai-agent`, `agent-skills`, `codex-skill`, `software-architecture`, `modular-architecture`, `robust-systems`, `system-design`, `refactoring`, `clean-architecture`, `ports-and-adapters`, `schema-validation`, `developer-tools`, `implementation-planning`

## SEO keywords

modular software architecture, robust systems design, AI coding agent skill, Codex skill, agent skills, software architecture automation, implementation planning, modular refactoring, ports and adapters, clean architecture, contract-first development, schema validation, resilient software design, safe migration planning, codebase architecture audit, AI developer tools.

## Author

Byron Jacobs  
GitHub: [@savedpixel](https://github.com/savedpixel)

## License

MIT
