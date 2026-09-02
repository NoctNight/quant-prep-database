# HFT / prop-shop coding-interview question research (2021–2026)

Firms: Hudson River Trading (HRT), Jump Trading, Tower Research Capital, Virtu Financial, Old Mission Capital, XTX Markets, Quantlab, Wolverine Trading, Belvedere Trading, Chicago Trading Company (CTC), Geneva Trading.
Compiled 2026-09-01.

## 0. How this was gathered, and how much to trust it

**Access constraints (important).** The research sandbox's egress proxy blocked direct fetches of glassdoor.com, teamblind.com, leetcode.com/discuss, 1point3acres.com, wallstreetoasis.com, reddit.com, quantnet.com, zhihu, medium, and every prep site (quantt, tradermath, dataford, interviewquery, prachub, fastprep, techinterview.org, quantvault, algodaily, interviewdb, naukri, indeed, ambitionbox). Only github.com / raw.githubusercontent.com was reachable, and the web-search quota (14 firm-level searches done) was exhausted early. So the primary channel became:

1. **Web-search result summaries** (14 queries; one per firm plus HRT/Jump forum-specific queries) – these carry snippets of Glassdoor/1point3acres/Blind/WSO content.
2. **GitHub question banks that mirror the blocked sources with primary URLs**, chiefly
   - `pushpa-kumar/placement-prep` (`raw-notes/company-hrt-citadel.md`, `company-janestreet-jump.md`, `company-twosigma-others.md`, `topic-algo-ds-oa.md`, `topic-system-design.md`, `topic-concurrency-atomics.md`, `wave2-personal-blogs.md`, …) – a bank compiled 2026-08-27 that records, per question: company, role, OA/interview, status REAL vs PRACTICE, and the source URL (LeetCode Discuss, Blind, Glassdoor, WSO, 1point3acres, FastPrep, PracHub, quantt, techinterview.org, ambitionbox…).
   - `Lazar-Ilic/Lazar` (`Notes/.../Interviews Coding Rounds/Hudson River Trading.txt`) – a verbatim dump of ~60 Glassdoor/AlgoDaily HRT interview items (2022 cycle) with the author's commentary.
   - `perixtar/quant-interview-oa-bank` (FastPrep tracker: 129 OA questions, 18 quant firms, refreshed 2026-07-31) – HRT 11, Virtu 7, Wolverine 3, Geneva 1.
   - `liquidslr/leetcode-company-wise-problems` (LeetCode company-tag CSVs for HRT, Jump, Tower, Virtu).
   - `ankitkushawaha1000/HFT` – an AI-assembled prep repo that self-labels each item `anecdotal` / `inferred` / `general-prep`; used only where tagged `anecdotal`, and always flagged.
3. **First-hand write-ups on GitHub**: `avinal/website` (HRT Systems intern 2021), `Shivam5022/Interview-Experiences` (HRT C++ SWE full-time, IIT-D campus), `ChinmayMittal/IITD-CSE` (Tower North-Moore QD intern), `spo-iitk/website` (Tower QR intern 2022, QT intern 2023), `Chao-Xi/jxtechbook` (Jump 2025 code round), `stanleywu111/jump-orderbook` (Jump take-home artifact), `OneRaynyDay` blog (HRT algo-engineer loop, 2020), `54skyxenon` blog (Old Mission onsite 2023), `Leader-board/OA-and-Interviews` (Virtu QTA 2021), `hudson-trading/wwhrt-bookbuilder-workshop` (HRT's own Core-Dev style exercise).

**Reliability tags used below**
- **[A]** first-hand candidate write-up, read in full.
- **[B]** candidate report on Glassdoor/Blind/LeetCode/WSO/1point3acres/AmbitionBox/Indeed, seen through a mirror or search snippet (primary URL given).
- **[B-]** aggregator that claims candidate origin but rewrites prompts (FastPrep, PracHub, InterviewDB, quantvault, LeetCode company tags).
- **[C]** prep-site "representative" question (quantt, tradermath, dataford, techinterview.org, hackerprep, codejeet, ankitkushawaha `inferred`). Not evidence a question was asked; included only where it corroborates a [A]/[B] theme.

**Level tags**: `[INTERNSHIP]`, `[FULL-TIME]` (new-grad or experienced; "NG" / "EXP" noted when the source says), `[unclear]`.

**Year coverage**: the request window is 2021–2026. A few pre-2021 items (2013–2020) are kept only where they are the sole evidence for a firm/round type, and are dated.

---

## 1. Cross-firm picture (what recurs everywhere)

| Theme | Where it shows up | Evidence grade |
|---|---|---|
| OA = 3–4 problems, 90–120 min, on CodeSignal (HRT), Codility (HRT systems, Jump, Virtu, CTC), HackerRank (Tower, Old Mission, Virtu SWE-intern). "All test cases must pass," hidden perf cases. | HRT, Jump, Tower, Virtu, CTC, Old Mission | A/B |
| Phone screen that is **not** LeetCode but C++/OS trivia: `inline` pros/cons, `vector` vs `list`, `map` vs `unordered_map`, `malloc`/demand paging/`sbrk`/`mmap`, virtual functions/vtable, stack vs heap, TCP vs UDP, threads vs processes, GIL. | HRT (strongest), Tower, Old Mission, XTX, Jump | A/B |
| Order-book / matching-engine build (add/cancel/modify/top-of-book; "now make cancel O(1)") as coding or design round; Jump has used it as a take-home. | HRT, Jump, Tower, Old Mission, Virtu, XTX | A/B/C |
| Lock-free SPSC ring buffer, false sharing / `alignas(64)`, memory_order semantics, cache lines. | HRT, Jump, Tower, XTX, Virtu (C++ core) | B/C |
| "Two threads increment a counter 1M times each; result < 2M – why?" | HRT (quantt), generic | B/C |
| Probability/brainteasers coded or oral even for SWE: 25 horses / 5 lanes; expected draws until taller; clock-hand angles (Virtu); dice sums vs coin heads (HRT); two-dice market-making (Old Mission). | HRT, Virtu, Tower, Old Mission, Jump | B |
| Performance follow-ups: solutions that are correct but TLE are rejected ("build a piece of a trading system … all tests TLE" at HRT). Interviewers escalate to complexity, then cache/memory. | HRT, Jump, XTX, Tower | B |
| Internship vs full-time: intern loops are shorter (OA + 1–2 technical calls, or OA + one 1.5 h interview on campus) and lean on DSA + fundamentals; full-time adds systems/C++ depth rounds, design rounds, and 4–6 h onsites. | all | A/B |

---

## 2. Hudson River Trading (HRT)

Roles seen: Software Engineer (C++ or Python), Core Developer / low-level C++, Algorithm Developer ("Algo Dev" = quant research; HRT's own postings and NUFT notes say the Algo Dev role is essentially QR), Algo Web Engineer, Systems / SysTrade / SRE, Data Scientist, ML engineer.

### 2.1 Pipeline

**Internship** (SWE intern, Systems intern, Algo Dev intern) `[INTERNSHIP]`
- OA first, sent within days of applying. Reported formats:
  - 2023 SWE intern test: 3 questions (add two binary strings; diamond-pattern matrix cipher; matrix min-queries with row/col removal) [B] (LeetCode Discuss 3078249).
  - 2024 SWE intern OA: 3 questions (O(n) counting; word-search in grid; time-string queries via binary search) [B] (LeetCode Discuss 4452641).
  - 1point3acres reports: "实习OA 4 hours, three questions, must be in C++" (HRT 实习OA, thread 668765) and "3 questions / 105 min, C/C++/Java allowed" (thread 468863) [B].
  - Systems intern 2021: **Codility**, 90-minute test inside a 2.5 h window, 3 medium questions, C/C++/Python/Go only (no Java), docs allowed but "do not copy code"; "correctness and performance are the most important factors, test duration also counts" [A] (avinal).
- Then 1–2 technical phone rounds. Systems intern: one 45-min **no-coding** call on Linux/Unix, C++ pointers & memory, Python/Bash, tooling [A]. SWE intern: reports of a 30-min OS/OOP/DS call and a live-coding call [B].
- Perk mentioned on 1point3acres: onsite candidates receive an Apple Watch.

**Full-time / experienced** `[FULL-TIME]`
- OA on **CodeSignal** (new-grad SWE and Algo Dev). Two distinct tests: the Algo-Dev challenge (2 h, 3 questions: two LeetCode-medium + one "harder than LC-hard", *all* hidden tests must pass within limits) and the generic CodeSignal "General Coding Assessment" for SWE (4 questions, 600-pt scale; one candidate scored 840+ and was still rejected) [B] (Glassdoor via Lazar-Ilic; ricsign playbook). Other reports: "4 questions / 2 hours, LC med/hard" (Glassdoor 2025–26 snippet); "1 hour, 4 questions (1 easy + 3 med, or 2 med + 1 hard)"; "4 easy/medium in 70 min"; "4 questions 90 min"; Shivam (C++ SWE, campus): 90-min CodeSignal, "four easy CP questions" [A].
- Phone screen 1 (30–45 min): systems/C++ trivia, sometimes no algorithms at all ("Phone interview deep C++ questions… No algo questions") [A][B].
- Phone screen 2 (60 min): live coding.
- Onsite: 4–6 rounds in one day. Reported mixes: coding (2 h, 4 questions), research/data-science round (pandas), open-ended/design (take a spec, design, absorb changing requirements), OS/systems, behavioral. One algo-engineer candidate: 6.5 h onsite after OA + two phone screens (~10 h total) [A] (OneRaynyDay, 2020).
- Language: C++ or Python for SWE (HRT posts "Software Engineer (C++)" and "(Python)" separately); intern OAs have sometimes been C++-only. AI tools explicitly prohibited (HRT careers text quoted in `alexeygrigorev` repo).
- Note: reviewers on Glassdoor describe interviewers as "rigid about the answer key" and rejections without feedback; several complain the OA rewards memorised problems.

### 2.2 Reported questions (categorised)

**(a) Arrays / strings / hashing**
- Add two binary strings `[INTERNSHIP]` 2023 OA [B] LeetCode 3078249; also in Glassdoor dump [B].
- Word search in a character grid `[INTERNSHIP]` 2024 OA [B] LC 4452641.
- Convert arrival-time strings to minutes, answer queries by binary search `[INTERNSHIP]` 2024 OA [B].
- "Remove comments from C++ source" variant; "permutation of palindrome"; "is this chemical equation balanced" – one 2h10m / 3-question OA `[unclear]` [B] Blind wy1hgi2m (also InterviewDB "Comment-Free Code Length", "Ways to Make Palindrome", "Chemical Reaction").
- Remove all adjacent AB/BA and CD/DC pairs repeatedly from a string of A–D `[unclear]` online coding round [B] Glassdoor (Lazar dump).
- Backtick-identifier converter (constants vs snake_case → camelCase); "Count fancy numbers" (digit-DP over base-4 using only digits 0/1); Max harvested crops (prefix sums over column pairs); Stock buy/sell position indicator (price series → +1/−1/0 tokens, match buy/sell patterns) `[unclear]` OA [B-] FastPrep via perixtar bank.
- Count 2×2 sub-matrices containing exactly 0..4 black cells; grid up to 1e5×1e5, ≤500 black cells `[INTERNSHIP/NG]` OA [B-] FastPrep.
- Sum of all 2-digit numbers not containing 7 or 8; smallest positive integer missing from a sequence; can a binary string be partitioned into k-sized intervals each with a given count of 1s; "very annoying string parsing with edge cases" (Algo Web Engineer OA, ~60 min on it) `[FULL-TIME]` [B] Glassdoor/Blind svkrykwf.
- Two Sum, then: two numbers closest to target, then: what changes with doubles (epsilon) `[unclear]` phone [B] Glassdoor.
- Count days between two dates; `stoi` in C with overflow corner cases (also "with 16-bit ints"); message splitting into length-limited parts ending in `<X/Y>`; count length-3 chat substrings containing a vowel; flipdigits equivalence pairs `[unclear]` [B]/[B-] quantt, PracHub.

**(b) Recursion / DP**
- Levenshtein edit distance; "Almost sorted array" (k-bounded displacement, heap of size k) `[unclear]` [B] AlgoDaily/Glassdoor 2022.
- Recursive divide-and-conquer OA problem (Algo Web Engineer) `[FULL-TIME]` [B] Blind.
- Longest path in a tree where adjacent nodes differ in label (A/B) — LeetCode "Longest Path With Different Adjacent Characters" is HRT-tagged at 97% frequency `[unclear]` [B] Glassdoor + LC tag.
- "Optimize/improve a backtracking problem" onsite round (C++ engineer, ~$600k offer reported) `[FULL-TIME/EXP]` [B] Blind 87MxP0h4.
- Can every number in an array be written as a sum of two Fibonacci numbers `[unclear]` OA [B].

**(c) Graphs / trees**
- Detect cycle in undirected graph; shortest path in matrix (BFS); max per tree level; swap every two nodes of a linked list; implement a BST; spiral matrix; next greater element in circular array `[unclear]` 2022 cycle [B] AlgoDaily/Glassdoor.
- Eulerian-path feasibility from odd-degree vertex counts (0/2/4 odd vertices, add-one-edge variant) `[unclear]` OA [B] LC 2492212 — matches LC "Add Edges to Make Degrees of All Nodes Even" (HRT-tagged 97%).
- Count empty cells within Manhattan distance K of *all* houses; naive per-cell TLEs `[unclear]` OA [B] LC 1458197.
- Root-to-leaf path sum; longest unique path in binary tree `[INTERNSHIP/unclear]` [B].
- Course-prerequisite / topo-sort, cycle detection (AlgoDaily set) [B-].

**(d) Design / OOP / simulation**
- "Build a piece of a trading system, write OO code that must be as performance-efficient as possible" — candidate solved it but every test TLE'd `[unclear]` [B] LC 628687.
- Implement an order-modification feature for a C++ client/server trading system `[FULL-TIME NG]` technical screen [B-] PracHub.
- Order book: add/cancel/match for one symbol, then "make cancel O(1)" (hash map of id → intrusive list node) `[FULL-TIME]` [C→B] techinterview.org; HRT's own public Core-Dev exercise is exactly this: **wwhrt-bookbuilder-workshop** — optimise a naive book builder on real crypto add/delete/modify events with `make measure / profile_functions / profile_lines / check` [A, official].
- Week-long take-home: implement an order router; then a Linux/networking/C++ interview `[FULL-TIME]` [B] Glassdoor.
- Take-home Verilog project, 4–8 h, self-checking grader disagreed with reviewer `[unclear, FPGA-adjacent]` [B] Glassdoor.
- Design a system to route packets between one hub and many node servers `[FULL-TIME]` onsite [B] Glassdoor QTN_8479239.
- "Implement a game with many edge cases" live coding (Algo Web Engineer phone 2) `[FULL-TIME]` [B] Blind.
- Simulations: molecular reactor 5-min queue; bird collecting sticks alternately; road with watchers; Wordle-solver (corroborated first-hand on 1point3acres thread 1145403) `[unclear]` [B-] PracHub.
- Data structures to design: deque-backed structure with O(1) index access; `read(n)` wrapper over fixed-chunk reader; insert/delete/getRandom with weighted sampling; running median (`add`, `median` sub-linear) `[unclear]` [B-]/[C].
- Design spec → design → absorb new facts on the fly (system-design round) `[FULL-TIME/EXP]` [B] Blind.
- 2-hour multi-file Python project onsite for Systems/SysTrade roles `[FULL-TIME]` [C] (NagarjunMa prep notes, unsourced).

**(e) Probability-to-code / stats**
- Roll a die 100×, flip a coin 400×: P(dice sum > #heads) — exact DP/FFT expected, Monte Carlo criticised `[unclear]` [B] Glassdoor.
- Expected draws until someone taller than the first person `[unclear]` [B] Glassdoor E470937.
- 3×3×3 painted cube: P(5 white, 1 red) = 6/27 `[unclear]` [B].
- Mean vs median for a trading P&L metric; Pearson correlation; Bayes/normal distribution 45-min math round; dice modular-sum distributions (Data Scientist) `[unclear]` [B]/[B-].
- Estimate average room size from a self-reported survey `[FULL-TIME]` [B] quantt.
- Heart-disease baseline ML model from a dataset (SWE/NG screen) [B-].

**(f) Low-level / systems / C++** (the densest category for HRT)
- Phone screen, C++ SWE full-time: `inline` pros/cons; `vector` vs `list` internals; how `malloc` works, demand paging; how the kernel hands memory to processes; `sbrk` vs `mmap` `[FULL-TIME NG]` [A] Shivam5022.
- Core Developer / low-level C++ (Blind yuqksebo): "lots of questions on STL containers, how implemented, pros and cons"; expectation that low-level programmers can write vectorised (SIMD) code; study virtual memory/paging and multithreading `[FULL-TIME]` [B].
- Glassdoor 2022 dump `[unclear]`: virtual memory vs physical (4 GB RAM, allocate 8 GB buffer — possible? how is it read?); thread vs process and threading models; IPC, named pipes; `inline`; virtual functions/vtable; `map` vs `unordered_map`; hashtable collisions/resizing; GIL; C++ exceptions vs UB on out-of-bounds; user-level threads without kernel support; STL + `malloc` internals; "deep systems questions about memory management"; TCP vs UDP; list vs vector vs array; smart pointers; compiler internals; polymorphism in depth [B].
- PracHub screen items `[unclear]` [B-]: segfault ↔ virtual-memory protection; pointers vs references; stack vs heap and probing stack growth direction; `new` vs `malloc` vs placement new; `inline` keyword vs actual inlining; large allocation + swap + `inline` trade-offs; `std::string` internals (SSO); Linux/filesystem fundamentals.
- Systems/SRE `[FULL-TIME/INTERNSHIP-systems]`: inode; RAID 5 vs 6; `du` vs `df` discrepancy; `mv *`; installing Linux on 100 nodes; soft vs hard links; troubleshoot host refusing SSH; Unix signals/zombies/reaping; Python generators vs decorators vs context managers [B] Glassdoor/PracHub; systems-intern phone call on Linux, pointers, Bash [A].
- Concurrency: two threads increment counter 1M times each, final < 2M — why/fix (quantt; also dataford) `[unclear]` [B]/[C]; SPSC lock-free ring buffer + false sharing/`alignas(64)` + memory orderings (techinterview.org "HRT devotes ~a quarter of the loop to systems", "candidates who can't articulate false sharing … rejected swiftly") [C].
- Design-round signature prompts (DesignGurus, [C]): market-data feed handler with correct book (sequence gaps, replay), pipeline reacting within a strict budget, lock-free shared structure, diagnose a latency problem (what to measure, in what order), cost of a context switch.

**(g) Math / number puzzles coded**
- Two rooks on a valued board, non-attacking, maximise sum; and the "2 roosters" variant maximising the sum *excluding* their rows/cols (O(MN) expected) `[FULL-TIME Algo SWE]` OA (Codility era, 2020) [B] LC 889638 / 498475 / 549526.
- Minimum comparisons to find 2nd largest (tournament, n + ⌈log₂n⌉ − 2) `[unclear]` [B].
- Count squares and rectangles formable from 2D points (O(n²) hashing on midpoint/distance) `[unclear]` OA [B].
- 25 bunnies / 5 lanes / no timer → 7 races (HRT warns candidates to say if they've seen it) `[FULL-TIME]` [B] quantt/Glassdoor.
- Integer → string without built-ins (`itoa`, INT_MIN edge) phone screen [B-] FastPrep.
- LeetCode HRT tags (liquidslr CSV): Detect Pattern of Length M Repeated K Times; Convert Integer to Sum of Two No-Zero Integers; Maximum Score From Grid Operations (H); Add Edges to Make Degrees Even (H); Longest Path With Different Adjacent Characters (H); Maximum Total Importance of Roads; Number of Steps to Reduce to Zero; Maximum 69 Number; Apply Operations to Make Array Zero; Largest Combination With Bitwise AND > 0; Count Unguarded Cells; Longest Common Prefix; Text Justification (H); Design Memory Allocator; Shortest Word Distance; Block Placement Queries (H) [B-].

**(h) Data manipulation**
- Onsite "data science" round: pandas, prediction tasks; SQL joins with CTEs; pandas dataframe joins; "Pandas question — expected if it's on your résumé" `[FULL-TIME / Algo-Dev-adjacent]` [B] Glassdoor.
- Python decorators, JSON tags, recursive string scoring, frequency counting with equivalent representations [B].

**(i) Take-home / debugging / code review**
- Week-long order-router take-home; 4–8 h Verilog take-home; a 2-hour Python "multi-file project" onsite for systems roles (see (d)). Debugging-on-real-infra: SysTrade phone-2 includes SSH into HRT cloud hosts to diagnose an issue [C, unsourced prep notes].

### 2.3 Difficulty & style
- OA is the biggest filter: 3–4 problems in 60–120 min with **all** hidden tests required; "Easy" here means "must be perfect and fast." Multiple reports of clean OA scores followed by silent rejection.
- Phone screens are conceptual C++/OS grilling for SWE/Core roles; algorithm-free screens are common. Onsite escalates to performance ("TLE = fail"), then to memory layout/cache behaviour for core roles.
- Total interview time for full-time loops ≈ 8–10 h; onsite 5–6.5 h.
- Internship loops: OA (C++-only in some years) + 1–2 calls; systems interns get a Linux-heavy no-code call. Difficulty of intern OA problems ≈ LC medium; less C++ trivia than full-time.
- Algo-Dev track adds a research/math phone screen (probability, Bayes, distributions) and a data-science onsite round.

### 2.4 Recurring HRT themes
Grid/matrix counting problems with large-N constraints; string parsing with edge cases; order-book / trading-system build with a performance bar; `inline`/`vector`-vs-`list`/`malloc`/virtual-memory trivia; probability estimation done exactly rather than by simulation; Linux internals for systems roles.

---

## 3. Jump Trading

Roles seen: Software Engineer (C++), Campus SWE/intern, Algorithmic Trading intern, Quantitative Researcher, SRE/infra, AI team.

### 3.1 Pipeline

**Internship** `[INTERNSHIP]`
- QR intern (1point3acres thread 1026654, "全集挂经"): **no OA**; three rounds – HR call, then a round with coding plus a trading-strategy / game-theory problem, then a further round [B].
- Summer-intern (quant) OA 2020: 3 questions in a 105-min window on Codility [B] LC 870149. Algo-trading intern superday (2013, dated): four rounds — whiteboard math, pen-and-paper brainteasers, probability, and a pure C++ coding-on-laptop round [B] WSO.
- Software Development intern (Cambridge office): behavioral phone screen, then an in-person technical round on C/pointers/arrays and a from-scratch hash map [B] WSO (2019).
- Campus SWE: 45-min on-campus whiteboard with two engineers → full onsite day in Chicago; any language allowed [B] WSO (2017).

**Full-time / experienced** `[FULL-TIME]`
- SDE (1point3acres thread 1086311, 2024–25): round 1 is an HR/background conversation on résumé and projects, then technical rounds [B]. Glassdoor summary: HackerRank OA with "hard DP and graph problems," but interviews "don't go beyond LeetCode-medium; centred on your grasp of programming"; Core-dev roles get systems/low-level questions [B]. Blind: interviews include "kernel, concurrency, CPU-architecture questions in addition to the usual algorithms" [B] (ufqxesha). Very old Glassdoor (2010): on-campus → 4-hour onsite, "fairly difficult, focused on concurrency in C/C++."
- Take-home order-book exercise (see (d)) has been used for SWE hires [A artifact, undated].
- 2025 SRE/infra code round (Chao-Xi notes): four Codility-style problems solved in Python [A] — see (a),(h).
- Language: C++ emphasised; Python accepted for research/infra tracks. NUFT note: "very engineering-focused with siloed teams," school-selective.

### 3.2 Reported questions

**(a) Arrays / strings / hashing**
- Smallest missing positive integer (Codility "MissingInteger", N ≤ 1e5, values ±1e6, O(N)) `[FULL-TIME SRE, 2025]` [A].
- Integer prices & trading indicators: given prices, a buy-indicator pattern (e.g. two consecutive rises, ignoring flat ticks) and a sell pattern, output the running position after each tick (buy +1 / sell −1) `[FULL-TIME SRE, 2025]` [A] — same family as HRT's FastPrep "stock buy sell position indicator."
- File-sync check: given source/destination listings (perm, user, size, mtime, name), return the files needing sync (missing or any field differs) subject to source-readable & dest-writable; O(N+M) `[FULL-TIME SRE, 2025]` [A].
- Maximum distance between two unequal elements (Codility OA) `[unclear]` [B] LC 686727; a second Codility question on stream/`istream_iterator` parsing with comment/delimiter handling [B].
- "Valid string: all a's before all b's" `[INTERNSHIP quant, 2020]` [B] LC 870149.
- LeetCode Jump tags: Permutation Sequence (H), Happy Number [B-]; 2021 "Jump Trading – LeetCode" PDF dump exists in `ProjectBarks/jobs-2021`.

**(b) Recursion / DP**
- Trees of varying heights with costs — DP (prompt lost) `[INTERNSHIP quant, 2020]` [B].
- Glassdoor: "hard DP and graph problems" in HackerRank OA `[FULL-TIME]` [B].

**(c) Graphs / trees**
- Decimal → 16-bit binary → 4×4 0/1 matrix; find/print a path of 0s from top-left to bottom-right `[INTERNSHIP/campus NG, 2017]` [B] WSO.
- Implement a trie in C++ `[INTERNSHIP algo-trading, 2013]` [B].
- Implement a linked list, then swap two given nodes `[FULL-TIME QR, Oct 2022]` — "pure C++/DS coding despite QR title" [B] WSO.

**(d) Design / OOP / simulation**
- **Take-home order book** (stanleywu111/jump-orderbook): parse a stream `A,<id>,<side>,<qty>,<price>` (add), `X,…` (cancel), modify, `T,<qty>,<price>` (trade); after every message print the mid-price (NAN if one side empty); every 10th message print the book; after each trade print cumulative volume at that price level; validate expected trades against fills. Author's design: prices as `uint32_t` (×1000), per-side `std::map`+`unordered_map` price-level map, intrusive order lists, id→iterator hash for O(1) cancel, custom pool allocator, error counters instead of exceptions `[FULL-TIME, take-home]` [A artifact].
- Implement a hash map from scratch (`add`, `get`), discuss implementation trade-offs `[INTERNSHIP SDE, 2019]` [B].
- QR intern round: coding + a trading-strategy problem with a game-theory flavour `[INTERNSHIP QR]` [B] 1point3acres.
- InterviewDB titles only (text behind login): "Auction" (phone), "Card Set Detection" (OA), "Executable File Query Analyzer" (OA), "Symbol Tracker", "User Creation Endpoint" (OA), "Networking and OS conceptual questions" `[unclear]` [B-].
- Design-round prompts (DesignGurus/techinterview, [C]): market-data feed handler; order gateway / in-memory order book; fast logging pipeline; store for billions of market events/day for research replay; share data between one fast writer and many readers without locks; "walk through a packet from NIC to your trading code with kernel bypass"; when FPGA beats software; profile a slow market-data processor.

**(e) Probability**
- Trailing zeros in 1000! `[INTERNSHIP 2013]` [B]; superday pen-and-paper probability [B]; QR intern game-theory problem [B]. Web-search summary of Jump QR interviews: probability + coding mix.

**(f) Low-level / systems / C++**
- Blind: kernel, concurrency, CPU-architecture questions for SWE `[FULL-TIME]` [B].
- Glassdoor 2010: concurrency in C/C++ onsite [B].
- quantt "struct with three 4-byte ints and a 1-byte flag — lay it out and why" (false sharing / padding) `[unclear]` [C].
- Blind "Jump Trading AI team interview process" thread exists (SE AI tooling / research scientist) — content not retrievable.
- Prep-site consensus [C]: memory model & `std::atomic` orderings on x86/ARM, `shared_ptr` cost, lock-free stack (CAS/ABA), SPSC ring buffer, arena/pool allocators, cache-hierarchy latency, kernel bypass.

**(g) Math puzzles coded**: swap two variables without temp storage `[INTERNSHIP 2013]` [B].

**(h) Data manipulation**
- CSV aggregation with pandas: for each company's zipped CSVs, produce per-year rows of the highest-volume day and highest-close day, returned as nested lists with datetime columns `[FULL-TIME SRE, 2025]` [A].

**(i) Take-home**: the order-book exercise above.

### 3.3 Difficulty & style
- OA problems are implementation-heavy Codility style (parsing, simulation) rather than pure algorithmics, though Glassdoor mentions hard DP/graphs on HackerRank. Interview coding is reported "not beyond LeetCode medium"; the differentiators are C++ depth and concurrency/CPU-architecture questions for engineering tracks.
- Internship loops: OA + 1–2 technical rounds; intern content is DS implementation (trie, hash map, linked list) plus math puzzles. Full-time engineering adds 4-hour onsites and systems rounds; QR full-time interviews can still be pure C++ DS coding.
- Thin 2021–2026 first-hand coverage; much of the concrete text is 2013–2020 or 2025 SRE.

### 3.4 Recurring Jump themes
Order-book build (take-home), hash map / trie / linked list from scratch in C++, Codility parsing/simulation problems, concurrency & CPU architecture, market-data path design.

---

## 4. Tower Research Capital

Roles seen: Software Engineer / Software Developer (core), Quantitative Developer (team-specific, e.g. North-Moore), Quant Researcher / Quant Trader intern (e.g. Limestone), C++ developer, Front-end, ML engineer.

### 4.1 Pipeline

**Internship** `[INTERNSHIP]` (mostly IIT campus reports)
- Résumé shortlist on CGPA (≈9.5+ for CSE at IIT-K) [A] spo-iitk 2022.
- 1-hour **HackerRank** test with three sections: 3 DSA problems (Codeforces 1600–1800, binary search / DP / graphs), probability/maths (Brainstellar-like), and C++/Python OOP + computer-architecture MCQs; DSA section decides selection [A] IITD North-Moore QD intern. Another IIT-D note: "combined test: mix of coding and quant designed to impose time pressure" [A]. Tarang Shah: "Quant: one-on-one testing guessing, mental math, probability; Software: standard coding test, interviews may follow."
- Interview 1: LeetCode medium/hard from a list, then medium-hard probability puzzles, then résumé (pandas) questions [A].
- Interview 2 (QD): core CS — parallel programming (sum & prefix-sum with p threads, complexity), computer architecture (why this C++ snippet is inefficient: branch prediction in the assembly; rewrite it), sort an extremely large array with limited RAM [A].
- QR intern 2022: test (OS/networks + CP), two technical rounds (probability, statistics, DS at CF 1900–2000, puzzles e.g. error propagation with two measured sticks), HR round = open-ended finance brainstorm [A] spo-iitk. QT intern 2023: single ~1.5 h interview mixing CS fundamentals, algorithms and puzzles [A].
- 2 offers from an IIT-D batch; "historically Tower only gives offers to the top DRs."

**Full-time / experienced** `[FULL-TIME]`
- GeeksforGeeks recruitment overview: OA (MCQ quant/verbal/reasoning + coding + CS concepts) → Tech-1 (OS, OOP, DBMS, networks, DSA medium-hard, projects) → Tech-2 (LLD/HLD) → HR [B].
- Software Developer qualification round: MCQs + 4 coding questions (SQL queries; find the bug in Python binary-tree code; formatted I/O parsing; one algorithmic) [B] GfG set-2.
- 1.5-YOE hire: 3 rounds — coding (Python string manipulation; matrix DP "max points top-left → bottom-right and back"), Round 2 (time arithmetic HH:MM + n minutes with exception handling; Python generators/yield/lambda; git), Round 3 (design patterns; "count fan blades while it's running, no gadgets") [B] GfG.
- Blind: HackerRank OA ~1 h (Python noted); C++ developer role has its own OA; Quant Developer OA ~1 h HackerRank; interviews "go beyond LC into C/C++ proficiency, systems/microprocessor concepts, OS" [B]. Glassdoor summary: 5 rounds typical (OA, virtual coding, onsite), 1–2 weeks; basic C++ (pointer, reference, const) + TCP/UDP, virtual memory, IPC [B].
- Levels: prep-guide claims 30-min recruiter → 60-min technical phone (live coding + C++ + perf reasoning) → 4–5 h onsite [C].

### 4.2 Reported questions

**(a) Arrays/strings/hashing**: Python string manipulation `[FULL-TIME EXP]` [B]; time arithmetic with exceptions [B]; "Median of two sorted arrays of different sizes," "Distinct palindromic substrings," "Reverse a sublist of a linked list" (GfG sample list) `[unclear]` [B]; LeetCode Tower tags: Using a Robot to Print the Lexicographically Smallest String, Shortest Bridge, Evaluate Division (all Medium) [B-]; CodeJeet claims Tower-tagged LC problems are 100% Medium, topics Math/DP/Tree/BST [C].

**(b) DP**: matrix path DP (there-and-back) `[FULL-TIME EXP]` [B]; OA DSA at CF 1600–1800 incl. DP `[INTERNSHIP]` [A].

**(c) Graphs/trees**: Binary tree → DLL; Alien Dictionary (topo sort) [B]; find-the-bug in binary-tree Python code (OA) [B]; Validate BST (CodeJeet) [C].

**(d) Design/OOP/simulation**: LLD/HLD round in Tech-2 [B]; "sketch an order book and defend the data structure under bid/ask; challenged on edge cases" `[FULL-TIME core]` [C] techinterview.org; ankitkushawaha `anecdotal` phone-screen items: generic thread-safe queue in C++17 with condition variables then analyse latency; max overlapping segments; median of two sorted arrays in O(log(m+n)) [C/B-]; onsite `anecdotal` items: segment tree with lazy propagation; real-time BBO aggregation across symbols; Fenwick tree → count inversions; suffix array; design co-lo ITCH handler < 500 ns; sequencer role [C].

**(e) Probability**: two random cards, P(third card's rank lies between them) `[FULL-TIME SD]` [B] GfG; Brainstellar-medium/hard puzzles, error-propagation with two sticks `[INTERNSHIP]` [A]; St Petersburg, Kelly, E[X | X>0.5] [C].

**(f) Low-level/systems/C++**
- Parallel prefix-sum with p threads + complexity `[INTERNSHIP QD]` [A].
- Why is this C++ inefficient at the assembly level (branch prediction); rewrite `[INTERNSHIP QD]` [A].
- External sort with limited RAM `[INTERNSHIP QD]` [A].
- TLB: purpose, huge pages, TLB vs cache access order, parallel access `[FULL-TIME SD]` [B].
- RISC vs CISC; shared vs static libraries; how syscalls are made in assembly and how `cout` reaches I/O; how `ls` works and filesystem layout; pipelining and branch prediction ("no pipeline vs pipeline flushed every cycle"); "how to check if a port is open" `[FULL-TIME SD]` [B] GfG.
- Basic C++ (pointer/reference/const), TCP vs UDP, virtual memory, IPC (Glassdoor summary) [B]; Linux commands (grep, ls), Flask vs Django `[FULL-TIME EXP]` [B].
- IIT-D advice: "for Tower, computer architecture and networks knowledge is essential" [A].
- [C] items: false sharing + `alignas(64)`, AVX2 dot product, SPSC queue with atomics, DPDK vs RDMA vs OpenOnload.

**(g) Math puzzles**: fan-blade counting (stroboscopic) [B].

**(h) Data manipulation**: pandas questions off the résumé `[INTERNSHIP]` [A]; SQL queries in OA `[FULL-TIME]` [B]; Indeed: "asset classes, Python, databases" for QD [B].

**(i) Debugging**: find-the-bug Python binary-tree in OA [B].

### 4.3 Difficulty & style
- Intern (India campus): fast HackerRank test where the DSA section (CF 1600–2000) dominates; interviews are LeetCode-from-a-list + probability + a computer-architecture/parallelism round for QD. QR/QT intern interviews are shorter (one 1.5 h mixed round in 2023) and puzzle-heavier.
- Full-time SD: moderate coding (Medium, Python allowed) but heavy computer-architecture/OS rapid-fire (TLB, pipelining, syscalls, libraries). Design round is a "smaller, sharper" trading-object design (order book), not web-scale.
- Little public evidence of lock-free/C++-template grilling beyond prep sites; most real reports emphasise architecture/OS concepts.

### 4.4 Recurring Tower themes
CF-style DSA under time pressure; computer architecture (branch prediction, TLB, pipelining); parallel programming; probability puzzles; pandas/Python off the résumé; team-specific process (North-Moore vs Limestone).

---

## 5. Virtu Financial

Roles seen: Software Developer / Core Software Developer / C++ core-HFT engineer, Trading System Developer, C# SWE, Quant Developer, Quant Strategist, Quantitative Trading Analyst, Data Scientist, SWE intern, QR intern.

### 5.1 Pipeline

**Internship** `[INTERNSHIP]`
- Résumé → **Codility/HackerRank OA: 5 questions / 75 min, LeetCode easy–lower-medium** (multiple reports; 2027 intern sheet says "HackerRank 5Q/75min Easy–Med") [B]; Codility 75-min "all LeetCode-easy" for an internship-trainee role (AmbitionBox) [B].
- HR round ("tell me about yourself", "what do you know about us") + brainteaser, then 2–3 technical rounds; Blind (Dec 2025) community expectation for SWE-intern technical: CS-class fundamentals, definitely networking, some LeetCode-like, open-ended coding [B].

**Full-time / experienced** `[FULL-TIME]`
- OA first, sometimes sent unprompted on Codility (Sept 2020) or ~2 h coding test before any phone screen (Nov 2020) [B] Blind; Glassdoor: "5 coding challenges with 60 or 75 min"; 4-round process "coding exercise, HR, engineer interview, in-person" [B].
- Phone with recruiter/trader including quick brainteasers (clock hands) [A] (QTA, Dublin 2021).
- Onsite: 4 back-to-back interviews for C++ Core/HFT (Oct 2025) [B]; multiple Blind reports that onsites are **brainteaser-heavy** ("4 hours straight of brain teasers" – Post-Trade SWE; "they just ask brainteasers, the coding is trivial" – NG SWE 2021; "lower than FAANG, brain teasers onsite" 2022) [B]; C++ low-latency (Dublin, Aug 2025): "they ask multithreading and concurrency" [B].
- Difficulty rating 3/5 on Glassdoor; Glassdoor also lists low-level topics for Core roles: memory allocation, fragmentation, alignment, lock-free programming, mmap/malloc internals, allocator design [B].
- Language: C++ for core/trading-system; Java/C#/Python roles exist (C# SWE virtual round: coding with test cases + OOP concepts).

### 5.2 Reported questions

**(a) Arrays/strings/hashing** (OA, mostly easy)
- HexSpeak (LC 1271) `[INTERNSHIP/NG OA]`; Count substrings with only one distinct letter (LC 1180) `[unclear OA]`; How many apples fit in the basket (LC 1196, greedy sort) `[INTERNSHIP OA]`; Minimum steps to a Fibonacci number `[INTERNSHIP/NG OA]`; Profit analysis: max-sum contiguous window of length ≤ k over monthly P&L, n ≤ 2e5 `[NG/INTERN OA]`; FIX-message reconciliation: parse `tag=value|` strings, compare tags 32/31/54/48 as raw strings `[unclear OA]`; Banking transaction simulator with InsufficientFundsError and history formatting `[unclear OA]` [B-] FastPrep, cross-validated by LeetCode Virtu tags (Array Transformation, Count Homogenous Substrings, Valid Parentheses, Design Linked List, Spiral Matrix) [B-].
- "Stabilising a row of student scores" daily simulation (n ≤ 1000) `[unclear, Quant Trading, Apr 2025]` [B] LC 6603346.
- OA of 4 problems: string parsing, bitwise, interval coverage, array partitioning `[FULL-TIME SWE]` [B-] PracHub.

**(b) DP**: "Maximise points by buying cost-multiplier cards" (DP + exchange argument) `[Data Scientist screen]` [B-].

**(c) Graphs/trees**: none reported specifically (Design Linked List LC tag only).

**(d) Design/OOP/simulation**
- Connect-Four winner detection (6×7, column drops, first win / 0 / −1 invalid) `[Data Scientist screen]` [B-] PracHub.
- Order book via two heaps: `update(side, price, qty)` `[unclear]` [C] quantt; "design a system for high-throughput market data feeds", "order-routing engine with partial fills/retries", "thread-safe LRU cache" [C] interviewchamp/techprep.
- C# SWE virtual round: coding with provided tests + OOP concepts `[FULL-TIME]` [B].
- Design basketball-shot outcome prediction (ML design) `[DS]` [B-].

**(e) Probability / brainteasers** (Virtu's signature)
- Angle between hands at 5:15; when do hands next coincide after 5:00 `[FULL-TIME QTA phone, Dec 2021]` [A] Leader-board; same on Glassdoor SWE page [B].
- General formula for expected flips until n consecutive heads `[FULL-TIME Quant Dev]` [B] AmbitionBox; "coin flips to two heads in a row" [C].
- Urn: 5R/5B/5G (then 10R), green returned, stop at 3 non-green, P(≥2 red) `[DS screen]` [B-].
- Random walk expected steps to +5; "why do you have to pay the spread?" [C] quantt.
- Market-making scenario: spread $0.10, 1M shares/day → revenue and what erodes it [C].

**(f) Low-level/systems/C++**
- C++ core/low-latency: multithreading & concurrency (Blind Aug 2025) `[FULL-TIME EXP]` [B]; Glassdoor: memory allocation/fragmentation/alignment, lock-free, `mmap`/`malloc`, allocator design `[FULL-TIME core]` [B]; TCP vs UDP and why market data uses UDP (corroborated by Blind intern thread) `[INTERNSHIP/FT]` [B/C]; "optimise a market-data feed parser for throughput" [C].
- Interview: "what database did you use, how do you test it?" [B] Indeed.

**(g)** clock puzzles as above. **(h)** none beyond DS prompts. **(i)** OA with provided test cases (C# role).

### 5.3 Difficulty & style
- Coding bar is the lowest in this cluster (80% Easy per CodeJeet; OA "lower-end LC Medium at most," finishable in ~40 of 75 min). The selective part is the **brainteaser/probability** onsite and, for core C++ roles, concurrency/memory questions.
- Internship: OA + HR/brainteaser call + 2–3 technical; intern OA problems are LC-easy classics (HexSpeak, apples, homogenous substrings).
- Full-time: same OA style, then 4-round onsite; rejection often without feedback even after passing rounds (QTA 2021).

### 5.4 Recurring Virtu themes
Codility 5×75; LC-easy string/greedy; clock-hand puzzles; expected-value coin problems; FIX/trade-simulation flavoured OA prompts; concurrency for core C++.

---

## 6. Old Mission Capital

Roles seen: Junior/entry Software Engineer, Senior Software Engineer, SWE intern (Chicago, summer & 4-person winter program), C++ trading apps.

### 6.1 Pipeline

**Internship** `[INTERNSHIP]`
- Résumé → **HackerRank OA: ~30 CS MCQs in 60 min + 2 medium–hard coding problems** → phone/video → Chicago onsite (~2 h) [B] (2027 intern application sheet, `Verdent06/Resume-Modifier`, "bottleneck: OA + low-level C++ tech"). Another report (WSO, role unclear): OA = 35 min for 25 quant problems, then one LeetCode-esque hash-map problem in 25 min where output formatting is the hard part, no Google allowed [B].

**Full-time / experienced** `[FULL-TIME]`
- Junior SWE (Glassdoor/WSO): HR screen with a senior SWE → tech onsite consisting of **DSA in Python, a Python data-analysis task, and a Linux challenge** [B].
- Senior SWE (WSO "Engineer Interview – Old Mission Capital (Chicago)"): online coding assessment = **one LeetCode-hard in one hour with no test cases provided**; phone screen on Linux fundamentals = "write a feature for a C++ library on the Linux command line"; phone screen on C++ implementation = **write an `unordered_map` class** [B].
- Onsite is physically in Chicago (flights/hotel paid; 2023 blog) [A] 54skyxenon — no question details (author notes needing OS/networks study for trading firms generally).
- Average 18 days to hire (Glassdoor). C++ explicitly required for SWE; Python secondary; Linux/low-latency networking/FIX in JDs [C].

### 6.2 Reported questions
- (a) Hash-map LeetCode-style OA problem with strict output format `[unclear OA]` [B]; LC-hard in 60 min, no tests `[FULL-TIME senior OA]` [B].
- (d) Implement an `unordered_map` class in C++ `[FULL-TIME senior phone]` [B]; add a feature to a C++ library from the Linux CLI `[FULL-TIME senior phone]` [B]; `anecdotal` items in ankitkushawaha (super-day): rolling average over last N (large N), running median from a price stream, hash map from scratch with collisions, Rule of Five class, three production examples of UB, sub-µs order book with add/cancel/modify/BBO (`inferred`) [C/B-].
- (e) `anecdotal` [C/B-]: "roll two dice, I tell you the sum, make a market on the higher die"; 50R/50B urn market-making with re-quote on new info; E[sum of two dice | sum even].
- (f) Linux challenge onsite; Linux-fundamentals phone screen `[FULL-TIME]` [B].
- (h) Python data-analysis task onsite `[FULL-TIME junior]` [B].
- Intern OA topic list (ankitkushawaha `anecdotal`): implement stack/queue under constraints; LC-medium string/array; graph traversal; simulation then optimise brute force [C/B-].

### 6.3 Difficulty & style / themes
Moderate volume of evidence, mostly second-hand. Distinctive: a **Linux command-line challenge** round, Python data task, and "implement a container class" C++ screens; MCQ-heavy intern OA. Evidence of market-making brainteasers is prep-site only. Intern vs FT: intern OA is MCQ + 2 coding; senior FT OA is a single LC-hard without tests plus two specialised phone screens.

---

## 7. XTX Markets

Roles seen: Software Engineer (core, data platform, Armenia/London/Singapore/NY), Quant Researcher, Junior Quant Analyst, Trade Analyst, SWE intern (summer, London).

### 7.1 Pipeline
- **OA** (both `[INTERNSHIP]` and `[FULL-TIME]`): "two or three hard algorithmic problems in 90–120 min"; "widely considered one of the harder OAs, pass rates reportedly 5–10%" [B/C] (quantt summary via search; Blind thread "XTX Markets interview experience – software engineering" exists but is blocked).
- **Phone screen** `[FULL-TIME]`: "around 20 general questions about C++, compiler and OS architecture" [B] Glassdoor summary.
- Deep-dive rounds `[FULL-TIME]`: RAII, pointers, memory alignment, vtable/virtual functions, variadic templates, `emplace_back`, `map` vs `unordered_map` implementation, hash functions, floating point, cache optimisation [B] Glassdoor/scoutify summary.
- Onsite: 5–6 interviews in one day in London (45–60 min each) with working researchers/engineers [B/C] quantt; Blind (Singapore, 5 YOE): 5 rounds total [B]; Blind poster asked whether it's "mostly LeetCode or advanced distributed systems" — answer: OS, networking, database knowledge assessed [B].
- QR: coding in Python + statistics/ML; NUFT: "branched out of GSA Capital; ML-first market making."

### 7.2 Reported questions
- (f) [B] C++ round topics above; [B→C] techinterview.org (claims candidate reports): "what does `std::vector` do on reallocation and why is that a problem on a hot path"; "here's a struct — reorder the fields for the cache and explain what you saved"; "this function is slow — profile it in your head, first change?" `[FULL-TIME]`.
- (d) [B→C] techinterview.org: design a market-data pipeline — fan-out to many consumers, allocation-free hot path, where to place a sequencer, reasoning about tail latency when the mean looks fine `[FULL-TIME]`. ankitkushawaha `inferred` list (order book O(1) BBO, deque/list/vector cache behaviour, `shared_ptr` deref cost, market-data normalisation across exchanges, nanosecond benchmarking artefacts, kernel bypass) [C].
- (e)/(h) Trade Analyst (AmbitionBox, June 2025): "10 strategies and the market drops 10% — how do they behave?"; "how to hedge overnight risk?" `[FULL-TIME]` [B]. QR [C]: overfitting/backtests, multiple comparisons across 100 signals, OLS/BLUE, validating a Sharpe-2.5 backtest.
- (a)/(b) OA: "2–3 hard algorithmic problems" — no verbatim text recovered.

### 7.3 Difficulty & style / themes
Hard OA (few pass), then breadth-first C++/compiler/OS oral exam (~20 rapid questions), then cache-layout and performance-profiling reasoning, and a distributed low-latency design (fan-out, sequencer, tail latency). Intern data is limited to "same OA style"; no intern-specific rounds found. Evidence thin on verbatim coding problems.

---

## 8. Quantlab (Quantlab Financial, Houston)

Roles seen: Software Engineer, Quantitative Research, FPGA.

### 8.1 Pipeline (evidence thin — all [B] via Glassdoor summaries; level `[unclear]` unless noted)
- Recruiter contact → **C++ test** (sent as a take-home/online test) → interviews [B].
- Quant/research: virtual quantitative exam (probability, statistics, calculus) → onsite [B]; another: mathematics exam → coding challenge → further rounds `[FULL-TIME QR]` [B].
- Glassdoor totals: 68 questions / 67 reviews; 9 SWE questions.

### 8.2 Reported questions
- (f) Networking-heavy: multicast, TCP, routers, switches, WAN vs LAN `[unclear, likely infra/SWE]` [B] Glassdoor.
- (e) Probability/statistics/calculus exam `[QR]` [B].
- GitHub: a candidate's interview artifact "Time-Series-CUSUM-Triple-Barrier: for QuantLab interview — CUSUM filter for label generation and triple-barrier labelling on a time series" (`zingerflame/Quantlab-Files`) `[QR/DS take-home, unclear]` [A artifact].
- No verbatim SWE coding problems recovered; no intern-specific reports. **Evidence is thin for this firm.**

### 8.3 Themes
C++ test as gate; networking (multicast/TCP) for engineering; math exam for research; ML-labelling take-home for research.

---

## 9. Wolverine Trading

Roles seen: Software Engineer (entry-level C++; "Software Engineer – Trading Systems"), SWE/Data/Quant interns (juniors+, no sponsorship).

### 9.1 Pipeline (`[unclear]` unless noted)
- Glassdoor summary: basic CS theory; C++ questions "relating to trading and automating processes"; statistics brainteasers + a couple of algorithm questions; static vs dynamic languages, Big-O; difficulty 3.1/5, ~17 days [B].
- OA exists (FastPrep has 3 Wolverine OA problems; one tagged full-time) [B-]. Dataford [C]: emphasis on clean OO architecture, core DS mechanics, "processing streaming market data under time constraints."

### 9.2 Reported questions
- (g) Permutation operations: min applications of `temp[i]=arr[p[i]]` before array returns to itself, mod 1e9+7 — LCM of cycle lengths `[unclear OA]` [B-] FastPrep (same problem appears for Geneva/Akuna/Optiver — likely a shared HackerRank library question).
- (c) "Shared interest": multigraph with weighted edges, sum per pair, find max, return max product of node ids among ties `[FULL-TIME OA]` [B-].
- (a)/(c) Huffman decoder: build trie from code table, decode bit string (≤7000 chars) `[FULL-TIME OA]` [B-].
- (f)/(e) static vs dynamic languages, Big-O, statistics brainteasers, C++ trading-automation questions `[unclear]` [B].
- No intern-specific reports found. **Evidence thin.**

### 9.3 Themes
HackerRank-library OA (graph aggregation, trie/decoding, permutation cycles); light CS theory and stats brainteasers in interviews.

---

## 10. Belvedere Trading

Roles seen: Software Engineer (entry-level 2023/2024, intern Summer 2027 at $130k/yr listed), Junior Quantitative Trading Analyst, FPGA.

### 10.1 Pipeline
- `[INTERNSHIP]` (2027 intern sheet, peer-pattern, [C]): résumé (Lever) → HackerRank/custom OA (med–hard DS&A + implementation) → 3–4 technical rounds "language-matched; C++/OOP systems; design → implement → debug trading applications" → behavioral. Not a first-hand report.
- `[unclear]` Glassdoor/Indeed summaries: 90-min online interview mixing behavioral and technical; behavioral weighting "more than candidates expect"; ~13 days to hire [B].

### 10.2 Reported questions
- (b)/(c) N×N matrix pathing from each corner to the centre, cost by cell weights and direction preferences `[unclear]` [B] Glassdoor (via search summary).
- (d) "Design a system to handle real-time trade data"; multithreading vs multiprocessing `[unclear]` [B].
- (e) Probability incl. Bayes' theorem `[unclear]` [B]; a Bayes-taxi style question appears in a Belvedere-sourced list in `signaldatascience/R-curriculum` (pre-2021).
- 1point3acres has a Belvedere tag page (count unknown); WSO lists 51 entries — not retrievable. **Evidence thin; no verbatim 2021–26 coding problems.**

### 10.3 Themes
Weighted-grid path DP, real-time trade-data design, Bayes probability, strong behavioral component.

---

## 11. Chicago Trading Company (CTC)

Roles seen: Software Engineer (C++ trading systems; Java/C++/Python), SWE intern (Summer 2027 posting: candidate picks Java/C++/Python for the interview), Quant Trading intern.

### 11.1 Pipeline
- `[INTERNSHIP]` (CTC campus page + 2027 JD, official): apply → **Codility** coding OA (SE) / aptitude assessment (QT) → behavioral (values) + technical (programming in the candidate's chosen language) [A, official]. `ricsign` playbook lists CTC under Codility [B].
- `[FULL-TIME]`: Glassdoor summary — Codility challenge with a small number of DS&A problems; interviews "focused more on C++ language and work-style questions"; C++ trading-system role covers OS-level synchronisation, concurrency, memory management [B]. Blind threads "Interview at Chicago Trading" and "First round technical interview with CTC, what to expect?" exist (blocked). quantvault "CTC OA guide" exists (blocked).

### 11.2 Reported questions
- (f) synchronisation, concurrency, memory management for C++ trading-systems role `[FULL-TIME]` [B].
- (a) Codility DS&A problems (count small) `[INTERNSHIP/FT]` [B] — no verbatim text.
- Blind thread on "How to clear HFT interviews" names CTC among firms probing metaprogramming, atomics/locks/semaphores, lock-free programming [B, indirect].
- **Evidence thin on concrete problems.**

### 11.3 Themes
Codility OA; language-of-choice technical round; C++ concurrency/memory for systems roles; explicit values/behavioral interview.

---

## 12. Geneva Trading

Roles seen: Software Engineer (C++), Junior Software Engineer, SWE intern, Quant Trader, Quant Risk intern.

### 12.1 Pipeline (`[unclear]`)
- Glassdoor (5 SWE questions, 4 reviews, 3/5 difficulty, ~22 days): several phone interviews — recruiter (behavioral) then development team lead (technical) [B].
- Scoutify/everythingquant [C]: Linux internals and system-level optimisation emphasis; Quant Trader guide exists (blocked).

### 12.2 Reported questions
- (g) "How would you swap two variables without creating a third variable in memory?" `[unclear]` [B] Glassdoor (most-cited Geneva question).
- (g) Permutation-operations LCM problem `[unclear OA]` [B-] FastPrep (shared library question, see Wolverine).
- Geneva appears in a 2025 "company-wise OA" list (AnuragSharma blog) — content not retrieved.
- **Evidence very thin; no intern-specific reports.**

---

## 13. Internship vs full-time — summary table

| Firm | Internship loop (evidence) | Full-time loop (evidence) | Key differences |
|---|---|---|---|
| HRT | Codility/CodeSignal OA 3 Q (sometimes C++-only), 1–2 calls; systems intern = Linux/C++ no-code call [A/B] | CodeSignal OA (Algo: 2 h/3 Q incl. > LC-hard; SWE: GCA 4 Q), 2 phone screens (C++/OS trivia + live coding), 5–6 round onsite incl. design & data-science [A/B] | FT adds systems depth, design, ~10 h total; intern problems LC-medium |
| Jump | QR intern: no OA, 3 rounds (HR, coding + game-theory strategy); quant-intern Codility 3 Q/105 min; SDE intern: hash map from scratch [B] | HR/background round first, HackerRank/Codility OA, C++ + concurrency/CPU rounds, 4 h onsite; order-book take-home [A/B] | FT emphasises concurrency, systems, take-home; intern = DS implementation + puzzles |
| Tower | HackerRank 1 h: 3 CF-1600–1800 DSA + prob + C++/arch MCQ; 2 interviews (LC med/hard + puzzles; parallelism/arch) [A] | MCQ+4-coding OA (SQL, bug-fix, parsing), 2 tech rounds (OS/arch rapid-fire, DP), LLD/HLD, HR [B] | FT heavier on OS/arch trivia and design; intern heavier on CP speed |
| Virtu | Codility/HackerRank 5 Q/75 min easy–med, HR + brainteaser, 2–3 tech [B] | Same OA, 4-round onsite dominated by brainteasers; concurrency for C++ core [A/B] | Similar OA; FT onsite = brainteaser marathon |
| Old Mission | HackerRank 30 MCQ + 2 med–hard coding, phone, 2 h Chicago onsite [B] | LC-hard 60-min OA (no tests), Linux-CLI C++ phone, implement `unordered_map` phone, onsite with Python DSA + data task + Linux challenge [B] | Senior FT screens are implementation-of-container and Linux; intern OA is MCQ-heavy |
| XTX | Same hard OA (2–3 hard, 90–120 min) [B/C] | + ~20-question C++/OS/compiler screen, cache/perf rounds, fan-out design, 5–6 round onsite [B/C] | Little intern-specific data |
| Quantlab | none found | C++ test → interviews; QR math exam → coding [B] | thin |
| Wolverine | none found (intern roles exist) | OA (FastPrep 3 Q), CS theory + stats brainteasers [B/B-] | thin |
| Belvedere | HackerRank OA → 3–4 tech (peer pattern) [C] | 90-min mixed behavioral/technical; grid-path DP; Bayes [B] | thin |
| CTC | Codility OA → behavioral + technical in chosen language [A official] | Codility → C++-focused interviews incl. concurrency/memory [B] | intern language-flexible; FT C++ depth |
| Geneva | none found | recruiter + team-lead phone rounds; swap-without-temp [B] | thin |

---

## 14. Source index (primary URLs recorded in the mirrors; direct access blocked in this run)

HRT: leetcode.com/discuss 3078249 (2023 intern OA), 4452641 (2024 intern OA), 889638, 498475, 549526, 1458197, 2492212, 628687; teamblind.com posts wy1hgi2m, svkrykwf, 87MxP0h4, yuqksebo; glassdoor.com E470937 / QTN_8479239 / QTN_4298492; 1point3acres threads 813599, 468863, 546991, 668765, 452382, 1145403; wallstreetoasis.com/company/hudson-river-trading-llc/interview; quantt.co.uk/resources/hudson-river-trading-interview; prachub.com/companies/hudson-river-trading; fastprep.io (hudson-river-* problems); github.com/hudson-trading/wwhrt-bookbuilder-workshop; github.com/avinal/website (hrt-interview-1.md); github.com/Shivam5022/Interview-Experiences; github.com/Lazar-Ilic/Lazar (Hudson River Trading.txt); oneraynyday.github.io (2020-09-30).
Jump: leetcode.com/discuss 870149, 686727; wallstreetoasis.com/company/jump-trading/interview; teamblind.com ufqxesha, jump-trading-ai-team-interview-process-53hgvozy; 1point3acres threads 1026654, 1163429, 1086311; zhuanlan.zhihu.com/p/352228951; github.com/stanleywu111/jump-orderbook; github.com/Chao-Xi/jxtechbook (docs/2025/sre/5jump_trade.md); interviewdb.io/question/jumptrading.
Tower: github.com/ChinmayMittal/IITD-CSE (Tower Research/north-moore.md); github.com/spo-iitk/website (2022-intern-antreev-singh-brar-tower-research-capital.mdx, 2023-intern-aditya-tanwar-tower-research-capital.mdx); github.com/devclub-iitd/Intern-Prep-Series-25; geeksforgeeks.org tower-research-recruitment-process, tower-research-interview-experience-set-2-software-developer, tower-research-interview-experience-1-5-years-experienced; teamblind.com/company/Tower-Research-Capital/posts; naukri.com/code360 Tower experiences (Mar 2022, Jul 2022 on-campus).
Virtu: github.com/Leader-board/OA-and-Interviews (2021-22/Virtu/Quantitative Trading Analyst.md); teamblind.com j4yhl2ku, 7k2nbcsw, yrksx4de, mtpx0q4u, rzp1vxep, nmivxh0o, oexf8qin, tkn20w4n, 8zzae5al; ambitionbox.com virtu-financial-interview-questions; leetcode.com/discuss/interview-experience/6603346; fastprep.io virtu-*; glassdoor.com EI_IE337434.
Old Mission: wallstreetoasis.com/company/old-mission-capital/interview (+ /senior-software-engineer); glassdoor.com E484782; teamblind.com sDfuBUc6; 1point3acres company page; 54skyxenon.github.io finale-2023; github.com/Verdent06/Resume-Modifier (reference/companies.md).
XTX: teamblind.com xtx-markets-interview-experience-6tizwwo2 and company page; glassdoor.com EI_IE2384243; ambitionbox.com xtx-markets; techinterview.org/post/3233476791; quantt.co.uk/resources/xtx-markets-interview.
Quantlab: glassdoor.com E262109; github.com/zingerflame/Quantlab-Files.
Wolverine: glassdoor.com EI_IE269559; indeed.com/cmp/Wolverine-Trading/interviews; fastprep.io wolverine-trading-*; wallstreetoasis.com/company/wolverine-trading/interview.
Belvedere: glassdoor.com EI_IE250716; wallstreetoasis.com/company/belvedere-trading/interview (51 entries); indeed.com/cmp/Belvedere-Trading/interviews; 1point3acres belvederetrading tag.
CTC: chicagotrading.com/campus; job-boards.greenhouse.io/chicagotradingcampus/jobs/4716932005; glassdoor.com EI_IE257151; teamblind.com Ue6Dw4yG, YaYkNTbR; quantvault.org/ctc-online-assessment.html; wallstreetoasis.com/company/chicago-trading-company/interview (30 entries).
Geneva: glassdoor.com EI_IE288835; indeed.com/cmp/Geneva-Trading/interviews; fastprep.io geneva-trading-minimum-number-of-permutation-operations; everythingquant.com Geneva quant-trader guide.
Question-bank mirrors: github.com/pushpa-kumar/placement-prep (raw-notes/*), github.com/perixtar/quant-interview-oa-bank, github.com/liquidslr/leetcode-company-wise-problems, github.com/ankitkushawaha1000/HFT (flagged), github.com/design-gurus/grokking-system-design (flagged), github.com/ayush-that/codejeet (flagged).
