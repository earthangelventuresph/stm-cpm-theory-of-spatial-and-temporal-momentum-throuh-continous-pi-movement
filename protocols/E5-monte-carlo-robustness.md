# E5 - Monte Carlo Robustness Study (§12.8)

**Tests:** Robustness of P5 across sampling rate, noise, harmonic count, loop bandwidth.

## Claim in plain language
The benefit should not depend on one lucky setting. It should survive across a grid of realistic settings.

## Formal Prediction
Fraction of eligible cells with lower bound Δ > 0.05; secondary same fraction for all 256 cells; cell-wise map of Δ.

## Falsification Threshold
Robustness established iff at least 80% of eligible cells (116 of 144) meet criterion. If fewer, robustness Not established; claim restricted to cells that meet criterion; restriction stated in any publication.

## Design
Simulation grid: samples/T0 in 10, 20, 50, 100; SNR in 0, 10, 20, 30 dB; K in 1, 2, 3, 5; ωL/ω0 in 0.02, 0.05, 0.1, 0.2 - 256 cells. δ = 0.10, Nd = 10. 200 replicates/cell, seeds fixed in registration. Eligible cells: SNR ≥ 10 dB and ≥ 20 samples/T0 - 144 cells.

## Apparatus / Materials
Software generator x(t) = A cos θ(t) + noise, drift Eq. 37; common code; computer.

## Step-by-step Procedure
1. Build grid (256 cells). 2. δ = 0.10, Nd = 10. 3. 200 replicates/cell, seeds fixed in registration. 4. Compute Δ against B1 with matching K. 5. Report eligible-cell fraction + all-cell fraction + map.

## Sample Size + Power
200 replicates/cell; bootstrap over replicates per cell. E5 runs BEFORE E2 so planning values (Δdesign, σΔ) may be updated once, before data collection, locked in registration.

## Blinding
Seeds fixed in registration; generator not tuned to model; second generator with non-sinusoidal waveform added.

## Frozen Analysis Plan
Per-cell bootstrap; eligibility rule fixed; no post-hoc cell exclusions.

## Confounds
Generator bias (second generator, non-sinusoidal waveform); seed dependence (three seed sets).

## Ethics / Safety
Computational only. No requirements.

## Data Availability
No data exist yet. Future raw data, code, hashes to be archived read-only and shared on a public repository.

## Status
Protocol Only. No data. No result claimed.
