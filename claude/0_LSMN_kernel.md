# LSMN Kernel

Version 0.2, 12 November 2026. Series kernel for Papers 1 to 4. Items marked [assumed] or [open] are not yet ruled.

**Chain.** $L \xrightarrow{\sigma} S \xrightarrow{\pi} M \xrightarrow{\gamma} N$.
$L$: Landscape. $S$: Territory, the agent's record of encounters, complex $K_S$ with relation $A_S$, metric $d_S$, measure $\mu_S$. $M$: Map, complex $K_M$ with vertices $V_M$, edges $E_M$, weights $W$, metric $d_M$. $N$: Navigation. $\pi: K_S \twoheadrightarrow K_M$ is non-injective. $\gamma = (m_0, \dots, m_H)$ is a trajectory in $K_M$ toward goal $b$, $\mathbf{1}^\top b = 0$.

**Unsurveyability.** Unsurveyability = Intractability + Intransigence. Intransigence = (Opacity, Contingency, Transience).
Intractability: $\lim_{\alpha \to \infty} \log \mathcal{N}(S_\alpha) / \dim K_M = \infty$. Consequence: search is local.

| Obstruction | Degree | Agent manufactures | Ordering | Description |
|---|---|---|---|---|
| Opacity | $o = 1 - \operatorname{corr}(j, j^\ast) \in [0,1]$ [assumed] | gradient $j$ | comes with | relations |
| Contingency | reversion cost $r \in [0,1]$ | virtual trajectories $\gamma$ | follows from | functions |
| Transience | drift rate $\delta \ge 0$ of $S_t$ | updates on divergence | follows after | dynamics |

Backtracking at $r < 1$ recovers options. It does not recover expended resources. At $\delta > 0$ it also loses information on $S$.
Coupling [assumed]: Contingency binds in proportion to $o$. Transience binds given a committed $\gamma$.

**Gradient.** $\Delta_0 = B_1 W B_1^\top$. $\Delta_0 \phi = b$. $j = -W B_1^\top \phi$.

**Instance.** Edge $e = (u,v) \in E_M$, fiber $F_e = \pi^{-1}(u) \cup \pi^{-1}(v)$.
Divergence: $d_e = \sum_{s,s' \in F_e} \mu_S(s)\mu_S(s') \, \lvert d_S(s,s') - d_M(\pi s, \pi s') \rvert^2 \ge 0$.
Conductance: $g_e = \big[(\chi_u - \chi_v)^\top \Delta_0^\dagger (\chi_u - \chi_v)\big]^{-1}$. Global summary: $\lambda_2(\Delta_0)$.
Warrant: $q_e = d_e / g_e$.
Lift: $\mathcal{L}(\gamma \mid s_0) = e_{s_0}^\top P_{m_0} A_S P_{m_1} \cdots A_S P_{m_H} \mathbf{1}$. If $\mathcal{L}(\gamma \mid s_0) = 0$, set $d_e = \infty$ at the failing edge.

**Regimes** at $e$ on $\gamma$, tolerance $\tau > 0$, $\epsilon_c(e) := d_e / \tau$.

| Regime | Condition | Repair acts on |
|---|---|---|
| Drift | $g_e > \epsilon_c(e)$ | the trajectory |
| Control | $g_e \le \epsilon_c(e)$ and $\exists \gamma'$ to goal with $\mathcal{L}(\gamma' \mid s_0) > 0$ | the choice of route, $u_t \ne 0$ |
| Remap | $g_e \le \epsilon_c(e)$ and no such $\gamma'$ | $K_M$ and $\pi$ |

**Allocation.** $a_e = a_e^{\text{mon}} + a_e^{\text{rec}} \ge 0$, $\sum_e a_e \le B$.
$a_e^{\text{mon}}$ is nondecreasing in $\lvert j_e \rvert / g_e$. $a_e^{\text{rec}}$ is nondecreasing in $q_e$ and ordered Drift $<$ Control $<$ Remap. Functional forms [open].
Instance $e$ is conscious iff $a_e > 0$. The agent is conscious iff $\sum_e a_e > 0$. Intensity at $e$ is $a_e$.
Control work: $\mathcal{W} = \int_0^T \lVert u_t \rVert^2 \, dt \ge 0$.
Map change, signed observable: $\frac{d}{dt} \log T_{\mathrm{RS}} = \frac{1}{2} \sum_q (-1)^{q+1} q \operatorname{Tr}(\Delta_q^\dagger \dot{\Delta}_q)$ at constant rank.

**Limit.** Zero Intractability $\Rightarrow \pi$ isometric $\Rightarrow d_e \equiv 0$ and $o = 0 \Rightarrow a \equiv 0$. A perfectly rational agent is not conscious.

**Stand-in for Papers 1 and 2.** $K(x) \approx \kappa_c$ stands for $g_e \approx \epsilon_c(e)$. $K(x) \gg \kappa_c$ stands for the absence of a lifting $\gamma'$.

**Notation changes from the notes.** Stage maps are $\sigma, \pi, \gamma$. Control is $u$ and control work is $\mathcal{W}$. The compression map is $\pi$ everywhere and $\phi$ is the potential. The obstructions are written out by name and carry no single-letter symbols.
