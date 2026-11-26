# E3 - Tide-Gauge Negative Control (§12.6)

**Tests:** P6a on natural data with known frequencies. **Hypothesis:** Δ < 0.02 because astronomical tide has exactly known frequencies, effectively zero-drift.

## Claim in plain language
Where frequency is exactly known, tracked phase should add nothing. If it adds value here, the drift-specific explanation fails for this domain.

## Formal Prediction
Pooled Δ upper bound < 0.02.

## Falsification Threshold
P6a replicated iff upper bound of pooled Δ < 0.02. If lower bound > 0.02 then P6a Not supported on natural data; added value present without drift; drift-specific explanation Not supported for tides (positive benefit recorded as observation). Any other result (interval straddling 0.02) = P6a Not supported (rule requires upper bound < 0.02).

## Design
Natural-data negative control. First 3 eligible stations alphabetically by name, each at least 10 years continuous hourly data, at most 2% missing hours. Train first 70%, test last 30%. Pool 3 stations. Horizon h = 6 h (about 0.5T0, T0 of M2 = 12.42 h).

## Apparatus / Materials
Public hourly sea-level records from University of Hawaii Sea Level Center research-quality archive or equivalent public archive; common code §12.1; Permanent Service for Mean Sea Level catalogue for station metadata.

## Step-by-step Procedure
1. Sort eligible stations alphabetically. 2. Take first 3 meeting criteria. 3. Train 70% / test 30% per record. 4. B1 = B0 + fixed harmonic terms at 8 constituents (M2, S2, N2, K2, K1, O1, P1, Q1); M2 = B0 + tracked phase of dominant semidiurnal component. 5. Forecast h = 6 h. 6. Pool 3 stations.

## Outcomes
Primary: pooled Δ. Secondary: station-level Δ.

## Sample Size + Power / Analysis
Moving-block bootstrap, 30-day blocks, 10,000 resamples.

## Blinding
Station selection rule fixed in advance (alphabetical, eligibility criteria); no station cherry-picking after seeing results.

## Frozen Analysis Plan
Common analysis §12.1 adapted for tides; no post-hoc constituent changes.

## Confounds
Non-tidal surge variability; nodal modulation (18.6-year); data gaps; instrument datum shifts (checked by station metadata).

## Ethics / Safety
Public data only. No ethical approval needed. No safety requirements.

## Data Availability
No data exist yet. Future raw data, code, hashes to be archived read-only and shared on a public repository.

## Status
Protocol Only. No data. No result claimed.
