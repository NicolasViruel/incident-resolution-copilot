# Architecture

The MVP is an evidence-first assistant, not an autonomous incident responder. Technology choices are deliberately deferred.

## Intended flow

1. Ingest approved, sanitized incident knowledge with source metadata.
2. Normalize and index that material for retrieval.
3. Receive a ticket or incident question and classify it.
4. Retrieve relevant evidence and compose a diagnosis only from that evidence.
5. Return citations, confidence, uncertainty, and safe suggested next steps.
6. Collect human usefulness feedback for later evaluation.

## Boundary model

| Boundary | Responsibility | Must not do |
| --- | --- | --- |
| Ingestion | Preserve document identity, source, timestamp, and access constraints. | Treat unapproved or secret material as ordinary input. |
| Retrieval | Return relevant, traceable evidence. | Hide sources or manufacture evidence. |
| Reasoning | Relate evidence to the reported symptom and state uncertainty. | Produce an uncited diagnosis. |
| Recommendation | Suggest safe, reviewable steps and escalation paths. | Execute production actions. |
| Feedback | Capture whether people found a response useful. | Imply feedback alone proves correctness. |

## Answer contract

Each user-facing answer should distinguish:

- **Classification:** the ticket category and any routing signal.
- **Diagnosis:** the evidence-backed explanation, or an explicit insufficient-evidence result.
- **Evidence:** citations that identify the retrieved material.
- **Confidence:** a visible indication of support and uncertainty.
- **Suggested steps:** human-reviewed, safe actions and escalation guidance.

## Safety invariants

- The system performs no autonomous production action.
- A diagnosis without supporting citations is rejected or labeled as insufficient evidence.
- Every operational change requires explicit human approval outside the copilot.
- Missing, conflicting, or weak evidence lowers confidence and is surfaced to the user.

## Deferred decisions

This scaffold does not choose a programming language, framework, model provider, vector store, ticketing integration, identity model, hosting platform, or deployment strategy. Those decisions should follow an evaluation plan and documented safety requirements.
