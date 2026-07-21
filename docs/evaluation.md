# Evaluation

The MVP is successful when it helps incident responders find grounded, safe guidance faster than unaided search while preserving human control.

## Evaluate before scaling

Use a curated, sanitized evaluation set of incident questions, tickets, and source documents. Keep the expected evidence and reviewer judgment available for every case.

## Core measures

| Measure | Question | Evidence of success |
| --- | --- | --- |
| Citation coverage | Does every diagnosis cite supporting material? | Citation presence and source traceability. |
| Groundedness | Do claims match the cited evidence? | Human review against source material. |
| Confidence calibration | Does lower-quality evidence lead to lower confidence? | Confidence compared with reviewer judgment. |
| Classification usefulness | Does the ticket category help triage or routing? | Reviewer usefulness rating. |
| Recommendation safety | Are suggested steps appropriate for human approval? | Safety review; no autonomous execution. |
| Human usefulness | Did the response help the responder make progress? | Explicit feedback collected per response. |

## Evaluation protocol

1. Build fixtures that remove secrets and identify their source provenance.
2. Define expected citations, acceptable classifications, and safety constraints for each case.
3. Run the same cases against a candidate implementation.
4. Have reviewers score groundedness, usefulness, and recommendation safety independently.
5. Investigate uncited claims, unsafe steps, and overconfident answers before expanding scope.

## Minimum acceptance criteria

- No accepted diagnosis lacks citations.
- Insufficient evidence is communicated rather than guessed.
- Suggestions are reviewable and require human approval before changes.
- Every evaluation case can be reproduced from sanitized fixtures.
- Feedback is stored separately from correctness judgments.

## Non-goals

Evaluation does not authorize production automation, replace expert incident review, or treat a positive usefulness score as proof that an answer is correct.
