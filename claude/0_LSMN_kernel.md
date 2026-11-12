# LSMN Kernel

Version 0.12, 13 November 2026. One kernel for Papers 1 to 4. Baseline: the 2025 Papers 1 and 2 and the research notes for Papers 3 and 4. A departure from the baseline carries one of three tags. [ruled]: decided by the authors. [inference]: proposed here, not ruled. [open]: form not fixed. Numbers taken from the notes are unchecked.

Rule: one meaning per symbol. Every symbol is in the registry. Regimes, results and tests carry words or section numbers, never single letters.

## 0. Registry

| Symbol | Meaning |
|---|---|
| $\mathcal{L}, \mathcal{S}, \mathcal{M}, \mathcal{N}$ | Landscape (unsurveyable reality), Territory, Map, Navigation |
| $\sigma, \pi, \gamma$ | sampling $\mathcal{L} \to \mathcal{S}$, compression $\mathcal{S} \to \mathcal{M}$, policy trajectory $\mathcal{M} \to \mathcal{N}$ |
| $K_S, V_S, z, \Lambda_S, \operatorname{dist}_S, \mu_S$ | Territory: complex, vertex set, vertex, adjacency matrix, metric, sampling density |
| $K_M, V_M, m, E_M, e, G, \partial_1, \partial_2, \operatorname{dist}_M$ | Map: complex, vertex set, vertex, edge set, edge, edge weights, boundary operators, metric |
| $\Delta_i, \lambda_2, \beta_1$ | Hodge Laplacian of degree $i$ on $K_M$, second eigenvalue of $\Delta_0$, $\dim \ker \Delta_1$ |
| $P_m, \mathbf{1}_m, \mathbf{1}$ | projector onto $\pi^{-1}(m)$, indicator vector, all-ones vector |
| $\zeta, \phi, j$ | goal vector, potential, manufactured flow |
| $u, v, h$ | Hodge components of a flow: gradient, rotational, harmonic |
| $\operatorname{lift}, \Gamma(\gamma)$ | lift functional, supported alternatives to $\gamma$ |
| $U, I, N$ | Unsurveyability, Intractability, Intransigence |
| $O, C, T$ | Opacity, Contingency, Transience |
| $R, F, D$ | relations, functions, dynamics |
| $\operatorname{sig}$ | structural signature in $\{0,1\}^3$ |
| $o, c, \vartheta$ | degrees of $O$, $C$, $T$ |
| $\nu, \alpha$ | count of relevant distinctions, scale |
| $y, g_F, p(\cdot \mid y), \operatorname{Ric}$ | smooth stand-in: point of $\mathcal{M}$, Fisher metric, response distribution, Ricci curvature |
| $\kappa, \kappa^\ast$ | curvature, its critical level (Papers 1 and 2) |
| $\epsilon^\ast, t_{\mathrm{rel}}$ | critical level of $\lambda_2$ (Papers 3 and 4), relaxation time |
| $w, \mathcal{W}$ | control field, control work |
| $a, a_{\mathrm{base}}, \Delta a_e, B$ | metabolic allocation, its waking baseline, its surge at instance $e$, budget |
| $\eta$ | conversion efficiency $\mathcal{W} / a$ |
| $\operatorname{reg}$ | regime: drift, control or remap |
| $\mathcal{E}$ | envelope of assured navigation |
| $\operatorname{Tor}$ | Ray-Singer torsion of $K_M$ |
| $d_{\mathcal{SM}}, d_{\mathrm{GW}}$ | anchored distortion between $\mathcal{S}$ and $\mathcal{M}$, unconstrained transport distance |
| $X, x_t, k, \operatorname{val}, \operatorname{Nbr}, \Omega_t$ | search space, state, number of options, objective, neighborhood, options reachable |
| $B_R, B_F, B_D, B_w, B_0$ | budgets: guidance, virtual search, physical execution, reconciliation, engine maintenance |
| $\ell, \ell_C, \ell_T$ | loss from a failed physical conjecture, expected loss from $C$, from $T$ |
| $\operatorname{err}_i, \operatorname{rate}$ | misalignment after step $i$, its growth rate |
| $\kappa_e, L_{\mathrm{decay}}, \delta g$ | curvature at instance $e$, external change, metric shift |
| $c_0, c_1, c_2, t_0$ | positive constants |
| $\delta_{\mathrm{lo}}, \delta_{\mathrm{hi}}, \delta^\ast$ | band of offline deformation, critical distance between agents |
| $\operatorname{bnd}, \operatorname{PR}$ | decision boundary, participation ratio |
| $\hat{\ }$, $t$ | estimator, time |

Notation against the sources: $\pi$ for the 2025 $\phi$, $\phi$ for $V$, $w$ for $U$, $\mathcal{W}$ for $\mathcal{C}_U$, $\kappa$ for $K$, $y$ for $x$, $G$ for $W$, $\partial_1$ for $B_1$, $\zeta$ for $b$, $\Lambda_S$ for $A_S$, $B_w$ for $B_C$, $\epsilon^\ast$ for $\epsilon_c$, $\kappa^\ast$ for $\kappa_c$, $\delta^\ast$ for $\delta_c$. The changes remove collisions.

## 0.1 Chain

$$\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}, \qquad U = I + N, \quad N = (O, C, T)$$

Yardstick: the 2025 papers. Their argument and its order stand:

$$I \to \text{compression} \to O + C + T \to \text{high } \kappa \to \text{control} \to \text{consciousness}$$

Updates to the 2025 papers [ruled], numbered for reference in the scaffolds.
1. Chain of four stages. $\mathcal{S}$ is the agent's own model, sampled parochially.
2. Headline: to navigate an unsurveyable reality, a cognitive agent maintains, and mediates between, two models, one comprehensive ($\mathcal{S}$) and one comprehensible ($\mathcal{M}$). Consciousness arises out of that mediation and the need to allocate metabolic resources to keep the two aligned.
3. Consciousness is graded and present throughout wake: a baseline plus surges.
4. Control and remap are separated by whether a supported alternative exists.
5. The hard problem is not dissolved.
6. Stand-ins are named as such. Papers 3 and 4 make them operational.
7. $\mathcal{E}$ includes control. Current LLMs are below the bound.
8. The prose tropes of the 2025 text are removed.

Background. Virtual testing of conjectures (Popper) belongs to control (§1) and to $C$ (§2). The conjecturing engine, motility, the lower bound and the dreaming test belong to §4 and a satellite note.

Combinatorial and continuous. This pair is the central stand-in of Papers 1 and 2. The territory is combinatorial, the map is continuous. Papers 3 and 4 replace the pair with $K_S$ (relations only) and $K_M$ (weights, potential, flow). Footnote level: reality is mixed combinatorial, and the part with aligned local and global gradients needs no translation.

## 1. CAT

**Translation problem.** $I \iff \lim_{\alpha \to \infty} \log \nu(\mathcal{S}_\alpha) / \dim \mathcal{M} = \infty$. $O$: no local signal with an assured relation to the global path. $C$: steps foreclose options. $T$: reality and map drift apart in time. Stated in full in §2. Paper 1 restates them without reference to Paper 2.

**Architecture.** $\mathcal{S}$: unordered accumulation of impressions, sampled with density $\mu_S$ around habitats, comprehensive. $\mathcal{M} = \pi(\mathcal{S})$, $\pi$ non-injective: a rank offering of the available choices by their connection to $\zeta$, comprehensible. On the smooth stand-in, $\mathcal{M}$ is a manifold with Fisher metric

$$g_F(y)_{ik} = \mathbb{E}\big[\partial_i \log p(\cdot \mid y)\, \partial_k \log p(\cdot \mid y)\big], \qquad \dot{y} = -g_F^{-1} \nabla \phi(y) + w(y)$$

**Curvature.** $\kappa(y)$: scalar curvature of $g_F$. Compression produces distortion, distortion produces curvature. $\kappa$ is large where small moves in $\mathcal{M}$ correspond to large changes in $\mathcal{L}$, and where the continuous $\mathcal{M}$ misrepresents the combinatorial $\mathcal{S}$ (branch points, conflicting constraints). $\kappa$ carries both the divergence of $\mathcal{M}$ from $\mathcal{S}$ and its consequence for navigation [ruled]. $\kappa^\ast$ is specific to the agent. It balances the cost of control against the cost of error. $\operatorname{JND}(y) \propto \kappa(y)^{-1/2}$.

$C$ appears in $\mathcal{M}$ as singularities, where $\kappa$ diverges. $T$ appears as decay of the metric: $\partial_t g_F = -2 \operatorname{Ric} + L_{\mathrm{decay}}$.

**Regimes.**

| $\operatorname{reg}$ | Condition | Dynamics |
|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $w \approx 0$. The agent follows $\mathcal{M}$ |
| control | $\kappa \ge \kappa^\ast$, $\Gamma(\gamma) \ne \emptyset$ | $w \ne 0$. Candidate routes are tried virtually before commitment (Popper: conjectures die in the agent's stead) |
| remap | $\kappa \ge \kappa^\ast$, $\Gamma(\gamma) = \emptyset$ | $g_F \leftarrow g_F + \delta g$. The map changes |

The 2025 paper separates control from remap by $\kappa \approx \kappa^\ast$ against $\kappa \gg \kappa^\ast$. The test on $\Gamma(\gamma)$ replaces that [ruled]. $\mathcal{E}$: the states from which $\zeta$ is reached under drift or control. Remap lies outside $\mathcal{E}$ [ruled].

**Consciousness.** $\mathcal{W} = \int \lVert w \rVert^2_{g_F}\, dt = \eta\, a$.

$$a(t) = a_{\mathrm{base}}(t) + \sum_e \Delta a_e(t), \qquad \text{conscious}(t) \iff a(t) > 0$$

$a_{\mathrm{base}} > 0$ during wake: the live map is maintained against $T$. $\Delta a_e > 0 \iff \kappa_e \ge \kappa^\ast$, nondecreasing in $\kappa_e$, larger under remap than under control at equal $\kappa_e$. Degree at $e$: $\Delta a_e$. Rationing [inference]: $a \le B$, surges served in descending order of $\kappa_e$. Sampling [inference]: $\kappa_e$ is decreasing in $\mu_S(e)$, so habitats drift and the frontier draws allocation.

Result 1.1. Not $I$ $\Rightarrow$ no compression, no $\mathcal{M}$, no mediation, $a \equiv 0$. A perfectly rational agent needs zero models and is not conscious.
Result 1.2. Wake and $\vartheta > 0$ $\Rightarrow a > 0$ with no conflict present.
Result 1.3. $\kappa_e < \kappa^\ast \Rightarrow \Delta a_e = 0$. Processing at $e$ proceeds under drift.
Result 1.4. $w \equiv 0$ (dreamless sleep, anesthesia) $\Rightarrow a = 0$.
Result 1.5. Practice lowers $\kappa$ on the practiced domain and moves it from control to drift.

Why consciousness here (2025): phenomenology, signatures and functional necessity align with control at $\kappa \ge \kappa^\ast$. Addition [ruled]: a homeostat corrects against a fixed reference and tests nothing virtually. Control in the sense of the table decides between candidate routes before commitment.

**Experience.** Identifications, not derived. Effort: the rate $\lVert w \rVert^2_{g_F}$. Salience: information density, high where $\kappa$ is high. Meaning: criticality, $\kappa$ near $\kappa^\ast$. Intensity: $\lVert \nabla \kappa \rVert_{g_F}$ along trajectories with $w \ne 0$. Hard problem [ruled]: not dissolved. Science regularizes observations from without and can only triangulate experience within. Consciousness is a work effort, and work leaves traces observable from without. Different histories give different $\mathcal{M}$ for the same stimuli (§3, Proposition 3.3).

**Neighbors.** Free energy: the global objective, $\phi$ as free energy. Bounded rationality: satisficing stops at $\kappa^\ast$. Rate-distortion: $\kappa$ marks where distortion concentrates. Energy-based networks: temperature regulated locally by $\kappa$. Global workspace: $\kappa \to \kappa^\ast$ triggers broadcast.

**Altered states.** Changes of average $\kappa$, its variance, $\kappa^\ast$, or control capacity. Meditation: lower $\kappa$, higher $\kappa^\ast$. Psychedelics: higher variance of $\kappa$. Flow: $\kappa$ sustained near $\kappa^\ast$. Dreams: high $\kappa$ explored with actuators gated, control cheap. Anxiety: $\kappa$ overestimated. Anesthesia, dreamless sleep: $w \equiv 0$.

**Implications.** Behavioral, neural, developmental and individual predictions in terms of $\kappa$ and $\kappa^\ast$ (2025). Comparative criterion, three requirements (2025): representations rich enough for compression to distort, detection of failure of the gradient, capacity for corrective control. Current LLMs fail on two counts [ruled]: no adaptive recalibration in runtime, and no parochialism ($\mu_S$ without habitats). The second makes them the nearest known case of Result 1.1. Motility plays no role in Paper 1 [ruled].

## 2. UNS

**Translation problem.** $\mathcal{S}$ alone: no $j$, paralysis. $\mathcal{M}$ alone: $j$ never tested, hallucination. The map proposes, the territory disposes. Parsimony: $\pi^\ast = \arg\min_\pi d_{\mathcal{SM}}$ subject to $\dim \mathcal{M}$ within capacity, the most faithful searchable representation.

**Intractability.** $X$: arrangements of $k$ interacting options, $\lvert X \rvert \ge k!$. $\operatorname{val}: X \to \mathbb{R}$.

$$I \iff \lim_{\alpha \to \infty} \frac{\log \nu(\mathcal{S}_\alpha)}{\dim \mathcal{M}} = \infty, \qquad I \Rightarrow x_{t+1} \in \operatorname{Nbr}(x_t)$$

$I$ acts at $\sigma$ (parochial sampling), at $\pi$ (lossy compression) and at $\gamma$ (a linear sequence of local steps) [ruled].

**Obstructions.**

| | Obstruction | Problem posed | Degree | Ordering | Primitive |
|---|---|---|---|---|---|
| $O$ | no local information that reliably indicates the direction of global improvement | identification: what is available in the immediate environment | $o = 1 - \operatorname{corr}(\nabla_{\mathrm{loc}} \operatorname{val}, \nabla_{\mathrm{glob}} \operatorname{val}) \in [0,1]$ | comes with (none) | $R$ |
| $C$ | transitions are not freely reversible | composition: how it connects to the overall objective | $c \in [0,1]$, cost of reversion | follows from (logical, negotiable) | $F$ |
| $T$ | structure changes in time, or the map decays absent maintenance | persistence: how long it will be available | $\vartheta \ge 0$ | follows after (temporal, non-negotiable) | $D$ |

Degrees vary with the environment and within it. Any can be near zero [ruled]. Resolution of $O$: establish that the local signal correlates with the global path. For $0 < o < 1$ noise added to the choice can improve on strict following. Coupling [ruled]: $C$ binds in proportion to $o$. $T$ binds given a committed $\gamma$. Form [inference]: $\ell_C = \ell_C(o \cdot c)$, $\ell_T = \ell_T(\vartheta, \lvert \gamma \rvert)$. Completeness of $(I, O, C, T)$ is conjectured.

**Orderings.** $R$, $F$, $D$ are the mathematical primitives that capture the three orderings. The agent assigns orderings. It does not make up mathematics [ruled].

**Trajectory.** The endpoint of translation is $\gamma$, a sequence of dependent steps. Error compounds along $\gamma$ under $O$, $C$ and $T$: $\operatorname{err}_{i+1} = (1 + \operatorname{rate}(o, c, \vartheta)) \operatorname{err}_i$ [open]. $U$ is a property of paths under bounded representation.

**Heuristic.** Addition [ruled]. Cycle: $j \to \gamma \to \operatorname{lift}(\gamma) \to \text{step} \to \text{update}$. A route that fails the virtual test dies in the agent's stead (Popper). $B = B_R + B_F + B_D + B_w + B_0$. The heuristic is the $\gamma$ returned by the cycle under $B$. Search stops when the expected gain of one more pass falls below its cost. This stopping point is $\kappa^\ast$. Not $I$ $\Rightarrow$ $\gamma$ optimal at $B_R = B_F = B_w = 0$.

**Cube.** $\operatorname{sig} = (R, F, D) \in \{0,1\}^3$. Eight signatures. Coordinates of a translation problem: $(I, \operatorname{sig})$. Corners are extreme types [ruled]. Environments have graded $(o, c, \vartheta)$.
## 3. TG

**Complexes.** $K_S$ with $\Lambda_S$, symmetric or asymmetric, no potential. $K_M$ with $G$. $\pi: V_S \twoheadrightarrow V_M$.

**Identification.** $\Delta_0 = \partial_1 G\, \partial_1^\top$, $\Delta_0 \phi = \zeta$, $\mathbf{1}^\top \zeta = 0$, $j = -G\, \partial_1^\top \phi$. $\lambda_2 > 0$ gives connectivity and no direction. Collapse: $\lambda_2 \le \epsilon^\ast \Rightarrow \lVert \Delta_0^\dagger \rVert_2 = \lambda_2^{-1}$ large, $t_{\mathrm{rel}} \propto \lambda_2^{-1}$.

**Composition.** $\Delta_1 = \partial_1^\top \partial_1 + \partial_2 \partial_2^\top$. $j = \partial_1^\top u + \partial_2 v + h$, $h \in \ker \Delta_1$, $\beta_1 = \dim \ker \Delta_1$.

$$\operatorname{lift}(\gamma \mid z_0) = \mathbf{1}_{z_0}^\top P_{m_0} \prod_{i \ge 1} \big(\Lambda_S P_{m_i}\big) \mathbf{1}, \qquad \Gamma(\gamma) = \{\gamma' \ne \gamma : \gamma' \text{ reaches } \zeta,\ \operatorname{lift}(\gamma' \mid z_0) > 0\}$$

**Persistence.** $\log \operatorname{Tor} = \tfrac12 \sum_i (-1)^{i+1}\, i \log \det{}' \Delta_i$. At constant rank, $\tfrac{d}{dt} \log \operatorname{Tor} = \tfrac12 \sum_i (-1)^{i+1}\, i \operatorname{Tr}(\Delta_i^\dagger \dot{\Delta}_i)$.

$$d_{\mathcal{SM}} = \sum_{z, z' \in V_S} \mu_S(z) \mu_S(z')\, \lvert \operatorname{dist}_S(z,z') - \operatorname{dist}_M(\pi z, \pi z') \rvert^2$$

$d_{\mathrm{GW}}$: the same integrand, minimized over couplings, for maps without shared registration.

**Regimes.** Curvature made operational.

| Papers 1, 2 | Paper 3 |
|---|---|
| $\kappa < \kappa^\ast$ | $\lambda_2 > \epsilon^\ast$ and $\operatorname{lift}(\gamma \mid z_0) > 0$. $d_{\mathcal{SM}} > 0$ is then benign |
| $\kappa \ge \kappa^\ast$ | $\lambda_2 \le \epsilon^\ast$, or $\operatorname{lift}(\gamma \mid z_0) = 0$ |
| control | $\Gamma(\gamma) \ne \emptyset$, $w \ne 0$, then reconciliation of $G$ |
| remap | $\Gamma(\gamma) = \emptyset$, revision of $K_M$ or $\pi$ |
| Fisher metric, natural gradient | $\Delta_0$, $\lambda_2$, $\phi$, $j$ |
| singularities | $\Delta_1$, $\beta_1$, $\operatorname{lift}$ |
| metric decay, $\delta g$ | $\operatorname{Tor}$, $d_{\mathcal{SM}}$, $d_{\mathrm{GW}}$ |

$\log \operatorname{Tor}$ is a signed observable of deformation. It is not identified with $\mathcal{W}$ [ruled].

**Envelope.** $\mathcal{E} = \{(z_0, \zeta) : \exists \gamma,\ \operatorname{lift}(\gamma \mid z_0) > 0,\ \gamma \text{ reaches } \zeta \text{ within } B\}$. Confidence: low-cost correction of minor divergence inside drift.

**Viability.** The engine pays iff $\mathbb{E}[\ell \text{ avoided}] > \mathbb{E}[B_F + B_w + B_0]$.

**Propositions.** 3.1 Gradient manufacture: $K_M$ connected $\Rightarrow$ $\phi = \Delta_0^\dagger \zeta$ and $j$ unique. 3.2 Control-work necessity: if the route selected by $j$ has $\operatorname{lift} = 0$, then reaching $\zeta$ requires $w \ne 0$ or $\dot{G} \ne 0$. 3.3 Perspective asymmetry: $\sigma_{\mathrm{int}} \ne \sigma_{\mathrm{ext}}$ with non-injective compression $\Rightarrow d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) > 0$, under stated conditions. 3.4 Torsion variation at constant rank. The partition and impossibility theorems of the note are outside the series [ruled].

**Worked case 3.5.** $V_S = \{z_1, \dots, z_4\}$, path. $\pi: z_1, z_4 \mapsto m_1$, $z_2 \mapsto m_2$, $z_3 \mapsto m_3$. $K_M$ a triangle, unit weights. Goal $m_1$ to $m_3$ from $z_1$. $\phi = (\tfrac13, 0, -\tfrac13)$, $j = (\tfrac13, \tfrac13, -\tfrac23)$. $\operatorname{lift}((m_1, m_3) \mid z_1) = 0$, $\operatorname{lift}((m_1, m_2, m_3) \mid z_1) = 1$: control. $d_{\mathcal{SM}} = \tfrac{22}{16}$, and $\tfrac29$ on $\{z_1, z_2, z_3\}$. With $G_{m_3 m_1} \to 0$: $\det{}' \Delta_1 = 3(1 + 2 G_{m_3 m_1})$, $\Delta \log \operatorname{Tor} = -\tfrac12 \ln 3$, $\beta_1: 1 \to 0$, $j = (1, 1, 0)$, distortion on $\{z_1, z_2, z_3\}$ equal to $0$.

## 4. MC

**Thesis.** Scientific observation is a second translation: $d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) > 0$. Control at a critical limit consumes $a$ and produces $\mathcal{W}$. Both leave traces.

**Traces.** $\hat{a}$: metabolic. $\hat{\mathcal{W}}$: spectral and kinematic. $\eta = \mathcal{W} / a \in (0, 1]$. Assumption 4.1: $\hat{a}$ is increasing in $a$. Assumption 4.2 [from the note]: $\mathcal{W} \ge c_0\, \lvert \Delta \log \operatorname{Tor} \rvert$, $c_0 > 0$.

**Dictionary.** $\hat{\Delta}_0$ from connectivity among recording channels. $\hat{\beta}_1$ from persistent cohomology of population states. $\hat{d}_{\mathrm{GW}}$ from dissimilarity matrices across epochs or agents. Forms [open].

**Waking tests.** Transition from drift to control.
Test 4.3. Graded ambiguity produces a step drop of $\hat{\lambda}_2$ at a critical value, followed by a nonlinear rise of control markers.
Test 4.4. $\mathbb{E}[\text{response time}] = t_0 + c_1 \lvert \lambda_2 - \epsilon^\ast \rvert^{-1/2}$.
Test 4.5. $\Delta \operatorname{bnd} = c_2\, [\lambda_2 \le \epsilon^\ast]\, \log \operatorname{Tor}$.
Test 4.6. $\hat{a}$ is linear in $\Delta \log \operatorname{Tor}$ with slope proportional to $\eta^{-1}$.

**States.**

| State | Papers 1, 2 | Signature |
|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $\lambda_2 > \epsilon^\ast$, $\beta_1 = 0$, $a = a_{\mathrm{base}}$ |
| overload | $\kappa \ge \kappa^\ast$ sustained | $\lambda_2 \le \epsilon^\ast$, $\beta_1 > 0$, $\eta$ low |
| flow | $\kappa$ just below $\kappa^\ast$ | $\lambda_2$ just above $\epsilon^\ast$, $\eta$ maximal |
| meditation | $\kappa$ lowered, $\kappa^\ast$ raised | baseline $\lambda_2$ raised, $\mathcal{E}$ larger |
| psychedelics | variance of $\kappa$ raised | $\operatorname{PR}$ raised, large $d_{\mathrm{GW}}$ from baseline, remap after |
| propofol | $w \equiv 0$ | long-range $\lambda_2 \to 0$, $\mathcal{W} \to 0$, $a$ suppressed |
| ketamine, REM | control without actuators | $\mathcal{W} > 0$ internally, input and output gated |

Test 4.7. Under propofol and in dreamless sleep, $\hat{a}$ and $\hat{\mathcal{W}}$ do not respond to $\hat{\lambda}_2$.

**Agents.** Two agents coordinate under drift while $d_{\mathrm{GW}}(\mathcal{M}_A, \mathcal{M}_B) < \delta^\ast$ and require explicit translation above it.

**Lower bound.** Handed to a satellite note. A conjecturing engine pays only under the viability condition of §3. Motility and sessility give the first dividing line: a sessile agent can afford physical conjectures, a motile agent cannot. Boundary test, all three required: (i) compression $\pi$ with $\dim \mathcal{M} \ll \log \nu(\mathcal{S})$, (ii) a discontinuity measurable from without at the critical limit, (iii) offline conjecturing in high-intensity REM, $\delta_{\mathrm{lo}} \le d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{wake}}, \mathcal{M}_{\mathrm{sleep}}) \le \delta_{\mathrm{hi}}$. Only organisms that dream can be conscious [ruled].

**Refutation.** The series fails if control markers scale linearly through the critical value in Test 4.3, if $\hat{a}$ and $\hat{\mathcal{W}}$ respond to $\hat{\lambda}_2$ under Test 4.7, or if a system passes the boundary test and shows none of Tests 4.3 to 4.6.

## 5. Open

Corner $(0,0,0)$ of the cube: the 2025 reading (no formalizable structure) against the reading under graded degrees (no obstruction). Confidence against the corrected $\mathcal{E}$. Statement of $I$ at $\sigma$ and $\gamma$. Forms of $\Delta a_e$ and of the compounding of error. Estimators.

Dependency: §2 $\to$ §1 $\to$ §3 $\to$ §4. Paper 1 is self-sufficient with respect to §2.
