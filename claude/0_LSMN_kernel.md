# LSMN Kernel

Version 0.4, 12 November 2026. One kernel for Papers 1 to 4. [assumed]: proposed, not ruled. [open]: form not fixed.

## 0. Model

$\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}$

$\mathcal{L}$: Landscape. $\mathcal{S}$: Territory, $(K_S, A_S, d_S, \mu_S)$ on $V_S$. $\mathcal{M}$: Map, $(K_M, W, d_M)$ on $V_M$, $E_M$, incidence $B_1$. $\pi: V_S \twoheadrightarrow V_M$, non-injective. $\mathcal{N}$: Navigation, $\gamma = (m_0, \dots, m_H) \subset K_M$ toward $b$, $\mathbf{1}^\top b = 0$.

Agent: $A = (\mathcal{S}, \mathcal{M}, \pi, b, B)$.

Unsurveyability: $U = I + N$. $I$: Intractability. $N = (O, C, T)$: Intransigence, with Opacity $O$, Contingency $C$, Transience $T$. Degrees: $o \in [0,1]$, $c \in [0,1]$, $\vartheta \ge 0$.

Instance $e$: $d_e \ge 0$ divergence. $\bar{d}_e = \mathbb{E}[d_e]$ expected divergence. $s_e \ge 0$ consequence. $\rho_e \ge 0$ use by $\gamma$. $q_e = d_e s_e$ warrant. $a_e \ge 0$ allocation. $\tau > 0$ tolerance. $u$ control. $\mathcal{W} = \int \lVert u_t \rVert^2 dt$.

## 1. CAT

$$a_e = f(\rho_e s_e \bar{d}_e) + h_{R(e)}(q_e), \qquad \sum_e a_e \le B$$

$f, h_\cdot$ nondecreasing, $f(0) = h_\cdot(0) = 0$, $h_{\mathrm{D}} < h_{\mathrm{C}} < h_{\mathrm{R}}$ on $q > 0$. Forms [open].

$$\text{conscious}(e) \iff a_e > 0, \qquad \text{conscious}(A) \iff \textstyle\sum_e a_e > 0, \qquad \text{intensity}(e) = a_e$$

$\Gamma_e = \{\gamma' : e \notin \gamma',\ \gamma' \text{ reaches } b,\ \gamma' \text{ supported by } \mathcal{S}\}$.

| $R(e)$ | Condition | Repair acts on |
|---|---|---|
| $\mathrm{D}$ (Drift) | $q_e \le \tau$ | $\gamma$ |
| $\mathrm{C}$ (Control) | $q_e > \tau$, $\Gamma_e \ne \emptyset$ | choice in $\Gamma_e$, $u \ne 0$ |
| $\mathrm{R}$ (Remap) | $q_e > \tau$, $\Gamma_e = \emptyset$ | $(\mathcal{M}, \pi)$ |

R1. $I = 0 \Rightarrow \pi$ isometric $\Rightarrow d_e = \bar{d}_e = 0\ \forall e \Rightarrow a \equiv 0$.
R2. $\vartheta > 0 \Rightarrow \bar{d}_e > 0$. With $\rho_e s_e > 0$: $a_e > 0$ at $q_e = 0$.
R3. $\rho_e s_e \bar{d}_e = 0 \wedge d_e = 0 \Rightarrow a_e = 0$. Processing at $e$ is not excluded.
R4. $B = 0 \Rightarrow a \equiv 0$.
R5. $\exists\, e, e'$: $s_e > s_{e'}$, $\Gamma_e \ne \emptyset$, $\Gamma_{e'} = \emptyset$, $h_{R(e)}(q_e) < h_{R(e')}(q_{e'})$.
R6. $d_e = 0,\ \bar{d}_e \to 0 \Rightarrow a_e \to 0$.

Postulate. $\text{effort}(e) \equiv h_{R(e)}(q_e)$. $\text{salience}(e) \equiv f(\rho_e s_e \bar{d}_e)$. Identification, not derived.

Stand-in. $(\mathcal{M}, g)$ smooth, $\dot{x} = -g^{-1} \nabla V + u$, $K(x) \sim s$, $\kappa_c(x) = \tau / d(x)$. $q \le \tau \iff K \le \kappa_c$.

## 2. UNS

$X$: arrangements of $n$ interacting options, $\lvert X \rvert \ge n!$. $f: X \to \mathbb{R}$.

$$I \iff \lim_{\alpha \to \infty} \frac{\log \nu(\mathcal{S}_\alpha)}{\dim \mathcal{M}} = \infty, \qquad I \Rightarrow x_{t+1} \in \mathrm{Nbr}(x_t)$$

| | Obstruction | Degree | Agent manufactures | Ordering | Primitive |
|---|---|---|---|---|---|
| $O$ | local gradient absent or unrelated to global | $o = 1 - \operatorname{corr}(\nabla_{\mathrm{loc}} f, \nabla_{\mathrm{glob}} f)$ [assumed] | gradient $j$ | comes with (none) | relations |
| $C$ | steps foreclose options | $c$ = cost of reversion | virtual $\gamma$ before the step | follows from (logical, negotiable) | functions |
| $T$ | $X_t$ varies | $\vartheta$ = rate of change | update of $\gamma$ on divergence | follows after (temporal, non-negotiable) | dynamics |

Reversion at $c < 1$ from $t$ to $t' < t$: $\Omega_t \leftarrow \Omega_{t'}$. $B_t - B_{t'}$ is not restored. Information: $\dot{\iota} = -k(\vartheta)\, \iota$, $k(0) = 0$, $k$ increasing [open].

Coupling [assumed]: $\ell_C = \ell_C(o \cdot c)$, $\ell_C(0) = 0$. $\ell_T = \ell_T(\vartheta, \lvert \gamma \rvert)$, $\ell_T(0, \cdot) = \ell_T(\cdot, 0) = 0$. Both increasing.

Cycle: $j \to \gamma \to \text{step} \to \text{update}$.

Heuristic: $B_{\mathrm{tot}} = B_O + B_C + B_T + B_{\mathrm{step}}$. $\gamma^\ast_t$ = output of the cycle under $B_{\mathrm{tot}}$. Stop when $\mathbb{E}[\Delta f \mid \text{one more pass}] < \text{cost}$. $I = 0 \Rightarrow B_O = B_C = B_T = 0$, $\gamma^\ast$ optimal.

Link to §1: $B \le B_{\mathrm{tot}} - B_{\mathrm{step}}$. Which of $B_O, B_C, B_T$ count toward $B$ is [open].

Cube: $(\mathbb{1}[o > 0], \mathbb{1}[c > 0], \mathbb{1}[\vartheta > 0]) \in \{0,1\}^3$ are extreme types. Environments lie in $[0,1]^2 \times \mathbb{R}_{\ge 0}$. That $O, C, T$ exhaust $N$ is conjectured.

## 3. TG

$$\Delta_0 = B_1 W B_1^\top, \qquad \Delta_0 \phi = b, \qquad j = -W B_1^\top \phi$$

For $e = (v, w) \in E_M$, $F_e = \pi^{-1}(v) \cup \pi^{-1}(w)$:

$$\rho_e = \lvert j_e \rvert, \qquad s_e = g_e^{-1}, \qquad g_e = \big[(\chi_v - \chi_w)^\top \Delta_0^\dagger (\chi_v - \chi_w)\big]^{-1}$$

$$d_e = \sum_{x, y \in F_e} \mu_S(x) \mu_S(y)\, \lvert d_S(x,y) - d_M(\pi x, \pi y) \rvert^2, \qquad D = \sum_{x, y \in V_S} \mu_S(x) \mu_S(y)\, \lvert d_S(x,y) - d_M(\pi x, \pi y) \rvert^2$$

$$\mathcal{L}_{\mathrm{lift}}(\gamma \mid x_0) = \chi_{x_0}^\top P_{m_0} A_S P_{m_1} \cdots A_S P_{m_H} \mathbf{1}, \qquad \gamma \text{ supported by } \mathcal{S} \iff \mathcal{L}_{\mathrm{lift}} > 0$$

$\mathcal{L}_{\mathrm{lift}}(\gamma \mid x_0) = 0 \Rightarrow d_e := \infty$ at the first failing edge.

$$\epsilon_c(e) = d_e / \tau, \qquad q_e \le \tau \iff g_e \ge \epsilon_c(e), \qquad d_e = 0 \Rightarrow \epsilon_c(e) = 0 \Rightarrow R(e) = \mathrm{D}$$

$o = 1 - \operatorname{corr}(j, j^\ast)$, $j^\ast$ the flow under the potential of $\mathcal{L}$ [assumed]. $\vartheta$: $\dot{D} > 0$ absent update. $\bar{d}_e$ as a function of $\vartheta$ and time since last check [open]. $c$ on $A_S$ [open]. $u_t$ on $K_M$ [open].

Remap, signed observable at constant rank: $\frac{d}{dt} \log T_{\mathrm{RS}} = \frac{1}{2} \sum_q (-1)^{q+1} q \operatorname{Tr}(\Delta_q^\dagger \dot{\Delta}_q)$. $\log T_{\mathrm{RS}} \ne \mathcal{W}$.

Worked case. $V_S = \{x_1, \dots, x_4\}$ path. $\pi: x_1, x_4 \mapsto m_1$, $x_2 \mapsto m_2$, $x_3 \mapsto m_3$. $K_M$ triangle, $W = I$, goal $m_1 \to m_3$ from $x_1$.
$\phi = (\tfrac13, 0, -\tfrac13)$, $j = (\tfrac13, \tfrac13, -\tfrac23)$.
$\mathcal{L}_{\mathrm{lift}}((m_1, m_3) \mid x_1) = 0$, $\mathcal{L}_{\mathrm{lift}}((m_1, m_2, m_3) \mid x_1) = 1 \Rightarrow \Gamma \ne \emptyset \Rightarrow R = \mathrm{C}$.
$D = \tfrac{22}{16}$. On $\{x_1, x_2, x_3\}$: $\tfrac29 \to 0$ as $w_{31} \to 0$. $\det{}' \Delta_1 = 3(1 + 2w)$, $\Delta \log T_{\mathrm{RS}} = -\tfrac12 \ln 3$.
Harmonic components: $\tfrac13$ for $(m_1, m_3)$, $\tfrac23$ for $(m_1, m_2, m_3)$. They do not separate supported from unsupported routes.

## 4. MC

$a_e$ is not observed. Traces: $E_e \ge 0$ metabolic expenditure, $\mathcal{W}_e$ control work, $\eta = \mathcal{W} / E \in (0, 1]$.
M1: $\partial E_e / \partial a_e > 0$. M2: $\mathcal{W}_e > 0 \Rightarrow R(e) = \mathrm{C}$.
Estimators $\hat{\Delta}_0, \hat{g}_e, \hat{\rho}_e, \hat{d}_e, \hat{\tau}$ [open]. No effect size is stated before the fact-check pass.

Presence ($a_e > 0$ against $a_e = 0$).
P1. Same input at $e$, reported against unreported: $\Delta E_e \ne 0$, specific to $e$.
P2. $\rho_e s_e \bar{d}_e \to 0$: report and $E_e$ decline together.
P3. $\Pr(\text{detect change at } e)$ increasing in $\rho_e s_e$ at fixed physical change.
P4. Anesthesia, dreamless sleep: $\partial E_e / \partial d_e = \partial E_e / \partial(\rho_e s_e) = 0\ \forall e$.

Degree (size of $a_e$).
D1. At $d_e = 0$: $E_e$ increasing in $\hat{\rho}_e \hat{s}_e$.
D2. Control begins at $\hat{g}_e < \hat{d}_e / \hat{\tau}$. At $\hat{d}_e = 0$ no $\hat{g}_e$ triggers it.
D3. Response time near the transition increasing in $\hat{s}_e$.
D4. At matched $q_e$: $E_e \mid \Gamma_e = \emptyset \;>\; E_e \mid \Gamma_e \ne \emptyset$.
D5. Degraded input lowers evidence for $d_e$. It does not raise $h$.

| Dissociation | Behavior | Prediction |
|---|---|---|
| Ketamine, dreaming | absent | $a_e > 0$ on internal instances, actuators uncoupled |
| Automatism | present | $a_e = 0$ on the driving instances |
| Masked stop signal | braking | brake at $a_e = 0$. The brake marks conflict, not presence |
| Flow | high | $\eta$ high |

Refutation: presence varies at fixed $(d_e, \rho_e s_e, \bar{d}_e)$ with $B > 0$. Or P3, D2 or D4 fail under valid estimators.

## 5. Correspondence

| Construct | Papers 1, 2 | Paper 3 | Paper 4 |
|---|---|---|---|
| consequence | $K(x)$ | $s_e = g_e^{-1}$ | $\hat{s}_e$ |
| use | route through $x$ | $\rho_e = \lvert j_e \rvert$ | $\hat{\rho}_e$ |
| divergence | map off at $x$ | $d_e$, $\mathcal{L}_{\mathrm{lift}} = 0$ | $\hat{d}_e$ |
| critical level | $\kappa_c(x) = \tau / d(x)$ | $\epsilon_c(e) = d_e / \tau$ | $\hat{\tau}$, D2 |
| alternatives | map holds another route | $\Gamma_e$ | D4 |
| allocation | $a_e$ | $a_e$ | $E_e$ under M1 |
| control | $u$, $\mathcal{W}$ | $u_t$ on $K_M$ [open] | $\mathcal{W}_e$ under M2 |
| Opacity | $o$ | $1 - \operatorname{corr}(j, j^\ast)$ [assumed] | [open] |
| Contingency | $c$ | on $A_S$ [open] | [open] |
| Transience | $\vartheta$ | $\dot{D}$ absent update | [open] |

Dependency: §2 $\to$ §1 $\to$ §3 $\to$ §4. Theorems on partition and perspective are outside the series unless a later version requires one.
