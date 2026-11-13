# LSMN Notation

Version 0.1, 14 November 2026. Symbols, tags and claim types for Papers 1 to 4 and the kernel. One meaning per symbol. Regimes, results and tests carry words or section numbers, never single letters.

## Tags

Provenance. [ruled]: decided by the authors. [inference]: proposed in drafting, not ruled. [open]: form not fixed. Numbers taken from the research notes are unchecked.

Claim types. (def) definition. (thm) theorem, with its assumptions. (post) modeling postulate: an element of the model, subject to empirical test. (hyp) empirical hypothesis, to be confirmed. (ill) illustration: a synecdoche or picture that explains a concept and makes no general claim.

## Symbols

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
| $f_{v,e}$ | outward flux at vertex $v$ along incident edge $e$ |
| $u, v, h$ | Hodge components of an edge chain: gradient, rotational, harmonic |
| $\operatorname{lift}$ | lift functional |
| $\Gamma_{\mathcal{L}}, \Gamma_{\mathcal{S}}, \Gamma_B$ | routes from $z_0$ to $\zeta$, the current one included: supported by $\mathcal{L}$, supported by $\mathcal{S}$, acceptable and found within budget |
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
| $w, \mathcal{W}, \Theta$ | control field, controller expenditure over an interval, matched interval |
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
| $\delta_{\mathrm{lo}}, \delta_{\mathrm{hi}}, \delta^\ast$ | band of offline deformation (separate paper), critical discrepancy between agents |
| $\operatorname{bnd}, \operatorname{PR}$ | decision boundary, participation ratio |
| $\hat{\ }$, $t$ | estimator, time |

## Against the sources

$\pi$ for the 2025 $\phi$, $\phi$ for $V$, $w$ for $U$, $\mathcal{W}$ for $\mathcal{C}_U$, $\kappa$ for $K$, $y$ for $x$, $G$ for $W$, $\partial_1$ for $B_1$, $\zeta$ for $b$, $\Lambda_S$ for $A_S$, $B_w$ for $B_C$, $\epsilon^\ast$ for $\epsilon_c$, $\kappa^\ast$ for $\kappa_c$, $\delta^\ast$ for $\delta_c$. The changes remove collisions.
