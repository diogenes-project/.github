# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in Diogenes, please report it
through
[GitHub's private vulnerability reporting](https://github.com/diogenes-project/.github/security/advisories/new).
This ensures your report is handled confidentially.

If private vulnerability reporting is unavailable, email
**w.phillip.moore@gmail.com** with the subject line
"Diogenes Security Report". Do not open a public issue for security
vulnerabilities.

## Scope

The following components are in scope for security reports:

- **Diogenes Claude Code plugin** — hooks, skills, and configuration
  that run within Claude Code sessions
- **Standalone prompt system** — the research methodology prompt
  definitions and framework logic
- **MCP server** — the Model Context Protocol server implementation
- **dio CLI** — the command-line interface
- **Research methodology framework definitions** — the structured
  process definitions that guide AI agent behavior

## Out of Scope

- Vulnerabilities in upstream dependencies (report these to the
  upstream maintainer)
- Vulnerabilities in the Claude API or Anthropic SDK
- Vulnerabilities in GitHub, Docker, or other third-party platforms
- Social engineering attacks against project contributors

## Response Commitment

- **Acknowledgment**: within 7 days of receiving a report
- **Assessment**: initial severity assessment within 14 days
- **Resolution**: target fix or mitigation plan within 30 days of
  acknowledgment, depending on severity and complexity

These timelines reflect the project's current scale as a small
community project. Response times may vary, but every report will be
acknowledged and investigated.

## Disclosure Policy

We follow coordinated disclosure. Once a fix is available, we will:

1. Release the fix
2. Publish a security advisory on GitHub
3. Credit the reporter (unless they request anonymity)

We ask that reporters allow reasonable time for a fix before public
disclosure.
