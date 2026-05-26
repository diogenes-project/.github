# Contributing to Diogenes

Thank you for your interest in contributing. This document covers
everything you need to get started.

## How the project works

Diogenes is a deterministic AI research coordinator that combines nine
intelligence and scientific frameworks into an evidence-based research
process. It lives in a single repository and ships in three forms:

- **Claude Code plugin** — installs as a skill for Claude Code sessions
- **Standalone prompt** — works with any capable LLM (Claude, ChatGPT,
  Gemini, etc.)
- **dio CLI** — command-line interface for scripted research workflows

The codebase also includes an MCP server for Model Context Protocol
integration.

## Development setup

### Prerequisites

- **Docker** — the only host-side dependency for running validation.
  All linting, type checking, and testing runs inside dev containers.
- **[uv](https://docs.astral.sh/uv/)** — Python package manager, used
  to install VERGIL's host-side CLI tools.
- **Python 3.14** — the project targets Python 3.14.

### Install the tooling

```bash
uv tool install --python 3.14 \
  'vergil-tooling @ git+https://github.com/vergil-project/vergil-tooling@v2.0'
```

This installs the `vrg-*` CLI tools (`vrg-commit`, `vrg-submit-pr`,
`vrg-validate`, `vrg-docker-run`, and others) on your host.

### Claude Code hook guard

The `.claude/hooks/guard.sh` PreToolUse hook blocks raw `git` and
`gh` commands in AI agent sessions — all operations must go through
the `vrg-git` / `vrg-gh` wrappers.

## Workflow

The repository uses `develop` as the integration branch.

1. **Branch from `develop`.**
   Use the naming convention `feature/<issue>-<slug>` or
   `chore/<issue>-<slug>`, where `<issue>` is the GitHub issue number.

2. **Commit with `vrg-commit`.**
   This enforces conventional commit format, branch policy, and
   co-author attribution. Raw `git commit` is blocked by the
   pre-commit hook.

3. **Validate locally.**
   ```bash
   vrg-docker-run -- uv run vrg-validate
   ```
   This runs the full validation pipeline (lint, typecheck, test,
   common checks) inside a dev container. The same checks run in CI.

4. **Submit a PR with `vrg-submit-pr`.**
   This creates a standards-compliant pull request linked to the
   issue.

5. **Wait for review.**
   All PRs require human approval and passing CI before merge.

## For contributors using AI tools

Diogenes welcomes AI-assisted contributions under a clear
accountability model.

### Identity

Each contributor who uses AI tools creates a dedicated
`<username>-agent` GitHub account for AI-assisted development. This
is a real GitHub account — not a bot, not a shared service account.
One agent identity per human, regardless of which AI tool or model
you use.

- **Agent identity** (`<username>-agent`): used for all AI-assisted
  commits and PRs
- **Human identity** (`<username>`): used for reviews, approvals,
  and merges

### Accountability

You are accountable for everything your agent produces. "The AI did
it" is not a defense. When you submit a PR from your agent account,
you are asserting that you reviewed the work, understand it, and take
responsibility for it.

### In practice

- All AI-assisted work is committed under the agent identity with
  a `Co-Authored-By` trailer
- All reviews and approvals are performed under your human identity
- At 2+ human contributors, cross-human review is required — you
  cannot approve your own agent's PRs
- The specific AI tool and model used are recorded in commit metadata
  for auditing, but the security boundary is human vs. not-human

## For contributors not using AI

Standard open-source contribution model:

1. Fork the repository
2. Create a feature branch
3. Make your changes and validate locally
4. Open a pull request

The same quality bar applies to all contributions regardless of how
they were produced. PRs require human approval from an org member and
passing CI.

## What to expect from review

- **Human approval required.** Every PR is reviewed and approved by a
  human before merge.
- **CI must pass.** The full validation pipeline runs on every PR.
  If CI fails, the PR cannot merge.
- **At 2+ contributors**, cross-human review is enforced: the
  reviewer must be a different human than the one who directed the
  work.
- **Feedback is constructive.** We review code, not people.

## Template override convention

This organization uses a shared `.github` repository for default issue
and PR templates. GitHub's inheritance for template directories is
all-or-nothing: if a repo has any file in its own
`.github/ISSUE_TEMPLATE/` directory, it gets none of the org defaults
for that directory. To customize templates for a specific repo, provide
the complete set in that repo's directory. Standalone files
(CONTRIBUTING.md, SECURITY.md, etc.) inherit independently on a
per-file basis.

## License

Diogenes is licensed under
[GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html). By
contributing, you agree that your contributions will be licensed under
the same terms.
