# 3 TG Scaffold

Paper 3, Translation Geometry. Version 0.1, 12 November 2026. Register level: Paper, about 14 pages. Scientific paper. Kernel: `0_LSMN_kernel.md` §3 and §5. Source: Research Note, Paper 3. Items marked [assumed] or [open] need a ruling.

Headline contribution: every construct of Papers 1 and 2 is given an operator on two finite complexes, so that consequence, divergence, the critical level and the three regimes can be computed. One small case is computed in full.

## Abstract (0.25 page)

- Claim: the stand-ins of Paper 1 are replaced by operators on a territory complex and a map complex.
- Claim: drift ends at a critical level that depends on the divergence found. Control and remap are separated by a lift test.
- Shape of support: definitions, their properties, and one worked case in which all operators act on the same agent.

## 1. Introduction (1.25 pages)

- Context: Papers 1 and 2 state the account in words and one smooth picture. A scientific theory needs quantities that can be computed and can come out wrong.
- Contribution: operators for the manufactured gradient, for consequence and use, for divergence, for support by the territory, and for change of the map.
- Novelty: the critical level is not a constant. It is the divergence divided by a tolerance. The second regime boundary is a reachability test and not a level.
- Scope: no neural data. Measurement is Paper 4.
- Depends on: Papers 1 and 2.

## 2. From Picture to Operator (2 pages)

- Claim: Papers 1 and 2 present a combinatorial territory and a continuous map. The pair shows that the two models differ in kind. This paper refines the pair and keeps that function.
- Claim: territory and map are finite complexes joined by a compression that is many-to-one. The territory complex carries relations only and has no potential. The map complex carries weights, a potential and a flow, which are the discrete counterparts of continuous structure.
- Claim: the smooth manifold itself is given up. Steps are path-dependent, the map changes, and curvature cannot be computed from data.
- Support: the correspondence table. Each element of the picture, the operator that replaces it, and what the replacement makes computable.
- Claim: an instance is an edge of the map, together with the territory vertices that the compression sends to its ends.
- Kernel: §0.1, §5.
- Depends on: Section 1.

## 3. Manufactured Direction (1.25 pages)

- Claim: connectivity alone gives no direction. Direction appears when a goal is posed on the map.
- Operator: the graph Laplacian with a goal vector gives a potential and a flow.
- Claim: the flow is the agent's manufactured gradient. Its magnitude on an edge is the use of that instance.
- Degree of opacity: how far the manufactured flow departs from the flow the landscape would give. [assumed] The reference flow is not available to the agent.
- Kernel: gradient, use.
- Depends on: Section 2. Answers opacity.

## 4. Consequence (1.25 pages)

- Claim: the consequence of a divergence at an instance is the inverse of its effective conductance.
- Support: a bridge edge has the lowest conductance its weight allows. A door is a bridge. A handle is not an edge of the route at all.
- Claim: the spectral gap is a summary over the whole map. It does not locate an instance and cannot serve as the local quantity.
- Kernel: conductance, consequence.
- Depends on: Section 3.

## 5. Divergence (1.25 pages)

- Claim: divergence at an instance is the distortion of territory distances under compression, restricted to that instance.
- Claim: total divergence is the same sum over the whole territory.
- Claim: compression is always lossy and mostly benign. Divergence matters when weighted by consequence.
- Kernel: divergence, total divergence, warrant.
- Depends on: Sections 2 and 4.

## 6. Support and Alternatives (1.5 pages)

- Claim: a route on the map is supported by the territory when a connected path in the territory projects onto it. The lift functional counts such paths.
- Claim: a failed lift is the strongest divergence. The compression has joined territory regions that are not connected.
- Claim: the set of supported alternatives decides between control and remap.
- Claim: a virtual trajectory is a route whose lift is computed before the step. This is the operator form of trying conjectures.
- Reversion cost on the territory relation: [open].
- Kernel: lift, alternatives.
- Depends on: Sections 3 and 5. Answers contingency.

## 7. The Critical Level (1.25 pages)

- Claim: drift holds while conductance stays at or above the divergence divided by the tolerance.
- Consequence: with no divergence, no bottleneck ends drift. With larger divergence, wider passages end it.
- Claim: the three regimes are fixed by this level and the lift test.
- Claim: the tolerance is the one free parameter. Paper 4 estimates it.
- Kernel: critical level, regime table.
- Depends on: Sections 4, 5, 6.

## 8. Change of the Map (1.25 pages)

- Claim: when the territory changes and the map does not, total divergence grows. This is transience in operator form.
- Claim: remap changes weights, the complex, or the compression.
- Observable: the rate of change of analytic torsion follows the change of the Laplacians at constant rank. It is signed.
- Claim: control work is the integrated squared control. It is nonnegative. Torsion is not control work.
- Form of control on the complex: [open].
- Kernel: update, torsion, control work.
- Depends on: Sections 5 and 7. Answers transience.

## 9. A Worked Case (1.75 pages)

- Setup: a four-vertex territory path compressed onto a three-vertex map, with two territory vertices sent to one map vertex.
- Step: the manufactured flow prefers the short route.
- Step: the short route has no lift from the agent's position. The long route has one.
- Step: the alternative set is not empty, so the regime is control.
- Step: lowering the weight of the false edge removes the divergence on the active part. Torsion falls.
- Finding: the harmonic part of a route does not tell supported from unsupported routes. The lift test does.
- Kernel: Worked case 3.1.
- Depends on: Sections 3 to 8.

## 10. What Is Fixed and What Is Open (1 page)

- Fixed: the inputs to allocation. Use, consequence, divergence, the regime.
- Open: the forms of the monitoring and recalibration functions. Expected divergence as a function of the rate of change. Control on the complex. The role of the higher Laplacian beyond the lift test.
- Hand-off: estimators and tests in Paper 4.
- Depends on: all sections.

## 11. Conclusion (0.25 page)

- One paragraph.

## Not in this paper

- The four propositions of the research note (partition, parochial charts, zero-work agents, perspective). Outside the series unless a later ruling requires one.
- Thresholds given as numbers. Neural correlates. Clinical cases. The determinant-line material.

## References to check

- Spectral graph theory. Effective resistance. Hodge Laplacians on graphs. Ray and Singer on torsion. Gromov-Wasserstein distance, credited to Mémoli. All through the fact-check pass.
