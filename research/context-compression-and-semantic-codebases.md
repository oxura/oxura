# Agent context compression and semantic codebases

## Research question

Can an agent receive less repository text while retaining the facts needed to make a correct change?

## Working model

Build context from semantic dependencies rather than directory proximity. Start with the requested symbol and acceptance contract, then include only relevant interfaces, callers, effects, invariants, tests, and source spans. Expand context on demand, and record why every item was selected.

## Evaluation

- tokens consumed per successful change;
- omitted facts that cause a failure;
- irrelevant context included;
- retrieval latency and index freshness;
- consistency between semantic summaries and source;
- performance on multi-file changes and repository-scale refactors.

## Open problems

Compression creates an information boundary. The system must know when its capsule is insufficient and expose uncertainty instead of presenting a compact but misleading view of the codebase.
