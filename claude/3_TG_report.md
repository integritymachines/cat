# Translation Geometry

Report, draft 0.3, 13 November 2026. Kernel: `0_LSMN_kernel.md` §3. The research note for Paper 3 is the yardstick. Changes since 0.2 adopt the review of 13 November under the authors' rulings. Provenance: [ruled], [inference], [open]. Claim types: (def), (thm), (post) modeling postulate subject to empirical test, (hyp) hypothesis to be confirmed, (ill) illustration.

Papers 1 and 2 explain the theory with synecdoches: a combinatorial territory, a smooth map with the Fisher metric, and curvature against a critical level. This report constructs computable candidates for the mechanisms those synecdoches explain. The correspondence is partial and lossy, and the report states what is lost. It contains definitions, theorems, postulates, one computed example and a bench of test cases. It contains no empirical claims.

## Contract

Each stand-in has a candidate. Each candidate keeps part of what the stand-in explains and loses the rest.

| Stand-in (Papers 1, 2) | Candidate | Kept | Lost |
|---|---|---|---|
| Fisher discriminability | divergence $D_{\mathrm{sym}}$ between neighboring map states | distinguishability of neighbors | smooth coordinates, full metric, curvature |
| natural gradient | potential $\phi$ and flow $j$ on $K_M$ | goal-conditioned ranking | invariance of Fisher geometry |
| curvature as fragility | task-conditioned gap $\lambda_\zeta$, with $\lambda_2$ as global bound | sensitivity of the ranking to the goal | intrinsic curvature |
| singularities | zero lift | aliasing of routes | probability of execution, unseen paths |
| metric decay, metric shift | weights $G_t$, distortion $d_{\mathcal{SM}}$, torsion | change of weights and structure | rate and cost of change |
| control work | correction cost on $K_M$ | computable expenditure | metabolic conversion |

Fisher information stays in the series. Paper 1 keeps it as the local measure of discriminability. This paper offers one bridge to it and declares the rest of Fisher geometry unestimated. Whether the bridge adds predictive power over a graph-only model is an empirical question for Paper 4.

## Complexes

The chain of the series is $\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}$: landscape, territory, map, navigation.

Territory (def). A relational complex $K_S$ with vertex set $V_S$, vertices $z$, adjacency matrix $\Lambda_S$ and normalized sampling measure $\mu_S$. It is a parochially sampled record of encounters. $\Lambda_S$ may be asymmetric. $K_S$ carries no task-given potential. It is not globally ranked, although adjacency already records some order.

Map (def). A simplicial complex $K_M$ with vertex set $V_M$, vertices $m$, oriented edge set $E_M$, positive diagonal edge weights $G$ and boundary operators $\partial_1$ (edges to vertices) and $\partial_2$ (faces to edges). The map does not create options. It orders them.

Compression (def). A surjection $\pi: V_S \twoheadrightarrow V_M$ that is not injective. $P_m$ is the diagonal projector onto the fiber $\pi^{-1}(m)$. Quotienting can create map edges that correspond to no territory transition.

Metrics (def). $\operatorname{dist}_S$ is the shortest-path distance on the symmetrized $\Lambda_S$. $\operatorname{dist}_M$ is the shortest-path distance with edge length $G_e^{-1}$.

Bridge to Fisher (def, optional). Let $p_m = p(\cdot \mid m)$ be the distribution of observations predicted at map state $m$, conditioned on goal and habitat. Then

$$D_{\mathrm{sym}}(m, n) = \mathrm{KL}(p_m \Vert p_n) + \mathrm{KL}(p_n \Vert p_m) \approx \delta y^\top g_F(y)\, \delta y \tag{1}$$

for neighboring states in a regular family. Statistical similarity does not imply reachability. Any rule that sets $G$ from $D_{\mathrm{sym}}$, from reliability or from cost is a modeling choice (post).

Weighted convention (def). All operators use one edge inner product:

$$\tilde{\partial}_1 = \partial_1 G^{1/2}, \qquad \tilde{\partial}_2 = G^{-1/2} \partial_2, \qquad \Delta_0 = \tilde{\partial}_1 \tilde{\partial}_1^\top = \partial_1 G\, \partial_1^\top, \qquad \Delta_1 = \tilde{\partial}_1^\top \tilde{\partial}_1 + \tilde{\partial}_2 \tilde{\partial}_2^\top \tag{2}$$

with $\tilde{\partial}_1 \tilde{\partial}_2 = 0$.

## Identification

Opacity poses the problem of identification, and relations are its primitive. With $0 = \lambda_1 \le \lambda_2 \le \dots$ the eigenvalues of $\Delta_0$, a connected $K_M$ has $\lambda_2 > 0$. Connectivity supplies no direction. Direction requires a goal vector $\zeta$ with $\mathbf{1}^\top \zeta = 0$, positive at the source and negative at the sink:

$$\Delta_0 \phi = \zeta, \qquad \phi = \Delta_0^\dagger \zeta, \qquad j = -G\, \partial_1^\top \phi \tag{3}$$

**Proposition 3.1 (gradient manufacture, thm).** Let $K_M$ be connected and $\mathbf{1}^\top \zeta = 0$. Then (3) has a solution $\phi$ unique up to an additive constant, and $j$ is unique.

*Proof.* $\Delta_0$ is symmetric positive semidefinite with $\ker \Delta_0 = \operatorname{span}(\mathbf{1})$. Since $\zeta \perp \mathbf{1}$, $\zeta$ lies in the range. Two solutions differ by a multiple of $\mathbf{1}$, and $\partial_1^\top \mathbf{1} = 0$. $\square$

At each vertex, $j$ ranks the outgoing edges. This is the rank offering of Paper 1. Route extraction (def): $\gamma_j$ starts at the agent's vertex and steps along the outgoing edge of largest positive $j$ until it reaches the sink.

Sensitivity. The global gap $\lambda_2$ bounds how strongly any goal can be disturbed. A given task sees its own gap:

$$\lambda_\zeta = \frac{\lVert \zeta \rVert^2}{\zeta^\top \Delta_0^\dagger \zeta} \tag{4}$$

For a source and sink pair, $\zeta^\top \Delta_0^\dagger \zeta$ is the effective resistance between them.

**Theorem 3.0 (thm).** $\lambda_2 = \min_{\zeta \perp \mathbf{1}} \lambda_\zeta$.

*Proof.* On $\mathbf{1}^\perp$, the largest eigenvalue of $\Delta_0^\dagger$ is $\lambda_2^{-1}$, so $\zeta^\top \Delta_0^\dagger \zeta \le \lVert \zeta \rVert^2 / \lambda_2$, with equality at the Fiedler vector. $\square$

Write $\zeta = \sum_k c_k v_k$ in the eigenvectors of $\Delta_0$ with eigenvalues $\lambda_k > 0$. Then $\lambda_\zeta^{-1} = \sum_k (c_k^2 / \lVert \zeta \rVert^2)\, \lambda_k^{-1}$ (thm): the mean relaxation time of the task potential, weighted by the goal's spectral content. A small $\lambda_2$ is therefore necessary for some task to be sensitive, and not sufficient for a given task to be. Two dense clusters joined by a weak bridge have a small $\lambda_2$. A task inside one cluster still sees a large $\lambda_\zeta$. With four vertices per cluster and a bridge of weight $0.01$, $\lambda_2 \approx 0.005$, while $\lambda_\zeta = 4$ for a pair inside one cluster and $\lambda_\zeta \approx 0.02$ for a pair across the bridge. The relaxation time of diffusion on $K_M$ is $t_{\mathrm{rel}} \propto \lambda_2^{-1}$.

## Composition

Contingency poses the problem of composition, and functions are its primitive. Under (2), every edge chain $r$ splits orthogonally (thm):

$$G^{-1/2} r = \tilde{\partial}_1^\top u + \tilde{\partial}_2 v + h, \qquad h \in \ker \Delta_1, \qquad \beta_1 = \dim \ker \Delta_1 \tag{5}$$

The first part is a gradient, the second circulates around filled faces, and $h$ circulates around cycles that bound no face. The scaled flow $G^{-1/2} j = -\tilde{\partial}_1^\top \phi$ is a pure gradient, so the harmonic part belongs to route chains and not to $j$. A harmonic cycle is a feature of the map. It does not by itself signal a contradiction with the territory.

The test of a route against the territory is the lift functional (def). For a start $z_0 \in \pi^{-1}(m_0)$,

$$\operatorname{lift}(\gamma \mid z_0) = \mathbf{1}_{z_0}^\top P_{m_0} \prod_{i \ge 1} \big(\Lambda_S P_{m_i}\big)\, \mathbf{1} \tag{6}$$

It counts the paths in $K_S$ from $z_0$ that project onto $\gamma$. A positive lift means that at least one compatible path exists in the recorded territory. It does not mean that every execution succeeds, that the sample is complete, or that the route is affordable. A zero lift means that the compression has joined parts of the territory that are not connected. Virtual rollout rejects such a route before execution. This is the exact form of the virtual backtracking of Paper 2.

Three kinds of support (def):

$$\Gamma_{\mathcal{L}}(\gamma) \supseteq \Gamma_{\mathcal{S}}(\gamma) \supseteq \Gamma_B(\gamma) \tag{7}$$

$\Gamma_{\mathcal{L}}$ holds the alternatives that reach $\zeta$ in the landscape. It is unavailable to the agent. $\Gamma_{\mathcal{S}}(\gamma) = \{\gamma' \ne \gamma : \gamma' \text{ reaches } \zeta,\ \operatorname{lift}(\gamma' \mid z_0) > 0\}$ holds those the recorded territory supports. $\Gamma_B$ holds those the agent's search finds within budget $B$. Where execution is stochastic, the lift is replaced by an estimated probability of success [open].

## Persistence

Transience poses the problem of persistence, and dynamics are its primitive.

Torsion (def). With $\det{}'$ the product of nonzero eigenvalues under (2),

$$\log \operatorname{Tor}(K_M) = \frac12 \sum_i (-1)^{i+1}\, i\, \log \det{}' \Delta_i \tag{8}$$

This is a combinatorial torsion of the finite complex. The analytic name of the note is kept only as a pointer.

**Proposition 3.4 (torsion variation, thm).** Along a smooth family $\Delta_i(t)$ with each $\dim \ker \Delta_i$ constant,

$$\frac{d}{dt} \log \operatorname{Tor} = \frac12 \sum_i (-1)^{i+1}\, i\, \operatorname{Tr}\big(\Delta_i^\dagger \dot{\Delta}_i\big) \tag{9}$$

*Proof.* At constant rank, $\tfrac{d}{dt} \log \det{}' \Delta_i = \operatorname{Tr}(\Delta_i^\dagger \dot{\Delta}_i)$. $\square$

A rank change is a discrete event. Deleting an edge changes the chain space and can change $\beta_1$. A weight that tends to zero on a retained edge does not. Log torsion is a signed observable of deformation. It is not identified with control work [ruled], and (9) supplies no energetic bound.

Distortion (def). An agent's own territory and map share a registration through $\pi$:

$$d_{\mathcal{SM}} = \sum_{z, z' \in V_S} \mu_S(z)\, \mu_S(z')\, \big\lvert \operatorname{dist}_S(z, z') - \operatorname{dist}_M(\pi z, \pi z') \big\rvert^2 \tag{10}$$

Two maps without a shared registration, with symmetric metrics and normalized measures, are compared by the squared transport discrepancy

$$d_{\mathrm{GW}}(\mathcal{X}, \mathcal{Y}) = \frac12 \min_{\text{couplings of } \mu_X, \mu_Y} \iint \big\lvert \operatorname{dist}_X(x, x') - \operatorname{dist}_Y(y, y') \big\rvert^2 \tag{11}$$

integrated against the coupling twice. Both (10) and (11) are squared. The corresponding distances are their square roots. (11) applies to two agents, to an agent and an observer, and to one agent at two times.

## Regimes

The regime rule is fixed before any data are seen (def).

| Regime | Condition | Action |
|---|---|---|
| drift | $\operatorname{lift}(\gamma_j \mid z_0) > 0$ and $\lambda_\zeta > \epsilon^\ast$ | follow $j$ |
| control | trigger, and $\Gamma_B(\gamma_j) \ne \emptyset$ | $w \ne 0$, then reconciliation of $G$ |
| remap | trigger, and $\Gamma_B(\gamma_j) = \emptyset$ (hyp) | revision of $K_M$ or $\pi$ |

Trigger: $\operatorname{lift}(\gamma_j \mid z_0) = 0$ or $\lambda_\zeta \le \epsilon^\ast$.

Under drift, $d_{\mathcal{SM}} > 0$ in general and the loss is benign. The note adds confidence, the low-cost correction of minor divergence that does not halt progress.

$\lambda_2$ remains a global diagnostic. No regime rests on it alone [ruled]. By Theorem 3.0, $\lambda_2 > \epsilon^\ast$ rules out a trigger by sensitivity for every task.

The threshold $\epsilon^\ast$ is a policy rule (post). A smooth change of weights moves the spectrum smoothly, and no bifurcation is claimed.

Remap on $\Gamma_B = \emptyset$ is a decision under budget (hyp). It does not establish that no route exists in $\mathcal{S}$ or in $\mathcal{L}$.

Control work. A candidate [inference] (post) is a correction $w_t \in \mathbb{R}^{E_M}$ to the flow, with $\mathcal{W} = \sum_t w_t^\top G^{-1} w_t$. Weight updates and maintenance carry separate nonnegative costs [open].

## Envelope

The envelope of assured navigation is certified by the agent within its budget (def):

$$\mathcal{E} = \{(z_0, \zeta) : \exists\, \gamma \in \{\gamma_j\} \cup \Gamma_B(\gamma_j),\ \operatorname{lift}(\gamma \mid z_0) > 0,\ \text{cost of } \gamma \le B\} \tag{12}$$

It contains everything reached under drift or control [ruled]. The note restricts the envelope to drift. The definition here follows the ruling. Remap lies outside $\mathcal{E}$ and can enlarge it as a consequence. "Assured" means certified by the agent's own search against its own record. It does not mean robust in the landscape.

## Viability

The machinery that performs the virtual test (6) and the reconciliation has a cost. Let $\ell$ be the loss from a failed physical test, $B_F$ the budget for virtual search, $B_w$ the budget for reconciliation and $B_0$ the cost of maintenance. Against the counterfactual policy of testing routes physically, over a stated horizon and in common units, the machinery is viable iff (def)

$$\mathbb{E}[\ell \text{ avoided}] > \mathbb{E}[B_F + B_w + B_0] \tag{13}$$

This is an ex ante decision criterion and not a theorem about consciousness. The left side grows with the number of mutually exclusive alternatives and with the irreversible cost of untested execution. The separate paper on the lower bound uses (13).

## Propositions

**Lemma 3.2 (fixed-policy failure, thm).** Formerly "control-work necessity". Let $\operatorname{lift}(\gamma_j \mid z_0) = 0$. Then no trajectory with $w \equiv 0$ and $\dot{G} \equiv 0$ reaches $\zeta$.

*Proof.* With $w \equiv 0$ and $G$ fixed, the agent executes $\gamma_j$. By (6) no path in $K_S$ from $z_0$ projects onto $\gamma_j$, so execution fails at the first edge at which the partial product vanishes. $\square$

Reaching the goal therefore requires $w \ne 0$ or a change of $G$. The lemma says nothing about metabolic expenditure or conscious engagement. Their identification with this mode of operation is Postulate 1.0 of Paper 1.

**Proposition 3.3 (perspective asymmetry).** Let $\mathcal{M}_{\mathrm{int}}$ be the map of an agent and $\mathcal{M}_{\mathrm{ext}}$ the map that an observer forms of the same landscape, each obtained by its own sampling and its own non-injective compression.

(thm) For finite metric measure spaces with symmetric metrics, $d_{\mathrm{GW}} = 0$ iff the spaces are isomorphic.

(post) Distinct parochial samplings that record different path-dependent constraints generically give non-isomorphic maps. Hence

$$d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) > 0 \tag{14}$$

The postulate is to be tested. Scientific observation is a regularized case of external observation. Proposition 3.3 supports the position of Paper 1 on the hard problem, that observation from without does not reproduce the map within. It does not resolve the hard problem.

The note also states an impossibility theorem for frictionless drift and a partition theorem. They are outside the series [ruled].

## Worked Case

One minimal system runs all operators. All values are reproducible from the matrices listed.

Setup. $V_S = \{z_1, z_2, z_3, z_4\}$, $\Lambda_S$ the path $z_1 - z_2 - z_3 - z_4$, $\mu_S$ uniform. $\pi(z_1) = \pi(z_4) = m_1$, $\pi(z_2) = m_2$, $\pi(z_3) = m_3$. $K_M$ is the triangle with edges $(m_1 m_2,\ m_2 m_3,\ m_3 m_1)$, each oriented from the first vertex to the second, no face, and $G = \operatorname{diag}(1, 1, g)$. With rows $m_1, m_2, m_3$,

$$\partial_1 = \begin{pmatrix} -1 & 0 & 1 \\ 1 & -1 & 0 \\ 0 & 1 & -1 \end{pmatrix}, \qquad \Delta_0\big|_{g=1} = \begin{pmatrix} 2 & -1 & -1 \\ -1 & 2 & -1 \\ -1 & -1 & 2 \end{pmatrix}$$

The task is to go from $z_1$ to $m_3$, so $\zeta = (1, 0, -1)$.

Flow at $g = 1$. $\phi = (\tfrac13, 0, -\tfrac13)$ and $j = (\tfrac13, \tfrac13, -\tfrac23)$. The extracted route is $\gamma_j = (m_1, m_3)$, the direct edge with flow $\tfrac23$. The spectrum of $\Delta_0$ is $\{0, 3, 3\}$, so $\lambda_2 = 3$, and $\lambda_\zeta = 2 / \tfrac23 = 3$.

Lift. $\operatorname{lift}((m_1, m_3) \mid z_1) = 0$ and $\operatorname{lift}((m_1, m_2, m_3) \mid z_1) = 1$. The shortcut exists only because $z_4$ was merged with $z_1$. The trigger fires on the lift, $\Gamma_B$ contains the route through $m_2$, and the regime is control. Both gaps equal 3, so the gap does not detect the alias. The lift does. With $\beta_1 = 1$ and $\ker \Delta_1$ spanned by $(1, 1, 1)$, the harmonic parts of the two route chains are $-\tfrac13$ and $\tfrac23$ per edge. They do not separate the supported route from the unsupported one.

Reconciliation by reweighting. Let $g$ fall from $1$ to $0^+$ on the retained edge. The nonzero spectrum of $\Delta_1$ equals that of $\Delta_0$, $\{3, 1 + 2g\}$, so $\det{}' \Delta_1 = 3(1 + 2g)$ and by (9)

$$\frac{d}{dt} \log \operatorname{Tor} = \frac{\dot{g}}{1 + 2g}, \qquad \Delta \log \operatorname{Tor} = -\tfrac12 \ln 3 \tag{15}$$

$\beta_1 = 1$ throughout, since the edge is retained.

Deletion. Removing the edge changes the chain space: $\beta_1 = 0$, $\lambda_2 = \lambda_\zeta = 1$ and $j = (1, 1)$ along the supported route.

Distortion. With (10), $d_{\mathcal{SM}} = \tfrac{22}{16}$ before deletion and $\tfrac{22}{16}$ after it. On $\{z_1, z_2, z_3\}$ with renormalized uniform measure it falls from $\tfrac29$ to $0$. Local repair need not improve global distortion, so task-conditional and global fidelity are reported separately.

Splitting. Splitting $m_1$ into one vertex for $z_1$ and one for $z_4$ is a remap. The map becomes isometric to the territory and $d_{\mathcal{SM}} = 0$.

Reweighting, deletion and splitting remain three distinct operations.

## Bench

A fixed classifier is applied to finite cases whose navigational facts are known independently (def). A pass means that the classifier reports these facts without exceptions added after the fact.

| Case | Construction | Required result |
|---|---|---|
| A | two dense clusters, weak bridge, task inside one cluster | small $\lambda_2$ alone does not trigger control |
| B | the worked case | a large gap does not hide a zero lift |
| C | a cycle whose routes all lift | $\beta_1 > 0$ alone does not trigger control |
| D | a transition present in $\mathcal{L}$ and omitted from $\mathcal{S}$ | failure under $\mathcal{S}$ is not called impossibility |
| E | slow drift of one weight, no change of topology | no regime change follows automatically |
| F | reweighting without splitting, as in the worked case | local distortion falls, global stays $\tfrac{22}{16}$ |
| G | Bernoulli family, $g_F = 1/(y(1-y))$ | varying discriminability at zero curvature is represented |

## Open

1. Control work on $K_M$, and the costs of weight updates and maintenance.
2. Whether reconciliation of weights while an alternative exists belongs to control, as assumed here, or to remap.
3. How the agent's costs set $\epsilon^\ast$, and its relation to $\kappa^\ast$.
4. A probabilistic lift for stochastic execution.
5. Remap after repeated failure under control on the same instance while $\Gamma_B$ is not empty.
6. Confidence in relation to the envelope (12).
7. Conditions on the samplings under which the postulate in Proposition 3.3 becomes a theorem.
8. Exploratory: determinant-line geometry as a unifying structure. The note keeps it as a candidate.
