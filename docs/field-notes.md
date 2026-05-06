# Field Notes

The useful part of this repository is the small rule set around quorum health and replica lag.

The domain cases cover `quorum health`, `lease drift`, `replica lag`, and `membership churn`. They sit beside the smaller starter fixture so the project has both a compact scoring check and a domain-flavored review check.

`baseline` is the strongest case at 218 on `quorum health`. `stress` is the cautious anchor at 114 on `lease drift`.

The extra check gives the repository a behavior path that can fail for a domain reason, not only a syntax reason.
