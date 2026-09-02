# Time-efficient coding / DSA prep for quant dev, quant trader and quant researcher interviews
## What works, what doesn't — according to people who passed, failed, or interview

_Compiled 2026-09-01. Evidence-graded. Read the "Sourcing caveats" section first._

---

## 0. Sourcing caveats (read this)

**What could and could not be read.** During this research session the network egress proxy blocked direct reads of almost every primary community and firm source: janestreet.com and blog.janestreet.com, hudsonrivertrading.com, citadelsecurities.com, twosigma.com, optiver.com, imc.com, news.ycombinator.com (and hn.algolia.com), reddit.com, teamblind.com, quantnet.com, wallstreetoasis.com, glassdoor.com, leetcode.com/discuss, medium.com, quora.com, interviewing.io, web.archive.org, and every prep-company site. The session's web-search quota was also exhausted after the first ~16 searches. What *was* readable in full: GitHub (github.com / raw.githubusercontent.com), which turned out to hold a surprising amount of first-hand material — personal interview retrospectives hosted as blog source, IIT placement-season prep logs written by people who got HFT/quant offers, and two large curated compilations that quote (with URLs) Glassdoor, LeetCode Discuss, Blind and WSO threads I could not open directly.

**Evidence grades used below**

| Grade | Meaning |
|---|---|
| **A — Official** | Firm's own prep page / blog / mock-interview video. Where the page itself was blocked, the content is taken from search-result excerpts or from GitHub compilations that cite the page; marked "(via excerpt)". |
| **B — First-hand, multiple** | ≥3 independent first-hand accounts (people who interviewed or got offers) agree. |
| **C — First-hand, single/few** | 1–2 first-hand accounts. Real, but could be idiosyncratic. |
| **D — Weak** | Prep-company marketing, synthesized "guides", tweets, unverifiable compilations. Included only when nothing better exists, and flagged. |

Where a claim below has no grade it is my synthesis of the graded evidence.

---

## 1. Bottom line (the time-efficient answer)

1. **The coding bar at quant firms is "clean, correct, fast implementation of medium-difficulty problems while talking", not "know every algorithm".** Jane Street's own guidance and its interviewers say they *deliberately* avoid "algorithm bingo" / single-clever-insight questions; HRT says it prefers "strong fundamentals" over "obscura and tricks"; SIG employees say "no leetcode, real-life problems". (A/B — §3, §4.)
2. **The exception is automated online assessments (OAs) — especially HRT, DE Shaw, Jump, Citadel and the Indian HFTs (Graviton, Quadeye, Tower, QuantBox, AlphaGrep)** — which are CP-flavoured and timed hard: 3–4 problems in 60–120 min at roughly Codeforces 1500–1800 (occasionally borrowed from CF 2000+). This is where CP-style speed actually matters. (B — §3.2, §4.2.)
3. **Minimal viable syllabus** (what actually appears in the live rounds, from ~60 reported questions across JS, HRT, Citadel, Optiver, IMC, DRW, SIG, Jump, DE Shaw, Two Sigma): hash maps/sets, arrays/strings/two-pointers/sliding window, stacks (incl. monotonic), heaps (running median, k-smallest, top-k window), binary search, BFS/DFS on grids and graphs, topological sort/cycle detection, tries (once), intervals, easy/medium DP, linked-list pointer surgery, and — very frequently — *"implement this class/data structure/simulation"* (LRU cache, stack machine, order book/matching engine, custom vector, log server, scheduler, connect-four variant, Tetris). Segment trees, union-find, advanced DP, flows: essentially absent from live rounds; occasionally in OAs. (B — §5.)
4. **The single most-reported way people fail live coding rounds is not lack of algorithms but execution**: slow/fumbling implementation, not handling boundary cases, not adapting when the interviewer "layers requirements", talking too much or too little, and freezing under time pressure. An experienced engineer who got Citadel and HRT offers failed Jane Street specifically because he "spent too much time explaining and didn't have enough time to finish the code". (B — §6.)
5. **Time budgets people actually reported**: campus/new-grad candidates who got HFT offers prepped ~3–4 months in season (on top of prior CP/DSA background), using one curated list (Blind 75 / NeetCode 150 / Striver sheet — "more than enough to clear all the tests") plus CSES and some Codeforces, with a 30-minute-per-hard-problem rule. Working professionals on Blind report ~200–225 problems over 1–5 months (1–2 h/day over 4–5 months, or 4–5 h/day over ~1 month). Nobody credible reported needing 500+ problems. (B/C — §7.)
6. **What is over-prepared**: hard DP and exotic data structures for live rounds; mental-math and brainteasers for *dev* roles (Jane Street: "dev interviews are about programming, plain and simple"; trading-systems guide: "math puzzles are not commonly asked in trading systems developer interviews"); C++ template metaprogramming for research roles; "easy" LeetCode once you are fluent. **Under-prepared**: writing code in a non-running editor (Jane Street, Google-Docs-style), edge cases, OOP/class-design tasks in C++ (Optiver, IMC, DE Shaw, Graviton), C++/OS internals for dev roles (HRT, Citadel, Squarepoint, QuantBox), and — for QR/QT — the fact that the *coding* round is usually the easy part and probability is the filter. (B — §5, §8.)
7. **No credible evidence** was found for or against spaced repetition of problems, and nothing first-hand credited mock-interview platforms (interviewing.io/Pramp) specifically — but several offer-holders credit *peer/real mocks* ("gave several Tech SDE interviews as a mock for tech rounds", "conducting mock interviews… knowing things and doing well in interviews is very different"). (C — §4.5.)

---

## 2. What the firms say they test (official guidance, grade A, mostly via excerpts)

**Jane Street (SWE).** Official pages: [Preparing for a Software Engineering Interview](https://www.janestreet.com/preparing-for-a-software-engineering-interview/), [Interviewing at Jane Street](https://blog.janestreet.com/interviewing-at-jane-street/), [What a Jane Street dev interview is like ("Memo")](https://blog.janestreet.com/what-a-jane-street-dev-interview-is-like/), [Interview process — 2020 edition](https://blog.janestreet.com/jane-street-interview-process-2020/), [official mock interview video](https://www.janestreet.com/mock-interview/). Excerpts obtained: "we prefer open-ended problems that have several plausible angles of attack"; "the bulk of technical interviews ask you to work through a coding and algorithms problem with 1–2 full-time Jane Street software engineers, with the goal of understanding how you work"; "Jane Street doesn't ask software engineers to do mental math or logic puzzles; dev interviews are about programming, plain and simple"; the mock video "offers advice on communication, code quality, and practice". A GitHub compilation paraphrasing the prep page: "write real code in the strongest language; collaborate on open-ended problems; communicate clearly; avoid relying on one clever insight or 'algorithm bingo'" ([source](https://github.com/aryehcarmi/leetcode-interview-coach/blob/main/skills/leetcode-interview-coach/references/interview-calibration.md)). Jane Street job posts (mirrored on GitHub) confirm: "most hired engineers arrive with zero OCaml experience; you learn it on the job" and that the ML-intern loop "follows the same structure as our Software Engineering intern interviews… an on-site with 2–4 technical rounds".

**Hudson River Trading.** Official: [How to prepare for your SWE interview at HRT](https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/), [Engineering and interviewing at HRT](https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/). Excerpts: interviews are "coding and debugging rounds, technical design discussions, and team fit"; HRT evaluates "collaboration — whether you take hints well and have openness to a different approach" and "teachability — did you apply ideas discussed earlier in the interview to subsequent problems"; HRT "strays away from 'burst of insight' leet-code style questions, preferring strong programmers with strong fundamentals but avoiding obscura and 'tricks'"; paraphrase: "deep fundamentals, listening, direct implementation, and low-level/runtime understanding matter more than obscure tricks". HRT also states use of AI tools in interviews is "strictly prohibited".

**Citadel Securities (early career).** Official page ([link](https://www.citadelsecurities.com/careers/career-perspectives/internship-and-new-graduates-engineering-interview-process/), blocked) paraphrased on GitHub: "explain strategy, clarify, discuss tradeoffs, use hints productively, and demonstrate programming plus DSA in timed coding."

**Two Sigma.** Official page ([link](https://www.twosigma.com/careers/interviewing-at-two-sigma/interviewing-for-software-engineering/), blocked) paraphrased: "prepare DSA, Big-O, testing, design, memory/performance, and language fluency; some roles also probe concurrency and system design."

**Optiver / IMC.** Optiver's SWE tips page ([link](https://optiver.com/working-at-optiver/career-hub/optiver-interview-tips-for-software-engineers/), blocked) paraphrased: "know the language and standard library under the hood, complexity, architecture, networking, concurrency, memory, latency, and how a design changes under new constraints." IMC's how-to-prepare page ([link](https://www.imc.com/ap/articles/how-to-prepare-for-an-interview-at-imc), blocked) quoted in a compilation: an automated "purely theoretical" LeetCode-style screening round, then a round pairing discussion with a coding exercise on "an approximation of our actual trading system".

**Takeaway (A):** every firm that publishes guidance says the same three things — write real working code, communicate/collaborate, and don't rely on trick algorithms. None of them tells you to grind hundreds of problems.

---

## 3. What the rounds actually look like (first-hand reports)

### 3.1 Jane Street (SWE / SWE intern) — grade B
- Full-loop candidate, NYC, accepted offer, April 2024 (Glassdoor, quoted in a [GitHub compilation](https://github.com/pushpa-kumar/placement-prep/blob/main/raw-notes/company-janestreet-jump.md)): "Coding problems seemed more implementation intense… interviewers have a strong emphasis on writing clean, understandable code. Communication and collaborating with the interviewer also appears important, solving the problem perfectly doesn't seem to be as important… Although the questions interviewers ask aren't inherently difficult on the surface… it feels like the criteria they're using to judge you is more wholistic and stricter than other companies." System-design "only asked to lateral/experienced applicants"; "no behavioral rounds for engineers".
- Another (June 2024): "questions they ask are in multiple steps" and "without allowing interviewee to run code".
- SWE intern, London (student guide, [GitHub](https://github.com/How-to-faang-UTCN/How-to-faang-Guide)): OA 45 min, "coding challenge only, no algorithm-heavy DSA — relies heavily on data structures/hash-maps/sets"; superday "3 rounds ~45 min, two interviewers per round, coding-only, language-agnostic in a Google-Docs-style non-runnable editor. Problems are game-like/real-world scenarios (modified connect-four, modified trading bot) that start simple and keep layering requirements to test adaptability under pressure."
- Reported problems: connect-four with infinite width (multiple reports), stack machine, custom stack with extra ops, Tetris, video-player API (under-specified by design), flag users with exactly k consecutive failed logins, streamed move-sequence detection, "optimal strategy for coin-flip game — no scratch paper". Candidate note on the stack machine: "emphasis on the small details, which one does not think about."
- Experienced SWE (offers from Google, Apple, Citadel Sec, HRT; **rejected by Jane Street**), [blog](https://github.com/OneRaynyDay/oneraynyday.github.io/blob/master/_posts/2020-09-30-Interviewing-During-Covid.md): "Time pressure — Jane Street. This is probably why I failed their interviews, which were a bit longer than usual… I tend to explain my approach before coding anything… I probably spent too much time explaining and didn't have enough time to finish the code."
- Blind threads (search excerpts only): Jane Street "wants to weed out candidates that are 'interview ready' because they do leetcode every day", cares about "clear, explainable code" over "algorithm tricks"; advice to "practice in front of others asking questions" and "find more code-heavy rather than algo-heavy leetcode problems"; design-ish questions like "write a chess game or AI bot" that you must actually code.

### 3.2 HRT — grade B
- OA: many reports. C++ SWE full-time ([Shivam5022](https://github.com/Shivam5022/Interview-Experiences)): "90-minute CodeSignal, four easy competitive-programming questions." Systems intern 2021 ([avinal](https://github.com/avinal/avinal.github.io/blob/main/src/content/posts/blogs/hrt-interview-1.md)): Codility, 3 questions, 90 min inside a 2.5 h window, "clear and medium level", and HRT states "while correctness and performance are the most important factors… we will take test duration into account as well." A 2022 candidate ([Lazar-Ilic notes](https://github.com/Lazar-Ilic/Lazar/blob/main/Notes/Computer%20Science/Algorithms/Interviews%20Coding%20Rounds/Hudson%20River%20Trading.txt)): "1 hour to complete 4 coding questions: 1 easy and 3 mediums [or 2 mediums and a hard]"; his complaint: "the only way you can complete the test within the time span is if you are Red on CodeForces… what feedback do you get if they managed to get all 4 within the time limit? That they have seen the problems before and memorised the answer." Reported OA problems: two-rooks placement, Manhattan-distance-to-all-houses (multi-source BFS), Eulerian path feasibility, remove comments from C++ source, chemical-equation balancing ("wrote 10+ edge cases"), binary-string add, min-queries with row/col removal (two heaps), word search with memo, arrival-time binary search.
- Phone screens are frequently **not coding**: 45 min on "`inline` pros/cons, vector vs list internals, how malloc works, demand paging, how the kernel allocates memory, sbrk/mmap" (full-time C++); for the intern: "Linux/Unix, C++ pointers and memory, Python/Bash, tooling, resume cross-check".
- Onsite (experienced candidate, got offer): 6.5 hours; "systems design, general algorithm questions, language-specific C++ knowledge, math problems"; total ~10 h of interviewing including OA and 2 phone screens. Onsite OO-design problem: "network packet routing system… TLE; performance-efficient OO C++ required."
- Search excerpts: "LeetCode medium and hard plus brain teasers and probability puzzles… very coding intensive… know Python or C++ well… explain CLT and LLN intuitively"; "even though the title had C++ in it… the interview ended up being in Python."

### 3.3 Citadel / Citadel Securities — grade B
- Campus SWE intern (IIT Delhi, got offer, [source](https://github.com/devclub-iitd/Intern-Prep-Series-25/blob/main/Interviews/Citadel_Pritesh_Mehta.md)): Round 1 "BFS", Round 2 "implementing Topological Sort", Round 3 projects/resume.
- OA reports: IPO share allocation simulation, Roman numerals, stable sort by length, stack implementation; "quite easy relative to onsite".
- Onsite/phone (compilation of Blind/LeetCode/Glassdoor): currency-exchange best path (graph; "missed edge cases like self-loops; rejected"), producer batching class, best-buy-sell profit, 2048 simulation, thread-safe counter, ring buffer, external merge sort, top-k in sliding window; **C++ debugging round with obfuscated code, 2 hours**; Blind: "asked multiple questions on std C++ structures underneath"; Blind (6 YOE): "younger → LC medium/hard; older → multithreading/systems"; 1point3acres: "single-fail onsite: weak round → next cancelled".
- QR (experienced, got offer): "really interesting math problems that aren't related to finance at all… interviewer continuously provided new problems"; "grilled me a lot on low level C++ stuff". Search excerpt for QR: "first [interview] focused on probability and statistics… second including coding… a dynamic programming problem"; OA "3 problems in 90 minutes".

### 3.4 Optiver / IMC — grade B
- Optiver SWE OA (multiple sources incl. a 2023 grad on GitHub): "neuro-assessment games (~1 h), HackerRank knowledge test (10 OOP MCQs, 20 min), HackerRank coding test (2 assignments, 120 min)". Coding tasks are *implementation/class* tasks: order-book simulation, supermarket checkout tracker, log server, process scheduler, LRU cache, KMP, S-expression parser, market-making game class. Candidate on the IIT campus version: "75-minute coding assignment where they described the requirements of a graph based network, we were simply asked to implement it (no optimizations required)… They just wanted to test if you could get a working solution."
- Optiver, **experienced (Principal) loop, 2026** ([candidate's prep repo](https://github.com/ErrolMc/OptiverInterviewPrep)) — recruiter feedback on why people get cut: "(1) graph/traversal problems (parse → build → traverse, with cycles and multiple paths); (2) slow execution — fumbling parsing/debugging and not adapting when the interviewer adds a twist; (3) for the experience review, architectural-ownership stories, not 'I improved an existing system.'" Takeaway written by the candidate: "drill graphs above all, and solve fast then iterate (MVP-first)."
- Optiver technical themes (Glassdoor UK): "write your own vector; CPU cache and TLB; multithreading; memory-leak detection". Optiver trader/research intern: no coding; "80 in 8" mental math, probability, guesstimates, card-game strategy.
- IMC: OA "two questions, both DP, 2 hours"; BFS knight problems; stack-with-increment variant ("Python solutions timing out initially"); onsite "implement a matching engine — skeleton code and unit tests, fill in add/delete/trade logic"; IIT-B campus (Glassdoor): OA "3 coding questions of LeetCode Medium/Hard, all on graphs, 1 debugging question in OOP, C++ only", then a pen-and-paper DSA round on a 10-page spec followed by a coding round where "more than passing all test cases they were interested in the way I approach the coding."

### 3.5 DRW, SIG, Jump, DE Shaw, Two Sigma, Squarepoint, Indian HFTs — grade B/C
- **DRW**: OA "three C++ questions in 120 min — one find-the-bug, two LeetCode medium-to-hard"; take-home/pen-and-paper "two CP questions (~CF 1700) plus two systems questions (concurrent bank transfers with locks; remove branching from a snippet)"; interview: "serialize a struct in binary… how do you handle endianness?"; Blind: "you get more points on OA if you write at least 1/3 questions in C++"; senior/UK: "no complicated DSA questions", take-home + onsite refinement, "don't expect perfect knowledge [of TCP/IP] but enough to make educated guesses and explain your reasoning."
- **SIG**: Blind: "all discussion based… no leetcode"; "no [silly] LC style q's but real life problems"; employee guidance: "when and where to use data structures and basic searching/sorting algorithms" over syntax; trading-systems intern: OA C++ strings/arrays, phone screen "joins, merges, aggregates using numpy/pandas", superday "implement std::vector from scratch". CodeSignal OA: "4 questions, first two easy, last two very hard".
- **Jump**: intern OA 3 questions/105 min (string validity, tree DP); onsite: implement a trie in C++, implement a hash map and discuss tradeoffs, swap without temp, trailing zeros of 1000!; QR Zoom: "create a linked list, swap two nodes".
- **DE Shaw (India, dev intern)**: OA "~1h20m, 3 DSA problems of increasing difficulty (DP, greedy, bitmasking)", "3 questions typically 1500–1600 [CF] difficulty; solving 2.5 leads to shortlisting"; rounds: graph problem in C++, inheritance/smart pointers, "design a Banking System class in C++, iteratively modified on interviewer feedback", 1–2 Brainstellar-style puzzles.
- **Two Sigma** (search excerpts of LeetCode Discuss/guides only): HackerRank round then phone; "graphs, trees, DP at LeetCode medium-hard, code-quality refactoring and numerical computation tasks"; QR adds regression/experiment-design discussion.
- **Squarepoint (C++ SWE)**: OA "two CP questions — one two-pointer (~CF 1600), one tricky implementation"; R1 CS trivia + "live-coding debug of a dummy vector implementation (missing destructor, copy ctor, leaks, bounds)"; R2 "how many copy/move/assignment calls in this snippet; char** exercise"; R3 "given a thread-safe queue and a benchmark, suggest optimizations."
- **Graviton / Quadeye / Tower / QuantBox / AlphaGrep (IIT campus)**: Graviton dev test "4 questions similar to Codeforces 1600–1700" + systems Qs; onsite "implement shared_ptr", CPU pipelining, branch prediction, "branchless binary search"; QuantBox OA "15 CS MCQs in 20 min + 3 non-CP C++ questions in 25 min", then a 3–4 h systems interview (shared_ptr, String class, memory pool, vtables, lock-free list, RCU); AlphaGrep QR OA "graph, DP, search & sort — CSES-style"; Tower: "CP, probability, markets"; generic campus test format (offer-holder): "2 leetcode hard questions with 30 mins each and an MCQ section of CS fundamentals or CP fundamentals or a quant section."

---

## 4. Methods: what the evidence says works and doesn't

### 4.1 LeetCode — which list, how many
- **Works, with a curated list, not volume.** IIT Delhi placement (joined QuantBox as dev; interviewed Optiver, Graviton, Quadeye, Tower, DE Shaw) ([repo](https://github.com/anirudhakulkarni/Placements-2024)): "Striver SDE Sheet, blind75, and Neetcode150 — solving these sheets is more than enough to clear all the tests"; "I kept a target of 30 minutes per leetcode hard question until I gave up and saw the hint"; "solving easy [is] a potential time waste." Then CSES ("probably a good source of questions after leetcode… most of the questions are good"), and a warning that "tests for HFTs sometimes borrow questions from codeforces 2000+ directly", particularly "dp on graphs". (C, strong specificity)
- IIT Bombay offer-holder ([PrepForge](https://github.com/PsychoX21/PrepForge/blob/main/Intern%20Prep.md)): "The level of questions they ask is much easier than any of this (I think someone able to maintain a 1600 rating is good enough)." IIT Delhi tips: "Leetcode is crucial for interview tests; start with the first 150 problems"; Codeforces "1600–1800 are generally sufficient". (B across three IIT cohorts)
- Berkeley QR/QT candidate ([Samarth Goel](https://github.com/sgoel97/blog/blob/main/content/blog/quant-interview/index.md)): "The best way to practice this is to stay sharp on Leetcoding skills. I find the Grind 75 to be a solid starting point and benchmark of Leetcode ability… make sure to have CS 170 level knowledge of programming and algorithms." (C)
- Blind snippets (working professionals, generic-ish): "completed 225 questions", "200ish leetcode problems", "a list of 75 problems can give you optimum breadth and depth". (C/D)
- A tweet-thread (D, unverified): "Blind 75… Dynamic programming is the most common failure point at final rounds at Citadel and Jane Street specifically." No first-hand account corroborates DP as *the* failure point; treat as weak.
- **Verdict:** one list (Blind 75 → NeetCode 150 / Grind 75) done *timed and to completion*, then CSES for HFT OAs. Skip easies once fluent. Nobody who passed reported needing more than ~200–250 problems.

### 4.2 Competitive programming — necessary or overkill?
- **For OAs at HRT / DE Shaw / Jump / Indian HFTs: helpful and sometimes decisive.** Consistent first-hand rating anchors: Graviton "CF 1600–1700", DE Shaw "1500–1600", Squarepoint "~1600", DRW "~1700", IIT-B "1600 is good enough", IIT-D "up to 1800". HRT OAs are described as "easy CP questions" by one offer-track candidate and as "only completable if Red" by a frustrated one — the difference is speed under 15-min-per-problem budgets. (B)
- **For live rounds at Jane Street, SIG, Optiver, DRW-senior: not what is tested.** Jane Street explicitly avoids "algorithm bingo"; its intern OA has "no algorithm-heavy DSA"; SIG "no leetcode". (A/B)
- A hiring-signal essay (D, synthesized): CP rating is "the ultimate signal for QD/SWE and a strong one for QT/QR", with the caveat that "a rating you inflated by grinding pattern-matched problems decays the moment an interviewer asks you to reason aloud about an unfamiliar one."
- **Verdict:** target ~CF 1600 speed (solve Div-2 A–C reliably, D sometimes) if your pipeline includes HRT/DE Shaw/Jump/Indian HFT OAs. Beyond ~1800 is overkill for interviews (it may still help résumé screening).

### 4.3 Timed practice / non-running editors
- Every account of failure in live rounds mentions time: Jane Street rejection "time pressure"; HRT OA "very frustrating time limit"; Optiver principal "slow execution"; IMC OA "Python solutions timing out". Jane Street and IMC run rounds in non-runnable editors / pen-and-paper. (B)
- **Verdict:** practice under a clock, and practice in a plain text editor without running code, then mentally test. This is the highest-leverage habit in the corpus.

### 4.4 Building projects (order book, backtester)
- **Helps only where the round *is* an implementation task**: Optiver OA (order book, checkout system, scheduler), IMC onsite (matching engine with skeleton + unit tests), Jane Street (connect-four/Tetris/trading-bot with layered requirements), DE Shaw (banking system class), Graviton/QuantBox (implement shared_ptr / memory pool / String class), SIG (implement std::vector). (B)
- Offer-holder advice: learn C++ topics "through practical projects rather than treating topics as blackbox"; HRT phone screen "cross-checked the resume closely — keep only genuine tool/work experience". (C)
- A backtester project has no reported bearing on any coding round; it is résumé/QR-discussion material only. (no evidence of it helping in coding rounds)
- **Verdict:** don't build a portfolio project *for the coding rounds*. Do practice "implement a small system in 45–90 min from a spec" (LRU cache, order book with add/cancel/best-bid, matching engine, event scheduler, tiny vector/shared_ptr), because that is literally the format at Optiver, IMC, DE Shaw, SIG, Jane Street.

### 4.5 Mock interviews and talking aloud
- Offer-holders: "I gave several Tech SDE interviews as a mock for tech rounds and HR rounds" (used real lower-priority interviews as mocks); "Stay confident in interviews (knowing things and doing well in interviews is very different)… mock interviews, speak clearly, keep dialogue"; "articulate your thought process clearly. Don't start blabbering immediately; take a moment." A year-long job-search retrospective (Chinese, quant roles 2018–19): the writer went "from stuttering and freezing when asked an algorithm question (interviewer: 'Just start from brute force solution… then we can talk about optimization') to sharing my thinking with the person on the other end of the line", and notes "utilitarian problem-grinding for interviews is different from real ability". (B for "talk through", C for mocks)
- No first-hand account in this corpus credited interviewing.io/Pramp specifically. Jane Street publishes its own mock (A).
- **Verdict:** do 3–5 mocks with a human (peer/real interview), specifically rehearsing the *brief plan → code → test* rhythm. The Jane Street failure above shows "talk through" can be over-done: plan in ≤3–5 minutes, then code.

### 4.6 Books
- Green Book (Zhou, *A Practical Guide to Quantitative Finance Interviews*): the one book cited by nearly everyone for QT/QR *math*; an experienced SWE who got Citadel/HRT offers "only solved one problem per section to timebox math preparation". Aniruddha Deb (Optiver SWE intern): "Amazing book. Especially the brainteasers and Probability section. Must do"; on *Fifty Challenging Problems*: unhelpful, "loosely worded"; on *Heard on the Street*: "looked like Cracking the Coding Interview but for quant, and I detest that book." (B for Green Book; C for the others)
- CLRS, EPI, CTCI, Skiena: **no offer-holder in this corpus credited any of them for quant coding rounds.** CTCI appears only in generic lists.
- C++ books: *Effective Modern C++*, *C++ Concurrency in Action*, *Linux Programming Interface* appear in curated lists (D) — but the C++ *topics* that first-hand accounts say were asked are concrete: "smart pointers, templates, move semantics, virtual destructors, const correctness, lvalue/rvalue", plus "copy elision, vtable, padding/packing, static, exceptions, iterators, std::threads" and OS: malloc internals, demand paging, sbrk/mmap, process vs thread, spinlock vs mutex, cache/TLB, false sharing. (B)
- **Verdict:** for coding rounds, books are the least time-efficient input. Use them as reference for the specific C++/OS list above.

### 4.7 Python fluency for QR / numpy-pandas drills
- Evidence that pandas/numpy is tested live: HRT QR onsite "data science (pandas, prediction)" round; SIG trading-systems phone "joins, merges, aggregates using numpy/pandas"; HRT phone "pandas-based task (expected if on resume)"; Two Sigma "numerical computation tasks". (B)
- Search excerpts (prep sites, D): "at banks and most hedge funds, Python interviews stop at 'can you write clean Python and use pandas'… for research-track at Two Sigma, XTX, AQR, Citadel, numpy/pandas internals are fair game."
- **Verdict:** for QR, a few hours of drills on groupby/merge/rolling/vectorisation is cheap insurance; the coding round itself is usually LeetCode-medium (Grind 75 level), and the real filter is probability/statistics.

---

## 5. Minimal viable syllabus (what actually shows up)

Derived from the ~60 reported live-round and OA questions in §3.

| Tier | Topic | Where it showed up |
|---|---|---|
| **Must** | Hash map / set fluency | Jane Street OA ("relies heavily on hash-maps/sets"), Jump (implement a hash map + tradeoffs), HRT, Citadel |
| **Must** | Arrays/strings, two pointers, sliding window, parsing | HRT ("string parsing — spent 60 min on this one"), Citadel, DRW, Squarepoint (two-pointer ~CF1600) |
| **Must** | Stacks/queues incl. monotonic stack; stack-machine style simulations | Jane Street (stack machine, custom stack), HRT (next greater circular, adjacent-pair removal), IMC (stack with increment) |
| **Must** | BFS/DFS on grids and graphs, cycle detection, topological sort, shortest path with constraints | Citadel intern (BFS, topo sort), IMC (all-graph OA), HRT (multi-source BFS, cycle), Optiver principal ("graph/traversal problems… #1 focus"), DE Shaw, Jane Street phone screens |
| **Must** | Heaps / running median / top-k | HRT (two heaps), Citadel (top-k window, running median), SIG |
| **Must** | Binary search (incl. "generalize it") | Jane Street phone, HRT (time queries), Rokos, DE Shaw |
| **Must** | Implement-a-class tasks: LRU cache, order book / matching engine, scheduler, log server, custom vector/shared_ptr | Optiver, IMC, SIG, Graviton, QuantBox, DE Shaw, Jane Street (game engines) |
| **Should** | Easy/medium DP (edit distance, buy/sell stock, subsequence counting, tree DP) | HRT OA, Jump OA, IMC OA, Citadel QR, DE Shaw OA |
| **Should** | Linked-list pointer surgery, BST implementation, tree traversals iterative | HRT, Jump QR, Rokos ("forced to iterative DFS with explicit stack") |
| **Should** | Intervals/sorting, recursion/backtracking/permutations | Jane Street phone, DRW |
| **Nice (OA only)** | Tries, bitmask DP, greedy proofs, Euler paths, CSES-style range queries | Jump (trie), DE Shaw (bitmask), HRT OA, AlphaGrep OA, Indian HFT tests "CF 2000+ DP on graphs" |
| **Skip for interviews** | Segment trees, union-find*, flows, suffix structures, computational geometry | *union-find appeared once, in a DRW OA (pseudoforest check). No live-round report. |

Plus, **for dev roles**, the non-DSA list that is asked as often as algorithms: complexity of STL containers, vector vs list vs deque memory layout, how malloc/new/placement-new work, smart-pointer implementation, move semantics/copy elision, vtables, threads vs processes, mutex vs spinlock, atomics/memory ordering, cache lines/false sharing, TCP vs UDP, endianness.

---

## 6. Common failure modes (as reported, not as imagined)

| Failure mode | Evidence |
|---|---|
| **Over-explaining before coding under a time-boxed, multi-step problem** | Jane Street rejection of an otherwise-successful senior SWE (§3.1). Jane Street questions are "in multiple steps". |
| **Slow execution / fumbling parsing & debugging; not adapting to a twist** | Optiver principal-level recruiter feedback (§3.4); Jane Street intern superday "keeps layering requirements". |
| **Missing edge cases** | Citadel: "missed edge cases like self-loops; rejected". HRT OA candidates wrote 7–10+ edge cases and still failed; HRT interviewer "likely wanted O(1) memory" in-place variant; "attention to detail on boundary cases… final 1xN or Nx1 must be handled carefully." |
| **Not knowing complexity / STL internals when asked** | Optiver MCQs on sorting complexity; Citadel "std C++ structures underneath"; IMC "best and worst case time complexity in each case." |
| **Language fluency gaps** (writing C++ that TLEs, or Python that times out) | HRT "TLE; performance-efficient OO C++ required"; IMC "Python solutions timing out"; DRW rewards C++ on OA. |
| **Freezing / going quiet** | Chinese job-search retrospective; IIT advice "don't start blabbering, take a moment"; HRT explicitly grades "take hints well", "teachability". |
| **Wrong role prep** (grinding LC for a trader loop, or math puzzles for a dev loop) | Jane Street: no math for devs; trading-systems guide: puzzles rare for devs; Berkeley: "a lot of trading interviews won't even test your programming skills." |
| **Resume claims you can't defend** | HRT phone screen "cross-checked the resume closely"; Optiver "Why Optiver" generic answers "sound unprepared". |
| **Not asking clarifying questions on deliberately under-specified prompts** | Jane Street video-player API "prompt is deliberately underspecified"; "clarifying questions expected". |

---

## 7. Time budgets reported

| Who | Budget | Outcome |
|---|---|---|
| IIT-D CS undergrad, placement season (dev track) | Aug–Nov (~4 months) of CP + CS fundamentals + C++, on top of quant prep done the previous year; ~80 quant problems on weekends; 30 min/hard problem rule | Offers incl. QuantBox (dev); interviews at Optiver, Graviton, Quadeye, Tower, DE Shaw |
| IIT-B undergrad (SDE/quant intern) | Reached ~CF 1600; "level asked is much easier than this"; wishes he had taken a probability course first | Quant/SDE internship offers (Optiver/IMC-tier tests) |
| Experienced SWE (ex-big-tech) interviewing at Citadel Sec QR, HRT, Jane Street | Did *not* grind; timeboxed Green Book to one problem per section; relied on existing skill; ~10 h of HRT interviews total | Offers from Citadel Sec and HRT; rejected by Jane Street on time pressure |
| Working professionals (Blind, generic) | "4–5 months at 1–2 h/day" or "1 month at 4–5 h/day"; "8 h/day for a week before the interview"; 200–225 problems | Mixed / unspecified |
| Optiver trader-track intern (Aniruddha Deb) | Multi-year, "unstructured, indisciplined" puzzle/mental-math prep; almost no coding-specific prep reported | Optiver SWE internship offer |
| Synthesized guide (D) | 8 weeks × 14 h/week; 150–250 timed problems | n/a |

**Reading:** for someone with a CS degree and rusty DSA, the first-hand data points cluster at **6–16 weeks, ~150–250 timed problems, plus 10–20 h of C++/OS review for dev roles**. For someone already fluent, days-to-weeks of targeted timed practice and mocks, not months.

---

## 8. Differences by role

- **Quant dev / SWE (HRT, Citadel Sec, Optiver, IMC, DRW, Jump, Indian HFTs):** hardest coding OAs; live rounds split between implementation-heavy DSA and C++/OS/systems depth; the systems half is where new grads are most often under-prepared (HRT phone screen with no coding at all; Citadel obfuscated-C++ debugging; Squarepoint copy/move counting). Probability is light ("medium to high effort from the probability section" on Indian campus tests; "no math" on HRT's algo-engineer phone screens per one Blind report; "math problems" on the onsite per another).
- **Quant trader (Jane Street, Optiver, SIG, IMC, Akuna):** "Programming is not usually tested for Quant Trading roles" (Berkeley); Optiver trader intern loop has zero coding; when coding exists it is a light Python/hash-map screen. Spend the time on mental math (80-in-8, Zetamac 50+), probability, EV/market-making games.
- **Quant researcher (Two Sigma, Citadel, HRT, Jump, Headlands, DE Shaw):** "commonly needed… a combination of online assessments and Leetcode-style interviews" (Berkeley); rounds are typically 1 probability/stats + 1 coding (LeetCode medium, sometimes a DP) + a data/pandas or modelling discussion; reported QR coding questions are *easier* than dev ones (linked-list swap, DP, target-sum). Python + numpy/pandas fluency, statistics-to-code (implement a regression/optimizer), and research narrative matter more than algorithmic depth. A QuantNet hiring-manager quote relayed second-hand (D): "Cannot stress how many 'Math whiz' PhDs with strong PDE skills we have not hired because they don't have a strong SWE background."

---

## 9. Internship / new-grad vs full-time / experienced-hire

**What is tested**

| | Internship / new-grad | Full-time experienced (lateral) |
|---|---|---|
| Gate | Automated OA (Codility/HackerRank/CodeSignal), 3–4 CP-style problems, 60–120 min; campus tests "2 LC hard × 30 min + MCQ". CGPA cutoffs (8–8.5/10 at Indian HFTs). Mental-math/neuro games for trader tracks. | Often *no* OA (Jane Street "does not use a standard OA platform before phone screens for SWEs"; DRW senior "take-home + onsite refinement, no live algo round per recruiter"); when present, smaller (Squarepoint 2 problems; DRW 3 incl. find-the-bug). |
| Live coding | Pure DSA/implementation: BFS, topo sort, class design (Citadel, DE Shaw, IMC, Optiver campus); Jane Street intern superday 3×45 min coding-only. | Same problem *style* but judged more "holistically and stricter"; plus C++/OS depth, debugging of real-ish code (Citadel 2 h obfuscated C++; Squarepoint broken vector), performance optimization of given code, concurrency. Blind (Citadel): "younger → LC medium/hard; older → multithreading/systems." |
| Design | Rare (DE Shaw "banking system class"; QuantBox campus had system-design round). | Standard: Jane Street "system design only for lateral/experienced applicants" + a project-discussion round; HRT "technical design discussions"; Optiver design round; trading-systems guide: expect "5–7 different people" incl. multithreading, lock-free, networking, low-latency, and "3 challenging technical projects and 3 interesting bugs" to discuss. |
| Behavioral | Light; "why firm" and resume walk. | Heavier and *scored*: Optiver principal cut for lacking "architectural ownership" stories; DRW hiring-manager round; Jane Street project discussion. |
| Math | Present for all tracks at campus (probability MCQ/puzzles even for dev). | Dev: rare ("more common for quants"); QR/QT: still central. |

**What prep works for each**

- *Intern/new-grad:* the time-efficient plan is one curated LeetCode list timed to completion → CSES/Codeforces to ~1600 speed for the OAs → 20–30 "implement a class from a spec" drills → a probability primer (Brainstellar / Green Book ch. 4) even for dev tracks → mocks. Budget reported: one placement season (3–4 months) part-time, or 6–8 weeks full-time. Applying to many companies and treating early interviews as mocks was a repeated tactic among offer-holders.
- *Experienced:* grinding is lower-yield; reported successes did *little* problem volume and instead (a) re-sharpened timed implementation on medium problems so that clean code is produced in 20–25 minutes with tests, (b) reviewed the concrete C++/OS/concurrency list in §5, (c) prepared 3 projects and 3 bugs in depth with ownership framing, (d) practiced *not* over-explaining. The one documented experienced failure (Jane Street) was pacing, not knowledge. Expect long loops (6–10 h at HRT) — schedule and sleep matter (Citadel's multi-day onsite was praised for exactly this).
- *PhD → QR:* the corpus repeatedly warns the coding round is where strong mathematicians fail; Grind 75-level fluency plus pandas drills is the cheap fix.

---

## 10. Contradictions and how to read them

1. **"CP is essential" vs "CP is overkill."** Both true, for different rounds: OAs at HRT/DE Shaw/Jump/Indian HFTs are CP-timed; Jane Street/SIG/Optiver/DRW-senior live rounds are not. Prep-company claims that HRT needs "Codeforces 1800+" (D) are stronger than first-hand data (offer-track candidates say the HRT OA was "four easy CP questions"; one frustrated candidate says "Red"). The honest reading: HRT's OA rewards *speed* at medium difficulty.
2. **"Talk through your approach" vs "he failed for talking too much."** Firms grade communication (A), but Jane Street's multi-step, time-boxed format punishes long preambles (C). Plan briefly, narrate while coding.
3. **"Skip easy problems" vs "start with the first 150."** Depends on starting fluency; the offer-holder who regrets easies had CP background.
4. **"Hard DP is the common failure at Citadel/JS finals" (tweet, D)** vs a trading-systems interview guide ("hard DP problems are not common") and the Jane Street reports (implementation-heavy, no algorithm bingo). Weight of evidence: DP appears in OAs (Jump, IMC, DE Shaw, HRT) and in one Citadel QR round; it is not the recurring live-round killer. Graph traversal and implementation speed are.
5. **Prep sites say "solve 100+ problems on arrays/trees/DP/graphs, prioritise medium-hard" (D)**; first-hand accounts say "one curated sheet is more than enough" and "the level asked is much easier than [CF 1600]". Prefer first-hand.
6. **"Projects don't matter for coding rounds" vs "Optiver/IMC ask you to build an order book."** Reconciled in §4.4: practise spec-to-implementation under a clock; don't build a portfolio piece.

---

## 11. Sources

### Official firm guidance (grade A; pages blocked, content via excerpts/mirrors)
- Jane Street — Preparing for a Software Engineering Interview: https://www.janestreet.com/preparing-for-a-software-engineering-interview/
- Jane Street blog — Interviewing at Jane Street: https://blog.janestreet.com/interviewing-at-jane-street/
- Jane Street blog — What a Jane Street software engineering interview is like: https://blog.janestreet.com/what-a-jane-street-dev-interview-is-like/
- Jane Street blog — The Jane Street Interview Process, 2020 edition: https://blog.janestreet.com/jane-street-interview-process-2020/
- Jane Street — SWE mock interview video: https://www.janestreet.com/mock-interview/
- HRT — How to prepare for your SWE interview at HRT: https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/
- HRT — Engineering and interviewing at HRT: https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/
- Citadel Securities — Internship & new-grad engineering interview process: https://www.citadelsecurities.com/careers/career-perspectives/internship-and-new-graduates-engineering-interview-process/
- Two Sigma — Interviewing for Software Engineering: https://www.twosigma.com/careers/interviewing-at-two-sigma/interviewing-for-software-engineering/
- Optiver — Interview tips for software engineers: https://optiver.com/working-at-optiver/career-hub/optiver-interview-tips-for-software-engineers/
- IMC — How to prepare for an interview at IMC: https://www.imc.com/ap/articles/how-to-prepare-for-an-interview-at-imc

### First-hand accounts read in full (grade B/C)
- OneRaynyDay, "Interviewing during COVID" (Citadel Sec QR, HRT algo eng, Jane Street SWE; offers from all but JS): https://github.com/OneRaynyDay/oneraynyday.github.io/blob/master/_posts/2020-09-30-Interviewing-During-Covid.md
- Samarth Goel (Berkeley), "Acing the Quant Interview" (source of blog.samarthgoel.com/quant-interview): https://github.com/sgoel97/blog/blob/main/content/blog/quant-interview/index.md
- Anirudha Kulkarni, IIT Delhi Placements 2024 prep for HFT dev/quant: https://github.com/anirudhakulkarni/Placements-2024
- Aniruddha Deb, quant-prep log (Optiver SWE intern): https://github.com/Aniruddha-Deb/quant-prep
- Shivam5022, Interview Experiences (HRT C++ SWE, Squarepoint, DRW, Graviton, QuantBox): https://github.com/Shivam5022/Interview-Experiences
- devclub-iitd Intern Prep Series 2025 (Citadel, Graviton, Quadeye, DE Shaw, Optiver, Millennium, QRT, AlphaGrep, Jane Street): https://github.com/devclub-iitd/Intern-Prep-Series-25 (e.g. Interviews/Citadel_Pritesh_Mehta.md)
- IIT Delhi CSE "intern ke fundae" student tips (Graviton, Quadeye, NK Securities, DE Shaw, Optiver): https://github.com/ChinmayMittal/IITD-CSE/blob/main/3rd-year/internship-season/tips-and-resources/intern-ke-fundae.md and intern-ke-fundae-24.md
- IIT Bombay PrepForge intern-prep notes: https://github.com/PsychoX21/PrepForge/blob/main/Intern%20Prep.md
- SarthakVerma18 Quant-SDE tips (Optiver, IMC, Graviton, NK): https://github.com/SarthakVerma18/Intern-Guidance/blob/main/QuantSDE_GODtips.md
- avinal, HRT systems-internship interview: https://github.com/avinal/avinal.github.io/blob/main/src/content/posts/blogs/hrt-interview-1.md
- Lazar-Ilic, HRT interview notes: https://github.com/Lazar-Ilic/Lazar/blob/main/Notes/Computer%20Science/Algorithms/Interviews%20Coding%20Rounds/Hudson%20River%20Trading.txt
- ErrolMc, Optiver principal-SWE interview prep with recruiter feedback: https://github.com/ErrolMc/OptiverInterviewPrep
- Leader-board, OA-and-Interviews (Rokos, Tibra first-hand): https://github.com/Leader-board/OA-and-Interviews
- How-to-faang-UTCN guide (Jane Street SWE intern London process): https://github.com/How-to-faang-UTCN/How-to-faang-Guide
- Chinese quant job-search retrospective 2018–19 (mirror): https://github.com/opendoccn0/geekdoc-quant-zh/blob/main/docs/quantml-2019/quantml-2019_194.md
- "Trading Systems Developer Interview Guide (C++ Edition)", Jeff Vogels, 2020 (experienced-hire, mirror): https://github.com/d2p-finance/cfmm-refs/blob/main/text/thunderberg-trading-systems-developer-2026.md

### Compilations that quote blocked forums with URLs (grade B/C by underlying source)
- pushpa-kumar/placement-prep raw notes (Glassdoor, LeetCode Discuss, Blind, WSO, 1point3acres quotes for Jane Street, Jump, HRT, Citadel, DRW, SIG, Optiver, IMC): https://github.com/pushpa-kumar/placement-prep/tree/main/raw-notes
- ankitkushawaha1000/HFT (per-firm process notes citing official pages): https://github.com/ankitkushawaha1000/HFT
- aryehcarmi interview-calibration (paraphrases of JS/HRT/Citadel/Two Sigma/Optiver official pages): https://github.com/aryehcarmi/leetcode-interview-coach/blob/main/skills/leetcode-interview-coach/references/interview-calibration.md

### Forum/community threads seen only as search excerpts (could not open)
- Blind: https://www.teamblind.com/post/jane-street-interview-tips-maxnssgn ; https://www.teamblind.com/post/how-to-prepare-for-jane-street-coding-interview-sf76tspg ; https://www.teamblind.com/post/jane-street-swe-interview-prep-1672gxrc ; https://www.teamblind.com/post/how-to-pass-quant-eng-interview-srmiqs3j ; https://www.teamblind.com/post/hudson-river-trading-hrt-interview-experience-xct5ndnq ; https://www.teamblind.com/post/how-much-time-did-your-allot-to-coding-preparation-before-the-interview-r0isfzzf
- Hacker News: https://news.ycombinator.com/item?id=33208622 (Ask HN: how to get a job at Jane St, Two Sigma) ; https://news.ycombinator.com/item?id=33550840 (JS mock interview) ; https://news.ycombinator.com/item?id=8504950 ; https://news.ycombinator.com/item?id=14734869 ; https://news.ycombinator.com/item?id=43174665
- QuantNet: https://quantnet.com/threads/study-programme-for-quant-researcher-interviews.50152/ ; https://quantnet.com/threads/tips-for-an-entry-level-c-quant-dev-interview.34398/ ; https://quantnet.com/threads/fell-short-in-my-interviews-would-appreciate-some-advice.53724/
- moderndescartes, "Joining Jane Street" (2025 experienced-hire retrospective): https://www.moderndescartes.com/essays/2025_job_search/
- LeetCode Discuss: Two Sigma QR phone screen https://leetcode.com/discuss/interview-question/1675656/two-sigma-quant-research-new-grad-phone-screen-usa/ ; Citadel QR phone https://leetcode.com/discuss/interview-question/427705/citadel-phone-interview-quant-researcher/
- WSO: https://www.wallstreetoasis.com/forum/trading/hudson-river-trading-algorithm-developer-interviewother-questions

### Prep-company / synthesized pages (grade D; used only for contrast)
- techinterview.org HRT guide (claims "Codeforces 1800+ baseline"): https://www.techinterview.org/companies/hudson-river-trading/
- quantt.co.uk, quantprep.io, getcracked.io, tradermath.org, datainterview.com, everythingquant.com, openquant.co, quantblueprint.com (various firm guides; blocked)
- hieptran1812 "Programming for quants: Python, C++ and the DSA bar" (synthesized budgets): https://github.com/hieptran1812/my-website/blob/main/content/blog/trading/quant-careers/programming-for-quants-python-cpp-and-the-dsa-bar.md
- cybergeekgyan/Quant-Developers-Resources (book lists): https://github.com/cybergeekgyan/Quant-Developers-Resources
- QuantBrainteasers awesome-quant-interview-prep (role-split advice; commercial link): https://github.com/QuantBrainteasers/awesome-quant-interview-prep
