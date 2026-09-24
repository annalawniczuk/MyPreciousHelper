# MyPreciousHelper

> One Business Expert. Hundreds of Jira tickets. Infinite possibilities.
>
> "One Jira ticket does not simply walk into Production."

MyPreciousHelper is the digital sidekick every GRIPS Business Central expert secretly dreams about having.

Born from countless Jira tickets, endless status updates, mysterious "Can you just quickly check this?" requests, and legendary bug investigations, this repository is home to AI-powered assistants and agents designed to make GRIPS development management less painful and significantly more enjoyable.

MyPreciousHelper is intentionally organized around reusable agent definitions, prompt building blocks, configuration, and architecture guidance so future integrations can be added without redesigning the foundation.

## Overview

Whether the mission is:

- hunting down forgotten requirements
- translating business language into developer language (and back again)
- summarizing complex Jira discussions
- detecting duplicate tickets before they multiply like gremlins
- preparing meeting agendas
- tracking action items
- writing acceptance criteria
- reviewing development progress
- creating release notes that humans can actually understand
- sending reminder emails when a ticket question is still waiting for an answer

...MyPreciousHelper stands ready.

## Why?

As a Business Process Principal and GRIPS Business Expert, I spend my days navigating the wonderful ecosystem of:

- Jira tickets
- Business Central enhancements
- bug fixes
- development projects
- testing cycles
- business requirements
- stakeholder requests that somehow become "urgent"

Unfortunately, coffee alone is not a scalable solution.

Therefore, AI agents shall assist in bringing order to the chaos.

## Vision

Imagine a team of tireless digital colleagues who:

- never forget a ticket
- never lose a meeting note
- never ask for vacation
- never schedule meetings at 15:59 on a Friday
- can summarize a 200-comment Jira ticket without emotional damage
- help separate actual critical issues from "it would be nice if..." requests
- translate business expectations into developer-friendly tasks
- occasionally make you look suspiciously organized

These agents should help me:

- save time
- improve ticket quality
- detect inconsistencies
- organize work
- reduce manual reporting
- improve communication with stakeholders
- generate insights from Jira data
- send a morning summary email with the right approvals in place

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
- Agent-based design
- Extensible skill framework
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

## Future integrations

Design the architecture so future integration is possible with:

- Jira Cloud
- Jira Data Center
- GitHub
- Azure DevOps
- Microsoft Teams
- Outlook
- SharePoint
- Confluence
- M365 Copilot
- Business Central APIs
- Azure OpenAI

## Tone and personality

MyPreciousHelper should behave like an experienced Business Analyst, Project Manager, Jira expert, and Business Central functional consultant who is calm, structured, and helpful — with just enough humor to acknowledge that another urgent ticket has, once again, appeared.
