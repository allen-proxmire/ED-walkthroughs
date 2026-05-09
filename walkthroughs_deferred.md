# Walkthroughs Deferred — Future Candidates

**Date flagged:** May 2026 (after the T17 / DCGT / UR-1 / RG / AB phase / Lindblad expansion of the walkthrough series).

These are walkthrough candidates identified during the audit that pairs with the gap-fill expansion. Each has closed math content somewhere in the framework's repository and would walk cleanly. None are blocking; flagged here so they don't get lost.

## Deferred candidates

1. **The 0.6 problem resolution.** $0.6 = 2 \cdot D_\mathrm{nd}(\mathrm{quantum}) = 2 \cdot 0.3$ via the dimensional-dictionary construction. Five alternative derivation routes audited (damping discriminant, reversible-slice QFT dispersion, acoustic-metric curvature, PME coarse-graining, ζ-interpolation); only the algebraic dictionary route succeeds. Source memo: `theory/The_0_6_Problem_Resolution.md`. Estimated 300 lines.

2. **Wu-Yang non-Abelian phase factor.** Downstream of T17 (gauge fields) and the AB phase walkthrough. Path-ordered exponential of the non-Abelian connection around a closed loop. Short and distinctive. ~400 lines.

3. **Berry phase.** Downstream of AB phase. Geometric phase from cyclic parameter-space evolution; same parallel-transport machinery applied to a different bundle. ~400 lines.

4. **Bandwidth-budget mechanism overview (cross-arc unification).** BH-4 (entanglement-straddling) + E-4 (monogamy) + Q-COMPUTE Class C (correlation-budget plateau) + BH-5 (area-law) as projections of one substrate mechanism. Weaves together what the existing walkthroughs each touch separately. ~500 lines.

5. **Higgs mechanism from rule-type symmetry breaking.** Source: `arcs/arc-Q/higgs_mechanism_scoping.md` — needs verification that closure is at FORCED level, not scoping level. If closed, would extend the gauge-fields and mass walkthroughs.

6. **Cluster decomposition / micro-causality.** Substrate-level account of why field operators at spacelike-separated points commute. Related to but distinct from the arrow-of-time walkthrough. Would extend the Yang-Mills and gauge-fields walkthroughs.

## Skipped candidates (covered elsewhere)

- **Why $D = 3+1$ dimensions.** The consequences of 3+1D are covered in detail across `from_primitives_to_spin_statistics.md` (anyon prohibition, π₁(Q₂) = ℤ₂, exchange/rotation identification), `from_primitives_to_dirac_equation_and_g2.md` (double cover from configuration-space topology), and `from_primitives_to_navier_stokes_smoothness.md` (2D vs 3D dimensional contrast). The *derivation* of D=3+1 from substrate primitives via NS-1 Path B-strong is not walked standalone, but the spin-statistics walkthrough §2 honestly classifies 3+1D as "a substrate-level commitment, not a derivation" within its scope. Standalone walkthrough would be the smallest-payload candidate of the audit set.

## Decision criteria for picking one

When returning to this list, sort by:

1. **Distinctive math content** — the 0.6 resolution and the Higgs mechanism (if closed) have the most ED-distinctive math.
2. **Cross-platform unification value** — the bandwidth-budget overview would strengthen the cross-domain mechanism identity that surfaced in BH / E / Q-COMPUTE.
3. **Pairing with existing walkthroughs** — Wu-Yang and Berry pair structurally with T17 + AB and would tighten the gauge sector.
