# CHPE: A Discrete Adjacency‑Rewriting Framework for Emergent Physics  
**Version 1.1 — 2025‑11‑20**

---

## Executive Summary

CHPE (Crystallized Hyperdimensional Probability Emergence) is a fully discrete framework in which labeled adjacency configurations evolve by local rewriting operators. States live in a countable Hilbert space spanned by admissible configurations; dynamics are encoded by a sparse operator algebra that preserves gauge covariance, spin‑label closure, and locality. A path‑sum over rewriting histories yields amplitudes for configurations and supports the extraction of coarse‑grained observables (effective fields, curvature proxies, entropy). Under explicit correspondence conditions, CHPE reduces to quantum field theory (QFT) and general relativity (GR). This document states axioms, operators, observables, effective equations, correspondence limits, proof obligations, and a computational test plan designed for reproduction and critique by researchers and LLMs.

---

## 1. Core Objects and Axioms

**A1 (Substrate).** A configuration is a labeled hypergraph A = (V, E, L, ≺) with finite local degree. V is a countable vertex set; E is a finite set of hyperedges; L assigns gauge and spin labels to edges (or nodes); ≺ is an optional acyclic partial order used for causal diagnostics.

**A2 (Admissibility).** Ω is the set of configurations with finite local degree, label covariance under local gauge G, and spin‑representation closure under H.

**A3 (State space).** The Hilbert space is a graded direct sum H = ⊕_N H_N, where H_N spans configurations with exactly N hyperedges and has an orthonormal basis |A⟩ for A ∈ Ω_N. (Optional) A Z2‑grading may be endowed to represent fermion parity.

**A4 (Local rewriting).** A finite set of local rewrite types {R_i} acts linearly on H with bounded support: R_i|A⟩ = Σ_{A′} A_i(A, A′) |A′⟩, and nonzero amplitudes only modify A on a finite patch.

**A5 (Symmetry constraints).** For all local gauge transforms U_g and spin actions: (i) gauge covariance U_g R_i U_g^{-1} = R_i; (ii) spin closure: label updates respect the decomposition rules in Rep(H).

**A6 (Evolution modes).** The one‑step operator T = Σ_i R_i acts either (a) in quantum mode as unitary on each H_N or as a block partial isometry mapping H_N → H_{N′} with Σ_{N′} T_{N′,N}† T_{N′,N} = I on H_N; or (b) in stochastic mode as a row‑stochastic kernel. **Mode exclusivity:** use either (a) or (b) per experiment. Quantum noise is modeled by completely‑positive trace‑preserving (CPTP) maps; stochastic noise by explicit kernels.

**A7 (Seedless initiation).** To initiate dynamics from a perfectly symmetric configuration, allow either an infinitesimal stochastic tie‑breaker ε→0+ or a single zero‑measure symmetry‑breaking rewrite per connected component.

---

## 2. Path‑Space and Amplitudes

A rewriting history of length n is P_n: A_0 → A_1 → … → A_n with allowed local steps. The path amplitude is the product of step amplitudes; the kernel K(A_0, A_n) is the sum of amplitudes over histories joining them; the depth‑n partition function is Z_n = Σ_{P_n} amplitude[P_n]. One may define a discrete action so that amplitude = exp(i Σ L(A_{k−1}, A_k)).

**Gauge/isomorphism quotient and schedule independence.** Path sums are taken over equivalence classes of configurations and histories modulo local gauge actions and graph isomorphisms (or, equivalently, by group‑averaging observables). Multiway sums include all local update orderings; kernels must be schedule‑independent up to an overall phase (confluence up to phase).

---

## 3. Observables

An observable is diagonal in the configuration basis: Ô|A⟩ = O(A)|A⟩. Classes include: (i) graph‑theoretic statistics (degrees, components, motifs, cycle spectra); (ii) gauge/spin label histograms; (iii) entropies (global and local patch); (iv) causal/horizon diagnostics (terminal subgraphs, causal depth); (v) spectral dimension via heat‑kernel return probability.

**Class functions.** Physical observables are gauge/isomorphism‑invariant: either work on quotient classes [A] or apply group averaging Ô ↦ ∫_G U_g^† Ô U_g dg.

Expectation values are Σ |ψ_n(A)|^2 O(A) in quantum mode or Σ μ_n(A) O(A) in stochastic mode.

---

## 4. Distinguished Substructures

**Horizon subgraph H.** A maximal set of edges with no causal successors outside H.  
**Inflating patch.** Neighborhoods whose ball growth exceeds a threshold.  
**Particle‑like motif π.** A small labeled subgraph that persists under T, has a finite stabilizer under local G, and conserves a prescribed set of motif observables.

---

## 5. Coarse‑Graining and Effective Equations

Let Φ_χ(v, t) be a coarse density of mass‑like motifs; S(v, t) a local entropy; a(v, t) a local expansion factor. Prototypical discrete effective dynamics:

• Geometry–energy coupling (Einstein‑like): Δ_t a(v, t) = −κ_1 Φ_χ(v, t) + κ_2 S(v, t).  
• Gauge density flow (Yang–Mills‑like): Δ_t Φ_G^a(v, t) = −div Φ_G^a(v, t) + J^a(v, t).  
• Motif number: Δ_t N_{π_k}(t) = −Γ_k N_{π_k}(t).  
• Horizon area: Δ_t A_H(t) = Σ_i (ε_i − η_i) over boundary events.  
• Entropy: Δ_t S(t) ≥ 0 for non‑reversible rewriting.

---

## 6. Correspondence Limits

**QFT limit.** (i) Adjacency statistics approximate a regular lattice with spacing Λ^{-1}→0; (ii) rewrite amplitudes become translation‑invariant; (iii) motif propagators reproduce free‑field correlators; (iv) local gauge covariance of T; (v) fermionic sectors are implemented via a Z2‑graded Hilbert space and satisfy canonical anti‑commutation relations (CAR), enforced by a discrete Ginsparg–Wilson‑type constraint to avoid doubling.

**GR limit.** (i) Large‑scale adjacency approximates a piecewise‑flat Lorentzian manifold; (ii) curvature arises from rewrite asymmetries (angle deficits, volume‑growth anomalies); (iii) causal partial order matches light‑cone structure; (iv) horizon subgraphs yield area–entropy scaling; (v) geodesic motion extremizes a discrete rewrite‑cost functional; (vi) boundary‑local reversible horizon rules factorize microstates to produce the area law.

**Fractal emergence (minimal).** Near a critical balance between growth, pruning, and motif freezing, CHPE supports fractal/multifractal structure: deterministic graph‑grammar fractals, stochastic aggregation/percolation‑like clusters, and computable iterated‑map sets. Verification uses Hausdorff/box and spectral dimensions and multifractal cascades; expect crossover from fractal microstructure to smooth 3+1D geometry off criticality.

### 6.1 Holographic/Bootstrap Rule‑Selection Principles (from Strings/AdS/CFT)

(H1) Crossing/associativity; (H2) reflection positivity; (H3) modular/large‑N hints; (H4) ANEC/QNEC‑style bounds; (H5) chaos/OTOC bound; (H6) entanglement inequalities. These act as **filters on allowed rewrite rules and amplitudes** (see Proof Obligations and Tests).

### 6.2 Spin‑Foam/GFT‑Guided Semiclassical Limit (GR Rigor)

Rewrite histories induce a 2‑complex with face/edge/vertex amplitudes subject to simplicity constraints; large‑spin stationary phase recovers a Regge‑like action and curvature via deficit angles. A GFT‑style RG flow controls the continuum limit.

### 6.3 Minimal Rule Set M0 (Concrete, Falsifiable)

**Substrate.** Bipartite, degree‑3 **causal diamond graph** approximating 1+1D (nodes split into even/odd time layers; edges connect (x,t)→(x±1,t+1)). Fixed adjacency to ensure clean unitarity; optional slow **edge‑jitter** (rare local rewires) to probe robustness.

**Labels.** (i) **Boson field** φ∈ℝ on nodes; (ii) **Fermion** ψ=(ψ_L,ψ_R) with Z2 parity on nodes (staggered by bipartition); (iii) **U(1) gauge links** U_e = e^{iθ_e} on directed edges.

**Local rewrites (unitary step T = T_g T_f T_b):**
- **(B) Boson transport:** on each diamond, swap/average φ along null edges so that φ obeys the discrete wave equation (central‑difference) with mass m via a local phase weight.  
- **(F) Fermion staggered shift:** ψ_L moves right, ψ_R left (chiral shifts), with a Wilson‑like counterterm implemented as a local phase on back‑scattering to satisfy a **discrete GW relation**.  
- **(G) Gauge update:** parallel transport of φ and ψ by U_e; local plaquette phase update U_⊞ ← U_⊞ e^{−i g^2 E_⊞ Δt} with Gauss‑law constraint enforced by a projector.

**Amplitudes.** All three layers are **exactly local and norm‑preserving** on the fixed graph; their product defines T per step. Parameters: (m, g, r) with r the Wilson‑like control.

**Gravity proxy (M0‑GR).** A second switchable phase adds **rare edge contraction/addition** with rate ε≪1 conditioned on local energy density (from φ,ψ,U). This defines a 2D Regge‑like curvature proxy (angle deficits from degree variations) used only for GR tests; ε=0 for pure QFT tests.

**Kill criteria (must pass or M0 is rejected).**
- **K1 (Lorentz/QFT):** free boson/fermion two‑point functions agree with continuum 1+1D predictions to ≤1% over **two decades** in x,t; measured max signal speed frame‑independent within ≤0.5%.
- **K2 (Fermions):** CAR holds numerically; spectral test shows **no doublers**; a background U(1) flux on a spatial circle exhibits correct **index/spectral flow**.  
- **K3 (Gauge):** charge conservation from a lattice Noether current; U(1) photon‑like correlator fits.  
- **K4 (Gravity proxy, when ε>0):** geodesic paths from rewrite‑cost functional reproduce Newtonian potential in weak‑field analogue to ≤5% over a decade; horizon analogs obey an area‑law with boundary‑local reversibility.

**Unique prediction (M0).** **Spectral‑dimension running** at micro‑scales on the causal diamond: d_s(ℓ) ≈ 2 + c (ℓ/ℓ_0)^α for ℓ≲10 lattice units with α≈1 and c set by (m, g, r); this produces a measurable sub‑diffusive return probability relative to a perfect lattice QFT. Failure to observe this in M0 simulations **falsifies** the rewrite composition chosen.

## 7. Rule Families Realizing Limits

**QFT‑aligned rules.** (1) Edge transport (motif propagation). (2) Label exchange (gauge rotation). (3) Fusion/decay (local interactions).  
**GR‑aligned rules.** (4) Edge addition (expansion). (5) Edge contraction (curvature). (6) Causal barrier (horizons).  
**Chiral/anomaly control.** (7) Domain‑wall motifs with anomaly inflow or (8) a discrete BRST‑like symmetry on rewrite generators.  
All rules obey gauge covariance and spin closure.

---

## 8. Minimal Discrete Action (Prototype)

Define a per‑step Lagrangian L(A_{k−1}, A_k) = α ΔC + β ΔK + γ ΔS, where C penalizes label curvature, K penalizes degree spikes, and S rewards local entropy smoothing. Then amplitude[P_n] = exp(i Σ L).

**Composition (cylinder) constraint.** Choose L so that kernels compose: in stochastic mode, Σ_{A_k} K(A_{k−1}, A_k) K(A_k, A_{k+1}) = K(A_{k−1}, A_{k+1}); in quantum mode, the analogous unitary composition holds. Reject actions that fail numerical consistency checks.

---

## 9. Empirical and Computational Program

**General protocols.** Use fixed seeds; periodic spatial boundary; open temporal boundary; measure with jackknife/bootstrap errors; report η‑exponents and χ²/d.o.f.

**P1 (Spectral‑dimension flow).** d_eff(scale) via heat‑kernel return; **Target:** d_eff→2 for ℓ≲10 (M0 prediction), d_eff→2 exactly in continuum 1+1; tolerance ±0.05.

**P2 (Lorentz recovery).** Free‑field two‑point fits under boosts induced by automorphisms; **Target:** dispersion E^2=k^2+m^2 within ≤1% over two decades; max speed stable within 0.5%.

**P3 (Area–entropy law, ε>0).** Linear scaling S≈(log κ)·|∂H| with κ determined by allowed boundary rewrites; **Target:** R²>0.98 in linear fit over sizes 8–64.

**P4 (Gauge sector).** Continuity equation ∂_t ρ + div J = 0 (discrete); **Target:** L²‑residual ≤1e−3 per step; U(1) plaquette correlator matches lattice‑QED free photon form within 2%.

**P5 (Fermions).** Verify CAR numerically; **GW test:** ||D γ5 + γ5 D − a D γ5 D||_op ≤ 1e−3; **No‑doublers:** spectral density shows single Dirac cone.

**P6 (Index test).** Adiabatically insert 2π flux; **Target:** eigenvalue spectral flow crosses zero the correct number of times (index=1) on a length‑L ring.

**P7 (Schedule independence).** Randomize local update orderings; **Target:** correlators invariant within Monte‑Carlo error; kernel phases differ by a global phase only.

**P8 (Block unitarity / stochastic normalization).** Verify Σ_{N′} T_{N′,N}† T_{N′,N} = I (ε=0) or row sums =1 (Markov mode); **Target:** operator norm deviation ≤1e−12 (double precision).

**P9 (Gravity proxy).** Geodesic‑deviation measured from rewrite‑cost; **Target:** Newtonian‑like 1/r potential fit with ≤5% error; curvature via degree deficits correlates (>0.9) with geodesic deviation.

**P10 (Prediction check).** Micro‑scale d_s(ℓ) curve: **Target:** slope α≈1±0.2 and intercept shift c within fitted band; disagreement ⇒ M0 falsified.

## 10. Comparison to Discrete Approaches Comparison to Discrete Approaches

**Wolfram Physics Project (WPP).** Minimal unlabeled hypergraph rewriting; lacks native amplitudes/labels. CHPE adds Hilbert structure, amplitudes, and explicit observables; WPP contributes structural parsimony.  
**Loop Quantum Gravity / Spin foams.** Compatible with spin‑labeled geometry; CHPE generalizes to gauge‑labeled motifs and explicit rewrite dynamics.  
**Causal Set Theory / Causal Dynamical Triangulations.** Shares causal partial order; CHPE uses it as a constraint within a richer labeled substrate.  
**Group Field Theory.** CHPE path‑sum parallels GFT diagrammatics but keeps primitive local rewrites.  
**Asymptotic Safety.** Realized as discrete RG on block‑adjacency; check fixed‑point behavior numerically.

---

## 11. Proof Obligations

O1 (Unitarity or Markov soundness): exhibit parameter regimes with T†T = I or proper normalization.  
O2 (Gauge invariance): prove U_g T U_g^{-1} = T.  
O3 (Anomaly control): demonstrate domain‑wall/BRST constraints prevent mirror doubling while keeping chiral sectors.  
O4 (Lorentz emergence): prove coarse correlators are invariant under a recovered Lorentz action in the continuum limit.  
O5 (EFT limit): derive local effective actions for coarse fields from rewrite statistics.  
O6 (Schedule independence): show confluence up to phase under all local update orderings.  
O7 (Block‑unitarity/partial isometry): establish Σ_{N′} T_{N′,N}† T_{N′,N} = I on each sector H_N.  
O8 (Fermionic CAR/GW): construct graded sectors satisfying CAR and a discrete Ginsparg–Wilson‑type relation.  
O9 (Area‑law factorization): prove boundary‑local reversible rules imply entropy proportional to boundary size.  
**O10 (Crossing/positivity):** show four‑point crossing and reflection positivity hold for boundary correlators derived from rewrite statistics.  
**O11 (Holographic causality):** prove ANEC/QNEC‑style inequalities and a discrete chaos bound are satisfied.  
**O12 (Entanglement structure):** prove strong subadditivity, monogamy, and wedge nesting for minimal‑cut entropies.  
**O13 (Spin‑foam asymptotics):** demonstrate large‑spin stationary‑phase of CHPE‑induced amplitudes reproduces a Regge‑like action and curvature via deficit angles.  
**O14 (GFT renormalization):** define and analyze a GFT‑style RG flow for induced amplitudes with fixed points consistent with GR/QFT limits.

---

## 12. Open Problems and Milestones

M1: Construct a minimal closed rewrite set achieving QFT+GR correspondence.  
M2: Formal discrete action with gauge‑fixing and a BRST‑like symmetry.  
M3: Black‑hole information transfer microdynamics under reversible rules.  
M4: Parameter scan for UV fixed points (discrete RG).  
M5: Publish an open benchmark suite and baselines.

---

## 13. Notation and Conventions (Abbrev.)

G: local gauge group; H: Lorentz‑like group; Rep(·): representation category; γ_r(v): radius‑r neighborhood; Φ: coarse density; S: entropy; a: local expansion factor; Δ_t: one‑step difference; div: graph divergence.

---

## 14. Reference Implementation Sketch (Pseudocode)

```
state := initial_config()
for step in 1..N:
  patches := sample_local_patches(state)
  proposals := []
  for p in patches:
    for rule in rules:
      if applicable(rule, p):
        proposals.append(apply(rule, state, p))
  weights := amplitude(proposals)  # via exp(i * L)
  state := select(proposals, weights)  # unitary or stochastic mode
  measure_observables(state)
```

---

## Appendix A: Minimal Axiom Set (Restated)

A1–A7 as in Section 1.

## Appendix B: Example Rewrite Templates

(QFT) transport / label‑exchange / fusion‑decay; (GR) addition / contraction / barrier; (chiral) domain‑wall or BRST‑like. Include gauges: local transforms leave T invariant.

**Appendix B1 — M0 Rule Tables (Exact).**

**Substrate:** causal diamond graph with nodes (x,t) ∈ ℤ×ℤ, bipartite by t parity; edges between (x,t) and (x±1,t+1).

**BOSON (B):** on each diamond D={(x,t),(x+1,t+1),(x−1,t+1),(x,t+2)}
- φ(x,t+2) ← φ(x+1,t+1)+φ(x−1,t+1)−(1−m^2Δt^2)φ(x,t)
- Implemented as two local rewrites (update then commit) to preserve unitarity in the composite step.

**FERMION (F):** staggered update on bipartition:
- ψ_L(x+1,t+1) ← U_{(x,t)→(x+1,t+1)} ψ_L(x,t)
- ψ_R(x−1,t+1) ← U_{(x,t)→(x−1,t+1)} ψ_R(x,t)
- Add local counterterm phase e^{i r Δ} on back‑scattering edges to satisfy a GW‑type relation.

**GAUGE (G):**
- Parallel transport: whenever a label crosses edge e, multiply by U_e.
- Plaquette: U_⊞ ← U_⊞ e^{−i g^2 E_⊞ Δt}, with Gauss projector enforcing local constraint.

(ε‑gravity proxy): with prob ε, replace a local 2‑diamond patch by a contracted version (edge contraction) conditioned on local energy density; inverse move allowed with detailed balance so boundary microstate counting is local and reversible.

## Appendix C: Suggested Test Suite: Suggested Test Suite

T1 spectral dimension scaling; T2 Lorentz invariance of two‑point functions; T3 horizon area law; T4 gauge charge conservation; T5 EFT fit to lattice propagators; T6 anomaly probes under chiral rewrites; T7 fractal benchmarks; T8 update‑order (schedule) invariance; T9 fermionic CAR and GW checks; T10 boundary reversibility & area‑law factorization; T11 block unitarity / stochastic normalization; T12 gauge/isomorphism‑averaging invariance of observables; **T13 crossing symmetry & reflection positivity** (boundary four‑point and two‑point tests); **T14 chaos bound/OTOC growth** (discrete Lyapunov extraction); **T15 entanglement wedge nesting & monogamy** (minimal‑cut diagnostics); **T16 spin‑foam stationary‑phase/Regge angle recovery**; **T17 GFT‑style RG flow** (fixed‑point structure).

---

## Changelog

**2025‑11‑21 v1.3** — Added **Minimal Rule Set M0** with exact substrate, labels, local rewrites, amplitudes, gravity proxy switch, hard **kill criteria**, and a **unique micro‑scale spectral‑dimension prediction**. Tightened empirical program with numerical **targets/tolerances** and detailed **index/GW** tests. Expanded appendices with **M0 rule tables**.

**2025‑11‑20 v1.2** — Holographic/Bootstrap constraints for rule selection; Spin‑foam/GFT‑guided semiclassical limit; new proof obligations O10–O14 and tests T13–T17.

**2025‑11‑20 v1.1** — Consistency patches integrated: sectorized Hilbert space, gauge/isomorphism quotient, schedule independence, graded fermions with GW constraint, composition constraint, horizon microstate factorization, expanded tests and obligations.

**2025‑11‑08 v1.0** — Initial share‑ready version.

