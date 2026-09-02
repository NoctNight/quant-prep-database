# Coding-interview evidence: Jane Street, Five Rings, Radix Trading, Headlands Technologies (2021–2026)

Compiled 2026-09-01.

## 0. Method and caveats (read first)

- **Coverage.** 27 web searches (Glassdoor, Blind, Reddit, LeetCode Discuss, QuantNet, WSO, 1point3acres, Taro, GitHub, prep sites), ~15 GitHub code/repo searches, ~90 page-fetch attempts. The session's web-search quota was exhausted after search 27 (cap = 200 for the whole session, most consumed by other tasks), so a few planned internship-specific searches could not be run; internship evidence below comes from the searches that did run plus GitHub-hosted sources.
- **Fetch restrictions.** The sandbox's egress proxy blocked full-page reads of glassdoor.com, teamblind.com, reddit.com, leetcode.com, quantnet.com, wallstreetoasis.com, 1point3acres.com, jointaro.com, janestreet.com, medium.com, and every prep site. Only github.com / raw.githubusercontent.com were readable. Consequently:
  - Forum content is quoted from **search-engine result summaries** (snippets), not full threads. Where a snippet paraphrased, I say "paraphrase".
  - The richest verbatim Glassdoor material comes from `pushpa-kumar/placement-prep` (GitHub), which transcribes **archived Glassdoor pages** (web.archive.org 2022-08-08 and 2024-09-10 snapshots) with country/date/outcome. I treat those as Glassdoor-grade evidence and cite the archive URL.
- **Reliability tags** used on every item: `[Glassdoor]`, `[Blind]`, `[Reddit]`, `[LC-Discuss]`, `[1p3a]`, `[WSO]`, `[QuantNet]`, `[personal-blog]`, `[official]`, `[prep-site]` (lower reliability), `[AI-compiled-repo]` (lowest: `ankitkushawaha1000/HFT` and `kishanBhandary/...` are LLM-generated question banks that self-label items "anecdotal"/"inferred"/"general-prep"; I list them only where they corroborate something else or to warn against them).
- **Level tags:** `INTERNSHIP`, `FULL-TIME` (new-grad or experienced; I say which when known), `unclear`.
- Nothing below is invented. Where a firm has thin evidence, the section says so explicitly.

---

## 1. Jane Street

### 1.1 Pipeline

**Language.** Official guidance (janestreet.com "Preparing for a Software Engineering Interview", quoted via search summary) `[official]`: "you can use any programming language you'd like … no bonus points for using OCaml … don't use OCaml just because you think it will make us happy." Candidates confirm: "you do not need OCaml for interviews, you can use any language, they want clean and simple code" `[Blind]`; Hong Kong FT candidate 2021: "OCaml (company language) not tested … there weren't any technical [language] questions" `[Glassdoor archived]`. Interview environment is a shared editor (Coderpad reported 2024 `[Glassdoor]`; "Google-Docs-style, no execution" `[personal-blog, UTCN guide]`; "values complete and correct code without allowing the interviewee to run their code" `[Glassdoor 2024]`). Python is the most common candidate choice; Blind has a thread literally titled "why jane street allowing python in interviews".

#### Internship (SWE)
- **No OA for SWE interns in most reports** (contrast with one 2021 report of a "1.5-hour HackerRank online test" before the phone interview — SWE, London-ish, see 1.2(d)). `[Glassdoor archived]`
- **Phone/online technical round:** ~45 min, one coding problem that grows in steps, plus Q&A. `[personal-blog: How-to-faang-UTCN Jane_Street_Guide.md]` A London SWE-intern phone interview was reported as **1 hour, "implement a board game described by the interviewer"**. `[1p3a thread-1034195, 2024-25]`
- **Onsite/"superday":** three 45-min coding rounds, **two interviewers per round**, "poor results in early rounds may result in same-day rejection without proceeding to round three." `[UTCN guide]` Corroborated by Blind: SWE-intern onsite candidate "got sent home after lunch" (2 of 4 rounds), another "made it about halfway (2/4) before the recruiter ended the day after lunch." `[Blind]` Hong Kong SWE intern: 3 technical rounds + 1 HR round; one technical round was "designing a game." `[1p3a thread 820245]`
- Blind consensus on interns: "questions are mostly implementation heavy and less leetcode style with an emphasis on clean code (functions, enums, structs, etc)"; "no math questions for SWE"; "there aren't behavioral interviews—they just want to see you write code." `[Blind]`
- Prep-site note (lower reliability): SWE-intern coding "incredibly hard" per one reviewer, "pretty typical interview with perhaps harder questions" per another. `[Glassdoor via search summary]`

#### Full-time / experienced (SWE)
- **Typical loop (2021–2025):** 1–2 technical phone screens (45–60 min) → onsite of 3–4 coding sessions (~60–75 min each, two interviewers) → 1 "project discussion / walk through a system you developed" round for experienced hires; some 2024 London loops added "system design" and light behavioural in the afternoon.
  - NY, offer accepted Apr 2024: "2 technical phone screenings + 4 onsite rounds (one being 'walk through a system you developed') … coding problems seemed more implementation intense … strong emphasis on writing clean, understandable code. Communication and collaborating with the interviewer appears important." `[Glassdoor archived 2024-09-10]` FULL-TIME
  - Poland, offer accepted 2021: "phone screen + 3×1 hr coding interviews + 1 project-discussion interview, 2 interviewers per session … very smoothly run." `[Glassdoor archived 2022-08-08]` FULL-TIME
  - Hong Kong, offer 2021: "one screening interview of one 1-hour session … then one final interview with three similar sessions." `[Glassdoor archived]` FULL-TIME
  - London 2024, no offer: "Full-day onsite … lots of coding and system design questions, some behavioural questions in the afternoon. Tough but fair." `[Glassdoor archived]` FULL-TIME
  - Glassdoor aggregate (SWE): 178 questions / 187 reviews, difficulty 3.5/5, 58% positive, ~19 days to hire; "3 rounds of technical interview, 2 before lunch. Each round consisted of a software question (think Leetcode easy-medium), with multiple steps being added along the way (two–three steps in total)"; "Four technical rounds in total: one virtual, two onsite before lunch, one onsite after lunch, followed by a Q&A with engineers"; "focus on writing clean code, OOP, nothing too algorithmic or leetcode"; "problems are open ended, the main concern of the interviewer is how you approach it." `[Glassdoor search summary]` FULL-TIME (mixed)
  - Experienced ML/agents hire, 2025 (Brian Lee, ex-Google): "the most thoroughly rigorous interview process and smartest interviewers by far … the highest quality data modeling problems by far." No question detail. `[personal-blog brilee/modern-descartes 2025_job_search.md]` FULL-TIME experienced
  - 2020 new-grad SWE (OneRaynyDay blog, kept for context): "general algorithm questions … Jane Street was a bit harder given the time pressure … I spent too much time explaining and didn't have enough time to finish the code." `[personal-blog]` FULL-TIME new grad (2020, pre-window)
- **Non-SWE engineering tracks** exist with different pipelines: Trade Desk Operations Engineer, London, Jan 2025: take-home test → mathematical problem-solving interview → technical coding interview; recruiter sent a "getting started" doc with basic Python syntax. `[LC-Discuss post 6340012]` FULL-TIME (graduate). A 1p3a "five-round" report (thread 1134748) matches this shape: take-home, HR call, "numeracy challenge", resume deep-dive, technical interviews. Data Engineer (Hong Kong): Round 1 "problem solving" coding. `[LC-Discuss post 7701675]` Network Engineer intern: a coding round exists (Blind thread title). `[Blind]`

#### Quant Trader / Quant Researcher (coding component only)
- **QT:** no HackerRank OA reported 2021–26 (a 2016 HackerRank 30-min/4-question probability test exists: `ptmminh/quanttest` `[GitHub, pre-window]`). Phone rounds are probability/EV/market-making; "the difficulty gets really hard at the 3rd interview." `[Blind]` Official trading-interviews page: final round "may include problem solving, probability and statistics, **coding (in any language of your choice), data analysis**, and general interests." `[official, via search summary]` Prep-site claim of a Zetamac-style mental-math OA at Jane Street appears in `hieptran1812/my-website` and a derived note — **not corroborated by any candidate report; treat as unverified** `[prep-site]`.
- **QR internship:** "3 phone rounds focusing on math/probability with one coding interview (not too much emphasis on algorithms)." `[Glassdoor QR-intern search summary]` INTERNSHIP. Feb 2024 QR: "first round asked a dice betting problem about optimizing expected value strategies, the second round included a coding problem." `[Glassdoor search summary]` unclear level. Blind: "Jane Street research final round" thread exists (no detail retrievable). `[Blind]`
- **ML Researcher (FT):** Blind thread "Jane Street Machine Learning Researcher interview tips"; David Foster's Medium guide (2025) — not fetchable. `[Blind/Medium]`

### 1.2 Reported coding questions, categorised

(a) **Arrays / strings / hashing**
1. **Transform String** — "repeatedly remove an adjacent 'AB'/'BA' pair or an adjacent 'CD'/'DC' pair …; return the final resulting string" (stack reduction, cf. LC 1544). OA problem, last seen **Jul 17 2024**. Role unclear. `[fastprep tracker perixtar/quant-interview-oa-bank; prep-site-derived, medium-low]` unclear
2. **Consecutive failed logins** — "Given a list of users and their login events (Success/Fail), flag users who have failed login exactly k times consecutively" (like Max Consecutive Ones). Data Engineer, Hong Kong, Round 1. Candidate missed an edge case, fixed it live, still rejected: "Jane Street expecting completely flawless first-pass execution." `[LC-Discuss 7701675]` FULL-TIME
3. **Encoded-moves stream detector** — "Given a set of encoded 'moves', write a function to encode a move, and a separate function to detect/execute a move once its full input sequence has been streamed into memory (O(n) target)" — dictionary keyed by move sequences / suffix check; Trie suggested (cf. LC "Stream of Characters"). SWE intern, rejected. `[LC-Discuss interview-question/882072]` INTERNSHIP
4. "Standard algorithmic interview questions, a bit related to time complexity analyses" — HK 2021, screening + 3-session final. `[Glassdoor archived]` FULL-TIME
5. "Data structure question using Python" — US 2021, round 2 after a background-focused phone call. `[Glassdoor archived]` FULL-TIME
6. **Memoization ladder (official example):** "write a memoized version of an expensive int→int function … only does the computation once per input" → hash table; Part 2: notice unbounded memory, add **FIFO eviction in O(1)**; Part 3: **LRU eviction with a doubly linked list**. `[official Jane Street blog "What a Jane Street dev interview is like", via spacecomplexity.ai summary]` Both levels

(b) **Recursion / DP** — no specific 2021–26 candidate report found; "recursion" appears only in prep-site topic lists (`interviewquery`). One AI-compiled repo lists "permutations of a string" as `[anecdotal]` — unverified.

(c) **Graphs / trees**
7. **Unit conversion** (official mock interview on YouTube, ~2022): given facts like "1 m = 3.28 ft", "1 ft = 12 in", answer queries "2 m = ? in" — build a graph of units, BFS/DFS with multiplied edge weights, handle unreachable units. Multiple candidate prep repos (`chantca95/JaneStreetUnitConversion`, `phantomgoose/unit_conversion`, `WebMettle/UnitConversion`, `NikolasBurzynski/Unit_Converter`, `Daniel-Harrington/Jane-Street-Interview-Prep`). `[official mock; GitHub]` Both levels (used as the canonical example of JS style)
8. "Find the k-th smallest element in a stream" listed for JS 2025 in `kishanBhandary/Projects-and-Interview-Question` — `[AI-compiled-repo, very low]`.

(d) **Design / OOP / simulation (the dominant JS category)**
9. **Tetris** — "implement the game state and core logic (no UI)"; onsite ~75 min; also given as final-round question after phone screen; "implementation accuracy is important"; deliberately underspecified, ask clarifying questions. SWE, 2024. `[Glassdoor archived 2024-09-10; corroborated by interviewing.io]` FULL-TIME (level not stated → unclear)
10. **Connect Four, infinite width** — "Implement the game state for a variant of Connect Four with infinite width (columns), pieces enter from the bottom." Remote Coderpad screen ("relatively straightforward (but fun!)"), then onsite with 3 similar coding questions + project explanation; offer accepted; rated Average. SWE 2024. `[Glassdoor archived 2024-09-10]` FULL-TIME
11. **"Puissance 4" with infinite columns of infinite height** — implement `move` and `checkWin` (column of consecutive same-colour pieces; two players R/B; infinite horizontal indices). Phone interview after a 1.5-h HackerRank test; no offer. SWE, 2021. `[Glassdoor archived 2022-08-08]` FULL-TIME (unclear)
12. **Board game implementation** — London SWE-intern phone interview, 1 hour, "implement a board game described by the interviewer." `[1p3a thread-1034195]` INTERNSHIP
13. **"Designing a game"** — HK SWE intern onsite, one of 3 technical rounds. `[1p3a thread 820245]` INTERNSHIP
14. **Stack machine** — "to make a stack machine"; single ~1 h interview, London, Software Developer 2023; "questions straightforward and interesting … big emphasis on the small details which one does not think about." `[Glassdoor archived]` FULL-TIME
15. **Custom stack with various operations** — phone interview, Poland 2021; "needed to explain my process of implementing a data structure. Little algorithm knowledge needed." `[Glassdoor archived]` FULL-TIME
16. **Video-player API** — design and implement; underspecified; deep edge-case exploration; ~75 min. `[interviewing.io, prep-site but from a real mock/loop]` unclear
17. "Write a chess game", "Write an AI bot" — cited on Blind as the kind of "design questions they expect you to code." `[Blind]` unclear
18. **Limit order book** — "Implement add, cancel, and match for a single-symbol book. Now make cancel O(1)." and "Design an order book with add, cancel and top-of-book, all better than O(n)" — attributed to Jane Street by techinterview.org `[prep-site, medium-low]`; a candidate built a price-time-priority book "for Jane Street final round interview prep" (Feb 2025) `[GitHub dominicchildrv/order-book-basics]`; one 2025 entry lists "design a high-throughput low-latency order matching engine" `[AI-compiled-repo, very low]`. Treat LOB as *plausible but not candidate-confirmed* for JS.
19. Systems-level: "design an exchange-trading system message flow; validate order-book data across multiple databases; sort trade executions into canonical order" — `[prep-site interviewquery, low]`.

(e) **Probability-to-code** — QR/QT final rounds include "coding … data analysis" `[official]`; a QR report pairs a dice-betting EV problem (round 1) with a coding problem (round 2) `[Glassdoor 2024]`. The official mock trading interview (YouTube) is a 20-sided-die / "rolling in the deep" style game that candidates solve by simulation (`ak2k2/Jane-Street-Trading-Mock-Interview`, `shivpatri/rolling-in-the-deep`, `womogenes/quant-dice-game`). No verbatim coded-probability question from a real loop retrieved.

(f) **Low-level / systems / C++** — essentially absent from SWE candidate reports ("not grilled on kernel-bypass and lock-free latency the way you would be at Jump or HRT" `[prep-site hieptran]`). The `ankitkushawaha1000/HFT` repo lists SPSC queues, acquire/release, NUMA for JS — all self-tagged `[inferred]`; **ignore**.

(g) **Math / number puzzles coded** — "Optimal solution for flipping coin games with opponent" (game-theory/EV, no scratch paper) in an onsite mathematical round for a **SWE**, HK 2021, no offer: "a bunch of challenging mathematical questions, including probabilities … expected me to show how I interpreted the question." `[Glassdoor archived]` FULL-TIME — note this contradicts the Blind claim "no math for SWE"; HK/APAC loops may differ. "Estimate of odd numbers from 0 to 60" (SWE, UK 2022, rated Easy). `[Glassdoor archived]` QT phone riddles: "when is the next time the date will contain only unique digits." `[Blind]`

(h) **Data manipulation (pandas/numpy)** — "data analysis" is an official QT/QR final-round component; ML-researcher loop has "data modeling problems" `[personal-blog brilee 2025]`. No verbatim pandas task retrieved.

(i) **Take-home** — Trade Desk Operations Engineer (London, 2025) and the 1p3a five-round report include a take-home test. `[LC-Discuss 6340012; 1p3a 1134748]` FULL-TIME graduate. No take-home reported for core SWE/QT/QR.

### 1.3 Difficulty and style notes
- Each round = **one problem with 2–3 escalating steps** ("multiple steps being added along the way"; "start with one implementation problem and keep building on it"). Interviewers "change one rule and ask you to update the implementation without rewriting everything." `[Glassdoor, prep-sites, UTCN guide]`
- **Clean code over cleverness**: "clean structure — whether you organise code so it's easy to extend", "response to hints"; "a careful, well-explained solution that covers less ground beats a rushed one with errors." `[Glassdoor 2024; prep-sites]` Time pressure is real: one strong candidate failed for over-explaining before coding `[personal-blog 2020]`; another was rejected after a single live-fixed edge-case bug `[LC-Discuss]`.
- **No code execution** in several loops; candidates must desk-check. `[Glassdoor 2024; UTCN]`
- **Two interviewers per session** at onsite; "felt like a carefully run collaborative session than a pile-on." `[Glassdoor; Blind; UTCN]`
- Complexity analysis is asked but secondary ("a bit related to time complexity analyses"). Testing: implicit — "reason about edge cases", "debug issues in real time" `[Blind recruiter quote]`.
- **Internship vs full-time differences:** interns get ~45-min phone + 3×45-min onsite, all coding, no project round; FT gets 1–2 phone + 3–4 coding rounds (60–75 min) + project/system walk-through (experienced) or system design (some 2024 London). Problem *type* (game/data-structure simulation) is the same at both levels; intern reports skew slightly easier ("relatively straightforward but fun"), FT reports mention system design more.

### 1.4 Recurring themes
1. **Implement a game / state machine with rules that later change** (Connect Four ×3 variants, Tetris ×2, "board game", "chess", "designing a game").
2. **Build a small data structure with an evolving API** (custom stack, stack machine, memoize→FIFO→LRU, encoded-move stream detector).
3. **Underspecified prompts** → clarify → clean class design → edge cases.
4. Language-agnostic, Python most common; OCaml irrelevant.
5. For QT/QR the coding round is light and secondary to probability/EV games.

---

## 2. Five Rings (Five Rings Capital / Five Rings LLC)

### 2.1 Pipeline
Glassdoor aggregate: 338 questions / 302 reviews, difficulty 3.57/5, **35.2% positive** (notably low). `[Glassdoor search summary]` Firm background: NYC (plus Boca Raton, London, Amsterdam), founded by an ex-Jane-Street trader, "very school-selective, mostly recruiting out of MIT" `[GitHub quantprep]`; C++ on Linux for developers `[official job post]`.

#### Internship
- **Quant Trader intern:** OA "covering mental math, probability, and geometry that requires answering questions extremely quickly"; then ~1-hour technical interview, "mostly technical and behavioral." `[Glassdoor QT-intern search summary]` INTERNSHIP
- Phone screen (role unclear, likely intern/new-grad quant): "many estimation questions (Fermi and computational math) with short time limits." `[Glassdoor]` unclear
- adam2392 blog (see 2.2) documents a 3-round phone sequence (mental math → dice games → tournament probability) and "Superday: never made it this far." Level unclear (author was a PhD student → likely internship/new-grad quant). `[personal-blog]`
- Software Developer intern: no separate intern report found; the SWE pipeline below is from a full-time report. Five Rings also runs "LINK", a 5-day software intensive for sophomores (Aug 2026). `[GitHub listing]`

#### Full-time / experienced
- **Software Developer (FT):** "15-minute recruiter video interview, a 1-hour technical video interview **implementing a well-known data structure**, and a 5-hour virtual onsite with **4 technical interviews focusing on data structures and algorithms and a chat with the CTO**." `[Glassdoor search summary]` FULL-TIME
- Another SWE reviewer: "some interviews focus on **extremely minute details of the C language, with lots of structs, pointers, and overloaded while loops where you had to keep track of multiple variables**." `[Glassdoor]` FULL-TIME (unclear)
- **Quant (role unspecified):** "behavioral plus **10 technical questions, with 30 seconds to both hear and answer each**." Samples: (i) coin with P(H)=2/3, P(T)=1/3 — expected tosses until #heads − #tails = 2; (ii) area of intersection of circles centred (0,1) and (1,0), radius 1; (iii) how many primes from 1 to 999. `[Glassdoor]` unclear
- **Full day:** "6.5 hours over Zoom, including 1:1 and 2:1 interviews with developers, quants, and traders." `[Glassdoor]` unclear

### 2.2 Reported coding questions, categorised

Evidence for *coding* at Five Rings is **thin**: the only concrete coding descriptions are "implement a well-known data structure" (1-hour screen), "DS&A" onsite rounds, and C-language minutiae. Everything else reported is mental math / probability, which is what quant candidates are asked.

(a) Arrays/strings/hashing — no verbatim item. Onsite rounds are "data structures and algorithms." `[Glassdoor]` FULL-TIME SWE

(b) Recursion/DP — none reported.

(c) Graphs/trees — none reported.

(d) Design/OOP/simulation — "implement a well-known data structure" (1-h technical video, SWE FT). `[Glassdoor]` A `cpp-order-book` repo claims "Five Rings expects C++ proficiency for production systems" `[GitHub, low]`.

(e) Probability-to-code — non-transitive **3-dice game**: three irregular dice; two players each choose one and roll; "should you pick first or second, and which die?" — a candidate wrote a notebook to simulate it "from the Five Rings interview." `[GitHub aryan-cs/five-rings-interview]` unclear (asked verbally; coded afterwards).

(f) Low-level / C++ — "extremely minute details of the C language … structs, pointers, overloaded while loops … keep track of multiple variables" (read-the-code / trace-the-output style). `[Glassdoor]` FULL-TIME SWE. Job post: C++/Linux, exchange connectivity, trader-facing UIs. `[official]`

(g) Math / number puzzles (verbal, the bulk of Five Rings evidence)
- Round 1 mental math `[personal-blog adam2392]`: tenth root of 10; log base 1.2 of 3; litres of water in an Olympic pool; weight of a baby elephant; number of digits in 50!; maximum pizza slices after 10 straight cuts.
- Round 2 dice `[same]`: EV of one 6-sided die; roll two dice but only roll the second if the first is ≤4 (sum can't exceed 10) — EV; you may choose number of sides — should the lower-sided die roll first or second; optimal number of sides to maximise EV.
- Round 3 tournaments `[same]`: 8 teams, each advances w.p. 0.5, random matchups — P(two specific teams meet); 9 teams, one randomly advances per level — P(two teams meet).
- Extras `[same]`: entry price for coin-flip game (H=$5, T=$0); max regions from 6 lines in a plane; expected distance from origin of a uniform point in the unit disc.
- Glassdoor quant samples (above): biased-coin stopping time, circle-intersection area, prime count to 999. `[Glassdoor]`
- Older (c. 2016, outside window, listed for pattern only) `[GitHub signaldatascience]`: flip 4 coins, $1/head, may re-flip one coin — EV; A has 6, B has 4, race to 10 on coin flips; pay to go first in an alternating-coin $30 game; expected consecutive heads in 3 flips; Fermi: windows in the Empire State Building, largest 24-h temperature swing in the US.

(h) Data manipulation — none reported. (i) Take-home — none reported.

### 2.3 Difficulty and style notes
- **Speed is the filter**: 30 seconds per question in the quant technical; OA "answer extremely quickly"; short time limits on Fermi questions. `[Glassdoor]`
- Developer loop is long (5–6.5 h virtual) with many rounds incl. CTO chat; C-level detail questions suggest they probe language fundamentals rather than LeetCode-hard algorithms.
- 35% positive experience rating — candidates describe it as abrupt.
- **Internship vs full-time:** intern QT has a timed OA + 1 technical hour; FT dev has no OA reported but a 1-h DS implementation screen + 4-round onsite + CTO. Topic mix is the same (probability/mental math for quant, DS&A + C/C++ for dev).

### 2.4 Recurring themes
Dice EV games with stopping/choice rules; tournament/meeting probabilities; Fermi estimation; 30-second rapid-fire; for developers, "implement a known data structure" plus C pointer/struct minutiae.

---

## 3. Radix Trading

### 3.1 Pipeline
Chicago; ~80 people; founded ~2010 by ex-Citadel/Tradelink quants `[Wikipedia/prep-site]`. Glassdoor: 71.4% positive, difficulty 3.07/5, ~25 days; "Quant Trading Researcher and Quantitative Technologist rated their interviews the hardest." `[Glassdoor search summary]` Roles: Quantitative Technologist (C++; also "Quantitative Technologist – C++ Intern" posting 2026), Quantitative Trading Researcher, Systems/Software.

#### Internship
- "Radix … selects a handful of interns every year. Just email your resume." `[GitHub quantprep, 2022]` No internship interview report with question content was found. **Evidence: none beyond existence of the C++ intern posting.**

#### Full-time / experienced
- Blind thread "what to expect from radix quant technologist interview": answer summarised as "**focused on pure C++**." `[Blind]` FULL-TIME (unclear)
- Prep-site pipeline (Quantt, lower reliability): SWE OA "two or three hard algorithmic problems in 90–120 minutes"; then "60–90 minute call with a senior engineer or researcher — live coding plus systems design"; onsite "five to seven interviews in a single day in Chicago" covering coding, systems design, a research-style problem-solving session, and a conversation with a senior partner; "interviewers are working senior engineers who keep the conversation technical from minute one." `[prep-site]`
- Quant Blueprint (prep-site): "expert-level C++ is the baseline … modern C++ (C++17/20), move semantics, template metaprogramming, SIMD intrinsics." `[prep-site]`
- 1point3acres thread 674977 "Radix Trading Quant Finance Interview Experience" exists (not fetchable). `[1p3a]`
- An AI-compiled repo asserts a Rust signal from r/rust — `[AI-compiled-repo, low]`; not corroborated.

### 3.2 Reported coding questions, categorised

Overall: **thin**. Three concrete items.

(a) Arrays/strings/hashing — "find the smallest non-negative integer absent from a provided collection of numbers" (set logic / sorting trade-offs / optimal array search). `[crackmlinterview.com, prep-site aggregating 3 reports]` unclear

(b) Recursion/DP — "**Write Python code to output all permutations of the list of integers from 1 to n, and analyse the time and memory complexity** of the algorithm." `[Glassdoor]` unclear (Python → likely research/intern track)

(c) Graphs/trees — none reported.

(d) Design/OOP — "topics that come up most: OOP, class design, C++, encapsulation." `[crackmlinterview, prep-site]` unclear

(e) Probability-to-code — none reported.

(f) Low-level/C++ — "Certain questions in matrix multiplication, some math brainteasers and C++ coding." `[Glassdoor QTN_4159850]` unclear. "Pure C++" for Quant Technologist `[Blind]`. Prep-site claims: move semantics, templates, SIMD `[prep-site]`; an AI-compiled repo lists "std::mutex vs std::atomic, when lock-free is preferred" and "concurrent queue in Rust" as `general-prep` — unverified.

(g) Math/number puzzles — "math brainteasers" alongside matrix-multiplication questions. `[Glassdoor]`

(h) Data manipulation — none. (i) Take-home — none reported (Quantt describes a timed OA rather than a take-home).

### 3.3 Difficulty and style notes
- Reported as one of the hardest bars ("among the highest in the industry" `[prep-site]`), yet Glassdoor's numeric difficulty is moderate (3.07) — small sample.
- Complexity analysis is explicitly requested (permutations question).
- Loop is long (5–7 onsite rounds) and technical from the first call.
- **Internship vs FT:** no intern reports; can only say the intern posting is C++-specific.

### 3.4 Recurring themes
C++ depth (Quant Technologist), math brainteasers + linear-algebra flavoured questions (research), OOP/class design. Sparse public data; candidates say "not much on Glassdoor."

---

## 4. Headlands Technologies

### 4.1 Pipeline
Chicago (also NYC, London); founded by ex-Citadel execs `[WSO]`; "a small firm willing to pay more than most competitors" `[GitHub quantprep]`. Glassdoor: ~57 questions, hiring ~11 days. Roles: Software Engineer/Developer, Quantitative Researcher, Research Developer (new grad), FPGA.

#### Internship
- No intern-specific interview report retrieved. A 1point3acres "headlands interview questions" index exists (not fetchable). **Evidence: none.**

#### Full-time / new-grad
- **Stage 1 — C++ HackerRank OA:** "90 minutes, 2 questions: one must be done in C++, the second can be C++, Java, or Python"; "medium-to-hard"; another report: "2-hour HackerRank … very challenging questions, study C++ beforehand or you won't be prepared." `[Glassdoor search summary; WSO thread "Headlands Tech Interview & Online Assessment"]` FULL-TIME (new grad)
- **Stage 2 —** "1-on-1 Zoom interview with a developer or researcher." `[Glassdoor]`
- **Later rounds —** "algorithms, OS concepts, concurrency, and open-ended systems questions." `[Glassdoor]`
- **Loop length:** new-grad 2023: "a grueling loop of **10+ interviews**. I faltered after about six rounds of intense C++ questions." `[personal-blog 54skyxenon finale-2023]` FULL-TIME new grad
- Also cited: QR-heavy firms "like HRT, Headlands, and Jump … will almost always test programming through a combination of online assessments and Leetcode-style interviews." `[personal-blog sgoel97 2022]`
- Blind: "Headlands interview — what are the best C++ books?"; "has anyone interviewed with Headlands Technologies LLC". `[Blind]`

### 4.2 Reported coding questions, categorised

(a) Arrays/strings/hashing / **data joins**
1. **As-of join on a CSV row struct** — "a struct API representing a row in a CSV table with one timestamp and several columns; implement a function similar to an **asof join**." `[Glassdoor]` FULL-TIME (unclear) — the single most-cited Headlands question.

(b) Recursion/DP — none reported.

(c) Graphs/trees / **union-find**
2. **"Disaster Recovery" (OA, Hard)** — "Reconstruct commit histories from a corrupted log: discard malformed entries; group commits into 'repositories' via **Union-Find** where commits sharing at least one matching file-path↔identifier pair merge into the same repository; detect 'ambiguity' when the same file path maps to more than one identifier within a repository (output 'AMBIGUOUS INPUT!'); answer queries returning sorted commit IDs within a timestamp range for a repository. Up to 10^7 log entries, 10^5 queries, 64-bit IDs/timestamps." Last seen **Mar 21 2026**. `[fastprep tracker perixtar/quant-interview-oa-bank; prep-site-derived, medium]` unclear (OA, likely new-grad)

(d) Design/OOP/simulation
3. "Identifying and **removing unused code** from a company's codebase" (technical/open-ended). `[Glassdoor]` unclear

(e) Probability-to-code — none; but "some **statistics problems** and C++ coding problems; the coding was quite easy but the statistics problems require preparation on statistical terminology and quantities" (QR-flavoured screen). `[Glassdoor]` unclear

(f) Low-level / systems / C++
4. "Deep questions about high-performance C++: **malloc vs new**, **std::copy vs memcpy**." `[WSO]` FULL-TIME
5. "OS concepts, concurrency, open-ended systems questions" in later rounds. `[Glassdoor]`
6. "Six rounds of intense C++ questions" (2023 new grad). `[personal-blog]`
7. Lock-free SPSC queue — tagged Headlands in one GitHub note, but the underlying source (eFinancialCareers) is generic "HFT interview" advice, **not Headlands-specific**. `[low]`

(g) Math/number puzzles — none beyond the statistics items.

(h) Data manipulation — the as-of join (1) is effectively a pandas `merge_asof` re-implementation in C++/Python; statistics-terminology questions for QR. `[Glassdoor]`

(i) Take-home — none reported (timed HackerRank instead).

### 4.3 Difficulty and style notes
- The OA is the gate and is C++-mandatory for at least one problem; multiple candidates call it very hard and C++-specific.
- Onsite is unusually long (10+ rounds reported) and C++-internals heavy (memory, allocation, copying primitives, concurrency, OS).
- Coding difficulty in the QR screen was "quite easy" relative to the statistics questions — i.e., difficulty is role-dependent.
- **Internship vs FT:** no intern data; FT/new-grad = C++ HackerRank → Zoom → many C++/systems rounds.

### 4.4 Recurring themes
C++ HackerRank OA; as-of join; malloc/new, memcpy/std::copy; concurrency + OS; time-series/CSV data handling; union-find style hard OA.

---

## 5. Cross-firm summary table

| Firm | OA? | Screen | Onsite | Language | Coding style | Evidence volume |
|---|---|---|---|---|---|---|
| Jane Street SWE (intern) | No (one 2021 HackerRank outlier) | 45–60 min, 1 evolving problem | 3×45 min, 2 interviewers each, same-day cuts | Any; Python common | Game/DS simulation, clean OOP, no execution | High |
| Jane Street SWE (FT) | No | 1–2×45–60 min | 3–4 coding (60–75 min) + project/system walk-through (+ system design, London 2024) | Any | Same style + project deep-dive | High |
| Jane Street QT/QR | No (HackerRank prob. test seen 2016 only) | Prob/EV phone rounds | Superday incl. light coding + data analysis | Any | Light coding after a math problem | Medium |
| Five Rings dev (FT) | No | 15 min recruiter + 1 h "implement known DS" | 5 h: 4×DS&A + CTO | C/C++ | DS implementation, C pointer/struct minutiae | Low–medium |
| Five Rings QT (intern) | Yes: timed mental-math/prob/geometry | ~1 h tech+behavioural | 30-s rapid-fire technical, 6.5 h day | n/a | Almost no coding | Medium (math) |
| Radix | Yes (SWE, per prep-site): 2–3 hard algos in 90–120 min | 60–90 min live coding + systems | 5–7 rounds Chicago | C++ (Python for research) | Pure C++; permutations+complexity; brainteasers | Low |
| Headlands | Yes: 90–120 min C++ HackerRank, 2 Qs | Zoom w/ dev or researcher | Up to 10+ rounds, C++/OS/concurrency | C++ mandatory for ≥1 OA Q | As-of join, union-find OA, malloc/new, memcpy | Low–medium |

## 6. Source index (URLs cited)
- Glassdoor JS SWE: https://www.glassdoor.com/Interview/Jane-Street-Software-Engineer-Interview-Questions-EI_IE255549.0,11_KO12,29.htm (archived: https://web.archive.org/web/20220808060706/… and https://web.archive.org/web/20240910034014/…)
- Glassdoor JS Quant Research: https://www.glassdoor.com/Interview/Jane-Street-Quant-Research-Interview-Questions-EI_IE255549.0,11_KO12,26.htm
- Glassdoor JS SWE Intern: https://www.glassdoor.com/Interview/Jane-Street-Software-Engineer-Intern-Interview-Questions-EI_IE255549.0,11_KO12,36.htm
- Jane Street official: https://www.janestreet.com/join-jane-street/interviewing/ ; https://www.janestreet.com/preparing-for-a-software-engineering-interview/ ; https://www.janestreet.com/trading-interviews/ ; https://blog.janestreet.com/what-a-jane-street-dev-interview-is-like/
- LeetCode Discuss: https://leetcode.com/discuss/post/7701675/ ; https://leetcode.com/discuss/interview-question/882072/jane-street-intern-interview/ ; https://leetcode.com/discuss/post/6340012/
- 1point3acres: https://www.1point3acres.com/interview/thread/820245 ; https://www.1point3acres.com/bbs/thread-1034195-1-1.html ; https://www.1point3acres.com/interview/thread/1134748 ; https://www.1point3acres.com/interview/thread/674977 (Radix) ; https://www.1point3acres.com/interview/company/headlands
- Blind: https://www.teamblind.com/post/jane-street-experienced-hire-interview-process-swe-riuyrkgz ; https://www.teamblind.com/post/jane-street-swe-intern-interview-jvxfxtxv ; https://www.teamblind.com/post/jane-street-onsite-interview-swe-0uhhwcc2 ; https://www.teamblind.com/post/why-jane-street-allowing-python-in-interviews-8rpcrzgm ; https://www.teamblind.com/post/jane-street-network-engineer-intern-coding-round-ekfq3qmh ; https://www.teamblind.com/post/what-to-expect-from-radix-quant-technologist-interview-cttcveez ; https://www.teamblind.com/post/Headlands-interview-What-are-the-best-c-books-75wjLE52
- Taro: https://www.jointaro.com/interviews/companies/jane-street/?tab=experiences
- WSO: https://www.wallstreetoasis.com/forum/hedge-fund/headlands-tech-interview-online-assessment ; https://www.wallstreetoasis.com/company/five-rings-capital-llc/interview ; https://www.wallstreetoasis.com/blog/detailed-in-person-jane-street-interview-software-engineer
- Glassdoor Five Rings: https://www.glassdoor.com/Interview/Five-Rings-Interview-Questions-E375785.htm ; https://www.glassdoor.com/Interview/Five-Rings-Quant-Trader-Intern-Interview-Questions-EI_IE375785.0,10_KO11,30.htm
- Glassdoor Radix: https://www.glassdoor.com/Interview/Radix-Trading-Interview-Questions-E1681590.htm ; https://www.glassdoor.sg/Interview/Certain-questions-in-matrix-miltiplication-some-math-brainteasers-and-C-coding-QTN_4159850.htm
- Glassdoor Headlands: https://www.glassdoor.com/Interview/Headlands-Technologies-Interview-Questions-E715901.htm
- GitHub: https://github.com/pushpa-kumar/placement-prep (raw-notes/company-janestreet-jump.md, topic-algo-ds-oa.md) ; https://github.com/perixtar/quant-interview-oa-bank ; https://github.com/ptmminh/quanttest ; https://github.com/How-to-faang-UTCN/How-to-faang-Guide/blob/main/guides/Jane_Street_Guide.md ; https://github.com/adam2392/adam2392.github.io/blob/master/_posts/academic/interview-questions.md ; https://github.com/aryan-cs/five-rings-interview ; https://github.com/54skyxenon/54skyxenon.github.io/blob/master/content/blog/finale-2023.md ; https://github.com/brilee/modern-descartes-v2/blob/master/essays/personal/2025_job_search.md ; https://github.com/OneRaynyDay/oneraynyday.github.io/blob/master/_posts/2020-09-30-Interviewing-During-Covid.md ; https://github.com/signaldatascience/R-curriculum/blob/master/interview-prep/technical-questions/interview-qs.md ; https://github.com/dominicchildrv/order-book-basics ; https://github.com/quantprep/quantnewgrad2022 ; https://github.com/ankitkushawaha1000/HFT (AI-compiled, low) ; https://github.com/kishanBhandary/Projects-and-Interview-Question (AI-compiled, low)
- Prep sites (lower reliability): https://www.quantt.co.uk/resources/radix-trading-interview ; https://www.quantblueprint.com/guides/how-to-get-a-job-at-radix-trading ; https://crackmlinterview.com/company/radix-trading ; https://interviewing.io/jane-street-interview-questions ; https://www.techinterview.org/post/3233477310/limit-order-book-matching-engine-interview/ ; https://spacecomplexity.ai/blog/jane-street-software-engineer-interview ; https://www.fastprep.io/problems/janestreet-transform-string ; https://www.fastprep.io/problems/headlands-disaster-recovery
