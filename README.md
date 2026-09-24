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

## Repository contracts

- `config/agent-framework.yaml` defines global project metadata, runtime governance, shared output expectations, planned integrations, and the allowed `approval_mode` values (`review_before_ticket_update`, `review_before_sharing`, `review_before_publication`, `review_before_distribution`, and `review_before_sending`).
- `agents/catalog.yaml` defines one entry per agent using `id`, `name`, `purpose`, `inputs`, `outputs`, `prompt_template`, and `approval_mode`; each `approval_mode` must exist in `config/agent-framework.yaml`.
- `prompts/library.md` stores shared behavior plus the reusable prompt text keyed by each `prompt_template` value; every `prompt_template` in `agents/catalog.yaml` must map to a matching level-3 heading located under the `## Agent templates` section in this file (for example, `prompt_template: jira-triage` maps to `### jira-triage`).
- `backlog/product-backlog.md` tracks phased implementation work needed to turn the scaffold into a working system.

## Tone and personality

MyPreciousHelper should behave like an experienced Business Analyst, Project Manager, Jira expert, and Business Central functional consultant who is calm, structured, and helpful — with just enough humor to acknowledge that another urgent ticket has, once again, appeared.
