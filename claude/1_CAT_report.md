# Consciousness as Translation

Report, draft 0.3, 13 November 2026. Kernel: `0_LSMN_kernel.md` §0.1 and §1. The 2025 paper is the yardstick. Its argument and order are kept. Departures are the eight ruled updates of the kernel, marked U1 to U8 where they enter. [inference] marks a proposal of this draft and [open] a form not fixed. Symbols are listed in the kernel registry.

*The territory is combinatorial; the map is continuous. Out of this friction, consciousness arises.*

To navigate an unsurveyable reality, a cognitive agent has to maintain, and mediate between, two models of the world, one comprehensive (the territory) and one comprehensible (the map). Consciousness arises out of that mediation and out of the need to allocate metabolic resources to keep the two aligned (U2).

The report is conceptual. It uses three stand-ins: the pair combinatorial and continuous, curvature, and the Fisher metric. Papers 3 and 4 make them operational (U6).

## Translation Problem

The world presents more configurations than any finite agent can represent. The agent compresses a combinatorial territory $\mathcal{S}$ into a continuous map $\mathcal{M}$ and navigates by the map. The full chain has four stages (U1):

$$\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N} \tag{1}$$

$\mathcal{L}$ is reality, the landscape. $\sigma$ is sampling, $\pi$ is compression, $\gamma$ is the policy trajectory and $\mathcal{N}$ is navigation. The paper does not claim that reality is combinatorial. Reality is unsurveyable, and combinatorial explosion is the closest formal expression of that property.

Translation fails in four characteristic ways. Together they constitute unsurveyability $U$:

$$U = I + N, \qquad N = (O, C, T) \tag{2}$$

Intractability $I$ is the boundary condition. Configuration spaces grow as $b^d$, $n!$ or $2^n$. Let $\nu(\mathcal{S}_\alpha)$ count the task-relevant distinctions at scale $\alpha$. The territory is unsurveyable whenever

$$\lim_{\alpha \to \infty} \frac{\log \nu(\mathcal{S}_\alpha)}{\dim \mathcal{M}} = \infty \tag{3}$$

Structure proliferates faster than any representation can encode, and translation has to be lossy.

Opacity $O$. The territory provides no gradients. Combinatorial state spaces differ in kind and support no differentiable structure. The agent manufactures a gradient by building a map with smooth geometry. Manufactured gradients need not align with the external objective. In satisfiability problems, flipping a variable to reduce violations locally often raises them globally.

Contingency $C$. Choices alter the topology of the reachable states. Some options are foreclosed and others become costly to recover. In the map, branch points appear as singularities.

Transience $T$. The world is non-stationary, and a map that was valid decays. With $g_F$ the metric of the map defined below, $\operatorname{Ric}$ its Ricci curvature and $L_{\mathrm{decay}}$ the external change,

$$\partial_t g_F = -2 \operatorname{Ric} + L_{\mathrm{decay}} \tag{4}$$

The four form a causal hierarchy:

$$I \to \text{compression} \to O + C + T \to \text{high curvature} \to \text{control} \to \text{consciousness} \tag{5}$$

## Architecture

The agent holds two models (U1, U2).

The territory $\mathcal{S}$ is the comprehensive model. It is the agent's accumulated record of the landscape, kept without order. Sampling has density $\mu_S$, concentrated around the habitats in which the agent lives and sparse elsewhere.

The map $\mathcal{M} = \pi(\mathcal{S})$ is the comprehensible model, with $\pi$ non-injective and $\dim \mathcal{M} \ll \log \lvert \mathcal{S} \rvert$. It presents the available choices ranked by their connection to the objective, as a chess engine ranks moves. Distinct states of the territory can lie close together in the map, and some states of the map correspond to nothing in the territory.

All models are wrong and some are useful (Box). The map is a lossy translation, and its loss is negligible in some instances and decisive in others.

Stand-in. Activity at a point $y \in \mathcal{M}$ generates a distribution $p(\cdot \mid y)$ over responses. The Fisher metric

$$g_F(y)_{ik} = \mathbb{E}\big[\partial_i \log p(\cdot \mid y)\, \partial_k \log p(\cdot \mid y)\big] \tag{6}$$

measures discriminability: how reliably nearby states can be told apart. It arises from the statistics of the coding itself. With a potential $\phi$ that encodes task-relevant value and a control field $w$,

$$\dot{y} = -g_F^{-1} \nabla \phi(y) + w(y) \tag{7}$$

With $w \approx 0$ the agent follows natural gradient descent. This is the backbone of automatic and habitual processing.

## Curvature

The Fisher metric captures discriminability and says nothing about its stability. In some regions discriminability varies smoothly and local information generalizes. In others it changes abruptly, and a small move in the map produces a large change in what can be distinguished.

Let $\kappa(y)$ be the scalar curvature of $g_F$. Large $\kappa$ marks regions where the map is sharply bent, stretched or folded, and where it is least reliable. Curvature relates to perceptual sensitivity:

$$\operatorname{JND}(y) \propto \kappa(y)^{-1/2} \tag{8}$$

High curvature gives fine discrimination and fragility. Low curvature gives coarse discrimination and stability.

High curvature signals that the continuous approximation has broken down. Branch points of the territory appear as singularities, conflicting structure appears as saddle points, and sparse structure appears as sharp ridges and valleys. Curvature is the geometric signature of the translation problem. It carries both how far the map diverges from the territory at an instance and how much that divergence matters for the route.

## Regimes

Behavior partitions into three regimes by a critical level of curvature $\kappa^\ast$. Let $\Gamma(\gamma)$ be the set of alternatives to the current route $\gamma$ that reach the objective and that the territory supports.

| Regime | Condition | Dynamics |
|---|---|---|
| drift | $\kappa < \kappa^\ast$ | $w \approx 0$ in (7) |
| control | $\kappa \ge \kappa^\ast$, $\Gamma(\gamma) \ne \emptyset$ | $w \ne 0$ |
| remap | $\kappa \ge \kappa^\ast$, $\Gamma(\gamma) = \emptyset$ | $g_F \leftarrow g_F + \delta g$ |

Drift. The map represents the territory faithfully enough, and the agent follows it. Drift includes skilled, abstract and rapid behavior in domains where learning has lowered curvature. A chess master in a standard opening drifts. So does a walker on flat ground.

Control. The geometry is fragile and small errors can derail progress. The agent deploys the control field to stabilize its trajectory. Candidate routes are tried virtually before commitment, so that a failed conjecture dies in the agent's stead. Control is effortful and metabolically expensive. A chess player in an unfamiliar position controls.

Remap. Control cannot stabilize the dynamics, and the representation itself changes. This is learning, insight and conceptual change.

The 2025 paper separates control from remap by degree: curvature near $\kappa^\ast$ against curvature far above it. The condition on $\Gamma(\gamma)$ replaces that (U4). Control applies while the map still holds a supported route. Remap applies when it holds none.

$\kappa^\ast$ is specific to the agent and metabolically constrained. It sits where the cost of intervening equals the cost of error.

The envelope of assured navigation $\mathcal{E}$ is the set of states from which the agent reaches its objective under drift or control (U7). A wingsuit flight that ends safely stays inside $\mathcal{E}$ and is far from drift. The envelope answers the dark-room objection to accounts built on minimizing surprise: an agent with an objective leaves the dark room and pays for control to remain assured outside it.

## Consciousness

The integrated control cost over a trajectory is

$$\mathcal{W} = \int \lVert w(y(t)) \rVert^2_{g_F}\, dt \tag{9}$$

and the local instability at a point is

$$\lVert \nabla \kappa(y) \rVert_{g_F} \tag{10}$$

which measures how rapidly the geometric demand changes nearby.

The 2025 paper identifies consciousness with the operation of the control field at $\kappa \approx \kappa^\ast$. Update U3 refines this. Let $a(t)$ be the metabolic allocation to the mediation between map and territory, with $\mathcal{W} = \eta\, a$ and $\eta \in (0, 1]$. Let $e$ index the instances on the route, with curvature $\kappa_e$.

$$a(t) = a_{\mathrm{base}}(t) + \sum_e \Delta a_e(t), \qquad \text{conscious}(t) \iff a(t) > 0 \tag{11}$$

The baseline $a_{\mathrm{base}}$ maintains the live map against transience and is positive throughout wake. The surge $\Delta a_e$ is positive when $\kappa_e \ge \kappa^\ast$ and grows with $\kappa_e$. Consciousness is graded, and its degree at an instance is $\Delta a_e$. It is absent in dreamless sleep and under anesthesia, where $w \equiv 0$. Boredom and stimulus deprivation are low surge on a positive baseline [open].

Two forms are proposed here [inference]. The budget is finite, so surges are served in descending order of $\kappa_e$. Curvature $\kappa_e$ is decreasing in the sampling density $\mu_S(e)$, so that habitats drift and the frontier draws allocation.

Why consciousness here. Three reasons of the 2025 paper stand. Phenomenology aligns: conscious experience is marked by effort, deliberation and active engagement, which is the signature of costly control. Neural and behavioral signatures align: tasks of high curvature produce longer reaction times, more errors and reports of difficulty. Functional necessity aligns: the agent intervenes when the cost of error exceeds the cost of control. One clarification is added. A thermostat and the stomata of a tree also control, against a fixed reference. Control in the sense used here decides between candidate routes before commitment and can revise the map itself.

## Experience

The 2025 paper claimed to dissolve the hard problem. This report does not (U5).

The geometric reading of experience stands as an identification.

| Experience | Geometric reading |
|---|---|
| effort | the rate of control cost in (9) |
| salience | information density, high where $\kappa$ is high |
| meaning | criticality, $\kappa$ near $\kappa^\ast$ |
| intensity | the instability (10) along trajectories with $w \ne 0$ |

Meaning here is felt significance and has no propositional content. Experiences differ in quality because embeddings differ: the geometry of color differs from the geometry of pain.

The hard problem is right that science, which regularizes observations from without, can only triangulate subjective experience within. The same stimuli meet maps with different histories. The same lamp trained on the same object casts different shadows on surfaces of different texture.

The claim of the series is that consciousness is a work effort and no inherent property. Work consumes resources and leaves physical traces, and those traces can be observed from without. No new physics is required. Consciousness stands to the underlying dynamics as temperature stands to kinetic energy.

## Neighbors

The framework connects to established theories. Each governs its own domain, and curvature adds the local criterion for when control becomes necessary.

| Account | What it specifies | What curvature adds |
|---|---|---|
| free energy, predictive coding | the global objective, with $\phi$ as free energy | when minimization becomes unstable |
| bounded rationality (Simon, March) | why agents satisfice | the stopping point is $\kappa^\ast$. Explore and exploit map to remap and drift |
| information theory | rate against distortion | where distortion concentrates. Control as error correction |
| energy-based networks | distributed dynamics with a global temperature | temperature regulated locally |
| global workspace, attention | broadcast | the trigger for broadcast |

Bounded rationality is the economic foundation. Without computational bounds there would be no compression, no translation problem and no consciousness. A fully rational agent would need zero models and cannot be conscious.

## Altered States

Altered states are systematic changes of the same geometry. The survey is qualitative here, and Paper 4 gives it a quantitative form.

| State | Change |
|---|---|
| meditation | lower average $\kappa$, higher $\kappa^\ast$ |
| psychedelics | higher variance of $\kappa$, access to remap |
| flow | sustained navigation near $\kappa^\ast$ |
| dreams | regions of high $\kappa$ explored with actuators gated, control cheap |
| anxiety, rumination | overestimated $\kappa$, control where none is needed |
| anesthesia, dreamless sleep | control disabled, $w \equiv 0$ |

## Implications

The predictions of the 2025 paper stand.

Behavior. Reaction time rises with curvature. Errors cluster in regions of high curvature and differ in kind between drift and control. Strategy shifts from heuristic to systematic as curvature rises.

Neural activity. Control-related activity tracks the approach to $\kappa^\ast$ and does not rise uniformly across tasks. Variability rises near the critical level.

Learning and development. Insight follows struggle. Practice lowers curvature and moves a domain from control to drift. Maturation smooths representations and raises control capacity.

Individual differences. Control capacity varies, and so does the willingness to enter regions of high curvature.

Comparative. Three architectural requirements decide which systems qualify: representations rich enough that compression distorts, a mechanism that detects when following the gradient fails, and the capacity to deploy corrective control. Current large language models do not meet them (U7). They have no adaptive recalibration in runtime and no parochialism, since their sampling has no habitat. The second point makes them the nearest known case of the fully rational agent that cannot be conscious. This replaces the 2025 claim that adaptive AI may require conscious AI.

## Open

1. The forms of $\Delta a_e$, and the two [inference] items under (11).
2. Relations (4) and (8) are carried from the 2025 paper and await the fact check.
3. Boredom and stimulus deprivation under (11).
