# Coding Interview Questions — Other Firms (2021–2026)

Firms covered: CFM, Peak6, Walleye Capital, Jain Global, Freestone Grove Partners, Seven Eight Capital, Valkyrie Trading, Volant Trading, Group One Trading, TransMarket Group, 3Red Partners, Gelber Group; crypto market-makers Wintermute, GSR, B2C2, Cumberland DRW, Amber Group.

**Methodology & limitations.** ~23 web searches across Glassdoor, 1point3acres, Wall Street Oasis, QuantNet, Blind, Reddit, GitHub, company sites and interview-prep aggregators. The research environment's network proxy blocked direct page fetches to nearly all source domains (Glassdoor, WSO, 1p3a, Reddit, Medium, QuantNet, mirror.xyz, etc.), so details below come from search-result extraction of those pages rather than full page reads, and the session's shared search budget capped further digging. Everything reported is sourced; where evidence is thin it is flagged explicitly. Nothing is invented. Dates: most reports are 2021–2025 era; exact years given only where the source stated them.

Track tags: **[SWE/QD]** = software engineer / quant developer; **[QT/QR]** = quant trader / researcher. **[INTERN]** / **[FT]** where sources say.

---

## 1. CFM — Capital Fund Management (Paris/NY, quant hedge fund)

**Pipeline.** Quant researcher / data scientist track: online assessment on **Python** → Zoom interview with the future manager → for researcher roles, a heavier gauntlet reported as: 45-min review of past research → **4-hour technical test** with numerical questions and theoretical problems (reportedly based on the Potters & Bouchaud textbook — CFM founders' book *Theory of Financial Risk and Derivative Pricing*) → 1-hour research seminar presented to all researchers → ~4 interviews with managers, HR, IT. Language: Python (R/SQL mentioned for data roles).

**Reported questions.**
- Math/quant-to-code **[QT/QR] [FT]**: binomial tree in option pricing; Newton's method (root finding); PCA. (Glassdoor interview reports, via search extraction.)
- Data manipulation **[QT/QR]**: statistical analysis, feature extraction from large datasets, data-modeling questions for data-scientist roles.
- Take-home/long-form: the 4-hour written technical test (numerical + theory) for QR roles.
- Probability + brain teasers reported generally.

**Style notes.** Very "French quant" flavour: heavy on statistics/statistical physics theory, less LeetCode. Coding is Python-centric and screened via OA. Evidence on the quant-dev/SWE track specifically is **thin** — no concrete C++/algorithm question reports found.

Sources: https://www.glassdoor.com/Interview/Capital-Fund-Management-Interview-Questions-E698649.htm ; https://www.quantt.co.uk/quant-firms/capital-fund-management-cfm

---

## 2. Peak6 (Chicago; Peak6 Capital Management / Peak6 Investments)

**Pipeline.** **[SWE] [INTERN & FT]**: HackerRank OA (**90 min, 2 questions, LeetCode-medium**) → phone interview (behavioral + 2 coding problems) → onsite/virtual final with ~3 interviews incl. a **two-hour coding challenge** and HR round. Avg ~19 days to hire for SWE interns.

**Reported questions.**
- Arrays/strings/hashing **[SWE] [INTERN]**: **"Kangaroo Words"** (find words containing a synonym as a subsequence — recurring OA question, reported by multiple candidates, several couldn't finish in time); a question described as "about terminals"; string manipulation — find words in a string separated by spaces that are not actual words.
- Scheduling/simulation **[SWE]**: **train schedule** problem; a variant reported as **flight schedules** (HackerRank OA); "Min gates" (minimum gates/platforms needed given arrivals/departures — classic interval problem) paired with Kangaroo Words in one OA report.
- Data: database-structure questions reported in later rounds.

**Style notes.** OA questions are recycled heavily (same pair reported by many candidates); medium difficulty but time-pressured. Trader-track evidence at Peak6 is **thin** in 2021+ sources (older reports are poker/mental-math flavoured; not confirmed recent).

Sources: https://www.glassdoor.com/Interview/PEAK6-Software-Engineer-Internship-Interview-Questions-EI_IE13323.0,5_KO6,34.htm ; https://www.glassdoor.com/Interview/OA-2-questions-Min-gates-and-Kangaroo-Words-QTN_3972967.htm ; https://www.glassdoor.ca/Interview/kangaroo-words-QTN_3478412.htm ; https://www.1point3acres.com/interview/company/peak6

---

## 3. Walleye Capital (Minneapolis/NY multistrat)

**Pipeline.** 4–6 rounds: HackerRank OA → behavioral/technical interviews → case study for most roles. Two OA formats reported: **120 min / 3 questions** (one LC-easy, one API question ~LC-medium, one LC-hard algorithm) and **180 min / 4 questions** (complex SQL, functional programming, API requests, algorithms). **[QD] [INTERN]** reports exist on Glassdoor ("Quantitative Developer Intern").

**Reported questions.**
- Arrays/algorithms **[SWE/QD]**: LC easy→hard spread in the HackerRank OA (no exact titles reported).
- Data manipulation **[SWE/QD]**: complex SQL in the 180-min OA; API-request/parsing tasks (call an API, aggregate results — HackerRank "REST API" style).
- ML/stats deep-dive **[QT/QR]**: walkthrough of a past statistical/ML project — hypotheses, model choice, features, performance, design choices; probability-distribution and **maximum-likelihood estimator** brainteasers.
- Math/data brainteasers **[QT/QR] [INTERN]**: "data manipulation and math brainteasers, nothing too hard" plus resume questions.

**Style notes.** Glassdoor difficulty 3.59/5; Internship and Quantitative Trading Intern rated hardest tracks. Theme: practical engineering (SQL + APIs) rather than pure algorithms; research side leans applied stats/ML.

Sources: https://www.glassdoor.com/Interview/Walleye-Capital-Interview-Questions-E429277.htm ; https://www.glassdoor.com/Interview/Walleye-Capital-Quantitative-Developer-Intern-Interview-Questions-EI_IE429277.0,15_KO16,45.htm ; https://www.1point3acres.com/interview/company/walleye ; https://walleyecapital.com/campus-faq

---

## 4. Jain Global (NY multistrat, founded 2024)

**Pipeline.** Screening call → **two live coding sessions** with experience/project discussion (typical reported flow). QD roles reported the slowest process (~28 days avg).

**Reported questions.**
- Low-level/systems **[QD] [FT]**: 1point3acres FO Quant Dev technical phone screen (2026 Jan–Mar) focused on **low-latency trading systems** and **Python for large-data processing**, with emphasis on **OS and I/O challenges** (thread title/summary; full thread paywalled/blocked).
- Take-home + data **[SWE-data] [FT]**: Data Engineer take-home focused on **rolling calculations and data pipelines**; Data Engineer video interview covered data-quality issues, user support, compliance data modeling (1p3a).
- Quant Research Intern **[QT/QR] [INTERN]** (Summer 2026 posting-based prep pages): probability & statistics, research rigor, behavioral; requires Python + linear/non-linear statistical modeling.

**Style notes.** Young firm, few public reports — evidence base is **thin** and skewed to 1p3a summaries. Recurring theme so far: Python-at-scale + latency/OS fundamentals for dev roles.

Sources: https://www.1point3acres.com/interview/thread/1164948 ; https://www.1point3acres.com/interview/thread/1185096 ; https://www.1point3acres.com/interview/company/jain%20global ; https://www.glassdoor.com/Interview/Jain-Global-Interview-Questions-E10133419.htm

---

## 5. Freestone Grove Partners (SF/NY multistrat, founded 2023 by ex-Citadel)

**Pipeline.** Not well documented publicly. One Glassdoor QD report describes timed technical rounds with little time per question.

**Reported questions.**
- **[QD] [FT]** (Glassdoor, verbatim candidate summary): "Interview questions varied from **system design**, to **finance programming + algos**, to somewhat **random recursive algorithms**. Make sure you're well warmed up — you're not given much time to complete these questions."

**Style notes.** Evidence is **very thin** (essentially one report): mix of system design, finance-flavoured programming, and recursion under time pressure. No OA platform or trader-track reports found.

Source: https://www.glassdoor.com/Interview/Interview-questions-varied-from-system-design-to-finance-programming-algos-to-somewhat-random-recursive-algorithms-Mak-QTN_7239132.htm

---

## 6. Seven Eight Capital (NY/Stamford stat-arb)

**Pipeline.** Hires "academically strong CS/math/stats/engineering" candidates; stack is Python/AWS/Docker; runs QD internships (2023 Quant Developer Intern posting; 2025 co-op via Greenhouse).

**Reported questions.**
- ML/stats-to-code **[QD] [FT]** (Glassdoor, Junior Quant Developer, **Aug 2023**): "**What gives the largest R²?** — Lasso, Ridge, or Linear Regression"; plus differences between data structures and general coding questions.

**Style notes.** Evidence **thin** (one dated report + job-posting inferences): expect Python coding, DS&A basics, and regression/statistics conceptual questions. No OA platform documented.

Sources: https://www.glassdoor.com/Overview/Working-at-Seven-Eight-Capital-EI_IE2975320.11,30.htm (interview section) ; https://simplify.jobs/p/6c3cee64-61f7-4e62-9202-c7f953bee20f/2023-Quant-Developer-Intern ; https://triplebyte.com/company/public/seven-eight-capital

---

## 7. Valkyrie Trading (Chicago options MM)

**Pipeline — SWE track [SWE] [FT & junior]**: **two rounds of C++ online assessment** emphasizing design and code style — unusually delivered via **SurveyMonkey for timing plus a GitHub-Gist-style pastebin** for the questions → brief HR phone screen → 1.5-hour combined technical/behavioral with three engineers. Avg ~34 days; difficulty 3.1/5 for Jr SWE.

**Pipeline — trader track [QT]**: OA (sequences and probability) → HR call (mental math, sequences, probability) → final onsite with **3 written tests** and a behavioral/**market-making game** with traders.

**Reported questions.**
- Trees **[SWE]**: implement a **BST**.
- DP/matrix **[SWE]**: **largest sub-square with black-pixel borders** (LeetCode 1139-style); some candidates report LC-hard level questions in later rounds.
- Probability/sequences **[QT]**: number-sequence puzzles and probability in OA and HR round; logic/IQ tests onsite.
- Options/strategy **[QT]**: phone-round games about optimal strategy; Black–Scholes discussion.

**Style notes.** C++ design and code-style focus (not just algorithms) for engineers; trader pipeline is written-test heavy with an MM game finale.

Sources: https://www.glassdoor.com/Interview/Valkyrie-Trading-Interview-Questions-E859999.htm ; https://www.glassdoor.com/Interview/Valkyrie-Trading-Software-Engineer-Interview-Questions-EI_IE859999.0,16_KO17,34.htm

---

## 8. Volant Trading (NY options MM)

**Pipeline.** Online coding test → phone interview → onsite; avg ~12 days. SWE/C++ SWE rated the hardest tracks.

**Reported questions.**
- Design/simulation **[SWE] [FT]**: online coding round = **two LeetCode-mediums + one matching/trade-engine question + multiple C++ questions in 120 minutes** (build a simplified order-matching engine).
- Low-level/C++ **[SWE]**: C++ container classes (differences/use), C++ + algorithm questions on the phone; **API design** round.
- Coding for quants **[QT/QR]**: quantitative analyst coding test = **2 C++ problems in 2.5 hours**, including a **chess problem** and a **largest product of a series** problem (LC 152 / Project-Euler-8 style).
- Probability/options **[QT]**: probability problems, options questions; **job-scheduling algorithm** question reported for quant analyst.

**Style notes.** Recurring theme: C++ fluency + a matching-engine build; trader/QR side mixes probability and options with real coding.

Sources: https://www.glassdoor.com/Interview/Volant-Trading-Interview-Questions-E407755.htm ; https://www.glassdoor.com/Interview/Volant-Trading-Software-Engineer-Interview-Questions-EI_IE407755.0,14_KO15,32.htm ; https://www.glassdoor.ca/Interview/Volant-Trading-Quantitative-Analyst-Interview-Questions-EI_IE407755.0,14_KO15,35.htm

---

## 9. Group One Trading (Chicago/NY options MM)

**Pipeline.** **[QT] [INTERN & FT]**: round 1 behavioral/fit + analytical; round 2 with head trader purely technical (mental math, probability, options). No coding OA documented for trader track; **no SWE-track coding reports found** (evidence thin on dev side).

**Reported questions (all [QT], probability/mental math — not coded).**
- Mental math: 39×21; 4% of 4; decimal value of 1/6; 2-digit multiplications.
- Expected value: EV of rolling two dice where each pip = $1; EV of coin flips; EV of two baseball at-bats with 50% strikeout probability.
- Pricing game: "You deal cards 1–10 and pay the player the value of the card dealt — what do you charge to play?" (EV = $5.50).
- Options: how market makers trade, option greeks, specific spreads.

**Style notes.** Pure trading pipeline: mental math + EV + options knowledge; think-aloud valued. Nothing suggests a programming round for trader trainees in reported period.

Sources: https://www.glassdoor.com/Interview/Group-One-Trading-Trader-Interview-Questions-EI_IE144236.0,17_KO18,24.htm ; https://www.glassdoor.com/Interview/Group-One-Trading-Trader-Trainee-Intern-Interview-Questions-EI_IE144236.0,17_KO18,39.htm ; https://www.wallstreetoasis.com/company/group-one-trading-lp-0/interview

---

## 10. TransMarket Group (Chicago prop / rates)

**Pipeline.** **[QT] [INTERN]**: **HackerRank coding challenge first** (TMG weights coding more than most prop shops) → two phone rounds → final round of **four 1-on-1 hour-long interviews** where math/probability is tied to trading. Difficulty rated 3.2/5. TMG publishes its own prep pages: *Quantitative Trading Interview Prep* recommends Hull, *Options, Futures and Other Derivatives*, chapters 1–7, 11–13, 19; there is a parallel *Algorithmic Trading Interview Prep* page.

**Reported questions.**
- Probability-to-reasoning **[QT] [INTERN]**: card-draw probability problems; expected-value problems; easier probability brainteasers.
- Markets **[QT]**: greeks; bond theory and option theory; "what's interesting in markets right now / recent market events."
- Coding **[QT/QD] [INTERN]**: HackerRank screen (specific problems not reported — evidence on exact questions thin); a "Trade Logic Developer Intern" track exists (Purdue posting) implying a dev-intern pipeline.

**Style notes.** Recurring theme: probability + fixed-income/options theory anchored to trading intuition; firm openly tells candidates what to study (Hull).

Sources: https://www.glassdoor.com/Interview/TransMarket-Group-Quantitative-Trader-Interview-Questions-EI_IE233421.0,17_KO18,37.htm ; https://www.wallstreetoasis.com/company/transmarket-group/interview ; https://www.transmarketgroup.com/quantitative-trading-interview-prep ; https://www.coachquant.com/transmarket-group

---

## 11. 3Red Partners (Chicago prop)

**Pipeline.** HR phone call → Zoom with traders → **take-home coding challenge** → Zoom with quant researchers → onsite. Avg ~33 days; difficulty 3/5; SWE rated hardest, Junior Quant Trader and FPGA Engineer easiest.

**Reported questions.**
- Low-level/Python internals **[SWE/QD]**: language-specific questions; "very specific data-structures questions"; **algorithm questions about numpy internals** (how numpy works under the hood).
- DS&A **[SWE/QD]**: general data-structures & algorithms rounds.
- Math **[QT]**: mental math and brainteasers alongside background/experience.
- Take-home **[SWE/QD]**: coding challenge (contents not publicly specified — thin).

**Style notes.** Theme: deep Python/numpy internals + DS&A, take-home before research rounds. Stack cited: Python, C++, Java; numpy/pandas.

Sources: https://www.glassdoor.com/Interview/3Red-Partners-Interview-Questions-E923555.htm ; https://www.glassdoor.com/Interview/3Red-Partners-Algo-Trading-Interview-Questions-EI_IE923555.0,13_KO14,26.htm ; https://scoutify.com/companies/3red-partners

---

## 12. Gelber Group (Chicago prop)

**Pipeline.** **[QT] [FT & junior]**: HR screen → 2 phone rounds with traders (behavioral + math/probability/coding) → **superday of ~5 interviews**; a technical round where candidates **present a technical project to an algo trader**. **[SWE/technical] [INTERN]**: coding round of **two LeetCode-medium problems in 45 minutes** at a fast pace, short behavioral at the end (Software Engineer Intern – Technical Operations reports).

**Reported questions.**
- Coding **[SWE] [INTERN]**: 2 LC-medium in 45 min (titles not reported).
- Probability/stats **[QT]**: mostly statistics + basic trading questions; probability brainteasers (specific dice-question texts not confirmed for Gelber — thin).
- Behavioral (recurring, trader track): "What is your edge as a trader?", "What kind of risk taker are you?", why trading / why Gelber, greatest failure, strengths/weaknesses.
- Python for data analysis cited as a plus in trader hiring.

**Style notes.** Fit-heavy trader pipeline ("mostly fit, nothing too technical" per WSO), with a project-presentation twist; light-medium coding bar for technical interns.

Sources: https://www.glassdoor.com/Interview/Gelber-Group-Junior-Trader-Interview-Questions-EI_IE18651.0,12_KO13,26.htm ; https://www.wallstreetoasis.com/company/gelber-group/interview ; https://www.interviewsense.org/opportunities/gelber-group-software-engineer-intern-technical-operations-team-chicago/

---

## 13. Wintermute (London, crypto MM) — best-documented crypto pipeline

**Pipeline (Graduate/Intern Algorithmic Trader; also used for algo-trading interns) [QT] [INTERN & FT-grad]:**
1. Online pre-screening: general **IQ test, pattern recognition, short-term-memory** assessment (40–45 min);
2. **Coding test up to 3 hours** (Python; requires real programming experience to pass);
3. **DeFi take-home task**: a list of technical + non-technical questions about DeFi, several days to complete, googling allowed;
4. Onsite/virtual: **1-hour written test, 5 problems** — math about crypto protocols + probability (deliberately overloaded: one highly-math-educated candidate reported finishing less than 1 problem);
5. 40-min interview with 2 traders.

**Reported questions.**
- Probability/math **[QT]**: the 5-problem written test (crypto-protocol math + probability); market-making questions that go beyond standard prep — e.g. **model the distribution of volumes in an order book**.
- Coding **[SWE/QD]**: medium-hard algorithm problems with crypto/market-data flavour — e.g. **parse and aggregate order-book updates while handling malformed messages** and keeping performance as feed volume grows (techinterview.org guide).
- System design **[SWE] [FT]**: design **multi-venue trading systems**; handle dozens of exchange connections; "what happens when one venue stalls?" — latency-critical architecture.
- There is also a **trading-system-design written exercise** for graduate algo traders (leaked "Wintermute System Design Interview" PDF on CourseHero).

**Style notes.** Recurring themes: psychometric + endurance testing, Python, order-book/market-microstructure math, DeFi literacy. Difficulty deliberately above completable level on the written test.

Sources: https://www.glassdoor.com/Interview/Wintermute-DeFi-Algorithmic-trader-Interview-Questions-EI_IE4841121.0,10_KO11,34.htm ; https://www.techinterview.org/companies/wintermute-interview-guide/ ; https://mirror.xyz/0x92Ec6e838Dd90845D7D34Dfaa82d6D00f66C8168/gpwDVp5JLrpiEDIyl113leJpIjA_zV_Z5FAe8TVXyOI ; https://www.coursehero.com/file/103964662/Wintermute-System-Design-Interview-virtualpdf/

---

## 14. GSR (crypto MM)

**Pipeline (Trading Internship, Singapore, report dated Aug 2024) [QT] [INTERN]:**
1. **90-min Python coding test on CoderPad**: 2 LeetCode-hard + 5 LeetCode-easy + Python MCQs;
2. 60-min interview on mathematical/logical reasoning — **probability brainteasers, dice and coin-flipping**;
3. 60-min **pair-coding** round: **DataFrames/pandas, search algorithms, OOP concepts**;
4. Final with senior trading managers.
Separately, a graduate-program OA on the **Correlation One platform** was reported: **45 min, 20 questions**, moderate-to-high difficulty, described as "very difficult."

**Reported question categories.** Arrays/algorithms (LC easy–hard mix); data manipulation (pandas); probability-to-reasoning (dice/coins); OOP design discussion. FT quant-trader postings expect C++/Python, microstructure, ML/optimization, automated MM strategies.

**Style notes.** Heavier formal LC component than most crypto MMs; pandas/data-frame fluency explicitly tested.

Sources: https://www.glassdoor.com/Interview/GSR-Singapore-Trading-Internship-Interview-Questions-EI_IE4172238.0,13_KO14,32.htm ; https://www.1point3acres.com/interview/company/GSR%20Markets ; https://www.tradermath.org/practice/firms/gsr

---

## 15. B2C2 (London crypto MM)

**Pipeline.** Numerous remote interviews with different team members; Glassdoor difficulty only 2.7/5, 39% positive.

**Reported questions.**
- OOP basics **[SWE] [FT]**: inheritance and polymorphism questions ("some basic questions").
- Design/discussion **[QD/QT] [FT]**: interviews were "a series of discussions on **trading logic & system architecture** and vision on future projects" for trading-side roles.
- Ops/other: compliance knowledge; standard behaviorals ("where do you see yourself in 3–5 years").

**Style notes.** Evidence **thin**; what exists suggests conversational, architecture-and-experience-driven interviews rather than formal OAs or LC gauntlets. Quant Dev postings cover spot/CFD/futures/perps strategy building (Python).

Sources: https://www.glassdoor.com/Interview/B2C2-Interview-Questions-E1973538.htm ; https://web3.career/i/=UTN5UzN

---

## 16. Cumberland DRW (crypto arm of DRW)

**Pipeline.** Follows the DRW trading pipeline: probability + fast mental math + market-making games, then role-specific rounds; Cumberland adds crypto-specific depth. Interviews described as conversational with rigorous questions woven in (DRW's own blog on a fully-remote Cumberland analyst hire).

**Reported questions.**
- Probability/EV **[QT]**: quick estimation and expected-value questions; a **sequential-decision or trading game** round (DRW-standard).
- Crypto market structure **[QT] [FT]**: crypto market microstructure, **on-chain mechanics, DeFi protocols, OTC sales-trading dynamics** (techinterview.org DRW/Cumberland guide).
- Coding: no Cumberland-specific coding questions surfaced — dev hiring goes through general DRW engineering loops (evidence for Cumberland-specific SWE questions **thin**).

**Style notes.** Breadth across asset classes valued; crypto knowledge is the differentiator vs. plain DRW loops.

Sources: https://www.techinterview.org/companies/drw-interview-guide/ ; https://www.drw.com/updates/insights/nate-shares-his-experience-joining-cumberland-100-remotely ; https://www.quantt.co.uk/resources/drw-interview

---

## 17. Amber Group (HK/Singapore crypto)

**Pipeline.** Covers crypto-market knowledge, coding, quantitative reasoning; roles reported: Quant Researcher, SDE, Blockchain Developer.

**Reported questions.**
- Low-level/C++ + code quality **[SWE/QD] [FT]**: **4–5 C++ problems in 2 hours, live-monitored** — explicitly *not* LeetCode-style puzzle solving; graded on **maintainable, readable code** and coding habits (Glassdoor/NodeFlair reports).
- Probability + brainteasers **[QT/QR]**: reported as standard components alongside crypto-market knowledge.

**Style notes.** Distinctive emphasis on code craftsmanship over algorithmic trickiness. Specific problem texts not public — moderate-thin evidence.

Sources: https://www.glassdoor.co.in/Interview/Amber-Group-Interview-Questions-E4071678.htm ; https://nodeflair.com/companies/amber-group/interviews ; https://www.quantt.co.uk/quant-firms/amber-group

---

## Cross-firm recurring themes (this cohort)

1. **HackerRank/CoderPad OAs with LC easy–hard mixes** dominate SWE/QD screens (Peak6 90min/2Q; Walleye 120min/3Q or 180min/4Q; GSR 90min CoderPad; TransMarket HackerRank first-round).
2. **Order-book / matching-engine builds** appear as coding questions at options and crypto MMs (Volant matching-engine question; Wintermute order-book update parsing/aggregation; Wintermute multi-venue system design).
3. **C++ code-quality rounds** (not puzzles) at Valkyrie, Volant, Amber — design, containers, readability, style.
4. **Practical data engineering** (SQL, APIs, pandas/numpy internals, rolling computations) at multistrats: Walleye, Jain Global, 3Red, GSR.
5. **Trader tracks stay math-first**: mental math + EV games (Group One, Gelber, TransMarket, Cumberland DRW), escalating to modeling questions (Wintermute order-book volume distributions; CFM binomial tree/Newton/PCA).
6. **Thin-evidence firms** (few or single public reports): Freestone Grove, Seven Eight Capital, B2C2, Jain Global (young), Cumberland-specific SWE, CFM dev-track, Peak6 trader-track, TransMarket exact OA problems, 3Red take-home contents. Treat those sections as indicative, not comprehensive.
