# Coding-interview evidence for systematic research funds (2021-2026)

Firms covered: Two Sigma, D. E. Shaw, Qube Research & Technologies (QRT), G-Research, Man Group / Man AHL, WorldQuant, AQR, Renaissance Technologies, PDT Partners, Voleon, Jump Trading (research side), Aquatic Capital, Voloridge, Engineers Gate, Quadrature, Cubist / Point72, Bridgewater (tech), Arrowstreet.

## 0. How this was gathered, and how much to trust it

**Method.** 24 web searches (Glassdoor, LeetCode Discuss, Blind, 1point3acres, QuantNet, WSO, Reddit, prep sites) plus ~40 GitHub code/repository searches and ~90 page fetches. The sandbox's egress proxy blocked direct reads of glassdoor.com, leetcode.com, teamblind.com, 1point3acres.com, quantnet.com, wallstreetoasis.com, reddit.com, medium.com, levels.fyi, and every prep-company domain; only github.com / raw.githubusercontent.com were readable in full. The web-search budget was also exhausted after 24 queries. Consequently:

- Forum content (Glassdoor/LeetCode/Blind/1point3acres/WSO) is captured only through search-result summaries, **not** full pages. Where a summary named a specific question it is recorded; year/role are given only when the summary stated them.
- The richest *readable* primary sources turned out to be GitHub: an IIT Delhi internship-report series (DE Shaw, QRT), an IIT campus intern notes file (DE Shaw, JPMC-quant, Graviton, Quadeye), a personal blog (DE Shaw SDET intern), a Chinese-language interview notebook (DE Shaw), a 1point3acres GitBook mirror of Two Sigma onsite sets, a FastPrep-derived tracker of *verified* OA problems with last-seen dates (Two Sigma, DE Shaw, QRT, Point72), a large third-party compilation (`pushpa-kumar/placement-prep`) that itself cites prachub/programhelp/JoinTaro/Glassdoor/Blind/1point3acres per entry, and LeetCode "company tag" CSV exports.
- Two GitHub "interview guide" repos (`ankitkushawaha1000/HFT`, `JiawenZhu/CareerVivid` scraping techinterview.org) are explicitly self-labelled as partly `inferred` / AI-generated. Their items are included **only** where marked `anecdotal` and are always tagged **[guide-anecdotal]**; they should be read as "plausible topic areas", not as confirmed questions.

**Reliability tags used below**
- **[A]** first-hand candidate report (named source, year/role usually stated)
- **[B]** aggregator that cites candidate reports (FastPrep tracker, prachub/programhelp mirrors, Glassdoor search summaries, LeetCode company-tag exports, prep-site summaries)
- **[C]** prep-guide content self-labelled anecdotal/inferred (`ankitkushawaha1000/HFT`, techinterview.org via CareerVivid, design-gurus, quantvault) — lowest reliability
- Role tags: **INTERNSHIP**, **FULL-TIME** (incl. new grad / experienced), **unclear**

**Pre-2021 items** are included only where they are still the best available evidence for a firm and are flagged as such.

**Question categories** (per brief): (a) arrays/strings/hashing; (b) recursion/DP; (c) graphs/trees; (d) design/OOP/simulation; (e) probability/stats-to-code; (f) low-level/systems/C++; (g) math puzzles coded; (h) data manipulation (pandas/numpy/SQL); (i) take-home / data challenge.

---

## 1. Two Sigma

### 1.1 Pipeline

| Stage | INTERNSHIP | FULL-TIME |
|---|---|---|
| OA | HackerRank. SWE-intern OA reported as linear interpolation + NYC-temperature regression + "patch ratio" problem (1point3acres, via [B]). QR-intern OA 2026: interpolation + daily temperature prediction (1point3acres, [B]). Verified intern-tagged FastPrep OA problems are LeetCode-easy (flood fill, pairs divisible by N). | HackerRank, 60 min LC easy-medium for some SWE reqs; other reqs 3 LC-medium problems then a 45-min first round (Glassdoor summary [B]). Quant/QD: **3-hour** HackerRank with 1 algorithmic (medium-hard) + 2 regression/data-science problems using scikit-learn (Glassdoor [B]); "2024 3hr OA Quant" thread on 1point3acres [B]; Blind: HackerRank OA 1-3 h, Python + data-science flavoured [B]. |
| Phone screen | 45-60 min coding (CoderPad), 1-2 problems. | Same; experienced SWE with 3 YOE: "3 coding questions in the morning" + coding phone screen (Blind [B]). |
| Onsite | QR intern superday (1point3acres thread 1149327 [B]): data analysis, domain questions, coding. | SWE: report of 60-min LC-hard round then two back-to-back 60-min LC-hard rounds emphasising data structures (Glassdoor [B]). QR: 3 technical rounds — data analysis, coding, statistics — after team conversations (Glassdoor [B]); ML questions are the norm (Blind [B]). Two Sigma's own site: QR/modelling interviews emphasise research + stats + coding. |
| Language | Python or C++ candidate's choice on coding; QR OA is Python/scikit-learn. | Same; SQL not reported. |
| Difficulty rating | — | Glassdoor SWE 3.4/5, QR 3.2/5; QR hiring ~30 days. |

### 1.2 Reported questions — INTERNSHIP

**(e) probability/stats-to-code / (h) data manipulation**
- SWE-intern OA (1point3acres via [B], year unclear, ≥2023): (1) linear interpolation on a polyline (interpolate inside range, extrapolate outside), (2) NYC daily-temperature prediction with Lasso/linear regression, (3) "patch ratio" calculation (see "Calculate y/x using Patch" below).
- QR-intern OA 2026 (1point3acres via [B]): linear interpolation + daily temperature prediction (same family).

**(a) arrays/strings/hashing** — FastPrep-verified OA, intern-tagged [B]
- *Nums That Are Divisible by N* (easy): count pairs i<j with arr[i]+arr[j] divisible by N; n ≤ 1e5, values ≤ 1e9; remainder bucketing.
- *Replacing Val* (easy): flood fill from a start cell replacing all 4-connected cells with the original value (LC 733).

### 1.3 Reported questions — FULL-TIME / unclear

**(e) probability/stats-to-code (the signature Two Sigma OA family)** — role: QR / QD / SWE; years 2023-2026 [B]
- *Linear interpolation* (Glassdoor QR OA): given discrete points forming a polyline, return y for query x; interpolate if inside, extend the end segments if outside.
- *Temperature prediction* (Glassdoor QR OA): linear regression of daily temperature by town; "efficient fitting" expected.
- *Linear regression without intercept, batch then streaming* (Glassdoor QR OA): first compute slope over the whole batch, then handle streaming data where you cannot recompute from scratch. FastPrep version *Online No-Intercept Linear Regression* (easy): maintain Σxy and Σx² incrementally, output k = Σxy/Σx² after each batch (last seen 2026).
- *Piecewise Linear Interpolation and Extrapolation* (FastPrep, full-time, medium, last seen May 2026): n points, sort by x, answer q queries with y = ya + (yb−ya)(xq−xa)/(xb−xa); n,q ≤ 2e5; tolerance 1e-6; expected O((n+q) log n). Sister variant *Linear Interpolator* adds tie rules for duplicate x (smallest y if x_input ≤ x, largest if >).
- *Calculate y/x using Patch* (FastPrep, easy): integer y/x rounded half-up to 2 decimals as a string; "-0.00" must print as "0.00" — fixed-point care.

**(a) arrays/strings/hashing**
- *Balanced Split String with Wildcards* (FastPrep + programhelp, HackerRank, 12 May 2026): string of ( ) [ ] and ?; count splits into two non-empty parts such that each part can be *rearranged* into a balanced bracket sequence; n ≤ 1e5; prefix counting.
- *Closest Color* (FastPrep + programhelp, same OA session, easy): 24-bit binary RGB strings → nearest of Black/White/Red/Green/Blue by Euclidean distance, "Ambiguous" on ties.
- *Decode a custom-encoded string* (JoinTaro, SWE NYC, 7 Nov 2025, HackerRank OA): "moderate, not on LeetCode"; candidate ran out of time; no offer.
- *First non-repeating character*; *Flatten an N-dimensional array* (programhelp, SWE phone/onsite, [B]).

**(c) graphs/trees**
- *Sewer Drainage Partition* (FastPrep, full-time OA, medium): tree given as parent array, each node has inflow; cut exactly one edge to minimise |flow(A) − flow(B)|; subtree DFS sums, answer min |total − 2·subtree|. prachub reports the same problem paired with an *IPO share allocation* problem (round-robin by price tier then timestamp) in a two-part new-grad SWE OA.
- LeetCode company-tag export (all-time, 19 problems, [B]): Random Pick with Weight (freq 100), Number of Provinces, Maximum Subarray Sum with One Deletion, Multiply Strings, Wildcard Matching, Longest String Chain, Game of Life, Power of Four, Intersection of Two Arrays, Maximum Sum Circular Subarray, Parallel Courses III, Word Search II, Merge k Sorted Lists, Minimum Space Wasted From Packaging, Design Memory Allocator, Valid Parentheses, Meeting Rooms II, Number of Islands, House Robber III. Last-6-months tags: Multiply Strings, House Robber III. CodeJeet's independent count of 19 recent Two Sigma tags: 16% easy / 53% medium / 32% hard; topics Array, String, DP, Math, Simulation.

**(d) design / OOP / simulation**
- *Implement a limit-order matcher with price-time priority* (prachub, SWE technical screen, [B]): up to 200k orders, values ≤ 1e9, O(n log n), heap vs tree trade-off, partial fills.
- *In-memory relational database* (prachub, SWE screen): support CREATE/INSERT/SELECT with AND-only WHERE, ≤10k queries/rows, malformed statements ignored, return insertion order.
- *Tax-loss-harvesting optimizer* (prachub, SWE system design): formulate optimiser (decision vars, wash-sale constraint, Big-M, multi-period), design the backtest (point-in-time data, sensitivity), run ~30k backtests (task granularity, concurrency).
- *Design a secure internal bank messaging system* (programhelp): real-time delivery, cross-device sync, 7-year retention, encryption at rest/in transit.
- 1point3acres onsite "sets" (GitBook mirror `GuanyiLi-Craig/two-sigma-interview`; **likely 2019-2020, pre-window but still the most detailed onsite record** [B]): RPN calculator class with extensible operator factory; remove a subtree from an array-represented tree in O(n) space; match two ascending blocking-queue streams for pairs with difference < 1 (threads); diagnose a slow web service; wildcard matching (* and ?) with DP + backtracking; power of 4 via bits; iterator wrapper returning only multiples of 5; Conway's Game of Life incl. infinite/sparse grid; text-editor OO design with rope, undo/redo; debug Guava AbstractMultimap; LRU and LFU cache incl. concurrent LRU; five "best time to buy/sell stock" variants; debug a buggy median-of-two-sorted-arrays; ATM OO design; refrigerator producer-consumer with synchronisation; internal news-feed system design; "super stack" with avg/min/max/mode; multiply two numbers as strings; populate next pointers; regex matching; set intersection complexity; compare sorting algorithms; **CSV of city power & temperature → daily max per city**; **weighted sampling with a binary indexed tree**.
- Design-gurus (C, "design-and-implement" format): build an in-memory time-series store / scheduler / rate limiter as working code in the hour; design a backtesting platform (no look-ahead leakage, deterministic replay, cache by inputs); feature store with point-in-time semantics.
- Blind Two Sigma QR interview (1point3acres "Two sigma quant 面试", [B]): ~1.5 h — **LRU cache**, **median in a data stream**, then ML/Bayesian questions on avoiding overfitting and how to measure error.
- Blind/levels.fyi QR summaries [B]: "what data types would you use to predict a stock within 10 minutes and how would you process the data" (creative, open-ended); follow-ups on optimising solutions test CS depth.

**(f) low-level / C++** — only [C] guide-anecdotal items exist: unique_ptr vs shared_ptr, move semantics, false sharing, lock-free stack with atomics, constexpr Fibonacci, "1M messages/s market-data processor", "10-year tick backtesting framework". Treat as topic hints only.

**(e) probability puzzles (verbal)** [C]: expected flips to consecutive heads; fair coin from biased coin.

**Senior full-stack loop (2023, `sumitsingh4411/interview-rounds`, medium reliability [B])**: DSA — rotting oranges, group anagrams, longest palindromic substring; machine coding — nested collapsible comment thread, colour picker; system design — analytics/metrics dashboard backend, news feed fan-out; deep-dive — deadlock prevention, CSS grid vs flexbox, code-splitting.

### 1.4 Difficulty / style
- OA: LC easy-medium for the algorithmic part, but the *data-science* part (regression/interpolation) is where QR/QD candidates report time pressure; 3-hour OAs are reported for quant tracks. Clean numerics matter (fixed-point rounding, streaming sums, 1e-6 tolerance).
- Onsite SWE: LC medium-hard, occasionally hard; strong emphasis on data structures, then OO/design-and-implement.
- QR: coding is weighted roughly equally with stats/ML; ML questions (overfitting, error measurement, Bayesian reasoning) appear in the same round as coding.
- Internship vs full-time: intern OA problems are noticeably easier (LC-easy tags) but share the interpolation/regression theme; the QR-intern superday mirrors the full-time QR loop (data analysis + coding + stats).

### 1.5 Recurring themes
Linear interpolation/extrapolation; regression from scratch (batch and online); streaming statistics (median, percentile, running sums); LRU/LFU; matching engines / order books; in-memory DB or time-series store built live; ML-overfitting discussion for QR; wildcard/regex matching; Game of Life.

---

## 2. D. E. Shaw

### 2.1 Pipeline

| Stage | INTERNSHIP | FULL-TIME |
|---|---|---|
| OA | India campus (Technology Developer Intern, IIT Delhi 2025 [A]): ~1h20m, 3 DSA problems with per-question slots (~20/20/40 min); topics DP, greedy, bitmasking, brute-force+optimisation. SDET intern (Aug, 5th semester, 2025 blog [A]): 2 DSA + 20-25 aptitude MCQs. Older campus format [A, pre-window]: HackerRank 50-min coding (2 Qs) + 20-min technical MCQ (DS/OS/DBMS/OOP/CN) + 20-min aptitude. | India MTS/SMTS (LeetCode Discuss Oct 2024 / Jan 2025 [B]): HackerRank with 8 CS-fundamentals MCQs + 8 aptitude + 3 coding. US/UK SWE (June 2022 [A]): HackerRank then CoderPad technical. Quant Analyst track: 60-min phone on probability and/or coding; probability/stats test with a small data-analysis component on a provided dataset (techinterview/quantt [B]). Select senior roles: 4-8 h take-home modelling/coding (techinterview [C]). |
| Rounds | 2 technical (~30 + ~20 min) + HR for interns [A]; some intern loops 2 × 45-60 min. | Onsite 5-7 interviews in one day (quantt [B]); India: 3-4 technical + HR; superday structure of coding ×2, C++/systems, probability, system design, behavioural [C]. |
| Language | C++ dominant on Indian campus; Python for SDET/quant. | C++/Python/Java; SQL asked in India SWE loops (LeetCode Discuss [B]). |
| Difficulty rating | — | LeetCode tag export: 124 problems, 12 easy / 74 medium / 38 hard (CodeJeet count [B]). |

### 2.2 Reported questions — INTERNSHIP (all India campus, 2024-2025 unless noted)

**(b) recursion/DP, (a) arrays**
- Count inversions; interviewer rejected `ordered_set` and hinted "use pre-computed answers" → merge-sort style recursion, on paper, with complexity (OA/round-1, IIT intern notes [A]).
- Car overtaking: given velocities and start positions of N ≤ 1e5 cars, count overtakes (round 2 [A]).
- Find any peak element in < O(n) (round 2 [A]).
- Excel column number → letters (round 2 [A]).
- DP "similar to AtCoder DP contest" (round 1 [A]).
- Event scheduling: events given as [s, e, t] repeating every t days within [s, e]; at most one event per day, maximise events attended (round 1 [A]).
- Pattern question on (1+x)^n coefficients (round 1 [A]).
- Product of array except self (SDET intern, 2025 [A]).

**(c) graphs/trees**
- Graph problem "likely cycle detection" (IIT Delhi TD intern 2025 [A]).
- Undirected graph with some hospital nodes: max edges deletable so every node still reaches a hospital; follow-up with weights → minimum-weight forest (round 1 [A]).
- DSU implementation, then optimise with a map (round 1 [A]).
- Implement a BST using only arrays (no structs/classes) (round 1 [A]).
- Complete binary tree check; internal implementation of `set` (round 2 [A]).

**(d) design/OOP/simulation**
- Design a Banking System class in C++ with iterative feedback (IIT Delhi TD intern round 2, ~20 min [A]).
- IPL tournament OO design with real-time statistics queries (two independent reports; one candidate "made it too complex" [A]).
- Calculator class with overloading, inheritance, polymorphism, virtual functions/vtables (round 2 [A]).
- Data structure: push(x), pop() removes the most frequent element, ties broken by most recent (LC 895 max-frequency stack) (round 1 [A]).
- LFU cache with optimal insert/evict complexity (round 2 [A]).
- Interval-based implementation problem using a hashmap, with solutions for different constraint regimes (round 1 [A]).

**(f) low-level / systems / C++** (very heavy in Indian intern loops)
- Inheritance, smart pointers (IIT Delhi [A]); virtual functions/destructors, vtables/vpointers with output prediction on code snippets; virtual inheritance (multiple reports [A]).
- Memory allocators, stack vs heap, virtual memory, paging, segmentation; "many browser tabs lag → page swaps"; semaphores vs mutexes, deadlock conditions, Banker's algorithm; threads vs processes; CPU- vs I/O-bound; multithreading vs concurrency; scheduler types [A].
- "Process 50 GB of data with 8 GB RAM and almost-full disk" [A].
- Socket.IO vs C socket API, TCP vs UDP for a chat feature [A].
- Docker, Python decorators, multithreading, OS basics (SDET intern [A]).

**(g) puzzles**
- 100 prisoners and a light bulb [A]; everyone picks a number, those below 2/3 of the average win — what happens under optimal play [A].

Observed tip from a rejected intern candidate [A]: "They play a rapid-fire game where they pick a word from your answer and ask the next question on it — don't use any word you can't defend in depth."

### 2.3 Reported questions — FULL-TIME / unclear

**FastPrep-verified OA problems (HackerRank; role mostly "unknown", one tagged full-time; last seen 2025-2026) [B]**
- (a) *Maximum Size Subarray Sum*: for each element, size of the largest window where it is the unique max; sum sizes (monotonic stack). Twin: *Calculate Region* (student heights).
- (a) *Find Number of Interesting Pairs*: count pairs with |a−b|+|a+b| = S (reduces to 2·max(|a|,|b|) = S).
- (a) *Minimum Frames for Equal Chunks* (easy, make every element even).
- (a) *Non-Alternating Binary Partitions*: split a binary string into minimum pieces of length ≤ frame, none perfectly alternating.
- (a) *Keep Them Apart*: delete minimum elements so equal values are ≥ d apart (greedy per value). Also seen at QRT.
- (a) *Subarray Removal* / *Count the Number of Incremovable Subarrays II* (LC 2972).
- (a) *Find Maximum Beauty*: delete elements to maximise count of positions with a[i] = i (LIS-style).
- (a) *Minimum Operations to Make Array Equal*: operations add +1,−1,+1,−1… over an even-length subarray; feasibility via difference/prefix parity.
- (b) *Array Break* (hard): count pairs (b non-decreasing, c non-increasing, b+c = arr) mod 1e9+7, n,values ≤ 3000, DP with prefix sums.
- (b) *Get Minimum Cost*: paid server vs free server that only works while the paid server is busy; greedy.
- (c) *Tree Points* (hard): collect A[j]−K or floor(A[j]/2) while halving all descendants; tree DP.
- (a) *Police Station*: choose `capacity` coordinates minimising distance to nearest station (binary search / heap).
- (a) *Maximum L1 Distance Between Equal-Length Subarrays* — **phone screen**, n ≤ 2000, O(n²) over diagonals.

**LeetCode Discuss / CodingKaro reports (India SDE/MTS/SMTS, 2021-2025) [B]**
- Find all articulation points in a graph; partition array into two subsets minimising |sum difference|; smallest subarray length containing the max-frequency element; OOP on abstract class vs interface; low-level design discussion; SQL questions. Recommendation from posters: 300+ LC problems, DSA + OOP.

**LeetCode company-tag export (3-month window, [B])**: Count Binary Substrings, Reorganize String, K-th Symbol in Grammar, Longest Repeating Character Replacement, Sliding Window Maximum, Count Vowel Substrings, Shortest Path in a Grid with Obstacles Elimination, Max Consecutive Ones III, Minimum Number of Refueling Stops, Asteroid Collision. All-time top: Binary Tree Cameras, Find Minimum Cost to Remove Array Elements, Maximum Number of Subsequences After One Inserting, Minimum Number of Taps, Minimum Size Subarray in Infinite Array, Letter Combinations, Maximum Points After Collecting Coins From All Nodes, Maximum Subsequence Score, Maximum Points Tourist Can Earn, Find Peak Calling Hours (SQL), Minimize Connected Groups by Inserting Interval, Minimum Runes to Add to Cast Spell, Relative Sort Array, Removing Minimum Number of Magic Beans, Minimum Cost Walk in Weighted Graph, Number of Subarrays With AND Value K, plus a long tail (LRU Cache, Median of Two Sorted Arrays, Trapping Rain Water, Coin Change II, Text Justification, Find Median from Data Stream, Basic Calculator II, Insert Delete GetRandom O(1)).

**Live rounds, US/UK/Asia [A]/[B]**
- SWE, June 2022, HackerRank → CoderPad [A]: implement a calculator; implement a queue on an array with dynamic resizing. Interviewer described the role as "50/50 computer science vs maths".
- DE Shaw interview (Chinese notebook `goldin2008/Note`, undated ≈2024-25 [A]): given an expression without parentheses (e.g. `1 + 2*3 + 4*5 + 6`, + and × only), add any number of parentheses to maximise the value and return it. Insight: wrap every maximal run of additions between products. (The same notes then list a **CodeSignal 90-min / 4-question OA**: coin change closest to a target, count string pairs that are suffixes of each other, "cut trees and report the longest remaining road segment after each cut" — the firm for this OA is not explicitly labelled; DE Shaw is known to use HackerRank, so attribution is unclear.)
- Senior full-stack 2023 (`sumitsingh4411`, medium reliability): sort colors; word ladder; max depth of binary tree; virtualized chat window that loads older messages; token-bucket rate limiter service; design YouTube; design Google-Docs-style collaborative editor; tree shaking; implement Promise.all; WeakMap/WeakSet.
- Quant Analyst / QR track (quantt, techinterview, datainterview summaries [B]): probability brainteasers, EV, conditional probability; e.g. expected rolls until every face of a die has appeared; coding "more likely to involve implementing a backtest, writing a simulation, or manipulating time series in Python"; onsite 5-7 interviews.
- WSO "Crazy D.E. Shaw phone interview question" thread exists (quant phone screen) — page blocked, content not captured.

**System design (senior SWE) [C]**: market-data pipeline (collect/clean/store for research), order-management system, pre-exchange risk check layer, research-job orchestration with resource governance; interviewers push on failure modes and "events/s, bytes/event, storage/year" arithmetic. techinterview.org sample coding [C]: topological order of research-job dependencies with cycle detection; running median in O(1)-query fixed structure; max profit with cooldown; bounded-memory top-K instruments by volume; simplified limit-order-book matcher.

**Probability round [C]**: two eggs/100 floors; expected flips to HH; expected rolls to see all faces; ±1 random walk to N; Bayes bag; 99% test base-rate; expected shuffles until sorted; ace-of-spades stopping.

### 2.4 Difficulty / style
- India campus (both intern and full-time) is the most C++/OS-heavy loop in this cluster: expect virtual-function internals, memory, concurrency, plus 1-2 medium-hard DSA and an OO design (banking system, IPL tournament, calculator). Paper coding still occurs.
- OA problems are LC medium with a real hard tail (tree DP, counting DP); time per question is enforced.
- US/UK SWE loops: HackerRank → CoderPad → onsite; mixed CS/maths.
- QA track: probability-first; coding = simulation / backtest / time-series in Python rather than LeetCode.
- Intern vs full-time: same OA platform; intern OAs are shorter (2-3 problems, ~80 min) with aptitude MCQs; intern interviews are shorter (20-60 min) and lean on projects + OS/C++; full-time adds SQL/LLD/system design and (for India) 8 CS MCQs.

### 2.5 Recurring themes
Monotonic-stack "range where I am the max" problems; subarray-removal/incremovable; greedy scheduling with a twist; tree DP; virtual functions/vtables; OS memory/concurrency rapid-fire; OO design of a small domain system; calculator/expression evaluation; LRU/LFU; probability puzzles for QA.

---

## 3. Qube Research & Technologies (QRT)

### 3.1 Pipeline
- **INTERNSHIP** (Quant Developer Intern, Mumbai, IIT Delhi 2025 report [A]): OA with two sections — coding (2 easy-moderate, CP-style) + quant (general probability & puzzles); "solving almost all correctly was crucial"; CGPA drove shortlisting. Then round 1 (aspirations, projects, experience) and round 2 (technical problem-solving with pseudocode on the spot). Some candidates had only one round.
- **INTERNSHIP** (Quant Research intern, Zurich, WSO [B], page blocked): exists; not captured.
- **FULL-TIME** QR (QuantBrainteasers guide [B]): theoretical ML interview (random forests, linear regression) → **two-week practical ML project (take-home)** → remote technical discussion of approach/results → longer onsite with in-depth technical questions. Glassdoor summaries [B]: rounds "mostly behavioural" with technical rounds on gradient descent and classic quant problems; interns/QR get conditional probability, combinatorics, random-walk questions; research candidates get Python questions, data work or **code-refactoring** tasks; quant-technology candidates get deeper C++/algorithms/systems. Glassdoor difficulty 3.07/5, 46% positive; QD and Analyst loops rated easiest. A student-society summary (ichack) [B]: LeetCode-style, mostly easy, then onsite day with multiple teams.
- Platform: Codility or HackerRank (tracker in `Maseeek/QuantML-InternHQ` [B]); assessment focus "vectorised math, time-series signal processing, C++/Python algorithms".

### 3.2 Reported questions
- **FULL-TIME (New Grad) OA, FastPrep-verified [B]**: (a) *Keep Them Apart* (delete min elements so equal values are ≥ d apart, n,d ≤ 1e5, greedy per value); (a) *Array Nullification* (decrement-by-1 or nullify-if-zero-and-change[i]>0, min ops or −1).
- **INTERNSHIP OA [A]**: 2 easy-moderate CP problems (unspecified) + probability/puzzle MCQ section.
- **INTERNSHIP round 2 [A]**: on-the-spot problem solving, pseudocode.
- **FULL-TIME QR [B]**: gradient descent (explain/derive), random forest vs linear regression theory, conditional probability / combinatorics / random walk; Python refactoring task; 2-week ML project (dataset/task not disclosed).

### 3.3 Difficulty / style / themes
Coding bar is low-to-medium (CP-style easy-medium; "mostly easy LeetCode"); the discriminators are the probability section, ML theory, and the two-week project + defence. Evidence is thin overall; intern data is from a single 2025 Mumbai report.

---

## 4. G-Research

### 4.1 Pipeline (FULL-TIME QR; internship loop reported as the same components)
- Official "Quantitative Researcher Assessment Process Guidance" PDF (gresearch.com, 2020, still linked 2025) [A-official]: phone screen → **coding test** + **quant quiz** → technical interviews → manager interview.
- Quiz (QuantNet + techinterview summaries [B]): **10 multiple-choice questions, 5 options each, 90 minutes**; mixes easy items with real maths, e.g. "find the minimiser of a given cost functional and how the cost scales with the initial condition"; topics probability, statistics incl. OLS, linear algebra, calculus/ODEs. The firm says the test assesses basic skills more than advanced maths.
- Coding test: firm recommends **Project Euler**-style bite-size maths-with-code problems, plus Codility/Kaggle/TopCoder practice; HackerRank or proprietary platform with 2-4 problems reported [C].
- Aptitude/psychometric (SHL-style numerical/logical/abstract) reported as a first screen for some tracks [C].
- 2025 "Quantitative research and machine learning interview prep recommended reading" PDF exists on gresearch.com (blocked; title only).
- Interviews: QRs "pushed hardest on mathematics, probability and ML"; SWEs on production C++ and Linux internals; "code you can defend line by line" (techinterview [B]).
- Difficulty: Glassdoor QR page exists (blocked); Blind mentions G-Research alongside Jane Street ML-researcher prep threads.

### 4.2 Reported questions
- **Quiz item (FULL-TIME QR, QuantNet [B])**: minimiser of a cost function and scaling with initial condition (variational/ODE flavour).
- **Coding test [C guide-anecdotal]**: LRU cache; streaming median in O(log n); (inferred) topological sort / DAG shortest path, interval merge, grid min-cost DP.
- **Technical interview [C]**: merged rate of n Poisson processes (anecdotal); move semantics, race conditions with std::atomic, strict aliasing, CTAD, object lifetime, Linux scheduling/CPU affinity, NUMA (all inferred, SWE-track).
- **Research interview [C, inferred]**: design a backtester and name look-ahead/survivorship/overfitting failure modes; HMM for regime detection; L1 vs L2 vs elastic net and sparsity for signal selection.
- Interns: G-Research runs ML-research and NLP internships (London, Workday postings 2027) and "explicitly accepts undergraduates with outstanding maths/CP ability" (student tracker [B]); no intern-specific question reports were found — **evidence thin**.

### 4.3 Style / themes
Maths-first (OLS, linear algebra, ODE), Project-Euler-style coding (maths problems requiring computation), C++ depth for engineering roles. No candidate-verbatim coding problems were recoverable in this run.

---

## 5. Man Group / Man AHL

### 5.1 Pipeline (FULL-TIME Quant Developer; internship = "AHL Summer Intern Quant Talent Programme", no question reports found)
- Glassdoor QD summary [B]: **take-home "homework" = one SQL query + a Python class that generates random numbers with given discrete probabilities**; then a two-part phone interview (discuss the homework, then general CS); later rounds include **pair programming**, algorithms/data structures on paper, and conversations about you/the firm. No speed-arithmetic or market-making game.
- Platform: CodeSignal / take-home (tracker [B]); focus "Python streaming concepts, architectural design, data-processing pipelines".
- Stack: Python-first (numpy/pandas/scikit-learn, Linux); AHL open-sources ArcticDB etc. A 2024 candidate's prep repo (`VikSil/Reengineering_Man_AHL`) confirms the Python-engineer job description but "nothing came of the interview" — no questions.
- Man AHL "Women in Quant" and "Summer Intern Quant Talent Programme" (Sept 2025 posting) exist; **intern loop evidence: none**.

### 5.2 Reported questions
- (h) SQL query (unspecified) — take-home.
- (e)/(d) Python class sampling from a discrete distribution — take-home; follow-up phone discussion of the code.
- (a)-(c) Algorithms/DS on paper; pair-programming exercise (unspecified).
- (h)/(i) "How would you build an alpha signal from earnings-call transcripts?" is attributed to "Man AHL, Two Sigma" in one portfolio repo's comments (`VedantUpasani46/quant-portfolio`) — low confidence.

### 5.3 Style / themes
Take-home + discussion; interviewers dig into your code and research; polish and reasoning over trick questions. Evidence thin (one Glassdoor-derived report).

---

## 6. WorldQuant

### 6.1 Pipeline
- **FULL-TIME QR (Glassdoor summary [B])**: screening online tests — **maths (many problems, wide variety)** + **programming (3 easy problems on data parsing and "filling in gaps")**; then 3 technical interviews (maths, programming, DS/finance), each a few warm-ups + 2 harder problems; then team interviews on your research/experience. Difficulty 3.5/5.
- **INTERNSHIP (India campus, 2023)** [A]: IIT Delhi — **2-hour test** on probability, number theory, discrete maths plus some ML questions, described as hard; shortlist CS/MT/EE/AM/PH with 8.5+ CGPA. IIT Kanpur — interview: interest in finance & projects, puzzle "create an equal-probability event from a biased coin", a Bayesian-probability puzzle, one maths question, HR.
- Platform: HackerRank; some research roles use a proprietary WorldQuant portal; "statistical models, pandas manipulation, Python OOP" (tracker [B]).
- SWE/C++ roles: one or two video calls mixing coding with C++/systems, then onsite C++ round and a finance/research-knowledge round [C].
- CodeJeet tag stats [B]: only 4 tagged questions, 3 of them Hard; DP, heap, string, recursion, array; 25-30 min per problem.

### 6.2 Reported questions
**FULL-TIME QR [B]**
- (g)/(e) live coding: **compute a square root** (Newton/binary search).
- Pseudocode reading: "what will x equal after this code runs".
- Probability: coin problems (biased and unbiased), "find the expectation of …", variance; linear algebra with intersection of geometric objects in 3-D; arithmetic "math enigmas"; Green Book questions in team interviews.
- (h) OA: three easy programming problems on **data parsing and filling gaps** in data.

**INTERNSHIP (2023, India) [A]**
- 2-hour written test: probability, number theory, discrete maths, a few ML questions.
- Interview: biased coin → fair event (von Neumann trick); Bayesian puzzle; one maths question.

**[C guide-anecdotal] (SWE/C++ track)**: sliding-window-max class; max drawdown from prices; search rotated sorted array; top-K alpha signals from a stream; std::move/forward; unordered_map internals; when to avoid virtual functions; expected flips until "HT"; autocorrelation vs cross-correlation. OA (anecdotal): count islands; volatility & Sharpe from daily returns; expected flips for 3 consecutive heads with bias p; expression parser/evaluator.

### 6.3 Style / themes
Maths/probability test volume is the filter; coding is easy (parse data, fill gaps, sqrt) for QR; C++ depth only for engineering roles. Finance-domain round (alpha types, information ratio, data-snooping) for research consultants. Intern test is maths-heavy and hard; intern interview is short puzzle + fit.

---

## 7. AQR Capital Management

### 7.1 Pipeline (FULL-TIME; internship = Summer Analyst — no intern question reports found)
- Glassdoor/Blind [B]: **CodeSignal** test for some roles ("don't know how to prepare for AQR CodeSignal test" thread); technical screen → coding or modelling exercise → behavioural/research-fit. QR and Summer Associate loops rated easiest at the firm.
- techinterview (CareerVivid) [C]: 1-2 probability/stats rounds (Bayesian reasoning, inference, regression diagnostics); 1-2 coding rounds, Python primary, "algorithms with practical engineering flavour"; research/portfolio discussion; domain depth.

### 7.2 Reported questions
- (a) "Sorting and Python code refactor" — Quant Software Developer, Glassdoor question page [B].
- (a) Time and memory complexity of sorting algorithms; two-pointer and sliding-window problems (Glassdoor [B]).
- (e) Derive the MLE for a given distribution; explain linear regression intuitively and derive the OLS estimate (Glassdoor [B]).
- (h) "How do you optimise a slow computational loop in Python or R when processing large financial matrices?" (Glassdoor [B]).
- Factor construction: explain and justify construction method, how to optimise it (Glassdoor [B]).
- [C] samples: maintain net positions from partial-fill trade stream and compute realised PnL; rolling correlation/covariance with numerical stability; max-profit window with limited round trips (DP); reconcile trade vs position snapshots via joins; sorting choice for nearly-sorted feeds; design a backtesting engine (20 years × 10k instruments), EOD PnL pipeline, versioned factor-data platform.
- WSO has 28 AQR interview entries (blocked, not captured).

### 7.3 Style / themes
Python refactoring/vectorisation, sorting-complexity trivia, OLS/MLE derivations, factor-investing domain; LC-medium at most.

---

## 8. Renaissance Technologies

### 8.1 Pipeline (FULL-TIME; RenTech has no public internship pipeline — student trackers note it "interviews some normal people for SWE, other roles extremely difficult")
- Glassdoor [B]: 18 reports; difficulty 3.39/5, 44% positive; Quant and SWE hardest, Data Programmer/Researcher easiest; researcher hiring ~46 days. Referral/academic-network driven (techinterview [C]).

### 8.2 Reported questions [B]
- Probability/stats "Green Book style, easy-medium".
- **Three LeetCode-hard coding questions** in one loop (role unclear).
- Brainteasers medium and hard.
- C++: "which features from recent C++ version updates would you include" (SWE).
- [C] samples (unverified): rolling VWAP / moving average over a tick stream with eviction; SPSC ring buffer with memory ordering; parse binary exchange messages with zero allocations; top-of-book O(1); optimal-stopping EV puzzle.

### 8.3 Style — evidence thin; LC-hard coding + Green Book probability + C++ standards knowledge.

---

## 9. PDT Partners

### 9.1 Pipeline
- **FULL-TIME QR** (Glassdoor/QuantNet summaries [B]): ~30-min phone → onsite of background + technical; PhD-only for QR; research presentation of past work; standard probability + open-ended probability modelling; coding is "practical data science in Python — cleaning data, implementing models, computing statistics, visualisations" rather than competitive programming (InterviewQuery [B]).
- **INTERNSHIP**: PDT recruits undergrads mainly for SWE (some SWE/QR hybrid) — student trackers [B]; Summer 2027 SWE and Systems internships list a "first-round technical assessment" (Greenhouse posting [A-official]); no intern question reports found.
- [C]: OA 60-90 min, 2-3 problems, possibly with a stats/maths item; superday 4-6 h (coding ×n, quant/stats, design for seniors, research discussion, behavioural).

### 9.2 Reported questions
- [B] "standard quant probability questions"; "open-ended probability modelling"; presentation of past research; Python data-science coding.
- [C] anecdotal: LRU cache; validate BST; expected flips to HH; Var(X+Y) for correlated normals; hash-map resize amortisation; top-k frequent in a stream; count islands; "what is a martingale, give a finance example"; R² = 0.95 — trust it?; Kelly criterion; design real-time PnL for 10k positions at 1M events/s; design a backtesting framework.

### 9.3 Style — evidence thin; research-presentation-centred for QR; Python data work over LeetCode.

---

## 10. Voleon Group

### 10.1 Pipeline
- **FULL-TIME** (Glassdoor summary [B], 221 reviews, difficulty 3.31, 32.8% positive): recruiter screen → technical screen → **4-part virtual onsite, one round being a two-hour coding session of multi-part real-world problems**; topics ML, data manipulation (SQL/Python), stats/maths, behavioural. AI-researcher loops ~90 days. Research roles: interviewers "probe the limits of knowledge on topics listed on your resume", value first-principles reasoning on ambiguous problems.
- **INTERNSHIP / NEW GRAD SWE**: Voleon recruits college students for SWE (Berkeley/Austin "University Hire" postings 2023-24); one 2019 new-grad onsite report says the loop leaned on network protocols, distributed systems, system design and debugging (`TerrenceHo/website` [A, pre-window]). No 2021+ intern question reports found.

### 10.2 Reported questions — none verbatim recovered; categories only: (h) SQL/Python data manipulation, (e) statistics/ML theory, (d) multi-part real-world coding (2 h).

### 10.3 Style — ML-research bar is PhD-level; coding session is long-form/applied rather than LeetCode. Evidence thin.

---

## 11. Jump Trading (research side)

### 11.1 Pipeline
- **FULL-TIME QR (Glassdoor summary [B], 65% positive, difficulty 3/5)**: a **3-hour block with two quants and a trader, ~1 h each**: (1) **1 h Python coding** — data structures, problem solving; (2) 1 h microstructure/trading — HFT strategies, backtesting; (3) 1 h conditional probability and statistics. datainterview [B]: coding "medium-hard, primarily Python, math-heavy — implementing simulations, pricing algorithms, data manipulation for statistical tests"; also stochastic processes, combinatorics, quick mental maths; ML basics (linear/logistic regression, time series, NNs).
- **INTERNSHIP (Campus Quant Trader/Dev)**: HackerRank OA on probability, combinatorics, algorithm speed (tracker [B]); CodeJeet tag stats: a typical Jump coding round has **4 questions: 2 easy, 1 medium, 1 hard**; topics hash table, math, two pointers, array, bit manipulation (Two-Sum family) [B].
- Engineering side (not in scope, for contrast): C++/low-latency, systems spread across the loop, FPGA questions [C]; a 2025 senior-frontend loop (`sumitsingh4411`, medium reliability) listed word ladder, jump game, kth smallest in BST, then React machine coding and design.

### 11.2 Reported questions (research)
- (e) Implement a Monte-Carlo-style simulation; write a pricing algorithm; manipulate data to run a statistical test (datainterview [B], role QR, 2024-25).
- (e) Conditional probability / stats hour (verbal) [B].
- (a) OA: Two-Sum variants, hash-table/two-pointer/bit-manipulation problems; one hard problem per set [B].
- [C] systems samples (engineering): feed handler, in-memory order book / order gateway, logging pipeline, storage for billions of events/day, lock-free single-writer multi-reader; phone: ring buffer, expression evaluator, LCA, longest substring without repeats, RAII, mutex vs spinlock, RDMA, multicast; onsite: thread-safe templated LRU, merge intervals, kth largest O(n), simple matching engine, custom allocator, memory_order, kernel bypass, FPGA order entry.

### 11.3 Style — Python, math-heavy coding for QR; clean correct code under time pressure while narrating; no market-making game.

---

## 12. Aquatic Capital Management

- **FULL-TIME QR** (Glassdoor/Blind summaries [B]): 2 quant interviews → virtual onsite → leadership call. "Several probability and stats questions, then a **take-home on cleaning tick data**. No LeetCode — more brain teasers and research rigour." Interviewers discuss past projects and how you validated signals out of sample; they care about overfitting and robustness. Prefers top research institutions / ex-top-quant-firm candidates.
- **INTERNSHIP**: QR intern (Chicago/London) and SWE intern (Chicago) Summer 2027 postings exist (Greenhouse [A-official]); no intern interview reports found.
- Categories: (e) probability/stats verbal; (i) take-home: clean tick data (dataset/grading not disclosed). **Evidence thin.**

---

## 13. Voloridge Investment Management

- **FULL-TIME QR / DS** (Glassdoor + InterviewQuery summaries [B]): HR interview → online assessments → **take-home exam** → interview with engineers → interview with senior researchers; rounds ~40 min with a quant researcher; "not a typical brain-teaser session". Ideal profile: advanced degree in physics/maths/stats.
- **INTERNSHIP**: QR intern 2027 and QD intern 2027 postings (Jupiter, FL; Greenhouse [A-official]); no interview reports found.
- No specific questions recovered. **Evidence very thin.**

---

## 14. Engineers Gate

- **FULL-TIME QR/SWE** (Glassdoor summary [B]): "tough, many steps"; one-on-one and group interviews; quant questions — brain teasers, probability, maths, data, feature engineering, ML; algorithms/coding review; **linear algebra: matrix multiplication and factorisation**; heavy resume grilling; Python concepts — **Python vs C++ differences, generators and iterators, decorators**; languages Python, C++, R, sometimes Java/MATLAB.
- **INTERNSHIP**: listed on student trackers as hiring SWE interns; no reports.
- Categories: (e), (f-lite Python internals), (g). **Evidence thin.**

---

## 15. Quadrature Capital

- **FULL-TIME / INTERNSHIP (Quant Developer, London)**: Blind "Quadrature Capital Quant Dev onsite interview" thread and 1point3acres company page exist (blocked); summary [B]: standard LeetCode-style coding + systems design + probability/stats. Quant Developer interns are placed in Research or Technology; "QR explicitly accepts undergraduates" (London tracker [B]).
- [C] (self-labelled medium confidence, ~15-30 reports cited): OA 60-90 min, 2-4 LC-medium problems incl. numerical tasks such as **computing a square root or simulating a random process**; phone 45-60 min: quicksort + worst case, search in rotated sorted array, process vs thread, Python GIL; onsite 3-5 panels: **median of a stream**, **merge intervals**, vector vs list memory layout, cache coherence, **expected dice rolls to see all six faces**, "you have a signal correlated with future returns — how do you test significance?".
- **Evidence thin; no first-hand verbatim.**

---

## 16. Cubist Systematic Strategies / Point72

### 16.1 Pipeline
- **INTERNSHIP**: HackerRank **45 min: 2 SQL + 3 Python** (Glassdoor, internship [B]); Point72 SWE-intern Superday Summer 2026 (Reddit r/csMajors [B]): three interviews — LC-medium-or-below coding ×2 + one OOP interview. "Cubist Quant Academy – Developers 2026" and Cubist QR intern postings (HK/Singapore/NY) exist.
- **FULL-TIME QR/QA**: HackerRank OA **180 min: 3 Python + 1 SQL** (Quant Analyst, Blind, "mentally tiring") [B]; some QR loops a **90-min take-home-style test** (quantvault [B]); one report of a **3-hour timed project with 3 questions + debrief** (Glassdoor SWE [B]). Pod-specific loops — two candidates can see different processes (ex-recruiter Medium post, blocked; quantvault summary [B]). Multiple phone rounds with SQL + Java + SDLC scenarios (Glassdoor SWE [B]).
- [C] process: recruiter → 90-min OA (HackerRank/Codility, 2-3 LC medium-hard) → 60-min phone → onsite coding ×2, C++/systems, design, behavioural.

### 16.2 Reported questions
**INTERNSHIP / early-career**
- (h) 2 SQL + 3 Python in 45 min (content not disclosed) [B].
- (a)/(d) LC-medium coding + OOP interview at Point72 SWE Superday 2026 [B].

**FULL-TIME (Data Scientist / QR technical screen, prachub via [B])**
- (a) Max profit with unlimited stock transactions (greedy).
- (g) Find the top-2 heaviest of 32 balls with minimum comparisons (tournament tree + lower-bound argument).
- (e) Sealed-bid second-price (Vickrey) auction: optimal bid; St. Petersburg coin-doubling game pricing (EV, log utility, Kelly).
- (e) Three probability problems in one screen: optimal stopping with 3 die rolls; two people meet in a 1-hour window waiting 15 min; Poisson P(≥1 in 30 min) given P(≥1 in 60 min) = 0.96.
- (e) Multi-step optimal stopping with a **100-sided die**, interviewer adding conditions progressively (quantvault [B]).
- (e) Classifier metrics from a confusion matrix (90 TP / 210 FP / 30 FN / 9670 TN); model validated 2015-2022 loses money live — name three mechanisms; Wald vs Bayesian credible interval for 8/10 wins; strategy with ±50%/∓40% annual returns — arithmetic vs geometric mean, median wealth after 10 years (quantfinancewiki via [B]).
- (d) Design a basketball-shot-outcome ML system (formulation, features, loss, metrics).
- (h) Data task: rolling statistics, a simple estimator, pandas/numpy fluency; linear and tree models, regularisation, CV strategy, overfitting/leakage (quantvault [B]).

**FULL-TIME SWE / QD [B]**
- (a) OA *Maximize "beauty"* (delete elements, count a[i] = i; up to 200k) — same problem family as DE Shaw's *Find Maximum Beauty*; *DFA simulator* (states, transitions, accepting; 200k); *Lexicographically smallest string after substring operation* (FastPrep, May 2026).
- (f) shared_ptr/weak_ptr/unordered_map; read streaming TCP socket data; IPC via shared memory (Glassdoor phone rounds).
- (g) Find the root of an equation without libraries (phone).
- Defensive testing vs pair programming for defect reduction (written).
- [C] anecdotal: kth most frequent; topological order with cycle report; minimum window substring; buy/sell with fees; insert/delete/getRandom O(1); in-memory order book best bid/ask; group anagrams; trie prefix search; word ladder; std::atomic counter; Rule of Five; data race vs race condition.

### 16.3 Style / themes
Python + SQL OAs (the only firm in this cluster where SQL is consistently reported, for both interns and QAs); probability escalation ("interviewer keeps adding conditions"); auction/game-theory and Kelly; ML validation/leakage; C++ for QD. Intern loops are shorter (45-min OA, LC-medium Superday); full-time QA OAs are 3 hours.

---

## 17. Bridgewater Associates (technology)

### 17.1 Pipeline
- **FULL-TIME SWE (Glassdoor summary [B])**: OA → technical phone → full-day onsite with two technical interviews + a "Life Interview" (culture/Principles). HackerRank OA. Java-heavy stack (techinterview [C]); take-home case/coding for some technical roles [C].
- **INTERNSHIP (TA programme, Fall 2017 report `echenran/interviews` [A, pre-window])**: HackerRank challenge, **untimed, two weeks to submit, expected 1-2 h**, "no language/time/memory restrictions, don't over-polish"; CoderPad phone: misc technical questions, walk through your challenge code, then **debug a failing test case live** and attempt an optimisation; onsite under NDA. Student trackers: "very unique culture and interviews, very school-selective."

### 17.2 Reported questions (FULL-TIME SWE, Glassdoor [B])
- (h) SQL: join three tables (teacher / college / salary).
- (a) Count words per sentence, correctly handling abbreviations like "i.e." and "e.g." as non-sentence-boundaries.
- Linux + regex task: find phone numbers across files (phone round).
- (d) System design: parking-lot fee system.
- [C] samples: rolling N-day mean/std with bounded memory; max cumulative-return window; cycle detection in an economic-relationship graph; simulate a systematic rule engine over indicator series; design backtester / time-series store / portfolio-construction service.

### 17.3 Style — LC-easy/medium coding + SQL + Linux/regex practicality + heavy culture screening; intern OA is untimed take-home style. Evidence moderate but mostly pre-2021 or summary-level.

---

## 18. Arrowstreet Capital

### 18.1 Pipeline
- **FULL-TIME QR (quantvault summary [B])**: "one of the most econometrics-forward loops in quant finance"; HR screen → online/technical baseline assessment → several technical stages → all-day Boston final round with an **on-paper written component covering linear regression/econometrics, probability, statistics and brain teasers**; coding questions "around LeetCode-easy".
- **FULL-TIME SWE / QD (Dataford/InterviewSense/Glassdoor summaries [B])**: **1 h pair-programming coding + 30 min behavioural back-to-back**; SQL and database optimisation; Java/Python/C++; distributed systems/cloud; sample topics TCP vs UDP, PowerShell scripting for infra automation.
- **INTERNSHIP**: QR intern, QD intern and Research Systems SWE intern postings (Boston, Summer 2027, Workday [A-official]); no intern interview reports found.

### 18.2 Reported questions — categories only: (e) linear regression derivations/diagnostics, portfolio optimisation and construction; (a) LC-easy coding; (h) SQL/db optimisation; systems trivia (TCP/UDP, PowerShell). **Evidence thin.**

---

## 19. Cross-firm patterns

1. **OA platform**: HackerRank dominates (Two Sigma, DE Shaw, Cubist/Point72, WorldQuant, Jump, Bridgewater); Codility/HackerRank at QRT; CodeSignal at AQR (and possibly Man Group); proprietary quiz + coding test at G-Research; take-home instead of OA at Man AHL, Aquatic (tick-data cleaning), Voloridge, QRT (2-week ML project), Bridgewater interns (untimed HackerRank).
2. **The "stats-to-code" OA is a Two Sigma signature** (interpolation, online regression, temperature prediction), and Cubist is the only firm where **SQL** is consistently part of the OA (2 SQL + 3 Python interns; 3 Python + 1 SQL QAs). Elsewhere SQL appears in Bridgewater and Man AHL take-homes.
3. **DE Shaw** has the largest verified pool of OA problems (16 in FastPrep, 124 LeetCode tags): monotonic-stack "range where I'm the max", subarray removal, greedy scheduling with a twist, tree DP; Indian campus loops add heavy C++/OS/OO-design.
4. **Internship vs full-time**: intern OAs are shorter and easier (LC-easy tags at Two Sigma; 2-3 problems ~80 min at DE Shaw; 45-min OA at Cubist; 2 CP questions + probability at QRT) and intern interviews are 20-60 min project-plus-fundamentals; full-time adds SQL/LLD/system design, longer (3 h) data-science OAs for quant tracks, and 5-7-round superdays. G-Research/Man/WorldQuant intern loops appear to reuse the full-time components (quiz/test/take-home).
5. **Coding weight for QR**: roughly one-third of the loop at Jump (1 h of 3), Two Sigma (1 of 3 technical rounds) and WorldQuant (1 of 3); coding is de-emphasised relative to probability/econometrics at Arrowstreet, Aquatic, PDT, AQR and G-Research; ML-from-scratch coding is reported only indirectly (QRT gradient descent, Two Sigma regression OA, Cubist "simple estimator" data task).
6. **Recurring live-coding problems across firms**: LRU/LFU cache (Two Sigma, DE Shaw, G-Research, PDT, Point72, Jump); median of a data stream (Two Sigma, G-Research, Quadrature, DE Shaw); merge intervals (DE Shaw tags, Quadrature, Jump); calculator/expression evaluation (Two Sigma, DE Shaw, WorldQuant, Jump); order book / matching engine (Two Sigma, Point72, Jump, RenTech guides); expected dice rolls to see all faces / expected flips to HH (DE Shaw, Quadrature, PDT, WorldQuant).
7. **Evidence gaps**: Voloridge, Engineers Gate, Aquatic, Arrowstreet, Quadrature, Man AHL, PDT, Voleon and RenTech have no recoverable verbatim coding questions in 2021-2026 from readable sources; G-Research's official prep PDFs and the 1point3acres/Blind/WSO threads for Two Sigma QR, QRT Zurich, Quadrature and DE Shaw quant phone screens are known to exist but were blocked in this environment and should be read directly.

## 20. Source list (readable in full unless marked *blocked* — blocked items were captured via search summaries only)

Primary / first-hand
- https://github.com/devclub-iitd/Intern-Prep-Series-25/blob/main/Interviews/DEShaw_Saumitra_Garg.md (DE Shaw TD intern, IIT Delhi, 2025)
- https://github.com/devclub-iitd/Intern-Prep-Series-25/blob/main/Interviews/QRT_Arnav_Jain.md (QRT QD intern, Mumbai, 2025)
- https://github.com/Aditya-Bhadoria/intern/blob/main/Intern_Guidance%20%2B1.txt (DE Shaw intern rounds, multiple candidates; also JPMC Quant, Graviton, Quadeye, GS Quant)
- https://github.com/FlashGrey3000/Blog/blob/master/content/post/First-Interview/index.md (DE Shaw SDET intern, 2025)
- https://github.com/ngocuong0105/dendron-wiki/blob/main/vault/interviews.Self%20evaluation.md (DE Shaw SWE, June 2022)
- https://github.com/goldin2008/Note/blob/master/interview_coding.md (DE Shaw interview question; CodeSignal OA of uncertain attribution)
- https://github.com/GuanyiLi-Craig/two-sigma-interview/blob/master/twosigmainterviewnotes.md (Two Sigma onsite sets mirrored from 1point3acres GitBook, ≈2019-20)
- https://github.com/VideepEkbote/VideepEkbote.github.io/blob/main/intern.html (IIT Delhi 2023 intern tests incl. WorldQuant)
- https://github.com/spo-iitk/website/blob/master/posts/2023-intern-harjap-singh-piramal-groups.mdx (WorldQuant intern interview 2023)
- https://github.com/echenran/interviews/blob/master/Bridgewater/fall2017.md (Bridgewater TA intern, 2017)
- https://www.gresearch.com/wp-content/uploads/2020/09/200630-quant-research-preparation.pdf *blocked* (official G-Research QR assessment guidance)
- https://www.gresearch.com/wp-content/uploads/2025/07/Quantitative-research-and-machine-learning-interview-prep-recommended-reading.pdf *blocked*

Aggregators citing candidate reports
- https://github.com/perixtar/quant-interview-oa-bank (FastPrep-verified OA titles with last-seen dates: Two Sigma, DE Shaw, QRT, Point72)
- https://github.com/pushpa-kumar/placement-prep/blob/main/raw-notes/topic-algo-ds-oa.md and raw-notes/company-twosigma-others.md, raw-notes/github-curated-lists.md (entries cite prachub, programhelp, JoinTaro, Glassdoor, Blind, 1point3acres, quantfinancewiki)
- https://github.com/liquidslr/interview-company-wise-problems (LeetCode company-tag CSVs for Two Sigma and DE Shaw)
- https://github.com/ayush-that/codejeet (tag statistics for Two Sigma, DE Shaw, WorldQuant, Jump)
- https://github.com/sumitsingh4411/interview-rounds (2023-25 senior loops for Two Sigma, DE Shaw, Jump — "commonly asked" compilations)
- https://github.com/northwesternfintech/2027QuantInternships and https://github.com/quantprep/quantinternships2022 (firm notes)
- https://github.com/Maseeek/QuantML-InternHQ/blob/main/data/action_items_and_priorities.md (OA platform per firm, 2026)
- Glassdoor pages *blocked*: Two Sigma QR/SWE/QD; DE Shaw QA; QRT; G-Research QR; Man Group QD; WorldQuant QR; AQR ("Sorting and Python code refactor"); Renaissance; PDT QR; Voleon; Jump QR; Aquatic; Voloridge; Engineers Gate; Cubist; Bridgewater SWE; Arrowstreet
- LeetCode Discuss *blocked*: Two Sigma OA + phone screen (907532); DE Shaw SMTS Oct 2024 (5973257); DE Shaw MTS Jan 2025 (6754544); DE Shaw SDE1 Hyderabad; Lead SWE May 2024
- 1point3acres *blocked*: Two Sigma 2024 3hr OA Quant (thread-1042317); Two sigma quant 面试 (546025); QR intern onsite (1149327); qube-rt and quadrature company pages
- Blind *blocked*: two-sigma-quant-researcher-oa; Two-Sigma-Quant-Research-Interview; Quadrature Quant Dev onsite; AQR CodeSignal; aquatic QR interview
- WSO *blocked*: DE Shaw phone question; QRT Zurich QR intern; AQR (28 entries)
- QuantNet *blocked*: G-Research thread 24997; PDT thread 45053
- JoinTaro Two Sigma SWE 7 Nov 2025 *blocked*; techinterview.org, quantt.co.uk, datainterview.com, quantvault.org, quantbrainteasers.com, interviewquery.com *blocked* (summaries only)

Prep-guide (inferred/anecdotal) — used only for topic hints
- https://github.com/ankitkushawaha1000/HFT (per-round files for two-sigma, de-shaw, g-research, jump-trading, pdt-partners, point72, quadrature-capital, worldquant)
- https://github.com/JiawenZhu/CareerVivid/tree/main/data/interview-guides (techinterview.org scrapes: de-shaw, aqr, bridgewater, renaissance)
- https://github.com/design-gurus/grokking-system-design/tree/main/companies (two-sigma, d-e-shaw, jump-trading)
