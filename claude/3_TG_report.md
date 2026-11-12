# Translation Geometry

Report, draft 0.2, 13 November 2026. Kernel: `0_LSMN_kernel.md` §3. Baseline: the research note for Paper 3. Tags: [ruled] marks a departure decided by the authors, [inference] marks a proposal of this draft, [open] marks a form not fixed.

Papers 1 and 2 argue with stand-ins: a combinatorial territory, a smooth map with the Fisher metric, and curvature against a critical level. This report replaces each stand-in with an operator on a pair of discrete complexes. It contains definitions, propositions and one computed example. It contains no empirical claims.

## Complexes

The chain of the series is $\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}$: landscape, territory, map, navigation.

The territory is a relational complex $K_S$ with vertex set $V_S$, vertices $z$, adjacency matrix $\Lambda_S$, metric $\operatorname{dist}_S$ and sampling density $\mu_S$. It is a parochially sampled record of encounters. $\Lambda_S$ may be symmetric or asymmetric. $K_S$ carries no potential and no gradient.

The map is a simplicial complex $K_M$ with vertex set $V_M$, vertices $m$, oriented edge set $E_M$, positive diagonal edge weights $G$, boundary operators $\partial_1$ (edges to vertices) and $\partial_2$ (faces to edges), and metric $\operatorname{dist}_M$. The map does not create options. It orders them.

The compression is a surjection $\pi: V_S \twoheadrightarrow V_M$ that is not injective. For $m \in V_M$, $P_m$ is the diagonal projector onto the fiber $\pi^{-1}(m)$. A route is a sequence $\gamma = (m_0, m_1, \dots)$ in $K_M$.

| | $K_S$ | $K_M$ |
|---|---|---|
| role | preserves observed constraints | enables navigation |
| gradients | none | manufactured |
| reversibility | execution is irreversible | virtual routes can be rejected |
| structure | relations | weights, potential, flow |

## Identification

Opacity poses the problem of identification, and relations are its primitive. The operator is the Hodge Laplacian of degree zero:

$$\Delta_0 = \partial_1 G\, \partial_1^\top \tag{1}$$

with eigenvalues $0 = \lambda_1 \le \lambda_2 \le \dots$ For a connected $K_M$, $\lambda_2 > 0$. Connectivity alone supplies no direction. Direction requires a goal vector $\zeta$ with $\mathbf{1}^\top \zeta = 0$, positive at the source and negative at the sink:

$$\Delta_0 \phi = \zeta, \qquad \phi = \Delta_0^\dagger \zeta, \qquad j = -G\, \partial_1^\top \phi \tag{2}$$

$\phi$ is the potential and $j$ is the manufactured flow. At each vertex, $j$ ranks the outgoing edges. This is the rank offering of Paper 1.

**Proposition 3.1 (gradient manufacture).** Let $K_M$ be connected and $\mathbf{1}^\top \zeta = 0$. Then (2) has a solution $\phi$ that is unique up to an additive constant, and $j$ is unique.

*Proof.* $\Delta_0$ is symmetric and positive semidefinite with $\ker \Delta_0 = \operatorname{span}(\mathbf{1})$. Since $\zeta \perp \mathbf{1}$, $\zeta$ lies in the range of $\Delta_0$. Two solutions differ by a multiple of $\mathbf{1}$, and $\partial_1^\top \mathbf{1} = 0$. $\square$

Collapse of the spectral gap. Let $\epsilon^\ast$ be the critical level of $\lambda_2$. Since $\lVert \Delta_0^\dagger \rVert_2 = \lambda_2^{-1}$, a perturbation $\delta\zeta$ changes the potential by at most $\lambda_2^{-1} \lVert \delta\zeta \rVert$, and the bound is attained. The relaxation time of diffusion on $K_M$ is

$$t_{\mathrm{rel}} \propto \lambda_2^{-1} \tag{3}$$

When $\lambda_2 \le \epsilon^\ast$ across a bottleneck, the ranking becomes sensitive to small errors and settles slowly. Drift stalls. This is the operational form of high curvature in its first sense: small changes with large consequences.

## Composition

Contingency poses the problem of composition, and functions are its primitive. The operator of degree one is

$$\Delta_1 = \partial_1^\top \partial_1 + \partial_2 \partial_2^\top \tag{4}$$

Every flow on the edges splits orthogonally:

$$j = \partial_1^\top u + \partial_2 v + h, \qquad h \in \ker \Delta_1, \qquad \beta_1 = \dim \ker \Delta_1 \tag{5}$$

The first part is a gradient flow, the second circulates around filled faces, and the harmonic part $h$ circulates around cycles that bound no face. $\beta_1$ counts those cycles. A harmonic cycle is a topological feature of the map. It does not by itself signal a contradiction with the territory.

The test of a route against the territory is the lift functional. For a start $z_0 \in \pi^{-1}(m_0)$,

$$\operatorname{lift}(\gamma \mid z_0) = \mathbf{1}_{z_0}^\top P_{m_0} \prod_{i \ge 1} \big(\Lambda_S P_{m_i}\big)\, \mathbf{1} \tag{6}$$

It counts the paths in $K_S$ from $z_0$ that project onto $\gamma$. If $\operatorname{lift} > 0$, the route is executable. If $\operatorname{lift} = 0$, the compression has joined parts of the territory that are not connected, and the route exists only in the map. Virtual rollout rejects it before execution. This is the exact form of the virtual backtracking of Paper 2.

The supported alternatives to a route are

$$\Gamma(\gamma) = \{\gamma' \ne \gamma : \gamma' \text{ reaches } \zeta,\ \operatorname{lift}(\gamma' \mid z_0) > 0\} \tag{7}$$

## Persistence

Transience poses the problem of persistence, and dynamics are its primitive. Two operators track how the map changes and how far it stands from the territory.

Torsion. With $\det{}'$ the product of the nonzero eigenvalues,

$$\log \operatorname{Tor}(K_M) = \frac12 \sum_i (-1)^{i+1}\, i\, \log \det{}' \Delta_i \tag{8}$$

**Proposition 3.4 (torsion variation).** Along a smooth family $\Delta_i(t)$ on which each $\dim \ker \Delta_i$ is constant,

$$\frac{d}{dt} \log \operatorname{Tor} = \frac12 \sum_i (-1)^{i+1}\, i\, \operatorname{Tr}\big(\Delta_i^\dagger \dot{\Delta}_i\big) \tag{9}$$

*Proof.* At constant rank, $\tfrac{d}{dt} \log \det{}' \Delta_i = \operatorname{Tr}(\Delta_i^\dagger \dot{\Delta}_i)$. $\square$

Where the rank changes, the total shift is the integral of (9) up to the change plus a discrete jump. Log torsion is a signed observable of the deformation of the map. It is not identified with control work [ruled].

Distortion. An agent's own territory and map share a registration through $\pi$. The anchored distortion is

$$d_{\mathcal{SM}} = \sum_{z, z' \in V_S} \mu_S(z)\, \mu_S(z')\, \big\lvert \operatorname{dist}_S(z, z') - \operatorname{dist}_M(\pi z, \pi z') \big\rvert^2 \tag{10}$$

Two maps without a shared registration are compared by the unconstrained distance. For metric measure spaces $\mathcal{X}$, $\mathcal{Y}$ with measures $\mu_X$, $\mu_Y$,

$$d_{\mathrm{GW}}(\mathcal{X}, \mathcal{Y}) = \frac12 \inf_{\text{couplings of } \mu_X, \mu_Y} \iint \big\lvert \operatorname{dist}_X(x, x') - \operatorname{dist}_Y(y, y') \big\rvert^2 \tag{11}$$

integrated against the coupling twice. It applies to two agents, to an agent and an observer, and to the same agent awake and asleep.

## Regimes

The regimes of Paper 1 are defined by curvature $\kappa$ against a critical level $\kappa^\ast$. Curvature carries two things: how far the map diverges from the territory, and how much the divergence matters. Each has an operator.

| Papers 1 and 2 | This paper |
|---|---|
| $\kappa < \kappa^\ast$ | $\lambda_2 > \epsilon^\ast$ and $\operatorname{lift}(\gamma \mid z_0) > 0$ |
| $\kappa \ge \kappa^\ast$ | $\lambda_2 \le \epsilon^\ast$, or $\operatorname{lift}(\gamma \mid z_0) = 0$ |
| Fisher metric, natural gradient | $\Delta_0$, $\lambda_2$, $\phi$, $j$ |
| branch singularities | $\Delta_1$, $\beta_1$, $\operatorname{lift}$ |
| metric decay, metric shift | $\operatorname{Tor}$, $d_{\mathcal{SM}}$, $d_{\mathrm{GW}}$ |

Drift. The gap is open and the planned route lifts. Compression is lossy, so $d_{\mathcal{SM}} > 0$ in general, and the loss is benign: the agent follows $j$. The note adds confidence, the low-cost correction of minor divergence that does not halt progress.

Control. The gap has collapsed or the planned route does not lift, and $\Gamma(\gamma) \ne \emptyset$. A control field $w \ne 0$ moves the agent to a supported alternative. Reconciliation then adjusts $G$ so that the next ranking no longer offers the failed route.

Remap. $\Gamma(\gamma) = \emptyset$. Control cannot restore a viable correspondence. The complex $K_M$ or the projection $\pi$ is revised.

The discrete form of $w$ and of the control work $\mathcal{W}$ is open. A candidate [inference] is a correction $w \in \mathbb{R}^{E_M}$ to the flow, with $\mathcal{W} = \sum_t w_t^\top G^{-1} w_t$.

## Envelope

The envelope of assured navigation is the set of start and goal pairs joined by a supported route within the budget $B$:

$$\mathcal{E} = \{(z_0, \zeta) : \exists\, \gamma \text{ that reaches } \zeta,\ \operatorname{lift}(\gamma \mid z_0) > 0,\ \text{cost of } \gamma \le B\} \tag{12}$$

It contains everything reached under drift or control [ruled]. The note restricts the envelope to drift. The definition here follows the ruling. Remap is defined independently of $\mathcal{E}$, as in the note, and it can enlarge $\mathcal{E}$ as a consequence.

## Viability

The machinery that performs the virtual test (6) and the reconciliation has a cost. Let $\ell$ be the loss from a failed physical conjecture, $B_F$ the budget for virtual search, $B_w$ the budget for reconciliation and $B_0$ the cost of its maintenance. It is viable iff

$$\mathbb{E}[\ell \text{ avoided}] > \mathbb{E}[B_F + B_w + B_0] \tag{13}$$

The left side grows with the number of mutually exclusive alternatives and with the irreversible cost of untested execution. Paper 4 uses (13) for the lower bound of consciousness.

## Propositions

**Proposition 3.2 (control-work necessity).** Let $\gamma_j$ be the route obtained from $z_0$ by following $j$, and let $\operatorname{lift}(\gamma_j \mid z_0) = 0$. Then no trajectory with $w \equiv 0$ and $\dot{G} \equiv 0$ reaches $\zeta$.

*Proof.* With $w \equiv 0$ and $G$ fixed, the agent attempts $\gamma_j$. By (6) no path in $K_S$ from $z_0$ projects onto $\gamma_j$, so execution fails at the first edge at which the partial product in (6) vanishes. $\square$

Reaching the goal therefore requires $w \ne 0$, which gives $\mathcal{W} > 0$, or a change of $G$, which by (9) changes log torsion in general. This is the formal content. Paper 1 identifies the mode of operation that it describes with conscious engagement. That identification is a postulate and is not proved here.

**Proposition 3.3 (perspective asymmetry).** Let $\mathcal{M}_{\mathrm{int}}$ be the map of an agent and $\mathcal{M}_{\mathrm{ext}}$ the map that any observer forms of the same landscape, each obtained by its own sampling and its own non-injective compression. If the two are not isomorphic as metric measure spaces, then

$$d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) > 0 \tag{14}$$

*Argument.* The distance (11) vanishes only between isomorphic metric measure spaces. An isomorphism requires equal distributions of pairwise distances. Two samplings that record different path-dependent constraints give different distance distributions except in special cases. The condition is generic and is not derived from the chain alone. Scientific observation is a regularized case of external observation.

Proposition 3.3 is the formal support for the position of Paper 1 on the hard problem: observation from without does not reproduce the map within. Proposition 3.2 supports the complementary claim that the work of control leaves traces.

The note also states an impossibility theorem for frictionless drift and a partition theorem. They are outside the series [ruled].

## Worked Case

One minimal system runs all operators.

Setup. $V_S = \{z_1, z_2, z_3, z_4\}$ with $\Lambda_S$ the path $z_1 - z_2 - z_3 - z_4$ and uniform $\mu_S$. The compression is $\pi(z_1) = \pi(z_4) = m_1$, $\pi(z_2) = m_2$, $\pi(z_3) = m_3$. $K_M$ is the triangle on $m_1, m_2, m_3$ with unit weights, no face, and edges ordered $(m_1 m_2,\ m_2 m_3,\ m_3 m_1)$. The task is to go from $z_1$ to $m_3$, so $\zeta = (1, 0, -1)$.

Flow. From (2), $\phi = (\tfrac13, 0, -\tfrac13)$ and $j = (\tfrac13, \tfrac13, -\tfrac23)$. The map prefers the direct edge from $m_1$ to $m_3$, with flow $\tfrac23$, over the route through $m_2$, with flow $\tfrac13$. Here $\lambda_2 = 3$.

Lift. From (6), $\operatorname{lift}((m_1, m_3) \mid z_1) = 0$ and $\operatorname{lift}((m_1, m_2, m_3) \mid z_1) = 1$. The preferred shortcut exists only because $z_4$ was merged with $z_1$. The planned route fails, an alternative is supported, and the regime is control. Here $\beta_1 = 1$. The harmonic component has magnitude $\tfrac13$ per edge for the shortcut and $\tfrac23$ for the supported route, which confirms that the harmonic part does not separate the two. The lift does.

Distortion. From (10), $d_{\mathcal{SM}} = \tfrac{22}{16}$. Restricted to $\{z_1, z_2, z_3\}$ it is $\tfrac29$.

Reconciliation. Let the weight of the false edge fall from $1$ to $0$. Then $\det{}' \Delta_1 = 3(1 + 2 G_{m_3 m_1})$, and by (9)

$$\frac{d}{dt} \log \operatorname{Tor} = \frac{\dot{G}_{m_3 m_1}}{1 + 2 G_{m_3 m_1}}, \qquad \Delta \log \operatorname{Tor} = -\tfrac12 \ln 3 \tag{15}$$

At weight zero the cycle opens, $\beta_1$ goes from $1$ to $0$, and the flow becomes $j = (1, 1, 0)$ along the supported route. The distortion on $\{z_1, z_2, z_3\}$ falls to $0$. Splitting $m_1$ into two vertices, one for $z_1$ and one for $z_4$, is a remap and brings $d_{\mathcal{SM}}$ to $0$.

## Open

1. The discrete control field and control work.
2. Whether the reconciliation of weights while an alternative exists belongs to control, as assumed here, or to remap.
3. How the agent's costs set $\epsilon^\ast$, and its relation to $\kappa^\ast$.
4. Confidence in relation to the envelope (12).
5. A proof of Proposition 3.3 from conditions on the samplings.
6. Exploratory: determinant-line geometry as a unifying structure for the operators. The note keeps it as a candidate.
