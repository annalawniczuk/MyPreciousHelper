# Product Backlog

## Phase 1 - Foundation

- [ ] Confirm target runtime and hosting model for agent orchestration
- [ ] Implement catalog loader for `agents/catalog.yaml`
- [ ] Implement prompt composer using shared and agent-specific templates
- [ ] Add audit logging model for requests, approvals, and outputs
- [ ] Define approval workflow for outbound communication and ticket updates

## Phase 2 - Core integrations

- [ ] Connect Jira Cloud data retrieval and issue update flows
- [ ] Add Jira Data Center compatibility strategy
- [ ] Add GitHub and Azure DevOps context ingestion for delivery status
- [ ] Add Outlook / Teams support for summaries, reminders, and follow-ups
- [ ] Define Business Central API adapters for functional context

## Phase 3 - Initial production agents

- [ ] Deliver Jira Triage Agent
- [ ] Deliver Jira Summarizer Agent
- [ ] Deliver Requirements Agent
- [ ] Deliver Release Notes Agent
- [ ] Deliver Sprint Health Agent
- [ ] Deliver Business Central Expert Agent
- [ ] Deliver Meeting Assistant Agent

## Phase 4 - Automation and reporting

- [ ] Add scheduled morning summary email capability with approval safeguards
- [ ] Add duplicate ticket detection heuristics and confidence scoring
- [ ] Add cross-ticket action tracking and overdue reminder flows
- [ ] Add release communication publishing workflow
