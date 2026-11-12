# 2 UNS Scaffold

Paper 2, Unsurveyability. Version 0.2, 12 November 2026. Register level: Paper, about 12 pages. Conceptual paper. Kernel: `0_LSMN_kernel.md` §2. Items marked [assumed] or [open] need a ruling.

Headline contribution: an account of how a cognitive agent arrives at a dynamic heuristic for navigating an unsurveyable reality. Unsurveyability is intractability plus three obstructions, and the agent answers each obstruction by assigning an ordering.

## Abstract (0.25 page)

- Claim: reality cannot be surveyed from above. Search is therefore local, and local search meets three obstructions.
- Claim: opacity, contingency and transience each force the agent to manufacture something. The three answers combine into a heuristic that is revised as it runs.
- Shape of support: a derivation in steps, with the cul-de-sac and chess as running cases.

## 1. Introduction (1.25 pages)

- Context: Simon asked how agents make goal-directed decisions under resource limits. His images of search were combinatorial and his formal answers were dynamic programs. The passage from the one to the other was left unstated.
- Contribution: the route from an unsurveyable search space to a dynamic heuristic, stated without assuming a view from above at any step.
- Novelty: the obstructions to local search are named, graded and linked. Satisficing appears as the outcome of the derivation and not as its premise.
- Relation to Paper 1: this paper says why an agent needs a map and what the map must supply. Paper 1 says what the agent does to keep the map usable.
- Depends on: nothing. The Simon record needs the fact-check pass.

## 2. No View From Above (1.5 pages)

- Claim: unsurveyable is literal. The agent cannot stand above the search space and inspect it.
- Claim: intractability is the reason. Arranging even a few options in an order, when they interact, yields more arrangements than any agent can enumerate.
- Claim: combinatorial explosion is the closest formal expression of unsurveyability. Reality is not claimed to be combinatorial. The territory is presented as combinatorial because that form keeps the distinctions and shows the pressure they exert.
- Consequence: exhaustive search gives way to local search on local information.
- Claim: intractability acts at each translation. It makes sampling parochial, compression lossy, and navigation a linear sequence of local steps. Each is an economy under the same resource constraint.
- Claim: navigation is the mediation of local steps under a global goal. The goal may be loose.
- Support: territory alone gives paralysis (Buridan). Map alone gives hallucination.
- Kernel: search space, intractability condition.
- Depends on: Section 1.

## 3. Three Obstructions (3 pages)

Lead: the obstructions a navigating agent can meet. Each comes in degrees. Each forces the agent to manufacture something.

### 3.1 Opacity

- Claim: the territory gives no gradient, or one unrelated to the global goal.
- Degree: how well the local gradient tracks the global one. With full tracking the obstruction reduces to noise. [assumed]
- Claim: a combinatorial space differs from a continuous one in kind. It has no differentiable structure and therefore no gradient to give.
- Answer: the agent manufactures a gradient. To do so it builds a continuous map, in which proximity stands for similarity.
- Ordering assigned: comes with. No order.

### 3.2 Contingency

- Claim: physical steps foreclose options.
- Degree: the cost of reversion, from free to impossible.
- Support: the cul-de-sac. Short of impossible, the agent returns to the last branch point. It recovers the search space. It does not recover what it spent.
- Answer: the agent manufactures virtual trajectories and tries them before it steps.
- Ordering assigned: follows from. Logical and negotiable.

### 3.3 Transience

- Claim: the search space changes during the search.
- Degree: the rate of change. In an unchanging space backtracking costs only resources. In a changing one the agent also loses information it had gathered.
- Answer: the agent updates its trajectory on observed divergences.
- Ordering assigned: follows after. Temporal and non-negotiable.

- Kernel: obstruction table, reversion.
- Depends on: Section 2.

## 4. Conjectures (1.5 pages)

- Claim: the three answers form one cycle. The agent invests in a gradient, tries routes along it virtually, steps, and corrects. Conjectures fail in place of the agent (Popper).
- Claim: the obstructions are not independent. [assumed] Where the gradient is reliable, foreclosure costs nothing, so contingency binds in proportion to opacity. Without a committed trajectory, change costs nothing.
- Claim: the unit of navigation is the trajectory. Error compounds along a path of dependent steps.
- Kernel: coupling, cycle.
- Depends on: Section 3.

## 5. The Dynamic Heuristic (1.5 pages)

- Claim: the product of the cycle is a heuristic revised as it runs. It satisfices. It is the best approximation the budget allows.
- Claim: the budget divides among the three answers and movement. Search stops when one more pass costs more than it is expected to return.
- Claim: without intractability the three budgets vanish and the route is optimal. Satisficing is what optimization becomes under unsurveyability.
- Link to Paper 1: part of this budget is what Paper 1 calls allocation. Which part is [open].
- Kernel: heuristic, link to §1.
- Depends on: Section 4.

## 6. Orderings and Their Mathematics (1 page)

- Claim: the agent assigns orderings. It does not do mathematics.
- Claim: relations, functions and dynamics are the primitives that capture the three orderings. They belong to the description.
- Footnote: "directional" as a second reading of the third.
- Kernel: last two columns of the obstruction table.
- Depends on: Section 3.

## 7. The Cube (1.25 pages)

- Claim: the cube is a picture of which obstructions an environment presents. Its eight corners are extreme types.
- Claim: real environments lie inside it and combine the three in degrees.
- Support: chess. Well-structured in rules and roles, and it presents all three obstructions.
- Support: the eight corners with one example each, corrected. SAT and constraint satisfaction share a corner.
- Use: a vocabulary for matching search methods to environments. One paragraph.
- Kernel: cube.
- Depends on: Sections 3 and 6.

## 8. Open Points (0.5 page)

- Completeness: that the three obstructions exhaust intransigence is conjectured.
- Measurement of the degrees: Paper 3.
- Depends on: Sections 3 and 4.

## 9. Conclusion (0.25 page)

- One paragraph. From no view from above to a dynamic heuristic, and the hand-off to Papers 1 and 3.

## References to add

- Carried from 2025: Rice on algorithm selection, Wolpert and Macready on no free lunch, Stadler and Stephens on landscapes, Simon 1957.
- New: Popper on conjectures. Bellman. Simon's dynamic-programming papers. Newell and Simon on heuristic search. All through the fact-check pass.

## Changes from the 2025 version

Full accounting, element by element: `0_LSMN_disposition.md`. The list below is a summary.

- Territory: "the most faithful formal approximation of the state space" becomes the agent's record of encounters.
- Obstructions: binary and independent become graded and coupled.
- Contingency: reversion cost on a scale with both extremes included.
- Primitives: structure of the territory becomes description of orderings the agent assigns.
- New: the conjecture cycle and the dynamic heuristic.
- Removed: the signature-count theorem, "periodic table of territories", the "take it or leave it" passage, the categorical remark.
