# Market-maker cluster: reported coding interview questions, 2021–2026

Firms covered: Optiver, IMC Trading, SIG, Akuna Capital, DRW, Flow Traders, Da Vinci Derivatives, Maven Securities, Mako, Tibra, Eclipse Trading, Vivienne Court, Trexquant.

Compiled 2026-09-01. Every question is tagged **[INTERNSHIP]**, **[FULL-TIME]** (new-grad/graduate or experienced) or **[unclear]**, plus a year and a source URL. "FT-NG" = new-grad/graduate full-time; "FT-EXP" = experienced hire.

## 0. Method, source reliability and gaps

- 30 web searches were run (Glassdoor, Reddit, LeetCode Discuss, Blind, QuantNet, WSO, 1point3acres, GitHub, prep sites). The session's search budget was then exhausted, so the remaining internship-vs-full-time work was done through GitHub code/repo search and by cloning first-hand write-up repositories.
- The sandbox egress proxy **blocks** glassdoor.*, leetcode.com, teamblind.com, 1point3acres.com, wallstreetoasis.com, reddit.com, quantnet.com, medium.com, jointaro.com, levels.fyi and all prep sites (interviewfox, prachub, dataford, techprep, quantt, everythingquant, linkjob, oavoservice). Their content was therefore recovered two ways: (1) search-engine snippets returned by the search tool, and (2) a GitHub repository (`pushpa-kumar/placement-prep`, `raw-notes/company-*.md`) that transcribes those pages entry-by-entry with the original URL, role and a REAL/PRACTICE status flag. Where I cite a Glassdoor/LeetCode/Blind/Taro/WSO URL below, that is the original source as recorded there; I could not open the page myself. Treat such entries as "reported, not independently verified by me".
- Fully read first-hand sources (cloned/raw): `Leader-board/OA-and-Interviews` (SIG QT 2022, Akuna Jr QR 2022, Maven QR 2022, Tibra QT 2021 and QTD 2023, Flow Traders maths test), `ChinmayMittal/IITD-CSE` (Optiver SWE intern), `SarthakVerma18/Intern-Guidance` (Optiver + IMC SDE intern, IIT), `devclub-iitd/Intern-Prep-Series-25` (Optiver QT intern), `How-to-faang-UTCN` (Optiver Amsterdam intern), `aayush01x/resources` (Optiver/IMC intern OA), `ErrolMc/OptiverInterviewPrep` (Optiver Sydney principal engineer), `vijaySadhuram/Optiver-Recruitment-Grad-SWE`, `CoolboySaurav/OptverOA`, `bencimp/giving-tree-of-errors`, `hackerrank1919/akuna-capital-hackerrank-2021`, `gxyau/flow` (Flow Traders C++ case-study PDF), `drunkirishcoder/drw-tetris` (DRW take-home PDF), `whosquant/hangman` (Trexquant spec), `perixtar/quant-interview-oa-bank`, `ankitkushawaha1000/HFT`.
- **Reliability tiers used below**: (R1) first-hand write-up read in full; (R2) first-hand report on Glassdoor/LeetCode/Blind/Taro/WSO recovered via transcription or snippet; (R3) prep-site / aggregator question bank claiming "real" questions (PracHub, InterviewFox, LinkJob, Dataford, TechPrep, FastPrep); (R4) prep guides explicitly labelled anecdotal/inferred (`ankitkushawaha1000/HFT`, EverythingQuant, Quantt). R4 items are listed only when nothing better exists and are marked as such.
- Evidence is **thin** for Da Vinci Derivatives, Mako, Eclipse Trading, Vivienne Court and (for developer roles) Tibra and Maven; those sections say so explicitly.

---

## 1. Optiver

### 1.1 Pipeline

**Internship (SWE intern, Amsterdam/Chicago/Sydney; QT/QR intern)**
- SWE intern OA, 2022–2024 (R1: How-to-faang-UTCN Optiver_Guide, Amsterdam intern; R1: IITD-CSE Optiver swe.md, campus; R1: SarthakVerma18 intern guide): 2 coding problems (~2 h, "hash-map heavy", Python recommended by one author) **or** one 75-min "implement this spec" problem (graph-based network) + 20-min MCQ (DSA, networks, SQL, system design) + Zap-N games (reaction, "4 numbers → target", balloon-pump risk game, card pattern-guessing). Indian campus version: the trading and software tracks share the first rounds (80-in-8 arithmetic, sequences, logic games), then a C++ coding test with 3 "trading-flavoured" OOP problems.
- Intern interview loop: behavioural/HR → tech screen (3 questions: data structure for values that don't fit native types, Python-vs-C++ language question, "design an app then scale it") → algorithmic round → system-design round → second behavioural (Amsterdam); campus: HR → system design ("trader in Amsterdam, exchange in Frankfurt — design the system") → "trading software" pseudocode round. Group discussion of logic puzzles (30 min) reported for the Indian campus SDE intern.
- QT/QR intern (R1: devclub-iitd optiver_tirth.md, Amsterdam 2025): OA = 80 arithmetic questions in 8 min (+1/−1 scoring), sequences/pattern games, 10 probability questions at 90 s each, personality test → group discussion (5 Fermi-estimation questions with bounds; card-game strategy on EV/variance) → technical interview (probability games) → HR.

**Full-time (graduate / new-grad SWE, experienced C++)**
- Graduate SWE OA 2023 (R1: vijaySadhuram/Optiver-Recruitment-Grad-SWE, Amsterdam): HackerRank coding 2 problems / 120 min (LC medium–hard) + HackerRank knowledge test 10 MCQ / 20 min (OOP) + Zap-N 9 games / ~1 h. Older Amsterdam grad OA (R2, LeetCode 588375): 8 questions = 5 MCQ + 3 coding (easy "findareas", medium "custom sort", hard LRU-cache-based).
- New-grad SWE Chicago 2024 loop (R2, LeetCode 4126574): OA (2 OOP coding + MCQ on DSA/OS/networking + Zap-N) → recruiter behavioural → technical (resume + DS&A, must explain/optimise) → superday: (1) resume review + OOP coding in C++, (2) system-design discussion needing DS&A/OS knowledge.
- 2025–2026 OA reports (R2/R3): one proctored 90-min problem (webcam/mic/process monitoring) or 3 coding in 90 min; Feb 2025 Glassdoor: C++ syntax/memory test + HackerRank with 1 OOP + 1 DSA medium; Nov 2024: standardised math/reasoning + personality tests then 2 LC-medium coding.
- Experienced C++ (R2, Blind hppufql2): video onsite = "design/build a simple stock trader" round, conceptual round (TCP vs multicast), behavioural; a HackerRank-review round was promised but not held; process varies by office. Experienced Sydney principal C# engineer (R1: ErrolMc): 5 rounds — coding, experience review, design, behavioural, CTO.
- Languages: C++ dominant (OA also accepts Java/Python; onsite OOP question in C++); C# for GUI roles.

### 1.2 Reported questions — Internship

(a) arrays/strings/hashing
- "Days between two dates" without Date objects, leap-year edge cases; paired with a graph problem, 2-h OA — [INTERNSHIP] 2023 cycle, SWE intern (avyukd blog, offer received) https://github.com/avyukd/avyukd.github.io ; C++ solution repo https://github.com/bencimp/days-between (2021).
- "Numbers Station"/message decoder: stream of (sequence id, char or '-'); a message is the chars between two hyphens; handle out-of-order samples, emit only the latest completed message, tricky "two words complete simultaneously" rule — [INTERNSHIP] 2023 https://leetcode.com/discuss/interview-question/3829548/Optiver-Online-Assessment-Internship ; again 2026 (medium.com/@program.net "optiver-oa-2026").
(b) recursion/DP
- Future-price / dividend adjustment: stock price S, dividends (amount, day); price from that day onward is reduced additively; later formalised as `FuturePricingEngine` with update-dividend-by-id + query(day) — [INTERNSHIP] Summer 2023 London https://leetcode.com/discuss/interview-question/2730450/Optiver-Online-Assessment-2022/ ; [FULL-TIME NG] https://leetcode.com/discuss/interview-question/3821560/Optiver-oa/
(c) graphs/trees
- "Giving Tree of Errors": input `(A,B)(B,C)(A,D)`; build binary tree, print S-expression `(A(B(C))(D))` with children lexicographically ordered; error codes E1 invalid input, E2 duplicate pair, E3 >2 children, E4 multiple roots, E5 cycle — [INTERNSHIP] Summer SWE intern (2020 thread, re-confirmed identical in 2022 and again in a 2026 OA guide) https://leetcode.com/discuss/interview-question/357982/optiver-oa-summer-swe-intern-2020/ ; C++ attempt https://github.com/bencimp/giving-tree-of-errors
- Implement a spec'd "graph-based network" class in 75 min, no optimisation required — [INTERNSHIP] IIT campus SDE intern (SarthakVerma18/Intern-Guidance).
(d) design/OOP/simulation
- LionCompetition / "Elephant Competition": constructor takes your animals (name, size) plus a private enter/exit schedule; rivals arrive via `entered(time,size)/left(time,size)`; `getBiggest(currentTime)` returns your animals ≥ tallest rival present — [INTERNSHIP-adjacent, "Campus SWE Chicago"] 2024 https://noinsights.medium.com/optiver-software-engineer-test-2024-c51cb8c14d61 ; https://leetcode.com/discuss/interview-question/2768659/Optiver-OA-Q1
- Supermarket checkout tracker: customers enter/exit, switch lines, modify baskets; notify on exit — [INTERNSHIP-adjacent, Campus SWE] 2024 (same Medium post; 95 % tests passed, 2-h OA).
- Beverage/"Lemonade" `OrderState`: `UpdateLimits(maxStores, maxPerBeverage)`, `OrderUpdate(id, store, beverage, qty)`, `CloseStore`, `CloseAllStores`, `PrintState` printing `number_of_stores:…, number_of_orders:…, number_of_different_beverages:…, number_of_beverages:…`; orders breaching limits print `reject_order: <id>`; lowering a limit closes offending stores — [unclear; SWE OA, Feb 2025] https://github.com/CoolboySaurav/OptverOA (4 sample cases in README).
- System design (intern onsite): "You are a trader in Amsterdam, the exchange is in Frankfurt — design the system", pushed iteratively to automation and co-location — [INTERNSHIP] IITD-CSE Optiver swe.md; "handle trading across multiple exchanges with different protocols" — [INTERNSHIP] SarthakVerma18.
- Tech screen: "data structure to store values that don't fit native types", "compare Python with C++", "design an app then scale it" — [INTERNSHIP] Amsterdam (How-to-faang-UTCN).
(g) math puzzles / trader-side
- 80-in-8 arithmetic, sequences, 10 probability MCQ at 90 s, Fermi estimates with bounds, card-game EV strategy — [INTERNSHIP QT] 2025 (devclub-iitd optiver_tirth.md).
Zap-N games as reported: reaction (click shapes/arrows), "four numbers, reach target", balloon pump (risk), card pattern guessing, "building block", PIN memory — [INTERNSHIP and FULL-TIME] (How-to-faang-UTCN; vijaySadhuram).

### 1.3 Reported questions — Full-time / experienced

(a) arrays/strings/hashing
- Sort an array of Roman-numeral strings — [unclear] Glassdoor QTN_5000517 (HackerRank test, part I).
- Count substrings of a binary string where #1s > (#0s)² — [FULL-TIME] Oct 2025 Chicago Software Division, WSO optiver/interview (brute force TLEs).
- KMP: return every start index of pattern in text — [unclear] 2026 OA (interviewfox optiver-oa-hackerrank-guide).
- "Custom sort", "findareas" — [FULL-TIME NG Amsterdam] LeetCode 588375.
- Max number of palindromic substrings of length ≥ k partitioning a string (2-stage DP) — [FULL-TIME NG] https://leetcode.com/discuss/interview-question/2007154/optiver-new-grad/
- Date ordering via min-heap of size 3 (year, month, day) — same thread.
(b) recursion/DP
- "Trading sequences": count distinct sequences from k shares to n shares in ≤ m one-share buy/sell transactions, holdings never negative — [FULL-TIME NG] 2026 (linkjob optiver-hackerrank-questions; also PracHub).
- Portfolio: allocate capital by fixed weights, rebalance daily, output mean and stdev of daily log returns — [FULL-TIME NG] same source.
(c) graphs/trees
- "Traveling the Graphs": undirected weighted edges `[A,B,dist]`, query `Start->Dest,maxTime`; print the unique shortest path if ≤ maxTime else E1 syntax / E2 logical (duplicate edge, undefined node, disconnected, **multiple shortest paths**) / E3 no route, in priority order; Java template, C++ accepted — [unclear] https://leetcode.com/discuss/interview-question/1768013/optiver-online-assessment-traveling-the-graphs
- Scheduler: processes (pid, start, end) + dependencies; implement `Scheduler` ctor + `PrintSchedule` respecting dependencies — [FULL-TIME NG] 2026 (programhelp.net/en/optiver-oa).
- BST: `Node* GetNode(Node* root, int n)` = smallest value > n — [unclear, onsite written test] FreeOZ forum tid=1031617.
(d) design/OOP/simulation
- Order-book simulation: process buys/sells; buy matches lowest sell ≤ price, sell matches highest buy ≥ price, output sum of transaction prices — [FULL-TIME NG] 90-min OA, 1 of 3 (linkjob; oavoservice; programhelp).
- Turn-based market-making game class: each round a realised mid arrives; each player posts bid/ask/size; track cash and inventory — [unclear] 2026 (interviewfox).
- `LogServer`: `recordLog(id, ts)`, `GetLogs()` (≤ m latest ids in last hour, ascending ts), `GetLogCount()` — [FULL-TIME NG] https://leetcode.com/discuss/interview-question/3821560/Optiver-oa/ and programhelp 2026.
- "Truck Positions": `S client truck` subscribe, `U truck dx dy` move, `R client` → current position + delta since last request; starter classes TruckPosition/TruckPositionDelta/Subscriber/Server, 2-h OA ("impossible for 2 hours") — [unclear] https://leetcode.com/discuss/interview-question/3816133/Optiver-or-OA-or-Truck-Positions/
- "Worst Trade Reporter": stream of Trade(TradeID, InstrumentID, Buy/Sell, Price, Volume) and price updates; query worst loss-per-lot trade per instrument, ties → latest, else "NO BAD TRADES" — [unclear] https://leetcode.com/discuss/interview-question/3812812/Optiver-or-OA-or-Worst-Trade-Reporter/ ; corroborated Glassdoor QTN_6557349.
- Fixed-capacity LRU cache ("Hard Coding" section) — [unclear] 2026 interviewfox; LRU-based hard problem in Amsterdam grad OA (LeetCode 588375); "cabinet/workbench item management, LRU-like" (LeetCode 2007154).
- Rectangle class with `getArea()` (trivial OOP) — Glassdoor QTN_5000517.
- FIFO/circular queue with O(1) fixed-capacity ops; `Date& AddDays(Date&, int)`; `std::string GetCommon(str1, str2)` — [unclear, onsite written test] FreeOZ tid=1031617.
- Implement a class managing trade products with properties/parameters — [unclear, final round] medium.com/@priydarshiroopak.
- "Design core components for market making incl. infrastructure, team and code distribution across geographies" — [unclear, design round] medium.com/@arpitjay099 (author withheld exact text).
- Final-round "design a system for the Frankfurt exchange for an Amsterdam trading company" — [unclear] medium.com/@priydarshiroopak.
- Onsite design prompt ("huge data/sec" trading GUI; conflation, subscription backend) — [FULL-TIME EXP, principal C# Sydney] https://github.com/ErrolMc/OptiverInterviewPrep/blob/main/docs/interview-feedback.md (candidate feedback: people are cut on graph parse→build→traverse problems with cycles, on slow execution when the interviewer adds twists, and on telling maintenance rather than ownership stories).
- "Design/build a simple stock trader" — [FULL-TIME EXP C++] Blind hppufql2.
(e) probability-to-code
- Black–Scholes from scratch, then re-derive via binomial tree explaining risk-neutral pricing; "Delta 0.5, underlying +1 cent → option price change?"; "asset quoted at $40,000 — design automatic order placement; how does the system react to a sudden sell-off?"; Fermi: milk-tea shops in Shanghai — [FULL-TIME NG SDE, 3 rounds, 2026] medium.com/@yourhome1106.
(f) low-level/systems/C++
- Write your own `vector`; CPU cache and TLB; multithreading with `notify_all`; memory-leak detection/avoidance — [FULL-TIME, C++ Developer] Glassdoor Optiver-C-Developer EI_IE243355.0,7_KO8,19.
- OO implementations, circular-buffer queue, scheduler, networking/systems, concurrency, complexity follow-ups — same Glassdoor page.
- "Speed of light — round-trip time for a packet Amsterdam↔Singapore?" — [FULL-TIME NG grad SWE, 2nd round] Blind Ku1cSSGi.
- Struct memory layout / "which struct takes more memory", C++ syntax & memory test — [unclear] Glassdoor SWE page, Feb 2025.
- TCP vs multicast conceptual round — [FULL-TIME EXP] Blind hppufql2. Hardware-research SWE loop: "low-level CPU/memory/network/concurrency, question bank is very small" — Blind xb2hb53e.
- "How would you optimise if data volume doubles? What changes if latency drops from seconds to milliseconds?" — [FULL-TIME NG] medium.com/@yourhome1106.
- MCQ set: time complexity of a pseudocode sort; ~6 DSA/complexity MCQs — [unclear] Glassdoor QTN_5000517; LeetCode 2007165.
(g) math puzzles coded
- Optiver "Prove It" puzzles (central binomial coefficient / Stirling; random-walk expected displacement, biased p=1/3 variant) — [unclear] Lazar-Ilic/Lazar notes (R2).
(i) take-home projects
- None reported for SWE. **Ready Trader Go** (annual open competition, not an interview stage): Python 3.11 autotrader on a simulated exchange, socket order entry + mmap market data, limits 100 position / 10 active orders / 200 volume / 50 msg/s, ~60-min matches scored on PnL; winners have been hired (optiver.com career-hub) — https://github.com/Soham-Deshpande/Optiver-ReadyTraderGo
(R3 practice-only, not confirmed asked: PracHub "Multicore Overheat Prevention Controller (set_core_load/tick)", "Balloon Stability Tracker", "cargo/flight booking profit", "currency arbitrage with cycle fee", "news subscription push engine", "freight-scheduler code review"; Pavel Guzenfeld's six "Optiver-style" C++ problems.)

### 1.4 Difficulty and style
- OA: 2 problems/2 h (intern) vs 2–3 problems/90–120 min or one proctored 90-min LLD problem (NG, 2025–26). Problems are long "story" specs with starter classes; the difficulty is scope management, not algorithms. Hidden tests run; several reports of TLE on brute force (binary-substring count) and of `std::cin` throughput mattering.
- Code quality is scored: 90 % correctness rejected while 77.8 % progressed (LeetCode 588375); avyukd's offer write-up stresses modularity/tests; Akuna-style "cleanliness" comments recur.
- Onsite escalation: interviewer adds twists mid-problem; design rounds go to CPU/memory/network/concurrency detail rather than boxes-and-arrows; "explain why you chose this data structure / what changes if input changes".
- Intern loops are lighter on C++ trivia (system design given verbally, no code) — SarthakVerma18: "I should have read about databases, networking, system design and C++ behaviour". NG/experienced loops add C++ memory/cache/TLB, vtable, multithreading questions.

### 1.5 Recurring themes
Order book / trade-stream simulation classes; dividend-adjusted pricing; graph problems with strict error-code specs (E1–E5); date arithmetic; LRU-style caches; log/time-window servers; Amsterdam→Frankfurt latency design; Zap-N + 80-in-8 for everyone; strong weight on communication and code style.

---

## 2. IMC Trading

### 2.1 Pipeline

**Internship (SWE intern Amsterdam/Chicago/Sydney; QT intern)**
- OA on HackerRank, 2 questions (2022: LC-1381 stack variant + knight/bishop BFS) — [INTERNSHIP] https://leetcode.com/discuss/interview-question/1483476/imc-software-engineering-internship-summer-2022-oa/ ; IIT campus SDE intern: 105-min, 2 questions (DP + directed-graph property) (SarthakVerma18); "2–3 problems, very implementation based" (aayush01x).
- One-way video ("Vielpe"/HireVue-style): 5 questions, 2 behavioural + 3 technical, 45 s read + 3 min answer, 3 retries — [unclear NG/intern] 1point3acres snippet; "explain CS fundamentals, most-proud project" — [INTERNSHIP, Amsterdam, Nov 2025] jointaro (rejected at this stage).
- Campus intern loop: group discussion = code review of a C++ `ResourceManager` / order-processing snippet using threads; find bugs, optimise, discuss OS scheduling — [INTERNSHIP] SarthakVerma18; aayush01x. Then 90-min technical: 30 min discussing the optimal order-book approach, 60 min coding it; then HR.
- US intern 2025: apply → OA → 1-h behavioural/yes-no technical → 2-h technical → offer — [INTERNSHIP] jointaro fc22e6e8.
- QT intern: Neurolympics (BrainsFirst, ~45 min, ~4 games), maths/probability test, one-way video (define eigenvalues, survivor bias, conditional probability, 15 s prep / 90 s answer), HR with market-making + quant questions, in-person Amsterdam superday (dice/cards probability, market-making game, options basics) — [INTERNSHIP/NG] Glassdoor IMC QT pages (search snippet).

**Full-time (graduate / new-grad / experienced)**
- New-grad SWE: HackerRank OA (2024: 2 medium-hard in 120 min per 1point3acres thread-1008358; Blind asregdsp: 2 DP problems / 2 h; 2023 assessment: Q1 MEX greedy + 5 MCQ + Q7 coding) → one-way video → final Zoom/onsite; IMC careers blog (Alex ten Brink): automated "purely theoretical" screen, then a discussion + coding exercise on "an approximation of our actual trading system" assessing C++ fluency, algorithms, code reading; you are not expected to finish.
- Onsite coding: "always the same question: implement a matching engine from skeleton code and pass the unit tests (add order, delete order, partial fills, multi-level sweeps)" — [FULL-TIME] Blind YZWWPk0J; Senior Java Dev India 2025: 2.5-h coding station, 44 tests passed, still rejected for not following the prescribed approach — jointaro 7d9ca4ed. Experienced Amsterdam SWE 2024: 6 rounds incl. Rock-Paper-Scissors home assignment ("keep it simple and GC efficient") — jointaro a0e1b0be.
- Languages: C++ (hot path) or Java track chosen at recruiter screen; Python for quant-dev/data roles.

### 2.2 Reported questions — Internship

(a)/(c) arrays, graphs
- Knight minimum path with a fixed bishop at (bi,bj); knight may never land on a square the bishop attacks (BFS) — [INTERNSHIP] Summer 2022 OA (LeetCode 1483476).
- Stack with `push/pop/peek`, range increment on first i elements, and O(1) `sum()` (LC-1381 + sum) — [INTERNSHIP] same OA; also [FULL-TIME NG] LeetCode 1798323; lazy-increment fix for TLE (LeetCode 873993, NG fast-track).
- Number of Islands; strstr; "elevator problem" (design/simulate) — [INTERNSHIP] coding round, 2018 https://leetcode.com/discuss/interview-experience/128304/imc-software-engineer-intern (older than range; kept because the same three reappear in 2025 reports).
- Taro's recurring IMC bank for SWE intern Chicago 2024 (offer): Asteroid Collision, Maximum Side Length of a Square with Sum ≤ Threshold, Minimum Space Wasted From Packaging — [INTERNSHIP] jointaro 994933b8 (not confirmed as that candidate's exact questions).
(d) design/OOP
- 90-min pair session: design then implement an order book (30 min discussion of optimal approach, 60 min coding) — [INTERNSHIP] SarthakVerma18.
- Group code-review: C++ ResourceManager / order-processing snippet with threads — find bugs, optimise — [INTERNSHIP] SarthakVerma18; aayush01x.
(f) low-level
- Differences between list/set/map/unordered_map; "sort from fastest to slowest: CPU cache, main memory, heap allocation, addition, disk"; "what happens when you type wikipedia.org" (routing tables) — [INTERNSHIP, SWE Intern Prop Trading, Amsterdam Oct 2025] WSO imc-financial-markets/interview.
- "Is multithreading always faster than single-threading?" + data-structure complexities + computer architecture + a simple system design — [INTERNSHIP, SWE intern Software, Amsterdam May 2025] WSO.
(e)/(g) trader intern
- Robot on a table, moves left/right with given probabilities, x cm from edge — expected moves to fall off; dice/cards probability; market-making game; define eigenvalues / survivor bias / conditional probability on video — [INTERNSHIP/NG QT] Glassdoor IMC Quant Trader pages (snippets).

### 2.3 Reported questions — Full-time / experienced

(a)/(b)/(c)
- MEX: sort, greedily assign 0,1,2,… (Q1 of 7; Q2–6 MCQ) — [FULL-TIME NG, 2023] https://leetcode.com/discuss/interview-question/3222400/IMC-trading-hackerrank-assessment-2023/
- Array range update: query (idx, v) adds v at idx, v−1 to neighbours, v−2 next … until 0 or boundary; left/right independent (difference arrays + prefix sums) — [unclear, "old OA"] https://leetcode.com/discuss/interview-question/4186527/IMC-trading-question/
- Seat-assignment queue: requests [1,3,3,2,2] → [1,3,4,2,5]; union-find / set solutions — [FULL-TIME NG grad SWE] https://leetcode.com/discuss/interview-question/4644033/IMC-Trading-Graduate-Software-Engineer/
- Knight moves on 150×150 board (BFS) + the lazy-increment stack — [FULL-TIME NG fast-track] https://leetcode.com/discuss/interview-question/873993/
- "Medium LeetCode, review BFS/DFS" — [FULL-TIME NG Systems Engineer] LeetCode 1861424. "Two DP questions, 2 h" — [FULL-TIME NG] Blind asregdsp. "Hard LC DP and graph" in a 90-min Python hands-on round — [FULL-TIME Python Dev] Blind zugas8tk. "Sorting a list two items at a time" — [FULL-TIME Quant Dev Python] Blind 10a131y6. LeetCode company tags: Find the Safest Path in a Grid, Time Taken to Cross the Door, Shortest Path with Obstacles Elimination, Min Stack (codejeet.com/company/imc).
- OA "calculate information from an order book", C++/Java preferred — [unclear] Glassdoor IMC-Trading-Interview-Questions-E278100.
(d) design/OOP/simulation
- Trade matching engine API: add Buy/Sell (return Trade if it matches), delete pending orders, market depth (price range + volume per level) — [FULL-TIME SWE] Glassdoor QTN_2738088; skeleton + unit tests onsite — Blind YZWWPk0J; 2.5-h coding station — jointaro 7d9ca4ed.
- Rock-Paper-Scissors home assignment, "simple and GC efficient" (Java) — [FULL-TIME EXP] jointaro a0e1b0be, 7d9ca4ed.
- Hotel booking system: "designed with a huge list — pros/cons, better structure?" (video round, 1.5 min think / 5 min answer; B+ tree/sharding) — [FULL-TIME NG grad] LeetCode 1798323; in-memory hotel booking data-structure design — WSO.
- Stack with increment (LC 1381), Number-of-Islands variant — [FULL-TIME, 2025 candidates] techprep.app imc-trading-interview-process.
(f) low-level/C++
- How smart pointers are implemented (control block, atomic refcount, destructor across threads); vtable memory layout under multiple inheritance, virtual destructor — [FULL-TIME EXP, SWE Risk, Amsterdam Oct 2025] WSO.
- False sharing; move constructors; CPU caches; "why does the compiler do X" — [FULL-TIME C++] jointaro guide; WSO.
- Threading vs multiprocessing — [FULL-TIME EXP Amsterdam 2024] jointaro a0e1b0be. LFU vs LRU "explain to a 5-year-old"; hash-map internals (video round) — Glassdoor/TechPrep.
- Theoretical multithreading + data-structure questions in one-way video — [FULL-TIME NG Amsterdam] LeetCode 1216573.
(R4/R3 practice only: TheWallStreetQuants "moving average / Greeks / 1M orders per second"; ankitkushawaha HFT list — CRTP, MESI, spinlock with atomic_flag, Bellman-Ford, SPSC ring buffer, "sum > 7 make a market" games.)

### 2.4 Difficulty and style
- OA: LC-medium baseline, 2 questions, 2 h (intern) / 105–120 min; TLE is common in Python (10-s limit reported) → need amortised-O(1) tricks. Hidden tests; sometimes a single 90-min implementation problem graded on correctness/attention to detail.
- Onsite: skeleton + 20–44 pre-written unit tests, single small screen; graded on pass rate **and** on following the interviewer's intended approach (a candidate passing all tests was rejected). Explicitly told not to expect to finish.
- One-way video round is a known filter with pass/fail ambiguity ("got all right, still rejected").
- Intern vs NG: intern OAs mirror NG OAs (same LC-1381/knight family), intern loops swap deep C++ trivia for a group code-review; NG/experienced loops add smart-pointer/vtable/false-sharing depth and a longer matching-engine build.

### 2.5 Recurring themes
Matching engine / order book (from OA to final round); stack-with-increment family; knight-BFS family; C++ internals (smart pointers, vtable, caches, false sharing); Neurolympics; strong cultural-fit filtering.

---

## 3. SIG (Susquehanna International Group)

### 3.1 Pipeline

**Internship**
- Quant Trader intern/2022 programme (Dublin) — [INTERNSHIP/NG programme] R1 Leader-board: Stage 1 maths entrance exam, 14 questions / 20 min (MCQ + integer answers; expectations of infinite streams, bet EV vs cost, brain-teasers) → HR-led round with 5 probability questions → (later stages not reached). Quant OA generally: 60–75 min, 30–50 questions, mental arithmetic + sequences + probability/EV; Mettl "Problem Solving Assessment" 1 h / 15 questions (probability, stats, brainteasers, single-variable calculus; graphing calculator allowed) — Leader-board Online Assessments.md.
- SWE / Trading Systems Engineer intern (US) — [INTERNSHIP] WSO: OA of C++ string/array problems → technical phone screen doing joins/merges/aggregates in numpy/pandas → superday with (i) implement `std::vector` from scratch, (ii) system design, (iii) math-focused round.
- Summer SWE intern OA on CodeSignal (1point3acres thread-812746, 2022); "SIG SDE OA: not algorithmic, implement functions against unit tests" (thread-1026746, 2023); phone interview 45 min / 2 maths problems or 60 min / 3 + behavioural (thread-1084002).

**Full-time / experienced**
- SWE: recruiter → CodeSignal (30 min + follow-up) or 4-question CodeSignal (2 easy + 2 very hard, mid-level 10-yr engineer, May 2026, LeetCode post 8252043) → virtual onsite (OOD + live coding) → onsite (team fit, resume deep-dive, managers). Blind: "discussion based, resume + tech questions, no LeetCode" vs "final round 3 h, 2 LC questions" — depends heavily on team. Stack: C++, C#, Python, PostgreSQL/SQL Server.
- Quant trader/researcher FT: same maths OA, then phone probability round, then superday (poker/game-theory flavoured EV, market-making, brainteasers with confidence intervals).
- Languages: developer OA any of C++/Java/Python/C#; trader track only basic Python data manipulation.

### 3.2 Reported questions — Internship

(e)/(g) probability (trader intern/programme)
- "Matching heads" bet valuation; painting authenticity EV; expected number of boxes to open; three biased coins (Bayes) — [INTERNSHIP-programme QT 2022] https://github.com/Leader-board/OA-and-Interviews/blob/main/Application%20experiences/2021-22/SIG/Quantitative%20Trader%20-%202022%20Programme.md
- Expectation of an infinite stream; compare EV to bet cost — same, stage-1 exam.
(f)/(h) developer intern
- Implement `std::vector` from scratch (superday) — [INTERNSHIP, Trading Systems Engineer Intern] WSO susquehanna-international-group/interview.
- pandas/numpy joins, merges, aggregates (phone screen) — [INTERNSHIP] same.
- C++ string manipulation and array problems (OA) — [INTERNSHIP] same.
- "Implement functions to pass provided unit tests, not very algorithmic" — [INTERNSHIP/NG SDE OA] 1point3acres thread-1026746 (snippet).

### 3.3 Reported questions — Full-time / experienced

(d) design/OOP
- OOD: define classes and orchestrate them (LC-medium) — [FULL-TIME] Blind (search snippet, sig on-site chqe8jcn).
- Coding round: code, explain, justify data structure, complexity; separate design round requiring an extensible SOLID design — [FULL-TIME SDE] Blind ksjpbtsb.
- "Sea Battle Game Server" — [unclear] hackerprep.io/company/sig (paywalled, "verified by multiple candidates").
(a)/(b)/(c) — format only
- CodeSignal 4 questions, 2 easy + 2 very hard — [FULL-TIME EXP] LeetCode 8252043. Final round 3 h with 2 LC questions — Blind w22t1O4b. Insider advice: "when and where to use data structures and basic searching/sorting", no need for the single optimal solution (Blind bcentffb).
(e)/(g) trader FT
- Final round 1 h, 2-on-1, mostly brainteasers; answer with a market/confidence interval — WSO forum susquehanna-international-group-final-round-interview.
- Practice-only (R3/R4, not confirmed): Dataford list (CSV movie catalog year-range index; cash register with inventory/profit; restricted frog paths; tickers in headlines; C++ ownership bug hunt; 3×3 matrix rotation; theatre seating; count subarrays with odd zero count; minutes between time strings); InterviewFox 4-question CodeSignal mock (first repeated value; smallest index reaching cumulative threshold; rolling-window task counts; k-th largest in stream); LinkJob (grid path-bounce, wildcard number match, "stations" DP to 1000, TreeSet closest heights); EverythingQuant (Maximum Drawdown, compound interest, Dijkstra, library class filtering); ankitkushawaha HFT (net delta exposure from options trades, sieve, card-game simulation, expression evaluator).

### 3.4 Difficulty and style
- Developer OA is implementation/unit-test driven rather than algorithmic; CodeSignal variant back-loads two hard problems. Trader OA is speed-bound (20–30 % pass reported) with negative marking on some sections.
- Onsite is conversational and design-heavy; pandas/numpy fluency tested for trading-systems interns; `std::vector` from scratch is the canonical C++ question. Escalation is via "why this structure / extend the class" rather than harder algorithms.
- Probability rounds: expectations, Bayes, gambler's ruin, random walks; interviewers accept confidence intervals.

### 3.5 Recurring themes
Unit-test-driven OA; `std::vector` implementation; pandas data manipulation; OOD/SOLID design round; EV/Bayes brainteasers; poker/game-theory culture.

---

## 4. Akuna Capital

### 4.1 Pipeline

**Internship (C++/Python SWE intern; QT intern; Quant Dev intern)**
- C++ SWE intern round 1 (R2, GeeksforGeeks): HackerRank, **80 min, 3 problems** (see 4.2). C++ track adds ~10 MCQs (C++17/20 syntax, code tracing, pseudocode) — 1point3acres threads 1012794, 1044580, 1026765 (snippets: "10 MCQ + 3 coding", "multiple-choice, pseudocode and code tracing").
- Python intern OA (Sydney): ~120 min, 10 CS MCQs + warm-up + "document printing" + coin-change variant — https://leetcode.com/discuss/interview-question/606488/akuna-capital-python-intern-oa-sydney
- 2026 intern OA (oavoservice snippet): HackerRank 70 min, order-book problem + probability question. Quant Dev intern 2026 (everythingquant forum post title only).
- After OA: C++ track → "debugging-style" round 2; Python track → build-from-scratch round 2 (interviewfox snippet). Then phone screen(s) → onsite/virtual day.
- QT intern: 2 OAs (arithmetic/sequences "trader math" + HackerRank 3 LC easy-medium) → EasyHire/HireVue webcam maths (7 questions × 5 min; probability/EV/stats) → trader interviews → HR — Glassdoor Akuna QT pages (snippets). Akuna Virtual Quant Trading Challenge (Aug 2026, binary-options market-making bot in Python) is a separate competition feeding QT recruiting (many GitHub repos).

**Full-time (junior/entry C++ dev, Quant Dev, Junior QR, experienced)**
- Junior QR 2022 (R1 Leader-board): HackerRank 3 LC-mediums (simulation-greedy, greedy, memoisation), C++ or Python, "pick any two, third is bonus", explicitly graded on cleanliness/readability → one-way video maths exam (5 questions × 5 min: moments, diverging integrals; numeric answer) → live probability interview on CodePair (no coding asked) → rejection citing "probability/statistics and strong coding".
- Junior Quant Dev final stage: HR, system design, math, CodePair, team lead — LeetCode 926316.
- C++ developer: OA (3 problems 60–90 min + C++ MCQ) → **take-home matching engine (72 h)** → phone screen(s) → onsite (coding, system design, projects). Some Singapore 2025 SWE loop: HackerRank 4 questions (3 use-case problems + 1 SQL) → one recruiter call — jointaro 01da9b16.
- Languages: C++ (dominant), Python, Java, C#; take-home in C++.

### 4.2 Reported questions — Internship

(d) design/simulation
- Simplified market-order tracking: process buy/sell orders and cancels, maintain bid/offer, recompute best quote after each event — [INTERNSHIP, C++ SWE intern, problem 1 of 3, 80 min] https://www.geeksforgeeks.org/interview-experiences/akuna-capital-round-1-assessment-my-experience-c-swe-intern/
- Data throttling / rate limiter: publish items subject to size/count caps per sliding time window, drop excess — [INTERNSHIP] same, problem 2 of 3; problem 3 unfinished ("algorithmic logic + data structure usage").
- 2026 intern OA: order-book problem + probability — [INTERNSHIP] oavoservice.com (snippet only).
(a)/(b)
- Coin-change variant; "document printing"; 10 CS MCQs — [INTERNSHIP Python, Sydney] LeetCode 606488.
- Write code to shuffle a 52-card deck; find common elements of two arrays; managed vs unmanaged memory languages — [INTERNSHIP, Software Developer Intern] Glassdoor AKUNA-CAPITAL-Software-Developer-Intern EI_IE608116.0,13_KO14,39.
(e)/(g) trader intern
- "Biased coin 70 % heads — produce a 50/50 outcome"; "what would you do with $1M for 3 years / 3 days?"; EV/expected-value phone questions; 7 timed probability questions on webcam — [INTERNSHIP/NG QT] Glassdoor Akuna QT pages.

### 4.3 Reported questions — Full-time / experienced

(i) take-home (the well-known one)
- **Order matching engine** (C++, 72 h): stdin commands `BUY|SELL <GFD|IOC> <price> <qty> <orderId>`, `MODIFY <orderId> <BUY|SELL> <price> <qty>`, `CANCEL <orderId>`, `PRINT`; GFD rests, IOC fills-or-cancels; price-time priority; print `TRADE` lines and the book on PRINT — [FULL-TIME, C++ dev; also Shanghai regular program] https://github.com/hackerrank1919/akuna-capital-hackerrank-2021 (README with 4 sample inputs, incl. a 60-line stress case), https://github.com/RoyProton/Akuna_SH_Code_Challenge ; the 1o24bbs/PracHub descriptions call it "GTC and FAK order types, 3-day window". Grading: hidden tests with a 2-s limit; one candidate passed 29/30 and failed the last on `std::cin` throughput (search snippet).
- Shanghai variant: parse binary message files (Order Entry type 1, Ack type 2, Fill type 3 with header seq/timestamp), compute per-trader stats and sort instruments by total quantity — https://gist.github.com/wangyangkobe/7cc67aef84f78836831e578c99ff4881 (year unclear, pre-2021).
(a)/(b)/(c) OA and screens (R3 PracHub "real" bank, role SWE, year unclear)
- Min swaps to sort a distinct array into strictly descending order (n − #cycles); count simple s→t paths in an undirected graph (n ≤ 20, backtracking); "Movie Ratings Scheduling" weighted interval scheduling — 3-part OA https://prachub.com/coding-questions/solve-swaps-graph-paths-and-movie-dp
- Multi-stock max profit over (date, symbol, price) records, one share at a time, buy strictly after previous sell, return profit + trade list (≤200k rows) — https://prachub.com/coding-questions/compute-max-profit-across-dated-stock-quotes
- Break a palindrome to the lexicographically smallest non-palindrome by one change; A→B with "−1"/"×2" min operations (reverse greedy); count inversions (merge sort); trace pseudocode + most-frequent char O(n) — PracHub.
- Cross-array swaps: ≤ k swaps between a and b to maximise distinct values in a; min cost to move all 1s right of all 0s in a binary string — technical screen, PracHub.
- Glassdoor snippets: bitwise combinations of two's-complement integers; "identify/fix a performance issue in a given algorithm" (HackerRank); maximum subarray; string parsing; **implement a move assignment operator**; a socket-based coding problem in a 45-min phone screen; C++ round = one easy algorithm + one hard C++-specific question — [FULL-TIME C++ SWE] EI_IE608116.0,13_KO14,33 and ,31.
- LeetCode company tags (crowd): Cherry Pickup, Delete and Earn, 3Sum, Combination Sum, Can Make Palindrome from Substring, Increasing Decreasing String, Rotate Image, Network Delay Time, Dice Roll Simulation, Min K-Consecutive Bit Flips, Wiggle Sort II, Longest String Chain, Maximum Product Subarray, Minimum Taps… — https://github.com/krishnadey30/LeetCode-Questions-CompanyWise/blob/master/akuna-capital_alltime.csv
(d)/(f) design & C++
- Refactor a buggy C++ **object pool**: races, double-free, ABA, leaks; implement `borrow()` (timeout/blocking), `returnObject()`, RAII handle (movable, non-copyable), FIFO fairness, safe shutdown; deliver C++17 + multithreaded unit tests — [FULL-TIME SWE OA/system-design] https://prachub.com/interview-questions/fix-and-harden-an-object-pool
- In-memory communication manager `connect/disconnect/clear` with idempotent undirected links — PracHub (easy).
- Streaming stats: max/mean/mode over a stream, then over the last k (sliding window; values in [1,1001]) — [FULL-TIME Data Scientist screen] PracHub.
- Language-choice design (Python vs Java vs C++ for three service profiles) — HR screen, PracHub.
- C++ quiz topics reported: C++17/20 MCQ, code tracing, pseudocode complexity, class/method semantics ("memorise C++ class and every type of method") — interviewfox/1point3acres snippets.
(e)/(g) quant tracks
- 3 LC-mediums (greedy/simulation/memoisation) then 5 video maths questions (moments, integral convergence) then a live expectation problem — [FULL-TIME Junior QR 2022] Leader-board (R1).
- 5–6 on-demand video questions on derivatives/integrals — [FULL-TIME/intern-track Jr QR, Nov 2021] Blind gzeniips.
- "How many ways to arrange digits 0–9 so each digit is a multiple or divisor of each neighbour?" — [FULL-TIME Quant Dev] Glassdoor EI_IE608116.0,13_KO14,36.
- Practice-only (R4 ankitkushawaha): SPSC ring buffer, false-sharing struct fix, acquire vs relaxed, "expected rolls to see a 6", biased-coin P(≥3 heads in 5), market-making game with inventory of 500 lots.

### 4.4 Difficulty and style
- OA: 3 problems in 60–90 min, LC easy–medium algorithmically but heavy on implementation/simulation; C++ track adds language-trivia MCQs. Explicit code-cleanliness grading (Leader-board); "any two of three" scoring.
- Take-home graded on hidden tests with a 2-s limit — I/O speed and correct IOC/MODIFY semantics decide the last cases; then discussed in the phone screen.
- Onsite escalation to concurrency-correct C++ (object pool, ABA, RAII) and system design; quant tracks are brutal on timed video maths (5 min per question, no references).
- Intern vs FT: intern OA is 80 min / 3 domain simulations (order tracker, throttler); FT adds the 72-h matching engine, C++17/20 MCQs and a debugging round.

### 4.5 Recurring themes
Order book / matching engine at every stage; sliding-window throttlers and streaming statistics; C++ value semantics (move assignment, RAII) and concurrency bugs; trader-math + webcam probability for QT; code-quality grading.

---

## 5. DRW

### 5.1 Pipeline

**Internship (Software Developer intern; Data Engineer intern)**
- Codility OA, **3 questions / 150 min** — [INTERNSHIP Summer 2024] https://leetcode.com/discuss/interview-question/3811002/DRW-Codility-OA-(Software-Developer-Intern)-Summer-2024-3-Questions/ ; PracHub bank confirms 3-in-150 for intern SWE. DRW's own blog "Preparing for our technical challenge" (drw.com, blocked) describes the Codility challenge; DRW LinkedIn post tags #codility.
- Scoring: partial credit for partially correct; "more points if at least 1 of 3 questions is in C++" — Blind qpfu5tmw (NG). Then team-specific interviews (each team interviews separately; Java or C++ expected).

**Full-time (new-grad, experienced SWE/Quant Dev)**
- NG: Codility 3/150 (2022 cycle) → phone → team interviews; C++ SWE off-campus: OA 3 C++ questions / 120 min (one "find the bug in this snippet", two LC medium-hard) → 1-h technical with senior engineer (GitHub Shivam5022/Interview-Experiences).
- Experienced: recruiter → remote technical rounds with two developers → **take-home** → remote coding → Chicago onsite of 5 rounds (1 coding, 3 technical, 1 hiring manager) — Blind x2f7kLG6; senior data/SWE: take-home then onsite where you extend/modify your take-home live, open-ended systems questions ("no algo live coding") — Blind 72cg8zbn. Quant Dev: take-home → system design → algorithms → culture fit → live coding, ~2 months — Glassdoor DRW-Quantitative-Developer.
- UK SDE 2025: single casual round, no DSA (jointaro 02e50ecf). Summer 2025 intern interviews "real-life problems, not that difficult" (Glassdoor snippet).

### 5.2 Reported questions — Internship

(a)/(b)/(c) Codility OA
- Bank transfers; letter arrangement with lexicographic ordering; string manipulation with constraints — [INTERNSHIP Summer 2024] LeetCode 3811002 (titles only).
- Knockout tournament match counts (n players, adjacent pairs, higher skill advances, return matches per player; O(n log n) simulation) — [INTERNSHIP SWE] https://prachub.com/interview-questions/solve-three-algorithmic-oa-problems
- Robot path planning: output `^v<>` moves visiting required floor cells across 5 subtasks (rectangle border, full rectangle, dumbbell, path, arbitrary connected), walk ≤ 100k — same.
- Max sum of two numbers sharing no decimal digit (10-bit digit masks) — same.
- Nested transactions in an in-memory DB (`begin/get/set/count/rollback/commit`, "ERROR: No active transaction", 200k ops) — [INTERNSHIP Data Engineer] https://prachub.com/interview-questions/implement-nested-transactions-in-an-in-memory-database
- Delete fewest chars so no run of 3 identical letters ("eedaaad"→"eedaad") — [INTERNSHIP DE] PracHub.
- Year-end balance with $5 monthly card fee waived if ≥3 card payments totalling ≥$100 (O(n), O(12) space) — [INTERNSHIP DE] PracHub.
- `isSecurePassword`: ≥6 chars, digit, lower, upper, special from `!@#$%^&*()_`, no spaces — [INTERNSHIP DE] PracHub.

### 5.3 Reported questions — Full-time / experienced

(a)/(b) OA
- Bulb-switcher toggle simulation; max even sum choosing K elements; min-length subarray containing all distinct elements — [FULL-TIME NG 2022, Codility 3/150] https://leetcode.com/discuss/interview-question/1512016/drw-2022-new-grad-swe-codility-oa/
- Odd-frequency string of length N; min |S−T| with minimal same-index digit swaps ("29162","10524"→2); two-choice slot assignment (pseudoforest / union-find) — [FULL-TIME SWE] https://prachub.com/coding-questions/solve-odd-string-digit-swap-patient-slot-assignment ; linkjob drw-codility-assessment.
- Three C++ questions in 120 min incl. "find the bug in this snippet" — [FULL-TIME C++ SWE] Shivam5022/Interview-Experiences.
- LeetCode DRW tags: Subsequence of Size K With Largest Even Sum, Counting Elements, Maximize Score After Pair Deletions (rohithgowda18/InterviewAtlas).
(f) low-level/C++/systems
- "Write pseudocode to serialise a struct to a binary file; how do you handle endianness?" — [FULL-TIME C++ SWE, 1-h technical] Shivam5022.
- "Tell me how TCP/IP works" (open-ended; reasoning > perfection) — [FULL-TIME EXP senior data/SWE] Blind 72cg8zbn.
- LeetCode-style with follow-ups on virtual memory, address space, function pointers; hashmaps + mutex/multithreading; concurrency and pointers; sliding-window with stacks/queues — [FULL-TIME SWE] Glassdoor DRW-Software-Engineer EI_IE235115.0,3_KO4,21.
(d) design
- Real-time market-data dissemination API (REST + message queues); DB schema design — [FULL-TIME SWE] Glassdoor (same page).
(e)/(g) quant dev
- Merge sort; dice-game expected value; a graph problem; window functions over time series; 3 mid-level LC questions with the hardest required in C++ — [FULL-TIME Quant Dev] Glassdoor DRW-Quantitative-Developer EI_IE235115.0,3_KO4,26. "One graph problem I still can't do" — WSO drw/interview (2020 superday, out of range but corroborates).
(i) take-home
- **Tetris engine** (DRW Trading "Tetris Programming Exercise", 4-page PDF): simplified Tetris on a 10-wide grid; pieces Q (2×2), Z, S, T, I, L, J with a column offset (`Q0,I4,L8…`), pieces drop until they rest, full rows clear and rows above drop; input file has one comma-separated piece sequence per line, output the resulting stack height per line — [FULL-TIME EXP, 2022] https://github.com/drunkirishcoder/drw-tetris (PDF + `input.txt` with 20 test lines, solved in Rust). Also reported: take-home "extended live" at onsite (Blind 72cg8zbn), Quant Dev take-home task (Glassdoor).
(R4 practice only, ankitkushawaha HFT: LRU cache, VWAP from trade stream, Bellman-Ford, spinlock vs mutex, memory orderings, mmap, epoll, RVO, coroutines, memory-pool allocator, pub-sub bus, EWMA, FIX parser/router, <1 µs risk check.)

### 5.4 Difficulty and style
- Codility OA: strict O(N)/performance tests, partial credit, 150 min for 3 (intern & NG) or 120 min for 3 in C++ (experienced); C++ earns extra points. Problems are ad-hoc/greedy/simulation more than classic DP.
- Later rounds are team-specific and conversational; experienced loops replace LeetCode with a take-home you then extend live, plus open-ended systems (TCP/IP, endianness, virtual memory). "Moderately difficult"; interviewers may seem unresponsive to feedback.
- Intern vs FT: intern = same Codility format, string/simulation-heavy, then light "real-life" interviews; FT/EXP = take-home + 5-round Chicago onsite with C++/systems depth.

### 5.5 Recurring themes
Codility 3-problem OA; simulation/greedy string problems; C++ preferred and rewarded; take-home (Tetris) extended live; endianness/serialisation, TCP/IP, virtual memory; team-by-team variance.

---

## 6. Flow Traders

### 6.1 Pipeline

**Internship / graduate (trader; graduate software programme)**
- Trader: mental-maths OA 75 questions / 10 min (three sections with negative marking: 30 easy +1/−3/−2, 30 harder +2/−1/−1, 15 estimation MCQ +2/−2/−1; pass 72/120 = 60 %; one-year ban on fail; some practice questions reappear) — [INTERNSHIP & FT trader] R1 https://github.com/Leader-board/OA-and-Interviews/blob/main/Online%20Assessments.md ; 60 Q / 6 min variant also reported (tradermath.org). Then 45-min video with trader + HR (brain teasers, ETF/market talk), then an Amsterdam day of 4–5 × 45-min interviews plus a market-making game on a series of payoffs (quantt snippet; WSO "Technical Interview at Flow Traders").
- Graduate C++ programme 2021: **C++ case study take-home, 36 h** (see 6.3) — R1 PDF.
- Junior Trading System Engineer (India, IIT): resume → Linux/scripting test (50 Q / 60 min, two difficulty sections, shell-command flags) → speed-maths + aptitude + personality → technical interview (ping, nmap, man, SSH reverse tunnelling, "given an IP how would you root it", XSS vs XSRF, TCP vs UDP) — [FULL-TIME NG] ambitionbox.com flow-traders-interview-questions (candidate selected).

**Full-time (SWE Java/C++; experienced)**
- Java SWE: HackerRank 3 tasks + 6 Java questions → video call discussing solutions — Glassdoor Flow-Traders-Java-Software-Engineer. C++ SWE: HR call → HackerRank ~12 questions, >half programming with I/O and corner cases, ~2 h, "most fail here" → HackerRank CodePair with a Flow developer → onsite (culture fit, technical, lunch, HR) — Glassdoor Flow-Traders-C-Software-Engineer. Amsterdam SWE 2024–25: 3 rounds — algorithmic, design, culture fit — Blind Flow-Traders company page.
- Languages: Java and C++ tracks (HackerRank tests are language-specific); Python for quant/trading-system roles.

### 6.2 Reported questions — Internship / graduate

(g) mental maths (trader)
- Sample items from Flow's own 2020 practice paper: `75 + 47`, `156 : 6`, `333 − 157`, `0.5 × 0.05`, `22200 × 0.003`, `8769 + 3654`; estimation MCQ `444 × 132 = a) 58608 b) 62608 c) 66608`, `1850 × 800 = …` — https://github.com/Leader-board/OA-and-Interviews/blob/main/media/Flow_Traders_Example_Math_Test_2020.pdf
- ETF brain-teaser: "ETF priced at x, Apple is y % of it, Apple moves z→z+t, new ETF price?" — [trader] quantt snippet.
(i) take-home (graduate C++ 2021)
- **Risk server** (R1 PDF "Flow Traders Graduate Software Development Program C++ Case Study", 36 h, submit as git branch `flow/graduates/2021`, GCC/Clang, C++17 STL): a TCP server receiving packed binary messages — 16-byte `Header{version,payloadSize,sequenceNumber,timestamp}` then `NewOrder(35 B: listingId, orderId, qty, price ×10⁴, side)`, `DeleteOrder(10 B)`, `ModifyOrderQuantity(18 B)`, `Trade(34 B)`; respond `OrderResponse{orderId, ACCEPTED|REJECTED}`. Per instrument keep NetPos (trades), BuyQty, SellQty; hypothetical worst buy = max(BuyQty, NetPos+BuyQty), worst sell = max(SellQty, SellQty−NetPos); reject if either exceeds the command-line buy/sell thresholds; rejected orders don't change state; disconnect discards a trader's positions. Worked example in the PDF (thresholds 20/15) — https://github.com/gxyau/flow (PDF + `message_specs.h`).

### 6.3 Reported questions — Full-time / experienced

(f) low-level / C++ / Linux
- Template meta-programming and templates, algorithms, design patterns — [FULL-TIME C++ SWE] Glassdoor (snippet).
- Linux: ping internals, nmap, `man`, SSH reverse tunnelling, root a server given its IP, XSS vs XSRF, TCP vs UDP; "difference between list and tuple" (Python) — [FULL-TIME NG TSE] AmbitionBox.
(a)/(h)
- Java OA "mostly numbers and data handling", 3 tasks + 6 Java MCQ — [FULL-TIME Java SWE] Glassdoor.
- HackerRank ~12 questions, input handling and corner cases, 2 h — [FULL-TIME C++ SWE] Glassdoor.
(d) design
- Design round in the 3-round Amsterdam loop (topic unreported) — Blind.
(R4/R3 practice only: order book with O(log n) best price; sliding-window max/min; ETF fair value from basket; k-th largest; unique_ptr vs shared_ptr; move semantics; false sharing; NIC→userspace packet path; biased-coin fair flip; median of stream; rate limiter.)

### 6.4 Difficulty and style
- Trader maths test is the hardest gate (negative marking, 60 % pass, live proctoring). Developer HackerRank is long (12 questions, 2 h) and language-specific with I/O and corner-case emphasis; "most people fail at this stage".
- The graduate C++ case study values simple, readable, STL-heavy C++17 with correct packed-struct parsing and socket handling; no Win API.
- Onsite is a full day with culture-fit weight; system-design round exists for SWE. Evidence on exact SWE onsite questions is thin.

### 6.5 Recurring themes
Mental-maths gate for anyone near trading; binary protocol parsing + TCP risk server; Linux/networking trivia for trading-system engineers; Java vs C++ language-specific HackerRank; ETF pricing intuition.

---

## 7. Da Vinci Derivatives (Amsterdam) — evidence thin

**Pipeline** (Glassdoor E2997120 + WSO snippets; all [unclear/graduate]): OA (mental maths "≈50 tough questions in 10 min, much tougher than Optiver's screening, not expected to finish"; balls-in-bag, coin flips, die rolls, EV, estimates) → HR interview (company knowledge, motivation, quick-fire personal and mental-maths questions) → technical interview with a senior trader (puzzles, market-making game, stock/strike/delta questions), all in quick succession; ~17 days. Software engineer track: "two assignments — one maths, one coding" (Glassdoor Da-Vinci-Derivatives-Software-Engineer); junior SWE/intern rated hardest. IIT intern guides mention Da Vinci quant tests but give no content (SarthakVerma18: rejected, no detail).
**Questions**: no concrete coding questions were recoverable for 2021–2026. Trader questions: option delta calculation, strike/price scenarios, EV of balls/coins/dice; "divide weird numbers in your head to arbitrary precision".
**Style**: fast, quantitative, heavy mental-maths; Glassdoor difficulty 3.3/5, 51 % positive.

## 8. Maven Securities (London) — developer evidence thin, QR evidence good

**Pipeline**
- Graduate SWE (2020–21, [FULL-TIME NG]): Codility entrance exam = one LC-medium flood-fill, 150 min → one-way video interview (failed there) — R1 Leader-board Maven QR write-up (prelude). Note Maven **permanently bans** unsuccessful graduate-programme applicants from re-applying to graduate roles (FAQ confirmed).
- Quant Researcher 2022 ([FULL-TIME]): HackerRank stage 1 = maths/ML MCQ (7 Q / 20 min: probability, statistics, basic ML, "good red herrings") + coding with **sectional** timers 20+20+35 min: LC-easy greedy, LC-medium stack, LC-medium tricky 2-D DP (no going back between sections) → stage 2 HackerRank 4-h data-science/ML take-home (references loading a `pickle`; not auto-graded; scores 127 and 20 obtained via GDPR) — https://github.com/Leader-board/OA-and-Interviews/blob/main/Application%20experiences/2021-22/Maven%20Securities/Quant%20Researcher.md
- SWE (Glassdoor EI_IE716525.0,16_KO17,34/35, [FULL-TIME]): screening → pair-programming round → office round with culture-fit + systems-design interviews; difficulty 3.3/5.
- Trader ([INTERNSHIP/NG]): stats & maths test on a computer with pen/paper, 15 questions / 30 min; in-person final with games against other candidates and one game with a trader; "mental maths and games rather than probability" (Glassdoor Trader/Trading Intern pages).
**Questions**: flood-fill (Codility); greedy / stack / 2-D DP (HackerRank); ML modelling take-home. No verbatim SWE onsite questions found; ankitkushawaha's Maven list (thread-safe bounded queue, placement new, TCP handshake, first missing positive, sliding-window average, O(1) order book, vtables, shared_ptr cost, 45/55 coin market, random-walk hitting time) is explicitly `inferred/general-prep`.
**Style**: sectional timing prevents banking time; explicit code-quality is not mentioned; pair-programming round for SWE; take-home ML for QR.

## 9. Mako (London) — evidence thin, C++ flavoured

**Pipeline** ([FULL-TIME C++/graduate SWE], Glassdoor E484377 snippets; mako.com blog blocked): 50-question ABCD test in 30 min (logic + ~1/3 C++/Python: OOP, time complexity, TCP/UDP, UNIX) → online coding platform with 2 coding tests + C++ questions → coding round with two engineers + a system-design question → technical interviews on optimisation and C++; ~17 days; difficulty 3.2/5.
**Questions reported**: "write a C++ constructor and destructor"; "write a hello-world-style C++ class and add features using templates"; arbitrary-precision integer addition; system design around **market-data consumption**; optimisation questions. Graduate SWE and C++ Developer pages list similar items. No intern-specific reports found.
**Style**: C++ trivia + MCQ screen, then modest coding and market-data design; less algorithmic than Optiver/IMC.

## 10. Tibra (Austinmer, AU) — good first-hand evidence for QT/QTD

**Pipeline**
- Junior Quant Trader 2021 and Quant Trader Developer 2023 ([FULL-TIME NG; Tibra hires trainees]) — R1 Leader-board: HackerRank **take-home style, 48-h window**, 3 questions: Q1 LC-medium with "pesky" implementation + algorithmic parts; Q2 LC-medium straightforward 2-D DP; Q3 HackerRank "approximate solution" question — interpolate/extrapolate to estimate data, partial marks, no score shown. **Identical questions reused every year since 2019-20** (repo author saw the same test three times). Then Talegent tests: English/maths/logic (5–6 questions in 4 min; 3 min per logic item) + ~100-item personality inventory. 2023 QTD: 30-min phone with recruiter incl. brain-teasers ("Jim has twice as many sisters as brothers; Jane has equal brothers and sisters — how many siblings?"; "largest axis-parallel square inside a 10×15 right triangle" → 36) → 3.5-h stage: 2 h solo analysis of a dataset (price + 8 unlabelled signals) in Jupyter/pandas to find tradeable relationships, 15-min presentation, then a 40-min **group** task with another candidate implementing a backtest/PnL; rejection feedback: "deeper statistical analysis, modelling and pandas". Salary quoted AUD 120k; <1 % of ~6,000 applicants hired. https://github.com/Leader-board/OA-and-Interviews/blob/main/Application%20experiences/2023-24/Tibra/Quant%20Trader%20Developer.md
- Glassdoor (E197452 snippets): 30-min numerical + 60-min logical tests (40 speed-maths in 30 min, matchsticks/ordering brainteasers); "coding 3 questions / 48 h, aptitude 1 h, psychometric 30 min, and a **99-minute C++ coding test**" for developer-track; puzzle: 12 poker chips, take 1 or 2, don't take the last — optimal strategy. Difficulty 3.3/5, 30 % positive.
**Categories**: (b) 2-D DP; (h) interpolation/extrapolation approximate problem; (h) pandas signal analysis + backtest; (g) brain-teasers; (f) 99-min C++ test (content unreported).
**Style**: relaxed OA timing but recycled questions; heavy personality/aptitude screening; the deciding round is data analysis + group work, not algorithms.

## 11. Eclipse Trading (Hong Kong) — evidence thin

**Pipeline** (Glassdoor E423801 snippets): Trader ([INTERNSHIP/NG]): online tests (speed maths, logic, market knowledge; onsite versions of mental maths / financial knowledge / options / probability with 10–15-min limits) → phone with trader → 2 days of market-making games + trader interviews; questions on estimation, "who is the Fed chair", odds/Kelly criterion, market-making strategies. Developer ([FULL-TIME]): HackerRank link to complete within a week → HR screen → take-home assessment → first round with two senior developers including **code review of the take-home** → team-lead round on experience/culture; "basic CS knowledge" in technicals.
**Questions**: no concrete coding problem text recovered. Kelly-criterion odds questions and market-making game for traders.

## 12. Vivienne Court (Sydney) — evidence thin

**Pipeline** (Glassdoor E1021406 snippets, [INTERNSHIP QT intern & graduate trader]): CV screen → assessment tasks (cognitive skills, pattern recognition, statistics/probability problems) → in-person with HR + senior trader → final day with **coding questions**, standard trading games, probability problems and model-building questions. Difficulty 3.4/5, 66 % positive.
**Questions**: "estimate how many cars you'd see on a drive" with probability follow-ups; "would you take a 50 % coin flip to win $1,000 if that was all your savings?" (risk/utility); coding content unreported.

## 13. Trexquant (Stamford / Gurugram / remote) — good evidence for QR

**Pipeline** ([FULL-TIME QR / Global Alpha Researcher; also early-career India], 2022–2025): HR call → **Hangman take-home** → coding/technical round(s) → project challenge/superday presentation → quant lead → CEO round (1point3acres thread 1142886; WSO trexquant/interview; Glassdoor EI_IE610375).
(i) take-home — the well-known one
- **Hangman API challenge**: write a `guess(current_word_with_underscores) → letter` function that plays Hangman against Trexquant's API; 6 wrong guesses allowed; training dictionary ≈250,000 words; test words are a disjoint 250,000-word set (enforced by code review — no other dictionary allowed); up to 100,000 practice games, then 1,000 recorded games; baseline ≈18 % win rate; reported advancement threshold ≈55–60 % — spec reproduced at https://github.com/whosquant/hangman (README quotes the official text); many solutions 2022–2026 (n-gram + length-conditioned letter frequencies ≈55–60 %; BiLSTM/transformer 63–73 % — https://github.com/Hritvija/Trexquant-Hangman-Challenge, https://github.com/deadsmash07/Hangman-Game).
(a)/(b)/(e)
- 3Sum (distinct triplets summing to target) — coding round, naukri code360 Trexquant Dec 2024 (snippet).
- Derive linear regression in matrix form (normal equations, loss) and **code it from scratch**; Markov-chain problems from the "Green Book"; LC-medium at the end of an 80 %-behavioural HR round; 45-min round = resume + Green-Book probability + LC-style — [FULL-TIME QR 2025] 1point3acres thread 1142886 and WSO quant-researcher-0 (snippets).
**Style**: ML-flavoured take-home is the gate; later rounds are light LeetCode + probability + project presentation; multi-round (5–6) with senior leadership.

---

## 14. Cross-firm summary tables

### 14.1 OA platform / format by firm and track

| Firm | Intern OA | Full-time OA | Platform |
|---|---|---|---|
| Optiver | 2 coding / 2 h (or 75-min spec problem) + 20-min MCQ + Zap-N | 2 coding / 120 min + 10 OOP MCQ / 20 min + 9 Zap-N games; 2025–26: 1 proctored 90-min or 3/90 | HackerRank + Zap-N; SHL for some regions |
| IMC | 2 coding / ~105–120 min | 2 coding (DP/graph) / 120 min, sometimes 7 items with MCQ | HackerRank; BrainsFirst Neurolympics; HireVue-style video |
| SIG | Trader: 14–50 maths Q / 20–75 min; SWE: unit-test implementation | CodeSignal 4 (2 easy + 2 hard) or 2 problems / 90 min; Mettl for quant | CodeSignal, HackerRank, Mettl |
| Akuna | 3 problems / 80 min (+ C++ MCQ) | 3 problems / 60–90 min + 10 C++ MCQ; 72-h matching-engine take-home | HackerRank; EasyHire/HireVue maths |
| DRW | 3 / 150 min | 3 / 150 (NG) or 3 C++ / 120 min; take-home (Tetris) for EXP | Codility |
| Flow Traders | 75 maths / 10 min (traders); 36-h C++ case study (grads) | HackerRank 3 tasks + 6 Java Q, or ~12 C++ Q / 2 h | HackerRank; proctored maths |
| Tibra | — | 3 Q / 48 h (recycled) + Talegent; 99-min C++ test | HackerRank, Talegent |
| Maven | trader maths 15 Q / 30 min | Codility flood-fill / 150 min (SWE); HackerRank MCQ + sectional coding + 4-h ML (QR) | Codility, HackerRank |
| Trexquant | — | Hangman API take-home | own API |
| Mako | — | 50 MCQ / 30 min + 2 coding tests | online platform |
| Eclipse | speed maths/logic/market tests | HackerRank within a week + take-home | HackerRank |
| Da Vinci / Vivienne Court | ~50 maths / 10 min; cognitive + stats | maths + coding assignments (DV SWE) | in-house |

### 14.2 Do they run hidden tests? Code-quality emphasis?
- Hidden tests with time limits: Optiver, IMC (also onsite unit tests), Akuna (OA + take-home, 2-s limit), DRW (Codility performance tests, partial credit), Flow Traders (HackerRank), Tibra (partial-credit "approximate" question), SIG (unit-test-driven OA).
- Explicit code-quality grading: Optiver (rejections at 90 % correctness; style reviewed), Akuna ("cleanliness and readability" stated in OA), IMC (rejection for not following the intended approach despite green tests), Flow Traders case study ("simple, efficient, readable"), Eclipse (code review of take-home).
- Take-homes graded by hand and discussed live: Akuna, DRW, Flow Traders, Eclipse, Maven (QR ML), Trexquant (win-rate + code review), Tibra (data-analysis presentation).

### 14.3 Internship vs full-time differences (where evidence supports it)
- Optiver: same OA family; intern loops = HR + verbal system design + pseudocode, group logic puzzles on campus; NG/EXP add C++ memory/cache/vtable/threading, harder LLD OA, and a design round that drills to hardware.
- IMC: same OA family (LC-1381, knight-BFS); intern loop uses group code review and a 90-min order-book pair session; NG/EXP add one-way video CS trivia, 2.5-h matching-engine build with unit tests, smart-pointer/vtable/false-sharing depth, and for Java seniors a GC-efficiency take-home.
- SIG: intern developer track tests pandas/numpy and `std::vector`; FT developer track has CodeSignal 2-easy/2-hard and SOLID design; trader OA identical across levels.
- Akuna: intern OA = 3 simulations in 80 min; FT adds C++17/20 MCQs, 72-h matching engine, debugging round, object-pool concurrency task.
- DRW: intern and NG share Codility 3/150; EXP replaces with take-home + 5-round onsite.
- Flow Traders: graduate C++ programme uses a 36-h case study; experienced SWE uses long HackerRank + CodePair + design round.
- Tibra/Trexquant/Maven QR: no separate intern data; graduate pipelines are take-home-centric.

### 14.4 Cluster-wide recurring question families
1. Order book / matching engine / trade-stream reporter (Optiver, IMC, Akuna, DRW-practice, Flow risk server, Maven-inferred).
2. Time-windowed structures: log server, rate limiter/throttler, sliding-window stats (Optiver, Akuna, SIG-practice).
3. Dividend/price-adjustment and PnL arithmetic (Optiver, Akuna multi-stock profit).
4. Grid/graph BFS with a twist (IMC knight+bishop, Optiver error-coded graphs, DRW robot walk).
5. Stack/heap/LRU design variants (IMC LC-1381+sum, Optiver LRU, SIG k-th largest).
6. C++ internals: implement vector/shared_ptr, move assignment, vtable layout, false sharing, cache/TLB, endianness/packed structs, RAII/object pools (Optiver, IMC, SIG, Akuna, DRW, Flow, Mako).
7. Mental-maths and EV gates for anything trader-adjacent (Optiver 80-in-8, Flow 75-in-10, Da Vinci 50-in-10, SIG, Akuna, IMC, Maven, Tibra, Eclipse).
8. Take-homes with binary or text protocols (Akuna, Flow, DRW, Trexquant).
