# Workflow Quick Reference

**Model:** Contractor (you direct, Claude orchestrates)

---

## The Loop

```
Your instruction
    ↓
[PLAN] (if multi-file or unclear) → Show plan → Your approval
    ↓
[EXECUTE] Implement, verify, done
    ↓
[REPORT] Summary + what's ready
    ↓
Repeat
```

---

## I Ask You When

- **Design forks:** "Option A (fast) vs. Option B (robust). Which?"
- **Code ambiguity:** "Spec unclear on X. Assume Y?"
- **Replication edge case:** "Just missed tolerance. Investigate?"
- **Scope question:** "Also refactor Y while here, or focus on X?"

---

## I Just Execute When

- Code fix is obvious (bug, pattern application)
- Verification (tolerance checks, tests, compilation)
- Documentation (logs, commits)
- Plotting (per established standards)
- Deployment (after you approve, I ship automatically)

---

## Quality Gates (No Exceptions)

| Score | Action |
|-------|--------|
| >= 80 | Ready to commit |
| < 80  | Fix blocking issues |

---

## Non-Negotiables

- **Path convention:** Relative paths from `Paper/` directory (e.g., `\bibliography{../Bibliography_base}`, `\includegraphics{../Figures/fig1}`)
- **Figure standards:** Publication-ready — white background, 300 DPI minimum, greyscale-compatible, descriptive captions with units
- **Color palette:** Conservative academic — blue/grey for diagrams; avoid red/green (conflates ESG sentiment with good/bad)
- **Tolerance thresholds:** N/A (pure literature survey; no numerical replication targets)
- **Citation keys:** `AuthorYear_keyword` format (e.g., `Friedman1970_social`, `Berg2022_disagreement`)

---

## Preferences

**Visual:** Publication-ready figures with descriptive captions; summary tables in `booktabs` style
**Reporting:** Concise academic prose; use tables to summarize literature when 5+ papers cover a topic
**Session logs:** Always (post-plan, incremental, end-of-session)
**Literature:** Flag when characterizing a paper's finding — always quote the specific result, not a paraphrase

---

## Exploration Mode

For experimental work, use the **Fast-Track** workflow:
- Work in `explorations/` folder
- 60/100 quality threshold (vs. 80/100 for production)
- No plan needed — just a research value check (2 min)
- See `.claude/rules/exploration-fast-track.md`

---

## Next Step

You provide task → I plan (if needed) → Your approval → Execute → Done.
