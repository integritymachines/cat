# LSMN Kernel

Version 0.15, 14 November 2026. Notation: `0_LSMN_notation.md`. Rulings and history: `0_LSMN_disposition.md`, `0_LSMN_review.md`.

To navigate an unsurveyable reality, a cognitive agent maintains, and mediates between, two models of it: a comprehensive territory and a comprehensible map. Consciousness arises out of that mediation and the need to allocate metabolic resources to keep the two aligned. Papers 1 and 2 state this with synecdoches. Papers 3 and 4 realize it in operators and tests.

## 1. Consciousness as Translation

$$\mathcal{L} \xrightarrow{\sigma} \mathcal{S} \xrightarrow{\pi} \mathcal{M} \xrightarrow{\gamma} \mathcal{N}, \qquad \pi \text{ non-injective}, \qquad U = I + N, \quad N = (O, C, T)$$

$$I \;\to\; \pi \;\to\; O + C + T \;\to\; \kappa \ge \kappa^\ast \;\to\; w \ne 0 \;\to\; \text{consciousness}$$

Stand-in (ill). $\mathcal{M}$ carries $g_F(y) = \mathbb{E}\big[\nabla \log p(\cdot \mid y)\, \nabla \log p(\cdot \mid y)^\top\big]$ and

$$\dot{y} = -g_F^{-1} \nabla \phi(y) + w(y)$$

$\kappa(y)$, the curvature of $g_F$, stands for the divergence of $\mathcal{M}$ from $\mathcal{S}$ together with its consequence for $\gamma$.

$$\operatorname{reg} = \begin{cases} \text{drift} & \kappa < \kappa^\ast, \quad w \approx 0 \\ \text{control} & \kappa \ge \kappa^\ast,\ \Gamma_B \ne \emptyset, \quad w \ne 0 \\ \text{remap} & \kappa \ge \kappa^\ast,\ \Gamma_B = \emptyset, \quad g_F \leftarrow g_F + \delta g \ \text{(hyp)} \end{cases}$$

$\Gamma_B$: acceptable supported routes to the goal, the current one included, found within budget $B$.

$$a(t) = a_{\mathrm{base}}(t) + \sum_e \Delta a_e(t), \quad \Delta a_e > 0 \iff \kappa_e \ge \kappa^\ast, \qquad \mathcal{W} = \int_\Theta \lVert w \rVert^2_{g_F}\, dt, \quad \eta = \frac{\mathcal{W}}{\int_\Theta \sum_e \Delta a_e\, dt}$$

Postulate. $\text{conscious}(t) \iff a(t) > 0$.

Consequences. $\neg I \Rightarrow a \equiv 0$: a perfectly rational agent needs zero models. Wake with $\vartheta > 0 \Rightarrow a \ge a_{\mathrm{base}} > 0$. Dreamless sleep, anesthesia $\Rightarrow a = 0$.

Experience (post). Effort $\lVert w \rVert^2_{g_F}$. Salience $\kappa$. Meaning $\kappa \approx \kappa^\ast$. Intensity $\lVert \nabla \kappa \rVert_{g_F}$.

## 2. Unsurveyability

$$I \iff \lim_{\alpha \to \infty} \frac{\log \nu(\mathcal{S}_\alpha)}{\dim \mathcal{M}} = \infty \;\Rightarrow\; x_{t+1} \in \operatorname{Nbr}(x_t)$$

| | Problem posed | Degree | Ordering | Primitive |
|---|---|---|---|---|
| $O$ | identification | $o = \tfrac12\big(1 - \operatorname{corr}(\nabla_{\mathrm{loc}} \operatorname{val}, \nabla_{\mathrm{glob}} \operatorname{val})\big)$ | none | $R$ |
| $C$ | composition | $c \in [0,1]$, cost of reversion | logical | $F$ |
| $T$ | persistence | $\vartheta \ge 0$, rate of change | temporal | $D$ |

$$\ell_C = \ell_C(o\, c), \qquad \ell_T = \ell_T(\vartheta, \lvert \gamma \rvert), \qquad \operatorname{err}_{i+1} \le \operatorname{amp}_i\, \operatorname{err}_i + \xi_i$$

$$j \to \gamma \to \operatorname{lift}(\gamma) \to \text{step} \to \text{update} \quad \text{under} \quad B = B_R + B_F + B_D + B_w + B_0, \qquad \text{stop at } \kappa^\ast$$

$$\pi^\ast = \arg\min_\pi d_{\mathcal{SM}} \ \text{ s.t. } \dim \mathcal{M} \le \text{capacity}, \qquad \operatorname{sig} = (R, F, D) \in \{0,1\}^3$$

## 3. Translation Geometry

$K_S = (V_S, \Lambda_S, \mu_S)$, $K_M = (V_M, E_M, G)$, $\pi: V_S \twoheadrightarrow V_M$.

$$\Delta_0 = \partial_1 G\, \partial_1^\top, \quad \Delta_1 = \tilde{\partial}_1^\top \tilde{\partial}_1 + \tilde{\partial}_2 \tilde{\partial}_2^\top, \qquad \Delta_0 \phi = \zeta, \quad j = -G\, \partial_1^\top \phi, \quad f_{v,e} = -(\partial_1)_{v,e}\, j_e$$

$$\lambda_\zeta = \frac{\lVert \zeta \rVert^2}{\zeta^\top \Delta_0^\dagger \zeta}, \qquad \lambda_2 = \min_{\zeta \perp \mathbf{1}} \lambda_\zeta, \qquad \lambda_\zeta^{-1} = \int_0^\infty \frac{\zeta^\top e^{-t \Delta_0} \zeta}{\lVert \zeta \rVert^2}\, dt \quad \text{(thm)}$$

$$\operatorname{lift}(\gamma \mid z_0) = \mathbf{1}_{z_0}^\top P_{m_0} \prod_{i \ge 1} \big(\Lambda_S P_{m_i}\big) \mathbf{1}, \qquad \Gamma_B \subseteq \Gamma_{\mathcal{S}} \subseteq \Gamma_{\mathcal{L}}$$

$$\text{trigger} \iff \operatorname{lift}(\gamma_j \mid z_0) = 0 \ \lor\ \lambda_\zeta \le \epsilon^\ast; \qquad \text{control} \iff \text{trigger} \land \Gamma_B \ne \emptyset; \qquad \text{remap} \iff \text{trigger} \land \Gamma_B = \emptyset$$

$$d_{\mathcal{SM}} = \sum_{z, z'} \mu_S(z) \mu_S(z') \big\lvert \operatorname{dist}_S(z, z') - \operatorname{dist}_M(\pi z, \pi z') \big\rvert^2, \qquad \frac{d}{dt} \log \operatorname{Tor} = \tfrac12 \sum_i (-1)^{i+1}\, i\, \operatorname{Tr}\big(\Delta_i^\dagger \dot{\Delta}_i\big)$$

Lemma (thm). $\operatorname{lift}(\gamma_j \mid z_0) = 0 \Rightarrow w \not\equiv 0 \lor \dot{G} \not\equiv 0$.

Perspective asymmetry. $d_{\mathrm{GW}}(\mathcal{M}_{\mathrm{int}}, \mathcal{M}_{\mathrm{ext}}) = 0$ iff isomorphic (thm). Distinct parochial samplings give $d_{\mathrm{GW}} > 0$ (post).

Correspondence, partial and lossy. $g_F \leftrightarrow D_{\mathrm{sym}}$. $\nabla \phi \leftrightarrow j$. $\kappa \ge \kappa^\ast \leftrightarrow$ trigger. $\delta g \leftrightarrow (\dot{G}, \Delta K_M, \Delta \pi)$.

Viability. $\mathbb{E}[\ell \text{ avoided}] > \mathbb{E}[B_F + B_w + B_0]$.

## 4. Measuring Consciousness

$$\hat{a} \uparrow a, \qquad \mathcal{W} \ge c_0\, \lvert \Delta_{\mathrm{ctrl}} \log \operatorname{Tor} \rvert \quad \text{(post)}$$

| Test (post) | Prediction |
|---|---|
| 4.3 | control policy and cost change at a calibrated threshold located by $\hat{\lambda}_\zeta$ |
| 4.4 | $\mathbb{E}[\text{response time}] = t_0 + c_1\, \lambda_\zeta^{-1}$ |
| 4.5 | $\Delta \operatorname{bnd}$ predicted by $[\operatorname{lift} = 0]$ and revision demand, $\Delta \log \operatorname{Tor}$ adds |
| 4.6 | $\int_\Theta \hat{a}\, dt \propto \eta^{-1} \hat{\mathcal{W}}$ |
| 4.7 | propofol, dreamless sleep: control channel unresponsive to $\lambda_\zeta$ |

Contrasts. Flow against overload: $\eta$. Propofol against ketamine: internal $\mathcal{W}$. Meditation against psychedelics: baseline against variance of $\lambda_\zeta$. Two agents coordinate under drift iff $d_{\mathrm{GW}}(\mathcal{M}_A, \mathcal{M}_B) < \delta^\ast$ (post).

Refutation. Each failure is recorded at its layer: operator, bridge, mechanism, or the postulate of §1.
