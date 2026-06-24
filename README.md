# Hermes Agent — Architecture Exploration

A living, self-contained explainer of the [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) codebase — the self-improving personal AI agent.

**→ [`hermes-exploration.html`](hermes-exploration.html)** — open it in any browser. It's fully self-contained (no external CSS/JS), adapts to light/dark mode, and embeds every diagram inline.

## What's inside

- **What Hermes is** and its two governing principles (prompt caching is sacred; the narrow-waist core)
- **Prompt caching** — system prompt, build-vs-restore, why caching is a prefix property, provider-vs-client division of labor
- **Architecture overview** — surfaces, core, and edges
- **The agent loop** — one turn from pre-turn setup through the tool loop to finalize
- **Tools & toolsets** — the registry, gating, and dispatch pipeline
- **The learning loop** — skills, the curator state machine, memory/Honcho, cross-session recall, and the background review fork
- **Cron** — the job model, scheduler tick, execution, and delivery
- **Session storage** — the SessionDB schema, write path, and the stored-vs-sent distinction
- **A request trace** tying sessions and the learning loop together

Diagrams are SVG, hand-built to illustrate the actual code paths (with `file:line` references throughout).

## Provenance

Generated during an interactive code-exploration session with Claude Code. Line numbers reference `hermes-agent` around version `0.17.0` and may drift as that codebase evolves. This repo documents an external open-source project; it ships no Hermes source.
