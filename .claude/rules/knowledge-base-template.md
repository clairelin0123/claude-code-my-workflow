---
paths:
  - "Paper/**/*.tex"
  - "explorations/**"
---

# Project Knowledge Base: ESG Survey Paper

<!-- Claude reads this before creating or modifying any paper content. -->

## Notation Registry

| Rule | Convention | Example | Anti-Pattern |
|------|-----------|---------|-------------|
| Firm index | $i$ for firm, $t$ for time, $j$ for sector | $\text{ESG}_{it}$ | Mixing $n$, $k$ for firm index |
| ESG pillars | $E_{it}$, $S_{it}$, $G_{it}$ for pillar scores | $G_{it}$ = governance score of firm $i$ at time $t$ | "ESG_G" or "Gov" |
| Aggregate ESG score | $\text{ESG}_{it}$ or $\text{ESG}_{it}^{p}$ (provider $p$) | $\text{ESG}_{it}^{\text{MSCI}}$ | "rating" without specifying provider |
| Cost of capital | $r_e$ for equity, $r_d$ for debt, $\text{WACC}$ | $r_{e,it}$ | "discount rate" unqualified |
| Returns | $R_{it}$ for raw, $\alpha_{it}$ for abnormal | $R_{it} - R_{ft}$ | mixing return definitions |
| Disclosure index | $D_{it} \in [0,1]$ | $D_{it} = 1$ if firm discloses, 0 otherwise | "disclosure quality" without operationalizing |
| Citations | `\textcite{key}` inline, `\citep{key}` parenthetical | \textcite{Friedman1970_social} argues... | Hard-coded author names without cite command |

## Symbol Reference

| Symbol | Meaning | First Used |
|--------|---------|------------|
| $\text{ESG}_{it}$ | Aggregate ESG score, firm $i$, time $t$ | Section 2 (Theory) |
| $E_{it}$, $S_{it}$, $G_{it}$ | Environmental, Social, Governance pillar scores | Section 2 |
| $r_{e,it}$ | Cost of equity capital | Section 8 (Valuation) |
| $D_{it}$ | ESG disclosure indicator or index | Section 6 (Disclosure) |
| $\text{CF}_{it}$ | Cash flows | Section 8 |
| $\beta^{\text{ESG}}$ | ESG factor loading in asset pricing model | Section 8 |
| $\lambda^{\text{ESG}}$ | ESG factor risk premium | Section 8 |
| $\text{CAR}_{it}$ | Cumulative abnormal return around event | Various |
| $p$ | Provider superscript for ESG rating source | Section 2, 6 |

## Paper Section Progression

| # | Section | Core Question | Key Concepts | Key Papers to Cover |
|---|---------|--------------|-------------|---------------------|
| 1 | Introduction | Why ESG? Why now? What does this survey cover? | ESG definition, scope, materiality | Broad motivation |
| 2 | Theoretical ESG Models | How does theory explain ESG adoption and effects? | Shareholder vs. stakeholder, agency, signaling, preferences | Friedman (1970), Freeman (1984), theoretical models |
| 3 | Climate Risk & Insurance | How do climate risks affect firms and insurers? | Physical risk, transition risk, stranded assets, insurance | NGFS scenarios, insurance solvency studies |
| 4 | Regulation & Policy | What are the effects of ESG mandates and carbon policy? | Mandatory disclosure, carbon tax, SEC rules, EU taxonomy | Policy evaluation studies, SFDR, CSRD |
| 5 | ESG Effects on Investment, Consumption & Employment | How does ESG affect real economic decisions? | Capital allocation, consumer preferences, labor markets, supply chains | Portfolio constraints, consumer ESG demand |
| 6 | ESG Disclosure & Assurance | What drives disclosure? Does assurance add value? | Voluntary vs. mandatory, greenwashing, auditor verification | GRI, TCFD, ISSB standards |
| 7 | Asset Management Industry | How does ESG change investment management? | ESG funds, screening, stewardship, engagement, index inclusion | Fund flows, engagement effects, index ESG |
| 8 | Firm Valuation, Cost of Capital & Asset Pricing | Does ESG affect firm value and returns? | ESG premium/discount, cost of equity, factor models | ESG-performance studies, sin stocks |
| 9 | Future Research Directions | What are the most important open questions? | Data gaps, identification challenges, emerging areas | Literature gaps synthesis |
| 10 | Conclusion | What have we learned? | Summary of consensus and debate | — |

## Key Frameworks and Theories

| Framework | Origin | Role in Survey | Section |
|-----------|--------|----------------|---------|
| Shareholder primacy | Friedman (1970) | Baseline benchmark for ESG debates | 2 |
| Stakeholder theory | Freeman (1984) | Theoretical foundation for ESG value | 2 |
| Agency theory | Jensen & Meckling (1976) | Managerial discretion in ESG investment | 2 |
| Signaling theory | Spence (1973) | Voluntary ESG disclosure as signal | 2, 6 |
| Attention-based ESG preferences | Fama & French style | Investor taste for ESG assets, pricing | 8 |
| SASB materiality framework | SASB | Sector-specific ESG materiality | 2, 6 |
| TCFD framework | FSB (2017) | Climate-related financial disclosure standard | 3, 6 |
| EU Taxonomy | EU (2020) | Green/sustainable finance classification | 4 |

## Anti-Patterns (Don't Do This)

| Anti-Pattern | Problem | Correct Approach |
|-------------|---------|-----------------|
| Conflating ESG ratings across providers | MSCI, Sustainalytics, Bloomberg ratings have ~0.5 correlation — they measure different things | Always specify the rating provider; note cross-provider disagreement |
| "ESG improves financial performance" without qualification | The effect is heterogeneous by sector, time period, and ESG pillar | Report effect sizes, conditions, and contradictory findings |
| Treating voluntary disclosure as exogenous | Firms self-select into disclosure; selection bias is severe | Note endogeneity; flag papers that address it |
| Conflating ESG disclosure quality with ESG performance | A firm can disclose a lot while performing poorly (greenwashing) | Distinguish disclosure quantity/quality from actual environmental/social outcomes |
| Calling all ESG-related fund flows "responsible investing" | ESG funds, impact funds, and SRI funds have different mandates | Use precise terminology: ESG integration, exclusionary screening, impact investing |
| Treating ESG as a single construct | E, S, G pillars are weakly correlated; aggregate scores obscure heterogeneity | Report pillar-level results where available |
| Ignoring survivorship bias | Samples that exclude delisted firms overstate ESG-performance correlations | Flag whether dataset has survivorship bias |

## ESG Data Sources Reference

| Source | Coverage | Strengths | Known Limitations |
|--------|----------|-----------|------------------|
| MSCI ESG Ratings | Global, 8,500+ firms | Long history, widely used in academia | Methodology changes retroactively; low correlation with peers |
| Sustainalytics | Global, 10,000+ firms | Risk-oriented framework | Different from MSCI; mergers changed coverage |
| Bloomberg ESG Scores | Global | Disclosure-focused | Heavily driven by disclosure quantity |
| Refinitiv (ASSET4) | Global, 9,000+ firms | Long panel | High correlation with firm size |
| CDP Scores | Climate-focused | Actual emissions data | Voluntary participation; firm selection bias |
| ISS Governance | Corporate governance | Detailed governance data | Narrow focus (G only) |
| MSCI Climate VaR | Climate risk | Forward-looking scenarios | Model-dependent estimates |
