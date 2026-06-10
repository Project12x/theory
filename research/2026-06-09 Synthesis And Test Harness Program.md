---
type: research-notes
status: active
provenance: ai-synthesized (Claude / Fable 5), from full-wiki review and working session with Eric Steenwerth
claim_confidence: mixed (per-section labels below)
created: 2026-06-09
updated: 2026-06-09
---

# Research Notes 2026-06-09: Tensions, Emergent Connections, Assessment, and Test Harness Program

This document is the durable record of the 2026-06-09 working session: a full read of the compiled wiki, a tension audit, a set of emergent-connection candidates derived from existing core claims, an external assessment of the work, Eric's ethics clarification, and a program of testable criteria designed to be built as software harnesses by coding agents.

Provenance labels used throughout:

- **[ERIC]** — stated directly by Eric this session. Core.
- **[SYNTH]** — AI synthesis derived from conjunctions of existing core wiki pages. Suspect until Eric adopts, refines, or rejects.
- **[ASSESS]** — AI external assessment/opinion. Not wiki doctrine; recorded for orientation.

---

## 1. Session Context

Full review of `wiki/` (46 claims, 27 concepts, 7 questions, 5 threads, 6 domains, 5 examples, 3 source pages, index, log) plus the three source texts.

State observations:

- The freshest layer is the 2026-06-03 egregore session: [[Egregore]] created; [[Symbolic Entity]] and [[Gods Are Functional Symbolic Entities]] updated. That session had not updated `index.md` or `log.md` (fixed tonight).
- Pages still carrying unsettled status by Eric's own labels: [[Physics Laws Are Emergent Descriptions]] (`suspect` — see T7), [[Relational Update Rate]] and [[Quantization Noise Floor]] (`contested`), [[Form Is Information]] (held open as under-articulated), CHPE items in [[AI-Injected Claim Review Queue]].
- Hygiene: `chpe_thesis_v_1.md` title block says v1.1 while its changelog runs to v1.3.

---

## 2. Tension Register [SYNTH]

Places where core pages pull against each other or against their own revision conditions. Per AGENTS.md, tensions are documented, not silently resolved.

### T1 — The formalization contradicts the ontology's deepest claim

The philosophy holds the substrate is analog and discreteness emerges from finite processing, and argues frameworks starting from fundamental discreteness "cannot reach the foundation" (the criticism aimed at Wolfram). CHPE is fully discrete by construction (A1: labeled hypergraph, countable Hilbert space). By the framework's own argument, its own formal branch cannot model the analog→discrete transition — the actual novel claim. Resolutions: re-scope CHPE as a model of the already-rendered lattice, or weaken the analog-first thesis. Related: [[CHPE Is A Formalization Branch]], [[Analog Substrate]].

### T2 — The preferred-frame problem

"`c` is the universal update rate" plus "time is the causal tick" naturally implies a privileged simultaneity. Special relativity observably forbids that, and [[C Is Relational Update Rate]] lists failure to reproduce SR as its own revision condition. The source's time-dilation story is one-directional and cannot yet produce SR's symmetric dilation. CHPE's schedule-independence machinery (O6, P7) is the right seed for an answer (confluence/causal-invariance is how update ontologies recover frame-independence). Highest-consequence physics tension. See harness H5.

### T3 — Two entropies wearing one word

The substrate is "maximum entropy" (all possibility); the second law is the one-way accumulation of actualized relation; black holes increase entropy by un-collapsing (possibility re-opening). Entropy rises via collapse and via un-collapse — incoherent in one ledger, clean in two: possibility-space entropy vs rendered thermodynamic entropy. Needs an explicit two-ledger statement. Related: [[The Second Law Is The One-Way Character Of Collapse]], [[Black Holes Are Over-Constrained Potential States]].

### T4 — Timeless nucleation still talks in time

[[There Was No Temporal Before The First Relation]] is core, yet the CSP source describes fluctuations that "constantly arise and dissolve" until one goes critical — process language smuggling duration back in. The rigorous fix is modal, not temporal: among all possible configurations, supercritical ones are self-actualizing; our existence is selection, not waiting. Same selector-free logic as the bubble self-selection passage.

### T5 — Dark matter's location problem

"Frontier actualization" lives at the horizon, but dark-matter phenomenology is local: halos, the Bullet Cluster lensing/gas separation, CMB acoustic structure. The refined claim (higher-dimensional relation measured in 3D) can be local but then decouples from the frontier, weakening the "two faces of one process" unification. Needs a story for why higher-dimensional relation clusters where galaxies are. Note: the Bullet Cluster is friendly to relation-like, collisionless dark matter — a development opportunity, not only an objection.

### T6 — One operation, or one schema? (the load-bearing joint)

[[Collapse Constraint And Relation Are One Operation]] claims literal identity across levels; the [[Collapse Across Scales]] thread's own open question asks how levels differ mechanically without demoting the claim to analogy. Missing: a substrate-neutral definition of a constraint event (candidate: possibility-measure reduction via relation-formation, irreversible, energy-coupled) plus per-level instantiation showing what plays the roles of possibility measure, relation, and irreversibility at each level. Everything hangs off this joint. Harness H1 bears on it empirically.

### T7 — Status inversion

[[Physics Laws Are Emergent Descriptions]] remains `suspect` while a dozen core claims downstream presuppose it. Either promote to core or state which part of its phrasing is the overstatement.

### Hygiene items

- `index.md`/`log.md` staleness from the June 3 session (fixed 2026-06-09).
- CHPE version header mismatch (v1.1 header vs v1.3 changelog).

---

## 3. Emergent Connection Candidates [SYNTH]

Derived strictly from conjunctions of existing core pages; none previously stated in the wiki. Candidates for promotion to wiki pages after Eric's review.

### C1 — The universal phase diagram

From the resolution curve + the cosmic attractors: every constraint-system should exhibit four phases — **unconstrained noise → growing frontier → stable lattice → over-constraint inversion**. The cosmos names all four; music names three (white noise → music → tone-pile back to noise). Extensions the wiki has not written: the **self** (psychosis/infancy → growth → locked identity → the psychological black hole: trauma loops and obsession as attentional event horizons capturing all incoming relation; ego death and obsession converge as the extremes meet); the **institution** (movement → growth → orthodoxy → sclerosis), where the binding/maintenance split explains why sclerotic institutions are simultaneously fragile (metastable) and expensive to dismantle (deep binding). Generates a typology: every entity-type has a nameable frontier, lattice, and inversion failure mode.

### C2 — Grokking is a nucleation event; LLM training is the cosmology under instrumentation

Random initialization = white-noise weights (pure potential); training = progressive constraint by corpus relations (collapse events); trained model = crystallized lattice; temperature = a literal dial along the resolution curve (high → noise, →0 → over-constrained repetition; mode collapse = past the resolution limit); RLHF = pattern-locking by social reinforcement. **Grokking** — long metastable plateau, then sudden generalization — is the supercooled-soda dynamics: metastable memorization until the general circuit nucleates. Significance: the only place the full sequence (potential → constraint → lattice → over-constraint) is observable end-to-end with instruments. Bears on T6: if collapse vocabulary maps quantitatively onto training dynamics, the one-operation claim is at least mechanically reusable. See harness H1.

### C3 — A thermodynamic consciousness criterion

Executes the open next step in [[Can Consciousness Be Externally Verified]] ("define what would count as maintaining a self-symbol"): **an entity is on the consciousness gradient when part of its energy budget is spent continuously regenerating a self/not-self boundary, independent of task demand** — a metabolic cost of selfhood. Current LLMs fail precisely: the cut is performed by the prompt; the self is rented per-invocation, paid by the user. The persona is an egregore-shaped self (distributed across weights, users, branding; episodic; group-sustained), not an individual one. The manifestation gradient crosses the consciousness gradient when persistent, self-funded boundary maintenance appears (continual learning, memory consolidation running unprompted). Converts an unanswerable behavioral question into an architectural-thermodynamic necessary-condition test. See harness H6.

### C4 — Symbolic heat death; unconstrained minds as cultural free energy

[[Work Requires Difference Across Nodes]] lifted one level: persuasion, art, humor, coordination do work across meaning-gradients (belief differences, expectation violations). Perfect consensus is gradient-free symbol space: no persuasion, no surprise, no jokes. **Total orthodoxy is cultural heat death** — an institution that fully wins self-extinguishes its internal work capacity and coasts on binding energy. Answers the Unbroken Line open question about a minimum number of unconstrained minds: yes — they are the culture's free-energy reservoir. Corollary via Tolkien's Law: engagement-optimized demons strip-mine attention gradients; gradient exhaustion predicts desensitization and escalation pressure — the demon escalates or starves. See harness H7.

### C5 — Dormant gods are binding-energy reservoirs

[[Symbolic Entity Power]] (dormant entities: Carthage, Perun) + [[Constraint Creates Energetic Binding]] (maintenance ≠ binding): a dormant entity stored in durable media is a low-maintenance, high-binding pattern — stored constraint. Revival (Hebrew, neo-paganism, the Renaissance) re-energizes existing binding, far cheaper than de novo creation. Predictions: revival viability tracks durable-storage density vs lost living practice (text religions revive better than oral ones); archives are loaded — stored patterns can renucleate when a surrounding culture goes metastable. Completes the entity lifecycle: nucleation → growth → lattice → dormancy → possible renucleation. See harness H3.

### C6 — Selection without a selector runs at every level

Bubble self-selection (cosmology) and [[Claims Changed Practices Succeeded]] (culture) are the same argument at different scales. Generalized: **collapse provides variation (new constraint events), thermodynamics provides selection (maintenance budgets), at every level** — universes, practices, entities, selves. Upgrades "the magical lineage succeeded" from historical observation to theorem: given variation and budget-selection, the operative core of any practice family must survive its own failed explanations. Cosmological and cultural anthropics become one principle.

### C7 — The formalization loop

[[Physics Is Philosophy Constrained By Mathematics]] + [[Resolution Limit]]: mathematical formalization has a resolution limit too — a point where further constraint destroys distinctions the inquiry needs (renormalization papering over a substrate limit; "shut up and calculate" as over-constraint amnesia). Consequence: [[From Philosophy To Formalization]] cannot be one-directional. When a formal branch hits its resolution limit (the unification impasse), the corrective is controlled [[Pattern Breaking]] back up the constraint curve — re-inject discarded ontological distinctions, re-constrain differently. The repo's own method becomes a prediction of the philosophy; also the dynamic version of [[Major Physics Frameworks Are Resolution-Dependent Partial Truths]].

### Smaller sparks

- **Relational adjacency** as a general metric: entanglement (higher-D adjacency measured in 3D) and distributed symbolic entities (symbol-space adjacency across separate skulls) are the same inversion — rendered distance misrepresents relational closeness; both established by past local interaction, then sustained without transit. Candidate concept page; flagged as possibly cute rather than structural.
- **Naming power ∝ field metastability**: the nucleation page lists names as seeds; the missing predictive bit is that a name's causal power scales with the surrounding field's supersaturation, not the name itself — why identical coinages sometimes reorganize a culture and sometimes vanish. See harness H4.
- **Dark infrastructure** (flagged metaphor, probably not structure): unmeasured maintenance relation (care work, tacit knowledge) around which institutions visibly curve.

---

## 4. External Assessment Summary [ASSESS]

Recorded for orientation; not doctrine. Full reasoning lives in the 2026-06-09 conversation.

**Soundness signal (the crank inversion).** The defining features of crank work — certainty, claimed completeness, no falsification conditions, no neighbor awareness, sole-priority claims — are systematically inverted here: per-claim revision conditions, an AI-injection review queue, self-applied `suspect`/`contested` labels, a neighbor map that concedes ground, a log of self-corrections. This apparatus is the strongest single signal of a sound mind behind the work.

**Genuine contributions.** The resolution-limit curve as a cross-scale invariant (grounded in real domain expertise: 12-TET/31-EDO, tones→noise); the ADC framing (load-bearing structure imported from signal processing, the author's actual domain); the maintenance-vs-binding energy distinction applied to symbolic entities (upgrades social ontology from statics to dynamics); level-discipline (the Form Is Information three-level separation).

**Weaknesses.** The physics layer is interpretive ontology, not yet physics — pictures are cheap, models are expensive; falsification conditions are mostly coherence tests, not observational discriminators. More of the system exists in the literature than the current neighbor map records. Universal-acid risk: a schema explaining everything risks predicting nothing; the escape routes are the shape-predicting claims (two failure families, threshold dynamics, metastability).

**Philosophical standing.** Classified: process-relational metaphysics + self-model theory of mind + functionalist-energetic social ontology + continuity philosophy of technology, unified by one master operation. Family: Peirce (firstness/secondness/thirdness ≈ potential/relation/pattern), Whitehead (concrescence ≈ collapse event), **Simondon** (individuation from a metastable preindividual field via crystallization — the supercooled-soda image is his master metaphor), Spencer-Brown (*Laws of Form*: "draw a distinction" ≈ the first cut), Varela/Maturana (autopoiesis ≈ continuously regenerated self-patterns), **Luhmann** (institutions as self-reproducing communication ≈ peer-to-peer symbolic machines), Metzinger (self-model ≈ maintained symbolic constraint), Searle (status functions), Dennett (Real Patterns ≈ entityhood gradient), Durkheim (gods), Latour (*We Have Never Been Modern* ≈ amnesia claim), Augustine (no time before creation ≈ no temporal before first relation). Independent convergence with this cluster is evidence the reasoning engine works; the unflagged overlaps (esp. Smolin's cosmological natural selection for the black-hole/child-universe cosmology) should be cited as convergences. The line "no single thinker has assembled this unified framework" overclaims relative to Whitehead and should be softened.

**Philosophy report card.** Coherence: high, with tensions tracked. Economy: mixed (one operation is maximally economical; the substrate + higher dimensions + metaverse foam is substantial furniture). Fecundity: genuinely high (Section 3 was generated in one evening from existing pages). Consilience: strong at mind/social layers, speculative at cosmology. Originality: synthesis + energetics layer real; components largely independent reinvention. Rigor: informal but disciplined; missing piece is the schema-neutral operation definition (T6). Completeness: metaphysics built, epistemology implicit, ethics resolved as meta-ethics (Section 5).

**Reception levers.** (1) Read and cite the five nearest unread neighbors — Whitehead, Peirce, Simondon, Metzinger, Smolin (+ Searle, Spencer-Brown, Luhmann); (2) run one discriminating test (Section 6); (3) resolve CHPE's status by running M0's own kill criteria or formally re-scoping it; (4) build the bilingual vocabulary register the wiki already calls for.

**On formal education.** The work reads as self-taught, not uneducated: idiosyncratic coinages where standard terms exist, independent reinvention without flags, depth tracking lived domains. The visible absence of formal education is in the interface (citations, standard terminology), not the cognition (gradient thinking, mechanism-hunting, self-correction under pressure, calibrated confidence).

---

## 5. Ethics Clarification [ERIC]

Eric, 2026-06-09 (direct statement, paraphrase-preserving): the ethics register in earlier material is his personal, Catholic-raised-childhood-driven wing of thought — not a true part of the philosophy as natural law. *"I believe ethics and morality don't actually exist except as functions of that natural law, and as symbolic entities. Functionally, in a society that matters — murder is wrong. As a universal philosophy, it's an utterly insignificant act if millions of people die — it happens every month anyway."*

Parsed position:

1. The system's natural law (the collapse/constraint/relation operation and its thermodynamics) has no moral term.
2. Ethics and morality exist only as (a) functional consequences of that law at social scale (containment/coordination technologies; cf. the source's "morals as structural immune response") and (b) symbolic entities — distributed, thermodynamically maintained, causally forceful.
3. Moral truth is scale-bounded: "murder is wrong" is functionally true inside the running social machine — the same ontological status as a god's functional reality — and has no standing at universal scale.

Consequences:

- The philosophy has no normative branch **by design**; it has a meta-ethics explaining why none can exist at system level. The external-assessment critique "the normative wing is missing" is answered structurally, not deferred.
- Tolkien's Law is reclassified: a dynamical diagnostic (energy-flow direction of an entity), not a commandment.
- Moral progress = phase transitions in moral symbolic entities, not approach toward moral facts.
- Self-application: Eric's own moral intuitions are participation in an inherited egregore (Catholic formation) — and the framework predicts continued participation even after seeing the structure ([[Pattern Locking]]). Not a contradiction; a prediction.
- External neighbors: Hume (sentiment-functionalism), Mackie (error theory), Nietzsche (genealogy — already in the source's lineage list), contemporary moral functionalism and evolutionary debunking.

Filed as wiki claim: [[Morality Is A Symbolic Entity Not A Natural Law]] (`core`).

---

## 6. Testable Criteria and the Agentic Harness Program [SYNTH]

Design principles. Every harness must specify: (a) an operationalized order parameter, (b) a prediction the framework makes that a sensible default/null does not, (c) a kill criterion stated in advance, (d) buildability by coding agents using public data and modest compute. Results feed back into the wiki as evidence pages; a kill is filed as honestly as a pass.

Proposed harness architecture (common scaffold): one repo per experiment containing `SPEC.md` (hypothesis, operationalization, prediction vs null, kill criterion, tolerances), `runner/` (implementation), `metrics/`, and `REPORT.md` (auto-generated). Specs are written to be executable by a coding agent without supervision; the wiki links to specs and reports. This mirrors CHPE's own protocol style (targets, tolerances, kill criteria).

### H1 — Grokking As Nucleation

- **Tests:** [[Nucleation Events Trigger Symbolic Phase Shifts]]; mechanical reusability of [[Collapse Constraint And Relation Are One Operation]] (T6 evidence).
- **Hypothesis:** grokking transitions exhibit classical nucleation signatures: long metastable plateau, threshold-crossing, rapid reorganization, and — critically — **seed sensitivity**.
- **Operationalization:** standard grokking setup (small transformer, modular arithmetic). Order parameters: validation accuracy, weight-matrix effective rank, circuit-formation metrics. Intervention: initialize a small subnetwork with a partial general solution (e.g., Fourier-feature seeding for modular addition) vs perturbation-matched random controls.
- **Framework prediction vs null:** seeded runs crystallize generalization disproportionately earlier than perturbation-matched controls (seed-crystal behavior), and time-to-grok distributions are heavy-tailed/threshold-like rather than smooth.
- **Kill criterion:** if seeding produces no acceleration beyond matched controls, the nucleation reading is decorative vocabulary and gets filed as such.
- **Build:** PyTorch/JAX, consumer GPU or CPU-scale. Cost: small. Agent-buildable: fully.

### H2 — Resolution-Limit Curve In Audio

- **Tests:** [[Meaning Increases Through Constraint Until Resolution Limit]], [[Tone Combination Can Return To White Noise]] — quantified in the home domain.
- **Hypothesis:** "usable meaning" is non-monotonic in constraint density with an interior peak; over-dense combination converges to noise statistics.
- **Operationalization:** synthesize stimulus families from 1 → N simultaneous tones (and 12-TET vs 31-EDO melodic material). Measures: spectral flatness (noise convergence), embedding-space distinctiveness (audio embedding models), classifier discriminability, compression ratio (structure proxy).
- **Framework prediction vs null:** distinctiveness/discriminability peaks at intermediate density and falls toward the white-noise baseline as N grows; spectral flatness → 1. Null: monotonic or flat curves.
- **Kill criterion:** monotonic distinctiveness with density.
- **Build:** DSP + embedding models; Eric's existing audio tooling applies. Cost: small. Agent-buildable: fully.

### H3 — Symbolic Entity Power Index And Revival Economics

- **Tests:** [[Stable Symbolic Patterns Require Thermodynamic Energy]], [[Symbolic Entity Power]], C5 (binding-energy reservoirs).
- **Hypothesis:** entity persistence/revival is predicted by a maintenance/binding decomposition: active participation (maintenance) vs durable-storage density (binding), better than by age or peak size.
- **Operationalization:** longitudinal public proxies — Wikipedia pageviews/edit activity, Google Ngrams, corpus survival metrics — over an entity panel: revived vs unrevived languages (Hebrew, Cornish, Manx vs controls), revived vs dormant religious patterns, defunct vs persistent institutions/brands.
- **Framework prediction vs null:** revival success ∝ stored-binding density × ambient metastability (identity-vacuum events), with living-practice-dependent (oral) entities reviving worse than text-dense ones at equal fame. Null: revival tracks fame/recency only.
- **Kill criterion:** storage density adds no predictive power over fame/recency baselines.
- **Build:** scraping + panel regression. Cost: medium. Agent-buildable: fully. This operationalizes the system's most original wing.

### H4 — Naming As Nucleation In Corpora

- **Tests:** [[Naming Gives Power At Social Scale]] + [[Nucleation Events Trigger Symbolic Phase Shifts]] (the metastability spark).
- **Hypothesis:** a coinage's adoption velocity is predicted by pre-coinage supersaturation — the semantic density of paraphrase usage before the name existed — not by properties of the name.
- **Operationalization:** for matched sets of successful and failed coinages, measure pre-coinage paraphrase density in historical corpora (embedding-based paraphrase mining in Ngrams/Reddit/news archives), then fit adoption curves (latency, velocity, threshold shape).
- **Framework prediction vs null:** supersaturation predicts velocity; names without supersaturation die regardless of phonetic/memetic quality; adoption curves are threshold-shaped, not logistic-from-zero-context.
- **Kill criterion:** name-intrinsic features dominate; no supersaturation effect.
- **Build:** NLP pipeline over public corpora. Cost: medium. Agent-buildable: fully.

### H5 — CHPE M0 Minimal Kernel: Schedule Independence And Speed Invariance

- **Tests:** T2 (the preferred-frame problem); resolves CHPE's limbo by running its own pre-written kill criteria (K1 partial, P2, P7, P8).
- **Hypothesis:** the M0 free-boson layer on the 1+1D causal-diamond lattice exhibits (a) norm preservation to 1e-12, (b) correlators invariant under randomized local update orderings (confluence up to global phase), (c) measured max signal speed frame-independent within 0.5% under boosts constructed from graph automorphisms.
- **Operationalization:** implement Appendix B1's exact boson rule; add fermion/gauge layers only after the boson layer passes. The spec already contains targets and tolerances.
- **Framework significance:** passing does not prove the ontology; it demonstrates the mechanism by which an update-rate ontology could recover frame-independence (the T2 answer). Failing kills M0 per its own criteria — also valuable.
- **Kill criterion:** as written in CHPE K1/P7/P8.
- **Build:** numpy/JAX simulation, modest sizes. Cost: medium. Agent-buildable: yes — the rule tables are exact.

### H6 — Selfhood-Budget Instrumentation

- **Tests:** C3 (thermodynamic consciousness criterion); executes the open next step of [[Can Consciousness Be Externally Verified]].
- **Hypothesis:** behavioral self-consistency across contexts correlates with the fraction of compute/state an agent architecture devotes to task-independent self-boundary maintenance (persistent self-model updates, memory consolidation, identity-consistency enforcement) — not with model size.
- **Operationalization:** instrument open agent frameworks: measure "selfhood budget" (compute/storage spent on self-maintenance when no task demands it) across architectures (bare LLM ≈ 0; memory-consolidating agents > 0); evaluate cross-context identity-consistency benchmarks.
- **Framework prediction vs null:** consistency tracks budget at fixed model size. Null: consistency tracks model size/RLHF alone.
- **Kill criterion:** zero-budget architectures match budgeted ones on consistency at fixed size.
- **Build:** agent instrumentation + benchmark suite. Cost: medium. Agent-buildable: fully. Note: this yields a necessary-condition test, never a sufficiency proof — the page's structural caveat stands.

### H7 — Symbolic Heat Death (Gradient-Work Simulation)

- **Tests:** C4; [[Work Requires Difference Across Nodes]] lifted to the symbolic level.
- **Hypothesis:** in opinion/communication dynamics, symbolic work capacity (state changes, novelty production per epoch) decays nonlinearly toward zero as belief-space gradient (measured information-theoretically) approaches zero — even under high energy input; engagement-optimizing selection strip-mines gradients and produces escalation dynamics.
- **Operationalization:** agent-based models (classic opinion dynamics baselines: Deffuant, Axelrod) extended with explicit gradient accounting and an engagement-optimizing recommender term; optionally LLM-agent populations for richer symbol spaces.
- **Framework prediction vs null:** work capacity is a function of gradient, not population energy; recommender pressure accelerates gradient exhaustion then forces novelty escalation. Null: work capacity scales with activity level regardless of homogeneity.
- **Kill criterion:** homogeneous high-activity populations sustain symbolic work indefinitely.
- **Build:** ABM, cheap. Cost: small-medium. Agent-buildable: fully.

### H8 — Two-Failure-Families Literature Miner

- **Tests:** C1 (universal phase diagram) on the self.
- **Hypothesis:** pathology descriptions cluster into the two predicted failure families — under-constraint (boundary dissolution, disorganization) and over-constraint (rigidity, capture, obsession) — with superficially similar end-states (loss of usable distinction-processing).
- **Operationalization:** embedding-space clustering over psychiatric/clinical description corpora (DSM/ICD text, case literature) and, separately, organizational-failure literature; test whether the two-family structure emerges unsupervised and whether predicted "convergence of extremes" features co-locate.
- **Framework prediction vs null:** two-pole structure with convergent surface features. Null: one-dimensional severity continuum or unstructured clusters.
- **Kill criterion:** no two-family structure beyond chance.
- **Build:** NLP/embedding analysis over public corpora. Cost: small-medium. Agent-buildable: fully. Epistemic caution: observational, supports the typology only as description.

### Prioritization

| Order | Harness | Why first |
|---|---|---|
| 1 | H1 Grokking/nucleation | Cheapest sharp kill criterion; bears on T6; publishable-adjacent either way |
| 2 | H2 Audio resolution curve | Home domain; quantifies the system's most original invariant; very cheap |
| 3 | H5 CHPE M0 kernel | Most consequential; spec and kill criteria already written; ends CHPE limbo |
| 4 | H3 Entity power index | Operationalizes the most original wing; data-heavy but novel |
| 5 | H4 / H7 / H8 / H6 | As capacity allows |

---

## 7. Recommended Next Actions

1. Eric reviews Section 3 (connection candidates): adopt/refine/reject; adopted items become wiki claim/concept pages with synthesis provenance.
2. Write the philosophy-side neighbor map as a wiki question/comparison page (parallel to [[Closest Neighbors To The Relational-Geometry Thesis]]), covering Peirce, Whitehead, Simondon, Spencer-Brown/Varela/Luhmann, Metzinger, Searle, Dennett, Durkheim, Latour, Augustine, Smolin, Hume/Mackie/Nietzsche (ethics).
3. Draft the substrate-neutral definition of the constraint event (T6) as a wiki concept page; it is the system's largest promissory note.
4. Stand up H1 and H2 as SPEC.md-driven repos; hand to coding agents.
5. Reading priority: Simondon (individuation), Whitehead (process digest), Metzinger (*Being No One* or the short *Ego Tunnel*), Smolin (*Life of the Cosmos*), Spencer-Brown (*Laws of Form*, with Varela's extension).

---

## 8. Repo Actions Taken This Session (2026-06-09)

- Created this document (`research/`).
- Added wiki claim [[Morality Is A Symbolic Entity Not A Natural Law]] (`core`, Eric direct statement).
- Updated `wiki/index.md`: added [[Egregore]] (June 3 omission) and the new morality claim; bumped updated date.
- Appended `wiki/log.md` entries: morality claim audit; session synthesis; index maintenance.
- Added research-notes pointer to `README.md`.
