# Muti-AgentClaw

Practical documentation for building a leader-and-coworker multi-agent system on OpenClaw.

This repo exists because end-to-end, fully workable OpenClaw multi-agent examples are still hard to find in public. The material here documents a reproducible pattern with clear leadership, isolated specialist agents, masked configuration, and production-shaped examples.

## What This Covers

- one leader agent: `main`
- specialist coworker agents: `coder` and `fins`
- isolated workspaces, identities, and session stores
- explicit delegation boundaries
- optional direct channel routing
- sanitized architecture diagrams and real-shaped outputs

## Versioned Documents

- [`OpenClaw_Multi_Agent_Leader_Coworker_Guide_v1.0.md`](./OpenClaw_Multi_Agent_Leader_Coworker_Guide_v1.0.md): original guide
- [`OpenClaw_Multi_Agent_Leader_Coworker_Guide_v1.1.md`](./OpenClaw_Multi_Agent_Leader_Coworker_Guide_v1.1.md): updated guide with shared-ideas workflow

## Short Changelog

### v1.1

- adds a shared ideas layer for coworker-to-coworker awareness without changing authority
- clarifies that `main` remains the only delegator and task assigner
- separates information sharing from delegation as an explicit architecture rule
- introduces a privacy boundary: shared knowledge must not reuse `MEMORY.md`
- adds `shared/ideas.jsonl` to the filesystem model and shared-ideas terminology to the guide
- expands prompt examples with shared knowledge curation for `main` and shared idea protocols for `coder` and `fins`
- adds a runtime sequence diagram for coworker idea publication
- extends validation tests and common-mistake guidance for misuse of the shared layer

### v1.0

- establishes the base leader-and-coworker pattern on OpenClaw
- defines the `main`, `coder`, and `fins` role split
- documents isolated workspaces, agent directories, routing, and delegation boundaries

## Core Principle

Shared knowledge is not shared authority.

The intended model is:

- `main` owns strategy, judgment, and task assignment
- coworkers execute narrow specialist work
- coworkers may publish reusable observations
- coworkers do not delegate sideways

## Notes

- Tokens, IDs, and machine-specific values are masked with placeholders such as `<STATE_DIR>`, `<MODEL_API_KEY>`, and `<DISCORD_BOT_TOKEN_FINS>`.
- The OpenClaw version context used in the guides is `2026.3.8`.
