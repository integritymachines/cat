# UNS Kernel

Version 0.1, 12 November 2026. Paper 2, Unsurveyability. Symbols as in `0_LSMN_kernel.md`.

**Search space.** $X$: arrangements of $n$ options under interaction. $\lvert X \rvert \ge n!$. Objective $f: X \to \mathbb{R}$, loosely defined. Survey: evaluation of $f$ on all of $X$.

**Unsurveyability.** $U = I + N$, $N = (O, C, T)$.

**Intractability $I$.** $\nu(\mathcal{S}_\alpha)$: number of relevant distinctions at scale $\alpha$. $I$ holds iff $\lim_{\alpha \to \infty} \log \nu(\mathcal{S}_\alpha) / \dim \mathcal{M} = \infty$.
$I \Rightarrow$ no survey $\Rightarrow$ local search: $x_{t+1} \in \mathrm{Nbr}(x_t)$ on local information, under goal $b$.

**Intransigence $N$.** Three obstructions to local search. Each has a degree.

| | Obstruction | Degree | Agent manufactures | Ordering assigned | Primitive |
|---|---|---|---|---|---|
| $O$ | no gradient, or local gradient unrelated to global | $o = 1 - \operatorname{corr}(\nabla_{\text{loc}} f, \nabla_{\text{glob}} f) \in [0,1]$ [assumed] | gradient $j$ | comes with: none | relations |
| $C$ | steps foreclose options | $c \in [0,1]$, cost of reversion | virtual trajectories $\gamma$, before the step | follows from: logical, negotiable | functions |
| $T$ | $X_t$ changes | $\vartheta \ge 0$, rate of change | updates of $\gamma$ on observed divergence | follows after: temporal, non-negotiable | dynamics |

The agent assigns the orderings. The primitives describe them.

**Reversion.** $\Omega_t$: options reachable at $t$. $B_t$: budget spent by $t$. $\iota_t$: information held on $X$.
$c = 0$: backtracking is free. $c = 1$: backtracking is impossible. $0 < c < 1$: backtracking from $t$ to $t' < t$ restores $\Omega_{t'}$ and does not restore $B_t - B_{t'}$.
$\vartheta = 0$: $\iota$ is kept. $\vartheta > 0$: $\iota$ decays at a rate increasing in $\vartheta$.

**Coupling** [assumed]. The obstructions are not independent.
Loss from $C$ is increasing in $o \cdot c$. At $o = 0$ foreclosure costs nothing.
Loss from $T$ is increasing in $\vartheta$ and in the committed length of $\gamma$.

**Conjecture cycle.** $j \to \gamma$ (virtual test, failures discarded at cost of computation) $\to$ step $\to$ update. One pass answers $O$, $C$, $T$ in that order.

**Dynamic heuristic.** $B = B_O + B_C + B_T + B_{\text{step}}$: gradient, virtual test, update, movement.
The heuristic is the policy $\gamma^\ast_t$ that the cycle returns under $B$, revised at each $t$. It satisfices: search stops when expected gain of one more pass falls below its cost.
$I = 0 \Rightarrow B_O = B_C = B_T = 0$ and $\gamma^\ast$ is optimal.

**Cube.** Extreme types: $(\mathbb{1}[o > 0], \mathbb{1}[c > 0], \mathbb{1}[\vartheta > 0]) \in \{0,1\}^3$. Environments lie in $[0,1]^2 \times \mathbb{R}_{\ge 0}$. The cube is a picture. It carries no result.

**Completeness.** That $O$, $C$, $T$ exhaust $N$ is conjectured.
