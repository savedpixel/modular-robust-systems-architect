# Security Policy

This repository contains an AI agent skill. It does not run production services or collect data by itself, but its instructions can influence how coding agents work in user repositories.

## Reporting security concerns

Open a private security advisory or contact the maintainer if you find guidance that could cause an agent to:

- expose secrets or credentials
- weaken authentication or authorization
- bypass review or approval steps
- execute unsafe commands without user intent
- modify unrelated project areas
- ignore trust boundaries or external input validation
- apply insecure defaults to generated implementation plans

## Security expectations for the skill

The skill should encourage agents to:

- preserve permission boundaries
- validate untrusted input at system boundaries
- avoid logging secrets or sensitive payloads
- ask before modifying risky systems
- identify migrations and public contract changes
- prefer least privilege for integrations and tools
- verify behavior with tests and operational checks

Do not use this skill as a substitute for professional security review on high-risk systems.
