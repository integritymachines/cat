# TG Kernel

Version 0.1, 12 November 2026. Paper 3, Translation Geometry. Symbols as in `0_LSMN_kernel.md`. Replaces the stand-ins of `1_CAT` with operators.

**Complexes.** $\mathcal{S}$: $K_S$ with vertices $V_S$, relation $A_S$, metric $d_S$, measure $\mu_S$. $\mathcal{M}$: $K_M$ with vertices $V_M$, oriented edges $E_M$, weights $W$, incidence $B_1$, metric $d_M$. $\pi: V_S \twoheadrightarrow V_M$. $P_m$: projector onto $\pi^{-1}(m)$.

**Gradient** (answer to $O$). $\Delta_0 = B_1 W B_1^\top$. Goal $b$, $\mathbf{1}^\top b = 0$. $\Delta_0 \phi = b$, $j = -W B_1^\top \phi$.
$o = 1 - \operatorname{corr}(j, j^\ast)$, $j^\ast$ the flow under the potential of $\mathcal{L}$ [assumed].

**Instance.** $e = (v, w) \in E_M$, fiber $F_e = \pi^{-1}(v) \cup \pi^{-1}(w)$.
$\rho_e = \lvert j_e \rvert$.
$g_e = \big[(\chi_v - \chi_w)^\top \Delta_0^\dagger (\chi_v - \chi_w)\big]^{-1}$, effective conductance. $s_e = 1 / g_e$. Global summary: $\lambda_2(\Delta_0)$.
$d_e = \sum_{x, y \in F_e} \mu_S(x) \mu_S(y) \, \lvert d_S(x, y) - d_M(\pi x, \pi y) \rvert^2$.
$q_e = d_e / g_e$.

**Lift** (answer to $C$). For $\gamma = (m_0, \dots, m_H)$ and $x_0 \in \pi^{-1}(m_0)$:
$\mathcal{L}_{\text{lift}}(\gamma \mid x_0) = \chi_{x_0}^\top P_{m_0} A_S P_{m_1} \cdots A_S P_{m_H} \mathbf{1}$.
$\gamma$ is supported by $\mathcal{S}$ iff $\mathcal{L}_{\text{lift}} > 0$. If $\mathcal{L}_{\text{lift}}(\gamma \mid x_0) = 0$, set $d_e = \infty$ at the first failing edge.
$\Gamma_e = \{\gamma' : \gamma' \text{ reaches } b,\ e \notin \gamma',\ \mathcal{L}_{\text{lift}}(\gamma' \mid x_0) > 0\}$.

**Regimes.** $\epsilon_c(e) = d_e / \tau$.

| Regime | Test |
|---|---|
| Drift | $g_e > \epsilon_c(e)$ |
| Control | $g_e \le \epsilon_c(e)$, $\Gamma_e \ne \emptyset$ |
| Remap | $g_e \le \epsilon_c(e)$, $\Gamma_e = \emptyset$ |

$d_e = 0 \Rightarrow \epsilon_c(e) = 0 \Rightarrow$ Drift at any $g_e$.

**Update** (answer to $T$). $\mathcal{S}_t$ changes at rate $\vartheta$. Absent update, $D(t) = \sum_{x,y \in V_S} \mu_S(x)\mu_S(y) \lvert d_{S_t}(x,y) - d_M(\pi x, \pi y) \rvert^2$ grows. Remap acts on $W$, $K_M$, $\pi$ to reduce $D$.
Signed observable of Remap at constant rank: $\frac{d}{dt} \log T_{\mathrm{RS}} = \frac{1}{2} \sum_q (-1)^{q+1} q \operatorname{Tr}(\Delta_q^\dagger \dot{\Delta}_q)$.
Control work: $\mathcal{W} = \int \lVert u_t \rVert^2 dt \ge 0$. $\log T_{\mathrm{RS}}$ is not $\mathcal{W}$.

**Worked case.** $V_S = \{x_1, x_2, x_3, x_4\}$, path. $\pi: x_1, x_4 \mapsto m_1$, $x_2 \mapsto m_2$, $x_3 \mapsto m_3$. $K_M$: triangle, $W = I$. Goal: $m_1 \to m_3$ from $x_1$.
$\phi = (\tfrac13, 0, -\tfrac13)$, $j = (\tfrac13, \tfrac13, -\tfrac23)$. The flow prefers $(m_1, m_3)$.
$\mathcal{L}_{\text{lift}}((m_1, m_3) \mid x_1) = 0$. $\mathcal{L}_{\text{lift}}((m_1, m_2, m_3) \mid x_1) = 1$. $\Gamma \ne \emptyset$: Control.
$D = \tfrac{22}{16}$. On $\{x_1, x_2, x_3\}$: $\tfrac29$, and $0$ after $w_{31} \to 0$.
$\det{}' \Delta_1 = 3(1 + 2w)$. $\Delta \log T_{\mathrm{RS}} = -\tfrac12 \ln 3$ for $w: 1 \to 0$.
The harmonic component of a route does not separate supported from unsupported routes. $\mathcal{L}_{\text{lift}}$ does.

**Open.** Estimation of $\tau$. Form of $u_t$ on $K_M$. Role of $\Delta_1$ beyond the lift test.
