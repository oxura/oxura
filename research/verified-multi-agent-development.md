# Verified multi-agent software development

## Research question

How can a software agent explore multiple implementations without turning parallelism into unreviewable change volume?

## Working model

Treat every candidate as a claim that must carry evidence. A controller defines an acceptance contract, isolates competing attempts, verifies observable behavior, and promotes only the exact change whose evidence satisfies the contract. Failed attempts remain useful as counterexamples rather than being merged into the working tree.

## Evaluation

- task success under fixed acceptance contracts;
- regressions introduced outside the requested scope;
- verification cost and wall-clock latency;
- useful diversity between candidates;
- reproducibility of the promoted artifact;
- human review effort per accepted change.

## Open problems

Verification can be incomplete, correlated agents can repeat the same mistake, and a passing test suite is not a proof of intent. The central problem is therefore not merely orchestration—it is constructing evidence that is strong enough for the risk of the change.
