# CLAUDE.MD -- Academic Project Development with Claude Code

<!-- HOW TO USE: Replace [BRACKETED PLACEHOLDERS] with your project info.
     Customize Beamer environments and CSS classes for your theme.
     Keep this file under ~150 lines — Claude loads it every session.
     See the guide at docs/workflow-guide.html for full documentation. -->

**Project:** ESG Survey: A Comprehensive Review of Environmental, Social, and Governance Literature
**Institution:** DePauw University
**Branch:** main
**Primary Artifact:** `Paper/esg_survey.tex` (LaTeX article manuscript)

---

## Core Principles

- **Plan first** -- enter plan mode before non-trivial tasks; save plans to `quality_reports/plans/`
- **Verify after** -- compile/render and confirm output at the end of every task
- **Single source of truth** -- Beamer `.tex` is authoritative; Quarto `.qmd` derives from it
- **Quality gates** -- nothing ships below 80/100
- **[LEARN] tags** -- when corrected, save `[LEARN:category] wrong → right` to MEMORY.md

---

## Folder Structure

```
my-project/
├── CLAUDE.md                    # This file
├── .claude/                     # Rules, skills, agents, hooks
├── Bibliography_base.bib        # Centralized bibliography (all ESG references)
├── Paper/                       # LaTeX article manuscript (primary)
│   ├── esg_survey.tex           # Main paper file
│   └── sections/                # Section stub files (input'd from main)
├── Figures/                     # Figures, tables, and images
├── quality_reports/             # Plans, session logs, merge reports
├── explorations/                # Research sandbox (see rules)
├── templates/                   # Session log, quality report templates
└── master_supporting_docs/      # Supporting papers and slides
```

---

## Commands

```bash
# LaTeX article (4-pass: pdflatex + bibtex + 2x pdflatex)
cd Paper && pdflatex -interaction=nonstopmode esg_survey.tex
bibtex esg_survey
pdflatex -interaction=nonstopmode esg_survey.tex
pdflatex -interaction=nonstopmode esg_survey.tex

# Quick compile (single pass, no bib — for drafting)
cd Paper && pdflatex -interaction=nonstopmode esg_survey.tex

# Quality score
python scripts/quality_score.py Paper/esg_survey.tex
```

---

## Quality Thresholds

| Score | Gate | Meaning |
|-------|------|---------|
| 80 | Commit | Good enough to save |
| 90 | PR | Ready for deployment |
| 95 | Excellence | Aspirational |

---

## Skills Quick Reference

| Command | What It Does |
|---------|-------------|
| `/compile-latex [file]` | 3-pass XeLaTeX + bibtex |
| `/deploy [LectureN]` | Render Quarto + sync to docs/ |
| `/extract-tikz [LectureN]` | TikZ → PDF → SVG |
| `/proofread [file]` | Grammar/typo/overflow review |
| `/visual-audit [file]` | Slide layout audit |
| `/pedagogy-review [file]` | Narrative, notation, pacing review |
| `/review-r [file]` | R code quality review |
| `/qa-quarto [LectureN]` | Adversarial Quarto vs Beamer QA |
| `/slide-excellence [file]` | Combined multi-agent review |
| `/translate-to-quarto [file]` | Beamer → Quarto translation |
| `/validate-bib` | Cross-reference citations |
| `/devils-advocate` | Challenge slide design |
| `/create-lecture` | Full lecture creation |
| `/commit [msg]` | Stage, commit, PR, merge |
| `/lit-review [topic]` | Literature search + synthesis |
| `/research-ideation [topic]` | Research questions + strategies |
| `/interview-me [topic]` | Interactive research interview |
| `/review-paper [file]` | Manuscript review |
| `/data-analysis [dataset]` | End-to-end R analysis |

---

## LaTeX Paper Conventions

| Element           | Convention    | Use Case       |
|-------------------|---------------|----------------|
| `\textcite{key}`  | Inline author-year citation | "Smith (2020) find that..." |
| `\citep{key}`     | Parenthetical citation | "...(Smith, 2020)" |
| `\begin{table}[h!]` | Float placement | All tables use `h!` for proximity |
| `\begin{figure}[h!]` | Float placement | All figures use `h!` for proximity |
| Section labels    | `sec:theory`, `sec:climate`, etc. | Cross-referencing |

---

## Current Paper State

| Section | File | Status | Key Content |
|---------|------|--------|-------------|
| 1: Introduction | `sections/intro.tex` | Stub | Motivation, scope, road map |
| 2: Theoretical ESG Models | `sections/theory.tex` | Stub | Shareholder vs. stakeholder, agency, signaling |
| 3: Climate Risk & Insurance | `sections/climate.tex` | Stub | Physical/transition risk, insurance markets |
| 4: Regulation & Policy | `sections/regulation.tex` | Stub | Mandatory disclosure, carbon pricing, SEC rules |
| 5: ESG Effects on Investment, Consumption & Employment | `sections/investment.tex` | Stub | Capital allocation, consumer behavior, labor |
| 6: ESG Disclosure & Assurance | `sections/disclosure.tex` | Stub | Voluntary vs. mandatory, greenwashing |
| 7: Asset Management Industry | `sections/asset_mgmt.tex` | Stub | ESG funds, index inclusion, stewardship |
| 8: Firm Valuation, Cost of Capital & Asset Pricing | `sections/valuation.tex` | Stub | ESG premia, cost of equity, factor models |
| 9: Future Research Directions | `sections/future.tex` | Stub | Open questions, recommended agenda |
| 10: Conclusion | `sections/conclusion.tex` | Stub | Summary and synthesis |
