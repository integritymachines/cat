# Consciousness as Translation

Report, draft 0.2, 12 November 2026. Kernel: `0_LSMN_kernel.md` §0.1 and §1. Baseline: the 2025 paper. Tags: [ruled] marks a departure decided by the authors, [inference] marks a proposal of this draft, [open] marks a form not fixed. Symbols are defined at first use and listed in the kernel registry.

*The territory is combinatorial; the map is continuous. Out of this friction, consciousness arises.*

This report states the conceptual argument. It uses three stand-ins: the pair combinatorial and continuous, curvature, and the Fisher metric. Papers 3 and 4 replace them with operators and tests.

## Reality

Let $\mathcal{L}$ be reality as a cognitive agent meets it, the landscape. The agent holds two models, a territory $\mathcal{S}$ and a map $\mathcal{M}$, and navigates along a trajectory $\gamma$:

$$\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N} \tag{1}$$

Here $\sigma$ is sampling, $\pi$ is compression and $\mathcal{N}$ is navigation. The landscape is unsurveyable. Unsurveyability $U$ has four constituents, one boundary condition and three obstructions:

$$U = I + N, \qquad N = (O, C, T) \tag{2}$$

Intractability $I$. Let $\nu(\mathcal{S}_\alpha)$ count the task-relevant distinctions at scale $\alpha$. Then

$$I \iff \lim_{\alpha \to \infty} \frac{\log \nu(\mathcal{S}_\alpha)}{\dim \mathcal{M}} = \infty \tag{3}$$

Distinctions outgrow any representation. A scheduling problem with $k$ tasks has $k!$ orderings. Intractability forces local search, and it acts on all three arrows of (1). Sampling is parochial, compression is lossy, and navigation is a linear sequence of local steps.

Opacity $O$. Reality gives no local signal with an assured relation to the global path. A bare wall in a maze gives no signal. An arrow of unknown origin gives a signal that may mislead. The agent has to manufacture its gradients.

Contingency $C$. A step forecloses options or makes them costly to recover. Reversion has a cost $c \in [0, 1]$.

Transience $T$. Reality changes at a rate $\vartheta \ge 0$, and a map that is not maintained decays.

The three obstructions vary between environments and inside one environment, and each can be near zero. They are the dimensions in which the mediation between the global objective and the local step can be obscured. Paper 2 develops them. This report needs only the statements above.

## Engine

To navigate is to choose local steps under a global objective $\zeta$. A tree acts on its surroundings and has no route to choose. An agent with a route to choose in an unsurveyable reality cannot know the route in advance. Each candidate route is a conjecture.

A conjecture can be tested in two ways. The physical test executes $\gamma$ in $\mathcal{L}$, and failure costs the agent a loss $\ell$ that can be the agent itself. The virtual test runs $\gamma$ against what the agent has recorded, and failure costs only the test. In Popper's words, the agent sends its conjectures to their deaths in its stead.

Virtual testing requires a capacity that generates candidate routes, runs them, and discards the failures. We call it the central conjecturing engine. It consumes metabolic resources whether or not a given test changes the route. Navigation with the engine is conjectural. Navigation without it is random, passive or myopic.

The engine comes first in the argument [ruled]. The two models are what the engine needs in order to run.

## Two Models

The engine cannot run on the experienced habitat as recorded, because the record grows with experience as in (3). It needs a compact travel guide. This gives two models with opposite virtues.

The territory $\mathcal{S}$ is the first model. It is the accumulation of impressions, kept without order. Sampling has density $\mu_S$, concentrated around the habitats in which the agent lives and sparse elsewhere. $\mathcal{S}$ is comprehensive and gives no direction.

The map $\mathcal{M} = \pi(\mathcal{S})$ is the second model. The compression $\pi$ is non-injective. $\mathcal{M}$ presents the available choices ranked by how they connect to the objective, as a chess engine ranks moves. It is comprehensible and it has lost distinctions.

Neither model serves alone. The territory without the map gives every option and privileges none. The map without the territory gives confident direction with no check. The agent needs both and a mediation between them.

Stand-in. We picture $\mathcal{S}$ as combinatorial and $\mathcal{M}$ as a smooth manifold. Activity at a point $y \in \mathcal{M}$ generates a distribution $p(\cdot \mid y)$ over responses. The Fisher metric

$$g_F(y)_{ik} = \mathbb{E}\big[\partial_i \log p(\cdot \mid y)\, \partial_k \log p(\cdot \mid y)\big] \tag{4}$$

measures how reliably nearby states can be told apart. With a potential $\phi$ that encodes the objective and a control field $w$, the dynamics are

$$\dot{y} = -g_F^{-1} \nabla \phi(y) + w(y) \tag{5}$$

The first term is natural gradient descent. It is the map's ranking, followed.

All models are wrong and some are useful (Box). The map is a lossy translation of the territory, and the loss is negligible in some instances and decisive in others. The next section says where.

## Curvature

Let $\kappa(y)$ be the scalar curvature of $g_F$ at $y$. Compression produces distortion, and distortion produces curvature. Curvature is low where discriminability varies smoothly, so that local information generalizes. It is high where a small move in $\mathcal{M}$ corresponds to a large change in $\mathcal{L}$. Discrete branch points of $\mathcal{S}$ appear in $\mathcal{M}$ as singularities, and conflicting constraints appear as saddle points.

Curvature therefore carries two things at once: how far the map diverges from the territory at an instance, and how much that divergence matters for the route [ruled]. A flat stretch can be extrapolated. A curved stretch cannot.

The 2025 paper relates curvature to perceptual sensitivity:

$$\operatorname{JND}(y) \propto \kappa(y)^{-1/2} \tag{6}$$

High curvature gives fine discrimination and fragility. Low curvature gives coarse discrimination and stability.

The obstructions of (2) enter through curvature. Opacity makes manufactured gradients unreliable. Contingency produces singularities where $\kappa$ diverges. Transience makes the metric decay,

$$\partial_t g_F = -2 \operatorname{Ric} + L_{\mathrm{decay}} \tag{7}$$

with $\operatorname{Ric}$ the Ricci curvature and $L_{\mathrm{decay}}$ the external change. The causal chain of the 2025 paper stands:

$$I \to \text{compression} \to O + C + T \to \text{high } \kappa \to \text{control} \to \text{consciousness}$$

Let $\kappa^\ast$ be the critical level of curvature. It is specific to the agent. Control costs energy, so $\kappa^\ast$ sits where the expected cost of error equals the cost of intervening.

## Regimes

Let $\Gamma(\gamma)$ be the set of alternatives to the current route $\gamma$ that reach $\zeta$ and that the territory supports.

| Regime | Condition | Dynamics |
|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $w \approx 0$ in (5) |
| control | $\kappa \ge \kappa^\ast$ and $\Gamma(\gamma) \ne \emptyset$ | $w \ne 0$ |
| remap | $\kappa \ge \kappa^\ast$ and $\Gamma(\gamma) = \emptyset$ | $g_F \leftarrow g_F + \delta g$ |

Drift. The agent follows the map, because in that instance the map does not differ substantially from the territory. Drift includes fast, skilled and abstract performance. A chess master in a standard opening drifts.

Control. The map's first offer fails and the map holds another supported route. Conjectures compete. The engine tries them virtually and the control field moves the trajectory to the survivor. A player in an unfamiliar position controls.

Remap. The map holds no supported route. The map itself has to change. This is learning and insight.

The 2025 paper separates control from remap by degree of curvature. The test on $\Gamma(\gamma)$ replaces that separation [ruled]. The boundary between drift and control is a threshold. The boundary between control and remap is a question of existence.

The envelope of assured navigation $\mathcal{E}$ is the set of states from which the agent reaches $\zeta$ under drift or control. A wingsuit flight that ends safely stays inside $\mathcal{E}$ and is far from drift [ruled]. Remap lies outside. The envelope answers the dark-room objection to surprise-minimizing accounts. An agent with an objective leaves the dark room and pays for control so that it remains assured outside it.

## Consciousness

Control work along a trajectory is

$$\mathcal{W} = \int \lVert w(y(t)) \rVert^2_{g_F}\, dt \tag{8}$$

Let $a(t)$ be the metabolic allocation to the mediation at time $t$ and $\eta = \mathcal{W} / a \in (0, 1]$ the efficiency of conversion. An instance $e$ is a point of choice on the route, with curvature $\kappa_e$. Allocation has two parts:

$$a(t) = a_{\mathrm{base}}(t) + \sum_e \Delta a_e(t) \tag{9}$$

The baseline $a_{\mathrm{base}}$ maintains the live map against transience. It is positive during wake. The surge $\Delta a_e$ is positive exactly when $\kappa_e \ge \kappa^\ast$. It is nondecreasing in $\kappa_e$, and at equal $\kappa_e$ it is larger under remap than under control.

Consciousness arises out of the mediation between the two models and out of the need to allocate metabolic resources to it:

$$\text{conscious}(t) \iff a(t) > 0, \qquad \text{degree at } e = \Delta a_e \tag{10}$$

Two assumptions complete the picture. Rationing [inference]: the budget $B$ is finite, $a \le B$, and surges are served in descending order of $\kappa_e$. Sampling [inference]: $\kappa_e$ is decreasing in $\mu_S(e)$, because the map interpolates where sampling is dense and extrapolates where it is sparse.

Result 1.1. Without intractability the agent can survey $\mathcal{L}$. It needs no compression, no map and no mediation, so $a \equiv 0$. A perfectly rational agent needs zero models and cannot be conscious.

Result 1.2. During wake with $\vartheta > 0$, $a \ge a_{\mathrm{base}} > 0$ with no conflict present. Higher-order organisms spend on mediation continuously while awake. Boredom and stimulus deprivation are cases of low surge on a positive baseline [open].

Result 1.3. $\kappa_e < \kappa^\ast$ gives $\Delta a_e = 0$. Processing at $e$ proceeds under drift and is automatic.

Result 1.4. With $w \equiv 0$, as in dreamless sleep and under anesthesia, $a = 0$.

Result 1.5. Practice lowers $\kappa$ on the practiced domain and moves it from control to drift. By the sampling assumption, habitats drift and the frontier draws allocation.

Control occurs in many systems that nobody takes to be conscious. A thermostat, a centrifugal governor and the stomata of a tree correct a deviation against a fixed reference. They test nothing virtually. Control in the table above is conjectural: it decides between virtual conjectures before commitment, and it revises the reference itself under remap. The identification of this mode with consciousness rests on three alignments of the 2025 paper. Effort and deliberate engagement accompany it. Its behavioral and neural markers are those of conscious processing. It engages when needed and is costly enough that it does not engage otherwise.

## Experience

The following are identifications. They are not derived.

| Experience | Geometric reading |
|---|---|
| effort | the rate $\lVert w \rVert^2_{g_F}$ in (8) |
| salience | information density, high where $\kappa$ is high |
| meaning | criticality, $\kappa$ near $\kappa^\ast$ |
| intensity | $\lVert \nabla \kappa \rVert_{g_F}$ along trajectories with $w \ne 0$ |

Meaning here is felt significance. Experiences differ in quality because embeddings differ. The geometry of color differs from the geometry of pain.

The 2025 paper claimed to dissolve the hard problem. This report does not [ruled]. The hard problem is right that science, which regularizes observations from without, can only triangulate subjective experience within. The same stimuli meet maps with different histories. The same lamp trained on the same object casts different shadows on surfaces of different texture. Paper 3 states this as a positive distance between the map of an agent and the map of any observer.

The claim of this series is narrower. Consciousness is a work effort, described by (8) to (10). Work consumes resources and leaves physical traces, and traces can be observed from without. Paper 4 builds its tests on them.

## Offline

During sleep with rapid eye movement the actuators are gated. The engine can then enact conjectures that are far-fetched or potentially lethal, at no physical risk. Offline conjecturing removes singularities of the map and lowers curvature for the next waking period. In the terms of the 2025 paper, curvature is high and control is cheap.

Other altered states are changes of the same quantities.

| State | Change |
|---|---|
| meditation | lower average $\kappa$, higher $\kappa^\ast$ |
| psychedelics | higher variance of $\kappa$, access to remap |
| flow | sustained $\kappa$ just below $\kappa^\ast$ |
| anxiety, rumination | overestimated $\kappa$, control where none is needed |
| anesthesia, dreamless sleep | $w \equiv 0$ |

Paper 4 gives these a quantitative form.

## Bound

Not every system that processes information meets the conditions above. The 2025 paper names three requirements: representations rich enough that compression distorts, a mechanism that detects when following the gradient fails, and the capacity to intervene. Paper 4 turns them into a boundary test.

Current large language models are not capable of conscious navigation [ruled]. They lack adaptive recalibration in runtime: no divergence met during use changes the map. They also lack parochialism: their sampling has no habitat. The second point makes them the nearest known case of Result 1.1.

## Neighbors

Each established account governs its own domain. Curvature adds the local criterion.

| Account | What it states | What curvature adds |
|---|---|---|
| free energy, predictive coding | the global objective, with $\phi$ as free energy | when minimization becomes unstable |
| bounded rationality (Simon) | why search must stop short | the stopping point is $\kappa^\ast$ |
| rate-distortion theory | the trade between compression and fidelity | where distortion concentrates |
| energy-based networks | distributed dynamics with a global temperature | local regulation of temperature |
| global workspace | the architecture of broadcast | the trigger for broadcast |

The series extends Simon's program. Bounded rationality makes compression necessary, and consciousness sits downstream of it.

## Open

1. The form of $\Delta a_e$, and the rationing and sampling assumptions [inference].
2. Whether (6) and (7) survive the fact check. Both are taken from the 2025 paper.
3. Boredom and stimulus deprivation under Result 1.2.
4. The relation of confidence, the low-cost correction inside drift named in the Paper 3 note, to the envelope $\mathcal{E}$ as defined here.
