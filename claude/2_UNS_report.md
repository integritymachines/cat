# Unsurveyability

Report, draft 0.1, 12 November 2026. Kernel: `0_LSMN_kernel.md` §2. Baseline: the 2025 paper. Tags: [ruled] marks a departure decided by the authors, [inference] marks a proposal of this draft, [open] marks a form not fixed.

This report is conceptual. It characterizes what makes the translation from territory to map unstable. It can be read before or after Paper 1.

## Translation Problem

A search process sees a small part of a state space and has to act on the whole. It translates between two representations.

The territory $\mathcal{S}$ is the most faithful formal approximation of the state space. It keeps the relevant distinctions and fabricates no structure. It presents alternatives and privileges none.

The map $\mathcal{M}$ is a compressed representation that enables movement. It orders the alternatives into better and worse. The ordering is manufactured. The map discards distinctions and smooths discontinuities in the service of search.

Let $j$ be the direction the map supplies and let a route $\gamma$ be a sequence of steps.

| Representation | Supplies | Alone it produces |
|---|---|---|
| $\mathcal{S}$ | fidelity, no $j$ | paralysis: every option visible, none privileged |
| $\mathcal{M}$ | $j$, untested | hallucination: confident movement with no check |

Buridan's ass is the first case. A map that reads "this way" at a cliff is the second. The map proposes and the territory disposes. Unsurveyability $U$ is the property that forces this translation:

$$U = I + N, \qquad N = (O, C, T) \tag{1}$$

$I$ is intractability, the boundary condition. $N$ is intransigence, with its three modes opacity $O$, contingency $C$ and transience $T$.

## Intractability

Let $X$ be the set of arrangements of $k$ interacting options, with objective $\operatorname{val}: X \to \mathbb{R}$. Then $\lvert X \rvert \ge k!$. Let $\nu(\mathcal{S}_\alpha)$ count the relevant distinctions of the territory at scale $\alpha$.

$$I \iff \lim_{\alpha \to \infty} \frac{\log \nu(\mathcal{S}_\alpha)}{\dim \mathcal{M}} = \infty \tag{2}$$

Unsurveyable is meant literally. No agent has a view from above. Under $I$ the state at time $t+1$ is chosen in a neighborhood of the state at $t$:

$$I \Rightarrow x_{t+1} \in \operatorname{Nbr}(x_t) \tag{3}$$

Intractability acts at each translation of the chain $\mathcal{L} \to \mathcal{S} \to \mathcal{M} \to \mathcal{N}$ [ruled].

| Translation | Intractability forces |
|---|---|
| sampling of reality into territory | parochial sampling, dense in habitats |
| compression of territory into map | lossy compression |
| map into navigation | a linear sequence of local steps |

Without $I$, the map can copy the territory and the remaining sections have no object. With $I$, compression is mandatory. Intractability says that translation is necessary. Intransigence says how it becomes unstable.

## Obstructions

Each mode of intransigence obstructs the mediation between the global objective and the local step in its own way, and each poses one problem to the agent.

**Opacity.** The territory provides no local information that reliably indicates the direction of global improvement. The problem posed is identification: what is available in the immediate environment.

A maze shows two forms. A bare wall gives no gradient. An arrow of unknown origin gives a gradient with no assured relation to the exit. Let the degree of opacity be

$$o = 1 - \operatorname{corr}\big(\nabla_{\mathrm{loc}} \operatorname{val},\ \nabla_{\mathrm{glob}} \operatorname{val}\big) \in [0, 1] \tag{4}$$

Opacity is resolved only by establishing that the local signal correlates with the global path. The correlation can be deterministic ($o = 0$) or stochastic ($0 < o < 1$). For $o < 1$, following the signal is better than ignoring it. For $0 < o < 1$, noise added to the choice can improve on strict following, and the useful noise vanishes as $o \to 0$. Hill climbing has a gradient everywhere and succeeds only where local and global gradients are aligned.

Sampling lowers opacity. Inside a habitat, where the sampling density $\mu_S$ is high, the agent has learned which local signals correlate with which outcomes.

**Contingency.** Transitions between states are not freely reversible. The problem posed is composition: how the available options connect to the overall objective.

Let $\Omega_t$ be the options reachable at $t$ and $c \in [0, 1]$ the cost of reversion, with both ends included. At $c = 1$ a step forecloses. At $c < 1$ the agent can return from $t$ to an earlier $t'$:

$$\Omega_t \leftarrow \Omega_{t'}, \qquad \text{budget spent between } t' \text{ and } t \text{ is not restored} \tag{5}$$

A cul-de-sac shows the point. Walking back recovers the options and does not recover the time. The map offers virtual backtracking: a route is simulated before commitment, at the cost of computation. Virtual backtracking is as good as the map's fidelity.

**Transience.** The structure of the territory changes over time at a rate $\vartheta \ge 0$, or the map decays absent maintenance. The problem posed is persistence: how long the options will be available. A map that was accurate becomes inaccurate. Stability is available only as equilibrium under continuous maintenance.

**Structure.** The causal order of the 2025 paper stands:

$$I \to \text{compression} \to N = \{O, C, T\}$$

The degrees $(o, c, \vartheta)$ vary between environments and inside one environment, and each can be near zero [ruled]. The three modes are not independent [ruled]. Contingency binds in proportion to opacity: an agent that can see which branch is right loses nothing to irreversibility. Transience binds given a committed trajectory: change hurts an agent in proportion to what it has planned. As a form [inference], the expected losses are

$$\ell_C = \ell_C(o \cdot c), \qquad \ell_T = \ell_T(\vartheta, \lvert \gamma \rvert), \qquad \ell_C(0) = \ell_T(0, \cdot) = \ell_T(\cdot, 0) = 0 \tag{6}$$

both increasing. That $I$, $O$, $C$ and $T$ exhaust unsurveyability is conjectured and not proved.

## Orderings

Each obstruction corresponds to an ordering that the options have or lack, and each ordering is captured by one mathematical primitive: relations $R$, functions $F$ or dynamics $D$.

| Obstruction | Problem | Ordering | Primitive |
|---|---|---|---|
| $O$ | identification | comes with: none | $R$: adjacency, compatibility, constraint |
| $C$ | composition | follows from: logical, negotiable | $F$: maps that can collapse distinctions |
| $T$ | persistence | follows after: temporal, non-negotiable | $D$: iterated transformations |

Under opacity, what remains is relational structure without direction or distance. Under contingency, a choice maps a set of options to a smaller set, and non-injective maps cannot be undone. Under transience, the structure is carried forward by a transformation that does not wait.

The agent assigns orderings to what it meets. Relations, functions and dynamics are the primitives in which mathematics captures these orderings. The paper makes no claim that a conscious agent makes up mathematics [ruled]. "Directional" is an alternative name for the third primitive.

## Conjectures

Under opacity the map's direction $j$ is a guess. Under contingency a wrong guess is costly to take back. Under transience a right guess expires. A route is therefore a conjecture, and the agent benefits from testing it before it commits. Popper's phrase applies: we send our conjectures to their deaths in our stead.

The agent runs a cycle:

$$j \;\to\; \gamma \;\to\; \text{virtual test of } \gamma \text{ against } \mathcal{S} \;\to\; \text{step} \;\to\; \text{update} \tag{7}$$

Each stage answers one obstruction. The ranking $j$ answers opacity. The virtual test answers contingency. The update answers transience. Paper 3 gives the test an exact form, the lift of a map route into the territory.

## Trajectory

The endpoint of translation is a trajectory $\gamma$, a sequence of actions whose feasibility and value depend on earlier commitments. The three obstructions act along $\gamma$:

- opacity makes local gradients unreliable predictors of distant consequences,
- contingency couples each action to a loss of future options,
- transience makes a correct projection decay.

Error compounds along the trajectory. A small misalignment at one step can amplify into a large deviation later. As a form [open], with $\operatorname{err}_i$ the misalignment after step $i$ and a growth rate $\operatorname{rate} \ge 0$ that increases in each of $o$, $c$ and $\vartheta$,

$$\operatorname{err}_{i+1} = (1 + \operatorname{rate}(o, c, \vartheta))\, \operatorname{err}_i \tag{8}$$

Unsurveyability is a property of paths under bounded representation. Guidance has to remain robust across a chain of dependent actions.

## Heuristic

The cycle (7) runs under a budget. Following the note for Paper 3, we split it:

$$B = B_R + B_F + B_D + B_w + B_0 \tag{9}$$

| Budget | Pays for |
|---|---|
| $B_R$ | constructing guidance where none is supplied |
| $B_F$ | exploring, comparing and rejecting virtual routes |
| $B_D$ | physical execution |
| $B_w$ | reconciliation of map and territory |
| $B_0$ | maintenance of the engine |

The heuristic is the route returned by the cycle under $B$, revised at each step. It is dynamic because every stage is repeated as the agent moves. Search stops when the expected gain in $\operatorname{val}$ from one more pass falls below the cost of the pass. This is satisficing in Simon's sense: the best approximation under budget. Without intractability, $B_R = B_F = B_w = 0$ and the route is optimal.

Simon's images of search are combinatorial and his formal tool is Bellman's dynamic optimization. His engagement with combinatorial optimization was limited and it was present. The route from an unsurveyable search space to a dynamic heuristic, described here, connects the two. Paper 1 identifies the stopping point with a critical level of curvature.

## Cube

The presence or absence of each primitive gives a structural signature:

$$\operatorname{sig} = (R, F, D) \in \{0, 1\}^3 \tag{10}$$

There are $2^3 = 8$ signatures. The coordinates of a translation problem are $(I, \operatorname{sig})$. Intractability scales the cube and the signature locates within it.

| $\operatorname{sig}$ | Name | Examples (2025) |
|---|---|---|
| $(0,0,0)$ | empty | no formalizable structure |
| $(1,0,0)$ | relational | graph problems, constraint satisfaction |
| $(0,1,0)$ | functional | pattern matching, classification, inverse problems |
| $(0,0,1)$ | dynamical | Rubik's cube |
| $(1,1,0)$ | relational-functional | metric spaces, manifolds |
| $(1,0,1)$ | relational-dynamical | graph rewriting, network flow |
| $(0,1,1)$ | functional-dynamical | dynamical systems, control, reinforcement learning |
| $(1,1,1)$ | full | job-shop scheduling, protein folding, strategic planning |

The cube is a metaphor [ruled]. Its corners are extreme types, and environments have graded degrees $(o, c, \vartheta)$. Chess presents all three obstructions. It is well-structured, because its rules and roles are unambiguous, and it is not smooth.

Algorithms assume signatures. Constraint propagation assumes relational structure, gradient descent assumes functional structure with smoothness, and local search assumes dynamical structure. Where the assumption matches the territory, performance is good. Where it does not, pathologies appear.

## Parsimony

Let $d_{\mathcal{SM}}$ be the distortion between territory and map. The parsimonious translation is the most faithful representation that can still be searched:

$$\pi^\ast = \arg\min_\pi\ d_{\mathcal{SM}} \quad \text{subject to } \dim \mathcal{M} \text{ within capacity} \tag{11}$$

The territory acts as the agent of the state space and the map as the agent of the representational limits. Parsimony lies between them. Paper 3 defines $d_{\mathcal{SM}}$.

## Open

1. The corner $(0,0,0)$. The 2025 paper reads it as a territory with no formalizable structure. Under graded degrees, the point where all three degrees vanish is an environment with no obstruction. The two readings need to be reconciled.
2. Formal definitions of the three obstructions beyond (4) and (5), and the form of (6) and (8).
3. A procedure that determines the signature of a territory from samples.
4. Whether intermediate signatures behave as restrictions of the full signature.
5. Completeness of the four dimensions.
