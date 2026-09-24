# Technical Architecture

## Goals

- Support reusable AI assistants for Jira-centric delivery management
- Separate prompts, agent metadata, runtime configuration, and integrations
- Keep human approval in the loop for sensitive or externally visible actions
- Make future integrations additive instead of disruptive

## Proposed architecture layers

### 1. Experience layer
- Chat, scheduled summary, and workflow-triggered entry points
- Output formats for summaries, checklists, agendas, release notes, and action logs

### 2. Agent orchestration layer
- Selects an agent from the catalog
- Applies shared personality and response rules from the prompt library
- Injects configuration such as approval requirements, logging policy, and enabled integrations
- Routes complex work to specialist agents when required

### 3. Skill and integration layer
- Jira Cloud / Jira Data Center
- GitHub
- Azure DevOps
- Microsoft Teams / Outlook / SharePoint / Confluence
- Business Central APIs
- Azure OpenAI or compatible model providers

### 4. Governance layer
- Audit logging for prompts, inputs, outputs, approvals, and external actions
- Enterprise security boundaries for secrets, connectors, and personally identifiable information
- Human approval before sending email, publishing release notes, or changing external systems

## Core domain objects

- **Agent definition**: name, purpose, inputs, outputs, prompt reference, approval mode
- **Prompt template**: reusable instructions plus agent-specific task framing
- **Execution context**: ticket data, comments, sprint metadata, stakeholders, delivery history
- **Action proposal**: changes or communications that require review before execution
- **Audit event**: who asked, what data was used, what was generated, and what was approved

## Recommended execution flow

1. Receive business request or scheduled trigger
2. Resolve the best-fit agent from the catalog
3. Build the final prompt from shared guidance plus agent template
4. Gather structured source data from approved integrations
5. Generate output with confidence notes, risks, and missing-information checks
6. Require approval for external actions or stakeholder-facing communication
7. Persist audit information and reusable delivery artifacts

## Extensibility notes

- Add new agents by extending `agents/catalog.yaml`
- Add new prompt variants in `prompts/library.md`
- Add integrations and policy switches in `config/agent-framework.yaml`
- Preserve stable output contracts so downstream automations remain compatible
