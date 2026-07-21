# Incident Resolution Copilot

An evidence-backed copilot for helping engineers diagnose and resolve technical incidents. The MVP turns approved incident material into grounded answers, then keeps the human operator in control of every operational decision.

## MVP outcome

An engineer can provide an incident ticket or question and receive:

- a classification of the ticket or request;
- a diagnosis grounded in retrieved incident evidence;
- citations and an explicit confidence signal;
- safe, suggested next steps for human review; and
- a way to say whether the response was useful.

## Scope

| Capability | MVP intent |
| --- | --- |
| Ingestion | Bring approved incident documents and records into a searchable knowledge base. |
| Retrieval | Retrieve relevant evidence for a question or ticket. |
| Grounded answers | Present RAG-based diagnosis with citations and confidence. |
| Suggested steps | Offer reversible, safe actions for a human to approve. |
| Classification | Categorize incoming tickets to support routing and triage. |
| Feedback | Capture human usefulness feedback to improve evaluation and future iterations. |

## Safety boundaries

- No autonomous production actions.
- No uncited diagnosis.
- Human approval is required before any change.

The copilot may explain evidence and propose a plan. It must not execute changes, claim certainty beyond available evidence, or replace incident ownership.

## Repository layout

| Path | Purpose |
| --- | --- |
| `app/` | Future product implementation. |
| `tests/` | Future automated tests. |
| `data/documents/` | Approved source material for ingestion. Do not add secrets or production exports. |
| `fixtures/` | Sanitized, reproducible samples for development and evaluation. |
| `docs/architecture.md` | Technology-neutral architecture and safety model. |
| `docs/evaluation.md` | MVP success measures and evaluation protocol. |

## Start here

1. Read [the architecture](docs/architecture.md) for the intended boundaries and flow.
2. Read [the evaluation plan](docs/evaluation.md) before selecting implementation details.
3. Read [the contribution guide](CONTRIBUTING.md) before proposing changes.

## Status

This is a repository scaffold. It intentionally contains no application implementation, framework choice, deployment configuration, or production integration.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Contributions should preserve evidence traceability, safety boundaries, and technology neutrality until an implementation decision is made.
