# matrix-mesh-raft-hub

`matrix-mesh-raft-hub` is a compact SQL repository for distributed systems, centered on this goal: Implement an SQL distributed systems project for raft diagnostic reporting, using negative fixtures and human-readable error snapshots.

## Why This Exists

The point is to make a small domain rule concrete enough that a reader can change it and immediately see what broke.

## Matrix Mesh Raft Hub Review Notes

`baseline` and `stress` are the cases worth reading first. They show the optimistic and cautious ends of the fixture.

## Capabilities

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/matrix-mesh-raft-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `quorum health` and `lease drift`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Implementation Shape

The repository has two validation layers: the original compact policy fixture and the domain review fixture. They are separate so one can change without hiding failures in the other.

The SQL checks add a separate view over the domain review fixture.

## Local Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Verification

The check exercises the source code and the review fixture. `baseline` is the high score at 218; `stress` is the low score at 114.

## Roadmap

This remains a local project with deterministic fixtures. It does not depend on credentials, hosted services, or live data. Future work should add richer malformed inputs before widening the public API.
