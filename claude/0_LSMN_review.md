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
