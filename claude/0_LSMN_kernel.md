# LSMN Kernel

Version 0.3, 12 November 2026. Series kernel: shared model, symbols, and the claim of each paper. Paper kernels: `1_CAT`, `2_UNS`, `3_TG`, `4_MC`.

**Chain.** $\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}$.
$\mathcal{L}$ Landscape: all options, no ordering. $\mathcal{S}$ Territory: the agent's record of encounters. $\mathcal{M}$ Map: compression of $\mathcal{S}$, $\pi$ non-injective. $\mathcal{N}$ Navigation: local steps along a trajectory $\gamma$ under a global goal $b$.

**Symbols.** Defined here once. Used in all kernels.

| Symbol | Meaning | Symbol | Meaning |
|---|---|---|---|
| $U$ | Unsurveyability | $e$ | instance (a place where $\mathcal{M}$ meets $\mathcal{S}$) |
| $I$ | Intractability | $d_e \ge 0$ | divergence of $\mathcal{M}$ from $\mathcal{S}$ at $e$ |
| $N$ | Intransigence | $s_e \ge 0$ | consequence of unit divergence at $e$ for $\gamma$ |
| $O$ | Opacity, degree $o \in [0,1]$ | $\rho_e \ge 0$ | use of $e$ by $\gamma$ |
| $C$ | Contingency, degree $c \in [0,1]$ | $q_e = d_e s_e$ | warrant |
| $T$ | Transience, degree $\vartheta \ge 0$ | $a_e \ge 0$ | allocation of metabolic resources to $e$ |
| $B$ | budget, $\sum_e a_e \le B$ | $\tau > 0$ | tolerance |
| $u$ | control | $\mathcal{W} = \int \lVert u_t \rVert^2 dt$ | control work |
| $\kappa_c$ | critical level, conceptual stand-in | $\epsilon_c$ | critical level, measurable |

**Claims by paper.**

`2_UNS`. $U = I + N$, $N = (O, C, T)$. $I$ forces local search. Each of $O$, $C$, $T$ forces the agent to manufacture one ordering. The product is a dynamic heuristic under $B$.

`1_CAT`. The agent synchronizes $\mathcal{M}$ with $\mathcal{S}$. Allocation $a_e$ is set by $\rho_e s_e$ before divergence and by $q_e$ after it. Instance $e$ is conscious iff $a_e > 0$. Three regimes differ in the locus of repair. $I = 0 \Rightarrow a \equiv 0$.

`3_TG`. $d_e$, $s_e$, $\rho_e$ and the regime tests are operators on complexes $K_S$, $K_M$. Drift ends at $\epsilon_c(e) = d_e / \tau$. Control and Remap are separated by a lift test.

`4_MC`. $a_e$ and $\mathcal{W}$ leave external traces. Tests address presence ($a_e > 0$) and degree ($a_e$) per instance.

**Dependency.** `2_UNS` $\to$ `1_CAT` $\to$ `3_TG` $\to$ `4_MC`.

**Status.** `1_CAT` and `2_UNS` are conceptual. They use $\kappa_c$ and a smooth picture as stand-ins. `3_TG` and `4_MC` are scientific. They use $\epsilon_c$ and discrete operators. Theorems on partition and perspective are outside the series unless a later kernel requires one.

**Marks.** [assumed]: proposed and not yet ruled. [open]: form not yet fixed.
