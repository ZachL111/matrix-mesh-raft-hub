# Review Journal

I treated `matrix-mesh-raft-hub` as a project where the smallest useful behavior should still be inspectable.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its distributed systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `quorum health`, score 218, lane `ship`
- `stress`: `lease drift`, score 114, lane `watch`
- `edge`: `replica lag`, score 133, lane `watch`
- `recovery`: `membership churn`, score 178, lane `ship`
- `stale`: `quorum health`, score 204, lane `ship`

## Note

A future change should add new cases before it changes the scoring rule.
