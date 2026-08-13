# Semantic representations for AI coding agents

## Research question

Can coding agents work more reliably with typed program structure than with file-sized text windows and textual patches?

## Working model

Expose stable symbol identities, definitions, references, callers, callees, types, effects, ownership transfers, module relationships, and exact source locations through a versioned semantic world. Refactors become operations over identities with stale-world checks, impact analysis, and rollback—not unconstrained text replacement.

## Evaluation

- successful changes per context token;
- missed call sites and unintended edits;
- refactor precision across module boundaries;
- stale-index detection;
- deterministic reconstruction from source;
- quality of minimal task-specific context capsules.

## Open problems

The representation must remain compact without hiding important source details. It must also preserve provenance: an agent should be able to move from a semantic fact back to the exact source and compiler evidence that established it.
