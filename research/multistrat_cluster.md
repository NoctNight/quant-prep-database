# Multi-strat / market-maker cluster: reported coding-interview questions (2021–2026)

Firms: Citadel (hedge fund), Citadel Securities, Millennium, Point72 / Cubist, Balyasny (BAM), ExodusPoint, Schonfeld, Squarepoint, Marshall Wace, Brevan Howard, Verition.

## 0. How this was gathered, and what to trust

**Access constraints (important for reading this document).** The research sandbox's egress proxy blocked direct reads of Glassdoor, Blind, Reddit, LeetCode Discuss, 1point3acres, QuantNet, Wall Street Oasis, Medium/dev.to, and every prep-company site (algo.monster, quantvault, quantt, interviewquery, dataford, techinterview.org, etc.). Only `github.com` / `raw.githubusercontent.com` were reachable. In addition the session's web-search budget was exhausted after ~21 searches (the budget was shared with earlier work in the session). So the evidence below comes from three channels:

1. **Web-search result snippets** (~21 queries) — these quote Glassdoor/Blind/LeetCode/prep-site content but only in summary; where a question is cited this way it is marked `(search snippet)`.
2. **GitHub repositories that mirror or catalogue first-hand reports** (~15 GitHub code/repo searches, ~80 page fetches). The most valuable were:
   - `pushpa-kumar/placement-prep` (raw-notes/company-hrt-citadel.md, topic-*.md) — a curated bank that labels each item REAL vs PRACTICE and links the original LeetCode Discuss / Glassdoor / Blind / dev.to / 1point3acres / techinterview.org source. Treated as **high reliability** for REAL items.
   - `perixtar/quant-interview-oa-bank` (FastPrep-sourced OA problem titles with dates, Jan 2024 – Jul 2026). **Medium-high** reliability for "this OA problem was seen at firm X on date Y"; problem statements themselves are behind FastPrep.
   - `krishnadey30/LeetCode-Questions-CompanyWise`, `liquidslr/leetcode-company-wise-problems`, `dr-o-ne/leetcode-company-problem-frequency` — scrapes of LeetCode's premium "company tags" (frequency data). **Medium** reliability; tells you which LeetCode problems are tagged Citadel/Millennium/Point72/Squarepoint, not which round they appeared in.
   - `Shivam5022/Interview-Experiences` (first-hand Squarepoint C++ SWE loop), `ZhiyongJing/algorithm` (Point72 面经 compiled from 1point3acres, 2019–2023), `kishanBhandary/Projects-and-Interview-Question` (2025 Citadel Securities SWE), `ngocuong0105/dendron-wiki` (Marshall Wace data engineer 2022), `SMath0510/Placement-Preparation` (Squarepoint quant, Indian campus), `nelsondude/schonfeld_interview` & other Schonfeld take-home repos, `Ozmercer/exodusPoint` (take-home), `MaximusPrimus/millennium-talent-scout` (2025 DS case study). **High reliability, small N.**
   - `ankitkushawaha1000/HFT` — an AI-assisted "company guide" repo whose per-round question lists are explicitly tagged `anecdotal` / `inferred` and whose own evidence matrix admits exact stage ordering is "anecdotal or unsupported". **Low reliability**; included only where it corroborates something else, and always labelled `(HFT-guide, low reliability)`.
   - `shreyasnarahari/cpp-interview` — a C++ prep bank labelled "Citadel"; **unattributed**, treated as a topic list, not as reported questions.
3. **Official firm pages** (via snippets only): Citadel "Our Engineering Interview Process", Citadel Securities "Internship and New Graduates: Engineering Interview Process", Marshall Wace "Quantitative Research Internship Process" / MW Quant Application Guide PDF.

**Tagging.** Every question/pipeline item carries one of `[INTERN]`, `[FT]` (full-time / new-grad / experienced), or `[unclear]`. Where a source says "campus" / "new grad" without distinguishing intern vs full-time, I use `[INTERN/NG]` (campus pipeline: the OA and early rounds are widely reported to be shared between intern and new-grad tracks at Citadel/CitSec, Point72 and Squarepoint).

**Nothing below is invented.** If a firm has thin evidence, the section says so.

---

## 1. Citadel (hedge fund: Citadel LLC / GQS / Global Fixed Income etc.)

Note: outside sources very often conflate Citadel LLC and Citadel Securities; the campus HackerRank OA is shared, and prep sites tag both as "Citadel". Where the source explicitly says Citadel Securities the item is in §2.

### 1A. Internship / campus (intern + new-grad shared pipeline)

**Pipeline `[INTERN/NG]`**
- Application (with 150–300-word written prompts: "share a story or experience that reflects who you are"; "Why Citadel?") → **HackerRank OA** → 1–2 technical video/phone rounds (CoderPad) → virtual or on-site "superday" of 2–4 rounds → committee decision. Sources: Verdent06/Resume-Modifier application notes (2027 intern cycle), Citadel "Our Engineering Interview Process" (search snippet), ricsign playbook ("HackerRank: Citadel, Millennium…"), TechScreen/norahq summaries (search snippets).
- **OA format** (repeatedly reported, SWE intern/new-grad, 2022–2026): 2 coding problems, ~60–90 min total (75 min is the most-cited number; some report 2×30–40 min). Difficulty "LeetCode medium–hard, luck-dependent". One report of an OA variant with **15 MCQs + 1 easy-medium coding problem** (Blind, 2023-ish; likely a non-SWE track). Evaluation rubric per search snippets: complexity, readability, edge cases. Sources: LeetCode Discuss "Citadel Software Engineering Campus Assessment 2022-2023", "Citadel | OA | 2023", "Citadel OA Questions" (2024); Blind "hackerrank interview citadel"; interviewfox/analyticsinsight summaries.
- Language: OA in any HackerRank language; interviews SWE-track are language-agnostic (Python/C++/Java), but C++ questions appear if you claim C++.
- Citadel Securities' official early-career page (quoted via aryehcarmi/leetcode-interview-coach): candidates are evaluated on ability to "explain strategy, clarify, discuss tradeoffs, use hints productively, and demonstrate programming plus DSA in timed coding".

**Reported OA / campus coding questions**

(a) Arrays / strings / hashing
- "Consecutive Sum" — count ways to write N as a sum of ≥1 consecutive positive integers (= LeetCode 829 *Consecutive Numbers Sum*, Hard). Tagged Citadel with the highest all-time frequency in the LeetCode company-tag scrape (1.73), and an algo.monster "Citadel OA" page exists for it. `[INTERN/NG]` 2021–2023. Sources: krishnadey30 citadel_alltime.csv; algo.monster/problems/citadel-oa-consecutive-sum (search snippet).
- "Global Maximum" — choose a subsequence of length k from an array maximizing the minimum absolute difference between adjacent chosen elements (binary-search-on-answer + greedy). `[INTERN/NG]` ~2022–2024. Source: algo.monster/problems/citadel-oa-global-maximum (search snippet).
- "Do They Belong?" — given a triangle's three vertices and two query points, classify each as inside/on/outside (geometry, cross-product). `[INTERN/NG]` ~2022. Source: algo.monster/problems/citadel-oa-do-they-belong (search snippet).
- "Triplets" — count index triplets satisfying a sum/ordering condition (prefix-count / two-pointer). `[INTERN/NG]` 2022. Source: algo.monster "Citadel OA 2022 Triplets" (search snippet). Same family as FastPrep's "Get Triplet Count" and LeetCode-tag "Count Increasing Triplets" (Jan 2024).
- Subarrays with `arr[i] == arr[j] == sum(arr[i+1..j-1])` — count such (i,j) pairs. `[INTERN/NG]` 2024–2025. Source: search snippet quoting a 2024/25 OA report (interviewcoder.co / jointaro).
- "Minimum Operations to Reduce Array Elements to Zero": given x, y, in one op pick one element and subtract x from it and y from all others; find min ops to make all ≤ 0 (= LeetCode 2702 *Minimum Operations to Make Numbers Non-positive*, Hard — binary search on answer). Tagged Citadel 13× in 0–6 months (2025–26). `[INTERN/NG]` 2024–2026. Sources: search snippet; dr-o-ne citadel.md; liquidslr All.csv.
- "Minimum Equal Sum of Two Arrays After Replacing Zeros" (LC 2918, Medium) — Citadel 10×; FastPrep lists "Find Minimum Equal Sum" as a Citadel **full-time** OA problem. `[FT]` (FastPrep) / `[unclear]` (LC tag). 2024–2026.
- "Length of Longest Subarray With at Most K Frequency" (LC 2958), "Max Consecutive Ones III", "Smallest Missing Non-negative Integer After Operations" (LC 2598), "Maximum Total Damage With Spell Casting" (LC 3186), "First Completely Painted Row or Column", "Group Anagrams", "Two Sum", "Find the Duplicate Number", "Count Primes", "Sqrt(x)", "Fizz Buzz", "String to Integer (atoi)". `[unclear]` LC company tag, 2024–2026 windows. Source: liquidslr / dr-o-ne scrapes.
- FastPrep-dated Citadel OA titles (statements not public): "Count Stable Segments" (Jan 2025), "Price Check" (Feb 2025), "Get Distinct Goodness Values" (Mar 2024 & Jan 2025), "Get Min(imum) Operations" (Mar 2024 & Jan 2025), "Find Consistent Logs" (Oct 2024), "Get Max Throughput" (Sep 2024), "Maximize the Lottery ID" (Apr 2024), "Count Increasing Triplets" & "Prime Factor Visitation" (Jan 2024), "Social Media Suggestions" (May 2025), "Minimum Changes for a Periodic Palindrome" & "Minimum Image Processing Cost" (Jul 2026), "Minimum Time to Process Requests" & "Process Scheduling" (Mar 2026). perixtar's role column: mostly `Intern/New Grad`; "Find Minimum Equal Sum" = Full-time; "Minimum Path Sum to Target in Binary Tree" = New Grad **phone screen** (Apr 2026). Source: github.com/perixtar/quant-interview-oa-bank.
- Older campus OA (2020–21, still cited in 2022 posts): **IPO share allocation** — bidders `[bidder_id, shares, price, timestamp]`; allocate shares by price priority, ties by earlier timestamp; return bidder IDs receiving zero shares. `[INTERN/NG]` Source: LeetCode Discuss "Citadel Campus Software Engineering Challenge" via pushpa-kumar REAL entry. (FastPrep lists "Initial Public Offering" again under **Point72, Jul 2026** — same problem family.)
- HackerRank set reported on Glassdoor (SWE track, year unclear): Roman-numeral conversion (1–1000); stable sort of words by length; implement a Stack class. `[unclear]` Source: Glassdoor via pushpa-kumar REAL entry.

(b) Recursion / DP
- "Count Palindromic Subsequences" (LC 2484, Hard) — the **single most-tagged Citadel problem in 2025–26** (16× in 0–6 months; also 5× Millennium). `[unclear]`, campus OA most likely. Source: dr-o-ne, liquidslr.
- "Palindromic Substrings" (LC 647) — FastPrep: Citadel New Grad OA, Jan 2025 `[FT/NG]`; also LC-tag 93.8.
- "Longest String Chain" (LC 1048), "Different Ways to Add Parentheses", "Longest Valid Parentheses", "Knight Dialer", "Maximal Square", "Best Time to Buy and Sell Stock I/II/III/IV/with fee", "Climbing Stairs", "Paint House", "Perfect Squares", "Number of Dice Rolls With Target Sum", "Knight Probability in Chessboard", "Number of Ways to Paint N×3 Grid", "Minimum Costs Using the Train Line" (LC 2361, Hard), "Best Sum Downward Tree Path" (FastPrep New Grad OA May 2025). `[unclear]` LC tags 2021–2026.
- QR-track: "two hard LeetCode DP questions" in one technical round; "maximum schedulable intervals (a DP question)". `[unclear]` (Glassdoor QR reviews, search snippet).

(c) Graphs / trees
- "Evaluate Division" (LC 399 — weighted-graph / currency-conversion) 9×; "Parallel Courses III" (LC 2050, Hard) 6×; "Course Schedule I/II"; "Number of Islands"; "Minimum Knight Moves" 7×; "Word Ladder I/II"; "Reconstruct Itinerary"; "Sort Items by Groups Respecting Dependencies"; "Find Eventual Safe States"; "Binary Tree Maximum Path Sum"; "Serialize and Deserialize Binary Tree"; "Validate BST"; "Inorder Successor in BST"; "Binary Tree Right Side View"; "Construct Binary Tree from Preorder and Inorder". `[unclear]` LC tags.

(d) Design / OOP / simulation
- "LRU Cache", "LFU Cache" (7×), "Design Circular Queue", "Time Based Key-Value Store", "Design Spreadsheet", "Number of Orders in the Backlog" (LC 1801 — an order-book simulation; **all three are the only problems tagged Citadel in the most recent 30-day window, mid-2026**), "Insert Delete GetRandom O(1)", "Design Excel Sum Formula", "Design In-Memory File System", "Design Tic-Tac-Toe", "Design A Leaderboard", "Design Front Middle Back Queue", "Design Search Autocomplete System", "Moving Average from Data Stream", "Find Median from Data Stream", "Min Stack", "Implement Trie", "Find Servers That Handled Most Number of Requests". `[unclear]` LC tags.
- FastPrep "Limit Order Book Matching Engine" — Citadel, Jul 2026 `[unclear]`.

(e) Probability-to-code (QR track)
- Phone screen: "3n people, person i passes with probability p_i; split into n groups of 3; a group scores 1 if ≥2 pass; maximize expected total score" (expected-value optimisation / greedy pairing). `[unclear]`, QR. Source: LeetCode Discuss 427705 / 660968 via pushpa-kumar REAL.
- "Compute E[X | X+Y>0] for X,Y iid N(0,1)" (QR, search snippet); "Design a game using a fair coin such that P(win)=p for arbitrary p∈(0,1)" (listed under Millennium in a Glassdoor snippet but is generic).
- Korean quant-interview-bank example: "Citadel OA: X,Y~U[0,1]; find P(|X−Y|>0.5)" `[unclear]` (KimSuminTHU/quant-interview-bank README example).

(g) Math puzzles coded
- "Compute the product of two very large matrices efficiently, using the structure of the problem and the matrices" (QR, Glassdoor snippet) `[unclear]`.

(h) Data manipulation
- QR / GQS: "statistics question evaluating a trading strategy; probability questions; small programming assignment" (video rounds) `[unclear]`; Cubist-style pandas work not reported for Citadel specifically.

**Style notes `[INTERN/NG]`.** 61% Medium / 32% Hard / 6% Easy in the codejeet pool (vs. 23/63/15 % easy/med/hard in another pool — the discrepancy is pool-dependent, but every pool agrees Citadel's Hard share is the highest of the eleven firms here). Two problems in 45 min is reported for on-site coding ("very fast paced, interviewer expects you to talk while typing"). Optimal complexity is expected on the OA (naive solutions TLE on several of the above — e.g. percentile / triplet-count problems). Behavioural: "Why Citadel?" is asked at application and in a ~20-min behavioural round; "no behavioural, purely technical" is reported for some QR loops.

### 1B. Full-time / experienced

**Pipeline `[FT]`**
- Recruiter screen (20–30 min) → HackerRank OA (60–90 min; experienced hires sometimes skip straight to CoderPad) → 1–2 CoderPad technical screens (45–60 min, 1–2 problems each) → on-site 3–4 rounds (2 algorithmic coding, 1 system design, +1 team-specific systems / low-latency round for senior) → committee. Four stages, ~8 weeks total; first two rounds general, later rounds team-aligned. Sources: TechScreen 2026 guide, osamataha04 hiring-readiness notes quoting Citadel's own page, Glassdoor SWE summaries (search snippets).
- Quant Researcher `[FT]`: typically two 60-min technicals — (1) probability/statistics, (2) coding — plus a research-case / "kill your own idea" round and PM fit round; "45-minute interviews with quants and sometimes software engineers, covering statistics (linear regression, PCA, regularization), brain teasers, and LeetCode-medium code". Sources: Glassdoor QR snippets; hieptran1812 blog.

**Reported questions `[FT]` unless noted**
- (d) "Write a *producer* class that batches messages and sends them to a network endpoint once either a max message count or a max hold-time is reached" — SWE, on-site coding round, NYC. Source: LeetCode Discuss via pushpa-kumar REAL.
- (c) "Given a list of currency pairs and exchange rates (e.g. BTC-USD), find the best exchange rate from currency1 to currency2" — Senior SWE, one of two coding rounds; candidate missed edge cases and was rejected. Source: LeetCode Discuss via pushpa-kumar REAL. (Matches LC 399 *Evaluate Division* tag frequency.)
- (a) "Given a series of prices, find the single buy/sell trade pair that gives maximum profit" — Senior SWE screening round AND reported again as a CoderPad phone round with a follow-up variation (Glassdoor). Source: pushpa-kumar REAL ×2.
- (d) "Design an order book supporting `get_exchange_bbo(exchange_id)` (best bid/offer for one exchange) and `get_nbbo()` (national best bid/offer across all exchanges)" — SWE coding round, followed by ~20-min behavioural; interviewer pushed heaps vs TreeMap, "probes three layers deep" on design choices. Source: dev.to (net_programhelp) via pushpa-kumar REAL; an independent Glassdoor "order book string problem" report is noted as the same question.
- (i) Blind: round 1 brain-teaser, round 2 one-hour CoderPad with hiring manager (non-trading role). Source: Blind via pushpa-kumar REAL.
- (f) Interview follow-ups "related to low-level OS optimisations such as predictive branching" after a standard LeetCode problem (search snippet, jointaro 2024 SWE, declined offer).
- (d) System-design round: "sketch a rate limiter and keep drilling into failure modes" (TechScreen snippet, 2025–26).

**Style notes `[FT]`.** Experienced SWE loops are described as "problem-solving rather than trivia or language depth", but C++-heavy teams do ask systems follow-ups. Committee decision after on-site. Offers are team-specific; declined-offer reports cite fast pace.

### 1C. Recurring themes (Citadel LLC)
- Binary-search-on-answer and prefix-sum counting problems dominate the OA (Consecutive Sum, Global Maximum, Non-positive ops, Triplets, subarray-sum-equals-endpoints).
- Interval / scheduling DP (Merge Intervals, Meeting Rooms II, Employee Free Time, Meeting Scheduler, "max schedulable intervals").
- Cache / order-book style design questions (LRU/LFU, Time-Based KV, Orders in the Backlog, NBBO order book) in live rounds.
- Stock buy/sell family appears at every level from OA to senior phone screen.

---

## 2. Citadel Securities (market maker)

### 2A. Internship / campus

**Pipeline `[INTERN/NG]`**
- Same HackerRank OA as Citadel LLC (2 problems / ~75 min; "Citadel Securities HackerRank OA … two problems in about 75 minutes" — search snippet). Then 1–2 technical video interviews (CoderPad/Zoom) and a final-round day. Official CitSec page: "Internship and New Graduates: Engineering Interview Process" stresses explaining strategy, clarifying, tradeoffs, using hints, timed DSA coding. Sources: search snippets; aryehcarmi calibration notes.
- Junior **C++ Quantitative Developer** track: "initial online assessment on HackerRank where the problem requires **optimising an already-given function**" (Glassdoor CitSec QD, search snippet) `[FT-junior / NG]`.
- QR intern (PhD) `[INTERN]`: two ~60-min technicals — probability/statistics then coding; "computing E[X|X+Y>0] for X,Y iid N(0,1)"; linear algebra; "problems at the intersection of optimisation and classical ML"; LeetCode-medium/hard coding in Python or C++. Sources: Glassdoor CitSec QR / QR Intern pages (search snippets); Blind "citadel securities quant research interview".
- Trading intern (not in scope but reported alongside): "make me a market on the sum of three dice rolls" `[INTERN]` (Glassdoor via pushpa-kumar).
- Datacenter/systems round: **no intern-level report found** of a dedicated "datacenter" round; systems questions (memory layout, cache) do show up as follow-ups in SWE intern interviews (HFT-guide only, low reliability).

**Reported questions `[INTERN/NG]`**
- The OA problems in §1A apply (shared pool). Verdent06's 2027 CitSec SWE-intern prep notes describe the binding constraint as "timed HackerRank / LeetCode mediums" plus "C++ MemoryPool / SPSC / memory-ordering" for the "math-and-systems loop" — a candidate's expectation, not a report.
- (f) 1point3acres (Citadel phone-screen set, HFT SWE, year unclear): **ring-buffer implementation**, merge-K-sorted, stock-DP. Source: 1point3acres company/citadel page via pushpa-kumar REAL `[unclear]`.

### 2B. Full-time / experienced

**Pipeline `[FT]`**
- Recruiter screen → HackerRank OA (60–90 min; some experienced C++ hires get a CoderPad "trick-question" phone round instead) → 1–2 technical phone screens (45–60 min; C++ + systems reasoning for C++ roles) → superday of 4–6 interviews: 2 coding/algorithms, 1–2 C++/systems, 1 system design, 1 behavioural/fit (HFT-guide, low reliability; consistent with the 2025 first-hand "4 rounds (coding + low-level C++ + systems)" account). OneRaynyDay (QR analyst, 2020, offer): on-site deliberately split over multiple days; "grilled on low-level C++ stuff" and "really interesting math problems not related to finance".
- A Glassdoor QD review describes a CoderPad phone round that "was in practice a series of trick questions about particular edge cases of C/C++ and the underlying implementation details of STL" (search snippet). Another SWE report: rounds included "heavy C++ debugging".

**Reported questions `[FT]`**
- (f) "Implement a non-blocking, lock-free SPSC (single-producer, single-consumer) queue" — SWE (HFT), 2025, 4-round loop. Source: kishanBhandary experiences.md #26. Independently: "Write a SPSC queue two threads share without a lock — no std::mutex anywhere" (ring buffer, power-of-two capacity, two atomic head/tail counters, `alignas(64)` against false sharing, acquire/release ordering) — Core/Systems developer. Source: techinterview.org lock-free-queue post via pushpa-kumar REAL.
- (d)/(h) "Given a stream of market-data ticks, design a data structure to query VWAP" (prefix sums) — same 2025 SWE loop.
- (f) "How would you optimise a matrix-multiplication function for a specific CPU architecture" (SIMD intrinsics, cache alignment) — same 2025 loop.
- (d) NBBO order book (see §1B) — reported under "Citadel" but the dev.to author labels it Citadel SWE; likely CitSec.
- (f) Phone-screen C++/systems topics reported as anecdotal in the HFT guide (low reliability): implement a hash map / explain `std::unordered_map` internals; allocator strategy for STL containers in low-latency code; ABA problem & memory reclamation in a lock-free stack; exceptions in low-latency C++; SPSC vs MPMC tradeoffs; MESI and false sharing; two-sum pairs / serialize-deserialize a binary tree.
- (f) On-site C++ (HFT guide, `anecdotal`): `std::move` semantics and when the move ctor is implicitly defined; object layout with virtual functions / vtable; rules of 0/3/5; `unique_ptr` vs `shared_ptr` cost on hot paths; LRU cache; min-heap from scratch; sliding-window order-book summary over a market-data stream.
- (d) System design (HFT guide, `inferred` — treat as topic list): multicast market-data feed handler with gap detection/recovery; pre-trade risk checks without adding latency; multi-venue OMS state machines.
- Behavioural (anecdotal): "a time you disagreed with a technical decision"; "a production incident you owned end-to-end".
- Unattributed C++ bank labelled "Citadel/Citadel Securities" (shreyasnarahari/cpp-interview) — useful as a checklist of what candidates *prepare*: memory_order acquire/release vs seq_cst on x86 vs ARM; spinlock with std::atomic; compare_exchange_weak vs strong; arena/bump allocator; fixed-size object pool with free list; what happens on `new` down to mmap/brk; placement new; cache hierarchy latencies; SoA vs AoS; branchless code; `[[likely]]`; CRTP to avoid virtual dispatch; constexpr lookup tables; consteval; "design an in-memory limit order book with price-time priority"; "10 M msgs/s at <1 µs".

**Style notes.** CitSec is the deepest C++ interviewer in this cluster: candidates consistently report trick questions on UB/STL internals at the *phone-screen* stage for C++ roles, and lock-free / cache / SIMD questions on-site. Algorithm rounds still run at 2 problems / 45 min. QR loops are "purely technical, no behavioural" in several reports; SWE loops end with a short behavioural. No first-hand report of a separately named "datacenter" round was found; the closest is the "team-specific systems depth or low-latency design" fourth round for senior candidates.

### 2C. Recurring themes (CitSec)
- SPSC/ring buffer appears in 4 independent sources (1point3acres phone screen, 2025 on-site, techinterview.org, HFT guide).
- Order book / BBO / VWAP-over-stream data-structure design.
- C++ memory model + cache effects; "how would you make this faster?" follow-ups on every question.

---

## 3. Millennium Management (incl. WorldQuant-affiliated and pod-embedded roles)

### 3A. Internship / campus

**Pipeline `[INTERN]`**
- "There is no single Millennium OA — format depends on the role and pod" (quantvault snippet). Reports:
  - **QR / quant-analyst intern HackerRank**: 8 questions = 4 MCQ (statistics/probability) + 4 coding: 2 pandas dataframe questions (group/merge/filter, rolling/aggregate quantities on price-like data) + 2 generic LeetCode-medium problems (array manipulation with space constraints, string/hash, matrix traversal). `[INTERN]` 2024. Sources: quantvault "Millennium Online Assessment" snippet; WSO "Millennium Quantitative Analyst Technical Assessment" thread (snippet).
  - **Quant Developer intern/new-grad OA** (1point3acres thread 1096305): "Python and transaction-cost-analysis focused, three medium-level HackerRank problems" `[INTERN/NG]` (snippet).
  - SWE intern (London/NY): HackerRank listed as Millennium's OA platform (ricsign playbook) `[INTERN]`; no problem statements recovered.
- Then 1 coding interview + 2 rounds with senior quant and PM for QR interns; "one round coding interview followed by two rounds of comprehensive interviews" (snippet).

**Reported questions `[INTERN]`** — pandas/data (h) and stats MCQ as above; specifics not published. LC company tags (2025–26 windows, level unclear): Validate BST, Path Sum III, Broken Calculator, Find the Smallest Divisor Given a Threshold, Count Palindromic Subsequences (Hard, 5×), Collect Coins in a Tree (Hard, 3×), Best Time to Buy and Sell Stock, Valid Parentheses, Merge Intervals, Remove Invalid Parentheses, Word Break, Design Circular Queue, Group Anagrams, LRU Cache (liquidslr / dr-o-ne). StealthCoder reports 7 Millennium problems of which 3 are DP ("Best Time to Buy and Sell Stock", "Partition Array", "Palindromic Substrings") (snippet).

### 3B. Full-time / experienced

**Pipeline `[FT]`**
- Average 25 days (all roles), ~41 days for QD (Glassdoor). Recruiter → HackerRank (2–3 problems, ~90 min, medium to medium-hard: sliding window, DP, graph, string parsing, hash maps — HFT guide, anecdotal) → technical phone screen (one coding problem + C++/systems discussion) → on-site of coding, C++/systems depth, domain/trading-systems design, behavioural. Pod-level hires interview with the PM directly and can be a single conversation + take-home.
- Data-science full-time case study (2025): build a "semantically-aware resume search engine for hedge-fund talent acquisition" — parse PDF/DOCX resumes with an LLM, store in a vector DB (Chroma), rank candidates, Streamlit UI. `[FT]` Source: MaximusPrimus/millennium-talent-scout ("DS case study 2025").

**Reported questions `[FT]`**
- (b) "Implement a recursive function to compute the nth Fibonacci number" (Glassdoor snippet — likely a warm-up).
- (h) "SQL query problems involving joining tables and handling missing data" (Glassdoor snippet).
- (e) "Design a game using a fair coin such that P(win)=p, 0<p<1" (Glassdoor QR snippet); "explain Fermat's theorem"; "limitations of the local-volatility model" (derivatives QR).
- (f) QD: "stochastic calculus, probability questions, and C++ questions" (Glassdoor QD snippet). A WorldQuant/Millennium engineer quoted by eFinancialCareers: lock-free questions "can show up" but are team-dependent; most teams emphasise STL/templates/modern C++ over lock-free specifics (via pushpa-kumar topic-concurrency).
- HFT guide (low reliability, all `anecdotal`): OA — Kadane variant; max profit with ≤K transactions; shortest path in a grid with blocked cells; validate a floating-point string. Phone — LRU cache; rate limiter (N req/s); meeting rooms; RAII example; move vs copy ctor; deleting derived via base pointer without virtual dtor; `unique_ptr` zero-overhead; mutex vs spinlock. On-site — thread-safe bounded queue with mutex+condvar; rolling average over last N ticks; k-th largest in a stream; LCA; merge K sorted lists; merge intervals; ring buffer; memory_order acquire vs seq_cst; false sharing; virtual-call walkthrough; atomic vs mutex; template specialisation vs overloading; three examples of UB; arena allocator.

**Style notes.** Millennium is the most heterogeneous firm here: central-technology SWE loops look like a mid-tier tech loop (LC medium, some C++), QR/QA loops are pandas + stats heavy with brainteasers, and pod hires are PM-driven. Glassdoor difficulty 2.94/5 — the lowest of the big multi-strats. Behavioural "why Millennium / why this pod" is asked. Hard-LC frequency is low except for the shared-with-Citadel "Count Palindromic Subsequences".

### 3C. Recurring themes
- pandas rolling/group-by on price series + stats MCQ for quant interns; SQL joins for data/platform roles; RAII/smart-pointer/virtual-dtor C++ basics rather than lock-free depth for QD.

---

## 4. Point72 / Cubist Systematic Strategies

### 4A. Internship / campus

**Pipeline `[INTERN/NG]`**
- Cubist Quant Developer intern (2027 cycle) and Point72 data-engineer / SWE interns: HackerRank OA (Point72 "coding assessments are HackerRank batteries that differ by track", including a **3-hour developer "task-scheduler" test** for developer roles — prachub/quantvault snippets), then 2–3 technical interviews. Cubist QR intern (PhD): coding screen (Python + pandas/NumPy under time pressure, LC-medium) → take-home modelling project → probability/statistics/ML rounds with pod researchers (theinterviewden / quantvault snippets).
- Campus data-engineer OA (2022–2023, master's new-grad, 1point3acres via ZhiyongJing): 3 HackerRank problems, 60–100 min; "some problems lacked stdin/stdout specs"; naive solutions time out.

**Reported questions `[INTERN/NG]`** (ZhiyongJing/algorithm compilation of 1point3acres posts, translated)
- (a) Frequency Sort (stdin/stdout, TLE issues) — Data Engineer, Market Intelligence, 2022 Q2 & 2023 Q1.
- (a)/(g) Price percentile cut-offs — compute the 80th percentile **without NumPy/pandas**, O(n log n) required — DE 2022–2023.
- (a) DFA (deterministic finite automaton) simulation problem — DE campus 2023 Q1.
- (h) Two SQL problems + a UNION of two tables — DE 2023 Q1 (career-changer).
- (b)/(a) LeetCode 870 *Advantage Shuffle* and "Nearest Neighboring City" (LeetCode Discuss 1389344) — SWE/finance-quant PhD new grad, 2022 Q2; the same pair reported as the **CIO PCA-group Quant Developer OA: 2 problems, 100 min** `[NG]`.
- (g) Divisors: return the p-th smallest divisor of n in O(√n); "degree of divisibility" — for each number in an unsorted list count how many list elements divide it; return the max (naive O(n²) rejected) — Data Services campus, 2019 Q4 (60 min, 2 problems, pre-window but same pool).
- (a)/(h) Web-scraping DE (2020 Q4): 60-min test with 3 Python + 1 SQL; phone: clock-angle at 3:15, HTTP GET vs POST, coin-flip game valuation (heads = $1 and continue, tails = stop), e-commerce data analysis; then a **5-day take-home** web-scraping assignment.
- (a)/(b) Rotational SWE program (2020 Q1, referral): LC 523 *Continuous Subarray Sum*; NYC-taxi Fermi estimate; 25-horses/5-per-race puzzle; Spiral Matrix (recursive vs iterative); queue vs linked list, map vs set; socket read vs DB write I/O; design patterns.
- (a)/(h) Market Intelligence SWE (2022 Q1): parenthesis-string evaluation `")()(())("`; top-3 locations/days by daily foot traffic per state; LC 300 *Longest Increasing Subsequence*; year-over-year profit table; distinct pairs summing to target with duplicates; plus SQL, web architecture, Kafka, schema design, graph DBs, Spark.
- FastPrep (perixtar): "Get Triplet Count" (Apr 2025), "Test the Hypothesis" (Jul 2026), "Lexicographically Smallest String After Substring Operation" (May 2026, **Full-time** OA), "Initial Public Offering" (Jul 2026, **Full-time** OA), "Generate an Optimal Portfolio Trading Report" (Apr 2026, phone screen).
- LC company tags (mid-2026, level unclear) are almost all **SQL**: "Weather Type in Each Country", "Restaurant Growth" (window function), "Replace Employee ID With The Unique Identifier", "Top Travellers", "Evaluate Boolean Expression", "Maximum OR". codejeet's Point72 pool: 60% Easy / 40% Medium / 0% Hard, "Database/SQL dominant", timed 25–30-min problems.

### 4B. Full-time / experienced

**Pipeline `[FT]`**
- Point72 technology/platform: recruiter → HackerRank/Codility (2–3 problems, ~90 min, LC med–hard per HFT guide) → phone (one coding + C++ questions) → on-site 4–5 rounds (two coding, C++/systems deep-dive for Cubist QD, system design, behavioural). Cubist Quantitative Software Developer JD explicitly names Linux kernel interaction, compilers, embedded, networking, filesystems, debuggers — interviews probe processes vs threads, virtual memory, syscalls, file descriptors, scheduling, signals (snippet).
- Cubist QR `[FT]`: coding screen → take-home → prob/stats/ML rounds; Point72's own tips post promises "tough games, mental challenges and hypothetical problems with no single right answer".
- Data Scientist `[FT]` (June 2022): take-home task, then silence (ngocuong0105 self-evaluation).

**Reported questions `[FT]`**
- (d) "Build a service that ingests real-time quotes from twenty venues and serves the latest price with millisecond latency" — SWE, quant platform. Source: techinterview.org Point72/Cubist post via pushpa-kumar REAL.
- (d)/(h) "Store ten years of tick data so a researcher can backtest over any window without waiting an hour" (partition by symbol/time, columnar formats, hot/cold tiers, staleness tradeoffs) — same source.
- (e)/(h) Cubist QR screen (quantfinancewiki via pushpa-kumar REAL): from TP=90, FP=210, FN=30, TN=9670 compute precision/recall/F1/accuracy; "a model validated on 2015–2022 loses money live from month one — what happened?"; 95% Wald CI for 8 wins in 10 trades; strategy returning +50%/−40% with equal probability — long-run growth (Kelly / geometric mean).
- (e) Balyasny-style "biased coin 60% heads → simulate fair coin" is also listed under Point72 in prep pools (generic).
- HFT guide (low reliability, `anecdotal`): OA — k-th most frequent element; topological order / cycle detection; minimum window substring; buy/sell with fees. Phone — LRU with DLL+hashmap; LIS; serialize/deserialize tree; shared_ptr/weak_ptr; Rule of Five; value/zero/default initialisation; data race vs race condition; inlining. On-site — thread-safe priority queue; rolling Sharpe over a sliding window; convex hull; simple matching engine; currency-arbitrage path (Bellman-Ford); implement std::vector with strong exception safety; lock-free SPSC ring buffer + memory orderings; `volatile`; context-switch cost; fixed-size object-pool allocator; ABI layout with virtuals; mmap/huge pages and TLB; optimizer vs std::atomic; branch prediction. Behavioural — "a latency–correctness tradeoff you made"; "why systematic trading vs other SWE".

**Style notes.** Two very different tracks: Point72 platform/data roles are SQL + LC-easy/medium + practical Python (percentiles without NumPy, stdin parsing) with explicit TLE traps; Cubist roles are pandas/NumPy + stats/ML judgement with a take-home. Hard-LC frequency is near zero in every pool. Behavioural / "why Point72" is present; the Academy-style "hypothetical problems" rhetoric is official.

### 4C. Recurring themes
- Percentile / frequency-sort / divisor-counting problems that punish O(n²); SQL window functions; time-series storage design (ticks, backtests); classifier metrics and overfitting judgement for Cubist.

---

## 5. Balyasny Asset Management (BAM)

**Evidence is thin** — no first-hand coding-question transcript was recoverable; everything below is from search snippets of Glassdoor/interviewquery/WSO/1point3acres or from GitHub repos of BAM hackathons (not interviews).

### 5A. Internship / campus `[INTERN]`
- BAM Software Engineering Summer Internship (London, posted Aug 2025); BAM ran an Imperial College hackathon 2025-11-11 ("Balyasny Coding Challenge") — the two GitHub repos found are hackathon submissions, **not** interview material.
- QR intern: Glassdoor "Quantitative Research" reviews mention a HackerRank with "programming and data-science problems, e.g. **return the n largest drawdowns** [of a price series], plus ad-hoc questions about research process" `[unclear]` (snippet).

### 5B. Full-time / experienced `[FT]`
- Pipeline: recruiter screen → timed HackerRank ("REST APIs, SQL, or core algorithms") → technical phone screens with engineers/hiring manager → virtual or on-site "Super Day" of 3–5 consecutive interviews (behavioural deep-dives, system design, technical). SWE-specific report: "HackerRank test, then a 1.5-hour coding interview all in Python, then 4 hours on-site of Python, system design and behavioural". Glassdoor difficulty 2.93/5, ~25 days. Sources: interviewquery, dataford, cookd.ai, Glassdoor (snippets); Mo3483 ichack notes.
- (a)/(h) Questions: "Python fundamentals and LeetCode-medium algorithm questions"; "return the n largest drawdowns" (data-science flavour) `[unclear]`.
- (e) Phone-round brainteaser: "You have a biased coin that lands heads 60% of the time — how can you use it to simulate a fair coin flip?" (von Neumann trick) `[unclear]` (snippet, attributed to BAM by cookd/interviewquery).
- Security Engineer (Mar 2023, shreyas-sriram notes): behavioural + role questions only — no coding.

**Style notes.** Python-first (not C++) for central tech; system design weight is high for the size of firm; behavioural "how do you operate under daily P&L measurement" is common across pod shops.

---

## 6. ExodusPoint Capital

**Evidence is thin.** No transcript with concrete algorithm questions found.

### 6A. Internship `[INTERN]`
- Campus process exists (scoutify "ExodusPoint Campus" page, snippet) but no question reports.

### 6B. Full-time `[FT]`
- Pipeline (Quantt / Quant Blueprint snippets): technical assessments covering coding, quantitative reasoning and market knowledge; central-quant roles "interview more like technology hires" (DSA, systems design, "the messy realities of market data and OMS"); pod-embedded roles add strategy-specific and fixed-income/rates questions; Python or C++ depending on seat; behavioural rounds probe autonomy under explicit daily performance measurement.
- (i) **Take-home**: front-end/full-stack take-home — "build an Angular app to select a server and schedule a reboot" (Angular 20, card/button components, server list/item, server API service with typed interfaces). Oct 2025, TypeScript. Source: github.com/Ozmercer/exodusPoint ("Home Test"). Role not stated (likely application-development SWE, not quant dev).
- Glassdoor has separate "Software Developer" and "Quantitative Developer" interview pages (snippets only; no content recovered).

---

## 7. Schonfeld Strategic Advisors

### 7A. Internship `[INTERN]`
- Quant Research intern (WSO "Intern Interview – Schonfeld (Central)"): one coding round, then two rounds with a senior quant and the PM (snippet). SWE summer intern postings exist (2025, 2026); Schonfeld's own "online coding exercises across 3 types of programming questions: algorithmic, compilation, and more specific questions" and "virtual whiteboarding and/or live codepair" (snippet from Schonfeld virtual-interview guide). Internal languages Java, C++, Python; "open to any OO language".

### 7B. Full-time `[FT]`
- Take-home projects are Schonfeld's signature and several are public:
  - (d) **Matching engine** take-home (Python 3.6, Falcon + Gunicorn, Docker, pytest): REST endpoint `POST /orders` (trader id, symbol, qty, side), `GET /orders/<trader_id>` with timestamp/status, in-memory storage, automatic matching so a 100-share AAPL buy and a 100-share AAPL sell both move from `open` to `filled`. 2018 (pre-window but the repo was still being referenced in 2022). Source: github.com/nelsondude/schonfeld_interview.
  - (h)/(i) **HKEX CCASS data app** (Sep 2022): single-page Flask/Dash/Plotly app that scrapes HKEX CCASS shareholding data, plots shareholding history, and a "transaction finder" that flags anomalous shareholding changes above a threshold; filtering/sorting/pagination; deployed on AWS App Runner; async requests with rate-limit throttling. Source: github.com/HTLK/schonfeld_hkex; a second Python submission the same month (cck75/schonfeld-interview-curtis).
  - (h) **Quant case** (Jun 2026, Python): four staged questions — q1 data handling, q2 signal analysis, q3 strategy construction, q4 backtest, plus a bonus. Source: github.com/Vini-Zola/Schonfeld_case; a similar "SchonfeldCaseStudy" HTML report (Aug 2026) and a Java "schonfeld assessment" Maven project (May 2026).
- Difficulty (Glassdoor snippet): QR and PM rated hardest; SDET and trade-support easiest; ~37 days.

**Style notes.** Schonfeld leans on practical take-homes (REST service + tests + Docker; data-scraping dashboards; signal/backtest notebooks) more than LeetCode. Java is acceptable. Coding-round specifics for the live rounds were not recovered.

---

## 8. Squarepoint Capital

### 8A. Internship / graduate (campus) `[INTERN/NG]`
- Pipeline: CV screen → online assessment within ~2 weeks (HackerRank-style, ~60 min, 1–3 problems; "easy-to-medium LC difficulty but skewed to implementation": parse a string of commands and execute them; simulate bank-account transactions and report balances) → 1–3 technical interviews → offer. Graduate Quant Developer (Montreal/London/Singapore/NY) and "Intern Software Developer – Winter 2026" postings exist. Sources: quantt, techinterview.org, interviewsense (snippets); Singapore internship tracker.
- QR-track campus (Indian campus placement, SMath0510): three rounds — rounds 1–2 "probability puzzles, random walks, central limit theorem, Markov chains"; round 3 HR/resume. No coding round reported for that track `[INTERN/NG]`.
- (a) FastPrep OA titles: "Suggested Products" and "Empty Shelf" (Sep 2024), "Evaluating Circuit Expressions" (Jul 2026) `[unclear]`. "Suggested Products" = LC 1268 *Search Suggestions System*, which is Squarepoint's most-tagged LeetCode problem (10× in 0–3 months, mid-2026).
- LC company tags (2025–26): Search Suggestions System, Maximum Xor Product, Subarray Product Less Than K, LRU Cache, Basic Calculator (Hard), Number of Perfect Pairs, Maximum Subarray, Trapping Rain Water, Best Time to Buy and Sell Stock, LIS, Group Anagrams, Frog Jump (Hard), Longest Non-decreasing Subarray From Two Arrays, Count Ways To Build Good Strings, Maximum Palindromes After Operations, Merge In Between Linked Lists, Minimum Sideway Jumps, Number of Islands, Minimum Path Sum, Find Valid Matrix Given Row and Column Sums, Minimum Equal Sum of Two Arrays After Replacing Zeros, Couples Holding Hands, Min Taps to Water a Garden, Subarrays with K Different Integers, Min Cost Climbing Stairs, Sort Characters By Frequency. codejeet pool: 4% Easy / 79% Medium / 17% Hard; top topics DP, array, greedy, sorting, string; "18 of 24 tagged problems are array problems".

### 8B. Full-time / experienced `[FT]`

**First-hand C++ Software Engineer loop (Shivam5022, 2025)** — the most detailed Squarepoint report found:
- OA: two competitive-programming problems — one "CF 1600-level two-pointers" problem and "a tricky implementation problem".
- Tech screen R1 (60 min): 10 min resume; 20 min CS fundamentals — virtual memory, process management, page tables, real-time systems, TCP vs UDP, dangling pointers; 30 min live **debugging a dummy `vector` implementation** — missing destructor, missing copy constructor, memory leaks, no out-of-range checks. (i)/(f)
- Tech screen R2 (60 min): TCP internal state machine; **count constructor/destructor calls** for given code snippets; a `char**` pointer exercise; 20-min live coding. (f)
- Tech screen R3 (60 min): **review a thread-safe queue implementation and its benchmark**, suggest optimisations — move semantics, condition variables, bounded queue, RAII locking, container cache-efficiency. (f)/(i)
- Systems & C++ round elsewhere: "walk through the memory layout of a process (globals/stack/heap); show how RAII cleans up a file handle; what goes wrong without it", paired with value/move semantics and standard-container cost questions in a market-data-pipeline context (techinterview.org via pushpa-kumar REAL) `[FT]`.
- Experienced hire (2020, CharAznable67 notes): "why Squarepoint / why leave", refactoring and architecture discussion for senior SWE.
- HFT guide (low reliability, `anecdotal`): SPSC circular buffer without mutex; rolling-window VWAP from timestamped trades; non-recursive BST iterator; `noexcept` and move semantics; strict aliasing; copy elision (C++17 mandatory vs permitted); template specialisation vs overload resolution; `condition_variable::wait` and spurious wake-ups; mmap vs malloc; multiple-virtual-base layout; `atomic_thread_fence`; as-if rule; CRTP; type erasure (`any_invocable`); placement new alignment; `launch::async` vs `deferred`; `restrict`; LTO; skip list; two-heap streaming median with removals; Dijkstra with different PQs; merge N sorted arrays; bucket-locked concurrent hash map.
- Other reported extras (quantt snippet): rounds may cover probability, statistics, finance, Linux, Git, system design, or "a transactional key-value-store exercise" (i.e. implement a KV store with BEGIN/COMMIT/ROLLBACK).

**Style notes.** Squarepoint's developer track is unusual in how much is **code review / debugging of supplied C++** (broken vector, thread-safe queue benchmark) and OS fundamentals (page tables, TCP state machine) rather than fresh LeetCode; the OA is the only pure-algorithms gate and is competitive-programming flavoured. QR track is probability/stochastic-process puzzles. Behavioural is light ("why Squarepoint").

---

## 9. Marshall Wace

### 9A. Internship / campus `[INTERN]`
- **Quant Research internship (official MW process page + MW Quant Application Guide PDF)**: after CV screen, three online assessments — (1) 60-min **programming test** on Codility ("advanced knowledge of any language not required; basic coding techniques and simple functions"; C++, Python, Java etc. supported); (2) a 50-min **Data Exam** — "light quant research: basic analysis on CSV files using any programming language"; (3) a numerical/psychometric-style test. Then interviews. Practice advice from prep sites: LC medium–hard or Codility's Finance section.
- Technology intern (London/NY/Singapore, 2026 postings): 2-hour interview of two technical "labs" — **problem-solving & debugging**, and **open-ended design** (snippet from MW technology graduate/intern description).

### 9B. Full-time / experienced `[FT]`
- Data Engineer, June 2022 (first-hand, ngocuong0105): screen chat → **HackerRank (1 easy + 2 medium)** → technical screening (algorithm round was "LeetCode hard, and I did it") + **SQL data interview with a given table schema** ("simple SQL stuff" but hints hard to follow) → pre-final round. Culture pitch: "small productive teams, no BAs, no PMs, ownership".
- Codility test story (linkjob.ai snippet): timed Codility with emphasis on maintainable, production-quality code.
- C++ Software Engineer / Senior Quant Developer (Oxford Knight agency postings): C++ trading-team roles exist, but no interview transcript found.

**Style notes.** Marshall Wace is Codility/HackerRank-gated and tests **data handling (CSV/SQL)** explicitly at both intern and full-time levels; algorithm difficulty ranges from easy-medium OA to one LC-hard live problem. Debugging + open-ended design labs are the distinctive full-time/intern tech format.

---

## 10. Brevan Howard

**Evidence thin.** All from Glassdoor/Quantt/scoutify snippets; no first-hand transcript.

### 10A. Internship `[INTERN]`
- 2026 Summer Internship – Systematic Trading Technology, New York (Workday posting). No interview reports found.

### 10B. Full-time `[FT]`
- Pipeline (Glassdoor QD/Engineer snippets): 3 technical interviews with team members including the team lead, then a final with the department head; discussions of macro markets.
- (a)/(d) "a Java coding question, a question related to coding around ticker prices, and a more quantitative question" (QD, Glassdoor).
- (h) SQL and database design — "design a schema and write queries to retrieve data based on specific criteria".
- (h)/(i) Excel VBA and database tests — DB connections, array formulas, UDFs, add-ins (analyst/dev hybrid roles).
- (e)/(h) "Write Python functions to simulate Brownian motion"; explain time-series models you have implemented and how you handle overfitting; stochastic calculus.
- Market discussion: recent macro events and implications.
- Digital-assets arm hires engineers separately (2024 Revolut hire noted); no interview data.

**Style notes.** Java and Python both appear; SQL/schema design and VBA reflect a more traditional macro-fund tech stack; "why macro / markets knowledge" matters more than LeetCode difficulty.

---

## 11. Verition Fund Management

**Evidence very thin.**
- QuantNet thread "A roadmap to Quantitative Researcher position at Verition" (2024–25): conversation-based interviews about options, trading strategies, past experience and fit; recommended prep is the Green Book and "150 Most Frequently Asked Questions on Quant Interviews". `[FT]`
- Glassdoor "VERITION GROUP": QR and QR-intern interviews rated hardest, SWE easiest (snippet). `[INTERN]` for QR intern exists but no question content.
- Quant Developer JD (Quant Blueprint): exposure to data ingestion, high-performance processing, features/modelling, portfolio/risk, live execution, post-trade analysis — suggests Python/C++ mixed, but no reported coding questions.

---

## 12. Cross-firm difficulty / style matrix

| Firm | OA platform & size | LC-Hard frequency | Live coding pace | C++ depth | Behavioural / "why trading" | Take-home |
|---|---|---|---|---|---|---|
| Citadel LLC | HackerRank, 2 Q / ~75 min (intern & NG); OA sometimes skipped for experienced | Highest in cluster (≈30% of tagged pool; CPS/Non-positive-ops both Hard) | 2 problems / 45 min | Medium (follow-ups on branch prediction etc.); QR is Python | Yes — app essays + ~20-min round; QR loops often "no behavioural" | Rare |
| Citadel Securities | Same OA; C++ QD OA = optimise a given function | High | 2 / 45 min | Deepest (UB, STL internals, lock-free, cache, SIMD) at phone-screen stage | Short; QR "purely technical" | Rare |
| Millennium | HackerRank; QR intern 4 MCQ + 4 coding (2 pandas); QD 3 medium Python/TCA | Low–medium (CPS Hard shared with Citadel) | 1 problem + discussion | Basic-modern C++ (RAII, smart ptrs, virtual dtor); lock-free team-dependent | Yes, pod-fit heavy | DS case study (resume search engine, 2025) |
| Point72 / Cubist | HackerRank, 2–3 Q / 60–100 min; 3-h "task scheduler" dev test reported | Near zero (SQL + easy/medium) | 25–30 min per problem | Cubist QD: Linux/systems; platform SWE: light | Yes; official "hypothetical problems" | Cubist QR modelling take-home; 5-day scraping project (DE) |
| Balyasny | HackerRank (REST/SQL/algos) | Low (LC medium) | 1.5-h Python coding interview | Low (Python-first) | Heavy (Super Day behavioural) | Not reported |
| ExodusPoint | Not reported | Unknown | Unknown | Seat-dependent | Autonomy under daily P&L | Angular server-reboot app (2025) |
| Schonfeld | Own online exercises (algorithmic / compilation / specific) | Low | Codepair/whiteboard | Java/C++/Python accepted | Moderate | Signature: matching-engine REST service; HKEX scraping dashboard; signal→backtest case |
| Squarepoint | HackerRank-style 1–3 Q / ~60 min; CP-flavoured (CF1600 two-pointers) | Medium (17% Hard in pool) | 20–30 min live + code review | High but *review/debug* style (broken vector, thread-safe queue), OS fundamentals | Light | KV-store exercise reported |
| Marshall Wace | Codility 60 min (intern QR) + 50-min CSV data exam; HackerRank 1E+2M (FT DE) | One LC-hard live reported | 2-h "labs": debugging + open design | Not reported | Culture/ownership pitch | Data exam |
| Brevan Howard | Not reported | Low | Java/Python coding question | Not reported | Macro-markets discussion | VBA/DB tests |
| Verition | Not reported | Unknown | Conversational | Unknown | Options/strategy conversation | Not reported |

## 13. Cross-firm recurring themes
1. **Order book / matching engine / BBO** appears as a live design-coding question at Citadel (NBBO), Citadel Securities (sliding-window order-book summary, limit order book), Point72 (matching engine, order book from add/cancel/fill), Schonfeld (take-home), and as LC 1801 tagged Citadel in 2026.
2. **Stock buy/sell max-profit family** (LC 121/122/123/188/714, ≤K transactions, with fees) shows up at Citadel (OA → senior phone screen), Millennium, Squarepoint, Point72.
3. **Cache design** (LRU/LFU/time-based KV) — Citadel, Citadel Securities, Millennium, Point72, Squarepoint all tag it.
4. **Streams**: rolling average / VWAP / median / Sharpe over a window of ticks — CitSec (VWAP), Millennium (rolling average), Point72 (rolling Sharpe), Squarepoint (VWAP, two-heap median).
5. **SPSC ring buffer / lock-free queue** — CitSec (4 sources), Squarepoint (thread-safe queue review), Point72/Cubist and Millennium (team-dependent).
6. **Data-frame / SQL / CSV** handling is the differentiator for pod shops vs market makers: Millennium (pandas), Point72 (SQL window functions, percentiles without NumPy), Marshall Wace (CSV data exam, SQL schema), Brevan Howard (schema design), Balyasny (drawdowns).
7. **Intern vs full-time differences** (where sources allow a comparison): the OA is shared and identical for intern/new-grad at Citadel/CitSec, Point72 and Squarepoint; full-time/experienced loops add (i) a systems/C++ or system-design round, (ii) a team-specific round, and (iii) sometimes drop the OA in favour of a CoderPad "trick-question" screen (CitSec C++). Intern loops are shorter (OA + 1–2 technicals + a shorter final), with more "explain your approach / use hints" evaluation (official CitSec guidance) and less production-judgment questioning. Difficulty of the *algorithm* content is not lower for interns — Citadel's Hard OA problems are reported by interns and new grads alike.

## 14. Source index (URLs actually consulted or cited by consulted sources)
- github.com/pushpa-kumar/placement-prep (raw-notes/company-hrt-citadel.md, topic-algo-ds-oa.md, topic-system-design.md, topic-concurrency-atomics.md, topic-os-networking-cpu.md, company-twosigma-others.md) — cites: leetcode.com/discuss/interview-question/427705 & 660968 (Citadel QR phone), dev.to/net_programhelp_e160eef28/citadel-swe-interview-experience-order-book-design-in-depth-behavioral-interview-3hb0, techinterview.org/post/3233476386 (lock-free queue), techinterview.org/post/3233477266 (Point72/Cubist), techinterview.org/post/3233477270 (Squarepoint), 1point3acres.com/interview/problems/company/citadel, quantfinancewiki.com (Cubist).
- github.com/perixtar/quant-interview-oa-bank (FastPrep OA titles/dates).
- github.com/krishnadey30/LeetCode-Questions-CompanyWise (citadel_alltime.csv); github.com/liquidslr/leetcode-company-wise-problems (Citadel, Millennium, Point72, Squarepoint Capital CSVs); github.com/dr-o-ne/leetcode-company-problem-frequency (companies/citadel.md, millennium.md, point72.md, squarepoint-capital.md).
- github.com/Shivam5022/Interview-Experiences (Readme.md, Squarepoint section).
- github.com/ZhiyongJing/algorithm (…/interview/company/Point72/Point72面试题目总结.md) — cites leetcode.com/discuss/interview-question/1389344 and 1point3acres threads.
- github.com/kishanBhandary/Projects-and-Interview-Question (C++_INTERVIEW/experiences.md #26).
- github.com/ngocuong0105/dendron-wiki (vault/interviews.Self evaluation.md).
- github.com/SMath0510/Placement-Preparation (README Squarepoint section).
- github.com/nelsondude/schonfeld_interview; github.com/HTLK/schonfeld_hkex; github.com/cck75/schonfeld-interview-curtis; github.com/Vini-Zola/Schonfeld_case; github.com/Drongma17/schonfeld; github.com/gabrielchristensen/SchonfeldCaseStudy_GabrielChristensen.
- github.com/Ozmercer/exodusPoint; github.com/MaximusPrimus/millennium-talent-scout.
- github.com/ankitkushawaha1000/HFT (companies/{citadel-securities,millennium,point72,squarepoint}/round-*/questions.md; research/company-evidence-matrix.md) — low reliability.
- github.com/shreyasnarahari/cpp-interview (real-interview-q/citadel.md) — unattributed.
- github.com/OneRaynyDay/oneraynyday.github.io (2020 interviewing post); github.com/hieptran1812/my-website (Citadel/CitSec archetype post); github.com/aryehcarmi/leetcode-interview-coach (cites citadelsecurities.com/careers/career-perspectives/internship-and-new-graduates-engineering-interview-process/); github.com/Verdent06/Resume-Modifier (2027 Citadel/CitSec intern application notes); github.com/osamataha04/nexus-dashboard (Citadel process notes); github.com/KimSuminTHU/quant-interview-bank; github.com/shreyas-sriram/security-engineer-job-search; github.com/CharAznable67/ComputerScience; github.com/ricsign/Ricsign-New-Grads-Jobs-2027 (docs/PLAYBOOK.md).
- Search-snippet-only sources: leetcode.com/discuss/interview-question/2744561, 5430576, 3749874 (Citadel OA 2022–2024); glassdoor.com Citadel / Citadel Securities / Millennium / Point72 / Balyasny / ExodusPoint / Brevan Howard / Schonfeld / Squarepoint / Marshall Wace / Verition interview pages; teamblind.com posts citadel-interview-questions-ktxzs4qh, hackerrank-interview-citadel-8fungxtm, citadel-securities-quant-research-interview-5guy7dke, citadel-securities-quant-developer-interview-npxcp7dj, interview-with-millennium-management-5xrlpf65, Schonfeld-interview-WwyCR1qR, marshall-wace-interview-xbatej7g; 1point3acres.com/interview/thread/1096305 (Millennium QD OA); wallstreetoasis.com Millennium quantitative-analyst technical assessment thread; quantnet.com threads 47765 (Millennium QR) and 59368 (Verition roadmap); algo.monster Citadel OA pages (consecutive-sum, global-maximum, do-they-belong, triplets); quantvault.org (Point72, Millennium OA); quantt.co.uk (Citadel, Squarepoint, ExodusPoint, Brevan Howard, Verition); techscreen.app Citadel 2026; interviewquery.com (Millennium, Balyasny, Squarepoint); mwam.com quantitative-research-internship-process and MW_Quant_Application_Guide.pdf; citadel.com/careers/career-perspectives/our-engineering-interview-process.
