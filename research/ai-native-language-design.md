# AI-native programming language design

## Research question

What changes when a language is designed for a human, a compiler, and a coding agent to understand together?

## Working model

Separate pure functions, effectful tasks, long-running flows, and state machines. Make effects and capabilities part of public interfaces. Preserve typed semantic identities through formatting and compilation. Treat specifications, incomplete typed work, impact analysis, and semantic refactors as first-class tooling contracts rather than editor conventions.

## Evaluation

- semantic equivalence across concise and canonical forms;
- ambiguity rejected before code generation;
- context required for safe automated changes;
- capability bypass resistance;
- reproducible native artifacts;
- simplicity of real CLI, backend, automation, and data programs.

## Open problems

AI-friendly cannot mean benchmark-specific syntax or a large hidden runtime. The language must remain coherent for humans, and every convenience must lower to one inspectable semantic pipeline.
