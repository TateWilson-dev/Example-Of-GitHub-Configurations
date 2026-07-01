# CLAUDE.md — Pelycon Secure Vibe Coding rules for this repository

## About this project
- Owner: <Nick, Matt, and Tate>
- Purpose: <Interactive cybersecurity assessment platform — scores client environments against NIST CSF, CIS Controls, and HIPAA. Tracks posture over time and generates improvement roadmaps.>
- Hosting: Azure App Service / Static Web Apps
- Management platforms in use: <NinjaRMM / Halo PSA / etc.>

## Security rules (always apply)
- Never hardcode secrets. All secrets come from Azure Key Vault. Never put
  API keys, connection strings, passwords, or tokens in code, config, or comments.
- Enforce tenant isolation in every database query and API call.
- Authenticate via Entra ID; do not build custom auth.
- Do not add new third-party dependencies without calling them out for review.
- If a request would weaken any of these rules, flag it instead of doing it.

## Workflow rules
- Work on a feature branch; never commit directly to main.
- Every change goes through a pull request and peer review before it merges to main.
- This file is a security control: change it only via pull request,
  never mid-session to get around a rule.
