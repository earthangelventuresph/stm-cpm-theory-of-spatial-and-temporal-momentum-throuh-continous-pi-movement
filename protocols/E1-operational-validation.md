# E1 - Operational Validation of Phase, Action, and Parity (§12.4)

**Tests:** P2 (energy accounting), P3, P4. **Hypothesis:** η ≤ 0.02 and ρP ≤ 0.03.

## Claim in plain language
The apparatus and definitions work: measured action J matches Emech/ω, and after one pi-step the signal is the negative of itself, as parity requires.

## Formal Prediction
Upper 95% bound of mean η ≤ 0.02 AND upper 95% bound of ρP ≤ 0.03 at all four amplitudes, with Q ≥ 200.

## Falsification Threshold
Validated ONLY if all three conditions above hold. If η fails, apparatus NOT validated and E2 does not proceed on it. If ρP fails at an amplitude, P4 Not supported at that amplitude and E2 amplitude is restricted to amplitudes that pass.

## Design
Validation study. 30 runs × 120 s. Amplitudes 2, 4, 6, 8 cm in randomized order, 7-8 runs per amplitude (same number per amplitude, 7 or 8). Empty-track noise-floor control (glider locked) before and after block.

## Apparatus / Materials
Low-friction air-track glider (mass 0.200 kg, measured to 0.1 g) between two linear springs; spring constant ks calibrated by static loading with five reference masses; laser displacement sensor (resolution ≤ 10 µm, ≥ 1 kHz); accelerometer; 24-bit synchronized DAQ with crystal clock ≤ 10 ppm; thermometer and hygrometer; reference ruler traceable to calibration certificate.

## Step-by-step Procedure
1. Calibrate ks and sensors. 2. Run 30 runs of 120 s. 3. Assign amplitude per randomized order. 4. Record empty-track control before/after. 5. Compute Emech = ½mv² + ½ksx² and ω per cycle from phase slope. 6. Compute Jmeas = (1/2π)∮ mv dx per cycle by trapezoidal integration. 7. Compute η (Eq. 35) and ρP (Eq. 36).

## Outcomes
Primary: mean η. Secondary: ρP at each amplitude; quality factor Q from amplitude decay; phase-space area per pi-step compared with πJ.

## Sample Size + Power / Analysis
Cluster bootstrap over runs for mean η and for ρP at each amplitude, with uncertainty budget (mass, ks, displacement, time base) propagated to η.

## Blinding
Run order randomized by schedule fixed in advance; analysis code frozen before data.

## Confounds
Sensor nonlinearity (checked vs reference ruler); spring nonlinearity (force-displacement calibration); air-track leveling error (empty-track control); temperature drift (logged); timebase error (checked vs reference frequency).

## Ethics / Safety
No human participants. Moving mass guarded; no loose cables; hearing protection not needed at these levels.

## Data Availability
No data exist yet. Future raw data, code, hashes to be archived read-only and shared on a public repository.

## Status
Protocol Only. No data. No result claimed.
