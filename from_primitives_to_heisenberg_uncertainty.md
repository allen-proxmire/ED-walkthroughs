# From Primitives to the Heisenberg Uncertainty Inequality

## A Walkthrough of the Event Density Derivation

**Allen Proxmire** · May 2026

---

## 1. The Question

In 1927, Werner Heisenberg published the inequality that bears his name:

```
Δx · Δp ≥ ℏ/2
```

The product of position and momentum uncertainties has a floor. No matter how the state is prepared, no matter how the measurement is performed, the uncertainty in position multiplied by the uncertainty in momentum cannot drop below half of Planck's reduced constant. The floor is sharp — there exist quantum states (Gaussian wavepackets) that saturate the bound, and no state goes below it.

The inequality is one of the most directly empirical structures in physics. It governs the diffraction of single particles through slits, the resolution limits of microscopes, the zero-point energy of harmonic oscillators, the stability of atomic ground states, the ultimate sensitivity of interferometric measurements. Any technology that pushes against the limits of precision measurement runs into ℏ/2 sooner or later.

The question this document addresses is: where does the bound come from, and why is the constant exactly ℏ/2?

In standard quantum mechanics, the answer is: the Heisenberg inequality follows from the canonical commutation relation [x̂, p̂] = iℏ together with the Cauchy-Schwarz inequality on the Hilbert space, applied to the variance operators. The argument is short, mechanical, and gives the right answer. But it leaves several deeper questions unanswered. Why is position-momentum a conjugate pair rather than just two unrelated observables? Why does the canonical commutation relation hold? Why is the constant in the commutator exactly ℏ?

Each of these questions points back to structural commitments that standard quantum mechanics treats as postulated. The position and momentum operators are postulated. The canonical commutation relation is postulated. The Hilbert space they act on is postulated. The Heisenberg inequality is then a derived consequence of postulated structure.

The Event Density framework derives the structural commitments themselves. The Hilbert space comes from U2. The momentum operator p̂ = -iℏ∇ comes from Stone's theorem applied to spatial translation symmetry on that Hilbert space (U5). The canonical commutation relation [x̂, p̂_j] = iℏ δ_ij comes automatically from the form p̂ = -iℏ∇ acting on position-representation wavefunctions. The Fourier-conjugacy of position and momentum representations comes from the same Stone identification. With all of this forced rather than postulated, the standard derivation of Heisenberg's inequality applies — and the bound ℏ/2 emerges as a derived consequence of substrate ontology, all the way down.

Like Bell-Tsirelson, Heisenberg is a place where the framework's contribution is upstream. The bound itself is mathematical physics — a theorem about Fourier transforms on L² spaces, applied to wavefunctions in the position-momentum conjugate basis. What the framework adds is forcing the structures that the standard argument requires. The Hilbert space, the momentum operator, the Fourier conjugacy — all derived rather than postulated.

That's worth being honest about upfront. The Heisenberg walkthrough does not introduce a new derivation hinge in the way Born or Schrödinger did. It shows that an established result of standard quantum mechanics survives and remains derivable when the underlying structure is itself derived from substrate primitives.

The chain has four steps:

1. The participation measure form is forced by T14, giving the complex-valued structure with U(1) phase content.

2. The inner product is forced by U2, giving the participation-measure space its Hilbert-space structure with the L² norm topology.

3. The momentum operator p̂ = -iℏ∇ is forced by U5 — Stone's theorem applied to spatial translation symmetry — with plane-wave eigenfunctions and the standard L² Fourier transform as the unique unitary intertwiner of position and momentum representations.

4. With the Fourier-conjugate position-momentum structure forced, the standard Hardy-Folland-Sitaram Fourier-uncertainty argument applies: Cauchy-Schwarz on the inner product, applied to variance operators on a function and its Fourier transform, produces Δx · Δp ≥ ℏ/2 with the sharp constant determined by the canonical commutation relation.

Steps 1, 2, and 3 are carried over from prior walkthroughs. Step 4 is the standard Fourier-uncertainty argument, walked here because that's where the specific bound emerges.

The structural payoff: Δx · Δp ≥ ℏ/2 is what falls out of Cauchy-Schwarz applied to the inner product on the U2-derived Hilbert space, evaluated against the variance operators of position and the U5-derived momentum operator. The bound is a consequence of inner-product geometry plus Fourier-conjugacy, both of which are derived structures in the framework rather than postulates.

---

## 2. The Primitives That Matter

The framework rests on substrate-level ontological commitments. The Heisenberg walkthrough uses the same working subset that Born, Schrödinger, and Bell-Tsirelson used:

**Micro-events.** Discrete acts of becoming, vertices in a graph spanning the event manifold.

**Participation.** The relation connecting micro-events. Participation is homogeneous — no vertex is privileged at the primitive level.

**Channels.** Stable subgraphs along which a chain can repeatedly instantiate its update rule. Channels are primitive ontological objects.

**Bandwidth.** The graded measure of participation, supplied as a non-negative real edge weight. Bandwidth has a four-band orthogonal decomposition.

**Polarity.** The U(1)-valued phase relation between a chain's update rule and the local ED-flow direction. Supplies the e^(iπ_K) phase in the participation measure.

**ED gradient.** The participation graph carries a continuous spatial axis with no preferred origin. Translations along this axis are well-defined.

**Commitment.** The discrete event in which a chain selects one channel from those available.

Three ingredients arrive as forced consequences of these primitives:

**T14:** The participation measure form P_K = √b_K · e^(iπ_K), with the square root forced by the Cauchy functional equation on bandwidth additivity and the complex phase forced by Frobenius's theorem on real division algebras.

**U2:** The sesquilinear inner product on the participation-measure space, with the Hilbert-space structure forced by primitive-level aggregation arguments (counting measures, local pointwise pairing, sesquilinearity from U(1) invariance). The continuum lift carries an explicit conformal gauge that's a description redundancy — every inner-product value is gauge-invariant.

**U5:** The momentum operator p̂ = -iℏ∇ as the unique self-adjoint generator of spatial translation on the U2 Hilbert space, with plane-wave eigenfunctions ⟨x|k⟩ = (2πℏ)^(-d/2) · e^(ik·x/ℏ) and the standard L² Fourier transform as the unique unitary intertwiner of position and momentum representations.

That's the structural setup. The Heisenberg argument runs on this.

---

## 3. The Position Operator and Canonical Commutation

Before the uncertainty argument, two structural pieces need to be made explicit: the position operator x̂ on the U2 Hilbert space, and the canonical commutation relation [x̂, p̂_j] = iℏ δ_ij that the Heisenberg argument requires.

### 3.1 The position operator

In the position representation of the U2 Hilbert space, wavefunctions ψ(x) are complex-valued functions of the spatial coordinate x ∈ R^d. The position operator x̂ acts by multiplication:

```
(x̂_i ψ)(x) = x_i · ψ(x)
```

This is a self-adjoint operator: multiplication by a real-valued coordinate function is self-adjoint on the L² inner product. Its eigenvalues are the real numbers (the spectrum is continuous), and its generalized eigenfunctions are position-localized states |x⟩.

The position operator's status in the framework is structural rather than derived in the same Stone-theorem sense as p̂. The position coordinate x is a primitive feature of the participation graph — it's the spatial axis that the ED gradient primitive supplies. The position operator x̂ is the operator-valued representation of that spatial coordinate on the U2 Hilbert space, with the eigenvalue interpretation following from the spectral theorem applied to multiplication operators on L² spaces.

This is worth saying plainly. The framework treats spatial position as a structural feature of the participation graph — vertices have spatial location, micro-events occur at spatial loci, the gradient primitive supplies a continuous spatial axis. The position operator is the operator-valued lift of this spatial-coordinate structure to the Hilbert space. Unlike the momentum operator, it doesn't require a Stone-theorem identification of a translation generator — the spatial coordinate is already there in the substrate.

### 3.2 The canonical commutation relation

With x̂ and p̂ both available on the U2 Hilbert space, their commutator is computable directly. In the position representation:

```
([x̂_i, p̂_j] ψ)(x) = x̂_i p̂_j ψ(x) - p̂_j x̂_i ψ(x)
                    = x_i · (-iℏ ∂_j ψ(x)) - (-iℏ ∂_j)(x_i ψ(x))
```

Computing the second term using the product rule:

```
(-iℏ ∂_j)(x_i ψ(x)) = -iℏ · [δ_ij ψ(x) + x_i ∂_j ψ(x)]
                     = -iℏ δ_ij ψ(x) - iℏ x_i ∂_j ψ(x)
```

Subtracting:

```
([x̂_i, p̂_j] ψ)(x) = -iℏ x_i ∂_j ψ(x) - [-iℏ δ_ij ψ(x) - iℏ x_i ∂_j ψ(x)]
                    = iℏ δ_ij ψ(x)
```

So:

```
[x̂_i, p̂_j] = iℏ δ_ij
```

This is the canonical commutation relation. It's not postulated separately — it's a direct consequence of x̂ being multiplication by x and p̂ being -iℏ∇ on position-representation wavefunctions, applied to differentiable functions where the product rule holds.

The factor of ℏ in the commutator comes from the factor of ℏ in p̂ = -iℏ∇. That factor was inherited via U5's identification of p̂ as the spatial-translation generator with the convention placing ℏ in the exponential T_a = exp(i p̂ · a / ℏ). The commutator inherits the same ℏ.

The δ_ij comes from the fact that ∂_j of x_i is δ_ij — different spatial directions are independent, and the product rule applied to x_i and ∂_j picks out exactly the diagonal Kronecker contribution.

### 3.3 What this delivers

The canonical commutation relation [x̂_i, p̂_j] = iℏ δ_ij is now a derived consequence of U5's identification of p̂ plus the multiplication-operator definition of x̂. It's not a separate axiomatic commitment. The relation that drives the Heisenberg argument is structural rather than postulated.

This is a small but real piece of structural derivation that happens automatically once the framework's earlier pieces are in place. It's worth surfacing because the Heisenberg argument leans on it directly.

---

## 4. The Variance Operator Setup

The Heisenberg inequality concerns variances of measurement outcomes. To set up the argument, we need to express variances in operator-theoretic language.

### 4.1 Expectation values and variances

For a normalized state |ψ⟩ ∈ H and a self-adjoint operator Â, the expectation value is:

```
⟨Â⟩ = ⟨ψ|Â|ψ⟩
```

The variance is:

```
(ΔA)² = ⟨ψ|(Â - ⟨Â⟩)²|ψ⟩ = ⟨Â²⟩ - ⟨Â⟩²
```

The standard deviation ΔA is the square root of the variance. For position and momentum:

```
(Δx_i)² = ⟨ψ|(x̂_i - ⟨x̂_i⟩)²|ψ⟩
(Δp_j)² = ⟨ψ|(p̂_j - ⟨p̂_j⟩)²|ψ⟩
```

These are computable from the U2 inner product applied to the appropriate operators.

### 4.2 Centered operators

Define the centered operators:

```
Â := x̂_i - ⟨x̂_i⟩ · I
B̂ := p̂_j - ⟨p̂_j⟩ · I
```

These are self-adjoint operators whose expectation values vanish: ⟨Â⟩ = 0 and ⟨B̂⟩ = 0.

The commutator of the centered operators equals the commutator of the originals, because constants commute with operators:

```
[Â, B̂] = [x̂_i - ⟨x̂_i⟩ · I, p̂_j - ⟨p̂_j⟩ · I]
       = [x̂_i, p̂_j]
       = iℏ δ_ij
```

The variances are now ⟨Â²⟩ = (Δx_i)² and ⟨B̂²⟩ = (Δp_j)².

### 4.3 What the argument needs

To prove Δx_i · Δp_j ≥ (ℏ/2) · |δ_ij|, we need to show:

```
⟨Â²⟩ · ⟨B̂²⟩ ≥ (ℏ/2)² · |δ_ij|²
```

The case i ≠ j is trivial — the right side is zero, so the inequality holds vacuously. The interesting case is i = j, where:

```
(Δx_i)² · (Δp_i)² ≥ (ℏ/2)²
```

or equivalently:

```
Δx · Δp ≥ ℏ/2
```

(suppressing the index for the same direction). This is what we need to derive from Cauchy-Schwarz applied to the inner product.

---

## 5. The Cauchy-Schwarz Argument

The Heisenberg inequality follows from the Cauchy-Schwarz inequality applied to specific vectors constructed from the centered operators. The argument is short and clean once the setup is in place.

### 5.1 Cauchy-Schwarz on the U2 inner product

The Cauchy-Schwarz inequality states that for any two vectors |φ⟩, |χ⟩ in a Hilbert space:

```
|⟨φ|χ⟩|² ≤ ⟨φ|φ⟩ · ⟨χ|χ⟩
```

This is a structural property of any sesquilinear inner product on a complex vector space. U2 establishes that the participation-measure space has such an inner product; Cauchy-Schwarz follows automatically.

### 5.2 Applying to the centered operators

Define two vectors in H:

```
|φ⟩ := Â|ψ⟩ = (x̂_i - ⟨x̂_i⟩)|ψ⟩
|χ⟩ := B̂|ψ⟩ = (p̂_j - ⟨p̂_j⟩)|ψ⟩
```

Apply Cauchy-Schwarz:

```
|⟨φ|χ⟩|² ≤ ⟨φ|φ⟩ · ⟨χ|χ⟩
```

Computing each piece:

```
⟨φ|φ⟩ = ⟨ψ|Â†Â|ψ⟩ = ⟨ψ|Â²|ψ⟩ = (Δx_i)²
⟨χ|χ⟩ = ⟨ψ|B̂†B̂|ψ⟩ = ⟨ψ|B̂²|ψ⟩ = (Δp_j)²
⟨φ|χ⟩ = ⟨ψ|Â†B̂|ψ⟩ = ⟨ψ|ÂB̂|ψ⟩
```

(using self-adjointness of Â and B̂ to drop the daggers).

So Cauchy-Schwarz gives:

```
|⟨ψ|ÂB̂|ψ⟩|² ≤ (Δx_i)² · (Δp_j)²
```

### 5.3 Extracting the commutator

The product ÂB̂ can be split into symmetric and antisymmetric parts:

```
ÂB̂ = (1/2){Â, B̂} + (1/2)[Â, B̂]
```

where {Â, B̂} = ÂB̂ + B̂Â is the anticommutator and [Â, B̂] = ÂB̂ - B̂Â is the commutator. The anticommutator of self-adjoint operators is self-adjoint; the commutator of self-adjoint operators is anti-Hermitian (its expectation value is purely imaginary).

Taking the expectation value:

```
⟨ÂB̂⟩ = (1/2)⟨{Â, B̂}⟩ + (1/2)⟨[Â, B̂]⟩
```

The first term is real (expectation of a self-adjoint operator). The second term is purely imaginary (expectation of an anti-Hermitian operator). For a complex number z = a + ib:

```
|z|² = a² + b² ≥ b² = |Im(z)|²
```

So:

```
|⟨ÂB̂⟩|² ≥ |Im(⟨ÂB̂⟩)|² = |(1/2)⟨[Â, B̂]⟩|² · (1/i)²
```

Working through the arithmetic carefully: ⟨[Â, B̂]⟩ is purely imaginary (let's call it ic for real c), so:

```
Im(⟨ÂB̂⟩) = Im((1/2)⟨{Â,B̂}⟩ + (1/2)(ic)) = c/2
```

And:

```
|⟨ÂB̂⟩|² ≥ (c/2)² = (1/4) |⟨[Â, B̂]⟩|²
```

(using |ic|² = c² for real c).

### 5.4 The canonical commutation relation enters

Section 3 established [Â, B̂] = [x̂_i, p̂_j] = iℏ δ_ij. So:

```
⟨[Â, B̂]⟩ = iℏ δ_ij
|⟨[Â, B̂]⟩|² = ℏ² δ_ij²
```

Substituting:

```
|⟨ÂB̂⟩|² ≥ (1/4) · ℏ² δ_ij²
```

### 5.5 Combining with Cauchy-Schwarz

From Section 5.2:

```
|⟨ÂB̂⟩|² ≤ (Δx_i)² · (Δp_j)²
```

From Section 5.4:

```
|⟨ÂB̂⟩|² ≥ (ℏ/2)² · δ_ij²
```

Combining:

```
(Δx_i)² · (Δp_j)² ≥ (ℏ/2)² · δ_ij²
```

Taking square roots:

```
Δx_i · Δp_j ≥ (ℏ/2) · |δ_ij|
```

For i = j (same spatial direction), this gives:

```
Δx · Δp ≥ ℏ/2
```

which is the Heisenberg inequality.

For i ≠ j (different directions), δ_ij = 0 and the inequality reduces to Δx_i · Δp_j ≥ 0, which is trivial since variances are non-negative. Position in one direction and momentum in a different direction don't have a non-trivial uncertainty relation — that's the structural meaning of the Kronecker delta in the canonical commutation relation.

### 5.6 The bound is tight

The Heisenberg bound is sharp — Gaussian wavepackets saturate it:

```
ψ(x) = (2πσ²)^(-1/4) · exp(-(x - x_0)² / (4σ²)) · exp(i p_0 x / ℏ)
```

For this state, Δx = σ and Δp = ℏ/(2σ), giving Δx · Δp = ℏ/2 exactly. Cauchy-Schwarz becomes an equality when the two vectors are linearly dependent, which is the structural condition that Gaussian wavepackets satisfy in the position-momentum conjugate setup.

The tightness of ℏ/2 is what makes the Heisenberg bound physically meaningful. It's not an upper bound that uncertainties happen to satisfy — it's the exact floor, achievable in principle by Gaussian states and approached in practice by carefully prepared wavepackets in atomic and molecular systems.

### 5.7 What the argument required

Walking through the Heisenberg argument, several structural ingredients were used:

The U2 Hilbert space H with its sesquilinear inner product, which makes Cauchy-Schwarz available.

The position operator x̂ as multiplication by the spatial coordinate, with self-adjointness on the L² inner product.

The momentum operator p̂ = -iℏ∇ from U5, with its specific factor of ℏ inherited from the Stone-theorem convention.

The canonical commutation relation [x̂_i, p̂_j] = iℏ δ_ij, which Section 3 derived from the explicit forms of x̂ and p̂ acting on differentiable wavefunctions via the product rule.

The split of ÂB̂ into symmetric and antisymmetric parts, which is a standard operator-algebraic identity that holds for any pair of operators on any Hilbert space.

In standard quantum mechanics, every one of these ingredients is part of the postulated formalism. In the framework, every one is derived: the Hilbert space comes from U2, the inner product comes from U2, Cauchy-Schwarz comes from the inner product, the momentum operator comes from U5, the canonical commutation relation comes from the explicit forms of x̂ and p̂. The factor of ℏ in the bound is the same ℏ that appears in p̂ = -iℏ∇, inherited via U5's Stone-theorem convention.

The Heisenberg bound ℏ/2 is therefore a derived consequence of substrate ontology, all the way down. The structures the standard argument requires are now forced rather than postulated.

---

## 6. The Fourier-Conjugacy Reading

There's a second way to see why position and momentum have a non-trivial uncertainty product, and it's worth surfacing because it makes the structural picture clearer.

### 6.1 Fourier transforms and uncertainty

The standard L² Fourier transform between position and momentum representations is, by U5, the unique unitary intertwiner of position and momentum on the U2 Hilbert space. A wavefunction ψ(x) in position representation has a momentum-representation counterpart ψ̃(p) given by:

```
ψ̃(p) = (2πℏ)^(-d/2) · ∫ e^(-ip·x/ℏ) ψ(x) dx
```

Parseval's theorem (a consequence of the Fourier transform being a unitary intertwiner on L²) gives:

```
∫ |ψ(x)|² dx = ∫ |ψ̃(p)|² dp
```

The variances are computed in the respective representations:

```
(Δx)² = ∫ (x - ⟨x⟩)² |ψ(x)|² dx
(Δp)² = ∫ (p - ⟨p⟩)² |ψ̃(p)|² dp
```

### 6.2 The Hardy-Folland-Sitaram theorem

A classical result in Fourier analysis states: for any function f ∈ L²(R^d) with Fourier transform f̃, the spread of f and f̃ are inversely related. Specifically:

```
(Δx)² · (Δp)² ≥ (ℏ/2)²
```

This is the Fourier-uncertainty inequality. It's a theorem about L² functions and their Fourier transforms — it doesn't require quantum mechanics for its statement or its proof. The factor of ℏ/2 comes from the specific Fourier convention (the factor of (2πℏ)^(-d/2) and the exponent ip·x/ℏ).

Different Fourier conventions give different specific constants, but the structural fact — that a function and its Fourier transform cannot both be sharply localized — is independent of convention. The convention used by U5, which placed ℏ in the exponential T_a = exp(i p̂ · a / ℏ), gives the constant ℏ/2.

### 6.3 What this tells us

The Heisenberg uncertainty inequality is a structural consequence of position and momentum being Fourier conjugates. The bound ℏ/2 emerges from the specific Fourier convention that U5's Stone-theorem identification fixed.

In standard quantum mechanics, this connection is sometimes obscured because the canonical commutation relation [x̂, p̂] = iℏ is presented as a separate postulate rather than as a derived consequence of position-momentum being Fourier-conjugate. The framework makes the connection explicit: U5 forces the Fourier conjugacy as a consequence of Stone's theorem on spatial translation, and Heisenberg's inequality is then a Fourier-uncertainty result that operates on that conjugacy.

The two paths to Heisenberg — Cauchy-Schwarz on the canonical commutator (Section 5) and Fourier-uncertainty on the conjugate representations (this section) — give the same bound for the same reason. They're not independent arguments; they're two views of the same structural fact. The canonical commutation relation [x̂, p̂] = iℏ is what you get when you compute the commutator of position and the Fourier-conjugate translation generator. The Heisenberg bound ℏ/2 is what Cauchy-Schwarz produces when applied to that commutator, or equivalently what Fourier-uncertainty produces when applied to the conjugate variances.

The framework's contribution is making both paths derived rather than postulated. The Hilbert space, the inner product, the momentum operator, and the Fourier conjugacy are all forced by substrate primitives. The Heisenberg bound emerges from any of these structures via standard mathematical physics.

---

## 7. What the Framework Adds

It's worth being precise about what changes when the framework is in place versus when it isn't.

In standard quantum mechanics, the Heisenberg inequality is a theorem given the postulated formalism. The Hilbert space is postulated. The inner product is postulated. The position and momentum operators are postulated. The canonical commutation relation is postulated (or, equivalently, the Fourier-conjugacy of position and momentum representations is postulated). The Cauchy-Schwarz argument runs on these postulates and produces ℏ/2 as a sharp lower bound on the position-momentum uncertainty product. The bound is real, the value is exact, and the argument is valid.

In the framework, the same Cauchy-Schwarz argument runs on the same Hilbert-space structure — but that structure is now derived from substrate-level commitments rather than postulated. The complex-valued participation measure is forced by T14. The inner product is forced by U2. The momentum operator p̂ = -iℏ∇ is forced by U5 — Stone's theorem applied to spatial translation. The canonical commutation relation is forced by the explicit forms of x̂ and p̂ acting on wavefunctions via the product rule. The Fourier conjugacy is forced by U5's identification of the standard L² Fourier transform as the unique unitary intertwiner.

What this changes:

The ℏ/2 bound is no longer the output of a chain of postulates ending at "and the canonical commutation relation has this commutator." It is the output of a chain of derived theorems beginning at substrate primitives and producing the same value through the same Cauchy-Schwarz argument. The mathematical content of Heisenberg's 1927 derivation is unchanged. What changes is the foundational status of the structures the derivation operates on.

Like Bell-Tsirelson, this is a smaller payload than what Born or Schrödinger's walkthroughs delivered. The framework's contribution is upstream: it forces the Hilbert space, inner product, and Fourier conjugacy that the standard Heisenberg argument requires. The bound itself comes from Cauchy-Schwarz plus the canonical commutation relation, both of which are derived structures in the framework.

The factor of ℏ in the bound is worth one specific note. In the framework, ℏ enters via U5's convention placing it in the spatial-translation operator T_a = exp(i p̂ · a / ℏ). This convention is inherited rather than derived — the numerical value of ℏ comes from the dimensional-atlas Madelung anchoring, which is a separate program component that fixes ℏ via the structural correspondence between participation-measure evolution and standard quantum mechanics. The framework derives the structural form within which ℏ appears; it inherits the numerical value of ℏ itself.

This is honest framing. The ℏ/2 bound is forced as a structural consequence of substrate primitives plus the inherited value of ℏ. The framework does not claim to derive Planck's constant from primitive ontology; it claims to derive the structural form of quantum mechanics within which Planck's constant appears.

---

## 8. The Place of This Result

The Heisenberg uncertainty inequality completes the four-part walkthrough series of foundational postulates of non-relativistic single-particle quantum mechanics.

The Born walkthrough established the probability rule of quantum mechanics from substrate primitives, with T14's Cauchy argument as the substantive new derivation step.

The Schrödinger walkthrough established the dynamical evolution rule, with Galilean Lie algebra integration producing the kinetic-plus-potential Hamiltonian and the factor of 1/(2m) emerging from a chain-rule Jacobian.

The Bell-Tsirelson walkthrough established the maximum quantum correlation between entangled systems, with U2's bipartite extension forcing the tensor-product Hilbert space that Tsirelson's operator-algebraic argument requires.

The Heisenberg walkthrough establishes the floor on position-momentum uncertainty, with U5's Stone-theorem identification forcing the Fourier-conjugate structure that the standard Cauchy-Schwarz argument requires.

Together, these four walkthroughs cover all four foundational postulates of non-relativistic single-particle quantum mechanics. Each postulate emerges from the substrate ontology rather than being assumed independently. The Hilbert space comes from U2. The Born rule comes from non-contextuality forced by the channel-as-primitive ontology, plus Gleason-Busch closure. The Schrödinger equation comes from Stone's theorem on time translation plus Galilean Lie algebra closure. The Bell-Tsirelson bound comes from Cauchy-Schwarz on the bipartite U2 inner product applied to the CHSH operator. The Heisenberg inequality comes from Cauchy-Schwarz on the U2 inner product applied to the variance operators of position and U5's momentum.

The structural picture: quantum mechanics is, at root, what the participation-graph ontology produces when you ask about probability, dynamics, correlations between separated systems, and uncertainty floors. Each foundational postulate is a derived theorem of the substrate, with no independent axiomatic content beyond what the primitives supply.

---

## 9. What This Argument Establishes

The chain runs:

Primitives (micro-events, participation, channels, bandwidth, polarity, ED gradient, commitment) → T14 (participation measure form forced) → U2 (inner product on participation-measure space forced) → U5 (momentum operator p̂ = -iℏ∇ forced via Stone's theorem on spatial translation) → canonical commutation relation [x̂, p̂_j] = iℏ δ_ij (forced by explicit forms of x̂ as multiplication and p̂ as -iℏ∇ acting via product rule) → Cauchy-Schwarz on the inner product applied to centered position and momentum operators → Δx · Δp ≥ ℏ/2.

The ℏ/2 bound is now a derived consequence of substrate ontology rather than a consequence of postulated Hilbert-space structure plus a postulated canonical commutation relation. The mathematical content of Heisenberg's 1927 derivation is unchanged — what changes is the foundational status of the structures the derivation operates on.

The framework reproduces the Heisenberg inequality exactly. It does not predict any new uncertainty relation, any new bound, or any deviation from standard quantum mechanics in regimes where standard QM has been tested. Position and momentum are bounded by ℏ/2 in the framework just as in standard QM. What changes is that the bound is now traceable to substrate primitives without invoking the Hilbert-space postulate or the canonical commutation postulate as independent commitments.

For experimentally verified uncertainty relations — single-photon diffraction, neutron interferometry, atom-trap measurements, squeezed-light experiments — every measurement that approaches the ℏ/2 floor confirms the bound to within experimental precision. The framework predicts the same. Heisenberg uncertainty is not a place where the framework differs from standard quantum mechanics; it's a place where the framework derives the structures that produce the bound rather than assuming them.

Whether the substrate commitments themselves are right is the load-bearing question, as in every other walkthrough. The framework stands or falls on whether participation, bandwidth, channels, polarity, and the rest are the correct foundational concepts. The empirical exposure of the framework lives elsewhere — in the soft-matter mobility law's prediction of sub-Fickian recovery in concentrated BSA, in the substrate-gravity prediction of MOND's transition acceleration, in other channels where the framework makes predictions that depart from standard physics.

For Heisenberg specifically, the structural case is closed. The ℏ/2 bound is what Cauchy-Schwarz on the U2-derived inner product produces when applied to the variance operators of position and the U5-derived momentum operator. The Hilbert space, the momentum operator, and the canonical commutation relation are no longer postulates; the bound is no longer suspended above an axiomatic gap. Every piece traces back to substrate primitives, with the numerical value of ℏ inherited via the dimensional-atlas Madelung anchoring.

The four-part walkthrough series — Born, Schrödinger, Bell-Tsirelson, Heisenberg — now covers all four foundational postulates of non-relativistic single-particle quantum mechanics. Each walkthrough stands alone as a self-contained argument from substrate primitives to a foundational postulate. Read together, they constitute a unified treatment showing that the postulates of QM are derived theorems of the participation-graph ontology rather than independent axiomatic commitments.

---

## 10. References

- Heisenberg, W. "Über den anschaulichen Inhalt der quantentheoretischen Kinematik und Mechanik." *Zeitschrift für Physik* 43, 172–198 (1927).
- Kennard, E. H. "Zur Quantenmechanik einfacher Bewegungstypen." *Zeitschrift für Physik* 44, 326–352 (1927).
- Robertson, H. P. "The Uncertainty Principle." *Physical Review* 34, 163–164 (1929).
- Folland, G. B., and Sitaram, A. "The Uncertainty Principle: A Mathematical Survey." *Journal of Fourier Analysis and Applications* 3, 207–238 (1997).
- Proxmire, A. *The Born Rule as a Forced Theorem of Event Density: A Gleason–Busch Reconstruction from First Principles.* April 2026.
- Proxmire, A. *The Inner Product as Forced Structure in Event Density: Discrete Derivation, Continuum Lift, and Gauge-Invariant Completion.* April 2026.
- Proxmire, A. *U5: The Forced Structure of Translation Symmetry and the Momentum Operator.* April 2026.
- Proxmire, A. *Theorem 14: The Participation Measure Form.* (T14 derivation memo.)
- Proxmire, A. *Event Density: One Substrate, Three Domains.* April 2026.
- Reed, M., and Simon, B. *Methods of Modern Mathematical Physics, Volume I: Functional Analysis.* Academic Press, 1980.
- The full Event Density corpus, including all forced theorems and supporting memos, is available at https://github.com/allen-proxmire/event-density.
