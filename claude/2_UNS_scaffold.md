# 2 UNS Scaffold

Paper 2, Unsurveyability. Version 0.1, 12 November 2026. Register level: Paper, 10 to 15 pages. Conceptual paper. Items marked [assumed] or [open] need a ruling.

## Abstract

- Claim: reality cannot be surveyed from above. This forces local search, and local search meets three obstructions.
- Claim: unsurveyability is intractability plus intransigence, and intransigence is opacity, contingency and transience.
- Claim: an agent answers each obstruction by assigning an ordering. The three answers combine into a dynamic heuristic, which is a satisficing solution under a budget.
- Shape of support: a derivation in steps from the search space to the heuristic, with worked cases.

## 1. Introduction

- Context: Simon's question of how agents decide under resource limits. The formal tradition answered with dynamic programs. The combinatorial side of the question stayed open.
- Contribution: an account of how an agent gets from an unsurveyable search space to a dynamic heuristic.
- Relation to Paper 1: Paper 1 says what the agent does with its map. This paper says why it needs one and what the map must supply.
- Depends on: nothing.

## 2. No View From Above

- Claim: unsurveyable is meant literally. The agent cannot stand above the search space and inspect it.
- Claim: intractability is the reason. Arranging even a few distinct options in an order, under interaction effects, produces more arrangements than any agent can enumerate.
- Consequence: exhaustive search gives way to local search on local information.
- Navigation: the mediation of local steps under a global goal, which may be loose or ill-defined.
- Keep from the 2025 version: paralysis on territory alone (Buridan), hallucination on map alone.
- Change: the territory is the agent's record of encounters, as in the four-stage chain. It is no longer "the most faithful formal approximation of the state space".
- Depends on: Section 1.

## 3. Three Obstructions

Lead: these are the fundamental obstructions a navigating agent can meet. Each comes in degrees.

### 3.1 Opacity

- Claim: the territory gives no gradient, or gives one that does not track the global goal.
- Degree: how well local gradients correlate with the global one. Full opacity is no correlation. As correlation rises, the obstruction fades into noise. [assumed]
- Answer: the agent manufactures gradients.
- Ordering: comes with. No order is given.

### 3.2 Contingency

- Claim: physical steps foreclose options.
- Degree: reversion cost on $[0, 1]$. At 0, backtracking is free. At 1, it is impossible.
- Support: the cul-de-sac. Below cost 1 the agent can return to the last branch point. It recovers the search space and not the resources spent.
- Answer: the agent manufactures virtual trajectories before it steps.
- Ordering: follows from. Logical, negotiable.

### 3.3 Transience

- Claim: the search space changes while the agent searches.
- Degree: rate of change. In an invariant space there is no transience and backtracking loses only resources. In a variant space the agent also loses information it had collected.
- Answer: the agent updates its trajectory in real time on observed divergences.
- Ordering: follows after. Temporal, non-negotiable.

- Depends on: Section 2.

## 4. Conjectures

- Claim: the three answers are linked. The agent invests in a gradient, tests routes along it virtually, and corrects as it moves. This is Popper's point that conjectures can die in the agent's stead.
- Claim: the obstructions are therefore not independent. [assumed] Foreclosure costs nothing when the gradient is reliable, so contingency binds in proportion to opacity. Change costs nothing without a committed trajectory.
- Trajectory: the unit of navigation is a path of dependent steps. Error compounds along it. Merge the 2025 section "Activity as Trajectory" here.
- Depends on: Section 3.

## 5. The Dynamic Heuristic

- Claim: what the agent ends up with is a heuristic that is revised as it runs. It is a satisficing solution, which is the best approximation the budget allows.
- Budget: effort divides among building gradients, testing routes, moving, and reconciling map with territory. State in words. Paper 3 formalizes.
- Link to Paper 1: reconciling is the synchronization that Paper 1 identifies with consciousness.
- Depends on: Section 4.

## 6. Orderings and Their Mathematics

- Claim: the agent assigns orderings. It does not do mathematics.
- Claim: relations, functions and dynamics are the primitives that capture the three orderings. They belong to the description.
- Footnote: "directional" as an alternative reading of the third.
- Change from the 2025 version: Principle 1 presented the primitives as structure the territory possesses, and derived irreversibility from non-injective functions.
- Depends on: Section 3.

## 7. The Cube

- Claim: the cube is a picture of which obstructions a search environment presents. Its eight corners are extreme types.
- Real environments sit inside the cube and combine the three in degrees. Chess presents all three.
- Keep: the eight corner descriptions, shortened.
- Fix: the diagnostic examples. They are written as four-tuples, and SAT is placed at the dynamical corner while constraint satisfaction is listed at the relational one.
- Remove: the signature-count theorem, "periodic table of territories".
- Use: a vocabulary for matching search methods to environments. One paragraph.
- Depends on: Sections 3 and 6.

## 8. Open Points

- Completeness: that these three exhaust intransigence is argued and not proven. State once.
- Measuring the degrees: deferred to Paper 3.
- Remove: the "take it or leave it" passage and the categorical-structure remark.

## 9. Conclusion

- One paragraph. The route from no view from above to a dynamic heuristic, and the hand-off to Papers 1 and 3.

## References to add

- Popper on conjectures. Bellman. Simon's dynamic-programming papers. Newell and Simon on heuristic search. Fact-check pass required.
