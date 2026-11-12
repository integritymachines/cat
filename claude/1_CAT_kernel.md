# CAT Kernel

Version 0.1, 12 November 2026. Paper 1, Consciousness as Translation. Symbols as in `0_LSMN_kernel.md`.

**Agent.** $A = (\mathcal{S}, \mathcal{M}, \pi, b, B)$, $\pi: \mathcal{S} \to \mathcal{M}$ non-injective, on a trajectory $\gamma \subset \mathcal{M}$ toward $b$.

**Synchronization.** At each instance $e$ the agent compares $\mathcal{M}$ with $\mathcal{S}$.
$d_e \ge 0$: divergence found. $s_e \ge 0$: change in $\gamma$ per unit divergence at $e$. $\rho_e \ge 0$: use of $e$ by $\gamma$.
Warrant: $q_e = d_e s_e$.

**Allocation.** $a_e = a^{\text{mon}}_e + a^{\text{rec}}_e$, $a_e \ge 0$, $\sum_e a_e \le B$.
$a^{\text{mon}}_e = f(\rho_e s_e)$, $f$ nondecreasing, $f(0) = 0$. Paid before divergence.
$a^{\text{rec}}_e = h(q_e, \text{regime})$, $h$ nondecreasing in $q_e$, $h(0, \cdot) = 0$. Paid after divergence.
Forms of $f$, $h$ [open].

**Definition.** $e$ is conscious iff $a_e > 0$. $A$ is conscious iff $\exists e: a_e > 0$. Intensity at $e$ is $a_e$.

**Regimes** at $e$. Let $\Gamma_e = \{\gamma' \subset \mathcal{M} : \gamma' \text{ reaches } b,\ \gamma' \text{ avoids the divergence at } e,\ \gamma' \text{ is supported by } \mathcal{S}\}$.

| Regime | Condition | Repair acts on | Cost |
|---|---|---|---|
| Drift | $q_e \le \tau$ | $\gamma$, in flight | $h_D$ |
| Control | $q_e > \tau$, $\Gamma_e \ne \emptyset$ | choice in $\Gamma_e$, $u \ne 0$, step paused | $h_C$ |
| Remap | $q_e > \tau$, $\Gamma_e = \emptyset$ | $\mathcal{M}$, $\pi$ | $h_R$ |

$h_D < h_C < h_R$ at equal $q_e$.

**Results.** Each follows from the definition and the stated condition.

R1. Rational limit. $I = 0 \Rightarrow \pi$ loses nothing $\Rightarrow d_e \equiv 0$ and no monitoring is needed $\Rightarrow a \equiv 0$. A perfectly rational agent is not conscious.
R2. Waking. $\vartheta > 0$ and $\exists e: \rho_e s_e > 0 \Rightarrow \exists e: a_e > 0$. An agent on a trajectory in a changing world is conscious without conflict.
R3. Unconscious processing. $a_e = 0$ is compatible with processing at $e$. Cases: $\rho_e s_e = 0$, or $e$ falls below the cutoff imposed by $B$.
R4. Global loss. If allocation is disabled, $a \equiv 0$ for all $d$, $s$.
R5. Consequence and cost separate. $s_e$ sets $a^{\text{mon}}_e$. The regime sets $a^{\text{rec}}_e$. Low $s_e$ with $\Gamma_e = \emptyset$ costs more than high $s_e$ with $\Gamma_e \ne \emptyset$.
R6. Fading. $d_e \to 0$ and $\rho_e s_e \to 0 \Rightarrow a_e \to 0$.

**Postulate.** Felt effort at $e$ is $a^{\text{rec}}_e$. Salience at $e$ is $\rho_e s_e$. This is an identification. It is not derived.

**Stand-in.** Smooth $(\mathcal{M}, g)$, $\dot{x} = -g^{-1} \nabla V(x) + u(x)$. Curvature $K(x)$ stands for $s_e$. $\kappa_c(x) = \tau / d(x)$. Drift: $K < \kappa_c$. Control: $K \ge \kappa_c$, $\Gamma \ne \emptyset$. Remap: $K \ge \kappa_c$, $\Gamma = \emptyset$. $\mathcal{W} = \int \lVert u \rVert^2_g \, dt$.
