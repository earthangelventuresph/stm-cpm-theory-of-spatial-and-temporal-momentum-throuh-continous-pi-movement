# E4 - Sunspot-Cycle Natural-Drift Test (§12.7)

**Tests:** P5 on natural quasi-periodic record with large cycle-length drift (about 9 to 14 years).

## Claim in plain language
The solar cycle drifts in length. If phase tracking helps on drifting lab oscillations, it should help here too - but this record alone cannot prove or overturn the lab result.

## Formal Prediction
Δ at h = 12 months; secondary Δ at h = 66 months.

## Falsification Threshold
Single-stage (record fixed): Supported on this record iff lower bound Δ > 0.05, else Not supported. E4 Not supported does NOT overturn E2 Supported; both reported.

## Design
Expanding-window evaluation: train 1749-1900, test 1901-end, refitting once per year. T0 = 132 months (11 years).

## Apparatus / Materials
Monthly total sunspot number, World Data Center SILSO, Royal Observatory of Belgium (about 3,300 months from 1749); common code. Record version number and download date.

## Step-by-step Procedure
1. T0 = 132 mo. 2. Expanding window: train 1749-1900, test 1901-end, refit yearly. 3. B0: x, backward differences for v and a, lags 1, 2, 3, 4, 5, 12, 24 months. 4. B1: B0 + fixed-period Fourier at 132 mo (k = 1..3). 5. M2: B0 + tracked phase features. 6. Horizons h = 12 mo (primary), 66 mo.

## Outcomes
Primary: Δ at h = 12 months. Secondary: Δ at h = 66 months.

## Sample Size + Power / Analysis
One fixed record (about 24 cycles). Limitation acknowledged: small number of cycles is why lower-bound rule applied without relaxation. Moving-block bootstrap, block length 132 months.

## Blinding
Window and refit schedule fixed in advance; version/date recorded.

## Frozen Analysis Plan
Common analysis §12.1; no post-hoc horizon changes.

## Confounds
Amplitude modulation unrelated to phase; revisions to sunspot series (version/date recorded); small number of cycles (about 24).

## Ethics / Safety
Public data only. No ethical approval needed. No safety requirements.

## Data Availability
No data exist yet. Future raw data, code, hashes to be archived read-only and shared on a public repository.

## Status
Protocol Only. No data. No result claimed.
