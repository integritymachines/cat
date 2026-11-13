# LSMN Kernel

Version 0.13, 13 November 2026. One kernel for Papers 1 to 4. Baseline: the 2025 Papers 1 and 2 and the research notes for Papers 3 and 4. Changes since 0.12 adopt the review of 13 November (`0_LSMN_review.md`) under the authors' rulings.

Provenance tags. [ruled]: decided by the authors. [inference]: proposed here, not ruled. [open]: form not fixed. Numbers taken from the notes are unchecked.

Claim types [ruled]. (def) definition. (thm) theorem, with its assumptions. (post) modeling postulate: an element of the model, subject to empirical test. (hyp) empirical hypothesis, to be confirmed. (ill) illustration: a synecdoche or picture that explains a concept and makes no general claim.

Rule: one meaning per symbol. Every symbol is in the registry. Regimes, results and tests carry words or section numbers, never single letters.

## 0. Registry

| Symbol | Meaning |
|---|---|
| $\mathcal{L}, \mathcal{S}, \mathcal{M}, \mathcal{N}$ | Landscape (unsurveyable reality), Territory, Map, Navigation |
| $\sigma, \pi, \gamma$ | sampling $\mathcal{L} \to \mathcal{S}$, compression $\mathcal{S} \to \mathcal{M}$, policy trajectory $\mathcal{M} \to \mathcal{N}$ |
| $K_S, V_S, z, \Lambda_S, \operatorname{dist}_S, \mu_S$ | Territory: complex, vertex set, vertex, adjacency matrix, metric, sampling measure |
| $K_M, V_M, m, E_M, e, G, \partial_1, \partial_2, \operatorname{dist}_M$ | Map: complex, vertex set, vertex, edge set, edge, edge weights, boundary operators, metric |
| $\tilde{\partial}_1, \tilde{\partial}_2$ | weighted boundary operators $\partial_1 G^{1/2}$, $G^{-1/2} \partial_2$ |
| $\Delta_i, \lambda_2, \beta_1$ | weighted Hodge Laplacian of degree $i$, second eigenvalue of $\Delta_0$, $\dim \ker \Delta_1$ |
| $\lambda_\zeta$ | task-conditioned gap $\lVert \zeta \rVert^2 / (\zeta^\top \Delta_0^\dagger \zeta)$ |
| $P_m, \mathbf{1}_m, \mathbf{1}$ | projector onto $\pi^{-1}(m)$, indicator vector, all-ones vector |
| $\zeta, \phi, j, \gamma_j$ | goal vector, potential, manufactured flow, route extracted from $j$ |
| $u, v, h$ | Hodge components of an edge chain: gradient, rotational, harmonic |
| $\operatorname{lift}$ | lift functional |
| $\Gamma_{\mathcal{L}}, \Gamma_{\mathcal{S}}, \Gamma_B$ | alternatives to a route supported by $\mathcal{L}$, by $\mathcal{S}$, found within budget |
| $U, I, N$ | Unsurveyability, Intractability, Intransigence |
| $O, C, T$ | Opacity, Contingency, Transience |
| $R, F, D$ | relations, functions, dynamics |
| $\operatorname{sig}$ | structural signature in $\{0,1\}^3$ |
| $o, c, \vartheta$ | degrees of $O$, $C$, $T$ |
| $\nu, \alpha$ | count of relevant distinctions, scale |
| $y, g_F, p(\cdot \mid y), \operatorname{Ric}$ | smooth stand-in: point of $\mathcal{M}$, Fisher metric, predicted observation distribution, Ricci curvature |
| $D_{\mathrm{sym}}(m, n)$ | symmetrized divergence between $p(\cdot \mid m)$ and $p(\cdot \mid n)$ |
| $\kappa, \kappa^\ast$ | curvature, its critical level (Papers 1 and 2) |
| $\epsilon^\ast, t_{\mathrm{rel}}$ | critical level of the gap (Papers 3 and 4), relaxation time |
| $w, \mathcal{W}, \Theta$ | control field, control work over an interval, matched interval |
| $a, a_{\mathrm{base}}, \Delta a_e, B$ | metabolic power allocated to mediation, its waking baseline, its surge at instance $e$, budget |
| $\eta$ | conversion efficiency |
| $\operatorname{reg}$ | regime: drift, control or remap |
| $\mathcal{E}$ | envelope of assured navigation, certified within budget |
| $\operatorname{Tor}$ | combinatorial torsion of $K_M$ |
| $d_{\mathcal{SM}}, d_{\mathrm{GW}}$ | anchored squared distortion, squared transport discrepancy |
| $X, x_t, k, \operatorname{val}, \operatorname{Nbr}, \Omega_t$ | search space, state, number of options, objective, neighborhood, options reachable |
| $B_R, B_F, B_D, B_w, B_0$ | budgets: guidance, virtual search, physical execution, reconciliation, maintenance |
| $\ell, \ell_C, \ell_T$ | loss from a failed physical test, expected loss from $C$, from $T$ |
| $\operatorname{err}_i, \operatorname{amp}_i, \xi_i$ | misalignment after step $i$, its amplification, new disturbance |
| $\kappa_e, L_{\mathrm{decay}}, \delta g$ | curvature at instance $e$, external change, metric shift |
| $c_0, c_1, t_0$ | positive constants |
| $\delta_{\mathrm{lo}}, \delta_{\mathrm{hi}}, \delta^\ast$ | band of offline deformation (§6), critical discrepancy between agents |
| $\operatorname{bnd}, \operatorname{PR}$ | decision boundary, participation ratio |
| $\hat{\ }$, $t$ | estimator, time |

Notation against the sources: $\pi$ for the 2025 $\phi$, $\phi$ for $V$, $w$ for $U$, $\mathcal{W}$ for $\mathcal{C}_U$, $\kappa$ for $K$, $y$ for $x$, $G$ for $W$, $\partial_1$ for $B_1$, $\zeta$ for $b$, $\Lambda_S$ for $A_S$, $B_w$ for $B_C$, $\epsilon^\ast$ for $\epsilon_c$, $\kappa^\ast$ for $\kappa_c$, $\delta^\ast$ for $\delta_c$. The changes remove collisions.

## 0.1 Chain

$$\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}, \qquad U = I + N, \quad N = (O, C, T)$$

The sum is symbolic. It names a decomposition and defines no aggregate.

Yardstick: the 2025 papers. Their argument and its order stand:

$$I \to \text{compression} \to O + C + T \to \text{high } \kappa \to \text{control} \to \text{consciousness}$$

Updates to the 2025 papers [ruled], numbered for reference in the scaffolds.
1. Chain of four stages. $\mathcal{S}$ is the agent's own model, sampled parochially.
2. Headline: to navigate an unsurveyable reality, a cognitive agent maintains, and mediates between, two models, one comprehensive ($\mathcal{S}$) and one comprehensible ($\mathcal{M}$). Consciousness arises out of that mediation and the need to allocate metabolic resources to keep the two aligned.
3. Consciousness is graded and present throughout wake: a baseline plus surges.
4. Control and remap are separated by whether a supported alternative is found within budget (hyp).
5. The hard problem is not dissolved.
6. Papers 1 and 2 develop conceptual synecdoches as stand-ins. Paper 3 supplies computable candidates for the mechanisms they explain. The correspondence is partial and lossy, and Paper 3 states what is lost.
7. $\mathcal{E}$ includes control. Current LLMs are below the bound.
8. The prose tropes of the 2025 text are removed.

Background. Virtual testing of routes (Popper) belongs to control (§1) and to $C$ (§2). The conjecturing engine, motility, the lower bound and dreaming as offline conjecturing are the subject of a separate paper (§6) and have no place in Paper 4 [ruled].

Combinatorial and continuous (ill). The central synecdoche of Papers 1 and 2. The territory is combinatorial, the map is continuous. Paper 3 gives candidates: $K_S$ (relations only) and $K_M$ (weights, potential, flow). Footnote level: reality is mixed combinatorial, and the part with aligned local and global gradients needs no translation.

## 1. CAT

**Translation problem.** $I \iff \lim_{\alpha \to \infty} \log \nu(\mathcal{S}_\alpha) / \dim \mathcal{M} = \infty$, with $\dim \mathcal{M}$ counted at finite precision. $O$: no local signal with an assured relation to the global path. $C$: steps foreclose options. $T$: reality and map drift apart in time. Stated in full in §2. Paper 1 restates them without reference to Paper 2.

**Architecture.** $\mathcal{S}$ (def): accumulation of impressions, not globally ranked, sampled with measure $\mu_S$ concentrated around habitats, comprehensive. $\mathcal{M} = \pi(\mathcal{S})$, $\pi$ non-injective: a rank offering of the available choices by their connection to $\zeta$, comprehensible.

Fisher metric (def). $p(\cdot \mid y)$ is the distribution of observations that the map predicts at state $y$, conditioned on the goal and the habitat. Regularity and identifiability are assumed. Where $g_F$ is singular, the identifiable subspace is used.

$$g_F(y)_{ik} = \mathbb{E}\big[\partial_i \log p(\cdot \mid y)\, \partial_k \log p(\cdot \mid y)\big], \qquad \mathrm{KL}\big(p(\cdot \mid y) \,\Vert\, p(\cdot \mid y + \delta y)\big) = \tfrac12\, \delta y^\top g_F(y)\, \delta y + o(\lVert \delta y \rVert^2)$$

$g_F$ measures local discriminability. It does not by itself measure distortion between $\mathcal{M}$ and $\mathcal{S}$ or the need for control. $\operatorname{JND}_v(y) \propto (v^\top g_F(y)\, v)^{-1/2}$ in direction $v$ (def, under a fixed criterion). Dynamics (post): $\dot{y} = -g_F^{-1} \nabla \phi(y) + w(y)$.

**Curvature (ill).** $\kappa(y)$: scalar curvature of $g_F$. In Papers 1 and 2 curvature is a synecdoche. It stands for four things that Paper 3 separates: discriminability, translation distortion, aliasing, and navigational sensitivity. None determines the others in general. A Bernoulli family has $g_F = 1/(y(1-y))$, varying discriminability and zero curvature. Within the picture, $\kappa$ is large where small moves in $\mathcal{M}$ correspond to large changes in $\mathcal{L}$ and where the continuous $\mathcal{M}$ misrepresents the combinatorial $\mathcal{S}$. $\kappa$ carries both the divergence of $\mathcal{M}$ from $\mathcal{S}$ and its consequence for navigation [ruled]. $\kappa^\ast$ is specific to the agent and balances the cost of control against the cost of error.

$C$ appears in $\mathcal{M}$ as singularities (ill). $T$ appears as decay of the metric (ill, a chosen dynamical model): $\partial_t g_F = -2 \operatorname{Ric} + L_{\mathrm{decay}}$.

**Regimes.** $\Gamma_B(\gamma)$: alternatives to $\gamma$ that reach $\zeta$ and that the agent finds within budget $B$ (def).

| $\operatorname{reg}$ | Condition | Dynamics |
|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $w \approx 0$. The agent follows $\mathcal{M}$ |
| control | $\kappa \ge \kappa^\ast$, $\Gamma_B(\gamma) \ne \emptyset$ | $w \ne 0$. Candidate routes are tried virtually before commitment (Popper: conjectures die in the agent's stead) |
| remap | $\kappa \ge \kappa^\ast$, $\Gamma_B(\gamma) = \emptyset$ | $g_F \leftarrow g_F + \delta g$. The map changes |

The 2025 paper separates control from remap by $\kappa \approx \kappa^\ast$ against $\kappa \gg \kappa^\ast$. The test on $\Gamma_B$ replaces that [ruled] (hyp). Remap is a decision under budget. It does not prove that no route exists. $\mathcal{E}$: the states from which $\zeta$ is reached under drift or control, certified within budget. Remap lies outside $\mathcal{E}$ [ruled].

**Consciousness.** $a(t)$ (def): metabolic power allocated to mediation, excluding background metabolism. $\mathcal{W}$ (def): control work over a matched interval $\Theta$.

$$a(t) = a_{\mathrm{base}}(t) + \sum_e \Delta a_e(t), \qquad \mathcal{W} = \int_\Theta \lVert w \rVert^2_{g_F}\, dt, \qquad \eta = \frac{\mathcal{W}}{\int_\Theta \sum_e \Delta a_e\, dt}$$

$\eta$ is dimensionless once both sides are expressed in energy units. The baseline maintains the live map against $T$ and is not part of $w$.

Postulate 1.0. $\text{conscious}(t) \iff a(t) > 0$. Degree at $e$: $\Delta a_e$. $a_{\mathrm{base}} > 0$ during wake. $\Delta a_e > 0 \iff \kappa_e \ge \kappa^\ast$, nondecreasing in $\kappa_e$, larger under remap than under control at equal $\kappa_e$. Rationing [inference]: $a \le B$, surges served in descending order of $\kappa_e$. Sampling [inference]: $\kappa_e$ is decreasing in $\mu_S(e)$, so habitats drift and the frontier draws allocation.

Result 1.1. Not $I$ $\Rightarrow$ no compression, no $\mathcal{M}$, no mediation, $a \equiv 0$. A perfectly rational agent needs zero models and is not conscious.
Result 1.2. Wake and $\vartheta > 0$ $\Rightarrow a \ge a_{\mathrm{base}} > 0$ with no conflict present.
Result 1.3. $\kappa_e < \kappa^\ast \Rightarrow \Delta a_e = 0$. Processing at $e$ proceeds under drift.
Result 1.4 (post). Dreamless sleep, anesthesia: no mediation, $a = 0$.
Result 1.5. Practice lowers $\kappa$ on the practiced domain and moves it from control to drift.

Why consciousness here (2025): phenomenology, signatures and functional necessity align with control at $\kappa \ge \kappa^\ast$. Addition [ruled]: a homeostat corrects against a fixed reference and tests nothing virtually. Control in the sense of the table decides between candidate routes before commitment.

**Experience.** Identifications (post), not derived. Effort: the rate $\lVert w \rVert^2_{g_F}$. Salience: information density, high where $\kappa$ is high. Meaning: criticality, $\kappa$ near $\kappa^\ast$. Intensity: $\lVert \nabla \kappa \rVert_{g_F}$ along trajectories with $w \ne 0$. Hard problem [ruled]: not dissolved. Science regularizes observations from without and can only triangulate experience within. Consciousness is a work effort, and work leaves traces observable from without. Different histories give different $\mathcal{M}$ for the same stimuli (§3, Proposition 3.3).

**Neighbors.** Free energy: the global objective, $\phi$ as free energy. Bounded rationality: satisficing stops at $\kappa^\ast$. Rate-distortion: $\kappa$ marks where distortion concentrates. Energy-based networks: temperature regulated locally by $\kappa$. Global workspace: $\kappa \to \kappa^\ast$ triggers broadcast.

**Altered states.** Changes of average $\kappa$, its variance, $\kappa^\ast$, or control capacity. Meditation: lower $\kappa$, higher $\kappa^\ast$. Psychedelics: higher variance of $\kappa$. Flow: $\kappa$ sustained near $\kappa^\ast$. Dreams: high $\kappa$ explored with actuators gated, control cheap. Anxiety: $\kappa$ overestimated. Anesthesia, dreamless sleep: no mediation.

**Implications.** Behavioral, neural, developmental and individual predictions in terms of $\kappa$ and $\kappa^\ast$ (2025). Comparative criterion, three requirements (2025): representations rich enough for compression to distort, detection of failure of the gradient, capacity for corrective control. Current LLMs fail on two counts [ruled]: no adaptive recalibration in runtime, and no parochialism ($\mu_S$ without habitats). The second makes them the nearest known case of Result 1.1. Motility plays no role in Paper 1 [ruled].

## 2. UNS

**Translation problem.** $\mathcal{S}$ alone: no task-given potential, paralysis. $\mathcal{M}$ alone: $j$ never tested, hallucination. The map proposes, the territory disposes. Parsimony (def): $\pi^\ast = \arg\min_\pi d_{\mathcal{SM}}$ subject to $\dim \mathcal{M}$ within capacity, the most faithful searchable representation.

**Intractability.** Example (ill): $X$ the orderings of $k$ interacting options, $\lvert X \rvert = k!$. $\operatorname{val}: X \to \mathbb{R}$.

$$I \iff \lim_{\alpha \to \infty} \frac{\log \nu(\mathcal{S}_\alpha)}{\dim \mathcal{M}} = \infty$$

Access (post): per step the agent evaluates only states in $\operatorname{Nbr}(x_t)$. With it, $I \Rightarrow x_{t+1} \in \operatorname{Nbr}(x_t)$: intractability forces local search [ruled]. $I$ acts at $\sigma$ (parochial sampling), at $\pi$ (lossy compression) and at $\gamma$ (a linear sequence of local steps) [ruled].

**Obstructions.**

| | Obstruction | Problem posed | Degree | Ordering | Primitive |
|---|---|---|---|---|---|
| $O$ | no local information that reliably indicates the direction of global improvement | identification: what is available in the immediate environment | $o = \tfrac12\big(1 - \operatorname{corr}(\nabla_{\mathrm{loc}} \operatorname{val}, \nabla_{\mathrm{glob}} \operatorname{val})\big) \in [0,1]$ | comes with (none) | $R$ |
| $C$ | transitions are not freely reversible | composition: how it connects to the overall objective | $c \in [0,1]$, cost of reversion | follows from (logical, negotiable) | $F$ |
| $T$ | structure changes in time, or the map decays absent maintenance | persistence: how long it will be available | $\vartheta \ge 0$ | follows after (temporal, non-negotiable) | $D$ |

$o$ (def) is computed by an experimenter who knows the global gradient. The agent does not. $o = 0$: aligned. $o = \tfrac12$: uninformative. $o > \tfrac12$: misleading. Degrees vary with the environment and within it. Any can be near zero [ruled]. Resolution of $O$: establish that the local signal correlates with the global path. For $0 < o < \tfrac12$, noise added to the choice can improve on strict following. Coupling [ruled]: $C$ binds in proportion to $o$. $T$ binds given a committed $\gamma$. Form [inference]: $\ell_C = \ell_C(o \cdot c)$, $\ell_T = \ell_T(\vartheta, \lvert \gamma \rvert)$. Completeness of $(I, O, C, T)$ is conjectured.

**Orderings.** $R$, $F$, $D$ are the mathematical primitives that capture the three orderings. The agent assigns orderings. It does not make up mathematics [ruled].

**Trajectory.** The endpoint of translation is $\gamma$, a sequence of dependent steps. Error compounds along $\gamma$ under $O$, $C$ and $T$ (post): $\operatorname{err}_{i+1} \le \operatorname{amp}_i \operatorname{err}_i + \xi_i$, with $\operatorname{amp}_i$ and $\xi_i$ nondecreasing in $o$, $c$, $\vartheta$ [open]. $U$ is a property of paths under bounded representation.

**Heuristic.** Addition [ruled]. Cycle: $j \to \gamma \to \operatorname{lift}(\gamma) \to \text{step} \to \text{update}$. A route that fails the virtual test dies in the agent's stead (Popper). $B = B_R + B_F + B_D + B_w + B_0$. The heuristic is the $\gamma$ returned by the cycle under $B$. Search stops when the expected gain of one more pass falls below its cost. This stopping point is $\kappa^\ast$. Not $I$ $\Rightarrow$ $\gamma$ optimal at $B_R = B_F = B_w = 0$.

**Cube.** Two coordinate sets (def). Presence of structure: $\operatorname{sig} = (R, F, D) \in \{0,1\}^3$, eight signatures, a taxonomy. Degree of obstruction: $(o, c, \vartheta)$, graded. More structure can lower an obstruction. Coordinates of a translation problem: $(I, \operatorname{sig})$, with degrees reported beside them. Corners are extreme types [ruled]. Signature $(0,0,0)$ means no formalizable structure. Degrees $(0, 0, 0)$ mean no obstruction. The two belong to different coordinate sets.

## 3. TG

**Translation contract.** Paper 3 constructs computable candidates for the mechanisms the stand-ins explain. Their correspondence is partial and lossy [ruled].

| Stand-in (Papers 1, 2) | Candidate (Paper 3) | Kept | Lost |
|---|---|---|---|
| Fisher discriminability | $D_{\mathrm{sym}}(m, n) \approx \delta y^\top g_F\, \delta y$ on map states | distinguishability of neighboring states | smooth coordinates, full metric, curvature |
| natural gradient | $\phi$, $j$ on $K_M$ | goal-conditioned ranking | invariance of Fisher geometry |
| curvature as fragility | $\lambda_\zeta$, with $\lambda_2$ as global bound | sensitivity of the ranking to the goal | intrinsic curvature |
| singularities | $\operatorname{lift} = 0$ | aliasing of routes | probability of execution, unseen paths |
| metric decay, $\delta g$ | $G_t$, $d_{\mathcal{SM}}$, $\operatorname{Tor}$ | change of weights and structure | rate and cost of change |
| control work | correction cost on $K_M$ | computable expenditure | metabolic conversion |

**Complexes.** $K_S$ with $\Lambda_S$, symmetric or asymmetric, no task-given potential. $K_M$ with diagonal $G > 0$. $\pi: V_S \twoheadrightarrow V_M$. Quotienting can create map edges with no territory transition. Metrics (def): $\operatorname{dist}_S$ shortest path on the symmetrized $\Lambda_S$, $\operatorname{dist}_M$ shortest path with edge length $G_e^{-1}$, $\mu_S$ normalized. Bridge (def, optional): $D_{\mathrm{sym}}(m, n) = \mathrm{KL}(p_m \Vert p_n) + \mathrm{KL}(p_n \Vert p_m)$. Any rule that sets $G$ from $D_{\mathrm{sym}}$, reliability or cost is a modeling choice (post).

**Weighted convention (def).** $\tilde{\partial}_1 = \partial_1 G^{1/2}$, $\tilde{\partial}_2 = G^{-1/2} \partial_2$, $\tilde{\partial}_1 \tilde{\partial}_2 = 0$. $\Delta_0 = \tilde{\partial}_1 \tilde{\partial}_1^\top = \partial_1 G \partial_1^\top$, $\Delta_1 = \tilde{\partial}_1^\top \tilde{\partial}_1 + \tilde{\partial}_2 \tilde{\partial}_2^\top$.

**Identification.** $\Delta_0 \phi = \zeta$, $\mathbf{1}^\top \zeta = 0$, $j = -G\, \partial_1^\top \phi$. $\gamma_j$ (def): from the current vertex, step along the outgoing edge of largest positive $j$. $\lambda_2 > 0$ gives connectivity and no direction. Task-conditioned gap: $\lambda_\zeta = \lVert \zeta \rVert^2 / (\zeta^\top \Delta_0^\dagger \zeta)$.

Theorem 3.0. $\lambda_2 = \min_{\zeta \perp \mathbf{1}} \lambda_\zeta$, and $\lambda_\zeta^{-1} = \sum_k (c_k^2 / \lVert \zeta \rVert^2) \lambda_k^{-1}$ for $\zeta = \sum_k c_k v_k$ in the eigenvectors of $\Delta_0$: the mean relaxation time of the task potential. A small $\lambda_2$ is necessary for a small $\lambda_\zeta$ and not sufficient. $t_{\mathrm{rel}} \propto \lambda_2^{-1}$ for diffusion on $K_M$.

**Composition.** Hodge decomposition of an edge chain $r$ (thm): $G^{-1/2} r = \tilde{\partial}_1^\top u + \tilde{\partial}_2 v + h$, $h \in \ker \Delta_1$, $\beta_1 = \dim \ker \Delta_1$. The scaled flow $G^{-1/2} j = -\tilde{\partial}_1^\top \phi$ is a pure gradient. Harmonic parts belong to route chains.

$$\operatorname{lift}(\gamma \mid z_0) = \mathbf{1}_{z_0}^\top P_{m_0} \prod_{i \ge 1} \big(\Lambda_S P_{m_i}\big) \mathbf{1}$$

$\operatorname{lift} > 0$: at least one compatible path in the recorded $K_S$. Support (def): $\Gamma_{\mathcal{L}} \supseteq \Gamma_{\mathcal{S}} \supseteq \Gamma_B$. $\Gamma_{\mathcal{S}}(\gamma) = \{\gamma' \ne \gamma : \gamma' \text{ reaches } \zeta,\ \operatorname{lift}(\gamma' \mid z_0) > 0\}$. $\Gamma_B$: members of $\Gamma_{\mathcal{S}}$ found by the agent's search within $B$. $\Gamma_{\mathcal{L}}$ is unavailable to the agent. Where execution is stochastic, $\operatorname{lift}$ is replaced by a probability of success [open].

**Persistence.** $\log \operatorname{Tor} = \tfrac12 \sum_i (-1)^{i+1}\, i \log \det{}' \Delta_i$ (def, weighted convention, $\det{}'$ the product of nonzero eigenvalues). At constant rank, $\tfrac{d}{dt} \log \operatorname{Tor} = \tfrac12 \sum_i (-1)^{i+1}\, i \operatorname{Tr}(\Delta_i^\dagger \dot{\Delta}_i)$ (thm). A rank change is a discrete event: deleting an edge changes the chain space, a weight tending to zero does not.

$$d_{\mathcal{SM}} = \sum_{z, z' \in V_S} \mu_S(z) \mu_S(z')\, \lvert \operatorname{dist}_S(z,z') - \operatorname{dist}_M(\pi z, \pi z') \rvert^2$$

$d_{\mathrm{GW}}$: the same squared integrand, minimized over couplings, for maps without shared registration. Distances are the square roots.

**Regimes.** Rule (def, fixed before data):

| $\operatorname{reg}$ | Condition | Action |
|---|---|---|
| drift | $\operatorname{lift}(\gamma_j \mid z_0) > 0$ and $\lambda_\zeta > \epsilon^\ast$ | follow $j$. $d_{\mathcal{SM}} > 0$ is benign |
| control | trigger, $\Gamma_B(\gamma_j) \ne \emptyset$ | $w \ne 0$, then reconciliation of $G$ |
| remap | trigger, $\Gamma_B(\gamma_j) = \emptyset$ (hyp) | revision of $K_M$ or $\pi$ |

Trigger: $\operatorname{lift}(\gamma_j \mid z_0) = 0$ or $\lambda_\zeta \le \epsilon^\ast$. $\lambda_2$ is a global diagnostic, and no regime rests on it alone [ruled]. The threshold is a policy rule (post). No bifurcation of the spectrum is claimed. Control work (post, candidate) [inference]: $\mathcal{W} = \sum_t w_t^\top G^{-1} w_t$. Weight updates and maintenance carry separate nonnegative costs [open].

$\log \operatorname{Tor}$ is a signed observable of deformation. It is not identified with $\mathcal{W}$ [ruled].

**Envelope.** $\mathcal{E} = \{(z_0, \zeta) : \exists \gamma \in \{\gamma_j\} \cup \Gamma_B(\gamma_j),\ \operatorname{lift}(\gamma \mid z_0) > 0,\ \text{cost of } \gamma \le B\}$, the agent's budget-certified envelope. Confidence: low-cost correction of minor divergence inside drift.

**Viability (def, ex ante criterion).** Against the counterfactual policy of physical testing, over a stated horizon, in common units: $\mathbb{E}[\ell \text{ avoided}] > \mathbb{E}[B_F + B_w + B_0]$. Used by the separate paper (§6).

**Propositions.** 3.1 Gradient manufacture (thm): $K_M$ connected $\Rightarrow$ $\phi = \Delta_0^\dagger \zeta$ unique up to a constant and $j$ unique. 3.2 Fixed-policy failure (thm, formerly control-work necessity): if $\operatorname{lift}(\gamma_j \mid z_0) = 0$, no trajectory with $w \equiv 0$ and $\dot{G} \equiv 0$ reaches $\zeta$. The identification with conscious engagement is Postulate 1.0, not a consequence. 3.3 Perspective asymmetry: (thm) for finite metric measure spaces, $d_{\mathrm{GW}} = 0$ iff they are isomorphic. (post) distinct parochial samplings with non-injective compression generically give non-isomorphic maps, so $d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) > 0$. 3.4 Torsion variation at constant rank (thm). The partition and impossibility theorems of the note are outside the series [ruled].

**Worked case 3.5.** $V_S = \{z_1, \dots, z_4\}$, path, uniform $\mu_S$. $\pi: z_1, z_4 \mapsto m_1$, $z_2 \mapsto m_2$, $z_3 \mapsto m_3$. $K_M$ a triangle, edges $(m_1 m_2, m_2 m_3, m_3 m_1)$, $G = \operatorname{diag}(1, 1, g)$, no face. Goal $\zeta = (1, 0, -1)$ from $z_1$. At $g = 1$: $\lambda_2 = \lambda_\zeta = 3$, $\phi = (\tfrac13, 0, -\tfrac13)$, $j = (\tfrac13, \tfrac13, -\tfrac23)$, $\gamma_j = (m_1, m_3)$. $\operatorname{lift}(\gamma_j \mid z_1) = 0$, $\operatorname{lift}((m_1, m_2, m_3) \mid z_1) = 1$: control. The gap does not detect the alias. The lift does. Harmonic parts of the route chains: $\tfrac13$ and $\tfrac23$ per edge, which do not separate the routes. $\det{}' \Delta_1 = 3(1 + 2g)$, so $\Delta \log \operatorname{Tor} = -\tfrac12 \ln 3$ as $g$ goes from $1$ to $0^+$, at $\beta_1 = 1$ throughout. Deleting the edge gives $\beta_1 = 0$ and $j = (1, 1)$. $d_{\mathcal{SM}}$: $\tfrac{22}{16}$ before and after deletion, $\tfrac29 \to 0$ on $\{z_1, z_2, z_3\}$. Local repair need not improve global distortion. Splitting $m_1$ (remap) gives $d_{\mathcal{SM}} = 0$. Three operations stay distinct: reweighting, deletion, splitting.

**Bench (def).** Fixed classifier, independently known ground truth. (A) two clusters, weak bridge, task inside one cluster: small $\lambda_2$ alone must not trigger control. (B) Worked case 3.5: a large gap must not hide a zero lift. (C) a harmless cycle: $\beta_1 > 0$ alone must not trigger control. (D) a transition omitted from $\mathcal{S}$: failure under $\mathcal{S}$ is not impossibility in $\mathcal{L}$. (E) slow drift of one weight: no regime change follows automatically. (F) local against global repair, as in 3.5. (G) Bernoulli family: varying discriminability at zero curvature.

## 4. MC

Scope [ruled]: making CAT measurable, predictive and falsifiable. Nothing else.

**Thesis.** Scientific observation is a second translation (Proposition 3.3). Control at a critical limit consumes $a$ and produces $\mathcal{W}$. Both leave traces.

**Constructs.** $a$: power, from metabolic markers. $\mathcal{W}$: correction cost over $\Theta$, from behavior and model fits. $\lambda_\zeta$, $\lambda_2$, $\operatorname{lift}$, $d_{\mathcal{SM}}$, $\operatorname{Tor}$: from estimated $K_M$. Assumption 4.1 (post): $\hat{a}$ is increasing in $a$. Postulate 4.2 (from the note): $\mathcal{W} \ge c_0\, \lvert \Delta \log \operatorname{Tor} \rvert$, $c_0 > 0$. It is not derived from Theorem 3.4.

**Qualification.** Estimators are validated on synthetic graphs with known structure, on known interventions and on held-out data. Threshold calibration and confirmation use separate data. Failures are assigned to one layer: estimator, translation, mechanism, or consciousness link.

**Waking tests (post).**
Test 4.3. At an independently calibrated task threshold, control policy and control cost change. $\hat{\lambda}_\zeta$ predicts the location of the threshold.
Test 4.4. $\mathbb{E}[\text{response time}] = t_0 + c_1\, \lambda_\zeta^{-1}$ near the threshold. The note's exponent $-\tfrac12$ requires a bifurcation model [open].
Test 4.5. Braking ($\Delta \operatorname{bnd}$) is predicted by failed lift and revision demand. $\Delta \log \operatorname{Tor}$ adds explanatory power beyond them.
Test 4.6. $\int_\Theta \hat{a}\, dt$ tracks $\hat{\mathcal{W}}$ with slope $\eta^{-1}$. $\lvert \Delta \log \operatorname{Tor} \rvert$ adds out-of-sample prediction.

**State contrasts.** Experimental contrasts, not a taxonomy.

| State | Papers 1, 2 | Contrast |
|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $\lambda_\zeta > \epsilon^\ast$, $a = a_{\mathrm{base}}$ |
| overload | $\kappa \ge \kappa^\ast$ sustained | $\lambda_\zeta \le \epsilon^\ast$ sustained, $\eta$ low |
| flow | $\kappa$ just below $\kappa^\ast$ | $\lambda_\zeta$ just above $\epsilon^\ast$, $\eta$ maximal |
| meditation | $\kappa$ lowered, $\kappa^\ast$ raised | baseline $\lambda_\zeta$ raised, $\mathcal{E}$ larger |
| psychedelics | variance of $\kappa$ raised | $\operatorname{PR}$ raised, large $d_{\mathrm{GW}}$ from baseline, remap after |
| propofol | no mediation | long-range $\lambda_2 \to 0$, $\mathcal{W} \to 0$, $a$ suppressed |
| ketamine, REM | control without actuators | $\mathcal{W} > 0$ internally, input and output gated |

Test 4.7 (post). With state, task and recording sensitivity fixed in advance, under propofol and in dreamless sleep the control channel does not respond to manipulated $\lambda_\zeta$. Positive and negative controls are required.

**Agents.** Two agents coordinate under drift while $d_{\mathrm{GW}}(\mathcal{M}_A, \mathcal{M}_B) < \delta^\ast$ and require explicit translation above it (post).

**Design.** A finite navigation task with known territory graph and local observations. Opacity, contingency, transience and task location are manipulated independently. A Fisher-informed model and a graph-only model are fitted to the same trials and predict held-out perturbations. Negative controls: bench cases A to E.

**Falsification.** Operator level: under known graphs, the identities or the fixed classifier fail. Bridge: Fisher-informed and graph quantities disagree beyond their stated domain. Mechanism: calibrated quantities do not predict route failures, corrections or energy costs prospectively. Consciousness link: the mechanism is present where experience-related evidence is absent, or the reverse. The last is Postulate 1.0 and is tested last. No numeric cutoff from the note is carried as established.

## 5. Open

Confidence against the budget-certified $\mathcal{E}$. Statement of $I$ at $\sigma$ and $\gamma$. Forms of $\Delta a_e$, of the compounding of error, and of control work on $K_M$. Probabilistic lift. Remap after repeated failure under control while $\Gamma_B$ is not empty. The relation between $\epsilon^\ast$ and $\kappa^\ast$. Estimators.

Dependency: §2 $\to$ §1 $\to$ §3 $\to$ §4. Paper 1 is self-sufficient with respect to §2. §6 depends on §1 and §3 and on nothing in §4.

## 6. Lower Bound (separate paper)

Not part of Papers 1 to 4 [ruled]. Kept here so that nothing is lost. A conjecturing engine pays only under the viability criterion of §3. Motility and sessility give the first dividing line: the combinatorial explosion of changing environments. A sessile agent can produce physical conjectures (literal branch and bound). A motile agent has to produce virtual ones, which requires a metabolically costly central conjecturing engine. The two models sit downstream of that need. Boundary test, all three required: (i) compression $\pi$ with $\dim \mathcal{M} \ll \log \nu(\mathcal{S})$, (ii) a discontinuity measurable from without at a critical limit, (iii) offline conjecturing in high-intensity REM, $\delta_{\mathrm{lo}} \le d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{wake}}, \mathcal{M}_{\mathrm{sleep}}) \le \delta_{\mathrm{hi}}$. Dreaming is the enactment of far-fetched, potentially lethal conjectures under physical incapacitation. Only organisms that dream can be conscious [ruled]. Comparative placement across taxa and of LLMs: summary report on the lower bound, unchecked.
