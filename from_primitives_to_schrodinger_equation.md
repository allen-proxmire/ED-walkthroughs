# From Primitives to the Schrödinger Equation

## A Walkthrough of the Event Density Derivation

**Allen Proxmire** · May 2026

---

## 1. The Question

The Schrödinger equation has been quantum mechanics's central dynamical statement for nearly a century:

```
iℏ ∂_t ψ = Ĥ ψ
```

with the Hamiltonian taking the standard non-relativistic form:

```
Ĥ = ℏ²|p̂|² / (2m) + V(x̂)
```

This equation has been used in calculations of atomic spectra, molecular bonding, semiconductors, neutron interferometry, and uncountably many other empirical settings. It works. The question this document addresses is *why* it has the form it does.

In standard quantum mechanics, the Schrödinger equation is a postulate. The Hilbert space is given. The momentum operator p̂ = -iℏ∇ is given. The kinetic energy form |p̂|²/(2m) is borrowed from classical mechanics — quantum mechanics inherits the factor of 1/2 from the classical formula T = p²/(2m) without further justification. The first-order time derivative is chosen because empirically it works. Each piece is accepted because the resulting equation matches experiment.

The Event Density framework derives the Schrödinger equation, in its full standard form, from a smaller set of structural commitments about what reality is made of at the substrate level. Every piece — the Hilbert space, the momentum operator, the linearity, the first-order time structure, the specific kinetic-plus-potential form, the factor of 1/(2m) — emerges as a forced consequence of the framework rather than as a separate postulate.

The structural shape of this derivation is different from the Born rule's. Born runs through Gleason-Busch as a closure step on a probability rule. Schrödinger runs through Stone's theorem applied twice — once on spatial translation, once on time translation — closed by Galilean Lie algebra integration that identifies the time-translation generator with the kinetic-plus-potential operator. The same theorem, applied to the same Hilbert space, on two different symmetries, produces the kinematic and dynamical generators respectively. The Galilean algebra binds them together.

The chain has five load-bearing steps:

1. The participation measure is forced by T14 to have the form √b · e^(iπ).
2. The inner product is forced by U2, giving the participation-measure space its Hilbert-space structure.
3. Stone's theorem applied to spatial translation forces the existence and uniqueness of the momentum operator p̂ = -iℏ∇ (this is U5).
4. Stone's theorem applied to time translation forces the existence and uniqueness of a self-adjoint time-evolution generator, with linearity and first-order time structure as automatic consequences (this is U3, parts F1-F4).
5. Galilean Lie algebra closure identifies the time-translation generator with the kinetic-plus-potential Hamiltonian, with the factor of 1/(2m) emerging as the integration Jacobian of the Galilean commutator condition (this is U3 part F5, and equivalently U4).

Steps 1 and 2 were the foundation of the Born walkthrough; they're carried over here. Steps 3, 4, and 5 are new and carry the substantive dynamical content.

The structural payoff: the Schrödinger equation is, at its root, what falls out when Stone's theorem is applied to time-translation symmetry on the participation-measure Hilbert space, and the resulting generator is identified with the Galilean-Lie-algebra-forced kinetic-plus-potential operator. The first-order time derivative is a consequence of operator exponentials, not a chosen feature. The factor of 1/(2m) is a consequence of integrating a commutator, not a borrowing from classical mechanics.

---

## 2. The Primitives That Matter

The framework rests on a set of substrate-level ontological commitments. The Born walkthrough used a working subset; the Schrödinger walkthrough uses the same subset plus one more — relational timing — that supplies the time axis on which the dynamical generator lives.

**Micro-events.** Reality consists of discrete acts of becoming. Each micro-event is a vertex in a graph that spans the event manifold.

**Participation.** Micro-events don't exist in isolation; they participate in one another's becoming. The graph's edges encode participation relations. The participation relation is homogeneous — no vertex is privileged at the primitive level.

**Channels.** A channel is a stable subgraph along which a chain (the substrate-level object the framework calls a "particle") can repeatedly instantiate its update rule. Channels are *primitive ontological objects* — their identity is intrinsic to the graph, not a basis-relative label.

**Bandwidth.** Bandwidth is the graded measure of participation, supplied as a non-negative real edge weight. Each channel K at vertex u has a bandwidth b_K(u). Bandwidth admits a four-band orthogonal decomposition with conservation along chains.

**Polarity.** Polarity is the U(1)-valued phase relation between a chain's update rule and the local ED-flow direction. It supplies the phase content e^(iπ_K) in the participation measure.

**ED gradient.** The participation graph carries a continuous spatial axis with no preferred origin. Translations along this axis are well-defined and admissible.

**Relational timing.** This is the new primitive that enters the Schrödinger derivation. It supplies the continuous time axis at the structural level, with translation symmetry along that axis (no privileged instant of time, no privileged time origin).

**Commitment.** Commitment is the discrete event in which a chain selects one channel from those available at a vertex.

That's the working set. Two additional ingredients arrive as forced consequences of these primitives, established in prior work:

The participation measure form, P_K = √b_K · e^(iπ_K), forced by the Cauchy functional equation on bandwidth additivity (which fixes the square root) and Frobenius's theorem on real division algebras (which fixes the complex-valued phase). This is T14.

The sesquilinear inner product on the participation-measure space, forced by primitive-level aggregation arguments (counting measure on channels and vertices, local pointwise pairing) plus U(1) invariance (which forces sesquilinearity over alternative bilinear pairings). This is U2. The continuum lift carries an explicit conformal gauge that's a description redundancy, not a physical ambiguity — every inner-product value is gauge-invariant.

With T14 and U2 in hand, the participation-measure space P is a complex Hilbert space H with sesquilinear inner product. That's the arena on which the rest of the Schrödinger derivation operates.

---

## 3. Forcing the Momentum Operator

The first dynamical step is the spatial-translation generator. The argument runs through Stone's theorem, applied to the abelian translation group acting on the U2 Hilbert space.

### 3.1 Translation symmetry as a kinematic feature

Define the spatial translation operator T_a acting componentwise on participation-measure components:

```
(T_a P)_K(x) := P_K(x - a)
```

for a ∈ R^d. Three primitive-level observations establish this as a symmetry of the participation graph:

The participation relation does not privilege any vertex (graph homogeneity). Translating the entire structure by a shifts every vertex by the same amount; no structural feature distinguishes the original from the translated configuration.

The spatial axis is continuous and unbounded. Translations along it are well-defined for any a ∈ R^d.

No primitive-level structure singles out a privileged origin or magnitude.

Translation symmetry is therefore a kinematic property of the participation graph — a symmetry of its static structure, not of any dynamical evolution. No reference to time evolution or to a Hamiltonian appears in this argument.

### 3.2 Linearity

Translation acts linearly on participation-measure components:

```
T_a(αP + βQ)_K(x) = αP_K(x - a) + βQ_K(x - a)
                  = α(T_a P)_K(x) + β(T_a Q)_K(x)
```

for any α, β ∈ C and any P, Q ∈ H.

### 3.3 Unitarity on the U2 Hilbert space

For any P, Q ∈ H:

```
⟨T_a P | T_a Q⟩ = Σ_K ∫ P*_K(x - a) Q_K(x - a) dμ(x)
                = Σ_K ∫ P*_K(x') Q_K(x') dμ(x')      (substituting x' = x - a)
                = ⟨P | Q⟩
```

The substitution works because the U2 measure is translation-invariant on the spatial axis — which is itself a primitive-level fact (the spatial axis carries a translation-invariant Lebesgue measure with no preferred origin). Translation operators preserve the U2 inner product.

### 3.4 Group structure and continuity

Direct calculation: T_a T_b = T_(a+b), T_0 = I, T_(-a) = T_a^(-1). The translation group is abelian and isomorphic to (R^d, +).

For any P with components in L²(dμ), the map a ↦ T_a P is strongly continuous because L²-translation is strongly continuous (a standard property of L², inherited by the direct integral structure of the U2 Hilbert space across the channel index).

### 3.5 Stone's theorem identifies the generator

Stone's theorem on one-parameter unitary groups: every strongly continuous one-parameter unitary group on a Hilbert space has a unique self-adjoint generator.

Applied to the spatial translation group along each direction ê_i, with a = a_i ê_i:

```
T_(a_i ê_i) = exp(i p̂_i a_i / ℏ)
```

for a unique self-adjoint operator p̂_i. The d generators p̂_i commute pairwise (because the abelian structure of the translation group means T_a T_b = T_(a+b) = T_b T_a), so the joint exponentiation is well-defined:

```
T_a = exp(i p̂ · a / ℏ),   p̂ := (p̂_1, ..., p̂_d)
```

The generator p̂ is unique. Self-adjointness is automatic from Stone's theorem.

### 3.6 The position-representation form

In the position representation of H, the translation operator acts on a wavefunction ψ(x) by:

```
T_a ψ(x) = ψ(x - a)
```

Taylor expansion in a:

```
T_a ψ(x) = exp(-a · ∇) ψ(x)
```

Comparing with T_a = exp(i p̂ · a / ℏ):

```
i p̂ · a / ℏ = -a · ∇   ⟹   p̂ = -iℏ∇
```

The eigenvalue equation p̂|k⟩ = k|k⟩ in the position representation reads -iℏ∇⟨x|k⟩ = k⟨x|k⟩, with solution:

```
⟨x|k⟩ = (2πℏ)^(-d/2) · e^(ik·x/ℏ)
```

These are the standard plane-wave eigenfunctions. The standard L² Fourier transform is the unique unitary intertwiner of position and momentum representations on the U2 Hilbert space.

A note on alternatives: fractional-Fourier transforms diagonalize rotated phase-space operators (cos θ · x̂ + sin θ · p̂ for fractional angle θ), not the translation generator p̂. They fail to provide the translation-conjugate basis. Wavelet transforms are multi-scale resolutions, not Stone's-theorem intertwiners of any one-parameter unitary group. Mellin transforms intertwine the dilation group x → e^t x, not the translation group; dilation is not a primitive-level kinematic symmetry of the participation graph (no preferred scale exists). The standard L² Fourier transform is forced by translation symmetry plus Stone's theorem; the alternatives are dismissed by structural inconsistency with the translation-driven conjugacy.

### 3.7 What this delivers

The momentum operator p̂ = -iℏ∇ is now a self-adjoint operator on the U2 Hilbert space, identified by Stone's theorem applied to spatial translation symmetry. Its eigenfunctions are plane waves; its position-momentum conjugate basis change is the standard Fourier transform.

This argument used only primitive-level inputs — graph homogeneity, the spatial axis, U(1) polarity from T14, the U2 inner product — plus Stone's theorem as standard mathematical infrastructure. No time-evolution operator, no Hamiltonian, no Schrödinger equation entered. The momentum operator is the *kinematic* generator on the U2 Hilbert space, identified at fixed time.

---

## 4. Forcing the Time-Evolution Generator

The second dynamical step parallels the first, but on the time axis instead of the spatial axes. The argument again runs through Stone's theorem.

### 4.1 Time-translation symmetry

Relational timing supplies a continuous time axis R_t at the structural level. Graph homogeneity extends to the time axis: the participation graph's structure at time s is structurally identical to its structure at time s - t, up to relabeling. No primitive-level structure singles out a privileged time origin or magnitude.

Time-translation symmetry is therefore a kinematic property of the participation graph, the temporal counterpart of the spatial translation symmetry that gave us p̂.

Define the time-translation operator U_t acting componentwise:

```
(U_t P)_K(x, s) := P_K(x, s - t)
```

for t ∈ R.

### 4.2 Unitarity, group structure, continuity

The argument is structurally identical to the spatial case.

Linearity: U_t(αP + βQ)_K(x, s) = α(U_t P)_K(x, s) + β(U_t Q)_K(x, s).

Unitarity:

```
⟨U_t P | U_t Q⟩ = Σ_K ∫∫ P*_K(x, s-t) Q_K(x, s-t) ds dμ(x)
                = ⟨P | Q⟩
```

(substituting s' = s - t, with ds' = ds because the U2 measure is translation-invariant on the time axis — relational timing supplies translation-invariant relational time with no t-dependent weighting).

Group structure: U_t U_s = U_(t+s), U_0 = I, U_(-t) = U_t^(-1). The time-translation group is abelian and isomorphic to (R, +).

Strong continuity: t ↦ U_t P is strongly continuous because L²-translation is strongly continuous, inherited by the direct-integral structure of the U2 Hilbert space.

### 4.3 Stone's theorem, again

Stone's theorem applied to {U_t : t ∈ R}: there exists a unique self-adjoint operator Ĥ on H such that:

```
U_t = exp(-i Ĥ t / ℏ)
```

The sign convention (negative exponent) is the standard physics convention; mathematically, Stone's theorem is symmetric under sign choice. The generator is unique. Self-adjointness is automatic.

### 4.4 Linearity and first-order time structure are automatic

Differentiating the operator-exponential at t = 0:

```
d/dt|_{t=0} U_t P = -(i/ℏ) Ĥ P
```

For the time-evolved state P(t) := U_t P_0:

```
iℏ ∂_t P(t) = Ĥ P(t)
```

The induced equation is linear in P(t) because: H is a complex vector space; Ĥ is a self-adjoint (hence linear) operator; {U_t} acts linearly on H; time translations form an additive abelian group with U_(t+s) = U_t U_s inheriting linearity. Linearity is not a separately imposed feature — it's a consequence of the unitary representation structure.

The equation is first-order in ∂_t for the same reason. Differentiating U_t = exp(-iĤt/ℏ) once produces the first-order equation. Higher derivatives produce powers of Ĥ:

```
iℏ ∂_t^n P(t) = Ĥ^n P(t)
```

which are downstream consequences of the first-order equation, not independent equations.

A second-order-in-time equation (Klein-Gordon-like) would arise if the symmetry being exponentiated were the Lorentzian boost group, where time and space are mixed. In the non-relativistic regime, time is absolute, the symmetry is the abelian R_t group, and the operator-exponential structure produces a first-order equation. The first-order character is forced by the choice of regime (non-relativistic) plus the structure of the abelian time-translation group.

Gross-Pitaevskii-like nonlinear equations are phenomenological — they arise from coarse-graining many-body systems, not from the substrate-level structure of single-particle dynamics. They do not enter at this level.

### 4.5 What this delivers

The time-evolution generator Ĥ is now a self-adjoint operator on the U2 Hilbert space, identified by Stone's theorem applied to time-translation symmetry. The induced evolution equation:

```
iℏ ∂_t P(t) = Ĥ P(t)
```

is linear and first-order in time, automatically. What's still missing is the *form* of Ĥ — whether it has the kinetic-plus-potential structure |p̂|²/(2m) + V(x̂) of standard QM. That's the next step.

---

## 5. Closing the Form: Galilean Lie Algebra

Stone's theorem gives the existence and uniqueness of Ĥ but says nothing about its functional form. To pin down the |p̂|²/(2m) + V(x̂) structure, we need an additional input — the Galilean Lie algebra of non-relativistic kinematics.

This is the load-bearing step. The argument runs through the commutator structure of Galilean transformations on the U2 Hilbert space, integration of a specific commutator condition, and a chain-rule Jacobian that produces the factor of 1/2 in 1/(2m).

### 5.1 Why Galilean

The Galilean Lie algebra is generated by spatial translations p̂_i, time translations Ĥ, spatial rotations Ĵ_i, and Galilean boosts K̂_i (with x̂_i and m as additional structural ingredients). The substantive commutators are:

```
[x̂_i, p̂_j] = iℏ δ_ij                  (canonical commutation)
[K̂_i, p̂_j] = iℏ m δ_ij                 (boost-translation, central extension)
[Ĥ, K̂_i] = -iℏ p̂_i                    (the load-bearing commutator)
```

The mass m enters [K̂_i, p̂_j] as the Galilean group's central-extension structure constant (Bargmann 1954). The boost generator takes the form:

```
K̂_i = m x̂_i - t p̂_i
```

forced by the requirement that K̂_i generate the standard Galilean boost p̂ → p̂ - mv.

A natural question: why Galilean and not Lorentzian? Boost-translation algebras compatible with absolute time fall into two categories. The Galilean group has absolute time and mass as the central charge of its boost-translation commutator. The Lorentzian group has time and space mixed by boosts; observers in different inertial frames see different time intervals; mass relates to energy and momentum through the relativistic dispersion. In the non-relativistic regime — defined by |p̂|²/(mc)² ≪ 1 and absolute time — the Galilean group is the unique consistent boost-translation algebra. The Lorentzian alternative is ruled out by absolute time, which is a feature of the regime, not an additional commitment.

This is a regime choice. The walkthrough is non-relativistic by scope; the relativistic generalization belongs to a different arc and produces different structural content (Klein-Gordon and Dirac equations rather than Schrödinger).

### 5.2 The Galilean group acts unitarily on H

All Galilean transformations act unitarily on the U2 Hilbert space:

Spatial translations T_a = exp(i p̂ · a / ℏ): unitary by Section 3 (Stone applied to spatial translation).

Time translations U_t = exp(-i Ĥ t / ℏ): unitary by Section 4 (Stone applied to time translation).

Spatial rotations: unitary by primitive-level rotation invariance of the participation graph (graph isotropy from homogeneity plus the spatial axis structure with no preferred direction).

Galilean boosts B_v = exp(i K̂ · v / ℏ): unitary as the exponential of a self-adjoint operator. K̂ = mx̂ - tp̂ is self-adjoint because x̂ and p̂ are both self-adjoint on H (multiplication by a real coordinate, and the Stone generator from Section 3 respectively), and a real-coefficient linear combination of self-adjoint operators is self-adjoint.

The U2 Hilbert space carries a unitary representation of the Galilean group.

### 5.3 The role of Ĥ in the Galilean representation

The time-translation generator Ĥ identified in Section 4 is, by uniqueness, the self-adjoint operator that generates time translations on H. The Galilean group also has a time-translation generator — which must be the same operator, because Stone's theorem produces a unique generator and there's only one time-translation symmetry on H.

Therefore Ĥ plays the role of the time-translation generator within the Galilean representation. In particular, it must satisfy the Galilean commutator:

```
[Ĥ, K̂_i] = -iℏ p̂_i
```

This is an algebraic constraint inherited from the Galilean group's structure. It is *not* an assumption imported from elsewhere — it's forced by the fact that Ĥ is the time-translation generator within a unitary representation of the Galilean group.

### 5.4 The kinetic-plus-potential decomposition

Before integrating the commutator, a structural fact about Ĥ's form is needed: the decomposition Ĥ = T(p̂) + V(x̂) into a part depending only on p̂ and a part depending only on x̂.

This follows from primitive-level translation invariance plus locality.

In the absence of an external potential, the free Hamiltonian commutes with translations: [Ĥ_free, T_a] = 0. This is structural — the participation graph itself is translation-invariant (graph homogeneity), and without external coupling, Ĥ_free inherits this invariance. Any operator commuting with the translation generator p̂ depends on p̂ alone via standard functional calculus on self-adjoint operators (a function of x̂ would generically not commute with p̂ since [x̂, p̂] = iℏ). Therefore Ĥ_free = T(p̂) for some function T.

Locality is a primitive-level structural property of the participation graph: edges connect adjacent vertices, and external influences couple to the participation measure at specific locations. In operator language, the local action of a potential on the wavefunction takes the form (Vψ)(x) = V(x)ψ(x) — multiplication by a position-dependent function. This is the form V(x̂), depending only on x̂. A potential depending on p̂ would be non-local in position representation (a momentum-space multiplication corresponds to a convolution in position space) and is structurally distinct from local external potentials.

Cross terms (products of p̂ and x̂) would violate either translation invariance (if part of the free Hamiltonian — the x̂ factor breaks translation symmetry) or locality (if part of the potential — the p̂ factor introduces non-locality). They are forbidden in the gauge-coupling-free scope.

A scope caveat: in the presence of magnetic vector potentials A(x̂), the kinetic operator becomes T(p̂ - eA(x̂)/c), coupling position and momentum via the gauge field. The clean kinetic-plus-potential decomposition holds in the absence of such gauge couplings. Gauge field theory is downstream content.

The decomposition Ĥ = T(p̂) + V(x̂) is forced. What remains is the form of T.

### 5.5 The four constraints on T

After the kinetic-plus-potential decomposition, the kinetic operator T(p̂) is a function of p̂ alone. Four structural constraints fix its form:

**Translation invariance** is already established — T depends on p̂ and not on x̂.

**Rotation invariance.** The participation graph supports rotations as a kinematic symmetry (graph isotropy from homogeneity plus the spatial-axis structure with no preferred direction). T(p̂) must commute with rotations of p̂. The unique rotational invariant of a vector operator p̂ (up to powers) is the squared magnitude |p̂|² = p̂ · p̂. Therefore T(p̂) = f(|p̂|²) for some function f.

This dismisses anisotropic alternatives. Any anisotropic candidate — a Hamiltonian like c_x p̂_x² + c_y p̂_y² + c_z p̂_z² with c_x ≠ c_y ≠ c_z, or T = (p̂ · n̂)² for a fixed direction n̂ — fails rotation invariance by selecting a preferred direction in space. The participation graph has no such direction; rotation invariance forbids these forms.

**Analyticity at low momentum.** f is analytic in |p̂|² at p̂ = 0, admitting a Taylor expansion:

```
f(|p̂|²) = a_0 + a_1 |p̂|² + a_2 (|p̂|²)² + a_3 (|p̂|²)³ + ...
```

The constant term a_0 is an additive zero-point energy; convention sets a_0 = 0.

This dismisses half-integer powers. A candidate term proportional to |p̂| (i.e., to (|p̂|²)^(1/2)) is not analytic in |p̂|² at the origin — the square-root function has a branch point. Such a term is excluded by analyticity. Physically, T = c|p̂| is the photon-like dispersion of a massless particle — relativistic massless behavior, incompatible with the non-relativistic massive-particle scope. A vector linear term α · p̂ is also excluded by rotation invariance unless α = 0.

**Non-relativistic limit.** In the regime |p̂|²/(mc)² ≪ 1, the relative size of the a_n (|p̂|²)^n term to the a_1 |p̂|² term scales as (v/c)^(2(n-1)) under the natural dimensional scaling a_n ~ a_1 / (mc)^(2(n-1)). Higher-order terms are suppressed by powers of (v/c)². In the strict non-relativistic limit (c → ∞ with v fixed), all a_n for n ≥ 2 vanish. Only the leading a_1 |p̂|² term survives.

This dismisses higher-even-power terms (|p̂|⁴, |p̂|⁶, etc.) in the non-relativistic regime. It also handles the full relativistic dispersion: T_rel = √(|p̂|²c² + m²c⁴) - mc² Taylor-expands as |p̂|²/(2m) - |p̂|⁴/(8m³c²) + ... In the strict non-relativistic limit, only the leading |p̂|²/(2m) term survives. The relativistic dispersion reduces to the same form in the non-relativistic limit, consistent with the regime.

Combined: T(p̂) = a_1 |p̂|² uniquely. The remaining question is the value of a_1.

### 5.6 The Galilean integration: factor of 1/2 from a chain-rule Jacobian

Dimensional analysis fixes a_1 ∝ 1/m with ℏ² supplying the dimensional bridge:

```
a_1 = c_1 · ℏ² / m
```

with c_1 a dimensionless constant. The standard Schrödinger form has a_1 = ℏ²/(2m), corresponding to c_1 = 1/2. The factor of 1/2 is the load-bearing question — dimensional analysis alone does not fix it.

In standard quantum mechanics, the factor of 1/2 is borrowed from the classical kinetic-energy formula T = p²/(2m). The framework derives it instead, from the Galilean commutator [Ĥ, K̂_i] = -iℏp̂_i.

Substituting K̂_i = mx̂_i - tp̂_i and using [Ĥ, p̂_i] = 0 (since Ĥ depends on p̂ alone in its kinetic part):

```
[Ĥ, K̂_i] = m[Ĥ, x̂_i] - t[Ĥ, p̂_i]
         = m[Ĥ, x̂_i]
```

Setting this equal to -iℏp̂_i:

```
m[Ĥ, x̂_i] = -iℏ p̂_i
```

Using the canonical commutation [x̂_i, p̂_j] = iℏδ_ij and the chain-rule identity [T(p̂), x̂_i] = -iℏ(∂T/∂p̂_i):

```
m · (-iℏ)(∂T/∂p̂_i) = -iℏ p̂_i

⟹ ∂T/∂p̂_i = p̂_i / m
```

This is the differential equation that Galilean invariance imposes on T. Using T = f(|p̂|²), so ∂T/∂p̂_i = 2 p̂_i f'(|p̂|²) by the chain rule:

```
2 p̂_i f'(|p̂|²) = p̂_i / m

⟹ f'(|p̂|²) = 1/(2m)
```

Integrating with f(0) = 0:

```
f(|p̂|²) = |p̂|² / (2m)
```

Restoring ℏ:

```
T(p̂) = ℏ² |p̂|² / (2m)
```

The factor of 1/2 emerges from the chain-rule Jacobian of differentiating f(|p̂|²) with respect to p̂_i. The factor of 2 in the chain rule — ∂(|p̂|²)/∂p̂_i = 2p̂_i — is what generates the 1/2 in the integrated form.

This is the methodologically distinctive content of the framework's Schrödinger derivation. The factor of 1/2 in 1/(2m) has appeared in classical mechanics for centuries; it has been borrowed into quantum mechanics via the operator-substitution p → p̂ without further justification. The framework establishes that the factor is forced by integrating the Galilean commutator condition — that the same Galilean invariance that produces T = p²/(2m) classically produces T = |p̂|²/(2m) in the operator-valued quantum case, by the same integration argument applied to the same algebra. The factor of 1/2 is not a feature of classical mechanics that quantum mechanics happens to inherit; it is a feature of Galilean kinematics that both classical and quantum mechanics inherit.

### 5.7 Form forced, values inherited

Combining the kinetic and potential parts:

```
Ĥ = ℏ² |p̂|² / (2m) + V(x̂)
```

The form is forced. The values are not all derived:

The mass m is inherited per the framework's "form forced, values inherited" methodology — the framework forces the structural form of mass-dependence but inherits all numerical mass values, ratios, and hierarchies from external context (a separate program arc addresses chain-mass structure).

The constant ℏ is inherited via the dimensional-atlas Madelung anchoring. Its numerical value is not derived from primitives; it's the structural constant that emerges via the Madelung-form correspondence between participation-measure evolution and standard quantum mechanics.

The potential V(x̂) is a scalar function of position whose specific form for any given physical system is inherited from external context (the source of the potential is whatever physical situation the system is in — a Coulomb field, a harmonic trap, a crystal lattice). The framework forces that V depend on x̂ alone; it does not derive what V is for any particular system.

This is honest framing. The framework does not claim to derive every numerical constant from primitives; it claims to derive the structural form within which those constants appear.

---

## 6. Closure: The Schrödinger Equation

The pieces now assemble. From Section 4, the time-evolution generator Ĥ is unique, self-adjoint, and produces a linear first-order evolution equation. From Section 5, Ĥ has the kinetic-plus-potential form with the specific factor of 1/(2m) forced by Galilean integration. Combining:

```
iℏ ∂_t P(t) = Ĥ P(t),   Ĥ = ℏ² |p̂|² / (2m) + V(x̂)
```

This is the Schrödinger equation in standard non-relativistic single-particle form.

Every piece traces to a structural commitment:

The Hilbert space comes from U2 (sesquilinear inner product on the participation-measure space).

The momentum operator p̂ = -iℏ∇ comes from Stone's theorem applied to spatial translation symmetry on H (Section 3).

The time-evolution generator Ĥ as a unique self-adjoint operator comes from Stone's theorem applied to time translation symmetry on H (Section 4).

Linearity and first-order time structure come automatically from the operator-exponential form U_t = exp(-iĤt/ℏ).

The kinetic-plus-potential decomposition comes from translation invariance plus locality.

The quadratic |p̂|² form comes from rotation invariance, analyticity, and the non-relativistic regime.

The factor of 1/(2m) comes from integrating the Galilean commutator [Ĥ, K̂_i] = -iℏp̂_i with K̂_i = mx̂_i - tp̂_i, with the factor of 1/2 emerging as the chain-rule Jacobian.

m and ℏ are inherited values; V(x̂) is inherited from external context.

The structural payoff: the Schrödinger equation is what falls out when the same theorem (Stone) is applied to the same Hilbert space (the U2 inner-product structure on the participation-measure space) on two different symmetries (spatial and temporal translation), with the resulting time-translation generator identified — via Galilean Lie algebra closure — with the kinetic-plus-potential operator forced by translation invariance, rotation invariance, and the regime.

---

## 7. The Architecture of the Derivation

Stepping back, the structural shape of this derivation is worth naming.

The Born walkthrough had a single philosophical hinge: the Cauchy functional equation in T14, which forces the squared-amplitude exponent before any quantum-mechanical structure has entered. From that one structural fact, everything else followed — the participation measure form, the inner product, the Gleason-Busch closure, the squared exponent in |⟨K|ψ⟩|².

The Schrödinger walkthrough has a different shape. There's no single hinge. Instead, the derivation has an architectural symmetry: Stone's theorem applied twice on the same Hilbert space, once on each axis of translation, plus a Galilean closure that binds them together.

The kinematic generator p̂ comes from Stone on space. The dynamical generator Ĥ comes from Stone on time. Both are forced uniquely from the same primitive-level inputs (translation symmetry, U2 unitarity, strong continuity) — the only difference is which axis the symmetry acts on. The mathematics of Stone's theorem is indifferent to whether the parameter is spatial or temporal; it produces a unique self-adjoint generator for any strongly continuous one-parameter unitary group.

What distinguishes the two generators is what happens *after* Stone identifies them. The momentum operator p̂ is a kinematic object — it lives at fixed time, governs translation symmetry, has plane-wave eigenfunctions, supports the position-momentum Fourier conjugacy. The Hamiltonian Ĥ is a dynamical object — it lives across time, governs evolution, and (this is the load-bearing step) identifies with the kinetic-plus-potential operator via Galilean Lie algebra closure.

The Galilean algebra is the bridge. Without it, Stone gives you a self-adjoint time-translation generator with no specified form. With it, the time-translation generator is constrained to satisfy [Ĥ, K̂] = -iℏp̂, which integrates against K̂ = mx̂ - tp̂ to give Ĥ = |p̂|²/(2m) + V(x̂). The Galilean structure is what turns the abstract dynamical generator into the specific Hamiltonian form.

This architectural shape — Stone twice plus Galilean closure — is what unifies the kinematic and dynamical content of non-relativistic single-particle quantum mechanics under a single derivation framework. The same theorem on both axes; the algebra that binds them. The Schrödinger equation, on this view, is what that architecture produces.

---

## 8. What This Argument Establishes

The chain runs:

Primitives (micro-events, participation, channels, bandwidth, polarity, ED gradient, relational timing) → T14 (participation measure form forced) → U2 (inner product forced) → Stone on spatial translation (momentum operator p̂ = -iℏ∇ forced) → Stone on time translation (Ĥ existence + uniqueness + linearity + first-order forced) → Galilean closure (kinetic-plus-potential form + factor of 1/(2m) forced) → Schrödinger equation iℏ ∂_t P = Ĥ P with Ĥ = ℏ²|p̂|²/(2m) + V(x̂).

Each step has its load-bearing arguments worked out rather than deferred. The factor of 1/(2m) is derived rather than borrowed from classical mechanics. The first-order time structure is a consequence of operator exponentials rather than an empirical choice. The kinetic-plus-potential decomposition is a consequence of translation invariance plus locality rather than an assumption.

The framework reproduces standard non-relativistic single-particle quantum mechanics exactly. It does not predict any new laboratory result that differs from standard QM in the regimes where standard QM has been tested. What it does is replace a list of independent postulates — Hilbert-space structure, momentum operator, Schrödinger equation, kinetic-energy form, mass dependence — with a smaller list of structural commitments about participation, bandwidth, channels, polarity, and timing. The QM postulates emerge as theorems rather than being assumed independently.

Combined with the Born walkthrough, all four foundational postulates of non-relativistic single-particle quantum mechanics are now derived from the substrate ontology:

The Born rule (probability equals squared amplitude) follows from T14's Cauchy step, U2's inner product, and the channel-as-primitive ontology forcing non-contextuality, with Gleason-Busch as the closure step.

The Bell-Tsirelson bound (the maximum quantum correlation between entangled systems) follows from Cauchy-Schwarz and operator-norm bounds on the bipartite Hilbert space supplied by U2.

The Heisenberg uncertainty inequality (the floor on position-momentum uncertainty product) follows from the L² norm structure of U2 plus the Fourier-conjugate adjacency-band partition supplied by the U5 momentum operator.

The Schrödinger equation (the dynamical evolution rule) follows from Stone's theorem applied to time-translation symmetry plus Galilean Lie algebra closure (Sections 4 and 5).

Quantum mechanics, on this view, is no longer a collection of postulates that happen to fit experiment. It is what the participation-graph ontology produces, all the way down — the kinematic structure, the probabilistic interpretation, the uncertainty structure, and the dynamical evolution.

Whether the substrate commitments themselves are right is a separate question and remains the load-bearing one. The framework stands or falls on whether participation, bandwidth, channels, polarity, and the rest of the primitive stack are the correct foundational concepts. The empirical exposure of the framework lives elsewhere — in the soft-matter mobility law's prediction of sub-Fickian recovery in concentrated BSA, in the substrate-gravity prediction of MOND's transition acceleration, in the kernel-level arrow of time, in the V1 finite-width vacuum kernel structure. These are where reality gets to weigh in.

For non-relativistic single-particle quantum mechanics specifically, the structural case is closed. Every postulate of standard QM emerges from the substrate. The Hilbert space is not assumed, the Born rule is not postulated, the Schrödinger equation is not borrowed. All three follow from the participation-graph ontology with no new commitment introduced anywhere in the derivation.

---

## 9. References

- Proxmire, A. *The Born Rule as a Forced Theorem of Event Density: A Gleason–Busch Reconstruction from First Principles.* April 2026.
- Proxmire, A. *The Inner Product as Forced Structure in Event Density: Discrete Derivation, Continuum Lift, and Gauge-Invariant Completion.* April 2026.
- Proxmire, A. *U5: The Forced Structure of Translation Symmetry and the Momentum Operator.* April 2026.
- Proxmire, A. *U4: The Forced Structure of the Non-Relativistic Hamiltonian.* April 2026.
- Proxmire, A. *U3: The Forced Structure of Time-Translation Symmetry and Schrödinger Evolution.* April 2026.
- Proxmire, A. *Theorem 14: The Participation Measure Form.* (T14 derivation memo.)
- Proxmire, A. *Event Density: One Substrate, Three Domains.* April 2026.
- Proxmire, A. *Event Density Foundations: A Unified Substrate Architecture for Quantum, Fluid, Gauge, and Gravitational Dynamics.* April 2026.
- Stone, M. H. "On one-parameter unitary groups in Hilbert space." *Annals of Mathematics* 33, 643–648 (1932).
- Bargmann, V. "On unitary ray representations of continuous groups." *Annals of Mathematics* 59, 1–46 (1954).
- Reed, M., and Simon, B. *Methods of Modern Mathematical Physics, Volume I: Functional Analysis.* Academic Press, 1980.
- The full Event Density corpus, including all forced theorems and supporting memos, is available at https://github.com/allen-proxmire/event-density.
