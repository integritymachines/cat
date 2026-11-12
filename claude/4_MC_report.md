# Measuring Consciousness

Report, draft 0.2, 13 November 2026. Kernel: `0_LSMN_kernel.md` §4. The research note for Paper 4 is the yardstick, with the summary report on the lower bound for the last section. Tags: [ruled] marks a departure decided by the authors, [inference] marks a proposal of this draft, [open] marks a form not fixed. Numbers quoted from the note are unchecked and are marked as note values.

This report states what the operators of Paper 3 predict in recordings of living systems. It follows the order of the note: thesis, traces, dictionary, waking tests, states, agents, and the handoff on the lower bound. It ends with a refutation condition.

## Thesis

An agent forms its map $\mathcal{M}_{\mathrm{int}}$ from its own sampling and compression. An observer forms $\mathcal{M}_{\mathrm{ext}}$ from another. By Proposition 3.3 of Paper 3 the two stand at a positive distance:

$$d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) > 0 \tag{1}$$

Scientific observation is a second lossy translation of first-person experience. It observes behavior and physiology from without and regularizes them across instances and species. It does not absorb what it is like to be the agent.

Proposition 3.2 gives the complement. When the spectral gap $\lambda_2$ of the map falls to its critical level $\epsilon^\ast$, or the planned route fails the lift test, the agent reaches its goal only with a nonzero control field $w$ or a deformation of the map. Control consumes a metabolic allocation $a$ and produces control work $\mathcal{W}$. Both are physical and both leave traces. The tests below concern those traces. They make no claim to measure experience itself.

## Traces

Allocation has a waking baseline and surges at instances $e$:

$$a(t) = a_{\mathrm{base}}(t) + \sum_e \Delta a_e(t), \qquad \mathcal{W} = \eta\, a, \qquad \eta \in (0, 1] \tag{2}$$

$\eta$ is the efficiency of conversion. Two traces are available.

| Trace | Estimates | Candidate channels (note) |
|---|---|---|
| $\hat{a}$ | metabolic input | regional hemodynamics, pupil diameter, autonomic balance |
| $\hat{\mathcal{W}}$ | control work | reconstructed $\hat{\lambda}_2$, $\hat{\beta}_1$, $\log \widehat{\operatorname{Tor}}$, midfrontal theta, decision boundary, response-time dynamics |

Assumption 4.1. $\hat{a}$ is increasing in $a$.

Assumption 4.2 (note). Control work is bounded below by the deformation it achieves:

$$\mathcal{W} \ge c_0\, \lvert \Delta \log \operatorname{Tor} \rvert, \qquad \text{hence} \qquad a \ge \frac{c_0}{\eta}\, \lvert \Delta \log \operatorname{Tor} \rvert \tag{3}$$

with a constant $c_0 > 0$. The note derives $c_0$ from a thermodynamic argument. That derivation is not reproduced and awaits the fact check. Log torsion remains a signed observable and is not identified with $\mathcal{W}$ [ruled].

Separating $a$ from $\mathcal{W}$ matters where the two decouple. In flow, much work is done at low input and $\eta$ is high. In overload, input is high and the trajectory stalls, so $\eta$ is low.

## Dictionary

Every test is conditional on estimators of the operators.

| Operator (Paper 3) | Role | Candidate estimator (note) |
|---|---|---|
| $K_S$ against $K_M$ | record against compressed map | orthogonal subspaces in population activity |
| $\Delta_0$, $\lambda_2$ | identification | graph Laplacian from phase-based or precision-based connectivity among channels |
| $\Delta_1$, $\beta_1$ | composition | persistent cohomology of population state clouds |
| $\operatorname{Tor}$ | persistence, deformation | log determinants on empirical clique complexes |
| $d_{\mathrm{GW}}$ | remap, distance between agents | transport distance between dissimilarity matrices |

The note names four empirical supports for this dictionary: a factorization of hippocampal activity into orthogonal subspaces for drift in time and for position, a link between the spectrum of $\Delta_0$ and the participation ratio $\operatorname{PR}$ of population activity, a contraction of variability in familiar regimes with aliasing at the boundary of ignorance, and a multiplexing of dominant and suppressed percepts during rivalry. This report lists them as candidates. None has passed the fact check.

The dictionary is the weakest link of the paper. A failed test refutes the series only under valid estimators.

## Waking Tests

The four tests follow the transition from drift to control. They concern the degree of allocation at an instance.

Test 4.3 (spectral). Let ambiguity or conflict be varied in small steps. Control markers do not scale linearly. $\hat{\lambda}_2$ shows a step drop at a critical value, and control markers rise nonlinearly immediately after it. Note values: a drop of more than half, preceding the rise by less than 50 ms.

Test 4.4 (kinematic). The relaxation time grows as $\lambda_2^{-1}$ (Paper 3). Response time follows

$$\mathbb{E}[\text{response time}] = t_0 + c_1\, \lvert \lambda_2 - \epsilon^\ast \rvert^{-1/2} \tag{4}$$

with constants $t_0$, $c_1$. Variability across trials rises in the same window, and errors separate into fast slips under drift and slow errors under control.

Test 4.5 (braking). Resolving a cycle before commitment requires halting execution. Let $\operatorname{bnd}$ be the decision boundary of a sequential-sampling model. Then

$$\Delta \operatorname{bnd}(t) = c_2\, [\lambda_2(t) \le \epsilon^\ast]\, \log \operatorname{Tor}(K_M(t)) \tag{5}$$

with a constant $c_2$ and the bracket equal to one when the condition holds. The behavioral form is vicarious trial and error at a fork: the animal stops, sweeps its head between options, and reverses a prepotent movement.

Test 4.6 (metabolic). By (3), $\hat{a}$ is linear in $\Delta \log \operatorname{Tor}$ across trials, with slope proportional to $\eta^{-1}$.

Individuals differ in baseline $\epsilon^\ast$ and in $\eta$. The note describes the margin just above $\epsilon^\ast$ as confidence, the low-cost correction of minor divergence, and reads individual differences in that margin as a spectrum between sequential and parallel styles of cognition. Above the lower bound, organisms differ in how they allocate, and Tests 4.3 to 4.6 are where that variance can be picked up. Bat navigation is a candidate case: stereotyped flight corridors with sonar locked to the wingbeat under drift, and strobe groups with braking when a target is displaced.

## States

Paper 1 describes altered states by curvature $\kappa$ against its critical level $\kappa^\ast$. The operators give each state a signature.

| State | Papers 1 and 2 | Operators | $\eta$ |
|---|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $\lambda_2 > \epsilon^\ast$, $\beta_1 = 0$, $a = a_{\mathrm{base}}$ | baseline |
| overload | $\kappa \ge \kappa^\ast$, sustained | $\lambda_2 \le \epsilon^\ast$, $\beta_1 > 0$, torsion spike | low |
| flow | $\kappa$ just below $\kappa^\ast$ | $\lambda_2$ just above $\epsilon^\ast$, $\beta_1 = 0$ | maximal |
| meditation | lower $\kappa$, higher $\kappa^\ast$ | higher baseline $\lambda_2$, larger envelope | high |
| psychedelics | higher variance of $\kappa$ | higher $\operatorname{PR}$, large $d_{\mathrm{GW}}$ from baseline, remap afterward | remap |
| propofol | $w \equiv 0$ | long-range $\lambda_2 \to 0$, $\mathcal{W} \to 0$, $a$ suppressed | none |
| ketamine, REM | control without actuators | $\mathcal{W} > 0$ internally, input and output gated | uncoupled |

The table makes three commitments that can fail separately. Flow and overload differ in $\eta$ at comparable work. Propofol and ketamine differ in internal $\mathcal{W}$ at comparable unresponsiveness. Meditation moves the baseline, where psychedelics move the variance.

Test 4.7. Under propofol and in dreamless sleep, $\hat{a}$ and $\hat{\mathcal{W}}$ do not respond to $\hat{\lambda}_2$. Local responses to input can persist. A drop of the gap triggers no control.

## Agents

Two agents $A$ and $B$ hold maps compressed from private territories. They coordinate under drift while

$$d_{\mathrm{GW}}(\mathcal{M}_A, \mathcal{M}_B) < \delta^\ast \tag{6}$$

and they build a shared representation as the distance falls. At or above $\delta^\ast$, automatic coordination breaks down and the agents need explicit translation at the boundary between their maps, with $w \ne 0$ on both sides. The note predicts that compatibility between people follows relational geometry, the structure of distances inside each map, and does not follow similarity of attributes. Note value: $\delta^\ast$ near 0.35 of the map's diameter.

## Lower Bound

Whether a system is conscious at all has a lower bound. The note hands this question to a satellite note. This section states the test that the satellite note applies.

Viability. The conjecturing engine pays only when the expected physical loss it avoids exceeds its cost. With $\ell$ the loss from a failed physical conjecture and $B_F$, $B_w$, $B_0$ the budgets for virtual search, reconciliation and maintenance (Paper 3),

$$\mathbb{E}[\ell \text{ avoided}] > \mathbb{E}[B_F + B_w + B_0] \tag{7}$$

Motility and sessility give the first dividing line [ruled]. An agent that moves meets changing environments, and their number explodes combinatorially. A sessile agent has limited need for the engine. It can produce physical conjectures in place of virtual ones: a tree grows many branches and lets the losers die, which is literal branch and bound. A motile agent has one body on one route. Its conjectures have to die in its stead, so they have to be virtual. The need for a compact map arises downstream, from the exploding complexity of the experienced habitat.

| | Sessile, reflexive | Motile, navigational |
|---|---|---|
| conjectures | physical, parallel | virtual, before commitment |
| map | none required | compressed from the record |
| gap at choice points | $\lambda_2 > \epsilon^\ast$ throughout | $\lambda_2 \le \epsilon^\ast$ occurs |
| cycles, torsion | $\beta_1 = 0$, $\log \operatorname{Tor}$ flat | $\beta_1 > 0$ resolved under control |
| offline | physical recuperation | physical and virtual recuperation |

Boundary test [ruled]. A system is above the bound iff it shows all three:

1. Compression. It holds a map $\mathcal{M} = \pi(\mathcal{S})$ with $\dim \mathcal{M} \ll \log \nu(\mathcal{S})$, separate from the record.
2. Discontinuity. At a critical limit the system shows a discontinuity that can be measured from without. Tests 4.3 to 4.6 give its forms.
3. Offline conjecturing. It has high-intensity REM phases. With actuators gated, the map deforms within a band:

$$\delta_{\mathrm{lo}} \le d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{wake}}, \mathcal{M}_{\mathrm{sleep}}) \le \delta_{\mathrm{hi}} \tag{8}$$

Note values: $\delta_{\mathrm{lo}} = 0.10$, $\delta_{\mathrm{hi}} = 0.45$, with $\operatorname{PR}_{\mathrm{REM}} > \operatorname{PR}_{\mathrm{wake}}$ and a higher $\lambda_2$ after sleep.

Dreaming is the enactment of far-fetched and potentially lethal conjectures under physical incapacitation. Only organisms that dream can be conscious [ruled]. An organism that does not dream recuperates physically in sleep. A conscious organism also has to recuperate virtually and send the singularities of its map to their deaths.

Applied across taxa, the summary report gives the following placement. It is unchecked.

| System | Compression | Discontinuity | Offline conjecturing | Placement |
|---|---|---|---|---|
| plants, microbes | no | no | no | well below |
| insects, spiders | local | minimal | borderline | at or below |
| reptiles | yes | yes | yes | at or just above |
| cephalopods | yes | yes | yes | above |
| mammals, birds | yes | yes | yes | well above |

Current large language models are below the bound [ruled]. They have no adaptive recalibration in runtime, so point 2 has no object, and they have no parochialism. Their sampling has no habitat, which makes them the nearest known case of the perfectly rational agent of Paper 1.

## Refutation

Under valid estimators, the series fails in any of three cases.

1. In Test 4.3, control markers scale linearly through the critical value, with no step in $\hat{\lambda}_2$.
2. Under the conditions of Test 4.7, $\hat{a}$ and $\hat{\mathcal{W}}$ respond to $\hat{\lambda}_2$ as they do in wake.
3. A system passes the boundary test and shows none of the forms of Tests 4.3 to 4.6.

A fourth case concerns the bound. An organism that demonstrably does not dream and passes points 1 and 2 of the boundary test would refute the claim that offline conjecturing is necessary.

No effect size is asserted before the fact check.

## Open

1. Validity of the estimators in the dictionary.
2. Identification of $\epsilon^\ast$ in data, independent of the markers it is meant to predict.
3. The band (8) and the level $\delta^\ast$.
4. The derivation of $c_0$ in (3).
5. The comparative table.

Satellite notes take over from here: dreaming, the lower bound, and defects of control.
