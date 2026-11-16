# AI Development Harness — Portfolio Case Study (Draft)

> **Status: architecture proposal, not a verified end-to-end system.** This document describes how existing public resources could be composed into a repeatable delivery method. It does not claim that the components are already integrated, tested together, or used in production.

## The idea

**From a business problem to a testable solution, with AI-assisted engineering and human accountability.**

Rather than treating every AI-assisted project as an isolated prompt session, the goal is a repeatable workflow with explicit specifications, reusable instructions, execution boundaries, tests, and evidence.

```text
Problem & success metric
        |
Discovery -> PRD -> architecture & risk review
        |
Agent instructions + reusable skills + scoped tools
        |
Implementation -> automated checks -> human review
        |
Demo / evaluation -> documented learnings -> iteration
```

## Public resources and their roles

| Resource | Potential role | What is actually established |
| --- | --- | --- |
| [VibeCoding](https://github.com/igorveloso/vibecoding) | Methods: PRDs, AI collaboration, quality assurance, architecture and operations | Public guidance repository; not proof of an automated orchestration system |
| [Agent Scripts](https://github.com/igorveloso/agent-scripts) | Execution layer: agent instructions, skills, helper scripts and validation hooks | Public tooling repository. Its README describes **Peter's local workspaces**; authorship, permission, and applicability must be checked before reuse or attribution |
| [ADK Samples](https://github.com/igorveloso/adk-agentsamples) | Agent design reference and experimentation | A repository based on Google's ADK sample collection. Upstream samples are not original work |
| [GTM lead qualification prototype PR](https://github.com/igorveloso/adk-agentsamples/pull/1) | Candidate example for evaluating rules, lead scoring and validation | A draft deterministic Python prototype using synthetic data; **not** a deployed ADK agent or CRM integration |

## Proposed delivery lifecycle

1. **Frame** — Define the user, problem, constraints, baseline and success metric.
2. **Specify** — Create a short PRD, acceptance criteria and a documented architecture decision.
3. **Prepare** — Select agent instructions, skills, permitted tools, test fixtures and human approval gates.
4. **Build** — Implement small, reviewable changes with traceable requirements.
5. **Verify** — Run deterministic tests, evaluate AI outputs where relevant, check privacy and security, and capture failures.
6. **Present** — Publish a reproducible demo, limitations, trade-offs and next steps.

## Candidate case studies

### GTM Lead Qualification
- **Problem:** qualify and route leads without duplicating records or wasting enrichment spend.
- **Evidence to build:** runnable synthetic-data demo, scoring rationale, tests, evaluation report, architecture diagram and explicit human approval points.
- **Current limitation:** deterministic prototype; no live Salesforce, Clay, Salesloft or ADK integration.

### PianoHero
- **Problem:** design an accessible, motivating piano-learning experience.
- **Evidence to build:** connect product requirements, pedagogical rules, MIDI architecture and a narrow testable MVP.
- **Current limitation:** the public README primarily documents product design and planned implementation.

### IbaArquitetura
- **Problem:** reduce repetitive document and checklist work in an architecture practice.
- **Evidence to build:** source-data validation, mapping rules, error handling, synthetic examples and human review of extracted documents.
- **Current limitation:** public documentation and validation script; not a complete deployed application.

## What a recruiter should be able to inspect

- **Decision trail:** Why this approach rather than an alternative?
- **Reproducibility:** Can the example run without private data or credentials?
- **Quality:** Which tests and evaluations pass, and what remains untested?
- **Human oversight:** What can an agent do autonomously, and what requires approval?
- **Ownership:** Which files are original, adapted, or third-party?
- **Outcomes:** What is measured, and what is only an aspiration?

## Validation checklist before calling this a working harness

- [ ] Confirm ownership and license/attribution of Agent Scripts and all borrowed resources
- [ ] Define a versioned, original harness configuration and a documented interface between components
- [ ] Demonstrate the same workflow on at least two independent projects
- [ ] Add automated checks and reproducible local setup
- [ ] Record a real evaluation run, including failures and limitations
- [ ] Add a diagram and short walkthrough using only synthetic or approved data

**Portfolio positioning:** *I build AI-assisted systems with a repeatable, evidence-driven development process. This page documents the process I'm formalizing and the projects used to validate it.*
