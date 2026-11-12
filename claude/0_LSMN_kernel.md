# LSMN Kernel

Version 0.7, 12 November 2026. One kernel for Papers 1 to 4. [assumed]: proposed, not ruled. [open]: form not fixed.

Rule: one meaning per symbol. Every symbol is in the registry. A case pair denotes related objects only: $(O, o)$, $(C, c)$, $(G, g)$, $(w, \mathcal{W})$, $(X, x)$. Regimes, results and tests carry words or section numbers, never single letters.

## 0. Registry

| Symbol | Meaning |
|---|---|
| $\mathcal{L}, \mathcal{S}, \mathcal{M}, \mathcal{N}$ | Landscape, Territory, Map, Navigation |
| $\sigma, \pi, \gamma$ | sampling $\mathcal{L} \to \mathcal{S}$, compression $\mathcal{S} \to \mathcal{M}$, trajectory in $\mathcal{M}$ |
| $K_S, V_S, z, \Lambda_S, \operatorname{dist}_S, \mu_S$ | Territory: complex, vertex set, vertex, adjacency matrix, metric, measure |
| $K_M, V_M, m, E_M, e, G, \partial_1, \operatorname{dist}_M$ | Map: complex, vertex set, vertex, edge set, edge (instance), edge weights, incidence, metric |
| $\Delta_i$ | Hodge Laplacian of degree $i$ on $K_M$ |
| $P_m, \mathbf{1}_m, \mathbf{1}$ | projector onto $\pi^{-1}(m)$, indicator vector of $m$ or $z$, all-ones vector |
| $\zeta, \phi, j, j_{\mathcal{L}}$ | goal vector, potential, manufactured flow, flow under the potential of $\mathcal{L}$ |
| $\Gamma_e, \operatorname{lift}$ | supported alternatives to $e$, lift functional |
| $U, I, N$ | Unsurveyability, Intractability, Intransigence |
| $O, C, T$ | Opacity, Contingency, Transience |
| $o, c, \vartheta$ | degrees of $O$, $C$, $T$ |
| $\nu, \lambda$ | count of relevant distinctions, scale |
| $d_e, \bar{d}_e, d_{\mathcal{SM}}$ | divergence at $e$, its expectation, total divergence |
| $s_e, \rho_e, q_e$ | consequence, use by $\gamma$, warrant |
| $g_e$ | effective conductance at $e$ |
| $\tau$ | tolerance |
| $\epsilon^\ast, \kappa^\ast$ | critical level: measurable, conceptual |
| $\kappa, y, d(y)$ | smooth stand-in: curvature, point, divergence at $y$ |
| $a^\circ_e, a_e, B$ | demand at $e$, allocation to $e$, allocation budget |
| $f, h$ | monitoring function, recalibration function |
| $\operatorname{reg}(e)$ | regime at $e$: drift, control or remap |
| $w, \mathcal{W}$ | control, control work |
| $\operatorname{Tor}$ | Ray-Singer torsion of $K_M$ |
| $X, x_t, k, \operatorname{val}, \operatorname{Nbr}$ | search space, state at $t$, number of options, objective, neighborhood |
| $\Omega_t, \beta(t), \iota, r$ | options reachable, budget spent, information held, decay rate function |
| $\ell_C, \ell_T$ | loss from $C$, loss from $T$ |
| $B_{\mathrm{tot}}, B_O, B_C, B_T, B_{\mathrm{step}}$ | navigation budget and its parts |
| $\operatorname{met}_e, \eta$ | metabolic expenditure at $e$, efficiency |
| $\hat{\ }$ | estimator |
| $t$ | time |

## 0.1 Model

$\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}$

$\pi: V_S \twoheadrightarrow V_M$, non-injective. $\gamma = (m_0, m_1, \dots)$, finite, toward $\zeta$, $\mathbf{1}^\top \zeta = 0$. Agent: $(\mathcal{S}, \mathcal{M}, \pi, \zeta, B)$.

$U = I + N$, $N = (O, C, T)$.

## 1. CAT

$$a^\circ_e = f(\rho_e s_e \bar{d}_e) + h_{\operatorname{reg}(e)}(q_e), \qquad q_e = d_e s_e$$

$f$, $h$ nondecreasing, zero at zero, positive elsewhere. $f$ continuous at zero. $h_{\text{drift}} < h_{\text{control}} < h_{\text{remap}}$ on $q_e > 0$. Forms [open].

Rationing [assumed]: instances are served in descending order of $a^\circ_e$ until $B$ is spent. $0 \le a_e \le a^\circ_e$, $\sum_e a_e = \min(B, \sum_e a^\circ_e)$.

Expected divergence [assumed]: $\vartheta > 0 \Rightarrow \bar{d}_e > 0$ for every $e$ not checked at the current $t$.

$$\text{conscious}(e) \iff a_e > 0, \qquad \text{conscious}(\text{agent}) \iff \textstyle\sum_e a_e > 0, \qquad \text{intensity}(e) = a_e$$

$\Gamma_e = \{\gamma' : e \notin \gamma',\ \gamma' \text{ reaches } \zeta,\ \gamma' \text{ supported by } \mathcal{S}\}$.

| $\operatorname{reg}(e)$ | Condition | Repair acts on |
|---|---|---|
| drift | $q_e \le \tau$ | $\gamma$ |
| control | $q_e > \tau$, $\Gamma_e \ne \emptyset$ | choice in $\Gamma_e$, $w \ne 0$ |
| remap | $q_e > \tau$, $\Gamma_e = \emptyset$ | $(\mathcal{M}, \pi)$ |

Result 1.1. Not $I$, with survey of $\mathcal{L}$ at every $t$, $\Rightarrow \pi$ isometric $\Rightarrow d_e = \bar{d}_e = 0\ \forall e \Rightarrow a_e = 0\ \forall e$.
Result 1.2. $\vartheta > 0$, $B > 0$, and $\rho_e s_e > 0$ for some unchecked $e$ $\Rightarrow \sum_e a_e > 0$, also when $q_e = 0\ \forall e$.
Result 1.3. $a_e = 0$ if $\rho_e s_e \bar{d}_e = 0$ and $d_e = 0$, or if $e$ is reached after $B$ is spent. Processing at $e$ is not excluded.
Result 1.4. $B = 0 \Rightarrow a_e = 0\ \forall e$.
Result 1.5. There are $e, e'$ with $q_e = q_{e'} > \tau$, $s_e > s_{e'}$, $\Gamma_e \ne \emptyset$, $\Gamma_{e'} = \emptyset$ and $h_{\operatorname{reg}(e)}(q_e) < h_{\operatorname{reg}(e')}(q_{e'})$.
Result 1.6. $d_e = 0$ and $\bar{d}_e \to 0 \Rightarrow a_e \to 0$.

Postulate 1.7. $\text{effort}(e) \equiv h_{\operatorname{reg}(e)}(q_e)$. $\text{salience}(e) \equiv f(\rho_e s_e \bar{d}_e)$. Identification, not derived.

Stand-in 1.8. $\mathcal{M}$ smooth, $\dot{y} = -\nabla \phi(y) + w(y)$. $\kappa(y)$ stands for $s_e$. $\kappa^\ast(y) = \tau / d(y)$. $q \le \tau \iff \kappa \le \kappa^\ast$.

## 2. UNS

$X$: arrangements of $k$ interacting options, $\lvert X \rvert \ge k!$. $\operatorname{val}: X \to \mathbb{R}$.

$$I \iff \lim_{\lambda \to \infty} \frac{\log \nu(\mathcal{S}_\lambda)}{\dim \mathcal{M}} = \infty, \qquad I \Rightarrow x_{t+1} \in \operatorname{Nbr}(x_t)$$

| | Obstruction | Degree | Agent manufactures | Ordering | Primitive |
|---|---|---|---|---|---|
| $O$ | local gradient absent or unrelated to global | $o = 1 - \operatorname{corr}(\nabla_{\mathrm{loc}} \operatorname{val}, \nabla_{\mathrm{glob}} \operatorname{val}) \in [0,1]$ [assumed] | flow $j$ | comes with (none) | relations |
| $C$ | steps foreclose options | $c \in [0,1]$, cost of reversion | virtual $\gamma$ before the step | follows from (logical, negotiable) | functions |
| $T$ | $X$ varies in $t$ | $\vartheta \ge 0$, rate of change | update of $\gamma$ on divergence | follows after (temporal, non-negotiable) | dynamics |

Reversion at $c < 1$ from $t$ to $t' < t$: $\Omega_t \leftarrow \Omega_{t'}$. $\beta(t) - \beta(t')$ is not restored. Information: $\dot{\iota} = -r(\vartheta)\, \iota$, $r(0) = 0$, $r$ increasing [open].

Coupling [assumed]: $\ell_C = \ell_C(o \cdot c)$, $\ell_C(0) = 0$. $\ell_T = \ell_T(\vartheta, \lvert \gamma \rvert)$, $\ell_T(0, \cdot) = \ell_T(\cdot, 0) = 0$. Both increasing.

Cycle: $j \to \gamma \to \text{step} \to \text{update}$.

Heuristic: $B_{\mathrm{tot}} = B_O + B_C + B_T + B_{\mathrm{step}}$. The heuristic is the $\gamma$ returned by the cycle under $B_{\mathrm{tot}}$, revised at each $t$. Stop when the expected gain in $\operatorname{val}$ of one more pass is below its cost. Not $I$ $\Rightarrow B_O = B_C = B_T = 0$ and $\gamma$ is optimal.

Link to §1: $B \le B_{\mathrm{tot}} - B_{\mathrm{step}}$. Which of $B_O, B_C, B_T$ count toward $B$ is [open].

Cube: $([o > 0], [c > 0], [\vartheta > 0]) \in \{0,1\}^3$ are extreme types. Environments lie in $[0,1]^2 \times \mathbb{R}_{\ge 0}$. That $O, C, T$ exhaust $N$ is conjectured.

## 3. TG

$$\Delta_0 = \partial_1 G\, \partial_1^\top, \qquad \Delta_0 \phi = \zeta, \qquad j = -G\, \partial_1^\top \phi$$

For $e = (m, m') \in E_M$, with $\pi^{-1}(e) := \pi^{-1}(m) \cup \pi^{-1}(m')$:

$$\rho_e = \lvert j_e \rvert, \qquad s_e = g_e^{-1}, \qquad g_e = \big[(\mathbf{1}_m - \mathbf{1}_{m'})^\top \Delta_0^\dagger (\mathbf{1}_m - \mathbf{1}_{m'})\big]^{-1}$$

$$d_e = \sum_{z, z' \in \pi^{-1}(e)} \mu_S(z) \mu_S(z')\, \lvert \operatorname{dist}_S(z,z') - \operatorname{dist}_M(\pi z, \pi z') \rvert^2$$

$$d_{\mathcal{SM}} = \sum_{z, z' \in V_S} \mu_S(z) \mu_S(z')\, \lvert \operatorname{dist}_S(z,z') - \operatorname{dist}_M(\pi z, \pi z') \rvert^2$$

$$\operatorname{lift}(\gamma \mid z_0) = \mathbf{1}_{z_0}^\top P_{m_0} \prod_{i \ge 1} \big(\Lambda_S P_{m_i}\big) \mathbf{1}, \qquad \gamma \text{ supported by } \mathcal{S} \iff \operatorname{lift}(\gamma \mid z_0) > 0$$

$\operatorname{lift}(\gamma \mid z_0) = 0 \Rightarrow d_e := \infty$ at the first failing edge.

$$\epsilon^\ast(e) = d_e / \tau, \qquad q_e \le \tau \iff g_e \ge \epsilon^\ast(e), \qquad d_e = 0 \Rightarrow \epsilon^\ast(e) = 0 \Rightarrow \operatorname{reg}(e) = \text{drift}$$

$o = 1 - \operatorname{corr}(j, j_{\mathcal{L}})$, with $j_{\mathcal{L}}$ the flow under the potential of $\mathcal{L}$ [assumed]. $\vartheta$: $\dot{d}_{\mathcal{SM}} > 0$ absent update. $\bar{d}_e$ as a function of $\vartheta$ and time since last check [open]. $c$ on $\Lambda_S$ [open]. $w$ on $K_M$ [open].

Remap, signed observable at constant rank: $\frac{d}{dt} \log \operatorname{Tor} = \frac{1}{2} \sum_i (-1)^{i+1}\, i \operatorname{Tr}(\Delta_i^\dagger \dot{\Delta}_i)$. $\mathcal{W} = \int \lVert w \rVert^2 dt \ge 0$. $\log \operatorname{Tor} \ne \mathcal{W}$.

Worked case 3.1. $V_S = \{z_1, z_2, z_3, z_4\}$, path. $\pi: z_1, z_4 \mapsto m_1$, $z_2 \mapsto m_2$, $z_3 \mapsto m_3$. $K_M$ is a triangle with unit weights. Goal: $m_1$ to $m_3$, from $z_1$.
$\phi = (\tfrac13, 0, -\tfrac13)$. $j = (\tfrac13, \tfrac13, -\tfrac23)$ on $(m_1 m_2, m_2 m_3, m_3 m_1)$.
$\operatorname{lift}((m_1, m_3) \mid z_1) = 0$. $\operatorname{lift}((m_1, m_2, m_3) \mid z_1) = 1$. Hence $\Gamma_e \ne \emptyset$ and $\operatorname{reg}(e) = \text{control}$ at $e = m_3 m_1$.
$d_{\mathcal{SM}} = \tfrac{22}{16}$. On $\{z_1, z_2, z_3\}$: $\tfrac29$, and $0$ as $G_{m_3 m_1} \to 0$.
$\det{}' \Delta_1 = 3(1 + 2 G_{m_3 m_1})$. $\log \operatorname{Tor}$ changes by $-\tfrac12 \ln 3$ as $G_{m_3 m_1}$ goes from $1$ to $0$.
Harmonic component: $\tfrac13$ for $(m_1, m_3)$, $\tfrac23$ for $(m_1, m_2, m_3)$. It does not separate supported from unsupported routes.

## 4. MC

$a_e$ is not observed. Traces: $\operatorname{met}_e \ge 0$ and $\mathcal{W}$ at $e$. $\eta = \mathcal{W} / \operatorname{met} \in (0, 1]$.

Assumption 4.1. $\operatorname{met}_e$ is increasing in $a_e$.
Assumption 4.2. $\mathcal{W} > 0$ at $e$ $\Rightarrow \operatorname{reg}(e) = \text{control}$.
Estimators $\hat{\Delta}_0, \hat{g}_e, \hat{\rho}_e, \hat{d}_e, \hat{\tau}$ [open]. No effect size is stated before the fact-check pass.

Presence: $a_e > 0$ against $a_e = 0$.
Test 4.3. Same input at $e$, reported against unreported: $\operatorname{met}_e$ differs, and only at $e$.
Test 4.4. $\rho_e s_e \bar{d}_e \to 0$: report and $\operatorname{met}_e$ decline together.
Test 4.5. $\Pr(\text{change at } e \text{ detected})$ is increasing in $\rho_e s_e$ at fixed physical change.
Test 4.6. Anesthesia, dreamless sleep: $\operatorname{met}_e$ does not depend on $d_e$ or $\rho_e s_e$, for all $e$.

Degree: size of $a_e$.
Test 4.7. At $d_e = 0$: $\operatorname{met}_e$ is increasing in $\hat{\rho}_e \hat{s}_e$.
Test 4.8. Control begins at $\hat{g}_e < \hat{d}_e / \hat{\tau}$. At $\hat{d}_e = 0$ no $\hat{g}_e$ triggers it.
Test 4.9. Response time near the transition is increasing in $\hat{s}_e$.
Test 4.10. At matched $q_e$: $\operatorname{met}_e$ is larger for $\Gamma_e = \emptyset$ than for $\Gamma_e \ne \emptyset$.
Test 4.11. Degraded input lowers evidence for $d_e$. It does not raise $h$.

| Dissociation | Behavior | Prediction |
|---|---|---|
| Ketamine, dreaming | absent | $a_e > 0$ on internal instances, actuators uncoupled |
| Automatism | present | $a_e = 0$ on the driving instances |
| Masked stop signal | braking | brake at $a_e = 0$. The brake marks conflict, not presence |
| Flow | high | $\eta$ high |

Refutation 4.12. Presence varies at fixed $(d_e, \rho_e s_e, \bar{d}_e)$ with $B > 0$. Or Tests 4.5, 4.8 or 4.10 fail under valid estimators.

## 5. Correspondence

| Construct | Papers 1, 2 | Paper 3 | Paper 4 |
|---|---|---|---|
| consequence | $\kappa(y)$ | $s_e = g_e^{-1}$ | $\hat{s}_e$ |
| use | route through $y$ | $\rho_e = \lvert j_e \rvert$ | $\hat{\rho}_e$ |
| divergence | map off at $y$ | $d_e$, $\operatorname{lift} = 0$ | $\hat{d}_e$ |
| critical level | $\kappa^\ast(y) = \tau / d(y)$ | $\epsilon^\ast(e) = d_e / \tau$ | $\hat{\tau}$, Test 4.8 |
| alternatives | map holds another route | $\Gamma_e$ | Test 4.10 |
| allocation | $a_e$ | $a_e$ | $\operatorname{met}_e$ under 4.1 |
| control | $w$, $\mathcal{W}$ | $w$ on $K_M$ [open] | $\mathcal{W}$ under 4.2 |
| Opacity | $o$ | $1 - \operatorname{corr}(j, j_{\mathcal{L}})$ [assumed] | [open] |
| Contingency | $c$ | on $\Lambda_S$ [open] | [open] |
| Transience | $\vartheta$ | $\dot{d}_{\mathcal{SM}}$ absent update | [open] |

Dependency: §2 $\to$ §1 $\to$ §3 $\to$ §4. Theorems on partition and perspective are outside the series unless a later version requires one.
