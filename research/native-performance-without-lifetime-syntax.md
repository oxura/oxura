# Native performance without explicit lifetime syntax

## Research question

How much deterministic memory safety and native performance can a language provide while keeping ordinary source free of explicit lifetime annotations?

## Working model

Use immutable values by default, explicit owned and borrowed parameters, type-directed move/drop plans, non-escaping views, checked resource closure, and compile-time rejection when safe ownership cannot be inferred. Keep raw pointers and foreign ownership inside explicit unsafe FFI boundaries.

## Evaluation

- ASan, UBSan, and LeakSanitizer results;
- use-after-move and escaping-view rejection;
- allocations, copies, and peak RSS;
- generated-code performance against readable C baselines;
- amount of lifetime and manual-memory syntax in application code;
- clarity of diagnostics when inference is unsafe.

## Open problems

Inference must stay predictable. A language that hides lifetime syntax but produces surprising moves, clones, or rejections has only moved complexity into the compiler. Diagnostics and observable storage policy are part of the design.
