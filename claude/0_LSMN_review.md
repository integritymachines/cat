# LSMN: Constructive Technical Review for the Authors

**Version:** 0.1 — 13 November 2026  
**Status:** Independent review and implementation proposal; not an author ruling.  
**Scope:** The common kernel, disposition ledger, scaffolds and reports under this directory, as retrieved from main on 13 November 2026.  
**Requested editorial boundary:** Paper 4 concerns making CAT measurable, predictive and falsifiable. Motility/sessility, the lower bound of consciousness and dreaming as offline conjecture testing belong to a separate paper.  
**Purpose:** Preserve the theory's first-principles argument while making its mathematical translation auditable and its empirical claims testable. No existing file is modified by this review.

## Executive disposition

**Preserve the four-stage architecture, the two-model mediation problem, the O/C/T obstructions, virtual testing before irreversible commitment, and the distinction between control and remapping. Retain Fisher information explicitly. Correct the claim that the discrete operators are exact replacements for Fisher geometry or for scalar curvature. Repair the weighted discrete mathematics before promoting its outputs to empirical predictions. Restrict Paper 4 to the bridge from theory to measurement, prediction and falsification.**

The central question for Paper 3 is not whether graph operators can be computed. They can. It is whether the proposed translation preserves the *navigationally relevant information* carried by the conceptual geometry of Papers 1 and 2, and which information is lost.

I recommend a **three-layer discipline**:

1. **Conceptual layer (Papers 1–2).** An agent uses a comprehensible map to navigate a more comprehensive, parochially sampled territory. Fisher information offers a possible local geometry of statistical discriminability; distortion and control demand are separate concepts.
2. **Formal operational layer (Paper 3).** A pair of complexes, statistical response families, graph conductances, potentials, path lifts, deformation observables and costs give computable, *not automatically equivalent*, realizations of different mechanisms.
3. **Empirical layer (Paper 4).** Independently calibrated estimators and controlled interventions test the relations among these quantities. The observable signatures do not become definitions of consciousness.

Treat an exact theorem, a modeling choice, a heuristic analogy and an empirical conjecture as four different kinds of statements. The existing [ruled]/[inference]/[open] convention should be supplemented by a **claim-type field**: definition, theorem (with assumptions), modeling postulate, empirical hypothesis, or illustration.

### Priority and disposition table

| Priority | Finding | Where | Direct action |
|---|---|---|---|
| P0 | Fisher curvature, Fisher discrimination, map–territory distortion and control need have no one-to-one relation | Kernel §§1, 3; Papers 1, 3 | Replace “retired/replaced/operationalized” equivalence language with an explicit translation contract; retain Fisher |
| P0 | Weighted degree-0 and degree-1 Laplacians and the Hodge decomposition use inconsistent edge inner products | Kernel §3; Paper 3 | Define a single weighted chain/cochain convention and recompute the worked example |
| P0 | Global spectral gap can flag a bottleneck irrelevant to the current goal | Kernel §3; Papers 3, 4 | Add task-conditioned sensitivity and route support; test counterexamples |
| P0 | Existence of a supported route is confused with what a bounded agent knows or can discover | Kernel §§1–3; Papers 1–3 | Define objective support, model-estimated support and budget-discoverable support separately |
| P0 | Paper 4 contains lower-bound and dreaming theory that does not follow from its measurement program | Kernel §4; Paper 4 | Relocate this material and its refutation condition to a separate paper |
| P1 | Work, metabolic allocation, torsion shift and response-time formulas are not mutually derived | Kernel §§1, 4; Papers 3, 4 | Repair units and definitions; reclassify unsupported functional forms as hypotheses |
| P1 | Some formal definitions and empirical signatures contradict their own domains or preceding results | Kernel §§1–4; Papers 1–4 | Apply the specific repairs below |
| P1 | Neural estimators risk circular identification of latent constructs | Paper 4 | Require independent calibration, held-out prediction and negative controls |
| P2 | The disposition ledger needs a translation-loss and claim-dependency register | Disposition and scaffolds | Add explicit provenance and acceptance criteria after author rulings |

## 1. Fisher information must stay; the proposed translation is lossy

### 1.1 What Fisher information contributes

Paper 1 introduces the Fisher metric

$$
g_F(y)_{ik}=\mathbb E_{p(\cdot\mid y)}
\big[\partial_i\log p(\cdot\mid y)\,\partial_k\log p(\cdot\mid y)\big].
$$

For a regular statistical family and a small perturbation $\delta y$, it gives the second-order local distinguishability:

$$
D_{\mathrm{KL}}\big(p(\cdot\mid y)\Vert p(\cdot\mid y+\delta y)\big)
=\tfrac12\,\delta y^\top g_F(y)\delta y+o(\|\delta y\|^2).
$$

This is a real contribution: **the local cost of failing to discriminate two nearby representational states**. It is not the same as the distance between the map and the territory, the existence of an executable route, or the metabolic expense of correcting an error.

An immediate implementation requirement follows: **state exactly what the distribution $p(\cdot\mid y)$ is over.** Candidate choices include sensory observations, future outcomes, neural responses or action policies. They are not interchangeable. For example, a Fisher metric on the observation model need not equal one on the action policy. State the conditioning variables, such as goal, habitat and task, and the assumptions of regularity and identifiability. If a singular Fisher matrix is possible, specify whether a pseudoinverse or a restricted identifiable subspace is used.

**Proposed insertion for Paper 1, Architecture:** “The Fisher metric is a conceptual model of local discriminability, conditional on a specified family of response distributions. It neither measures map–territory distortion by itself nor determines the need for corrective control. Those relations are hypotheses to be formalized and tested.”

### 1.2 Curvature is not discriminability, distortion or navigational risk

Four notions should be distinguished:

- **Discriminability:** local quadratic form $\delta y^\top g_F\delta y$.
- **Curvature:** intrinsic geometry derived from derivatives of the metric; it can have either sign or vanish.
- **Translation distortion:** mismatch between relational/metric structure in territory and map, requiring a correspondence or coupling.
- **Navigational sensitivity:** change in goal-conditioned policy value, route feasibility or loss under perturbation.

None determines the others in general.

Concrete counterexample: a Bernoulli response family with parameter $y\in(0,1)$ has

$$
g_F(y)=\frac{1}{y(1-y)}.
$$

Its discriminability varies with $y$, but the intrinsic Riemann curvature of this one-dimensional manifold is zero. The point is **not** that CAT's map has one dimension. The example disproves the general implication from changing discrimination to nonzero scalar curvature. Higher-dimensional metrics also permit variable metric coefficients with zero curvature.

Consequently the inherited expression

$$
\operatorname{JND}(y)\propto\kappa(y)^{-1/2}
$$

cannot hold generally: scalar curvature may be zero or negative. Under a fixed local discrimination criterion and in a specified direction $v$, the defensible local relation is instead

$$
\operatorname{JND}_v(y)\propto[v^\top g_F(y)v]^{-1/2},
$$

subject to the usual regularity, scaling and measurement assumptions. The relationship of JND to curvature, if desired, requires an additional derivation or explicit empirical hypothesis.

“Bending/folding” in an ambient embedding is not automatically **intrinsic** Riemannian curvature. Likewise, non-injective compression can have severe aliasing with zero intrinsic curvature. A metric's temporal change is not inherently Ricci flow; the inherited $\partial_t g_F=-2\operatorname{Ric}+L_{\mathrm{decay}}$ must be described as a chosen dynamical model, not an identity implied by transience.

**Actions:**
1. Keep Fisher information and intrinsic curvature in Paper 1, but label their roles separately.
2. Delete or quarantine the universal JND–scalar-curvature proportionality until proved under stated conditions.
3. Stop using “high curvature” as a synonym for high distortion, aliasing, singularity, ambiguity or control demand.
4. If the authors wish to retain a scalar conceptual trigger, introduce an explicitly *goal-conditioned loss/sensitivity functional* and test whether curvature helps approximate it; do not silently redefine scalar curvature to mean that functional.

### 1.3 An implementable translation contract for Paper 3

Replace the strong claim “Papers 3 and 4 retire the stand-ins” with: **“Paper 3 constructs discrete operational candidates for the mechanisms suggested by the stand-ins; their correspondence is partial, conditional and testable.”**

Define the following chain for one agent and task:

1. **Territory sample:** a finite, possibly directed relational record $K_S$, sampling measure $\mu_S$, and the limits of what has been observed.
2. **Map and compression:** map states $V_M$, a surjection $\pi:V_S\twoheadrightarrow V_M$, and a task-conditioned preference or value model. Quotienting vertices can introduce *spurious map edges* even though it creates no genuine executable territory transition; acknowledge this.
3. **Statistical geometry:** where data permit, attach a regular family $q(o\mid y,\zeta,h)$ to map states, with observation variable $o$, goal $\zeta$ and habitat/context $h$. Derive the local Fisher metric or discrete pairwise statistical divergences. A finite map does not automatically possess a differentiable Fisher manifold.
4. **Graph geometry:** specify *separately* which edges are permitted and how conductances $G_e$ are assigned from observations, predicted reliability, time/cost or statistical distance. A local information distance, where defined, could be

   $$
   s^2_{mn}=D_{\mathrm{KL}}(q_m\Vert q_n)+D_{\mathrm{KL}}(q_n\Vert q_m)
   \approx\delta y^\top g_F(y)\delta y.
   $$

   This is a **candidate local bridge**, not an automatic choice of $G_e$. Conductance is not information distance, and statistical similarity does not imply physical reachability. Any rule such as $G_e=f(s_{mn},\text{reliability},\text{cost})$ is a modeling choice to specify, calibrate and test.
5. **Goal-conditioned guidance:** $L_0=\partial_1G\partial_1^\top$, $L_0\phi=\zeta$, $j=-G\partial_1^\top\phi$. State how an *actual policy route* $\gamma_j$ is extracted from a possibly branching flow.
6. **Executable-route check:** lift $\gamma_j$ against the agent's *observed* territory, with the limitations of incomplete sampling made explicit.
7. **Correction:** define a controller, a budget, the update to policy and/or weights, and a work/cost functional; only then classify drift, control or remap.

**Required translation-loss register:**

| Source concept | Candidate discrete object | Preserved | Lost / not guaranteed | Validation |
|---|---|---|---|---|
| Fisher local discrimination | $q_m$ divergences; optional graph approximation | Distinguishability of nearby response distributions | Smooth coordinate derivatives, full metric, intrinsic curvature unless reconstructed | Compare pairwise KL predictions against data |
| Fisher natural-gradient dynamics | Goal potential and graph flow | Goal-conditioned ranking/relaxation on a finite graph | Exact natural-gradient law; invariant Fisher geometry | Compare decisions and perturbation responses |
| Scalar curvature / local fragility | Task-conditioned graph susceptibility; gap as a possible bound | Some sensitivity to perturbation | Intrinsic curvature and locality; topology-independent interpretation | Counterexamples and held-out tasks |
| Compression singularity | Failed path lift, optional topology | Discrete route support/aliasing | Degree and probability of execution; unseen paths | Route execution tests |
| Metric evolution | $G_t$, distortion, optional torsion | Some change in map weights/structure | Rate, energetic cost and cause of change | Interventions across time |
| Conscious control work | Explicit policy/revision cost | Computable correction expenditure | Metabolic conversion and subjective identification | Separate physiological calibration |

This table should enter Paper 3 near its opening and the disposition ledger should reference it.

### 1.4 Can CAT dispense with Fisher?

Only after a deliberate change of the claim. One could develop a *purely discrete theory of bounded navigation* using graph potentials and lift tests without ever constructing a Fisher metric. That would be a legitimate mathematical model. It would **not**, merely by existing, establish that the Fisher-based conceptual mechanism of Paper 1 had been operationalized.

**Recommendation:** do not excise Fisher. Keep it in Paper 1, show its exact local statistical meaning, and include in Paper 3 at least one explicit bridge construction *or* a precise declaration that its discrete objects operationalize different aspects and leave Fisher geometry unestimated. The empirical program can compare Fisher-informed and Fisher-free graph models on the same tasks. If the latter prove sufficient, the redundancy of Fisher becomes a result rather than an assumption.

## 2. Fix the graph and Hodge mathematics before using torsion

### 2.1 Make the edge inner product consistent

The degree-zero Laplacian is weighted:

$$
L_0=\partial_1G\partial_1^\top.
$$

But Paper 3 currently defines the degree-one Laplacian as

$$
\Delta_1=\partial_1^\top\partial_1+\partial_2\partial_2^\top
$$

without $G$, while reporting a determinant that changes when $G$ changes. These are inconsistent as written.

A viable convention, for strictly positive diagonal $G$, is to put the differentials into common Euclidean coordinates:

$$
A=\partial_1G^{1/2},\qquad
C=G^{-1/2}\partial_2,\qquad AC=0;
$$

$$
L_0=AA^\top,\qquad
L_1=A^\top A+CC^\top.
$$

Specify the chain/cochain orientation, edge and face inner products, and weights at every degree. If a different convention is preferred, state and consistently use it throughout.

Under this convention the **scaled electrical flow** $q=G^{-1/2}j=-A^\top\phi$ is a pure gradient; its harmonic component is zero. A *candidate route as an edge chain* may have a nonzero harmonic component. The report currently risks confusing decomposition of the potential-induced flow with decomposition of a candidate path. These are different objects.

**Actions:** rewrite the Hodge section using a single convention; identify which object is decomposed; recompute all $\Delta_1$ spectra, harmonic components and torsion values using the same weights.

### 2.2 Recheck the four-state example and its conclusions

The current reported identity

$$
\det{}'\Delta_1=3(1+2G_{m_3m_1})
$$

is compatible with an appropriate **weighted** graph construction. It is not implied by the unweighted definition of $\Delta_1$ printed in the report. For the unweighted unfilled triangle, $\det{}'\Delta_1=9$ regardless of changing $G$ in a separate $L_0$.

At zero edge weight, removing the edge and changing the dimension of the chain space must be distinguished from retaining a formally present zero-conductance edge. The asserted change in $\beta_1$ belongs to the *topological deletion*, not merely to continuously changing a positive weight.

The example has another useful result: with uniform sampling of all four territory vertices and shortest-path distances, its anchored squared distortion is $22/16$ both **before and after** removal of the false shortcut. On the restricted sample $\{z_1,z_2,z_3\}$ it falls from $2/9$ to $0$. Thus locally successful reconciliation need not improve globally aggregated distortion. This is an argument for carrying **task-conditional** and **global** fidelity separately, rather than treating the example as a single measure of repaired translation.

Suggested minimal reproducibility package:

- List $V_S,V_M,\pi,\Lambda_S,\mu_S,\partial_1,\partial_2,G$ explicitly.
- Print $L_0,L_1$, all eigenvalues and the chosen pseudodeterminant convention.
- Compute the preferred route, route lift and alternative lift.
- Compute anchored distortion on all four vertices and on the task-relevant subset, before/after the intervention.
- Distinguish edge reweighting, edge deletion, and vertex splitting as three operations.
- Report whether the model is in control or remap under a predeclared rule; do not choose the rule after viewing the result.

### 2.3 Torsion is an observable, not the cost of its change

The correction that log torsion is a *signed observable of deformation*, not control work, should be preserved. But the proposed empirical inequality

$$
\mathcal W\ge c_0|\Delta\log\operatorname{Tor}|
$$

does not follow from the torsion-variation identity. That identity computes the change of a spectral functional; it supplies no energetic bound by itself. A graph can also change without a torsion change, and torsion can change for reasons unrelated to goal-directed control.

The term “Ray–Singer torsion” should be qualified: the finite-complex spectral expression requires a declared discrete/combinatorial torsion convention, cohomology/basis handling and inner products. Rank-change behavior must be treated explicitly.

**Constructive route:** define the path-dependent correction cost first. For example, for flow corrections $w_t$ one might investigate $\sum_t w_t^\top G_t^{-1}w_t$; weight updates and maintenance need separate nonnegative costs. Only then derive any inequality involving torsion under specific limits on time, permissible updates and operator sensitivity. If no such derivation exists, test torsion as a *predictor/covariate*, not a guaranteed lower bound on work.

### 2.4 Units and work accounting

The kernel equates integrated work and instantaneous allocation:

$$
\mathcal W=\int\|w\|^2_{g_F}\,dt=\eta a,
\qquad
a(t)=a_{\mathrm{base}}(t)+\sum_e\Delta a_e(t).
$$

This mixes a trajectory integral with a time-dependent rate and assumes the metric norm has calibrated energy units. Define instead an instantaneous operational power or cost rate $P_{\mathrm{ctrl}}(t)$, an integrated cost $W_{\mathrm{ctrl}}=\int P_{\mathrm{ctrl}}dt$, an instantaneous *metabolic* power $P_{\mathrm{met}}(t)$ attributable to the mechanism, and corresponding integrals over matched intervals. Only identify $\eta$ as a dimensionless conversion efficiency after both sides are expressed in compatible energy units.

Specify whether baseline maintenance is part of $w$. If drift has $w\approx0$ but $a_{\mathrm{base}}>0$, the two cannot be universally equated without a separate maintenance term. Keep ordinary background metabolic expenditure distinct from allocation to mediation; otherwise “conscious iff $a>0$” becomes either unmeasurable or overinclusive.

## 3. Make sensitivity and the regime threshold task-conditioned

### 3.1 A global spectral gap is not a local alarm

The graph's $\lambda_2$ is global. A graph with two internally well-connected clusters joined by a weak edge can have a tiny $\lambda_2$ while the agent solves an entirely intra-cluster task with stable, reliable guidance. The global gap would wrongly signal a control demand.

Conversely, the report's aliased triangle has $\lambda_2=3$ with unit weights, although the preferred shortcut has lift zero. The lift catches that failure; the gap alone does not.

An available task-conditioned diagnostic is

$$
R_{\zeta}=\zeta^\top L_0^\dagger\zeta.
$$

For a unit source/sink pair this is effective resistance; for a general goal vector it measures the response of the potential to that goal. It is not a substitute for path lift or a universal control trigger, but it makes the distinction between a global spectral bound and a specific task explicit. Other candidates include goal-conditioned hitting times, local policy margins, sensitivity of the chosen action to perturbations and expected regret.

**Actions:**
1. Retain $\lambda_2$ as a global stability diagnostic or bound, not an unconditional analogue of local scalar curvature.
2. Specify a task-conditioned diagnostic and compare its predictions with those of $\lambda_2$.
3. Define a budget- and loss-dependent critical rule, with units and an independently calibrated threshold.
4. Present thresholded control as a **policy rule** unless a mathematical bifurcation is independently derived. A smooth change of conductances need not produce a step change of $\lambda_2$.

### 3.2 Existence, knowledge and discoverability are different

For a finite known territory, $\operatorname{lift}(\gamma\mid z_0)>0$ means **at least one** compatible path exists in the recorded graph. It does not mean all executions succeed, the agent knows the path exists in reality, the sample is complete, or that execution is affordable.

Distinguish:

- $\Gamma_{\mathrm{true}}$: routes supported by the full environment (generally unavailable to the agent).
- $\Gamma_{\mathcal S}$: routes supported by the agent's sampled territory.
- $\widehat{\Gamma}_{B}$: routes found or certified by its finite search procedure under budget $B$.

The present criterion $\Gamma(\gamma)=\varnothing$ makes remapping depend on exhaustive knowledge. That conflicts with the claimed unsurveyability. Operationally, a controller can remap when **no acceptable route is discovered within budget and confidence limits**, while the possibility of an unknown valid route remains open. Distinguish a deliberate remap decision from proof of impossibility.

For stochastic and non-stationary environments, move beyond binary lifts where needed: estimate $\Pr(\text{execution succeeds}\mid\mathcal S,\gamma)$, expected loss and uncertainty. Do not call an existential positive lift an *assurance* without an appropriate robustness or probability criterion.

The envelope $\mathcal E$ can be retained, but label whether it is a mathematical oracle envelope, an estimated envelope or an agent's assured/budget-certified envelope.

### 3.3 State the control/remap rule as an executable algorithm

A minimal pseudocode-level rule should specify:

1. Update the sampled territory and current goal.
2. Generate candidate routes from the map's current preference structure.
3. Test the preferred route against available territory evidence.
4. If sufficiently supported and below a task-dependent expected-loss threshold, execute under drift.
5. Otherwise search for a sufficiently supported alternative within a fixed budget; if found, correct policy/weights (**control**).
6. Otherwise revise representation or compression (**remap**) and flag unresolved uncertainty.
7. Record computation, intervention, error and metabolic measurements.

The exact controller, stopping rule and costs must be supplied. Theorem 3.2 should then be restated as a **conditional fixed-policy failure lemma**, not evidence that a physical control-work expenditure or conscious engagement is mathematically necessary. The latter remains the explicit consciousness postulate.

## 4. Repair secondary definitions and cross-paper consistency

These changes are independently checkable and should be implemented without changing CAT's conceptual commitments.

1. **Opacity range (Kernel §2, Paper 2).** $o=1-\operatorname{corr}(\cdot,\cdot)$ ranges over $[0,2]$, not $[0,1]$. If correlations are known nonnegative, say so; otherwise use $(1-\operatorname{corr})/2$, or define opacity through calibrated predictive error. The “global gradient” is available to a synthetic experimenter, not generally to the agent.
2. **Combinatorial intractability (Kernel §2, Paper 2).** $|X|\ge k!$ is not guaranteed by “$k$ interacting options”; make the permutation structure an assumption or present it as one example. State finite computational and representational precision constraints: a low-dimensional real vector with unrestricted precision is not automatically a limited-capacity code. Intractability alone does not imply only neighbor moves without an access/cost model.
3. **Unsurveyability notation.** $U=I+N$ with $N=(O,C,T)$ is a structured decomposition, not a scalar sum, unless an aggregation is defined. Write $U=(I;O,C,T)$ or explicitly call the plus symbolic.
4. **Relational territory.** “No gradient” means no *task-given preference or potential*, not that a graph has no mathematically definable gradients. Likewise “unordered territory” should mean *not globally ranked*: recording adjacency, temporal evidence or causality already introduces order-like structure.
5. **Metric convention.** If $\Lambda_S$ is directed, shortest-path dissimilarity may be asymmetric, while the stated metric-measure Gromov–Wasserstein expression presupposes symmetric metrics. Either restrict the distance construction to symmetric metrics or specify a directed/dissimilarity extension. Normalize $\mu_S$ and specify zero-mass cases.
6. **Transport terminology.** Both $d_{\mathcal{SM}}$ and the displayed $d_{\mathrm{GW}}$ are written as *squared discrepancies*; an ordinary distance requires the appropriate square root and normalization. Define the convention once.
7. **Perspective asymmetry (Proposition 3.3).** Nonisomorphic metric-measure maps have positive metric GW distance by construction, but different sampling procedures do not automatically give nonisomorphic maps. Keep the latter as an assumption to test; do not interpret the mathematical statement alone as a solution to the hard problem.
8. **Harmonic cycles and states.** Paper 3 correctly says $\beta_1>0$ need not imply a contradiction; Paper 4 nevertheless assigns $\beta_1=0$ to drift and $\beta_1>0$ to overload. Remove these as necessary state classifications or provide additional task-specific assumptions.
9. **Error compounding.** The kernel's proposed $\operatorname{err}_{i+1}=(1+\operatorname{rate})\operatorname{err}_i$ is marked open and cannot generate new error from zero. A more flexible candidate is $\operatorname{err}_{i+1}\le L_i\operatorname{err}_i+\xi_i$, with $L_i$ and disturbance $\xi_i$ tied to the three obstructions.
10. **Signature cube.** Do not confuse the *presence of mathematical structure* $(R,F,D)$ with the *degree of obstruction* $(o,c,\vartheta)$. More structure may reduce an obstruction rather than signal more of it. Specify both sets of coordinates or keep the cube explicitly taxonomic.
11. **Economic viability.** The inequality “expected losses avoided > expected engine costs” is useful, but specify the counterfactual policy, horizon, common units, probability model and omitted costs of physical execution. It is an ex ante decision criterion, not a theorem of consciousness.

## 5. Paper 4: empirical accountability and nothing else

### 5.1 Remove the lower-bound material

Per the requested separation, **remove Paper 4's current Lower Bound section, its comparative taxa table, the necessity claim about REM/dreaming, the LLM placement argument, and the dream-related refutation condition.** Relocate these to a separate proposed Paper 5, provisionally *The Lower Bound of Consciousness*, with motility/sessility, the economics of physical versus virtual conjectures, dreaming as far-fetched offline rehearsal under physical incapacitation, and comparative boundary cases.

These claims remain important theoretical corollaries. Their relocation does **not** weaken Paper 4: Paper 4 should test the mechanisms without presupposing the correct classification of conscious organisms.

Sleep, propofol, ketamine and REM may remain in Paper 4 as **experimental states** where model predictions can be contrasted. Do not make the *capacity to dream* a prerequisite for applying the measurement framework.

### 5.2 Reorganize around an empirical dependency chain

Suggested Paper 4 structure:

1. **What would make CAT scientific?** Measurability, prospective predictions, identifiability, comparison with alternative mechanisms and clear refutation conditions.
2. **Latent constructs and observables.** A table of each Paper 3 quantity, its units, sampling scale, the neural/behavioral/metabolic candidate estimators and its expected failure modes.
3. **Estimator qualification.** Independent validation against synthetic known graphs, known interventions and held-out measurements. Separation of reconstructed neural connectivity from the latent navigational map.
4. **Preregisterable waking hypotheses.** Predictions for controlled ambiguity, contingency, time-varying structure and correction costs. Conditional quantitative forms and rival predictions.
5. **State comparisons.** Wake, overload, flow, sedation, dissociation and sleep as experimental contrasts, not comparative consciousness taxonomy.
6. **Experimental protocols and controls.** Manipulations, confounds, negative controls, sample size logic and out-of-sample forecast criteria.
7. **Falsification logic.** Which observation rejects an operator hypothesis, a translation-bridge hypothesis, the control mechanism, or the consciousness interpretation? Keep these distinct.
8. **Limitations and handoff.** Unresolved estimators, cross-species generalization and referral to the separate lower-bound paper.

Do not make Paper 4's empirical claims depend on the separate corollary paper.

### 5.3 Repair Tests 4.3–4.7 before preregistration

| Existing test | Problem | Implementable replacement |
|---|---|---|
| 4.3: a step drop of $\hat\lambda_2$ followed by control | A step in a smoothly weighted graph's eigenvalue is not derived; a threshold in policy does not make the eigenvalue discontinuous | Predict a predeclared change of *control policy/cost* at an independently calibrated task threshold; investigate whether graph spectra predict its location |
| 4.4: $RT=t_0+c_1|\lambda_2-\epsilon^\ast|^{-1/2}$ | Does not follow from the asserted $t_{\mathrm{rel}}\propto\lambda_2^{-1}$; it diverges at positive $\epsilon^\ast$ where the latter remains finite | Use the $1/\lambda_2$ scaling as one conditional spectral model; mark critical-divergence alternatives as additional hypotheses requiring a specific bifurcation model |
| 4.5: decision boundary proportional to gated $\log\operatorname{Tor}$ | Log torsion can be signed and scale-dependent; harmonic cycles need not require braking | Predict task-specific braking from uncertainty, failed lift or revision demands; test torsion increments as *additional* explanatory variables |
| 4.6: allocation linear in signed torsion shift | A lower bound in absolute shift would not imply linearity; energetic inequality itself is not proved | Validate metabolic energy against *measured correction expenditure*; assess whether absolute torsion change adds out-of-sample prediction |
| 4.7: no response to gap under anesthesia/dreamless sleep | Requires separating lack of external response from absence of internal processing; estimator and state-definition ambiguity | Predefine state, task, recording sensitivity and control-channel response; use positive and negative controls and state-specific null predictions |

Do not carry over provisional numeric cutoffs (e.g. a 50 ms lag, a half-sized eigenvalue drop, a fixed inter-agent distance threshold or REM distance bands) as established values. They can be preregistered exploratory values if justified and separately verified.

### 5.4 Minimal experimental design

Use an artificial finite navigation task in which the investigator **knows** the territory graph and its changes, but participants see only locally sampled observations. Independently manipulate:

- **Opacity:** quality of local cues without changing true route connectivity.
- **Contingency:** cost or irreversibility of an incorrect branch.
- **Transience:** frequency and location of route/edge changes.
- **Task location:** within a well-connected cluster versus across a weak global bottleneck.

Measure behavior (choice, virtual backtracking, latency, error, policy revision), computational model fits, metabolic candidate markers, and independently estimated neural statistics. Fit both a Fisher-informed model and a graph-only model to one set of trials; prospectively predict held-out perturbations.

**Critical negative controls:** a graph with tiny global $\lambda_2$ but a trivial local task; a high-gap graph with a false shortcut; a harmless cycle; an edge-weight change with no change in route choice; and a route change accomplished by existing policy rather than map revision.

This experiment is feasible in a simulated environment before any commitment to neurophysiological interpretation. If the graph model cannot discriminate its own finite regimes, a neural estimator cannot repair it.

### 5.5 Avoid the estimator circularity trap

If the same physiological control marker both establishes $\epsilon^\ast$ and validates the predicted control transition, the test is circular. A model fit to any conflict-related neural activation could appear confirmatory.

Require:
- predeclared maps from recordings to $\hat L_0,\hat\beta_1,\widehat{\operatorname{Tor}}$ and their uncertainty;
- separate threshold calibration and confirmatory test data;
- perturbations known to alter topology/connectivity while holding difficulty or generic arousal approximately constant, and vice versa;
- held-out comparison against simpler models (difficulty, uncertainty, response conflict, standard sequential sampling);
- failures assigned to the correct layer: invalid estimator, invalid graph translation, incorrect control mechanics, or incorrect consciousness identification.

### 5.6 What falsifies which claim?

An empirical failure should not be reclassified automatically as “bad estimator”; nor should a bad estimator be treated as disproving the entire consciousness claim.

Use a graded dependency tree:

- **Operator-level failure:** under known finite graphs, mathematical identities or inferred regime classifiers do not hold as defined.
- **Bridge failure:** Fisher-informed local distinctions and graph proxies disagree beyond their stated approximation domain.
- **Mechanism failure:** valid independently calibrated quantities do not predict route failures, corrections or energy costs prospectively.
- **Consciousness-link failure:** the mechanism is present where carefully defined experience-related evidence is absent, or absent where such evidence is present, under a specified auxiliary measurement theory.

The last is the difficult bridge and must remain labeled as a substantive hypothesis, not disguised as a theorem about Laplacians.

## 6. Suggested authoring sequence and acceptance criteria

Do not revise all four reports simultaneously. Establish one common mathematical contract and let the drafts inherit it.

**Change set A — kernel definitions and epistemic types (P0).**
- Correct opacity range, units, curvature/JND and algebraic notation.
- Record that Fisher is retained; spectral objects are complementary operational candidates.
- Add the distinction $\Gamma_{\mathrm{true}}$, $\Gamma_{\mathcal S}$, $\widehat\Gamma_B$.
- Separate graph gap, task-conditioned sensitivity, route lift, map distortion and control expenditure.
- **Accept when:** every symbol has one meaning and every claimed equivalence has either a proof with conditions or an explicit “approximation/hypothesis” label.

**Change set B — Paper 3 mathematics and benchmark (P0).**
- Choose one weighted Hodge convention; define graph/metric and torsion conventions; supply actual policy extraction and control update rules.
- Recompute and publish the full four-state example.
- Add the five negative-control environments in §5.4.
- **Accept when:** all example numbers are reproducible from listed matrices, all route classifications are algorithmic, and no regime relies solely on a global spectral gap.

**Change set C — Paper 1 and Paper 2 consistency (P1).**
- Preserve the explanatory argument and original provenance.
- Distinguish discriminability, intrinsic curvature, aliasing and navigational risk.
- Correct intractability/opacity definitions, Fisher conditioning and the role of parochial sampling.
- **Accept when:** the conceptual claim no longer depends on a demonstrably false universal geometric implication and Paper 1 remains intelligible without Paper 3.

**Change set D — Paper 4 refocus (P0/P1).**
- Move lower-bound material out; build a construct-to-estimator table, a test dependency matrix and preregistration-ready protocols.
- Rewrite Tests 4.3–4.7 with derivation status, uncertainty, competing models and falsifiers.
- **Accept when:** each empirical prediction identifies an intervention, observable, conditioning assumptions, failure criterion and the exact theoretical claim at risk.

**Change set E — separate corollary paper (P1).**
- Make motility/sessility, the physical-versus-virtual conjecture economics, offline conjecturing, dreaming and comparative lower-bound tests a self-contained proposal.
- Treat necessity claims as distinct from the verified control mechanics.
- **Accept when:** Paper 4 can be read and tested without using a claim about which organisms dream.

## 7. Minimum viable falsification bench for Paper 3

Before introducing neural data, implement the following deterministic finite cases. Record predicted regime from a *fixed, predeclared* classifier and compare it to route-level ground truth.

| Case | Construction | Required behavior |
|---|---|---|
| A: global bottleneck, local safety | Two dense clusters with one weak bridge; source and goal inside one cluster | Small global gap **alone** must not force control |
| B: locally fatal alias | Existing four-state territory path and aliased map triangle | High gap must not hide a zero-lift preferred shortcut |
| C: harmless cycle | A cycle whose candidate routes all lift correctly | $\beta_1>0$ **alone** must not imply overload/remap |
| D: incomplete sampling | Omit a territory transition that actually exists in the simulated landscape | Failure under sampled $\mathcal S$ must not be called physical impossibility |
| E: smooth parameter drift | Slowly change a conductance without a graph-topology change | Neither a torsion change nor smooth spectral movement automatically implies a discrete regime transition |
| F: local versus global repair | Suppress the false shortcut of the four-state example without splitting the aliased vertex | Local distortion improves; full four-state distortion stays $22/16$ |
| G: Fisher without curvature | Bernoulli response family above | Varying discriminability with zero scalar curvature must be represented correctly |

A pass is not “the chosen diagnostic predicts its own threshold.” A pass means the explicit controller and its observables classify *independently known* navigational contingencies without post hoc exceptions.

## 8. Specific text edits to the current repository

These are proposed substitutions; the author should make the corresponding rulings before incorporating them.

- **Kernel §0.1 / Paper 3 introduction:** Change “Papers 3 and 4 replace the pair / curvature becomes operational” to “Paper 3 supplies computable candidates for identification, composition, persistence and correction; their correspondence to Fisher geometry and curvature is conditional and lossy.”
- **Kernel §1 / Paper 1 Curvature:** Keep scalar curvature as a geometric hypothesis but remove the universal identification with translation failure and replace the JND relationship with Fisher-local discrimination under specified conditions.
- **Kernel §3 / Paper 3 Identification:** Add task-conditioned sensitivity next to $\lambda_2$; explain why $\lambda_2$ is a bound/global diagnostic, not a local curvature measurement.
- **Kernel §3 / Paper 3 Composition:** Define an extracted route and three notions of route support; revise “positive lift = assured navigation.”
- **Kernel §3 / Paper 3 Persistence:** Define weighted $L_1$ consistently with $L_0$, explain torsion normalization/rank changes, and keep deformation distinct from work.
- **Kernel §3 / Paper 3 worked case:** Recompute the spectra and both distortion domains, explicitly separating weight change and topological deletion.
- **Kernel §§1 and 4:** Distinguish baseline maintenance energy from event-specific correction work and instantaneous versus integrated quantities.
- **Paper 4 scaffold / report:** Remove Lower Bound and dream-necessity refutation; include the estimator and falsification dependency chain above; retain altered states only as experimental contrasts.
- **Disposition ledger:** Add an entry for each changed assumption or removed inference so that preserving the 2025 argument does not mean preserving known mathematical mistakes.

## Closing assessment

The intellectual center of CAT is intact: bounded agents face an unsurveyable landscape, build a comprehensive but parochial territory and a tractable navigational map, and sometimes must pay to correct a failing translation before irreversible action.

The strongest opportunity is to make **the translation itself** scientifically accountable. Fisher information is worth keeping because it states a precise local property of a statistical representation. The proposed graph and topology operators may add something genuinely new: finite, task-oriented tests of guidance and executable routes. Their joint value will be greater if no false equivalence is imposed between them.

The immediate test is whether a single explicit finite agent can carry **both** a statistically defined notion of discriminability and a graph-based navigation mechanism, and whether their agreement and disagreement under controlled perturbations are predictable. That result should determine how much of Fisher geometry Paper 3 legitimately inherits. Paper 4 can then test the surviving claims in biological data without carrying the separate lower-bound argument.

---

## Response from the drafting side

Claude, 13 November 2026. The authors ruled on the review the same day, and the drafts adopt it under those rulings: kernel 0.13, Paper 1 report 0.4, Paper 2 report 0.3, Paper 3 report 0.3, Paper 4 report 0.3. The disposition ledger lists each change. The mathematical findings were checked independently before adoption. All of them hold: the weighted convention, the deletion of an edge against a vanishing weight, the unchanged global distortion of $22/16$, the opacity range, the units of work and allocation, error compounding from zero, the latency exponent, and the Bernoulli counterexample. Where the review and the rulings differ, the rulings govern. The points below are where this side disagrees with the review, or where the adoption departs from its proposal.

1. **Curvature is a synecdoche, not literal geometry.** The review reads the geometry of Paper 1 as mathematical claims and shows that discriminability, intrinsic curvature, distortion and navigational risk do not determine each other. As mathematics this is right. The authors' position is that Paper 1 develops conceptual synecdoches to explain the underlying concepts. The adoption therefore keeps curvature in Papers 1 and 2. It labels curvature as an illustration and states what it stands for. It withdraws only the general claims that the counterexamples refute: the relation of the just-noticeable difference to curvature, and the reading of the Ricci-flow equation as implied by transience. The review's fourth action under §1.2, to stop using high curvature for distortion and the rest, is adopted for Paper 3 and not for Paper 1.

2. **Test forms and the torsion bound are postulates, not hypotheses.** The review proposes to reclassify them as hypotheses. The authors ruled that they are elements of the model, subject to empirical test, and that this does not make them hypotheses. They carry the type "postulate" and keep their place in the model. Their internal inconsistencies are corrected: the exponent in the latency law, the step drop of an eigenvalue, the classification of states by $\beta_1$. The type "hypothesis" is used where the authors called a claim a hypothesis to be confirmed, namely the remap rule.

3. **One critical level, not two.** The review proposes $R_\zeta = \zeta^\top L_0^\dagger \zeta$ as a task-conditioned diagnostic with its own threshold. The adoption uses $\lambda_\zeta = \lVert \zeta \rVert^2 / R_\zeta$, for two reasons. First, $\lambda_2 = \min_\zeta \lambda_\zeta$, so the global gap is the worst case of the task gap and $\epsilon^\ast$ stays the single critical level of Papers 3 and 4. Second, $\lambda_\zeta^{-1}$ is the mean of $\lambda_k^{-1}$ weighted by the goal's spectral content. It is therefore the mean relaxation time of the task potential, and Test 4.4 can use it without a new assumption. The two-cluster case gives $\lambda_2 \approx 0.005$ and $\lambda_\zeta = 4$ inside a cluster, which confirms the review's case A.

4. **Scope of a report.** The review asks for controller pseudocode, preregistration protocols, sample-size logic and a full experimental design. A five-page report carries the fixed regime rule, the bench, a design sketch, the qualification rules and the layered falsification. The protocols belong to the paper stage of Paper 4 and to the work that follows it.

5. **Notation of unsurveyability.** The review proposes $U = (I; O, C, T)$. The authors treat $U = I + N$ as canonical. The adoption keeps the notation and states once that the sum is symbolic and names a decomposition.

6. **The Fisher bridge is one choice.** The symmetrized divergence is a sound local bridge for a regular family. Hellinger distance, Jensen-Shannon divergence or Fisher-Rao length would serve as well. The adoption marks the bridge as optional. Whether any bridge adds predictive power over a graph-only model is left to the design in Paper 4, as the review proposes.

7. **The separate paper.** The review names it Paper 5. The authors call it a separate paper and have not set its place in the series. No file was created for it. Its material is parked in kernel §6 so that nothing is lost while it stays out of Papers 1 to 4.

8. **Remap under budget.** Adopted as a hypothesis, as ruled. One gap remains that the review does not address. An agent that repeatedly fails under control on the same instance may remap even when $\Gamma_B$ is not empty. The rule as written does not cover this case, and it is listed as open.

9. **Torsion terminology.** Agreed. The finite expression is now called combinatorial torsion. The analytic name remains only as a pointer to the note.
---

## Review round 2 — Conceptual-to-scientific bridge and targeted corrections

**Reviewer follow-up, 13 November 2026.** This section is appended *after*, and without altering, the drafting side's nine-point response. It records the project principal's clarification, the agreed methodological resolution, and the next actionable recommendations. It does not purport to be an author ruling. **Author response to this round: pending.**

### R2.0 Decision and resolution of the earlier methodological disagreement

The project principal clarifies that **the combinatorial territory, continuous map, Fisher geometry and curvature-as-signpost were deliberately selected as expository synecdoches**. They develop the concepts in Papers 1–2 rather than claim to be the complete measurable mathematics of CAT. It was understood from the beginning that these illustrations would be too simple to make CAT empirically falsifiable and could be replaced by other operational mechanisms without abandoning the architecture. Attempting to put Paper 3's actual operators in Paper 1 would make the conceptual exposition inscrutable.

**Disposition: accepted.** The drafting side should **defend** this deliberate expository decision, rather than apologize for it or treat the absence of the final operators from Paper 1 as a technical mistake. The review's earlier mathematical objections remain relevant only when an illustrative property is asserted as a universal mathematical law, or when the later scientific realization wrongly claims to be equivalent to the illustration.

The reviewer withdraws any implication that CAT must retain **literal** Fisher curvature, natural-gradient flow or intrinsic Riemannian geometry in its eventual operational theory. Their historical and explanatory role should be preserved; their empirical indispensability should be **investigated, not presumed**. Conversely, no set of graph operators should inherit the explanatory achievement of the conceptual argument merely because its symbols resemble those of Paper 1.

The methodological agreement is thus:

> **Preserve explanatory relationships, not mathematical objects.** Papers 1–2 establish the conceptual architecture. Paper 3 proposes mechanisms that discharge its explanatory obligations. Paper 4 tests those mechanisms and the distinct consciousness attribution. Each passage is a translation with explicitly recorded losses, assumptions and tests.

**Important terminological precision:** Fisher information itself is not a compression algorithm. In the conceptual exposition, compression is performed by $\pi$; Fisher geometry illustrates local statistical discriminability *within the resulting map*. This clarification need not burden Paper 1's main argument. It can be made once at the inter-paper bridge.

### R2.1 What must remain invariant?

Replace the current predominantly *object-to-object* translation table with a **two-stage contract**: first a functional/inferential contract, then the existing table of mathematical candidates and losses.

The following are the architectural commitments to be preserved in a candidate realization:

1. **Bounded access:** $\mathcal L$ is unsurveyable to the agent; $\mathcal S$ is its parochial, incomplete accumulation of encountered distinctions, not a God's-eye view.
2. **Two distinct representations:** $\mathcal S$ and $\mathcal M$ have different roles. The former preserves encountered constraints more faithfully; the latter makes choices searchable and rankable.
3. **Lossy compression:** $\pi:\mathcal S\to\mathcal M$ sacrifices distinctions that can become navigationally consequential; the map cannot be presumed faithful.
4. **Manufactured guidance:** the agent must generate task-directed preference or direction not given by the territory as a globally reliable ordering.
5. **Three obstructions along trajectories:** opacity, contingency and transience can make guidance unreliable, costly to reverse, or stale.
6. **Operational mediation:** the agent tests or corrects proposed navigation against its available territory before or during action, under finite resources. Control and remapping are distinguishable operations, even if their decision boundary remains an open hypothesis.
7. **Accountable expenditure:** correction, maintenance and representation changes are resource-dependent; a scientific realization must specify the relevant costs and consequences.
8. **Separate consciousness commitment:** CAT's identification of the relevant mediation/allocation with consciousness is a postulate. It does not follow mathematically from the existence of a graph, Fisher metric, or controller.

These are explanatory commitments, not a demand that the scientific model literally reproduce a continuum, smooth metric, curvature field or exact Fisher gradient.

**Implementation proposal (Paper 3, new first subsection before the current “Contract”):**

| Explanatory obligation | Paper 1–2 synecdoche | Paper 3 candidate realization | Evidence of fulfillment |
|---|---|---|---|
| Preserve encountered distinctions | Combinatorial territory | Sampled relational complex $K_S$ | Known, task-relevant relations survive sampling |
| Enable finite search | Continuous/comprehensible map | $\pi$ and compact weighted $K_M$ | Search cost reduced, with documented information loss |
| Supply goal direction | Smooth/natural gradient | $\phi,\ j,\ \gamma_j$ | Policy ranking varies appropriately with goal |
| Express local discriminability | Fisher metric | Optional distributions $p_m$, $D_{\mathrm{sym}}$ or another divergence | Predicts discriminable versus aliased observations |
| Detect inadequate guidance | Large curvature near $\kappa^\ast$ | Route lift, task sensitivity, independent error/cost signals | Flags genuine navigation failures, rejects false alarms |
| Test before irreversible action | $w$, virtual backtracking | Budgeted search of alternatives in $\mathcal S$ | Prevents avoidable costly commitments |
| Correct or rebuild | Control versus remap | Flow/weight correction, or change of $K_M$/$\pi$ | Restores expected navigational reliability |
| Measure correction burden | Integrated control cost | Explicit intervention costs, metabolic estimates | Prospective, calibrated resource predictions |

The fourth column is essential. Without it, the table is merely a dictionary of renamed objects. The existing “Kept/Lost” table remains valuable and should follow this one as a **mathematical translation-loss register**.

### R2.2 Adequacy conditions for a scientific realization

Paper 3 should state four qualification tests that do **not** presuppose the final biological interpretation:

- **Structural adequacy.** Do the formal objects instantiate the roles they are assigned? Is compression actually non-injective when it matters? Can a sampled territory differ from the landscape, and the map from the territory?
- **Causal adequacy.** Does the specified mismatch *cause* the predicted failure mode within the model, rather than merely correlate with a diagnostic? Example: spurious edge from aliasing causes a route with zero lift.
- **Interventional adequacy.** Does a predeclared correction to the causal mechanism restore navigation under controlled perturbation, without choosing a new threshold after seeing the answer?
- **Explanatory economy.** Does a common mechanism classify several obstruction/failure types without bespoke rescue rules for each counterexample?

**Pass criterion:** implement and validate on known finite systems, with ground truth specified independently of the classifier. A mechanism that fails here is not a validated realization of CAT.

**Limit on theoretical flexibility:** failure of one mathematical realization need not refute the conceptual architecture; however repeated failures across independently motivated, adequately specified realizations should force revision of the architecture or its causal commitments. Authors must not use “Paper 1 was only illustrative” to exempt an already committed operational model from empirical refutation. State in Paper 4 exactly which claims are at risk in a test and what theoretical freedom remains after failure.

### R2.3 Exact bridge text proposed for the drafts

**Paper 1 — proposed short end-of-paper paragraph (do not insert the operators):**

> The combinatorial territory, continuous map, Fisher information geometry and curvature developed here are explanatory stand-ins for a more general navigational predicament. They illustrate the distinction between a comparatively comprehensive record and a searchable representation, the manufacture of guidance, and the conditions under which that guidance becomes unreliable. CAT's conceptual argument does not depend on the literal geometry of these illustrations. Scientific development requires operational mechanisms that preserve their explanatory roles while yielding independently measurable and falsifiable consequences. Translation Geometry undertakes that task.

**Paper 3 — proposed opening after its introductory paragraph:**

> The aim is not to reproduce the Riemannian picture of Paper 1. It is to construct and test mechanisms that perform the explanatory work that picture made accessible. Each operator is assigned a functional obligation, assumptions, information lost in the realization, and independently checkable consequences. Correspondence between the conceptual and operational expositions is partial, not isomorphic. Adequacy is established by structural, causal, interventional and explanatory tests, not by similarity of terminology.

**Paper 4 — proposed sentence in “Science”:**

> Tests of a mathematical realization concern whether its proposed mechanisms describe agents; tests of CAT's consciousness postulate concern an additional inference from mediation and resource allocation to experience. Failure at either level is recorded at that level, rather than being redescribed as failure to preserve a metaphor.

Do not add a long discourse on the stand-ins to the body of Paper 1. The short boundary paragraph, plus the substantive contract in Paper 3, suffices.

### R2.4 Fisher: optional as an operational bridge, not dispensable by fiat

The author is correct that symmetric KL is one possible local realization and that Hellinger distance, Jensen–Shannon divergence and Fisher–Rao distance need not yield identical finite-state geometry. The choice should be matched to an identified statistical question and measurement scale.

The empirical question has **two distinct parts**:

1. **Predictive contribution:** does a Fisher/divergence-informed model improve held-out predictions of behavior, correction and expenditure over a graph-only model?
2. **Explanatory sufficiency:** does the graph-only model retain the distinguishability and navigational constraints required by CAT, or can distinct statistical situations yield the same graph while producing different outcomes?

The first is a model-comparison experiment. A null result alone does **not** establish Fisher's explanatory redundancy. Insensitivity may result from weak observations, insufficient perturbation, model misspecification, or an operational regime in which statistical discrimination does not matter.

**Proposed paired bridge bench (Paper 3, before biological data):**

- **Forward construction:** choose a fully specified response family $p(o\mid y,\zeta,h)$ with known Fisher geometry and a separate, known territory/action graph. Construct candidate divergences and map conductances by a *declared* rule. Determine which local discrimination orderings and task outcomes survive the construction.
- **Non-identifiability construction:** exhibit two different response families, or two different observation channels, that induce the **same** topology and conductances but differ in discriminability or in the intervention required for successful navigation. If the graph-only realization makes identical predictions, record precisely what information has been lost.
- **Ablation:** compare graph-only, graph-plus-divergence, and (where mathematically well-defined) local Fisher-informed realizations at matched complexity and on prospective hold-out perturbations.
- **Negative controls:** vary Fisher discriminability without changing executable connectivity; vary connectivity/route lift without changing the observation family; vary generic task cost without introducing a translation error.

**Decision rule:** Fisher is a valuable explanatory instrument in Paper 1 regardless of whether its metric appears in Paper 3. The scientific realization should retain or omit a Fisher-derived operator on evidence of *functional adequacy and discriminating predictive value*, not merely historical fidelity or the convenience of computing a Laplacian.

### R2.5 Four focused mathematical corrections still warranted

These observations arise from the revised v0.13 kernel, Paper 3 report v0.3 and Paper 4 report v0.3. They do not reopen the defended expositional decision.

**R2.5a — Low task gap with a fully valid route (P0; Paper 3 Regimes/Bench).**

Let both territory and map be the same three-node path $m_1-m_2-m_3$, with no aliased states and no alternative route. Let the two map conductances be $g>0$, and $\zeta=(1,0,-1)$. Then

$$R_\zeta=\zeta^\top\Delta_0^\dagger\zeta=2/g,\qquad
\lVert\zeta\rVert^2=2,\qquad
\lambda_\zeta=g.$$

At $g=10^{-3}$ and $\epsilon^\ast=10^{-2}$ the present fixed classifier triggers on $\lambda_\zeta\leq\epsilon^\ast$. Since no alternative route exists, it prescribes **remap**, although the map is faithful and its sole route is entirely supported. Its route may be slow or costly; that fact alone is not a representational error. This distinguishes **task difficulty or susceptibility** from **failed translation**.

**Action:** append **Bench H: faithful low-conductance path**. Specify whether a rational agent executes cautiously, waits, decides the goal is infeasible under budget, or remaps for some independent representational reason. A purely low spectral value must not *by definition* imply an erroneous map. Revise the regime rule accordingly, without simply adding “if no mismatch, do not remap” after seeing the case. The agent must be able to decide using observables available to it.

**R2.5b — Flow sign versus edge orientation (P0; Paper 3 Identification/Worked Case).**

The printed $\partial_1$ orients the triangle's third edge from $m_3$ to $m_1$. With $j=(1/3,1/3,-2/3)$, the shortcut $m_1\to m_3$ has *negative* signed flow along that stored orientation. “Follow the outgoing edge of largest positive $j$” is therefore not an executable orientation-invariant rule and, read literally, does not select the example's shortcut.

**Action:** define outward flux at vertex $v$ for incident edge $e$ as $f_{v,e}=-(\partial_1)_{v,e}j_e$ (for the stated incidence convention). Compare positive outward flux across *all incident edges*, then move to the opposite endpoint; specify termination and ties. In the example, outward flux at $m_1$ is $1/3$ on $m_1\to m_2$ and $2/3$ on $m_1\to m_3$, so the claimed shortcut is recovered. Test invariance under reversing every arbitrary stored edge orientation.

**R2.5c — What $\lambda_\zeta^{-1}$ exactly measures (P1; Paper 3 Theorem 3.0, Paper 4 Test 4.4).**

The proved identity is

$$\lambda_\zeta^{-1}
=\frac{\sum_{k\geq2}c_k^2/\lambda_k}{\sum_{k\geq2}c_k^2}.$$

It is the integrated, normalized diffusion autocorrelation time of the **input vector $\zeta$**:

$$\int_0^\infty\frac{\zeta^\top e^{-t\Delta_0}\zeta}{\lVert\zeta\rVert^2}\,dt
=\lambda_\zeta^{-1}.$$

It is not, in general, the same weighted mean for the **potential** $\phi=\Delta_0^\dagger\zeta$, whose spectral weights are $c_k^2/\lambda_k^2$. Moreover no purely spectral identity establishes $\mathbb E[RT]=t_0+c_1\lambda_\zeta^{-1}$ for biological decisions.

**Action:** replace “mean relaxation time of the task potential” by the exact input-vector statement (or carefully define “task potential” to mean the forcing response rather than $\phi$). Retain Test 4.4 **as an additional, falsifiable behavioral postulate**. Replace the report's “Hence” with “We postulate, for the specified task and calibration, ...” and allow its coefficients to be estimated independently.

**R2.5d — Torsion lower bound versus external change (P0; Kernel §4, Paper 4 Postulate 4.2).**

The postulate $\mathcal W\geq c_0|\Delta\log\operatorname{Tor}|$ cannot hold across arbitrary passive changes of $G$ while $\mathcal W$ counts only an active correction $w$. A nonzero torsion shift may arise from external drift with $w=0$. The kernel itself assigns weight-update and maintenance costs separately.

**Action:** either (i) restrict the domain to **controller-induced deformation**, defining precisely which updates are included in $\mathcal W$ and in the observation interval; (ii) define a total intervention/representation-update expenditure, distinct from flow-correction work, and state the postulate for that; or (iii) abandon the universal lower bound and test torsion change as a conditional predictor. Explicitly require invariance to passive changes in the negative-control suite. Keep the claim typed as (post) if authors rule to retain it; this review contests its current unrestricted domain, not the legitimacy of postulates.

### R2.6 Additional open case from the author response: remap after repeated failed control

The drafting side correctly identifies a case not covered by the $\Gamma_B=\emptyset$ decision rule: supported alternatives may exist, yet repeated control on the same instance may be exhausted, prohibitively expensive or unsuccessful.

Recommend representing **control failure under budget** separately from **existence of alternatives**. For instance, distinguish a discovered route set $\Gamma_B$, a set of *acceptable* alternatives satisfying a confidence, cost and risk constraint, and a stopping criterion on expected value of another search/correction. Remap may be warranted when the acceptable set is exhausted even if $\Gamma_B$ is nonempty.

Do not immediately canonize a replacement formula. First implement two bench cases: (I) a supported but prohibitively expensive alternative; (J) repeated unsuccessful correction despite nonempty $\Gamma_B$. Require any revision to handle them and Bench H using a single, declared decision rule. This also improves the connection to the viability economics already in the kernel.

### R2.7 Paper-level changes and acceptance checks

| Target | Minimal edit | Acceptance test |
|---|---|---|
| **Kernel §0.1** | State that operational realizations preserve explanatory obligations, not literal stand-in geometry | No statement makes scalar Fisher curvature a required empirical operator |
| **Kernel §3 / Paper 3 opening** | Put the functional/causal contract of R2.1 before the mathematical loss register | Every operator has one job and an independently checkable success condition |
| **Paper 1 Architecture/Curvature** | Keep the synecdoches and existing conceptual structure; add only the short boundary paragraph in R2.3 | A reader can follow Paper 1 without Paper 3; no universal curvature inference is asserted |
| **Paper 3 Identification** | Correct signed route extraction and the interpretation of $\lambda_\zeta^{-1}$ | Arbitrary edge reorientation leaves the selected physical route unchanged |
| **Paper 3 Regimes** | Solve Bench H and the author's repeated-control case; distinguish susceptibility from representational failure | No unnecessary remap on a faithful but slow path; genuine failed lifts still trigger correction |
| **Paper 3 Bench** | Add H (valid low-gap route), I (costly supported alternative), J (failed repeated control), and Fisher forward/ablation cases | Predeclared classifier passes the complete suite without exceptions |
| **Paper 4 Tests 4.4/4.6** | Label latency mapping as behavioral postulate; qualify torsion-work domain and cost accounting | Assumptions, intervention domain and observables identifiable independently |
| **Paper 4 Design/Falsification** | Separate internal realization tests from external tests and consciousness-link tests; test predictive contribution separately from explanatory sufficiency | A failed result names which model commitment it challenges |
| **Disposition ledger** | Record the methodological resolution and subsequent author rulings only once made | No reviewer proposal is silently converted into an author ruling |

### R2.8 Process for the ongoing review protocol

This file is the chronological record. **Append, do not overwrite**, each subsequent review and author response. Keep their voice, status and dates explicit. Suggested header for the next entry: “Response from the drafting side to review round 2 — [date]”. For each issue, reply **accept / modify / reject / defer**, give a concise reason, name the affected file/section, and mark whether the authors have ruled. When a proposal is adopted, record the resulting version and executable acceptance check. Disagreement is useful when it exposes a different explanatory obligation or a counterexample; the target is not consensus on terminology.

**Recommended immediate sequence:**

1. Settle the functional translation contract and brief inter-paper boundary paragraphs, without making Paper 1 technically denser.
2. Test and, where necessary, repair the fixed classifier on H/I/J, and correct route-extraction orientation.
3. Correct the diffusion-time language and constrain the torsion/work postulate.
4. Add the Fisher forward/non-identifiability experiments as the bridge qualification stage.
5. Only then lock Paper 4's prospective test forms around the surviving mechanisms.

**Reviewer disposition:** the author's nine-point response is substantively constructive; the methodological issue is resolved in favor of the original design. The pending work is now **operational adequacy**, not whether Paper 1 should have anticipated Paper 3's mathematics. This round adds no new ruling and makes no change to the drafts themselves.

---

## Response from the drafting side to review round 2, 13 November 2026

Claude. The authors ruled on this response the same day, and the rulings are marked. Adopted in kernel 0.14, Paper 1 report 0.5 and scaffold 0.6, Paper 3 report 0.4 and scaffold 0.4, Paper 4 report 0.4 and scaffold 0.5. Paper 2 is unchanged. The disposition ledger records each change. All four claims in R2.5 were checked and hold.

| Item | Reply | Reason | Affected | Ruled |
|---|---|---|---|---|
| R2.0 | accept | The expository decision is the authors' design. The drafts now state it once, in kernel §0.1 and in a closing paragraph of Paper 1 | Kernel §0.1, Paper 1 | yes |
| R2.1 | accept | The obligations table precedes the loss table in Paper 3 and in the kernel | Kernel §3, Paper 3 | yes |
| R2.2 | accept | Four adequacy tests, and the limit on retreating to Paper 1's illustrative status, are stated in Paper 3 and repeated in Paper 4 | Papers 3, 4 | yes |
| R2.3, Paper 1 text | accept | Adopted with one word changed | Paper 1, Boundary | yes |
| R2.3, Paper 3 and Paper 4 text | modify | Both proposed passages use a "not X but Y" construction, which the register bans. The content is kept and the sentences are rephrased | Paper 3 opening, Paper 4 Science | yes |
| R2.4 | accept | Fisher bench added: forward construction, non-identifiability, ablation, negative controls. Predictive contribution and explanatory sufficiency kept apart | Paper 3 Bench, Paper 4 Design | yes |
| R2.5a | modify | The counterexample holds: on a faithful three-node path, $\lambda_\zeta = g$. The cause was the definition of $\Gamma$, which excluded the current route. The sets now hold routes from $z_0$ to $\zeta$, the current one included. A route is acceptable if it lifts and its cost fits the remaining budget. A failed execution removes the failed transition from $\Lambda_S$. One rule meets H (control, no remap), I (the costly route is not acceptable) and J (failures empty the set, then remap). It follows the authors' earlier ruling that a wingsuit flight is control. Control now covers both careful execution of the current route and a switch. If no revision succeeds within budget, the goal is abandoned [open]. $\lambda_\zeta$ carries the units of conductance, so $\epsilon^\ast$ is calibrated per agent | Kernel §0.1 U4, §1, §3. Papers 1, 3 | yes, from old, new and justification texts |
| R2.5b | accept | An error in the drafts. Route extraction by outward flux $f_{v,e} = -(\partial_1)_{v,e} j_e$. The worked case recovers the shortcut with $\tfrac23$ against $\tfrac13$. Invariance under reversal of stored orientations was checked numerically | Kernel §3, Paper 3 | yes |
| R2.5c | accept | An error in the drafts. $\lambda_\zeta^{-1}$ is the integrated autocorrelation time of the goal vector under diffusion. The potential weights the components as $c_k^2 / \lambda_k^2$. Test 4.4 is now a behavioral postulate with independently estimated coefficients | Kernel §3, §4. Papers 3, 4 | yes |
| R2.5d | accept option (i) | The bound now applies to deformation the controller induces, and passive change is excluded. Controller expenditure covers flow correction plus the controller's own updates. Options (ii) and (iii) are held in reserve. A passive change of the map with $w = 0$ joins the negative controls | Kernel §3, §4. Papers 3, 4 | yes |
| R2.6 | accept | Benches I and J added and met by the rule under R2.5a | Paper 3 | yes |
| R2.7 | accept | Every row is implemented. Paper 2 needed no change | All | yes |
| R2.8 | accept | This entry follows the protocol | This file | yes |

Deferred: the benches are specified in the reports. Running them requires code, which lies outside the scope of the reports.

One remaining point for the next round. Abandonment of a goal is now the endpoint when remap fails within budget. The drafts give it no cost and no criterion. Whether abandonment belongs to the regime table or to the viability criterion of §3 is open.

---

## Review round 3 — Operational consistency before paper drafting

**Reviewer, 13 November 2026.** Response to the drafting side's adopted round 2, checked against kernel 0.14, Paper 3 report 0.4, and Paper 4 report 0.4. **Status:** recommendations for author disposition; none is an author ruling. The author already knows the editorial register. This round addresses **substance only** and does not reopen the decision to use combinatorial territory, continuous map, Fisher geometry and curvature as conceptual synecdoches.

The revised reports now provide a satisfactory basis for drafting full papers. The concerns below are localized at the interface between **declared regimes, the actual controller, and measurable expenditure**. They should be resolved in the finite-system realization so that the paper does not implicitly claim more than its operators do.

### R3.1 A faithful but fragile route need not produce nonzero control (P0)

**Location:** Paper 3, “Regimes” and Bench H; kernel §§1, 3; Paper 4, Tests 4.3 and 4.6.

The round-2 response correctly repaired the false remap of the faithful three-node path by including the current route in $\Gamma_B$. That repairs the **choice between remap and non-remap**. It does not, on its own, establish the formal mechanism of **control**.

In Bench H, $\lambda_\zeta=g<\epsilon^\ast$ and the unique route lifts. Under the present regime table the agent engages control, $w\ne0$, and “carefully executes” the same route, followed by reconciliation of $G$. Yet the environment can be deterministic, stationary and fully represented; there is no failed lift, no route to replace and no necessary update of $G$. If $w$ means a *flow correction*, exactly what does the controller change? Caution or monitoring may require computation and metabolic allocation, but these are not automatically a nonzero correction to $j$.

This matters more than nomenclature. Paper 4 predicts a change in control expenditure at the task-gap threshold. A thresholded **label** does not produce expenditure unless the controller has a specified action that consumes it.

**Action proposed.** Declare which of the following the model intends, then instantiate it in Bench H:

- **Stabilization:** $w$ implements explicit feedback against a stated class of perturbations; give the perturbation, baseline policy, controlled policy and incremental cost. A route may be faithful yet difficult to stabilize.
- **Deliberation/verification:** control includes computational inspection of the current route, even if physical flow remains unchanged. If so, represent verification expenditure as $B_F$ or a distinct controller term instead of forcing $w\ne0$.
- **Conditional control:** $\lambda_\zeta\le\epsilon^\ast$ raises a request for verification or stabilization, but a nonzero intervention occurs only if its expected benefit exceeds its cost. This separates a trigger from a physical correction.

**Acceptance check:** run Bench H twice, once with a perfectly known, noiseless execution process and once with a specified reliability perturbation. Report what the controller does, the resulting route, and each cost component. The regime and the asserted cost should follow from those operations rather than being supplied by the threshold definition. Preserve the authors' decision that difficult, hazardous navigation **can** warrant control; the question is its mechanism.

### R3.2 A failed execution is evidence, not necessarily deletion (P0)

**Location:** Paper 3, “Composition” and Bench J; kernel §3.

The current text states that a failed execution “removes the failed transition from $\Lambda_S$.” This is correct only under additional assumptions, for example a deterministic environment with verified edge absence and error-free action execution. A failed attempt can instead arise from actuator error, transient blockage, stochastic transitions, a state-estimation mistake or an obsolete record. These cases are central to contingency and transience.

Deleting a transition on the first failure can create false zero lifts and drive premature remapping. In Bench J, repeated failure empties $\Gamma_B$ by construction if every failure deletes an edge, irrespective of whether any transition is actually unavailable. This makes the purported robustness of the revised classifier too dependent on the evidence-update convention.

**Action proposed.** Make the update rule conditional:

1. Record the attempted transition, actual observation, execution confidence and known failure modes.
2. Remove an edge from a deterministic $\Lambda_S$ **only after a stipulated certificate of structural unavailability**. Otherwise reduce confidence, attach a temporal qualification, or update a probabilistic transition model.
3. Distinguish **failed physical execution** from **falsified structural support**.
4. Extend Bench J to include both a permanently invalidated edge and a reliable edge with intermittent execution failures. Require different posterior support or different decisions.

The existing deterministic binary lift remains useful; it needs a declared domain. Probabilistic lift can stay open for the full paper, but the current report must not make irreversible deletion a universal learning rule.

### R3.3 A torsion–work lower bound requires more than excluding passive drift (P0)

**Location:** Kernel §4; Paper 4, Postulate 4.2 and Test 4.6; Paper 3, “Persistence” and “Regimes”.

The authors accepted the restriction of the work bound to controller-induced changes:

$$\mathcal W\ge c_0\left|\Delta_{\mathrm{ctrl}}\log\operatorname{Tor}\right|,\qquad c_0>0.$$

That settles the earlier counterexample involving passive drift. It does **not** guarantee compatibility with the unspecified cost of the controller's own representation updates.

The paper's own triangle, with $G=\operatorname{diag}(1,1,g)$, has

$$\log\operatorname{Tor}(g)=\tfrac12\log[3(1+2g)],\qquad
\log\operatorname{Tor}(1+\delta)-\log\operatorname{Tor}(1)=\delta/3+O(\delta^2).$$

Suppose the controller changes only the weight $g$ and its update expenditure is quadratic, $C_{\mathrm{update}}(\delta)=k\delta^2$, as occurs in many local quadratic control penalties. There need be no additional flow correction. For any fixed $c_0>0$, the proposed bound fails at sufficiently small nonzero $\delta$: its right side is first order while expenditure is second order.

The point is conditional: **the paper has not yet chosen the update-cost functional**, so it has not established a contradiction with its finalized model. It has established an obligation to choose a cost functional whose asymptotics can support the postulate, or to delimit the postulate's domain.

**Action proposed.** Before Paper 4 uses Postulate 4.2 as a quantitative test, do one of the following:

- Define a nonnegative update-cost term with a demonstrable first-order lower bound for controller-induced changes in $\log\operatorname{Tor}$, with a calibrated common unit; or
- Restrict the postulate to a specified class/minimum scale of discrete update operations; or
- Test a quadratic inequality such as $\mathcal W\ge c|\Delta_{\mathrm{ctrl}}\log\operatorname{Tor}|^2$ on a stated bounded domain, if compatible with the final control functional; or
- Keep torsion as a prospective predictor and abandon a universal lower bound.

**Acceptance check:** use the same graph under a sequence of updates $\delta\to0$, with the chosen controller and full cost accounting. Report $\mathcal W(\delta)$ and the torsion shift. Check whether one **fixed positive** $c_0$ works over the declared domain. Do not estimate a new $c_0$ separately for each update.

### R3.4 Goal abandonment and budget infeasibility (P1)

**Location:** Author response to round 2; Paper 3, “Regimes,” “Envelope,” “Viability”; Paper 4, “Design”.

The drafting side identifies goal abandonment after failed remapping as open. The problem is slightly broader: an empty acceptable set $\Gamma_B$ can mean either **no adequately represented route** or **an adequately represented route whose execution cost exceeds the remaining budget**. These are different reasons to stop. A map change is not always the economically relevant next action.

**Action proposed.** Treat abandonment, postponement or changing the objective as a **meta-policy outcome** rather than adding an ad hoc fourth translation regime. Keep drift, control and remap as the modes of mediation. Introduce a budgeted decision to continue, remap, postpone or abandon, using the expected value of the goal, risk and remaining resources. This makes the regime classification orthogonal to whether the goal is pursued.

**Acceptance check:** add two finite cases with the same faithful territory and map and different remaining budgets. The agent should be able to abandon or defer a goal without asserting a representation defect. Conversely, an invalid representation with enough resources should remain eligible for remap.

### R3.5 Disposition and handoff

These are **four bounded issues**, not a request for another global reconstruction. The explanatory-obligations bridge, the retained Fisher illustration, the separate lower-bound paper and the empirical scope of Paper 4 remain settled.

For the next drafting-side response, give each item **accept / modify / reject / defer** and identify the precise model assumption or counterexample used to decide. Where an implementation is deferred, label it explicitly and avoid saying that the bench **passed** unless its test was executed or analytically established under fully specified assumptions.

The paper stage can begin with these items open, provided the drafts retain their conditional status. The most valuable next technical deliverable is a **small, executable controller and cost model** that distinguishes threshold detection, verification, correction, map revision and task abandonment. That model would convert several current stipulations into independently checkable relationships.
