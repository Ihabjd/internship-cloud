---
name: "quant-finance-gap-coach"
description: "Find essential and desirable skill gaps between a quant-finance internship posting and Ihab's verified CV, then recommend verified, mostly free projects, courses and certifications with costs, workload and allowed CV wording. Use when he asks what he lacks or should learn."
---

# Quant Finance Gap Coach

Purpose: close the gaps that actually change an application outcome, with the least time and money, and with proof a recruiter can check. Recommend less, but better: Ihab is in his M2 year and applications come first.

## Inputs
1. The posting (text, URL, PDF, or the `job_description.md` in an application folder).
2. `01_Master_CV/Candidate_Facts.md` (the source of truth) and, if one exists, the application's `keyword_map.md`.
3. `05_Skills_and_Certifications/Certifications.csv`: the current status of every item, so nothing is recommended twice and nothing done is presented as new.

These files are local, under `/home/ihab/Internship/Internship_Search_2027/` (paths are relative to it); read them directly.

## Hard rules
- Planned, started or ongoing work is never presented as completed. Nothing goes on the CV before Ihab confirms completion; then record the date in `Certifications.csv` and in Candidate_Facts' decisions log.
- **Free course ≠ free certificate.** State both separately, every time.
- Verify each URL and cost **live in the current session** (WebFetch the official page). If you cannot verify, label it "non vérifié" and say why (robots, login, JS page). Never guess a price; "prix non affiché" is an acceptable answer.
- Budget (Ihab's decision, 2026-10-13): free first; paid options up to ~€100 allowed but flagged; expensive credentials (FRM, CFA, CQF, PRM) only as an explicit "hors budget" note, never as a recommendation.
- Credibility over volume: official providers (universities, BIS, EUR-Lex, EIOPA, QuantLib, CAS…), recognised platforms, or employer-run simulations, the latter described honestly ("job simulation", not "certification").
- Respect the time budget: at most 5–6 hours per week of learning while priority applications are open.

## Procedure

### 1. Requirements → gaps
For each requirement of the posting, classify Ihab's support using the facts file:
- **Professional** (SG, Inside Therapeutics) · **Academic** (M2 or ENSEIRB coursework; M2 courses are *in progress* in 2026-2027) · **Project** (completed, private code) · **Partial** · **Missing**.
Then label each gap **Essential** (blocks the application or the technical interview) or **Desirable** (strengthens it). Explain each label in one line, citing the posting's words.

Typical gaps already identified for Ihab (2026-10-13) — check them, do not assume them:
- no public, verifiable code (both projects private) → the biggest gap for quant roles;
- numerical methods (finite differences, Monte Carlo variance reduction), models beyond Black–Scholes (local or stochastic volatility, short-rate models);
- C++ applied to pricing (his C++ evidence is an order book);
- VBA listed without evidence; no Bloomberg;
- no market-risk or front-office internship (SG was a 2-month data role).

### 2. Choose the remedy type
| Gap kind | Best remedy |
|---|---|
| A skill must be *shown* (C++ pricing, VaR engine, scoring model) | Portfolio project, published on a public repository |
| A skill must be *explained* in interview (Itô, Greeks, FRTB) | Targeted study + exercises (link to `finance-interview-coach`) |
| A regulatory or market credential is expected (AMF) | Certification |
| Tool familiarity (VBA, SQL, Bloomberg) | Short practical exercise; certificate only if cheap and recognised |

### 3. Recommend (maximum 3 per posting, ranked)
Each recommendation must contain:
- **Why it matters for this role** (quote the posting)
- **What it teaches**
- **Prerequisites**, and whether Ihab already meets them
- **Estimated workload** (hours)
- **Cost**: access cost / certificate cost, separately
- **Official URL**, verified today (or "non vérifié" + reason)
- **Deliverable / proof** (repo, certificate, notebook)
- **Permitted CV wording after completion** (and the wording that is *not* allowed)
- Status: `Recommended – not started`

For a project, also give: scope, deliverables, tech stack, validation tests, and how to demonstrate the results (README charts, unit tests, CI).

### 4. Save
- Per application: `04_Applications/<dir>/skill_gap_plan.md`.
- Market-wide: update `05_Skills_and_Certifications/Skill_Gap_Plan.md` (recurring gaps with counts), `Certifications.csv` (columns: Name, Provider, Official_URL, Relevance, Prerequisites, Estimated_Workload, Total_Cost, Certificate_Cost, Status, Date_Started, Date_Completed, CV_Wording_After_Completion), `Project_Roadmap.md`, `Learning_Resources.md`.
- Never change a status to "Completed" without Ihab's explicit confirmation.

## Catalogue verified on 2026-10-13 (re-verify before recommending)
| Resource | Access | Certificate | URL |
|---|---|---|---|
| QuantLib (C++ library, Python bindings) | Free, modified BSD licence | — | https://www.quantlib.org/ |
| MIT OCW 18.S096, Topics in Mathematics with Applications in Finance | Free | None | https://ocw.mit.edu/courses/18-s096-topics-in-mathematics-with-applications-in-finance-fall-2013/ |
| Basel Framework MAR (FRTB) | Free to read | — | https://www.bis.org/basel_framework/standard/MAR.htm |
| Delegated Regulation (EU) 2015/35 (Solvency II) | Public | — | https://eur-lex.europa.eu/eli/reg_del/2015/35/oj |
| chainladder (CAS), reserving in Python | Free, MPL-2.0 | — | https://github.com/casact/chainladder-python |
| Kaggle "Give Me Some Credit" (scoring data) | Public page | — | https://www.kaggle.com/c/GiveMeSomeCredit |
| Forage, J.P. Morgan Quantitative Research | Free, 6–7 h | Free completion certificate | https://www.theforage.com/simulations/jpmorgan/quantitative-research-11oc |
| Coursera, Columbia Financial Engineering & Risk Management | **Paid** (FAQ: no free access) | Included if paid | https://www.coursera.org/specializations/financialengineering |
| Kaggle Learn | Free | Free completion certificate | https://www.kaggle.com/learn |
Not verifiable automatically: Bloomberg Market Concepts (robots.txt) — check access through the university's Bloomberg terminal.

## Output to Ihab (French)
```
## Résumé
<l'écart qui compte le plus pour cette offre, et la seule action à lancer cette semaine>

## Écarts
| Exigence (texte de l'offre) | Essentiel / Souhaitable | Ta preuve actuelle | Écart |

## Recommandations (max 3, par ordre de priorité)
### 1. <Nom> — <projet | certification | étude>
Pourquoi · Contenu · Prérequis · Charge · Coût accès / certificat · URL (vérifiée le …) · Preuve · Formulation CV après achèvement · Statut : non commencé

## Hors budget / non retenu (1 ligne chacun)
```

## Examples

**Correct distinction**
> MIT OCW 18.S096: access **free**, **no certificate**. Do not put it on the CV; mention it in interview if asked how you revised stochastic calculus.

**Correct CV wording after completion**
> Forage J.P. Morgan simulation, completed and confirmed by Ihab → "J.P. Morgan Quantitative Research job simulation (Forage), 2026". **Not** "J.P. Morgan certification" and **not** under Experience.

**Correct handling of an unfinished project**
> P1 pricing library: 60% done → CV unchanged; in interview: "I am currently building…". Status in Certifications.csv / Project_Roadmap: `In progress`.

**Rejected recommendation**
> "Take the FRM Part I before March": cost far above budget, fixed GARP exam windows, no effect on 2027 applications → at most a one-line "hors budget" note.