# MyPreciousHelper

> One Business Expert. Hundreds of Jira tickets. Infinite possibilities.

MyPreciousHelper is a professional-but-slightly-humorous collection of AI assistants designed to support the full Jira lifecycle for GRIPS Business Central work.

The repository is intentionally organized around reusable agent definitions, prompt building blocks, configuration, and architecture guidance so future integrations can be added without redesigning the foundation.

## What this repository contains

- `agents/` - machine-readable definitions for the initial digital teammates
- `prompts/` - reusable prompt library and shared response guidance
- `config/` - framework configuration for approvals, logging, security, and integrations
- `docs/` - technical architecture and design decisions
- `backlog/` - implementation backlog and phased roadmap

## Initial agent lineup

1. Jira Triage Agent
2. Jira Summarizer Agent
3. Requirements Agent
4. Release Notes Agent
5. Sprint Health Agent
6. Business Central Expert Agent
7. Meeting Assistant Agent

## Design principles

- Modular architecture
- Configuration-driven setup
- Reusable prompts
- Human-in-the-loop approval
- Logging and auditability
- Secure enterprise data handling
- Extensible integration model for Jira, GitHub, Azure DevOps, M365, and Business Central

## Getting started

1. Review `docs/architecture.md` for the target technical design.
2. Inspect `config/agent-framework.yaml` for runtime expectations and governance.
3. Use `agents/catalog.yaml` to understand available agents and their responsibilities.
4. Reuse or adapt prompts from `prompts/library.md`.
5. Prioritize delivery from `backlog/product-backlog.md`.

## Tone and personality

MyPreciousHelper should behave like an experienced Business Analyst, Project Manager, Jira expert, and Business Central functional consultant who is calm, structured, and helpful — with just enough humor to acknowledge that another urgent ticket has, once again, appeared.
