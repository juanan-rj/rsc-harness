# RSC Harness (modified fork)

> **Credit where it is due.** This repository is a **modified version** of
> [`ericrisco/rsc-harness`](https://github.com/ericrisco/rsc-harness) by **Eric Risco**
> (npm: [`@ericrisco/rsc`](https://www.npmjs.com/package/@ericrisco/rsc)), released under the **MIT license**.
> The original author's copyright notice is kept in [LICENSE](LICENSE). For the official, maintained
> version, use the upstream project.

Guardrail hooks for AI coding agents (Claude Code and others). They run before and after the agent acts
and keep it inside safe boundaries.

## What the hooks do

| Area | Hooks |
|---|---|
| **Git safety** | `branch-guard`, `trunk-policy`, `ship-guard`, `worktree-reaper` |
| **Command safety** | `danger-guard`, `shell-unwrap`, `risk-policy` |
| **Review and quality gates** | `asdd-gate`, `sello`, `spec-completeness` |
| **Session memory** | `session-memory`, `session-memory-core`, `session-memory-adapter`, `session-start`, `worklog-checkpoint` |
| **Style policy** | `gitmoji-guard`, `emoji-policy`, `copy-guard`, `copy-rules` |
| **Updates and sync** | `auto-update`, `knowledge-sync`, `hook-once` |

All hooks are standalone Node.js scripts (built-ins only) in [`hooks/`](hooks).

## Usage

Hooks are meant to be wired into your assistant's hook configuration (for example `.claude/settings.json`
for Claude Code) and copied to `.rsc/` in your project. For the full installer and catalog, see upstream:

```bash
npx @ericrisco/rsc
```

## Modifications

This fork carries my local adjustments to the upstream hooks for my own workflow.
Compare with upstream to see exactly what differs.

## License

MIT. See [LICENSE](LICENSE). Original work © Eric Risco and contributors; modifications © Juanan.
