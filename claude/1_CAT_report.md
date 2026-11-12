# Consciousness as Translation

Report, draft 0.1, 12 November 2026. Oliver Beige, Viktor Arvidsson. Expands §0.1 and §1 of `0_LSMN_kernel.md`, version 0.9. Symbols are those of the kernel registry. [assumed] marks a proposal not yet ruled. [open] marks a form not yet fixed.

## 1. Model

A cognitive agent that navigates an unsurveyable reality has to maintain two models of that reality, a comprehensive one and a comprehensible one, and has to mediate between them. Keeping the two aligned takes metabolic resources, and because the resources are limited the agent has to allocate them. Consciousness arises out of this mediation and allocation. Four stages are involved.

$$\mathcal{L} \xrightarrow{\ \sigma\ } \mathcal{S} \xrightarrow{\ \pi\ } \mathcal{M} \xrightarrow{\ \gamma\ } \mathcal{N}$$

The Landscape $\mathcal{L}$ is unsurveyable reality itself. It contains the options and gives them no order. The Territory $\mathcal{S}$ is the agent's record of its encounters with $\mathcal{L}$, obtained by sampling $\sigma$. It is internal to the agent. Sampling is parochial: its density $\mu_S$ is concentrated around the habitats of the agent and is thin elsewhere, so the Territory is small compared with the Landscape. It is the comprehensive model: it keeps every distinction the agent has encountered and gives none of them an order. The Map $\mathcal{M}$ is a compression $\pi$ of the Territory. The compression is many-to-one,

$$\pi: V_S \twoheadrightarrow V_M, \qquad \lvert V_M \rvert < \lvert V_S \rvert,$$

and the Map carries the orderings by which the agent chooses its steps. It is the comprehensible model. Navigation $\mathcal{N}$ is carried by a policy trajectory $\gamma = (m_0, m_1, \dots)$, a sequence of local steps on the Map directed at a goal $\zeta$. The agent is the tuple $(\mathcal{S}, \mathcal{M}, \pi, \zeta, B)$. The budget $B$ is defined in Section 2.

Papers 1 and 2 present the two models through one pair of terms. The Territory is combinatorial and the Map is continuous. A combinatorial structure consists of discrete options under interaction. It keeps every distinction, it has no gradient, and its size explodes under enumeration. It is the closest formal expression of unsurveyability, and reality itself is not claimed to be combinatorial. A continuous structure lets proximity stand for similarity. It has gradients, it allows interpolation between samples, and it is cheap to follow. The pair has a specific function. It shows that the two models differ in kind, so that no translation between them is exact. Discrete branch points and conflicting constraints have no continuous image, and the Map is most wrong where the Territory has most of them. Each translation in the chain changes the kind of structure: unsurveyable to combinatorial at $\sigma$, combinatorial to continuous at $\pi$, continuous to sequential at $\gamma$. The pair is a stand-in. Paper 3 refines it and keeps its function.

Two facts from the companion report on unsurveyability are used. Intractability $I$ acts at each of the three translations. It forces sampling to be parochial, it forces $\pi$ to be many-to-one, and it forces navigation into a linear sequence of local steps. Transience $T$ has a degree $\vartheta \ge 0$, the rate at which the search space changes.

Because $\pi$ loses distinctions and the search space changes, Map and Territory diverge. The agent compares them at instances. An instance $e$ is a place where the Map makes a commitment that the Territory can confirm or contradict. Paper 3 identifies instances with edges of the Map. This report needs only that instances are countable and that $\gamma$ uses some of them.

Four quantities are attached to an instance.

$$d_e \ge 0, \qquad \bar{d}_e = \mathbb{E}[d_e] \ge 0, \qquad s_e \ge 0, \qquad \rho_e \ge 0$$

$d_e$ is the divergence found at $e$ when the agent checks it. $\bar{d}_e$ is the divergence the agent expects at $e$ before it checks. $s_e$ is the consequence, the change in $\gamma$ per unit of divergence at $e$. $\rho_e$ is the use of $e$ by $\gamma$. The warrant at $e$ is

$$q_e = d_e s_e. \tag{1}$$

It is the size of a found divergence weighted by what the divergence does to the route.

One assumption links these quantities to Transience. [assumed]

$$\vartheta > 0 \ \Rightarrow\ \bar{d}_e > 0 \ \text{ for every } e \text{ not checked at the current } t. \tag{A1}$$

In a changing world, an unchecked commitment of the Map is expected to be off by some amount.

A second assumption links them to sampling. [assumed] Write $\mu_S(e)$ for the sampling density at the Territory vertices that $\pi$ sends to $e$.

$$\bar{d}_e \ \text{ is decreasing in } \ \mu_S(e). \tag{A2}$$

Where sampling is dense the Map interpolates between observations. Where it is sparse the Map extrapolates.

## 2. Allocation

Synchronization of Map and Territory costs metabolic resources. The agent has a budget $B \ge 0$ for it. The demand at an instance is

$$a^\circ_e = f(\rho_e s_e \bar{d}_e) + h_{\operatorname{reg}(e)}(q_e). \tag{2}$$

The first term is monitoring. It is paid before any divergence is found, and it grows with use, with consequence and with expected divergence. The second term is recalibration. It is paid after a divergence is found. It depends on the warrant and on the regime $\operatorname{reg}(e) \in \{\text{drift}, \text{control}, \text{remap}\}$, which Section 4 defines.

The functions satisfy

$$f(0) = h_{\cdot}(0) = 0, \qquad f(x) > 0,\ h_{\cdot}(x) > 0 \ \text{ for } x > 0, \qquad f, h_{\cdot} \text{ nondecreasing}, \qquad f \text{ continuous at } 0, \tag{3}$$

$$h_{\text{drift}}(x) < h_{\text{control}}(x) < h_{\text{remap}}(x) \ \text{ for } x > 0. \tag{4}$$

Their forms are [open]. Conditions (3) and (4) are all that the results below use.

Total demand can exceed the budget. A rationing rule decides what each instance receives. [assumed] Instances are served in descending order of demand until $B$ is spent. Let $e_{(1)}, e_{(2)}, \dots$ be the instances in that order. Then

$$a_{e_{(n)}} = \min\Big(a^\circ_{e_{(n)}},\ B - \sum_{n' < n} a_{e_{(n')}}\Big). \tag{5}$$

It follows that

$$0 \le a_e \le a^\circ_e, \qquad \sum_e a_e = \min\Big(B,\ \sum_e a^\circ_e\Big). \tag{6}$$

Equation (2) states how much synchronization an instance warrants. Equation (5) states how much it receives. The two differ only when the budget binds.

A remembered door on the route has high $\rho_e s_e$. Its state is monitored closely even while it is found as expected. The handle of that door has $\rho_e s_e$ near zero and draws almost no monitoring.

Rule (5) is the simplest that serves larger demands first. Of the results in Section 5, only the second case of Result 1.3 depends on it.

## 3. Consciousness

$$\text{conscious}(e) \iff a_e > 0, \qquad \text{conscious}(\text{agent}) \iff \sum_e a_e > 0, \qquad \text{intensity}(e) = a_e. \tag{7}$$

Statement (7) is a criterion for where consciousness arises and to what degree. It applies at the instance. The agent-level predicate is derived from the instance-level one. No separate global quantity is introduced. By (6),

$$\text{conscious}(\text{agent}) \iff B > 0 \ \text{ and } \ a^\circ_e > 0 \text{ for some } e. \tag{8}$$

The definition ties consciousness to the allocation of resources for synchronization. It does not tie it to processing. An instance can be processed, and can influence behavior, while it receives no allocation.

## 4. Regimes

Let $\Gamma_e$ be the set of alternatives to $e$ that the Territory supports,

$$\Gamma_e = \{\gamma' : e \notin \gamma',\ \gamma' \text{ reaches } \zeta,\ \gamma' \text{ is supported by } \mathcal{S}\}, \tag{9}$$

and let $\tau > 0$ be the tolerance, the largest warrant the agent can absorb without leaving its route. The regime at $e$ is

$$\operatorname{reg}(e) = \begin{cases} \text{drift} & q_e \le \tau \\ \text{control} & q_e > \tau \ \text{ and } \ \Gamma_e \ne \emptyset \\ \text{remap} & q_e > \tau \ \text{ and } \ \Gamma_e = \emptyset. \end{cases} \tag{10}$$

The regimes differ in what the repair acts on.

In drift the repair acts on $\gamma$. The trajectory is adjusted in flight. For $q_e > 0$ the cost $h_{\text{drift}}(q_e)$ is positive and small.

In control the repair acts on the choice of route. The current route fails at $e$ and the Map holds at least one supported alternative. The agent pauses the step, tries members of $\Gamma_e$ virtually and selects one. A control term $w \ne 0$ acts on the trajectory, with control work

$$\mathcal{W} = \int \lVert w \rVert^2 \, dt \ \ge\ 0. \tag{11}$$

In remap the repair acts on $(\mathcal{M}, \pi)$. The Map holds no supported alternative and must itself change.

Two tests separate the regimes. The first compares $q_e$ with $\tau$. The second asks whether $\Gamma_e$ is empty. The second test concerns the content of the Map. The size of the warrant plays no part in it.

A door found closed is a case of control when the Map holds a detour. A door handle found changed is a case of remap when its warrant exceeds $\tau$, because the Map holds nothing for it.

The regime is a property of the instance. One agent can be in different regimes at different instances at the same $t$.

## 5. Results

**Result 1.1, rational limit.** Suppose $I$ does not hold and the agent surveys $\mathcal{L}$ at every $t$. Then $\pi$ can be taken injective and distance-preserving, and

$$d_e = \bar{d}_e = 0 \ \ \forall e \quad \Rightarrow \quad a^\circ_e = f(0) + h_{\cdot}(0) = 0 \ \ \forall e \quad \Rightarrow \quad a_e = 0 \ \ \forall e.$$

By (7) the agent is not conscious. A perfectly rational agent has nothing to synchronize. For $\vartheta > 0$ the premise requires a full survey at every $t$. The result describes a limiting case.

**Result 1.2, waking.** Let $\vartheta > 0$ and $B > 0$, and let some unchecked $e$ have $\rho_e s_e > 0$. By (A1), $\bar{d}_e > 0$. By (3),

$$a^\circ_e \ \ge\ f(\rho_e s_e \bar{d}_e) \ >\ 0,$$

and by (8) the agent is conscious. This holds when $q_e = 0$ for all $e$. An agent on a route in a changing world is conscious without any found divergence. Rest is such a state.

**Result 1.3, unconscious instances.** $a_e = 0$ in two cases.

$$\text{(a)} \quad \rho_e s_e \bar{d}_e = 0 \ \text{ and } \ d_e = 0 \ \Rightarrow\ a^\circ_e = 0. \qquad \text{(b)} \quad a^\circ_e > 0 \ \text{ and } \ \sum_{n' < n} a_{e_{(n')}} = B \ \text{ for } e = e_{(n)}.$$

Neither case excludes processing at $e$. Case (a) covers content off the route and routines whose outcome does not bear on $\gamma$. Case (b) covers content that warrants allocation and loses to larger demands. Which empirical phenomena fall under each case is a question for Paper 4.

**Result 1.4, global loss.** If $B = 0$, then by (5) $a_e = 0$ for all $e$, whatever the values of $d_e$ and $s_e$. Anesthesia and dreamless sleep are read as states with $B = 0$. That reading is a hypothesis.

**Result 1.5, consequence and cost separate.** Take two instances with equal warrant above tolerance and unequal consequence,

$$q_e = q_{e'} = x > \tau, \qquad s_e > s_{e'}, \qquad \Gamma_e \ne \emptyset, \qquad \Gamma_{e'} = \emptyset.$$

By (1), $d_e < d_{e'}$. By (10) and (4),

$$h_{\operatorname{reg}(e)}(q_e) = h_{\text{control}}(x) \ <\ h_{\text{remap}}(x) = h_{\operatorname{reg}(e')}(q_{e'}).$$

The instance of higher consequence is the cheaper one to repair. With equal use and equal expected divergence, it is also the one monitored more, since $f$ is nondecreasing. The closed door and the changed handle are such a pair. Consequence sets how closely an instance is watched. The regime sets what a divergence there costs.

**Result 1.6, fading.** Let $d_e = 0$ and let $\bar{d}_e \to 0$ with $\rho_e s_e$ fixed. By (2), (3) and (6),

$$0 \ \le\ a_e \ \le\ a^\circ_e = f(\rho_e s_e \bar{d}_e) \ \to\ 0.$$

Content that is stable and repeatedly confirmed leaves consciousness. A found divergence at the same instance restores allocation through $h$.

**Result 1.9, habitat and frontier.** [assumed] Fix $\rho_e s_e$. By (A2) and (3), monitoring demand $f(\rho_e s_e \bar{d}_e)$ is nonincreasing in $\mu_S(e)$. Assume further that the probability of $\Gamma_e = \emptyset$ is decreasing in $\mu_S(e)$, since a sparse Territory supports fewer alternatives. Then instances inside a habitat draw little monitoring and are mostly repaired by control. Instances at the frontier draw much monitoring and are more often repaired by remap. Familiar surroundings fade by Result 1.6, and unfamiliar ones hold allocation.

## 6. Identification

$$\text{effort}(e) \equiv h_{\operatorname{reg}(e)}(q_e), \qquad \text{salience}(e) \equiv f(\rho_e s_e \bar{d}_e). \tag{12}$$

The theory identifies felt effort with the cost of recalibration and salience with the monitoring an instance draws. Statement (12) is a postulate. Sections 1 to 5 do not derive it and cannot.

The postulate has content. By (4), effort at equal warrant is ordered drift, control, remap. By Result 1.5, an instance can be low in salience before a divergence and high in effort after it. By Result 1.6, salience falls for confirmed content while use and consequence stay fixed. Each of these can be tested, and Paper 4 states the tests.

## 7. Stand-in

Papers 1 and 2 develop the continuous side of the pair into one smooth picture, which stands in place of the operators of Paper 3. Curvature in the picture is large where the continuous Map misrepresents the combinatorial Territory. Let $\mathcal{M}$ be smooth with points $y$, a potential $\phi$ and a control $w$,

$$\dot{y} = -\nabla \phi(y) + w(y). \tag{13}$$

Let the curvature $\kappa(y)$ stand for the consequence $s_e$ and let $d(y)$ stand for $d_e$. The warrant is $q(y) = d(y)\, \kappa(y)$, and the drift condition of (10) becomes

$$q(y) \le \tau \iff \kappa(y) \le \kappa^\ast(y), \qquad \kappa^\ast(y) = \frac{\tau}{d(y)}. \tag{14}$$

The critical level $\kappa^\ast$ is not a constant. It falls as the divergence grows. As $d(y) \to 0$ it grows without bound, and no curvature ends drift where the Map is not off.

In drift, $w = 0$ and $y$ follows the gradient. In control, $\kappa(y) > \kappa^\ast(y)$, $\Gamma \ne \emptyset$ and $w \ne 0$, with work given by (11). In remap, $\kappa(y) > \kappa^\ast(y)$ and $\Gamma = \emptyset$, and the picture itself changes.

The picture is an illustration. Curvature is not computed from data anywhere in the series. Paper 3 replaces $\kappa$ by the inverse of an effective conductance and $\kappa^\ast$ by $\epsilon^\ast(e) = d_e / \tau$. The second test has no expression in curvature. Where an earlier version of this work wrote "far above the critical level", the present account writes $\Gamma = \emptyset$.

## 8. Open

The forms of $f$ and $h$. The rationing rule (5). The form of $\bar{d}_e$ as a function of $\vartheta$ and of the time since $e$ was last checked, of which (A1) and (A2) fix only signs. The relation of $B$ to the navigation budget of the companion report. The value of $\tau$, which Paper 4 estimates.
