# MC Kernel

Version 0.1, 12 November 2026. Paper 4, Measuring Consciousness. Symbols as in `0_LSMN_kernel.md`. Operators as in `3_TG_kernel.md`. No effect size is stated here. All estimators are [open] until the fact-check pass.

**Observation model.** $a_e$ is not observed. Two traces are.
Input trace: metabolic expenditure $E_e(t) \ge 0$.
Output trace: control work $\mathcal{W}_e$ and its effect on $\gamma$.
Efficiency: $\eta = \mathcal{W} / E \in (0, 1]$.
Assumption M1: $E_e$ is increasing in $a_e$. Assumption M2: $\mathcal{W}_e > 0$ only in Control.

**Estimators** [open]. $\hat{\Delta}_0$ from recorded connectivity. $\hat{g}_e$ from $\hat{\Delta}_0^\dagger$. $\hat{\rho}_e$ from task flow. $\hat{d}_e$ from the mismatch between predicted and encountered input at $e$. $\hat{\tau}$ from the Drift to Control transition.

**Presence.** Tests of $a_e > 0$ against $a_e = 0$ for one instance.
P1. Contrast. Same input at $e$, reported against unreported: $E_e$ differs. The difference is specific to $e$.
P2. Fading. Stable, predicted input with $\rho_e s_e \to 0$: report and $E_e$ decline together.
P3. Relevance. Probability of detecting a change at $e$ is increasing in $\rho_e s_e$ at fixed physical change.
P4. Global loss. Under anesthesia and dreamless sleep, $E_e$ shows no dependence on $d_e$ or $\rho_e s_e$ for any $e$.

**Degree.** Tests of the size of $a_e$.
D1. Monitoring. Before any divergence, $E_e$ is increasing in $\hat{\rho}_e \hat{s}_e$.
D2. Threshold. Control begins at $\hat{g}_e \le \hat{d}_e / \hat{\tau}$. The critical $\hat{g}_e$ rises with $\hat{d}_e$. At $\hat{d}_e = 0$ no $\hat{g}_e$ triggers Control.
D3. Slowing. Response time near the transition is increasing in $\hat{s}_e$.
D4. Regime cost. At matched $q_e$, $E_e$ is larger when $\Gamma_e = \emptyset$ than when $\Gamma_e \ne \emptyset$.
D5. Data limits. Degrading the input lowers the evidence for $d_e$. It does not by itself raise $a^{\text{rec}}_e$.

**Dissociations.** The account must hold in each.

| Case | Behavior | Prediction |
|---|---|---|
| Disconnected experience (ketamine, dreaming) | absent | $a_e > 0$ for internal instances, actuators uncoupled |
| Automatism | present | $a_e = 0$ for the instances that drive it |
| Masked stop signal | braking | brake without $a_e > 0$. The brake marks conflict and not presence |
| Flow | high performance | high $\eta$: $\mathcal{W}$ maintained at reduced $E$ |

**Refutation.** The account fails if presence varies at fixed $(d_e, \rho_e s_e)$ with allocation enabled, or if P3, D2 or D4 fail under valid estimators.

**Out of scope.** Clinical nosology, comparative taxa, sleep remapping and dyads go to the satellite notes.
