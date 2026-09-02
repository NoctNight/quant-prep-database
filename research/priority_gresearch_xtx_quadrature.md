# Priority deep-dive: G-Research, XTX Markets, Quadrature Capital — interview pipelines & reported coding questions (2023–2026)

Compiled 2026-09-01. ~55 web searches + GitHub code/repo searches.

## 0. Read this first: evidence quality and environment limits

- **Access limits.** In this session the network egress proxy hard-blocked Glassdoor (all country domains), Blind, Reddit, TheStudentRoom, QuantNet, 1point3acres, Hacker News, Medium/Substack, Wikipedia, Greenhouse job boards, and the three firms' own websites (gresearch.com, xtxmarkets.com, quadrature.ai), as well as prep sites (Quantt, Quant Blueprint, techinterview.org, Intervyo, Scoutify, Canary Wharfian, Dataford, Tradermath). Only GitHub was fetchable. **Everything from those blocked sources below comes from search-engine result snippets/summaries of the named pages, not from a full read of the page.** URLs are given so the user can open them directly; page-level text should be re-verified by the user.
- **Reliability tags used:** `[official]` = firm's own guidance/job posting; `[first-hand]` = a candidate report on Glassdoor/Blind/1point3acres/HN; `[prep]` = third-party prep site or aggregated guide (often unsourced, sometimes AI-generated); `[inferred]` = a prep-repo question explicitly self-labelled as inferred, NOT a reported question.
- **Concrete verbatim coding questions are scarce for all three firms.** All three run NDAs / discourage sharing; Quadrature candidates explicitly cite an NDA. Where a question is reported, the wording below is the reporter's paraphrase. Nothing here is invented; where a prep source clearly generated a question rather than reported it, it is labelled `[inferred]` and should not be treated as "asked at X".
- One popular GitHub repo (`ankitkushawaha1000/HFT`) has per-round "question banks" for all three firms. Its own README says every question is tagged `anecdotal` or `inferred` and that it is a self-built (possibly AI-assisted) study aid. Its G-Research "Round 1 psychometric test" does not match any official or first-hand description and is likely wrong. I list its content only where it is tagged anecdotal, and label the source.

---

## 1. G-Research (London; also NYC/Paris/Austin/Dallas)

### 1.1 Role families and tracks
- **Quantitative Researcher (QR) / Machine Learning Researcher** — full-time (postgraduate/experienced) and **Quant Research internship** (summer, PhD/Masters/strong undergrad). ML Researcher and "Quantitative Analyst Researcher" are rated hardest on Glassdoor.
- **Software Engineer / Quant Platform engineer / ML Engineer / Research Engineer** — full-time and **Software Engineering internships** (Platform, Research Engineering, Architecture & Innovation, Office of the CTO, AI Engineering intern). Stack: C#/.NET historically dominant, plus C++, Python, F#; heavy Kubernetes/Linux platform work (G-Research OSS: Armada, helm charts, F# guidelines).
- **Quant trader:** G-Research does not run a discretionary trading desk and does not advertise "quant trader" roles; the closest is Quantitative Analyst. No trader-track interview evidence exists.

### 1.2 Pipeline — Quantitative Research (full-time) `[official + first-hand]`
Sources: G-Research assessment-process PDFs (2020 v1, 2022 v3, July-2025 "Quantitative research and machine learning interview prep – assessment process" and "– recommended reading"), career-guide page "Quantitative Researcher Interview Questions", Glassdoor QR pages, techinterview.org write-up (prep, but consistent with first-hand).
- https://www.gresearch.com/wp-content/uploads/2025/07/Quantitative-research-and-machine-learning-interview-prep-assessment-process.pdf
- https://www.gresearch.com/wp-content/uploads/2025/07/Quantitative-research-and-machine-learning-interview-prep-recommended-reading.pdf
- https://www.gresearch.com/wp-content/uploads/2022/12/Quantitative-Researcher-Assessment-process-guidance-v3.pdf
- https://www.gresearch.com/career-guides/quantitative-researcher-interview-questions/
- https://www.glassdoor.com/Interview/G-Research-Quantitative-Researcher-Interview-Questions-EI_IE297747.0,10_KO11,34.htm
- https://www.techinterview.org/post/3233477268/g-research-interview-quiz-quant/

1. **Online "Quant Quiz"** `[official]`. Two variants: a *general quantitative aptitude* quiz or an *ML-specific* quiz, chosen by G-Research based on your background. Official topics: probability, statistics (incl. OLS), linear algebra, calculus (esp. differential equations), programming, finance. Official line: it "assesses basic skills more than advanced mathematics". Format details vary by source/era:
   - 2020/2022 official guidance: 8 questions in Part A + a choice of 6 in Part B, 90 minutes, 15/25 marks to pass `[official, older]`.
   - Dec-2025 Glassdoor review and 2025 techinterview write-up: **10 multiple-choice questions, 5 options each, 90 minutes** `[first-hand + prep]`. A reviewer noted "questions that required actual math knowledge such as finding minimizer functions of cost functions" (i.e., derive the minimiser of a given loss — an OLS/convex-optimisation style item).
   - Jan-2024 Glassdoor review: "two-hour online test on stats, probability and computer-science basics" then an online interview `[first-hand]`.
   - Time-management failure mode reported: candidates "run out of time because they treat every question as equal and grind the first hard one for twenty-five minutes" `[prep]`.
   - G-Research publishes practice questions ("G-Research Example Questions" PDF, mirrored on CliffsNotes https://www.cliffsnotes.com/study-notes/28095361 and Scribd https://www.scribd.com/document/701685858/Quant-Research-Preparation) — the user should download these; they are the only official sample of quiz style.
2. **Triage interview** (1 hour, with a working quant) `[official + first-hand]`. Described by a candidate as "more challenging than the online assessment and comparable to the sample quant exam"; covers probability theory and machine learning. Official guidance: G-Research's own sample-exam questions ("Stefanica, Radoicic & Wang"-level) are "closer to the level of our triage interview questions than of our quiz questions".
3. **Technical interviews** — typically **3–4 × 1 hour**: one in-depth mathematics interview plus two subjects chosen from programming / statistics / machine learning / finance `[official]`. A candidate describes them as "3 interviews with group heads — one on ML, one on stats, one on engineering" `[first-hand]`. "All interviews are technical, and cover areas from probability brainteaser, statistical estimations, machine learning methods, to algorithmic complexity" `[first-hand, Glassdoor]`.
4. **Management and senior-management interviews** (team fit, motivation) `[official]`.
- Timeline: Glassdoor average ~21–23 days; official says "one to two weeks" for the intern version.
- Reported difficulty 3.45/5 company-wide; QR/ML Researcher rated hardest.

### 1.3 Pipeline — Quant Research internship `[official + first-hand]`
- Official (Bright Network / gresearch.com/graduates): **four stages, 1–2 weeks**: online quantitative aptitude test → technical interviews → final interview with a functional lead.
- Glassdoor "Quant Research Intern" (rated 3/5, 50% positive, ~21 days): "math/ML online assessment followed by 3 technical rounds, covering ML, statistics, probability, coding, and brainteasers, with a challenging but fair focus on fundamentals"; another: "online assessment, then a technical interview, then three mentor interviews, and a final interview"; another: "online assessment covering mostly probability and statistics, followed by three interviews in one day, all covering probability, stats, and brainteasers"; questions "cover motivation and background, a variety of concrete stats/maths/probability questions, and bigger-picture questions about how one might use these tools for trading" `[first-hand]`.
  - https://www.glassdoor.com/Interview/G-Research-Quant-Research-Intern-Interview-Questions-EI_IE297747.0,10_KO11,32.htm
  - https://www.glassdoor.com/Interview/G-Research-Quantitative-Researcher-Intern-Interview-Questions-EI_IE297747.0,10_KO11,41.htm
  - https://www.glassdoor.com/Interview/G-Research-Intern-Interview-Questions-EI_IE297747.0,10_KO11,17.htm
- **Intern vs full-time difference:** same quiz gate; interns get fewer/shorter technical rounds compressed into one day, more emphasis on fundamentals and "how would you use this for trading" reasoning, and mentor interviews instead of group-head/senior-management rounds. Official tip for interns: be honest about what you don't know rather than bluffing.

### 1.4 Pipeline — Software / Quant Platform engineering (full-time) `[official + first-hand]`
- **Official "What to expect from a Quant Platform Software Engineering interview"** (gresearch.com/news, mirrored on Gradcracker):
  - https://www.gresearch.com/news/what-to-expect-from-a-quant-platform-software-engineering-interview/
  - https://www.gradcracker.com/hub/347/g-research/blogs/2449/what-to-expect-from-a-quant-platform-software-engineering-interview
  - Stage 1 is a **take-home "homework"**: a **single question that should take about two hours**; any language/tools ("we mostly work in C#, but we don't require you to know it"); it "aims to most accurately reflect how software is written in the real world". The rest of the process is shortened to compensate.
  - If successful: remaining interviews **face-to-face, either two half-days or one full day** (candidate's choice).
- Generic official engineering pipeline (gresearch.com career pages): online application → Stage 1 technical (meet a team member **or** a remote technical test) → Stage 2 behavioural → Stage 3 further technical interviews → Stage 4 management interviews.
- Glassdoor Software Engineer (55 reviews, 45 questions, difficulty 3.3/5, 46% positive, ~15 days):
  - "recruiter screen, a technical screen with easy Python questions and topics like 'name 3 data structures', followed by three rounds of technical interviews" `[first-hand]`.
  - "mostly algorithmic questions to be solved on a whiteboard" `[first-hand]`.
  - "a test beforehand, with 2–3 parts depending on team and pretty in-depth topics" `[first-hand]`.
  - **"One interview focused on improving the performance of a bit of code by only looking at the logs"** `[first-hand]` — a distinctive G-Research round (performance diagnosis from logs, no source access).
  - Oct-2024: "received an online assessment … fairly easy but got rejected even after passing all test cases" `[first-hand]` — implies the OA is graded on code quality/approach, not just tests.
  - 2024–25 reviews mention **2 coding rounds** and questions on **Kubernetes and Ansible** for platform/infra-flavoured roles `[first-hand]`.
  - Hacker News (2018, older): "online automated coding test with straightforward questions including SQL" `[first-hand, dated]` https://news.ycombinator.com/item?id=18502116
  - https://www.glassdoor.co.uk/Interview/G-Research-Software-Engineer-Interview-Questions-EI_IE297747.0,10_KO11,28.htm
- **ML Engineer** (Glassdoor, 2 reviews, 3/5): "online test combining mathematics, probability and machine-learning questions, followed by a triage interview"; questions on **autoregressive models, attention mechanisms, memory-optimisation tricks** `[first-hand]`. https://www.glassdoor.co.uk/Interview/G-Research-Machine-Learning-Engineer-Interview-Questions-EI_IE297747.0,10_KO11,36.htm
- Blind: a "Quant Engineer" final-round candidate mentions a **90-minute assessment** gate for engineering-adjacent quant roles too `[first-hand]`. https://www.teamblind.com/post/How-about-G-Research-4EZdTeNn

### 1.5 Pipeline — Software Engineering internships `[official + first-hand]`
- Official (Bright Network listings 2023/2025; gresearch.com/graduates): **three stages, 1–2 weeks**: online application/CV review → **online skills (coding) test** → **assessment centre** followed by **mentor interviews** exploring technical and behavioural competencies. 2023 cycle assessment-centre dates: 5 Oct, 24 Oct, 15 Nov, 23 Nov, 7 Dec (i.e., rolling autumn hiring; apply Sept).
  - https://www.brightnetwork.co.uk/graduate-jobs/g-research/software-engineering-internship-platform-london-2025
  - https://www.brightnetwork.co.uk/graduate-jobs/g-research/software-engineering-internship-research-engineering-london-2025
- Glassdoor: "received the online coding assessment a few days after CV submission, and interview offers a few days after completing the coding assessment" `[first-hand]`.
- **Intern vs full-time (engineering):** interns get an automated OA + assessment centre (group/individual exercises + mentor interviews); full-time gets a 2-hour take-home + full/half-day onsite with 3 technical rounds incl. the logs/performance round and management interviews.

### 1.6 Concrete reported questions — G-Research
| # | Question (as reported) | Category | Role / track | Year | Source | Reliability |
|---|---|---|---|---|---|---|
| 1 | Quiz item: find the minimiser of a given cost function (derive argmin) | prob/stats-to-maths | QR FT | Dec 2025 | Glassdoor QR page | first-hand |
| 2 | Quiz: 10 MCQ, 5 options, 90 min; topics probability, stats/OLS, linear algebra, ODEs, programming, finance | quiz format | QR FT/intern | 2025 | Glassdoor + techinterview.org | first-hand + prep |
| 3 | "Improve the performance of a bit of code by only looking at the logs" | low-level/systems/perf | SWE FT | ~2023–24 | Glassdoor SWE page | first-hand |
| 4 | Technical screen: "name 3 data structures", easy Python questions | arrays/strings basics | SWE FT | 2024 | Glassdoor SWE | first-hand |
| 5 | Whiteboard algorithm questions (unspecified) in 3 technical rounds | algorithms | SWE FT | 2023–25 | Glassdoor SWE | first-hand |
| 6 | Kubernetes / Ansible questions | systems/infra | SWE (platform) FT | 2024–25 | Glassdoor SWE | first-hand |
| 7 | Online OA with test cases (passed all, still rejected) | OA | SWE FT | Oct 2024 | Glassdoor SWE | first-hand |
| 8 | Autoregressive models; attention mechanisms; memory-optimisation tricks | ML-to-code / systems | ML Engineer FT | 2024 | Glassdoor MLE | first-hand |
| 9 | Probability brainteasers, statistical estimation, ML methods, algorithmic complexity | prob/stats, algorithms | QR intern/FT | 2023–25 | Glassdoor QR intern | first-hand |
| 10 | "How might you use these tools for trading" big-picture questions | design/reasoning | QR intern | 2024 | Glassdoor QR intern | first-hand |
| 11 | SQL in the automated coding test | data manipulation | SWE FT | 2018 | Hacker News | first-hand (dated) |
| 12 | Take-home: single ~2-hour question, any language | take-home | Quant Platform SWE FT | 2021–25 | gresearch.com blog | official |
| 13 | Merged Poisson processes rate (given n independent Poisson processes, rate of merged process) | probability | "SWE technical" | n/a | ankitkushawaha1000/HFT (tagged anecdotal) | prep, unverified |
| 14 | LRU cache; streaming median in O(log n) | design / heaps | "coding test" | n/a | ankitkushawaha1000/HFT (tagged anecdotal) | prep, unverified |

Categorisation summary (G-Research): **prob/stats-to-maths dominates for QR** (quiz + triage + math interview); **coding for QR** is complexity/algorithms discussion rather than LeetCode grind; **SWE** = algorithms on whiteboard + a distinctive **performance-from-logs** round + platform/infra questions + a realistic take-home; **data manipulation/SQL** appeared in older automated tests; **no evidence of pair-programming or "design an ML pipeline" rounds** at G-Research specifically (ML topics appear in the ML-engineer track as knowledge questions).

### 1.7 What G-Research rewards / fail reasons
- Official recommended reading (July 2025 PDF): Grinold & Kahn *Active Portfolio Management* (first 4 chapters), undergraduate (year 1–2) probability/statistics for early rounds, and "prepare at most two weeks before the first round" `[official]`. Zhou's *Green Book* is cited by prep sources as the closest match for the brainteaser style; Stefanica/Radoicic/Wang (numerical methods heavier) for triage-level `[official-ish: G-Research says its own sample exam is at that level]`.
- Rewarded: "mathematics, probability, statistics, and code you can defend line by line"; clean derivations; being honest about gaps; communication/collaboration (official emphasises quants work side-by-side with engineers).
- Fail reasons seen: quiz time management; passing OA test cases but weak code quality; shallow C++/systems depth on platform roles; treating triage like the quiz (it is harder).

---

## 2. XTX Markets (London HQ; also NYC, Paris, Singapore, Mumbai, Yerevan)

### 2.1 Role families and tracks
- **Quantitative Researcher** (ML-first; "Junior Quantitative Researcher" is the new-grad title) and **Quant Research Summer Intern** (2025, 2026 cohorts). Also **XTY Labs AI Research (PhD) internship** (NYC).
- **Software Engineer** (C++ core/trading systems; also Python/Go platform; "Software Engineer (C++)", "Senior Software Engineer") and **Software Engineering Intern – Summer 2026** (London).
- **Trading-adjacent:** "Junior Quant Analyst" (NYC, 2026 new-grad) and "Quantitative Trading Intern"; "Trading Analyst (Crypto)" Singapore. No evidence of a classic discretionary quant-trader interview loop; treat these as QR-lite roles.
- Other internships with published process: Risk internship (10–12 weeks, 1 intern): shortlisted candidates get a **take-home test (~90 min) then 2 × 45-min interviews with the CRO/intern mentors** `[official, Greenhouse job 6688991003]`.
- Hiring scale (prep sources): ~30–50 researchers and engineers globally per year; OA pass rate "reportedly 5–10%" `[prep, unverified]`.

### 2.2 Pipeline — Quantitative Researcher (full-time / junior) `[official + first-hand + prep]`
Sources:
- https://www.glassdoor.com/Interview/XTX-Markets-Quantitative-Researcher-Interview-Questions-EI_IE2384243.0,11_KO12,35.htm (8 reviews, 3/5, 40% positive, ~50 days; reviews from Apr-2023, Sep-2023)
- https://www.glassdoor.com/Interview/XTX-Markets-Junior-Quantitative-Researcher-Interview-Questions-EI_IE2384243.0,11_KO12,42.htm
- Junior QR job posting (Armenia/Yerevan office; Greenhouse 7524152003, mirrored on LinkedIn/Tradermath/BuiltIn) `[official]`
- Blind threads: https://www.teamblind.com/post/Interview-at-XTX-markets-dYCZ6QTn , https://www.teamblind.com/post/onsite-interview-with-xtx-markets-zi2ovdsg , https://www.teamblind.com/post/Interviewing-at-XTX-markets-V3wi5nES
- Prep: https://www.quantt.co.uk/resources/xtx-markets-interview , https://www.quantblueprint.com/guides/how-to-get-a-job-at-xtx-markets , https://www.techinterview.org/companies/xtx-markets-interview-guide/

1. **Online test** `[official, from the Junior QR posting]`: "The test contains **20 questions (problems and/or equations)** on: **probability theory, linear algebra, calculus, algorithms, brainteasers**. Limited to **60 minutes** after launch. Administered through **TestGorilla**. Once the test starts you cannot go back to skipped/completed questions." (Note: this exact spec is from the Yerevan Junior QR posting; London QR/intern OAs are described by prep sources as "a combined ML and probability test of similar length, often with a small data-analysis component", 90–120 min `[prep]`.)
2. **4–5 interviews (phone/video/onsite) with quant researchers** "that involve questions and problems on the above topics" `[official]`. Prep sources: initial 45–60 min call with a researcher covering background + technical questions; a 60-min call with "ML and statistics discussion for researchers".
3. **Take-home / project** `[first-hand, Blind]`: one Blind poster describes "standard quant interviews covering ML and math, followed by a **very hard take-home project (Kaggle-style with 3 submission attempts)**, and if you pass, a **10-round onsite spanning 2 days**". Prep sources corroborate "a take-home problem involving data analysis, model building, or theoretical ML questions".
4. **Onsite**: 5–6 interviews in a single day (45–60 min each) in London with working researchers/engineers, "HR plays a minimal role"; includes whiteboard derivations; final conversation with senior leadership/team lead on research direction and fit `[prep, consistent with first-hand]`.
- Style `[first-hand, Blind]`: "questions are standard without stupid IQ tests or custom questions, but coverage is broad requiring solid knowledge across all areas, with a couple of bad answers in any round resulting in rejection." Interviewers "actually quite nice", "provide ample preparation material", process "well administered" `[first-hand, Glassdoor]`. XTX's stated philosophy (via prep sites quoting recruiters): "get a broad signal … successful candidates are strong in all areas and exceed expectations in at least one."
- Older (10 yrs ago) Blind quant report: "actual maths and physics puzzles like in college … among the hardest set of interviews" `[first-hand, dated]`.

### 2.3 Pipeline — Quant Research Summer Intern `[official + prep]`
- Posting (Quant Blueprint mirror, 2025/2026): the QR team "designs the statistical models … deploying state-of-the-art machine learning techniques to generate price forecasts". No official stage list in the snippet. Prep sites describe the same shape as full-time but shorter: OA (ML+probability, small data-analysis component) → 1–2 researcher video interviews → possibly a take-home → shorter final round. Expect Python depth checks ("numpy broadcasting internals, pandas memory layout, vectorisation") `[prep]`.
- Risk internship gives the concrete official template for intern loops: ~90-min take-home + 2 × 45-min interviews.
- **Intern vs full-time:** interns are not reported to face the 10-round two-day onsite; full-time QR has more rounds, a harder Kaggle-style project, and leadership round. Evidence for the London intern loop is thin — mark as *partly inferred*.

### 2.4 Pipeline — Software Engineer (full-time) `[first-hand + official]`
Sources:
- https://www.glassdoor.co.uk/Interview/XTX-Markets-Software-Engineer-Interview-Questions-EI_IE2384243.0,11_KO12,29.htm
- https://www.glassdoor.com/Interview/XTX-Markets-Interview-Questions-E2384243.htm?filter.jobTitleExact=Software+Engineer+(C%2B%2B)
- https://www.glassdoor.com/Interview/leetcode-hard-questions-were-asked-QTN_7991920.htm
- https://www.glassdoor.com/Interview/Questions-around-CV-and-coding-question-QTN_8065613.htm
- https://www.teamblind.com/post/xtx-markets-interview-experience-6tizwwo2 ; https://www.teamblind.com/post/XTX-Markets-interview-experience-k54fOeeH
- 1point3acres: https://www.1point3acres.com/bbs/thread-949252-1-1.html (London onsite invite "including coding and system design")

Reported loop variants (all first-hand):
- **Variant A (C++ dev):** "phone interview → **coding task (for one evening)** → conversation with team lead → another phone interview → **5 × 1:1 onsite interviews, ~1 hour each, all technical**."
- **Variant B:** "phone screening about past experience and knowledge of writing low-latency code → **take-home test** → **5 hours of on-site interviews with Google-style questions**."
- **Variant C (senior):** "**~30-minute voice-only phone screen with ~20 rapid-fire questions on C++, compiler and OS architecture** — fast-paced, no time to think." Topics named: **RAII, pointers, memory alignment, vtable/virtual functions, variadic templates, std::map vs unordered_map implementation, hash functions, floating-point numbers, cache architecture**; also **atomic data structures, system-call overheads, modern C++ features**.
- **Variant D (Blind SWE write-up):** "phone screen relatively easy; **take-home was a lot of fun**; onsite day: **a few LeetCode-hard problems and pretty standard system design**, plus domain-knowledge questions depending on role. Probably the hardest tech interview overall but not crazy — slightly harder than FAANG and other HFTs." Got an offer.
- **Variant E (rejection):** "three technical interviews and a **technical assignment to design and build a simple system**; rejected four weeks later with feedback that **the system was too simple and should have addressed a number of other factors**" — i.e., the take-home is graded on robustness/edge-cases/observability, not minimal correctness.
- "Coding tests are sometimes included in manager interviews."
- Glassdoor firm-wide: difficulty 3.42/5, 50% positive, ~41 days.
- Prep-source additions `[prep]`: HackerRank-style timed OA 60–90 min for engineers (or "2–3 hard algorithmic problems in 90–120 min"); "depth over breadth — interviewers pick one or two areas and probe to the limit"; recommended prep "100 LeetCode hards with a strict time budget", *Effective Modern C++*, *C++ Concurrency in Action*.
- Languages: C++ essentially required for core engineering; Python for research; Go is used for some platform work (XTX is listed among Go users; github.com/XTXMarkets).

### 2.5 Pipeline — Software Engineering Intern (Summer 2026) `[thin]`
- Posting exists on Greenhouse (London, opened ~Sep 2025). No first-hand intern SWE interview reports found. By analogy with the Risk-intern template and SWE full-time: expect OA/take-home (~90 min) + 2 short technical interviews. Mark as *inferred*.

### 2.6 Concrete reported questions — XTX
| # | Question (as reported) | Category | Role / track | Year | Source | Reliability |
|---|---|---|---|---|---|---|
| 1 | OA: 20 problems in 60 min on probability, linear algebra, calculus, algorithms, brainteasers (TestGorilla, no back-navigation) | quiz format | Junior QR (new-grad) | 2024–25 | Greenhouse/LinkedIn posting | official |
| 2 | Rapid-fire C++/OS: RAII, pointers, memory alignment, vtable & virtual functions, variadic templates, map vs unordered_map internals, hash functions, floating point, cache architecture | low-level/C++ | Senior SWE FT | 2023–25 | Glassdoor SSE | first-hand |
| 3 | Atomic data structures; system-call overheads; modern C++ features | low-level/C++ | C++ Developer FT | 2023–24 | Glassdoor | first-hand |
| 4 | "LeetCode hard questions were asked" (onsite) | algorithms (unspecified) | SWE FT | 2024–25 | Glassdoor QTN_7991920; Blind | first-hand |
| 5 | Standard system design (onsite) | design | SWE FT | 2024 | Blind | first-hand |
| 6 | Take-home: "design and build a simple system" (rejected as too simple) | take-home / design | SWE FT | 2024 | Glassdoor | first-hand |
| 7 | Take-home coding task "for one evening" | take-home | C++ SWE FT | 2023 | Glassdoor | first-hand |
| 8 | "Questions around CV and a coding question" (screen) | mixed | SWE | 2024 | Glassdoor QTN_8065613 | first-hand |
| 9 | Kaggle-style take-home with 3 submission attempts | take-home / data challenge | QR FT | 2024–25 | Blind | first-hand |
| 10 | "Tell me about a model you built that failed in production; what did you do?" | behavioural-technical (post-mortem rigour) | QR FT | 2025 | Glassdoor QR (via Quantt summary) | first-hand/prep |
| 11 | "Here's a dataset of market data. How would you build a model to predict short-term price movements?" — walk through formulation, method, pitfalls, evaluation | design-an-ML-pipeline | QR FT | 2025 | Quant Blueprint | prep |
| 12 | Explain bias-variance in detail; gradient boosting at the maths level; Bayesian NNs; when causal inference over correlation | ML theory | QR FT | 2025 | Quant Blueprint | prep |
| 13 | numpy broadcasting internals, pandas memory layout, vectorisation | data manipulation (Python depth) | QR intern/FT | 2025 | Quant Blueprint | prep |
| 14 | Risk intern: ~90-min take-home + 2 × 45-min interviews | take-home | Risk intern | 2026 | Greenhouse 6688991003 | official |
| 15 | Order book with O(1) best bid/ask; deque/list/vector cache trade-offs; shared_ptr cost; market-data normalisation design; overfitting in backtests; multiple-comparisons with 100 signals; derive OLS/BLUE | various | SWE/QR | n/a | ankitkushawaha1000/HFT | **inferred by prep repo — not reported** |

Categorisation summary (XTX): **low-level/systems/C++** is the single biggest bucket for engineers (rapid-fire trivia + deep probing), then **algorithms (LeetCode-hard)**, **design/system design** and a **take-home build** graded harshly. For researchers: **probability/linear algebra/calculus/brainteasers** in the OA, **ML theory from first principles** (implement/derive, not library calls), a **Kaggle-style data challenge**, and "design an ML pipeline"-style discussion. Whiteboard derivations expected.

### 2.7 What XTX rewards / fail reasons
- Rewards: breadth *and* depth ("strong in all areas, exceptional in one"); production-quality code even for researchers; post-mortem honesty; systems that handle "other factors" (failure modes, scale, monitoring) not just the happy path.
- Fail reasons: "a couple of bad answers in any round" → reject; too-simple take-home; not knowing C++/OS internals cold at phone-screen speed; OA time pressure (20 in 60, no backtracking).
- Official reading (via prep sites quoting XTX prep material): *Elements of Statistical Learning* ch. 1–9 for researchers.

---

## 3. Quadrature Capital (London, 122 Leadenhall St; ~US$8.4bn AUM, ~2026)

### 3.1 Role families and tracks
- **Quant Developer** — Quadrature's unified title for "software engineers and mathematical researchers who are strong programmers"; sub-tracks **Quant Developer – Research** and **Quant Developer – Technology**. Also **Core Technology** (Systems Engineering, Platform Engineering) and Software Engineer titles.
- **Internships:** 11-week summer programme for undergrads/postgrads across Quant Development (Research & Technology) and Core Technology; **hiring window Sept–Dec each year** (the intern programme "runs Sep–Jan only") `[official, quadrature.ai/careers/internships]`. Glassdoor titles: "Quantitative Developer Intern", "Software Engineer Internship", "Software Developer Internship".
- **No quant-researcher-only or quant-trader track**; research is inside Quant Developer. Also runs the "Fullhouse Hackathon" (2026, poker-bot competition) as an outreach/talent funnel (GitHub: advitrocks9/fullhouse-bot).
- Levels.fyi lists SWE intern pay ~$117/hr equivalent (London).

### 3.2 Official process — "How we hire" `[official, snippets]`
- https://www.quadrature.ai/careers/how-we-hire/ (also /careers/recruitment)
- Initial informal call (background + explain the process) → **invited into the London office for a morning or afternoon of face-to-face interviews, meeting 2–3 people from the team to work through technical or case-study questions** — "you work with your interviewer to solve these problems, with the interviewer there to guide and brainstorm" → if that goes well, **invited back to meet a few more people, ending with the CEO**.
- Talent acquisition "screens thousands of CVs per cycle, most read in under 30 seconds" `[prep, Intervyo]`.

### 3.3 Reported pipeline — Quant Developer (full-time) `[first-hand]`
Sources:
- https://www.glassdoor.com/Interview/Quadrature-Interview-Questions-E1013879.htm (company-wide: ~24 questions, difficulty 3.2–3.25/5, 40–50% positive, ~35–49 days avg)
- https://www.glassdoor.ca/Interview/Quadrature-Capital-Quant-Developer-Interview-Questions-EI_IE1013879.0,18_KO19,34.htm
- https://www.glassdoor.com/Interview/Quadrature-Quantitative-Developer-Interview-Questions-EI_IE1013879.0,10_KO11,33.htm
- Blind: https://www.teamblind.com/post/Quadrature-Capital-Quant-Dev-onsite-interview-sPu8HeXx , https://www.teamblind.com/post/quadrature-onsites-nZxGyWEK , https://www.teamblind.com/post/quadrature-capital-quant-dev-xsvfrlzk , https://www.teamblind.com/post/quadrature-capital-interview-uym1nwuq
- Reported loops:
  - "**Programming task that took 8 hours**, followed by a 15-minute HR call about CV" (take-home first) `[first-hand, Glassdoor QD]`.
  - "**Online task at home, then 3 onsite interviews in one day (1 hour each), then another day with 2 interviews with directors — all technical**" `[first-hand, Glassdoor QD]`.
  - "**Take-home Python challenge that everyone has to complete, followed by 1-1 interviews with fundamental problems**" `[first-hand, Glassdoor]`.
  - Blind "Quadrature onsites": "**2 LeetCode-type interviews with a big focus on runtime analysis and one system design**; LC medium for the first question, hard for the second; no extra questions about fundamentals" `[first-hand]`.
  - Blind quant-dev onsite: "**two-on-one** tech interview that started with a simple problem statement and continued with **ever-shifting requirements**" `[first-hand]` — i.e., an evolving-spec coding/design exercise.
  - "Coding assessment → behavioural and aptitude interview → general interview"; "multiple interviews in one day with engineers and senior management" `[first-hand]`.
  - Many reviewers: "there's an **NDA** so can't disclose too much" `[first-hand]`.
- Languages: Python (take-home) and C++; interviews mix "algorithms and data-structure questions; simple math problems (even if you're pure dev); simple coding/programming-language questions; questions on past experience" `[first-hand]`.

### 3.4 Reported pipeline — Internships (Quant Dev / SWE) `[first-hand + official]`
- Glassdoor: Quantitative Developer Intern had the *quickest* process (~21 days); Software Engineer Internship the *slowest* (~49 days). SWE-internship rated both "hardest" and "easiest" by different reviewers.
- "Skills test and phone interview" ; "**four interviews consisting of algorithmic and implementation questions; no specific questions on finance background**" `[first-hand, SWE internship]`.
  - https://www.glassdoor.com/Interview/Quadrature-Software-Engineer-Internship-Interview-Questions-EI_IE1013879.0,10_KO11,39.htm
  - https://www.glassdoor.com/Interview/Quadrature-Software-Developer-Internship-Interview-Questions-EI_IE1013879.0,10_KO11,40.htm
- Blind: intern candidate "has a tech interview and assessment coming up for the Quant Dev intern role; information hard to find online" `[first-hand, confirms OA + interview for interns]`.
- **Intern vs full-time:** interns → OA/skills test + phone/video + up to 4 algorithm/implementation interviews (no finance knowledge expected, quicker turnaround for quant-dev interns); full-time → longer take-home (reports of 8 hours / "online task at home"), a 3-interview onsite, then a second day with directors/CEO, and more math/probability and system-design content.

### 3.5 Concrete reported questions — Quadrature
| # | Question (as reported) | Category | Role / track | Year | Source | Reliability |
|---|---|---|---|---|---|---|
| 1 | "Code up a **queue implementation of a streaming median estimator**" | design / heaps / streaming | Quant Dev FT | ~2023–24 | Glassdoor | first-hand |
| 2 | "**System design question regarding stock buying/selling**" | design/simulation | SWE internship | ~2023–24 | Glassdoor | first-hand |
| 3 | "**Binary search vs hash map: trade-offs depending on CPU cache**" | low-level/systems | SWE internship | ~2023–24 | Glassdoor | first-hand |
| 4 | "An implementation question related to trading" | design/simulation | SWE internship | ~2023–24 | Glassdoor | first-hand |
| 5 | "Tell briefly about one of your projects" | behavioural | SWE internship | ~2023–24 | Glassdoor | first-hand |
| 6 | Return-rate calculations: simple day-to-day; with a dividend; when two companies merge | prob/stats-to-code (finance arithmetic) | Quant Dev FT | ~2022–24 | Glassdoor QD | first-hand |
| 7 | "Questions on the test to identify arbitrage opportunities" (discussion of the take-home) | take-home / data | Quant Dev FT | ~2022–24 | Glassdoor QD | first-hand |
| 8 | Poker: probability of a royal flush; combinatorial counting "to test maths and programming" | math puzzles coded / probability | Quant Dev FT | ~2022–24 | Glassdoor QD | first-hand |
| 9 | 2 × LC-style (medium then hard) with heavy runtime-analysis focus + 1 system design | algorithms + design | Quant Dev FT onsite | ~2024 | Blind | first-hand |
| 10 | Two-on-one problem with ever-shifting requirements | design/OOP/simulation (evolving spec) | Quant Dev FT | ~2024–25 | Blind | first-hand |
| 11 | 8-hour programming task; "take-home Python challenge everyone completes" | take-home | Quant Dev FT | 2023–25 | Glassdoor | first-hand |
| 12 | Merge overlapping intervals; expected dice rolls to see all six faces; median of a stream | arrays / probability / heaps | Quant Dev | n/a | ankitkushawaha1000/HFT (tagged anecdotal, "Blind search") | prep, unverified |
| 13 | Rotated sorted array search; quicksort worst case; process vs thread | arrays / systems | Quant Dev screen | n/a | ankitkushawaha1000/HFT (anecdotal/general-prep) | prep, unverified |
| 14 | OA topic areas: DP/memoisation; BFS/DFS/shortest path; numerical computation (e.g., sqrt, random-process simulation) | recursion/DP, graphs, numerical | Quant Dev OA | n/a | ankitkushawaha1000/HFT + pushpa-kumar/placement-prep (anecdotal) | prep, unverified |

Categorisation summary (Quadrature): **design/OOP/simulation** (trading-flavoured: order flow, buy/sell system, evolving requirements) and **streaming data structures** (median) are the signature; **algorithms with rigorous runtime analysis** (LC medium→hard); **low-level cache awareness**; **light probability/combinatorics** even for pure devs; a **substantial Python take-home** (data/arbitrage flavoured) for full-time.

### 3.6 What Quadrature rewards / fail reasons
- Rewards: collaborative problem-solving ("work with your interviewer … guide and brainstorm"), clear complexity analysis, adapting cleanly to changing requirements, clean Python/C++.
- Fail reasons: weak runtime analysis; over-engineering or freezing when requirements shift; slow full-time turnaround (35–49 days) leads some to drop; strict NDA means little public prep signal — expect to be surprised by format.
- Evidence is thinner than for G-Research/XTX: ~6–24 Glassdoor reports total, a handful of Blind threads, no TheStudentRoom/1point3acres reports found.

---

## 4. Cross-firm comparison

| Dimension | G-Research | XTX Markets | Quadrature |
|---|---|---|---|
| Gate | 90-min Quant Quiz (10 MCQ; older 8+6 format) for QR/ML; automated coding OA for SWE interns; 2-h take-home for platform SWE FT | TestGorilla 20-Q/60-min maths+algo test (Junior QR); HackerRank-style/take-home for SWE; ~90-min take-home for interns | Take-home Python task (up to ~8 h reported) for FT; skills test/OA for interns |
| Rounds after gate | Triage (1 h) + 3–4 × 1 h technical (maths + 2 of prog/stats/ML/finance) + management | 4–5 researcher interviews; SWE: phone screen(s) + 5 × 1 h onsite; some report Kaggle-style project + 10-round/2-day onsite | Informal call → half-day onsite (2–3 people) → second day incl. directors/CEO |
| Coding style | Whiteboard algorithms; performance-from-logs; C#/C++/Python/K8s | LeetCode-hard + system design; rapid-fire C++/OS trivia; take-home graded for robustness | LC medium→hard with runtime analysis; streaming/heaps; trading simulation; evolving-spec pair exercise |
| Maths style | Probability/stat brainteasers, OLS, ODEs, derivations | Probability/LA/calculus/brainteasers; ML from first principles; whiteboard derivations | Light: returns arithmetic, poker combinatorics, expected values |
| Take-home | Yes (SWE platform, ~2 h) | Yes (SWE evening task / design-and-build; QR Kaggle-style) | Yes (Python, long) |
| Pair programming | Not reported | Not reported (interviews are technical 1:1s) | Yes-ish: collaborative "work with your interviewer"; two-on-one evolving problem |
| "Design an ML pipeline" | Not reported (ML knowledge Qs for MLE) | Yes (market-data prediction walkthrough; feature pipeline discussion) `[prep]` | Not reported |
| Research presentation | Not reported | Not reported (PhD XTY Labs internship may differ — no evidence) | Not reported |
| Intern vs FT | Same quiz; compressed 1-day interviews; assessment centre for SWE interns | Interns: take-home + 2 short interviews; FT: multi-day onsite | Interns: OA + up to 4 algo interviews, no finance; FT: long take-home + directors/CEO |
| Difficulty (Glassdoor) | 3.45/5 | 3.42/5 | 3.2/5 |
| Avg process length | ~15–23 days | ~41–50 days | ~35–49 days |

## 5. Prep implications for the user (evidence-based)
1. **G-Research:** do the official example-question PDF and the 2025 assessment-process/recommended-reading PDFs; practise 10-question/90-min MCQ pacing; refresh OLS derivations, ODEs, conditional probability; for SWE prepare a "read these logs, find the bottleneck" exercise and Kubernetes basics; keep take-home code production-quality (tests, README).
2. **XTX:** drill timed maths (20 problems/60 min, no backtracking); LeetCode-hard under time; C++ internals flashcards (RAII, vtables, alignment, unordered_map internals, atomics, syscalls, cache); ESL ch.1–9; be ready to implement logistic regression/GBM logic from scratch and to defend a take-home against "what else would you handle?".
3. **Quadrature:** two-heap streaming median, interval/queue problems with crisp Big-O; small trading simulators (order matching, P&L with dividends/mergers); cache-aware data-structure trade-offs; expect an evolving-requirements pairing session; budget a full day for the Python take-home.

## 6. Source index (all URLs referenced)
Official: gresearch.com career-guides & PDFs (2020, 2022, 2025), gresearch.com/news quant-platform-interview post (+ Gradcracker mirror), gresearch.com/graduates, Bright Network G-Research pages, XTX Greenhouse postings (6688991003 Risk intern, 7524152003 Junior QR, 6274458003, 6927688003), quadrature.ai/careers/how-we-hire, /careers/internships, /careers/recruitment.
First-hand: Glassdoor pages listed per section; Blind threads listed per section; Hacker News 18502116; 1point3acres thread 949252.
Prep/aggregators: techinterview.org (G-Research quiz post; XTX guide), quantt.co.uk XTX pages, quantblueprint.com XTX guide & job mirrors, intervyo.co.uk Quadrature guide, scoutify.com XTX, canarywharfian.co.uk XTX, tradermath.org, github.com/ankitkushawaha1000/HFT (self-labelled anecdotal/inferred), github.com/sgoel97/blog quant-interview (lists all three only as "very difficult, smaller firms"), github.com/perixtar/quant-interview-oa-bank (no entries for these firms), github.com/Leader-board/OA-and-Interviews (no entries for these firms).
Not found despite searching: TheStudentRoom threads specific to any of the three firms; 1point3acres G-Research/Quadrature 面经; Reddit threads surfaced by the search engine (Reddit was blocked and site: queries returned nothing).
