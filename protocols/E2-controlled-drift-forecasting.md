# E2 - Controlled Frequency-Drift Forecasting (§12.5)

**Tests:** P5 and P6. **Hypotheses:** Δ > 0.05 at δ = 0.10; Δ < 0.02 at δ = 0; Δ rises with δ; onset near δ* = 0.039 (Nd=10).

## Claim in plain language
When frequency drifts, the causal phase tracker beats a fixed-period model. When it does not drift, it does not beat it.

## Formal Prediction
Primary Δ (M2 vs B1) at δ = 0.10, h = 0.5T0. P6a: Δ(δ=0) upper bound < 0.02. P6b: Spearman ρs ≥ 0.90 across five drift levels. P6c: Δ(δ=0.02) < 0.05 and Δ(δ=0.05) > Δ(δ=0.02).

## Falsification Threshold
Two-stage (§12.3): Stage 1 (20 runs/δ): if lower bound Δ > 0.05 then Supported, end. If upper bound Δ < 0.02 then Not supported, end. Else Stage 2 (40 runs/δ incl. Stage 1): Supported iff lower bound Δ > 0.05, else Not supported. No further stage. P5 Not supported if rule returns Not supported. P6 Not supported if P6a, P6b, or P6c fails. Complexity control: if M2 beats B1 by < 0.02 while beating B0 by > 0.05 then benefit attributed to periodic terms in B1; P5 Not supported.

## Design
Controlled experiment. δ in 0, 0.02, 0.05, 0.10, 0.20. Stage 1: 20 runs/δ = 100 runs. Stage 2 (if needed): 40 runs/δ. Each run 600 s (1,200 cycles). Fit first 300 s, evaluate last 300 s. Horizons h = 0.25T0, 0.5T0, T0; primary 0.5T0.

## Apparatus / Materials
E1 sensing chain on electrodynamic shaker platform with spring-mass oscillator; function generator capable of frequency modulation; power amplifier; E1 data system; processing computer with frozen code; environment logger.

## Step-by-step Procedure
1. Set T0 = 0.5 s (2 Hz), Td = 10T0 (Nd = 10), sampling 200 Hz (100 samples/T0). 2. Command Eq. 37 + band-limited Gaussian noise at 20 dB SNR for each δ. 3. Run 600 s per run. 4. Stage 1: 20 runs/δ; run order, drift phase, noise seed randomized by schedule fixed in advance. 5. Fit first 300 s, test last 300 s. 6. Fit B0, B1, M2; compute Δ for all horizons. 7. Apply §12.3. 8. Controls: shaker off (noise floor) and δ = 0 (fixed-period) in every block of ten runs.

## Outcomes
Primary: Δ vs B1 at δ = 0.10 and h = 0.5T0. Secondary: Δ vs B0; Δ at other δ and h; ρs; onset location.

## Sample Size + Power
Unit = run. Planning Δdesign = 0.15, Δmin = 0.05, σΔ = 0.12 gives nruns = [3.2415 × 0.12 / 0.10]² = 15.1, rounded up to 16. Stage 1 uses 20/δ (25% above requirement); Stage 2 uses 40/δ. Planning values are assumptions, not results; revisable only before data collection using E5. Analysis: §12.1 + §12.3, cluster bootstrap over runs.

## Blinding
Randomization schedule fixed in advance; test data sealed until code frozen; no peeking to choose thresholds.

## Frozen Analysis Plan
Common analysis §12.1: B0/B1/M2 as in README; ridge λ by blocked CV in training only; 10,000-resample cluster bootstrap; lower = 2.5th, upper = 97.5th percentile.

## Confounds / Alternative explanations
Extra parameters (B1 complexity-matched; ridge penalty both); harmonic distortion vs phase (repeat with distortion-free command); look-ahead leakage (code audit + time-reversal check: result must not improve if test data shifted into training window); sensor artifacts (controls).

## Ethics / Safety
No human participants. Shaker guarded, emergency stop, amplitude limit. Acoustic output measured; hearing protection above 85 dB(A).

## Data Availability
No data exist yet. Future raw data, code, hashes to be archived read-only and shared on a public repository.

## Status
Protocol Only. No data. No result claimed.
