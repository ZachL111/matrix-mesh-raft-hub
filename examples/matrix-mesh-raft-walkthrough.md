# Matrix Mesh Raft Hub Walkthrough

I use this file as a small checklist before changing the SQL implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 218 | ship |
| stress | lease drift | 114 | watch |
| edge | replica lag | 133 | watch |
| recovery | membership churn | 178 | ship |
| stale | quorum health | 204 | ship |

Start with `baseline` and `stress`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

If `stress` becomes less cautious without a clear reason, I would inspect the drag input first.
