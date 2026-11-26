# Protocols - STM-CPM v1.0 (§12)

E1 operational validation | E2 controlled drift | E3 tide negative control | E4 sunspot natural drift | E5 Monte Carlo robustness.

All protocols: Protocol Only. No data. Falsification thresholds decided in advance. Order (§12.9): E1 must pass before E2; E5 before E2; E3/E4 independent after registration.

**§12.3 Decision rule (applies to E2, referenced by E3/E4/E5):**
1. Stage 1 (20 runs/δ): if lower bound Δ > 0.05 → Supported, end. If upper bound Δ < 0.02 → Not supported, end. Else go to Stage 2.
2. Stage 2 (40 runs/δ incl. Stage 1): Supported iff lower bound Δ > 0.05, else Not supported. No further stage.
3. P6a: at δ=0 upper bound Δ must be < 0.02, else P6 Not supported.
4. P6b: Spearman ρs between 5 drift levels and 5 point estimates of Δ must be ≥ 0.90, else P6 Not supported.
5. P6c: point estimate Δ at δ=0.02 must be < 0.05 and at δ=0.05 must be > that at δ=0.02, else P6 Not supported.
6. Complexity control: if M2 exceeds B1 by < 0.02 while M2 exceeds B0 by > 0.05, benefit attributed to periodic terms in B1, P5 Not supported.

**§15.1 Outcomes table:** E1 passes + E2 Supported + E5 robust → report onset/scope, follow-up engineering datasets in follow-up manuscript. E1 passes + E2 Supported + E5 not robust → restrict claim to cells where robustness holds. E1 passes + E2 Not supported → reject forecasting hypothesis for this tracker/baseline, publish null, definitions remain reference. E1 fails → do not run E2 on that apparatus, repair/replace, repeat E1. E3 replicates P6a + E4 Supported → consistent with drift-specific benefit. E3 fails P6a → drift-specific explanation not supported for tides; positive benefit recorded as observation. E4 Not supported → reported alongside E2; does not by itself overturn E2.
