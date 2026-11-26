# GLOSSARY - STM-CPM (§7.2 + §7.1 symbols)

| Term | Definition in this theory |
| --- | --- |
| Spatial momentum | p = γmv, momentum associated with change of position. |
| Temporal momentum | pt = E/c = γmc = mc(dt/dτ), the time component of four-momentum. Established quantity; no new law implied. |
| Phase momentum | Action variable J, conjugate to phase θ (J = Emech/ω for a harmonic oscillator). |
| Continuous pi movement | Motion whose phase θ(t) is continuous, differentiable, and non-decreasing, so that it advances through successive pi-steps without jumps. |
| Pi-step | Phase advance of π radians, one half cycle. Duration τπ = π/ω; action Sπ = πJ; count Nπ = θ/π; rate νπ = ω/π = 2f. |
| Phase-state | Vector (x, v, a, θ̂, ω̂) describing instantaneous motion + estimated phase. |
| Drift | Time variation of angular frequency around ω0, measured by δ. |
| Drift index δ | Fractional frequency excursion, δ = max|ω(t) − ω0|/ω0 (dimensionless). |
| Critical drift δ* | δ* = π/(8Nd). Predicted onset where fixed-period phase error reaches quarter pi-step. For Nd=10, δ* = 0.039. |
| Nd | Reference periods per drift period, Td/T0 (dimensionless). |
| Complexity-matched baseline | Model with same regression form + comparable parameters using fixed-period Fourier terms instead of tracked phase (B1). |
| B0 / B1 / M2 | B0: kinematic baseline (no phase). B1: B0 + fixed-period Fourier (primary comparator). M2: B0 + tracked phase features (hypothesis model). |
| Δ | Relative improvement, Δ = 1 − RMSE_M2 / RMSE_B1 (dimensionless). |
| Δmin / no-benefit bound | Δmin = 0.05 (smallest meaningful improvement); no-benefit bound = 0.02. |
| η | Action calibration deviation, η = |Jmeas − Emech/ω| / (Emech/ω). E1 threshold at most 0.02. |
| ρP | Pi-step parity residual, ρP = RMS[x(t+τπ)+x(t)] / RMS[x(t)]. E1 threshold at most 0.03. |
| ρs | Spearman rank correlation (P6b: at least 0.90 across 5 drift levels). |
| Supported / Not supported | Only two final decision states for a preregistered claim. No third outcome after final stage. |
| Preregistration | Filing full protocol + thresholds + analysis code with time-stamp (planned: OSF) before any data collection. |
| Gate gn | Amplitude gate: gn = 1 if An ≥ 0.1 × Ā else 0. Prevents meaningless phase use. |
| PLL | Second-order phase-locked loop estimating θ̂, ω̂ (ξ = 0.707, ωL = 0.1ω0, warm-up 5T0). |
| Pπ | Pi-step operator: θ → θ + π; Pπ² = identity; Z2 parity symmetry. |

**Full symbol chart (§7.1):** t (s), Δt (s), h (s), r(t) (m), x,y (m), R (m), v (m/s), a (m/s²), m (kg), c = 299792458 m/s, γ (dimensionless), p (kg·m/s), E (J), Emech (J), pt (kg·m/s), τ (s), ζ (dimensionless), θ (rad), θ0 (rad), θ̂ (rad), ω (rad/s), ω0 (rad/s), ω̂ (rad/s), f (Hz), T (s), T0 (s), τπ (s), νπ (pi-steps/s), Nπ (dimensionless), J (J·s), Sπ (J·s), H (J), Pπ (operator), R(χ) (operator), χ (rad), k (dimensionless), K = 3, zn (m), An (m), Ā (m), gn (dimensionless), gmin = 0.1, en (rad), Kp,Ki (dimensionless), ξ = 0.707, ωL = 0.1ω0, δ (dimensionless), Td (s), Nd (dimensionless), δ* (dimensionless), ωd(t) (rad/s), εθ (rad), εmax (rad), y, ŷ, φ, w,b, λ (dimensionless), τs = T0/20, ℓ = 1..5, B0,B1,M2, RMSE, Δ, Δdesign = 0.15, Δmin = 0.05, σΔ = 0.12, dt, μd,σd, ρ, N,Neff,Nreq,nruns, α = 0.025, β = 0.10, z1−α = 1.960, z1−β = 1.282, η, ρP, ρs, Q, ks (N/m), fs (Hz), SNR (dB), Jmeas (J·s), CI.
