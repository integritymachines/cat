# Translation Geometry: Scaffold

Version 0.4, 13 November 2026. Kernel: `0_LSMN_kernel.md` §3. The research note for Paper 3 is the yardstick. Changes since 0.2 adopt rounds 1 and 2 of the review protocol under the authors' rulings. Each bullet carries a claim type: (def), (thm), (post), (hyp), (ill).

Headline. Papers 1 and 2 explain the theory with synecdoches. This paper constructs computable candidates for the mechanisms they explain: manufactured direction, task sensitivity, the virtual test of a route, distortion and deformation. The correspondence is partial and lossy, and the paper states what is lost.

Status. Scientific. Definitions, theorems, postulates, one computed example and a bench. No neuroscience. Empirical models belong to Paper 4.

## 1. Introduction

- Papers 1 and 2 argue with synecdoches. This paper constructs and tests mechanisms that do the explanatory work of the Riemannian picture.
- Obligations (def): each candidate, its explanatory obligation, and the evidence that the obligation is met.
- Adequacy (def): structural, causal, interventional, economy. One failed realization does not refute the architecture. Repeated failures force its revision.
- The translation contract: each stand-in, its candidate, what is kept, what is lost.
- Compression is performed by $\pi$. Fisher illustrates discriminability within the map.
- Fisher information stays. One bridge is offered and the rest is declared unestimated. Whether the bridge adds predictive power is tested in Paper 4.
- The operators are unified by their roles along the chain. No scalar summary statistic is assumed.

## 2. Two Complexes

- Territory $K_S$ (def): relations only, no task-given potential, not globally ranked, normalized sampling measure.
- Map $K_M$ (def): weights, potential, flow.
- Compression (def): surjective, non-injective. Quotienting can create map edges with no territory transition.
- Metrics (def): symmetrized shortest path on $K_S$, edge length $G_e^{-1}$ on $K_M$.
- Bridge to Fisher (def, optional): symmetrized divergence between predicted observation distributions. Setting weights from it is a modeling choice (post).
- Weighted convention (def): one edge inner product for all degrees.

## 3. Identification

- Potential and flow from a goal vector. Proposition 3.1 (thm).
- Route extraction by outward flux (def). Independent of stored edge orientation.
- Task-conditioned gap $\lambda_\zeta$ (def). Theorem 3.0: $\lambda_2$ is its minimum over goals, and $\lambda_\zeta^{-1}$ is the integrated autocorrelation time of the goal vector under diffusion (thm). It is not the relaxation time of the potential. It carries the units of conductance.
- Two clusters with a weak bridge: small $\lambda_2$, large $\lambda_\zeta$ inside a cluster.
- Answers opacity.

## 4. Composition

- Hodge decomposition of route chains under the weighted convention (thm). The scaled flow is a pure gradient.
- A harmonic cycle is a feature of the map and no contradiction by itself.
- Lift functional (def). Positive lift: one compatible path in the recorded territory, no more.
- Three sets of routes, the current one included: supported by the landscape, supported by the territory, acceptable and found within budget (def). A failed execution removes the failed transition from the territory.
- Probabilistic lift for stochastic execution [open].
- Answers contingency.

## 5. Persistence

- Combinatorial torsion under the weighted convention (def). Variation at constant rank, Proposition 3.4 (thm).
- Deletion against a weight tending to zero.
- Torsion is a signed observable of deformation, not control work [ruled]. No energetic bound follows.
- Anchored squared distortion (def). Squared transport discrepancy for unregistered maps (def). Distances are square roots.
- Answers transience.

## 6. Regimes

- Rule fixed before data (def). Trigger: zero lift of the extracted route, or task gap at or below its critical level.
- Control when an acceptable supported route is found within budget, the current one included: careful execution or a switch. Remap when none is (hyp). Abandonment of the goal if no revision succeeds [open].
- No regime rests on $\lambda_2$ alone [ruled].
- The threshold is a policy rule (post). No spectral bifurcation is claimed.
- Controller expenditure, candidate (post) [inference]: flow correction plus the controller's own updates. Maintenance and passive change excluded.
- Confidence (note).

## 7. Envelope

- The pairs of start and goal with a nonempty set of acceptable routes found within budget (def). Includes drift and control [ruled].
- Remap lies outside and can enlarge it.

## 8. Viability

- Ex ante criterion against physical testing, over a stated horizon, in common units (def).
- Used by the separate paper on the lower bound. Not a theorem about consciousness.

## 9. Propositions

- Lemma 3.2, fixed-policy failure (thm), formerly control-work necessity. The link to consciousness is Postulate 1.0 of Paper 1.
- Proposition 3.3, perspective asymmetry: (thm) zero discrepancy iff isomorphic. (post) distinct parochial samplings generically give non-isomorphic maps.
- Outside the series [ruled]: the impossibility and partition theorems of the note.

## 10. Worked Case

- Matrices listed. Flow, extracted route, both gaps, lift failure of the shortcut, control.
- Reweighting: torsion shift $-\tfrac12 \ln 3$ at constant $\beta_1$.
- Deletion: $\beta_1$ falls to zero.
- Distortion: global unchanged at $\tfrac{22}{16}$, local falls to zero.
- Splitting as remap. Three operations kept distinct.

## 11. Bench

- Ten cases, A to J, with required results (def). H: a faithful but slow path is not remapped. I: a costly supported route is not acceptable. J: repeated failure empties the set, then remap.
- Fisher bench: forward construction, non-identifiability, ablation, negative controls. Predictive contribution and explanatory sufficiency are separate questions.

## 12. Open Points and Conclusion

- Controller expenditure, abandonment of the goal, reconciliation, $\epsilon^\ast$ against $\kappa^\ast$, probabilistic lift, confidence, conditions for Proposition 3.3.
- Exploratory: determinant-line geometry (note).
- Hands over to Paper 4.
