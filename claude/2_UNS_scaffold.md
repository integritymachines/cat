# Unsurveyability: Scaffold

Version 0.3, 12 November 2026. Baseline: the 2025 paper. Kernel: `0_LSMN_kernel.md` §2. Tags as in the kernel. In the series this paper stands beside Paper 1 as its companion.

Headline. Unsurveyability is the property of reality that forces a cognitive agent to translate between a comprehensive territory and a comprehensible map. It has one boundary condition, intractability, and three sources of instability: opacity, contingency and transience. Each source poses one problem, calls for one kind of ordering, and corresponds to one mathematical primitive.

Status of the paper. Conceptual. A design guide for parsimony in formal modeling (2025, kept).

## 1. The Translation Problem

- Claim: local search has to translate the observable part of a state space into a representation that gives guidance.
- Territory: the most faithful formal approximation of the state space. Comprehensive, intractable and intransigent. It presents alternatives and privileges none.
- Map: a compressed representation that enables movement. Tractable and transigent. Its gradients are manufactured.
- Claim: territory alone gives paralysis (Buridan's ass). Map alone gives hallucination. The map proposes, the territory disposes.
- Claim: parsimony is the most faithful searchable representation.
- Reference: Korzybski.

## 2. No View From Above

- Claim: unsurveyable is meant literally. No agent has a view of the whole.
- Intractability: relevant distinctions exceed the capacity of any feasible map. Limit condition of the kernel.
- Claim: intractability forces local search. It acts at all three translations [ruled]: parochial sampling, lossy compression, navigation as a linear sequence of steps.
- Claim: intractability determines that translation is necessary. The three obstructions determine how it becomes unstable.

## 3. Three Obstructions

### 3.1 Opacity

- Definition (2025): the territory provides no local information that reliably indicates the direction of global improvement.
- Problem posed: identification. What is available in the immediate environment.
- Maze [ruled]: a bare wall gives no gradient. An arrow of unknown origin gives a gradient that may mislead. Opacity is resolved only by establishing that the local arrow correlates with the global path, deterministically or stochastically.
- Hill climbing gives gradients everywhere. They work only where local and global gradients are aligned.
- Claim: in the stochastic case, noise added to the choice can improve on strict following.
- Claim: dense sampling inside a habitat serves to reduce opacity.
- Support (2025): in satisfiability problems, local reduction of violations often raises them globally.

### 3.2 Contingency

- Definition (2025): transitions between states are not freely reversible.
- Problem posed: composition. How the available options connect to the overall objective.
- Claim: reversibility is graded. Cost of reversion in $[0, 1]$, both ends included [ruled].
- Cul-de-sac [ruled]: backtracking recovers the options and does not recover the budget spent.
- Claim: the map enables virtual backtracking at the cost of computation.

### 3.3 Transience

- Definition (2025): the structure of the territory changes over time, or the map decays absent maintenance.
- Problem posed: persistence. How long the options will be available.
- Claim: perfect stability is impossible. The best achievable is equilibrium through continuous maintenance.

### 3.4 Structure

- Causal structure (2025): intractability, compression, intransigence.
- Claim: the degrees of all three vary with the environment and within it, and any can be near zero [ruled].
- Coupling [ruled]: contingency binds in proportion to opacity. Transience binds given a committed trajectory.
- Conjecture (2025): the four dimensions are complete.

## 4. Orderings and Their Mathematics

- Claim: each obstruction is the absence or the kind of an ordering.
- Opacity: comes with. No ordering.
- Contingency: follows from. Logical ordering, negotiable.
- Transience: follows after. Temporal ordering, non-negotiable.
- Correspondence (2025): opacity with relations, contingency with functions, transience with dynamics.
- Claim [ruled]: the agent assigns orderings. Relations, functions and dynamics are the mathematical primitives that capture them. The paper does not claim that a conscious agent makes up mathematics.
- Footnote: "directional" as an alternative to "dynamic".

## 5. Conjectures

- Claim: under the three obstructions a route is a conjecture. Popper: we send our conjectures to their deaths in our stead.
- Cycle: manufacture a ranking, form a virtual route, test it against the territory, step, update.
- Claim: the cycle links the three obstructions. Opacity makes the ranking conjectural, contingency makes the virtual test worth its cost, transience makes the update necessary.

## 6. Activity as Trajectory

- Claim (2025): the endpoint of translation is a trajectory, a sequence of dependent steps.
- Claim: error compounds along the trajectory.
- Claim: unsurveyability is a property of paths under bounded representation.

## 7. The Dynamic Heuristic

- Claim [ruled]: the paper explains the route from an unsurveyable search space to a dynamic heuristic.
- Budgets (Paper 3 note): guidance, virtual search, physical execution, reconciliation, engine maintenance.
- Claim: satisficing is the best approximation under budget. Search stops when one more pass costs more than it is expected to gain.
- Simon: his images are combinatorial, his formal tool is Bellman's dynamic optimization, and his engagement with combinatorial optimization was limited and present [ruled].
- Dependency: Paper 1 identifies the stopping point with the critical level of curvature.

## 8. The Cube

- Signature (2025): presence or absence of relations, functions and dynamics. Eight signatures. Coordinates: intractability and signature.
- The eight corners with the 2025 examples.
- Claim [ruled]: the cube is a metaphor. The corners are extreme types. Environments have graded degrees. Chess presents all three obstructions. It is well-structured, with unambiguous rules and roles, and it is not smooth.
- Open: the reading of the corner with no primitive.

## 9. Implications and Open Points

- Algorithm selection (2025): algorithms assume signatures. Mismatch produces pathologies.
- Expansions (2025): formal definitions of the three obstructions, a diagnostic for signatures, completeness, the structure of the cube.
- Dependency: Paper 3 gives operators for the three primitives.

## 10. Conclusion

- Restates the headline.
- Hands over to Paper 1 (what the translation costs the agent) and Paper 3 (operators).

## Not carried from 2025

- The proof environment for the count of signatures. The count stays as a remark.
- Claim-and-denial phrasing of the 2025 prose.
