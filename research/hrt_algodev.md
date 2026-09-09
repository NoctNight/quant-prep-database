# HRT — Algorithm Developer (Quant Researcher) track: interview research

Research date: 2026-09-09. Target role: **Algorithm Developer / "Algo Dev" / "Algorithm Developer (Quant Researcher)"**. Explicitly *not* Software Engineer, Algo Engineer, Core Developer, or Systems/SRE.

## 0. Sourcing discipline and access constraints — READ FIRST

**Evidence labels used throughout:**

| Label | Meaning |
|---|---|
| **OFFICIAL** | HRT's own words (job posting / HRT Beat blog) |
| **FIRST-HAND** | A traceable individual candidate account with a URL |
| **TRANSCRIBED** | A GitHub repo or aggregator preserving/pointing at the original source URL |
| **PREP-SITE** | Unattributed assertion on a commercial prep/SEO site. **Not fact.** |

**Network blocking in this sandbox was severe.** Blocked at the proxy: `glassdoor.com`, `reddit.com`, `teamblind.com`, `leetcode.com`, `1point3acres.com`, `jointaro.com`, `wallstreetoasis.com`, `prachub.com`, `hudsonrivertrading.com`, `news.ycombinator.com`, `medium.com`, `web.archive.org`, `archive.org`, `boards-api.greenhouse.io`, `builtinnyc.com`, `ocs.yale.edu`, `simplify.jobs`, `themuse.com`, `nodeflair.com`, `oavoservice.com`, `quantblueprint.com`, `techinterview.org`, `1o24bbs.com`, `thefreshdev.com`, `oneraynyday.github.io`.

**What that means for confidence.** I could open **at source** only: `raw.githubusercontent.com`. Everything else in this document that is labelled FIRST-HAND or OFFICIAL reached me as a **search-engine summary of a page I could not open myself**. Search summaries can compress, paraphrase, or conflate. Where a claim rests only on a summary of a page I could not open, I say so inline with *(summary-only)*. Two GitHub files I read in full and can vouch for verbatim.

**A specific warning about this topic area.** Nearly every top-ranked English-language result for "HRT algo dev interview" is a commercial prep/SEO page: `tradermath.org`, `quantt.co.uk`, `spacecomplexity.ai`, `myntbit.com`, `datainterview.com`, `dataloopr.com`, `linkjob.ai`, `hacktherounds.com`, `oavoservice.com`, `quantblueprint.com`, `techprep.app`, `interviewprep.org`, `companyinterviews.com`, `yourcareersupport.com`, `everythingquant.com`, `thewallstreetquants.com`. These pages contain confident, specific, **unattributed** claims and they contradict each other on basics (OA length: 90 vs 120 vs 130 vs 150 minutes; onsite rounds: 4 vs 5 vs 6). Independent corroboration that they invent: the GitHub question bank `pushpa-kumar/placement-prep` (read in full, below) explicitly re-labels Quantt and Tradermath HRT items as **`Status: PRACTICE`**, noting Tradermath's Romeo-and-Juliet problem is *"explicitly labeled 'a representative HRT problem', not a confirmed real report"* and Quantt's items are *"generic prep example, no candidate attribution."* **Treat every PREP-SITE claim below as unverified.**

**One outright fabricated source found.** `github.com/sumitsingh4411/interview-rounds` (`content/companies/hudson-river-trading.md`) lists five HRT "interview experiences" for roles **"Mid · Full-stack", "Junior · Backend", "Staff · Frontend", "Junior · Frontend"**. HRT does not hire frontend/full-stack quant staff in these shapes; this repo is machine-generated filler. **Discard it.** I flag it because it will surface in future GitHub searches for this firm.

---

## 1. Two sources I read in full at source (highest confidence in *what they say*)

### 1a. `Lazar-Ilic/Lazar` — `Notes/Computer Science/Algorithms/Interviews Coding Rounds/Hudson River Trading.txt`
- URL: https://github.com/Lazar-Ilic/Lazar/blob/main/Notes/Computer%20Science/Algorithms/Interviews%20Coding%20Rounds/Hudson%20River%20Trading.txt
- Raw (fetched, 34 KB): https://raw.githubusercontent.com/Lazar-Ilic/Lazar/main/Notes/Computer%20Science/Algorithms/Interviews%20Coding%20Rounds/Hudson%20River%20Trading.txt
- **Label: TRANSCRIBED.** This is one candidate's personal prep dossier. He states he is scraping *"their August 2022 recruiting cycle past that date which are in fact live in public on GlassDoor"* and *"According to AlgoDaily"*. So the **questions** are transcribed Glassdoor/AlgoDaily items; the **commentary** interleaved with them is his own opinion, not an interviewer's. Do not read his commentary as HRT's position.

### 1b. `pushpa-kumar/placement-prep` — `raw-notes/company-hrt-citadel.md`
- URL: https://github.com/pushpa-kumar/placement-prep/blob/main/raw-notes/company-hrt-citadel.md
- Raw (fetched, 55 KB): https://raw.githubusercontent.com/pushpa-kumar/placement-prep/main/raw-notes/company-hrt-citadel.md
- **Label: TRANSCRIBED, and unusually disciplined.** Compiled 2026-08-27. Every entry carries `Company / Role / Type / Round/Stage / Status: REAL|PRACTICE / Source: <URL>`. It preserves LeetCode Discuss permalinks and separates real reports from prep-site inventions. **This is the best-sourced artifact I found on HRT anywhere.** Caveat: its HRT coverage is overwhelmingly **SWE/Algo-Engineer OA**, not Algo Dev; only a handful of Algo-Dev-adjacent items appear.

---

## 2. The Algo Dev pipeline, end to end

### 2.1 Summary of the best-supported shape

```
Resume screen
   ↓
Online Assessment (coding, CodeSignal/HackerRank/Codility)
   ↓
Phone round 1  — probability & statistics (~45 min)
   ↓
Phone round 2  — algorithms / live coding / statistics
   ↓
Onsite / VO    — 4–5 one-hour 1:1 rounds, split morning/afternoon with lunch
```

### 2.2 The online assessment

**The strongest-supported figure for Algo Dev is 3 coding questions in 150 minutes.** Multiple distinct 1point3acres Algo-Dev threads converge on it *(summary-only, could not open source)*:
- https://www.1point3acres.com/bbs/thread-1025739-1-1.html — "hrt algo dev 第一轮概率统计面经"
- https://www.1point3acres.com/bbs/thread-1112867-1-1.html — "HRT Algo Dev OA"
- https://www.1point3acres.com/bbs/thread-1026334-1-1.html — "[HRT] Algo Dev OA"
- https://www.1point3acres.com/bbs/thread-1022110-1-1.html, /thread-1100539-1-1.html, /thread-1101053-1-1.html

Reported content of a 150-min/3-question Algo Dev OA: **(1) "fancy number" / "pretty number"** — numbers whose base-4 representation uses only digits 0 and 1, count how many are < n (a digit-DP); **(2) implement Reversi/Othello** given a move list, return each player's piece count; **(3) merge two trees / pre-order tree problem** *(summary-only)*.

**On "all hidden tests must pass": I could not verify this as an HRT-stated rule.** What I can support:
- One Glassdoor-sourced candidate quote transcribed in `Lazar-Ilic/Lazar` reports the requirement as *"ALL test cases within the limits"* for a **2-hour, 3-question** assessment — but that quote is attributed there to the **algo engineer** track, with a separate "General Coding Assessment" for the software engineer track. **TRANSCRIBED.**
- The same file transcribes a candidate saying they passed the SWE assessment with 20+ minutes remaining and were still rejected: *"very happy to send out OA to applicants, but passing the OA is a mystery."* **TRANSCRIBED.**
- **Conclusion:** the "2 hours / 3 questions / all hidden tests" description is real but is best-attributed to the **algo engineer** track. For **Algo Dev** the recurring number is **150 minutes / 3 questions**. Both figures circulate; do not assume the 2-hour variant.

**Counts of 4 questions also appear** for Algo Dev: one Glassdoor Algorithm-Developer-Intern report describes *"an online assessment with 4 questions including one involving Pandas"* *(summary-only)*, and `Lazar-Ilic/Lazar` transcribes both "4 Easy/Medium In 70 Minutes" and two separate "4 Questions 90 Minutes" entries. **The OA is not standardised across seasons.** Plan for 3–4 questions and 90–150 minutes.

**A pandas question can appear in the OA itself** (not only onsite) — see §5.

**Does the Algo Dev OA differ from SWE?** Only PREP-SITE sources claim a separate probability/statistics OA for the research track (`hacktherounds.com`, `quantt.co.uk`: *"for quant researcher candidates, there is a probability and statistics test of similar length"*). **No first-hand account supports a stats-only OA for Algo Dev.** Every Algo Dev first-hand thread I found describes a **coding** OA. Treat the "stats OA" claim as PREP-SITE invention.

### 2.3 Phone rounds

**Two phone screens before onsite is the standard reported shape.** Round 1 = math/probability; round 2 = algorithms, sometimes with live coding.
- Blind: *"The first phone typically includes a CV walk-through followed by basic maths and stats brain teasers, while the second phone focuses mostly on algorithm questions (without actual coding)."* — https://www.teamblind.com/post/hudson-river-trading-hrt-algo-developer-phone-interview-what-to-expect-1nz00wah *(summary-only, FIRST-HAND in origin)*
- 1point3acres thread-1026529 "HRT Algo Dev 电面二面挂经" (2nd-phone rejection): the second round asked the candidate to **write a number-guessing game in Python or C++** — Bob generates an integer 0–999, Alex guesses. https://www.1point3acres.com/bbs/thread-1026529-1-1.html *(summary-only)*
- Another 2025 account: *"the next round focused on statistics exercises rather than brain teasers; the third round was live coding involving optimal strategy for a game"* *(summary-only)*.

So round 2 **can** involve real coding for Algo Dev, in Python or C++ at the candidate's choice.

### 2.4 Onsite

**Best first-hand account** — HRT **Algorithm Developer Internship** onsite, went onsite Oct/Nov, posted Mar 2026. Mirrored at PracHub and 1point3acres:
- https://prachub.com/interview-experiences/hudson-river-trading-intern-algorithm-developer-interview-experience-rejected-after-the-morning-onsite-rounds
- https://www.1point3acres.com/interview/thread/1102726 (= bbs thread-1102726 "HRT Algo Dev 面经")

*(summary-only — both hosts blocked; content below is the search engine's rendering of that account)*

- Pipeline: **1 coding OA → 2 math online interviews → onsite.**
- Onsite = **4 rounds**: **programming, data analysis, system design, math.**
- **Each round is one hour.** In-person at the office. **Two rounds in the morning, two in the afternoon, lunch at the company in between.**
- **Round order is randomised per candidate.** This candidate drew programming + data analysis in the morning.
- **They cut candidates at lunch.** *"If your results in the first two rounds aren't good, they might just cut the interview short right there."* This candidate was rejected after the morning rounds and never saw the afternoon two.
- Math rounds: probability and combinatorics; *"you need a solid grasp of the Central Limit Theorem and basic probability."*

**A second, independent onsite description** from a Glassdoor Algorithm-Developer-Intern report: OA (4 questions, one pandas) → then rounds on **probability, algorithms, "system design", and data science**, *"each round around an hour long over Zoom"* *(summary-only)*. Note this one is **remote**; the PracHub one is **onsite in the office**. Both formats occur.

**A third shape — 5 rounds — is asserted by PREP-SITE sources only** (`oavoservice.com`, `tradermath.org`, `quantt.co.uk`: *"around five 1-on-1 rounds: coding, probability, expected value games and data analysis"*). One Blind thread title ("For those who had algo dev onsite at HRT") is consistent with a multi-round onsite but I could not read the replies. **The 4-round shape has first-hand support; the 5-round shape does not.**

**Total hours:** roughly **4 hours of interviews** for the 4×1hr onsite, plus 2.5hr OA, plus ~1.5hr of phone screens ≈ **8 hours of assessed time**, spread over weeks. No source gives an official total.

### 2.5 How it differs from the SWE track, stage by stage

| Stage | Algo Dev | SWE / Algo Engineer / Core Dev |
|---|---|---|
| OA | Coding, 3 Q / 150 min (sometimes 4 Q). Pandas question can appear. | Coding. "2h/3Q, all test cases" (algo engineer); a separate "General Coding Assessment" for SWE. Codility/HackerRank/CodeSignal. |
| Phone 1 | **Probability & statistics.** ~45 min. | C++/systems/OS. `Lazar-Ilic/Lazar` transcribes: *"Phone interview deep C++ questions, including implementation details of STL and memory allocation for the run time… **No algo questions during phone interview, only C++ questions.**"* |
| Phone 2 | Algorithms, sometimes live coding (Python **or** C++). | Linux, networking, C++ concepts; kernel concepts. |
| Onsite | programming / **data analysis (pandas)** / system design / **math** | coding & debugging / technical design / systems (inode, RAID 5 vs 6, soft vs hard links, du vs df, virtual vs physical memory, TCP vs UDP, threading & IPC) / team fit |

Blind, on the track split *(summary-only)*: *"Algo dev is much more math focused, while Algo eng is more like SWE with some math, and SWE is pure software."* — https://www.teamblind.com/post/hrt-algo-engineer-vs-core-developer-o7pufvsd and https://www.teamblind.com/post/hrt-hudson-river-trading-algo-developer-vs-algo-engineer-orfsnfoz

**Note on HRT's official interview blog:** https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/ covers **"Software Engineering" and "Algo Engineering" only** — *not* Algo Dev *(summary-only, site blocked)*. **OFFICIAL.** So HRT has published no public description of the Algo Dev interview. The generic HRT Beat piece https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/ says only: *"the interview process begins with a series of Zoom calls that can be exploratory conversations or jump right into technical phone screens, depending on the role and candidate"*, that *"each stage of the interview process will have a particular focus/scope and a standardized set of questions for the season"*, and that the goal is *"to get a sense of how you think and what it would be like to collaborate with you."* **OFFICIAL** *(summary-only)*.

---

## 3. Round 1 in detail

**This is the round the candidate is about to sit. Here is what is actually supported.**

### Confirmed
- **Content: probability and statistics. Nothing else.** Multiple independent 1point3acres Algo Dev threads: *"all technical questions surround probability and statistics"*; *"the first round covers probability/statistics with three problems total, involving conditional probability, distribution, and Bayes theorem."* *(summary-only)*
- **Length: 45 minutes.** *"one round of interviews includes self-introductions and three probability and statistics questions over 45 minutes"* — recurring across https://www.1point3acres.com/bbs/thread-1025739-1-1.html and https://www.1point3acres.com/bbs/thread-952752-1-1.html *(summary-only)*
- **Structure: brief self-intro / resume walk-through, then 3 problems.** Some accounts say the interviewer asks about **data-science projects on your resume** before the problems.
- **Platform: Zoom.** thread-1032012 "HRT Algo Dev 第一轮phone": *"the first round phone interview was conducted via Zoom where candidates answered math problems"* — https://www.1point3acres.com/bbs/thread-1032012-1-1.html *(summary-only)*
- **CoderPad is sent but is not a coding test.** The existing evidence the parent agent already holds — a CoderPad link emailed ahead of round 1, *"mainly used to run simulations for the probability-related problems"* — is **corroborated** by a search summary of the same claim, and is consistent with every account describing round 1 as pure probability. **No first-hand Algo Dev round-1 account describes being scored on code.**

### Not confirmed — do not assume
- **Camera on/off: unknown for Algo Dev round 1.** The only camera data point I found is for the **algo engineer** OA: *"three very difficult problems within a two-hour ten-minute timeframe with **no camera or screen recording required**"* *(summary-only)* — that is the OA, not the interview. Since it is a Zoom call, assume camera on and be ready either way.
- **One interviewer vs two: unknown.** Every account is phrased in the singular ("the interviewer", "he asked me"), which weakly implies **one**. A PREP-SITE (`spacecomplexity.ai`) asserts *"a single 60-minute call with a working engineer or researcher"* — note it says **60**, contradicting the first-hand **45**. Trust 45.

### Concrete reported round-1 / phone probability questions

**From a Glassdoor HRT phone interview, three questions in one sitting** — the Glassdoor page title itself preserves them verbatim (this is why the title is worth quoting in full):
> *"phone interview: (1) 3x3 large square, the surface is painted in red. After cutting into 27 pieces, just take one piece and throw it on the table. Five sides are white and white. Ask the probability that the last face is red. (2) X = the sum of 100 rolls of dice, Y = the number of heads of 600 coin flips, ask Pr(X>Y) (3) N points randomly in a circle. The probability that all of them lie in a semicircle"*
> — https://www.glassdoor.com/Interview/phone-interview-1-3x3-large-square-the-surface-is-painted-in-red-After-cutting-into-27-pieces-just-take-one-piece-a-QTN_5094471.htm **FIRST-HAND** *(title read from search results; page blocked)*

Answers as discussed in the Glassdoor replies *(summary-only)*:
1. **6/7.** Seven of the 27 cubies have exactly five white faces — the six face-centres and the one body-centre. Six of those seven have a red sixth face.
2. **≈99%.** E[X]=350, Var(X)=100·(35/12)≈291.7; E[Y]=300, Var(Y)=600·¼=150. X−Y ≈ N(50, ~442), σ≈21, so P(X−Y>0)=Φ(50/21)=Φ(2.38)≈0.991. **Expected method: CLT.**
3. **n/2^(n−1).** Standard.

**Other reported Algo Dev / HRT probability items** *(summary-only unless noted)*:
- **Estimator efficiency (the one the parent agent already has).** With probability 0.2, X = μ exactly; with probability 0.8, X ~ N(μ,1). Mean or median to estimate μ? Then **prove** P(|μ̂_median − μ| > 0.1) < P(|μ̂_mean − μ| > 0.1). Then discuss intuitively when the mean beats the median and when the median beats the mean. **Confirmed independently by search summary.** Corroborated in kind by `pushpa-kumar/placement-prep` line 437, which logs an HRT item *"Choose mean or median for a trading profit metric (statistics reasoning), Status: REAL, Source: PracHub"* — same theme, different dressing. **This is a recurring HRT theme, not a one-off.**
- **1000 coins, one is double-headed (HH), the rest are HT; 10 tosses.** Classic Bayes-update-to-posterior. From thread-1025739 "hrt algo dev 第一轮概率统计面经". **This is the single most on-point thread I found and its content is a Bayes problem.**
- **Biased coin Bernoulli(p): find p maximising the probability that the first "HT" completes exactly on the 5th toss.** Reported as a first-round math question. Optimisation over a probability expression — calculus + probability combined.
- **Expected number of people you see until you see someone taller than you** (infinite exchangeable population). Answer via H_n = 1 + 1/2 + … + 1/n; for the "until strictly taller" variant the expectation diverges. **Confirmed on the Glassdoor Algorithm-Developer-Intern question list.**
- **Roll a fair d6 until you've seen all six faces — expected number of rolls.** Coupon collector, 6·H₆ = 14.7. **On the same Glassdoor Algorithm-Developer-Intern list.**
- **Expected number of socks you must pull to identify which drawer is which.** Same list.
- **Expected number of loops (spaghetti problem).** Same list. Answer H_n.
- **P(sum of 100 dice = 400)** — from a phone-screen account; *"the interviewer suggested using Binomial Approximation… and asked follow-up questions about variance in a normal distribution approach."* **The interviewer steered toward the analytic approximation.** — https://1o24bbs.com/t/topic/1861 *(summary-only)*
- **x and y i.i.d. standard normal** — opening question of a first-round phone (thread-1032012). Exact follow-up not captured.
- **25 bunnies, 5 lanes, no timer, only relative order per race — how many races to find the top 3?** Confirmed as an HRT question via search summary. Classic answer: **7**. Note this is a *combinatorial/algorithmic* puzzle, not probability.
- **Two rooks on a chessboard, non-attacking, maximise the sum of their squares' values** — HRT OA, **REAL**, `Status: REAL` in `pushpa-kumar/placement-prep`, source https://leetcode.com/discuss/interview-question/889638/hudson-river-trading-oa-two-rooks

### Recurring topic map for Algo Dev probability/stats

Ordered by strength of evidence:

| Topic | Evidence |
|---|---|
| **CLT / normal approximation to sums** | **Strongest.** Dice-vs-coins, P(sum=400), and the PracHub onsite account's explicit *"you need a solid grasp of the Central Limit Theorem."* |
| **Bayes / conditional probability / posterior updating** | Very strong. 1000-coins, painted cube, and 1point3acres' own topic summary (*"conditional probability, distribution, and Bayes theorem"*). |
| **Expected value & expectation by conditioning / harmonic sums** | Very strong. Taller-person, coupon collector, socks, spaghetti loops. |
| **Estimators, efficiency, robustness (mean vs median)** | Strong and *distinctive to HRT*. Two independent instances. |
| **Order statistics** | Moderate — named by Blind summaries and prep sites; the taller-person and mean/median problems are order-statistics in substance. |
| **Distributions (normal, binomial, Bernoulli) and their variances** | Strong. Recurs in every dice/coin variant. |
| **Combinatorics** | Moderate–strong. Named explicitly in the PracHub onsite account's math round. |
| **Linear algebra** | Moderate, **intern-specific** — see §9. |
| **Markov chains / Markov processes** | **Weak.** Named only by PREP-SITE pages (quantt, tradermath). **No first-hand Algo Dev report of a Markov chain question surfaced.** Worth knowing, but the evidence is not there. |
| **Hypothesis testing** | **Weak.** PREP-SITE only. |
| **Regression / time series** | **Weak as an interview topic** — but see §6: it is explicit in HRT's *job description*, and plausibly appears in the data-science round rather than as a stated question. |
| **Martingales / stochastic calculus** | **No evidence at all.** No source, first-hand or prep, reports a martingale or Itô question for Algo Dev. HRT is a market maker, not a derivatives desk. **Deprioritise.** |

---

## 4. The data-science / pandas round

### What is confirmed

- **The round exists and is one of the 4 onsite rounds.** PracHub/1point3acres intern account: onsite = programming, **data analysis**, system design, math. **1 hour.** *(summary-only)*
- `Lazar-Ilic/Lazar` transcribes a Glassdoor report verbatim — **this is the single most concrete description of the round** and I read it at source:
  > *"Phone interview research + math; then 4 rounds of onsite interview: One round coding, **one round data science [use pandas, prediction tasks]**, one round open-ended questions, one round behavioral. Signed non disclosure for the onsite part."*
  **TRANSCRIBED, read at source.** Note this describes a **different** 4-round split (coding / data science / open-ended / behavioural) than the intern account (programming / data analysis / system design / math). **The onsite composition varies.**
- **A concrete task: heart-disease prediction.** *"One candidate received a heart disease prediction problem with features like age, weight, and height, requiring comfort with pandas and seaborn for plotting, with documentation access allowed."* *(summary-only)*. Independently logged in `pushpa-kumar/placement-prep` (read at source, line ~618): *"**Build a baseline machine-learning model predicting heart disease from a dataset** — Company: HRT — Round/Stage: Technical screen — **Status: REAL** — Source: PracHub."*
- **Pandas is expected if it is on your resume.** `Lazar-Ilic/Lazar`, read at source, on the "Pandas Question" entry: *"OK if you write it down on your Resume for sure expected knowledge."* **TRANSCRIBED.** This directly corroborates the existing evidence.
- **A pandas question can appear in the OA too**, not only onsite: a 1point3acres thread is titled literally *"HRT OA 要用pandas？"* ("Does the HRT OA need pandas?") — https://www.1point3acres.com/bbs/thread-921241-1-1.html, with candidates mentioning **pandas aggregation** as an OA question. A Glassdoor Algorithm-Developer-Intern report likewise describes *"an online assessment with 4 questions including one involving Pandas."* *(summary-only)*
- **You may Google / consult documentation.** Reported for the data round specifically, and consistent with a general HRT posture — Blind: *"You are free to google things during the interview, and HRT generally tries to be transparent and evaluate people at their best state."* *(summary-only)*

### So: EDA, modelling, feature engineering, or backtesting?

**Answer, on the evidence: EDA + a baseline predictive model, in a notebook. Not backtesting.**

- "prediction tasks" (transcribed, read at source) + "build a **baseline** ML model" (REAL, logged) ⇒ **you fit something simple and defend it**, you do not build a tuned model.
- seaborn plotting + "explore it in a Python notebook" ⇒ **exploratory data analysis is a real component**.
- Feature engineering: implied (the heart-disease features are named: age, weight, height — the obvious move is BMI-style derived features), not directly attested as a stated task.
- **Backtesting: no first-hand evidence.** It is asserted only by PREP-SITE pages, and HRT's job posting mentions backtesting as a *job duty*, not an interview task. One PREP-SITE claim — *"filtering sets of timestamped trades and calculating profits"* — is plausible in shape but unattributed.

**Library set to be fluent in:** `pandas`, `numpy`, `matplotlib`/`seaborn`, `scikit-learn`, `scipy`. (scikit-learn/scipy naming is PREP-SITE; pandas/seaborn/numpy are attested.)

---

## 5. Language: Python or C++?

**Resolved, and the answer is Python — with a specific caveat.**

**OFFICIAL — HRT's own Algorithm Development (Quant Research) Internship posting**, qualifications, quoted from a search-engine rendering of https://www.hudsonrivertrading.com/hrt-job/algorithm-development-quant-research-internship-summer-2026-3/ *(site blocked; also mirrored at prosple.com, capd.mit.edu, builtinnyc.com)*:
> - *"**Experience programming in Python is a must; C++ is a plus for those interested in high-frequency trading**"*
> - *"Experience with statistical analysis, numerical programming, or machine learning in **Python, Pandas/Numpy, R, and/or MATLAB**"*
> - *"Interns rotate between high-frequency trading, multi-frequency trading, and/or **machine learning** teams"*
> - *"using **machine learning and time series techniques** to derive insights on market behavior from large, complex datasets"*
> - *"Interns leverage proprietary infrastructure (Python/C++) and third-party tools for quantitative research and data analysis"*

**OFFICIAL — the full-time "Algorithm Developer (Quant Researcher)" posting** (2025/2026/2027 Grads and PhDs variants) carries the same statistical-programming bullet — *"Experience with statistical analysis, numerical programming, or machine learning in Python, Pandas/Numpy, R, and/or MATLAB"* — plus *"Brilliant analytical and problem solving skills"* and a Math/CS/Stats/Physics degree. **C++ does not appear prominently in the Algorithm Developer (Quant Researcher) qualifications.** *(summary-only)*

**Where the conflicting evidence comes from — and it is a real distinction, not noise.** HRT runs a *separate*, differently-worded posting titled plainly **"Algo Developer"** (https://www.hudsonrivertrading.com/hrt-job/algo-developer/, the experienced-hire listing) whose skills list **does** include *"familiarity with the C++ programming language"* and describes *"a mix of quantitative (math, stats, data analysis) and technical (C++/Python programming) skills in researching, backtesting, and monitoring new strategies."* **The source that said "C++ is essentially required for algo dev" was reading that posting; the source that said "Python for research roles" was reading the campus/quant-researcher posting. Both are quoting HRT accurately about different listings.**

**Practical resolution for this candidate:**
1. **Python is the expectation for the Algorithm Developer (Quant Researcher) track.** It is a stated *must*. Prototype in Python; pandas/numpy fluency is assumed.
2. **C++ is not required at any Algo Dev interview stage on the evidence.** The one Algo Dev round where a language was chosen — phone round 2, the number-guessing game — the report says *"in Python **or** C++"*, candidate's choice.
3. **The deep-C++ phone screen (STL internals, memory allocation, "no algo questions, only C++") is the SWE / Core Developer / Algo Engineer track**, transcribed as such in `Lazar-Ilic/Lazar`. Do not prepare for it.
4. If asked about C++ at all, the honest framing is the workflow HRT's own materials describe: **researchers prototype signals in Python and pair with systems developers to move winning signals into production C++.**

---

## 6. Machine learning content

**How much: real but shallow-to-moderate, concentrated in the data round and the resume conversation. Not a dedicated ML-theory grilling.**

- **OFFICIAL:** ML is written into the Algo Dev job description twice — interns *"rotate between high-frequency trading, multi-frequency trading, and/or machine learning teams"*, and the role uses *"machine learning and **time series** techniques… on large, complex datasets."* Qualifications ask for *"statistical analysis, numerical programming, or **machine learning** in Python, Pandas/Numpy, R, and/or MATLAB."*
- **The one attested ML interview task is the heart-disease baseline model** (§4) — logged `Status: REAL`. That is *applied* ML: load, explore, featurise, fit a baseline, evaluate, explain.
- **Round 1 accounts mention the interviewer asking about your data-science projects** before the probability problems. Expect to defend your own ML work.
- **Depth of theory questions: unverified.** A PREP-SITE (`oavoservice.com`) claims one onsite round covers *"machine learning techniques and their application in quantitative finance, including algorithms, model assumptions, and feature engineering."* Plausible, unattributed. Overfitting/regularisation/L1-L2 material surfaced in searches but **only from generic ML-interview pages, never from an HRT report.**

**Practical:** be able to (a) fit and justify a baseline in scikit-learn, (b) talk crisply about **bias–variance, overfitting, train/test discipline, and why a linear model is often the right answer on noisy financial data**, (c) discuss **time-series specific pitfalls** — lookahead bias, non-stationarity, autocorrelated residuals invalidating i.i.d. assumptions — since time series is explicitly in the job spec. **Do not over-invest in deep learning.**

---

## 7. The exact-computation-over-simulation trap — verified in substance, corrected in detail

**Verdict: the underlying instinct is right, but the specific story is slightly wrong. HRT steers toward *analytic* answers — and the analytic answer they want is usually the CLT/normal approximation, not a dynamic program.**

**What I confirmed:**

1. **The dice-vs-coin question is real and recurs, with varying constants.**
   - Glassdoor phone interview, question (2): *"X = the sum of 100 rolls of dice, Y = the number of heads of 600 coin flips, ask Pr(X>Y)"* — https://www.glassdoor.com/Interview/phone-interview-1-3x3-large-square-the-surface-is-painted-in-red-After-cutting-into-27-pieces-just-take-one-piece-a-QTN_5094471.htm **FIRST-HAND (title verbatim)**
   - `Lazar-Ilic/Lazar`, read at source, transcribes the variant: *"Toss A Dice 100 Times And A Coin 400 Times, Compute P[Dice Sum > Coin Heads]"* **TRANSCRIBED**
   - So the constants move (600 coins vs 400 coins). **Do not memorise a number; memorise the method.**

2. **The expected method is CLT.** The Glassdoor discussion's accepted answer computes E and Var for both sums, forms X−Y ~ N(50, ~450), and reads off ≈99% from a 2.38-sigma z-score. **That is the answer HRT wants: two moments and a z-score, in under a minute.**

3. **An interviewer was independently observed steering a candidate to the analytic approximation.** On the P(sum of 100 dice = 400) variant: *"the interviewer suggested using Binomial Approximation… and asked follow-up questions about variance in a normal distribution approach."* — https://1o24bbs.com/t/topic/1861 *(summary-only)*. **This is the closest thing I found to direct evidence of HRT preferring exact/analytic over simulation, and it is an interviewer intervention, not a candidate's opinion.**

4. **The "exact DP beats Monte Carlo" argument does exist in a source — but it is a candidate's own prep note, not an interviewer's criticism.** `Lazar-Ilic/Lazar`, read at source, on the 100-dice/400-coins variant:
   > *"Certainly feels intuitively like the direct discrete accurate answer with 0 error might be stronger than any sort of naive simulations based approach here… you can actually do this in O[a log b] by first computing those probabilities and then doing a Fast Fourier Transformation to extract out all coefficients in the probability generating function polynomial… **Proposing naive simulations would be Wrong here also in part due to the Probability being ~1 so it would take many iterations to converge into the accurate answer.**"*
   He then prints the exact rational answer, ≈0.9999999999999925.

**Correction to the brief:** I found **no first-hand report of a candidate's Monte Carlo answer being criticised by an HRT interviewer.** The "Monte Carlo criticised, exact DP expected" claim is not attested at source; what *is* attested is (a) an interviewer pushing toward binomial/normal approximation, and (b) a candidate's own written reasoning that simulation is the wrong tool here.

**But the reasoning behind it is sound and worth internalising, because it is a genuine statistical point.** When P ≈ 0.99999999999999, a Monte Carlo estimate needs an astronomically large sample to resolve the answer at all — every draw comes back "yes". **Simulation has no resolution in the tails.** That is exactly the kind of statistical-judgement failure a market maker screens for.

**Operational rule for CoderPad in round 1:**
- **Lead with the analytic answer.** Moments → CLT → z-score → number. Say it out loud before you touch the keyboard.
- **Use NumPy to *check*, not to *answer*.** "Let me sanity-check my 99% with 10⁵ draws" is a good look. "Let me simulate to find the answer" is not.
- **If the true probability is extreme (near 0 or 1), say so and say why simulation cannot resolve it.** That sentence is worth more than the code.
- **If an exact discrete computation is cheap — a convolution / DP over the score distribution, or `numpy.convolve` on the pmf — do that instead of sampling.** It is exact, it is fast, and it demonstrates you know the difference.

---

## 8. What gets Algo Dev candidates rejected, versus SWE

**FIRST-HAND, the clearest signal I found** *(summary-only)*, from the intern onsite account: **HRT cuts candidates at lunch.** *"If your results in the first two rounds aren't good, they might just cut the interview short right there."* The poster was rejected after the morning rounds. **Because round order is randomised, whichever two rounds you draw in the morning are effectively a gate.**

Other reported failure modes for Algo Dev:
- **The second phone screen is a real cull.** Blind: rejected at the 2nd phone round, *"an interview that included difficult questions toward the end"*; 1point3acres thread-1026529 is literally a 2nd-phone rejection post. **The two phone rounds are not a formality.**
- **Not finishing / not reaching the optimal answer under time pressure** is the OA failure mode, shared with SWE — and passing the OA is no guarantee (*"passing the OA is a mystery"*).
- **No feedback is given.** *"They did not give feedback on why they rejected."* *(summary-only)*
- **Cooldown.** A PREP-SITE claims a strong rejection on a specific round extends the reapplication wait to ~18 months. **PREP-SITE, unverified.**
- **Culture fit is a live rejection reason.** One candidate reported passing all technical rounds and believing they were cut on the culture-fit interview. *(summary-only, single report.)*

**The Algo Dev vs SWE difference in what kills you:**
- **SWE/Core Dev candidates fail on depth**: C++ internals, OS/memory/networking, low-latency reasoning. `Lazar-Ilic/Lazar` transcribes *"LeetCode questions were easy… **Systems questions required deep knowledge on Operating Systems, memory, networking, etc.**"* — the systems questions, not the coding, are the filter.
- **Algo Dev candidates fail on statistical judgement**: getting probability right *and proving it*. Blind, repeatedly: *"HRT will ask a medium difficulty probability question and **will make you prove your method in edge cases** over the phone"*; *"they will also ask you to prove algo questions"*; *"The coding part is easier than Google, but that's not the main part of HRT interview. **Main emphasis is on probability theory.**"* *(summary-only)*
- **Reciting memorised brainteasers is a stated failure mode.** Blind: *"Make sure that you spend time learning maths and cs properly, not just memorizing brainteasers and LC… at some point in the interview process, there will be a question that you haven't seen before."* *(summary-only)*

---

## 9. Intern vs full-time on the Algo Dev track

**Confirmed differences:**

| | Algo Dev **Intern** | Algo Dev **Full-time** |
|---|---|---|
| Pipeline | Coding OA → **2 math phone rounds** → onsite | OA → phone 1 (prob/stats) → phone 2 (algorithms) → onsite |
| Phone content | **Probability + linear algebra.** Blind: *"For Algo dev positions, HRT asks some basic probability questions and **linear algebra** questions"* *(summary-only)* | Probability/statistics, then algorithms |
| Onsite | **4 rounds × 1 hour**, in-office, 2 AM + 2 PM, lunch between, **randomised order, cut at lunch** | 4 rounds reported (coding / data science / open-ended / behavioural), NDA signed for onsite |
| Comp | $5,800/week + $25,000 signing bonus + paid housing/meals (**OFFICIAL**) | $300,000 base for 2026 PhD grads + signing + discretionary bonus (**OFFICIAL**, *summary-only*) |

- **The existing evidence — interns get probability + linear algebra rather than the SWE conceptual round — is corroborated.** The linear-algebra element appears in Blind's Algo Dev description and in 1point3acres intern threads (thread-945196 "HRT algo deve intern 一面二面", thread-952752). The SWE "conceptual" round (OS/memory/networking/C++) is transcribed in `Lazar-Ilic/Lazar` as belonging to the engineering tracks. **These are genuinely different question sets.**
- **Interns also get the data-science round** — the intern onsite includes "data analysis" as one of the four.
- **The intern OA and the full-time OA look the same** (3 questions / 150 min, coding). Reported intern OA items: "fancy number" base-4 digit DP, Reversi, tree merge/pre-order.
- **Full-time PhD hiring is a distinct posting** ("Algorithm Developer (Quant Researcher) – 2026 PhDs") but no evidence of a different interview loop surfaced.

---

## 10. Actionable read for a candidate with round 1 tomorrow

1. **Round 1 is 45 minutes, on Zoom, ~3 probability/statistics problems after a short resume/self-intro. Almost certainly one interviewer. CoderPad will be open but is a scratchpad, not a test.**
2. **Answer analytically first, every time.** Moments → CLT/z-score, or Bayes, or expectation-by-conditioning. Only then reach for NumPy — and frame it as *verification*.
3. **Never propose simulation as the primary method for a near-0 or near-1 probability**, and say out loud why: Monte Carlo has no resolution in the tails.
4. **Be ready to prove, not just answer.** The most-repeated Algo Dev-specific signal in the entire corpus is that HRT makes you *justify the method and handle edge cases*. The estimator question is literally "prove P(|median error| > 0.1) < P(|mean error| > 0.1)".
5. **Drill, in priority order:** CLT & normal approximation to sums; Bayes/posterior updating; expectation by conditioning and harmonic sums; **mean-vs-median / estimator efficiency and robustness** (HRT's signature theme); variances of binomial/Bernoulli/uniform-discrete; combinatorics; basic linear algebra if interning.
6. **Deprioritise:** martingales, stochastic calculus, option pricing, Markov chains (all weakly or un-evidenced for this track), and deep C++.
7. **Know your own resume's pandas/ML projects cold** — the interviewer may open on them, and a pandas question is expected if pandas is listed.
8. **If you reach onsite: the morning is a gate.** Two of {programming, data analysis, system design, math} in random order, one hour each, and a bad morning ends the day at lunch.

---

## 11. Source ledger

### Read in full at source (verbatim-verifiable)
- https://raw.githubusercontent.com/Lazar-Ilic/Lazar/main/Notes/Computer%20Science/Algorithms/Interviews%20Coding%20Rounds/Hudson%20River%20Trading.txt — **TRANSCRIBED** (Glassdoor/AlgoDaily items + own commentary)
- https://raw.githubusercontent.com/pushpa-kumar/placement-prep/main/raw-notes/company-hrt-citadel.md — **TRANSCRIBED**, REAL/PRACTICE-labelled with LeetCode Discuss permalinks

### FIRST-HAND in origin, reached only via search summary (page blocked)
- https://www.glassdoor.com/Interview/phone-interview-1-3x3-large-square-the-surface-is-painted-in-red-After-cutting-into-27-pieces-just-take-one-piece-a-QTN_5094471.htm — the three-question phone interview; title read verbatim
- https://prachub.com/interview-experiences/hudson-river-trading-intern-algorithm-developer-interview-experience-rejected-after-the-morning-onsite-rounds — intern onsite, 4×1hr, cut at lunch
- https://www.1point3acres.com/interview/thread/1102726 · https://www.1point3acres.com/bbs/thread-1102726-1-1.html — same onsite account
- https://www.1point3acres.com/bbs/thread-1025739-1-1.html — "hrt algo dev 第一轮概率统计面经": 3 prob/stats Q in 45 min; 1000-coins problem
- https://www.1point3acres.com/bbs/thread-1032012-1-1.html — round 1 on Zoom, i.i.d. standard normals
- https://www.1point3acres.com/bbs/thread-1026529-1-1.html — 2nd-phone rejection; guessing game in Python or C++
- https://www.1point3acres.com/bbs/thread-952752-1-1.html · /thread-945196-1-1.html — intern round 1, prob + linear algebra
- https://www.1point3acres.com/bbs/thread-921241-1-1.html — "HRT OA 要用pandas？"
- https://www.1point3acres.com/bbs/thread-1112867-1-1.html · /thread-1026334-1-1.html · /thread-1022110-1-1.html · /thread-1100539-1-1.html · /thread-1101053-1-1.html · /thread-1090083-1-1.html · /thread-1144412-1-1.html · /interview/thread/1028674 — OA and VO threads
- https://1o24bbs.com/t/topic/1861 — P(100 dice sum = 400); interviewer steered to binomial/normal approximation
- https://www.teamblind.com/post/hudson-river-trading-hrt-algo-developer-phone-interview-what-to-expect-1nz00wah — two-phone structure
- https://www.teamblind.com/post/for-those-who-had-algo-dev-onsite-at-hrt-dzkkiek4 — Python allowed, open-ended research question, Google allowed
- https://www.teamblind.com/post/hrt-algo-engineer-vs-core-developer-o7pufvsd · .../hrt-hudson-river-trading-algo-developer-vs-algo-engineer-orfsnfoz — track split
- https://www.glassdoor.com/Interview/Hudson-River-Trading-Algorithm-Developer-Intern-Interview-Questions-EI_IE470937.0,20_KO21,47.htm — taller-person, coupon collector, socks, spaghetti loops; OA with pandas
- https://www.wallstreetoasis.com/forum/trading/hudson-river-trading-algorithm-developer-interviewother-questions

### OFFICIAL (HRT's own words), reached only via search summary
- https://www.hudsonrivertrading.com/hrt-job/algorithm-development-quant-research-internship-summer-2026-3/ — *"Python is a must; C++ is a plus"*; ML + time series
- https://www.hudsonrivertrading.com/hrt-job/algorithm-developer-quant-researcher-2026-phds/ — full-time quant researcher qualifications
- https://www.hudsonrivertrading.com/hrt-job/algo-developer/ — the **experienced-hire** listing that does mention C++ (source of the conflict in §5)
- https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/ — covers **SWE and Algo Engineering only**, not Algo Dev
- https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/ — general process statements

### PREP-SITE — cited nowhere as fact in this document
tradermath.org · quantt.co.uk · spacecomplexity.ai · myntbit.com · datainterview.com · dataloopr.com · linkjob.ai · hacktherounds.com · oavoservice.com · quantblueprint.com · techprep.app · interviewprep.org · companyinterviews.com · yourcareersupport.com · everythingquant.com · thewallstreetquants.com · interviewdb.io · dataford.io

### Fabricated — discard
- https://github.com/sumitsingh4411/interview-rounds/blob/main/content/companies/hudson-river-trading.md — invented "Full-stack / Backend / Frontend" HRT interview experiences
