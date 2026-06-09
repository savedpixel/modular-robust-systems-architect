# Modular Architecture Principles

## Modularity is ownership, not folder count

A system is modular when each module has a clear reason to exist, owns a coherent set of responsibilities, exposes stable contracts, hides private internals, and depends in a deliberate direction.

## Define the module boundary

For each target, define:

- what the module owns
- what it does not own
- how other modules call it
- what contracts it exposes
- what internals are private
- where concrete dependencies are wired
- which tests prove the boundary

## Keep dependency direction deliberate

Prefer dependencies that point toward stable policy and domain concepts. Avoid domain code that reaches directly into framework glue, UI state, provider SDKs, database clients, global singletons, generated files, or unrelated modules.

## Use adapters at unstable edges

External providers, legacy formats, file systems, queues, databases, CLIs, UI frameworks, and generated artifacts often change for reasons outside the domain. Put adapter seams around them when they threaten modularity or testability.

## Name the source of truth

Each important concept should have an authoritative place. Repeated definitions are acceptable only when one is generated from another or when compatibility requires a transitional duplicate with a removal plan.

## Keep public contracts stable

A public contract can be an API payload, event, schema, config shape, package export, command, file format, or database constraint. Treat public contracts as architecture, not incidental implementation detail.

## Avoid abstraction theatre

Do not add interfaces, factories, registries, plugins, or service layers just to make code look architectural. Add a seam when it isolates change, protects a contract, improves testability, enables migration, or clarifies ownership.
