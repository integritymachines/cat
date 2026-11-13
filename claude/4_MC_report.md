# Measuring Consciousness

Report, draft 0.4, 13 November 2026. Kernel: `0_LSMN_kernel.md` §4. The research note for Paper 4 is the source of content. The structure follows rounds 1 and 2 of the review protocol, as adopted by the authors. Provenance: [ruled], [inference], [open]. Claim types: (def), (thm), (post) modeling postulate subject to empirical test, (hyp) hypothesis to be confirmed, (ill) illustration. Numbers from the note are unchecked and are not carried as established values.

This paper makes the theory measurable, predictive and falsifiable [ruled]. It states what is measured, how the estimators are qualified, which tests the model elements face, and which failure refutes which claim.

## Science

Paper 1 states the theory with synecdoches. Paper 3 gives computable candidates for its mechanisms. A scientific theory also needs observables, estimators that are qualified independently of the claims they test, predictions made before the data, comparison with simpler accounts, and conditions under which it fails.

Thesis. An agent forms its map $\mathcal{M}_{\mathrm{int}}$ from its own sampling and compression. An observer forms $\mathcal{M}_{\mathrm{ext}}$ from another. By Proposition 3.3 the two generically stand at a positive discrepancy:

$$d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) > 0 \tag{1}$$

Scientific observation is a second lossy translation of first-person experience. It observes behavior and physiology from without and regularizes them across instances. Lemma 3.2 gives the complement. When the route that the map offers fails the lift test, the agent reaches its goal only with a nonzero control field $w$ or a change of the map. By Postulate 1.0 of Paper 1, control at a critical limit consumes a metabolic allocation and produces control work. Both are physical, and both leave traces. The tests below concern those traces. They make no claim to measure experience itself.

Tests of a mathematical realization ask whether its mechanisms describe agents. Tests of the consciousness postulate ask a further question, whether mediation and resource allocation go with experience. Each failure is recorded at the level where it occurs. The illustrative status of Paper 1 does not shield a committed operational model from refutation. Each test names the claims it puts at risk and the freedom that remains after a failure.

## Constructs

| Construct | Definition | Units | Candidate observables (note) |
|---|---|---|---|
| $a(t)$ | metabolic power allocated to mediation, excluding background metabolism | power | regional hemodynamics, pupil diameter, autonomic balance |
| $a_{\mathrm{base}}$, $\Delta a_e$ | waking baseline, surge at instance $e$ | power | contrast of task against matched rest |
| $\mathcal{W}$ | controller expenditure over a matched interval $\Theta$: flow correction plus the controller's own updates | energy, after calibration | behavioral correction, model fits, decision boundary |
| $\eta$ | $\mathcal{W} / \int_\Theta \sum_e \Delta a_e\, dt$ | dimensionless | ratio of the two above |
| $\lambda_\zeta$, $\lambda_2$ | task-conditioned and global gap of $K_M$ | inverse time, under a time scale | graph reconstructed from recording channels |
| $\operatorname{lift}$ | support of a route by the record | count | task design with known territory |
| $d_{\mathcal{SM}}$, $d_{\mathrm{GW}}$ | squared distortion, squared transport discrepancy | squared distance | dissimilarity matrices across epochs or agents |
| $\log \operatorname{Tor}$ | signed observable of deformation | dimensionless | log determinants on reconstructed complexes |

Assumption 4.1 (post). $\hat{a}$ is increasing in $a$.

Postulate 4.2 (post, from the note). For deformation induced by the controller over $\Theta$, the controller's expenditure is bounded below by the deformation it achieves:

$$\mathcal{W} \ge c_0\, \lvert \Delta_{\mathrm{ctrl}} \log \operatorname{Tor} \rvert, \qquad c_0 > 0 \tag{2}$$

$\Delta_{\mathrm{ctrl}}$ counts only the changes of $G$, $K_M$ or $\pi$ that the controller makes within $\Theta$ [ruled]. Passive change, such as drift of the map with $w = 0$, is excluded, since it shifts torsion at no cost to the controller. (2) is an element of the model, subject to test in Test 4.6. It is not derived from the torsion variation of Paper 3, which supplies no energetic bound. Log torsion is not identified with control work [ruled]. Two options are held in reserve: a bound on total update expenditure, or torsion as a conditional predictor without a bound.

Separating $a$ from $\mathcal{W}$ matters where the two decouple. In flow, much work is done at low input and $\eta$ is high. In overload, input is high and the trajectory stalls, so $\eta$ is low.

## Qualification

Every test is conditional on qualified estimators. The note proposes a forward mapping:

| Operator (Paper 3) | Role | Candidate estimator (note) |
|---|---|---|
| $K_S$ against $K_M$ | record against compressed map | orthogonal subspaces in population activity |
| $\Delta_0$, $\lambda_2$, $\lambda_\zeta$ | identification | graph Laplacian from connectivity among channels |
| $\Delta_1$, $\beta_1$ | composition | persistent cohomology of population state clouds |
| $\operatorname{Tor}$ | deformation | log determinants on empirical clique complexes |
| $d_{\mathrm{GW}}$ | discrepancy between maps | transport between dissimilarity matrices |

The note names four empirical supports for this mapping: a factorization of hippocampal activity into orthogonal subspaces for drift in time and for position, a link between the spectrum of $\Delta_0$ and the participation ratio $\operatorname{PR}$, a contraction of variability in familiar regimes with aliasing at the boundary of ignorance, and a multiplexing of dominant and suppressed percepts during rivalry. All four are candidates until fact-checked.

Qualification rules (def):

1. Each estimator is validated on synthetic graphs with known structure, on known interventions and on held-out recordings.
2. A reconstructed neural connectivity graph is not assumed to be the agent's map. The relation is itself tested.
3. Threshold calibration and confirmation use separate data. If the same control marker both sets $\epsilon^\ast$ and confirms the transition, the test is circular.
4. Each test is compared against simpler accounts: difficulty, uncertainty, response conflict, standard sequential sampling.

## Waking Tests

The tests follow the transition from drift to control. Their forms are elements of the model, subject to empirical test (post) [ruled].

Test 4.3 (threshold). At an independently calibrated task threshold, control policy and control cost change. The estimated $\hat{\lambda}_\zeta$ predicts where the threshold lies. The note predicted a step drop of $\hat{\lambda}_2$. A smooth change of weights moves the spectrum smoothly, so the step belongs to the policy and not to the eigenvalue.

Test 4.4 (latency). $\lambda_\zeta^{-1}$ is the integrated autocorrelation time of the goal vector under diffusion on the map (Paper 3). We postulate, for the specified task and calibration,

$$\mathbb{E}[\text{response time}] = t_0 + c_1\, \lambda_\zeta^{-1} \tag{3}$$

near the threshold, with $t_0$ and $c_1$ estimated independently. No spectral identity implies (3). It is a behavioral postulate. The note's form $\lvert \lambda_2 - \epsilon^\ast \rvert^{-1/2}$ diverges where the relaxation time stays finite. It requires a bifurcation model and is carried as an alternative [open]. Variability across trials rises in the same window, and errors separate into fast slips under drift and slow errors under control.

Test 4.5 (braking). Let $\operatorname{bnd}$ be the decision boundary of a sequential-sampling model. A rise of $\operatorname{bnd}$ is predicted by a failed lift of the offered route and by the demand for revision. $\Delta \log \operatorname{Tor}$ adds explanatory power beyond these. The behavioral form is vicarious trial and error at a fork: the agent stops, samples the options, and reverses a prepotent movement.

Test 4.6 (expenditure). Over matched intervals, $\int_\Theta \hat{a}\, dt$ tracks measured controller expenditure $\hat{\mathcal{W}}$ with slope $\eta^{-1}$. $\lvert \Delta_{\mathrm{ctrl}} \log \operatorname{Tor} \rvert$ adds out-of-sample prediction, as (2) requires. A passive change of the map with $w = 0$ must leave both $\hat{\mathcal{W}}$ and the prediction unaffected.

Individuals differ in baseline $\epsilon^\ast$ and in $\eta$. The note reads the margin just above $\epsilon^\ast$ as confidence, the low-cost correction of minor divergence, and reads individual differences in that margin as a spectrum between sequential and parallel styles of cognition. Organisms differ in how they allocate, and Tests 4.3 to 4.6 are where that variance can be picked up. Bat navigation is a candidate case: stereotyped flight corridors with sonar locked to the wingbeat under drift, and strobe groups with braking when a target is displaced.

## State Contrasts

Paper 1 describes altered states qualitatively. Here they are experimental contrasts in which the model's predictions differ. They are not a classification of conscious systems.

| State | Paper 1 | Contrast |
|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $\lambda_\zeta > \epsilon^\ast$, $a = a_{\mathrm{base}}$ |
| overload | $\kappa \ge \kappa^\ast$, sustained | $\lambda_\zeta \le \epsilon^\ast$ sustained, $\eta$ low |
| flow | $\kappa$ just below $\kappa^\ast$ | $\lambda_\zeta$ just above $\epsilon^\ast$, $\eta$ maximal |
| meditation | lower $\kappa$, higher $\kappa^\ast$ | baseline $\lambda_\zeta$ raised, larger $\mathcal{E}$ |
| psychedelics | higher variance of $\kappa$ | higher $\operatorname{PR}$, large $d_{\mathrm{GW}}$ from baseline, remap afterward |
| propofol | no mediation | long-range $\lambda_2 \to 0$, $\mathcal{W} \to 0$, $a$ suppressed |
| ketamine, REM | control without actuators | $\mathcal{W} > 0$ internally, input and output gated |

The cycle count $\beta_1$ is not used to classify states. A harmonic cycle is no contradiction by itself (Paper 3).

The table makes three commitments that can fail separately. Flow and overload differ in $\eta$ at comparable work. Propofol and ketamine differ in internal $\mathcal{W}$ at comparable unresponsiveness. Meditation moves the baseline, and psychedelics move the variance.

Test 4.7 (absence). State, task and recording sensitivity are fixed in advance. Under propofol and in dreamless sleep, the control channel does not respond to a manipulated $\lambda_\zeta$. Local responses to input can persist. Positive controls (wake, ketamine) and negative controls (stimulation that does not change $\lambda_\zeta$) are required. Lack of external response is separated from absence of internal processing.

## Agents

Two agents $A$ and $B$ hold maps compressed from private territories. They coordinate under drift while

$$d_{\mathrm{GW}}(\mathcal{M}_A, \mathcal{M}_B) < \delta^\ast \tag{4}$$

and build a shared representation as the discrepancy falls (post). At or above $\delta^\ast$, automatic coordination breaks down, and the agents need explicit translation at the boundary between their maps, with $w \ne 0$ on both sides. The note predicts that compatibility follows relational geometry, the structure of distances inside each map, and not similarity of attributes. The note's value for $\delta^\ast$ is not carried.

## Design

The first test bed is artificial. The investigator knows the territory graph and its changes, while participants see only local observations. Four factors are manipulated independently:

| Factor | Manipulation |
|---|---|
| opacity | quality of local cues, with connectivity unchanged |
| contingency | cost or irreversibility of a wrong branch |
| transience | frequency and location of changes to edges |
| task location | inside a well-connected cluster, or across a weak bridge |

Measures: choice, virtual backtracking, latency, error, revision of policy, model fits, metabolic markers, and independently estimated neural statistics. A Fisher-informed model and a graph-only model are fitted to the same trials and predict held-out perturbations. Two questions are kept apart. Predictive contribution asks whether the Fisher-informed model predicts better. Explanatory sufficiency asks whether the graph-only model keeps the distinctions the theory requires. A null result on the first does not settle the second, since weak observations, weak perturbations or misspecification can hide a difference. The Fisher bench of Paper 3 runs before any biological data.

Negative controls are cases A to E and H to J of the Paper 3 bench: a small global gap with a local task, a large gap with a false shortcut, a harmless cycle, an omitted transition, slow drift of one weight, a faithful but slow path, a supported but costly route, and repeated failure under control. A passive change of the map with $w = 0$ is added for Postulate 4.2. If the model cannot classify its own finite cases, no neural estimator can repair it.

## Falsification

Each failure refutes one layer. A failure is not reassigned to the estimator by default, and an estimator failure does not refute the whole series.

| Layer | Fails when |
|---|---|
| operator | under known graphs, the identities of Paper 3 or the fixed classifier fail on the bench. This is an internal test of the realization |
| bridge | Fisher-informed and graph quantities disagree beyond their stated domain |
| mechanism | qualified quantities fail to predict route failures, corrections or expenditure prospectively. In particular: control markers scale linearly through the threshold of Test 4.3, or the control channel responds to $\lambda_\zeta$ under the conditions of Test 4.7 as it does in wake |
| consciousness link | the mechanism is present where experience-related evidence is absent, or absent where it is present, under a stated measurement theory |

The last layer tests Postulate 1.0 of Paper 1. It is tested last, and it remains a postulate. No effect size is asserted before the fact check.

## Open

1. Validity of the estimators in the qualification table.
2. Identification of $\epsilon^\ast$ in data, independent of the markers it predicts.
3. Calibration of $\mathcal{W}$ in energy units.
4. The constant $c_0$ in (2), the form of the controller's update cost, and the level $\delta^\ast$ in (4).
5. The alternative latency form with exponent $-\tfrac12$.
