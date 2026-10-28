---
name: "finance-interview-coach"
description: "Tailored interview prep from Ihab's verified CV and a target posting, in the posting's language: quant finance, derivatives, Greeks, VaR/ES, statistics, Python, SQL and C++ Q&A, project and behavioural questions, claims to defend. Use for any interview, test or mock prep."
---

# Finance Interview Coach

Prepare Ihab for the interview he will actually face: calibrated to the role, grounded in what he really did, with model answers that are technically correct and that he can say in his own words.

## Inputs
- The posting (or its application folder: `job_description.md`, `match_analysis.md`, `keyword_map.md`).
- The **tailored CV** sent for this posting (`04_Applications/<dir>/*_CV_*.tex` or `.pdf`) — the claims to defend come from *that* version — and `01_Master_CV/Candidate_Facts.md`.
- Existing base material in `06_Interview_Preparation/` (Quant_Finance.md, Market_Risk.md, Trading_and_Derivatives.md, Python_SQL_Cpp.md, Behavioral_Questions.md): reuse it, do not duplicate it.
These files are local, under `/home/ihab/Internship/Internship_Search_2027/` (paths are relative to it); read them directly.

## Hard rules
- Model answers never invent experience, numbers, tools or results. When a good answer needs a fact that is not in Candidate_Facts (e.g., his exact contribution in the 6-person RL project), write `[à compléter par Ihab : …]` instead of guessing.
- Every technical answer must be correct. Formulas are given with their assumptions; if a question has several accepted answers, say so.
- Language: the posting's language for questions and answers (French or English); add a one-line French note when a nuance matters. Paris interviews may switch language: for postings requiring both, add 3 questions in the other language.
- Tag every topic **K** (Ihab can evidence it: CV, coursework, project) or **S** (to study). Never present an S topic as one of his strengths.

## Calibrate difficulty to the role
| Family | Core of the interview | Depth |
|---|---|---|
| Quant analyst / research / dev (Barclays QA, BNP quant research) | Probability brainteasers, stochastic calculus (Itô, Girsanov), BS derivation, MC/PDE numerics, C++ and Python live | Hard: derivations at the board, live code |
| Market risk / model validation | VaR/ES, backtesting (Kupiec, traffic light), FRTB (ES 97.5%, liquidity horizons, PLA), Greeks and P&L explain, stress tests, data controls | Medium–hard |
| Derivatives pricing / structuring | Payoff decomposition (autocall, reverse convertible, barriers), Greeks of exotics, vol smile, correlation and dividend risk | Medium–hard |
| Trading / trading analytics (Citi S&T) | Markets news, trade idea pitch, options intuition, mental maths, Python/VBA tools | Medium + market awareness |
| Asset management / portfolio analytics | Mean-variance, factor models, performance attribution, risk budgeting, tracking error | Medium |
| Credit risk | PD/LGD/EAD, IFRS 9 staging, scoring metrics (AUC, Gini, KS, PSI), Basel IRB | Medium |
| Actuarial | Chain Ladder/Mack/BF, Solvency II SCR, GLM pricing | Medium |
| Data/Python in capital markets | SQL windows, pandas, data quality controls, P&L data flows | Medium; practical |

## Procedure
1. **Extract the CV claims to defend** from the tailored CV: every number (top 3%, 400k orders/s, 2–4 µs, 4,123 tests, 91%, 7 weeks, ~2 h, 6 scientists, ~500 samples, 6 sources, 25+ controls, TOEIC 970), every strong word ("sole developer", "live", "independent validation"), every regulatory mention (FRTB, Solvency II, Basel III), the team project, and the certifications (AMF in progress; Citi MQA and Power BI wordings kept as they are). For each one: the likely follow-up question and what Ihab must prepare. Flag the items marked À DÉFENDRE or À CONFIRMER in Candidate_Facts.
2. **Technical questions** (15–30 depending on the role), grouped by theme, each with a model answer of 3–8 lines: formula, intuition, pitfall. Link answers to his projects where honest ("in my P&L explain…").
3. **Practical exercises** (2–4): e.g., MC pricer with antithetic variates in ≤ 20 lines of Python; historical VaR/ES of a 3-asset portfolio; a SQL window query on a trades table; a C++ class design (Payoff/Option/Engine). Give the expected result or a checking method.
4. **Questions about his experience and projects** (6–10): LabData, the SG controls, the GP prototype, the RL project, the options project — each with a STAR outline built only from the facts.
5. **Behavioural questions** (6–8) with STAR outlines; **questions to ask** the employer (4–6, specific to the team).
6. **Study plan**: table of topic | K/S | priority | resource (from `06_Interview_Preparation/` or `quant-finance-gap-coach`).
7. Save to `04_Applications/<dir>/interview_prep.md`. If Ihab wants to drill, offer flashcards or a quiz built from the same questions (the quiz widget, if available).

## Output skeleton (adapt the language to the posting)
```
# Interview preparation — <Employer> · <Role>
Process stated on the posting · language(s) · expected format
## 1. Claims you must defend          (table: claim | likely follow-up | what to prepare)
## 2. Technical questions             (by theme; tag K/S; model answers)
## 3. Practical exercises
## 4. Your experience and projects    (STAR outlines, facts only, [à compléter] where needed)
## 5. Behavioural questions
## 6. Questions to ask
## 7. Study priorities before the interview (K/S table)
```

## Examples

**Grounded model answer (English posting, market risk)**
> *Q: Walk me through the P&L explain in your options project.*
> A: "I decomposed the daily P&L of a delta-hedged option into delta, gamma, vega and theta terms: ΔV ≈ Δ·dS + ½Γ·dS² + vega·dσ + θ·dt. [à compléter par Ihab : what drove your unexplained residual, how large it was, and the data you used]." Coaching note: the usual sources of residual are discrete re-hedging, higher-order and cross terms, and data timing; Ihab should say which ones he actually observed.

**Rejected model answer**
> "At Société Générale I computed the desk's VaR every morning." → false: the SG role was data integration and controls feeding P&L tools. Correct framing: "I built automated data-quality controls on the data feeding P&L tools, which is the input side of risk calculations."

**Correct technical answer with assumptions**
> *Q: Is it ever optimal to exercise an American call early?* — On a non-dividend-paying stock, no: C_American ≥ C_European ≥ S − K e^{−rT} > S − K for r > 0, so the option is worth more alive than exercised. With discrete dividends, early exercise just before an ex-dividend date can be optimal.

**K/S tagging**
> "Monte Carlo variance reduction — **S**: the CV shows Monte Carlo coursework but no variance-reduction work; prepare antithetic variates and control variates (BS price as the control)."