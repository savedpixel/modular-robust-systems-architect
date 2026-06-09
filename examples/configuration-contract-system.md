# Example: Configuration and Contract System

```text
Use the modular-robust-systems-architect skill.

Redesign our integration manifest flow. The goal is a compact human-maintained source format, strict validation, reference resolution, normalized generated output, compatibility tests, and runtime consumers that do not read raw config directly. Ask questions first, then inspect the loaders, schemas, generators, runtime consumers, and tests.
```

Expected agent focus:

- identify the authoritative source of truth
- separate human-owned config from generated runtime representation
- reject unknown keys and invalid references where strictness is required
- define schema and normalization phases
- preserve compatibility through generated diffs or parity tests
- keep complex behavior in code rather than hidden config logic
