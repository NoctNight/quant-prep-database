I have enough evidence to write the report; no further fetches are needed. Below is the consolidated research, with intern vs full-time tagging per firm as requested.

# Coding rounds at quant trading firms (2024–2026): what the evidence says

## 0. How this was researched, and caveats

- ~45 web searches plus ~120 page fetches. The egress proxy blocked most primary hosts (janestreet.com, blog.janestreet.com, hudsonrivertrading.com, optiver.com, citadel.com, deshaw.com, glassdoor, teamblind, reddit, medium, leetcode, 1point3acres, quantnet, jointaro, interviewing.io, HN). For those, I have only the search-engine excerpts of the page text. GitHub (github.com + raw.githubusercontent.com) was fully reachable, so the deepest material comes from (a) first-hand interview write-ups hosted on GitHub (IIT Delhi student repos, personal blogs in repos) and (b) two large sourced compilations that cite Glassdoor/Blind/LeetCode/Taro entries with URLs and label each item REAL vs PRACTICE:
  - `pushpa-kumar/placement-prep/raw-notes/*` (per-firm files, each entry has a source URL)
  - `ankitkushawaha1000/HFT/companies/*` (labels: official / anecdotal / inferred / general-prep; the "inferred" items are the author's guesses and I treat them as non-evidence)
- Marketing/SEO pages (interviewquery, prachub, linkjob, interviewfox, techprep, quantt, techinterview.org, hackerprep, hieptran1812 "playbooks") are used only where they corroborate first-hand reports. One of the compilations explicitly assessed the hieptran1812 series as synthetic content built around fictional candidates ("Maya", "Wei"), so I do not rely on it.
- Tags: [INTERN], [NEW GRAD], [EXPERIENCED], [FT-unspecified]. Dates given where the source states them.

## 1. Official firm guidance pages

| Firm | Page | What it says (from page excerpts) |
|---|---|---|
| Jane Street | https://www.janestreet.com/preparing-for-a-software-engineering-interview/ (also https://www.janestreet.com/mock-interview/, https://blog.janestreet.com/what-a-jane-street-dev-interview-is-like/) | "SWE interviews are about programming, plain and simple" — no mental math or logic puzzles for devs. "We also don't award bonus points for using a functional language like OCaml. Please don't use OCaml just because you think it will make us happy... use the language you're most comfortable with." They don't go out of their way to hire people who already know FP. The mock-interview page notes they used to ask a question called "Memo" but no longer do. |
| HRT | https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/ and https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/ | Interviews are "coding and debugging rounds, technical design discussions, and team fit." HRT "strays away from 'burst of insight' leet-code style questions"; ideal is "a strong programmer from a competitive firm would ace their technical interview with no studying"; they want strong fundamentals but "stay away from obscura and 'tricks'"; systems knowledge (memory, I/O, process management) matters; "expect to program during the interview" at every level. HRT job posts also state "use of AI tools is strictly prohibited... we evaluate the authenticity of candidate responses". |
| Optiver | https://www.optiver.com/join-us/stories/optiver-interview-tips-for-software-engineers/ | "Confident knowledge of a major object-oriented language (C++, Java, or Python) is key"; reflect on motivations; STAR-format stories about projects. |
| Citadel / Citadel Securities | https://www.citadel.com/careers/career-perspectives/our-engineering-interview-process/ | Guide covers both firms at once; candidates report the page instructs them to "share your thought process, discuss trade-offs, be clear about what you know and don't know". |
| D. E. Shaw | https://www.deshaw.com/careers/interviewing | Application review, phone interview, virtual interviews, references, offer. "Slow but very deliberate" batch process. |

## 2. Firm-by-firm findings

### Jane Street
- Format [FT / NEW GRAD]: no standard OA for SWE (one 2021 report of a 1.5-hour HackerRank exists, but 2024 reports go straight to phone screens). 1–2 phone screens (45–60 min, CoderPad), then onsite of 3–4 one-hour coding sessions plus a project-discussion round; most rounds have two interviewers. An April 2024 NYC hire described "2 technical phone screenings (hardest coding in this stage) + 4 onsite rounds = 2 implementation-heavy coding interviews + 2 system-design interviews (one is 'walk through a system you developed')" and said "Jane Street doesn't have behavioral rounds for engineers." A June 2024 reject: questions come "in multiple steps. Make sure you make it to the final step", and Jane Street "values 'complete and correct code' without allowing the interviewee to run their code". A Feb 2024 candidate got "implement Tetris game state and core logic (no UI)" in ~75 min; another got Connect-Four with infinite width (`move()`, `checkWin()`), plus "3 similar questions + project explanation" onsite. Exponent 2024 senior account: "long, collaborative coding interviews where they start with one implementation problem and keep building on it... almost every onsite round had two interviewers". (Sources: Glassdoor via placement-prep compilation; https://www.tryexponent.com/experiences/jane-street-senior-software-engineer-interview-d9cb42)
- Format [INTERN]: LeetCode-discuss intern account: streaming problem — encode "moves" and detect a move once its full input sequence has streamed in, O(n) target (Trie/stream-of-characters style); rejected. Jane Street SWE intern OA at IIT Delhi described as a "software test emphasising readability" separate from the quant test. Differences: intern loop is shorter (phone + fewer onsite rounds), same style of open-ended implementation problems.
- Language: any; OCaml explicitly not required ("OCaml wasn't needed", HK 2021 hire). Python and C++ common.
- Topic mix: implementation-heavy, underspecified simulations/games (Tetris, Connect Four, stack machine, video-player API, custom stack, rate limiter), data-structure design; little classic algorithm trivia; probability appears occasionally ("optimal strategy in coin-flipping game against opponent", HK 2021). No C++-internals or OS questions reported.
- Difficulty / evaluation: time pressure is the differentiator (2020 first-hand: "Jane Street was a bit harder given the time pressure... I probably spent too much time explaining and didn't have enough time to finish the code" — https://github.com/OneRaynyDay/oneraynyday.github.io/blob/HEAD/_posts/2020-09-30-Interviewing-During-Covid.md). Criteria "more wholistic and stricter than other companies"; "strong emphasis on writing clean, understandable code"; "communication and collaborating... solving the problem perfectly doesn't seem to be as important" (Apr 2024). A 2025 HK Data Engineer reject attributed it to Jane Street expecting "completely flawless first-pass execution" after fixing an edge case live.

### Hudson River Trading (HRT)
- OA [FT C++ SWE]: CodeSignal, 90 min, "four easy CP questions" (IIT Delhi full-time C++ SWE, 2024/25 — https://github.com/Shivam5022/Interview-Experiences). Other FT reports: 2h10min / 3 questions (remove C++ comments variant, palindrome permutation, balance a chemical equation — "10+ edge cases... hardest of three"); Blind C++ engineer: "2 hours to solve 4 questions: a warm-up parsing question, implementing a data structure, and algorithm questions with an emphasis on real-world efficiency". Platform varies (CodeSignal/Codility/HackerRank); C++ or Python.
- OA [INTERN, 2023–24]: LeetCode-discuss intern set: add two binary strings; diamond-pattern cipher; min-value queries with row/column removal (two heaps); word-search-in-matrix; time-string binary search. Compilation notes intern OA "easier than full-time track".
- OA [SYSTEMS INTERN 2021]: Codility, 2.5 h, 3 medium questions, C/C++/Python/Go allowed; "correctness and performance are the most important factors" (https://github.com/avinal/avinal.github.io, hrt-interview-1.md).
- Phone screens [FT]: 45 min "in-depth systems interview": C++ `inline` pros/cons, `vector` vs `list` implementation, how `malloc` works and demand paging, kernel memory allocation, `sbrk`/`mmap` (Shivam5022). Blind: round 1 "OS internals and algorithms — expected math but found none"; round 2 live-coding "implement a game with many edge cases". Systems-intern phone (2021): Linux/Unix, C++ pointers/memory, Python/Bash, tools — non-coding.
- Onsite [FT]: 2020 first-hand: "6 hours 30 minutes" onsite plus "2 phone screens", ~10 hours total; systems design, general algorithms, C++-specific questions; got offer. Blind C++ engineer: "a large coding task where you take a spec and implement it, questions on OS/'how computers work', and system design" (declined ~$600k). Reported HRT questions (Glassdoor/Quantt/PracHub/Dataford, FT-unspecified): two threads incrementing a counter 1M times ends < 2M — why/fix; class with `add(x)` and `median()` faster than O(n); real-time risk system with 1 ms budget; design packet routing between hub and node servers; `new` vs `malloc` vs placement new; stack vs heap and stack-growth direction; segfaults/virtual memory; Python dict internals; days-between-dates; `stoi` with overflow; 25 horses/5 lanes.
- Rejection pattern: candidates report rejections after correct-but-slow solutions ("solved it but no test case passed; TLE"; "HRT nails down on your OO C++ performance skills").
- Language: C++ or Python (job titles literally "Software Engineer (C++ or Python)"). Systems/low-level roles are C++.
- Difficulty vs FAANG (Blind thread "How much harder are trading interviews..."): trading firms "have C++, compiler, and OS questions on top of leetcode and system design"; Jump and HRT rated "very strong", Optiver "a bit less tech-focused".

### Citadel / Citadel Securities
- OA [NEW GRAD / INTERN]: HackerRank, most commonly 2 problems in 75 min (some 3 in 90). Early-2024 report: "two coding questions... ninety minutes with large constraints and no partial credit for solutions that time out"; example: max concurrent employees from start/end arrays (https://hiya31.medium.com/...). Other reported OA problems: Roman numerals 1–1000, stable sort words by length, implement a Stack class, sliding window / DP, two graph questions LC med/hard, IPO share allocation by price then timestamp (campus challenge). Proctoring: webcam, second-monitor detection, focus loss can end the test. Reported OA failure rate >85% (prep-site claim, unverified).
- Phone/CoderPad [FT]: "multiple questions on how some of the std C++ lib structures and functions are implemented underneath... specific low-level networking questions" (Blind). Best-time-to-buy/sell then variants (Glassdoor). "Younger [interviewers] love to ask LC medium/hard, older ones love multithreading/system programming" (Blind, 6 YOE).
- Onsite [FT]: Jan 2024 Medium account (https://useinterviewstudy.medium.com/my-software-engineer-interview-experience-at-citadel-january-2024-70d238371b01): in-depth conceptual C++ templates discussion; "mastery of C++... memory management... how code interacts with the OS". Glassdoor/Blind: Round 1 order-book string-parsing DSA; Round 2 "obfuscated C++ code full of loops/complex logic — comprehend and optimize it within ~2 hours" ("Got f***ed... much harder than expected"); Round 3 non-standard system design (low-latency trading system, market-data feed handler, time-series store). Coding: "producer class batching messages, send on max count or hold-time"; currency-exchange best-rate graph (senior SWE rejected for missing self-loop edge case); order book with `get_exchange_bbo` / `get_nbbo`. Reported single-fail policy: weak round cancels remaining rounds (1point3acres).
- [INTERN, Singapore] Medium account exists (https://medium.com/@adityashrivastava2003/...) — page blocked; search excerpt only. [INTERN, IIT Delhi campus 2025] Citadel Software Developer Intern: R1 30 min BFS; R2 45 min implement topological sort; R3 45 min projects/resume — offer (https://github.com/devclub-iitd/Intern-Prep-Series-25/blob/HEAD/Interviews/Citadel_Pritesh_Mehta.md). Intern loops are pure DSA + resume; C++-internals/debugging rounds appear in full-time loops.
- Language: C++ or Python; C++ teams expect concurrency, templates, memory model.

### Jump Trading
- OA [NEW GRAD / INTERN]: HackerRank/Codility, 90–120 min, 2–3 hard problems; Jan 2026 candidate: "hard DP and Graphs", "100 LeetCode problems advisable". 2020 quant-intern OA: 3 questions/105 min (string a's-before-b's validation; tree-heights DP). Codility: max distance between unequal elements; C++ stream/iterator parsing. Reported pass rate 10–15% (prep-site claim).
- Phone/onsite [FT]: Blind: "coding problems around LeetCode Medium/Hard with important C++ concepts... string manipulation, reference counting, I/O, move semantics". 2010-era Glassdoor: "fairly difficult and focused on concurrency, mainly in C/C++", 4-hour onsite. Campus whiteboard (2017): decimal→16-bit binary, then path-finding in 4x4 matrix; "let you use any language".
- [INTERN superday, 2013 — dated]: 4 rounds: pure C++ coding (implement a Trie; swap without temp), whiteboard math/linear algebra, two pen-and-paper probability rounds. Recent intern data is thin; treat Jump intern as OA-hard-DSA + C++ phone.
- Language: C++ expected for engineering; Python roles exist ("Campus Python Software Engineer").
- Topics: memory layout, cache, lock-free, memory model (prep sites; only anecdotally corroborated via "C++ concepts" Blind post).

### Optiver
- OA [NEW GRAD, Chicago 2024]: "OA (2 OOP coding + MCQ on DSA/OS/networking + Zap-N) → recruiter behavioral → technical round → superday"; rejected after final, recruiter cited hiring pause (LeetCode Discuss via compilation). US campus SWE test 2025: 1 coding question, C++/Java/Python, ~75 min. Recurring OA problems (multiple corroborating reports): order-book matching simulation (sum of transaction prices), trading-sequences DP (k→n shares in ≤m transactions, non-negative), dividend-adjusted future pricing, log server (last-hour retention), supermarket checkout simulation, truck-position subscriptions, S-expression tree validation with error codes, LRU cache, Roman-numeral sort. Nov 2025 Taro intern: "OA felt more like an object-oriented software design exercise than a pure algorithms test."
- OA [INTERN, IIT Delhi]: "80 in 8" mental math + reflex games, then C++ coding test with "3 questions based on trading problems... not that difficult... some CP/DSA knowledge required... emphasised OOP concepts"; full completion not needed (https://github.com/ChinmayMittal/IITD-CSE/.../Optiver/swe.md).
- Interviews [INTERN]: HR round; system-design: "design a system enabling a trader in Amsterdam to trade with an exchange in Frankfurt" ("Think loudly!"; bottlenecks → network → co-location); "trading software" pseudocode round.
- Interviews [EXPERIENCED, Principal C# SWE, Sydney, 2026]: coding round ~60 min on Zoom+HackerRank, two engineers observing, graph parse→build→traverse with escalating requirements; feedback quotes: "iteration speed... below expectations", "spent a significant portion resolving basic coding and parsing issues", "limited ability to adapt as requirements became more complex". Design round ~90 min, verbal, no whiteboard ("real-time UI that loads huge amounts of data per second"). Experience-review ~60 min ("would I trust this person to represent my team?"). (https://github.com/ErrolMc/OptiverInterviewPrep)
- Onsite [FT-unspecified, Glassdoor/Blind]: C++ custom vector implementation; CPU cache and TLB; multithreading sync; circular-buffer queue; TCP vs multicast; speed-of-light packet latency Amsterdam→Singapore.
- Language: C++/Java/Python (C# for GUI roles); C++ fluency noted as advantage.
- Difficulty: LC-medium with OOP/design emphasis; Blind consensus "less technically demanding than HRT/Jump".
- Prep artefact: six Optiver-OA-style C++ problems with an AoS→SoA rewrite, from Pavel Guzenfeld's blog (not first-hand interview; modelled on public OA reports).

### IMC
- OA [NEW GRAD / INTERN]: HackerRank, 2 questions, 120 min, hard DP/graph (BFS/DFS); Australia 2024 grad: HackerRank "restricted to Java/C/C++", then Vieple one-way video with technical questions, behavioral phone, then super day (technical + behavioral) (https://github.com/saikumarmk/website, guide-to-tech-3). Plus "Neurolympics" cognitive games and, in some loops, a small home assignment ("Rock-Paper-Scissors... keep it simple and GC efficient").
- Interviews [FT-unspecified, WSO/Blind/Taro]: R1 45 min conceptual: lists/sets/maps, "fastest to slowest: CPU cache, RAM, heap, disk", false sharing, "is multithreading always faster?", smart-pointer internals, vtable memory layout, hotel-booking design. R2 60–90 min: matching engine from skeleton code with unit tests (partial fills, multi-level matching) — "appears in nearly every interview loop" — or hard DP/graph. June 2024 Amsterdam Taro reject (page blocked) and a note that a candidate was rejected "despite passing all tests", implying style/approach is graded.
- Language: Java or C++ track chosen at recruiter screen.
- Difficulty: "LeetCode mediums basically" for coding; systems/C++ conceptual depth is the differentiator.

### SIG (Susquehanna)
- OA [NEW GRAD]: CodeSignal (or HackerRank), 4 questions ~70 min, "first two easy, last two hard" (LeetCode Discuss, May 2026); alternatively a 2-problem set.
- Interviews [FT]: 60–90 min live coding+optimization; some rounds the interviewer leaves for 30 min while you implement on CodeSignal, then walk-through/optimization. Final: OOD round ("program an object from scratch, interviewer asks you to add methods"; "not a traditional system design"; SOLID/extensibility). Blind: phone "all discussion based, resume and tech, no LeetCode"; final "3 hours, 2 LCs"; employee advice: "when and where to use data structures... explain why you chose your approach"; don't switch to C# syntax if you're a Java person.
- [INTERN, Trading Systems Engineer]: OA C++ string/array problems; phone on numpy/pandas joins/aggregates; superday: implement `std::vector` from scratch, a system-design question, a math round (WSO). Intern track = more raw-C++ implementation; FT track = OOD + optimization.
- Language: C++, C#, Java, Python depending on team.

### Two Sigma
- OA [NEW GRAD / FT]: HackerRank 60–75 min, 2 questions LC easy–medium; Nov 2025 NYC candidate: "decode a string encoded using a specific algorithm — not standard LeetCode" (https://www.jointaro.com/interviews/companies/two-sigma/experiences/software-engineer-new-york-new-york-november-7-2025-no-offer-neutral-d1417978/); others: max concurrent clients via join/leave events; balanced bracket splits with wildcards; IPO share allocation; best drainage cut in weighted tree.
- Interviews [FT]: pair-programming round (Python: "implement a binary tree class and debug intentionally incorrect functions"); Nov 2025: "first technical was a LeetCode hard, next two back-to-back also hard... BFS/DFS with math and binary search... 60 min each, pretty intense". Gitbook onsite: RPN calculator with Token/Operand/Operator + factory pattern; remove subtree from parent-index array; two ascending blocking queues, find pairs with difference <1 using threads; "why is this web service slow" design. Technical screens: in-memory limit-order matcher (price-time priority); in-memory relational DB (CREATE/INSERT/SELECT WHERE).
- Language: choice (Python common); C++ for execution/market-data teams.
- Difficulty: DSA rounds "consistently described as hard"; less C++-internals than HFTs; some design.

### D. E. Shaw
- [INTERN, IIT Delhi 2025]: OA 3 DSA problems ~80 min (20/20/40 min splits; DP, greedy, bitmask). R1 30 min: graph (cycle detection) in C++ + project deep-dive on inheritance/smart pointers; R2 20 min: "design a Banking System class in C++" (https://github.com/devclub-iitd/Intern-Prep-Series-25/blob/HEAD/Interviews/DEShaw_Saumitra_Garg.md). GfG intern 2025: OOP (private constructor), strings, SQL, LLD.
- [FT, India MTS Jan 2025 LeetCode; Glassdoor]: OA "4 LeetCode medium-hards"; interviews: 2 LC mediums + DS question; senior round OS + DP + databases; resume grilling. US new-grad data is thin (deshaw.com blocked).
- Language: C++/Java/Python; OOP design in C++ common.

### Tower Research Capital
- [INTERN, IIT Delhi]: HackerRank 1 h, 3 sections: 3 DSA (CF 1600–1800), probability/maths, C++/Python OOP + computer architecture. R1: LC medium/hard + probability puzzles + pandas details. R2 fundamentals: "calculate sum and prefix sum of n elements with p threads"; analyze inefficient C++ for branch prediction; "sort an extremely large array with limited RAM" (https://raw.githubusercontent.com/ChinmayMittal/IITD-CSE/HEAD/3rd-year/internship-season/interview-experiences/Tower%20Research/north-moore.md). Tarang Shah 2025: Tower final day = "systems design, competitive programming, quant puzzles, project discussion".
- [FT, India GfG]: MCQ OA + 4 coding (SQL, find Python bug, parsing, algorithm); interview: TLB and huge pages, RISC vs CISC, shared vs static libraries, syscalls at assembly level, pipelining/branch prediction; probability with cards. Experienced hires report "more basic, tricky coding questions" rather than senior system design; processes differ per pod. Prep pointers cited: Effective Modern C++, C++ Concurrency in Action, Solarflare/onload, DPDK.

### Virtu
- OA: Codility (unprompted, ~2 h for some roles); [INTERN trainee] 75 min all LC-easy; [SWE] 2 HackerRank-style problems/90 min.
- Interviews: [NEW GRAD] "they just ask brainteasers, the coding is trivial"; post-trade onsite "brain teasers 4 hours straight"; C++ core/HFT: 4 back-to-back rounds, "multithreading and concurrency"; thread-safe LRU cache; TCP vs UDP and why market data is UDP; design order routing with partial fills/retries.

### Millennium
- Decentralized: firm-wide platform teams vs pods. HackerRank coding + Caliper personality/cognitive test; technical screen 45–60 min on languages/ETL/SQL; possible take-home; onsite 3–4 h with design. [INTERN QR, Bangalore] test of maths/probability/CP, then ML-projects round, DSA coding round, HR (IIT Delhi). Languages: C++/Python/Java/SQL/kdb.

### Point72 / Cubist
- OA [INTERN]: HackerRank 45 min, 5 questions (2 SQL, 3 Python); quant-analyst variant 180 min (3 Python + 1 SQL). [NEW GRAD superday, Nov 2025 Reddit] "3 interviews: all basic LeetCode medium or below, one focuses on OOP". [FT phone] root-finding without libraries; C++ `shared_ptr`/`weak_ptr`/`unordered_map`; read streaming data from a TCP socket; IPC via shared memory; SQL/Java; a 3-hour timed 3-question project then debrief. Cubist quant dev: real-time ingestion design, C++ concurrency debugging, FIX protocol. Languages: Python/C++/C/Java accepted.

### Qube (QRT)
- [FT] 3 rounds all technical (2 team, 1 manager): LC-style problems in C++, modern C++ (ownership, lifetime, templates, concurrency), OS questions. [INTERN quant dev, IIT Delhi] OA: 2 easy–moderate coding (algorithms/CP) + probability; onsite: discussion round + pseudocode problem-solving round.

### XTX Markets
- OA: 2–3 hard algorithmic problems, 90–120 min, reportedly ~5–10% pass; Aug 2024 candidate got a take-home around crypto operations; Jan 2025 online test first. Then 60-min live coding call, then 5–6 interviews in one London day (45–60 min each). ML-heavy for research; SWE rounds probe deque/list/vector cache behaviour, `shared_ptr` cost, benchmarking to ns, kernel bypass (aggregated, medium confidence). Blind experience thread exists (blocked).

### Five Rings
- 15-min recruiter, 1-hour technical video "implementing data structures", 5-hour virtual onsite: 4 technical DS&A interviews + CTO chat (~2-month process). OA "coding questions in C++... relatively straightforward with some edge cases"; questions on C pointers/dereferencing and string algorithms. 25% positive Glassdoor experience rating.

### Akuna
- OA: HackerRank ~15 MCQ (C++, GC, data structures) + 3 coding, 90 min. Reported OA problems: min swaps to sort descending; count simple s–t paths; weighted interval scheduling (movies); multi-stock max profit with no same-day flips; break-a-palindrome; A→B with -1/×2 ops; refactor a buggy C++ object pool (races, double-free, ABA; RAII handles). Interviews "focus more on understanding of C++ syntax than algorithms" — e.g., implement a string class; "memorize C++ classes and every method". Taro July 2023 C++ SWE reject (blocked).

### DRW
- OA [NEW GRAD / INTERN]: Codility, 3 questions, 150 min, ~72-hour window; "more points if you write at least 1/3 questions in C++"; Java or C++ required. Reported problems: knockout-tournament match counts; robot path with 5 subtasks; max sum of two numbers sharing no digits; bulb toggles; max even sum of K; nested transactions in-memory DB; password validator; year-end balance with monthly fees.
- [FT C++ SWE, off-campus]: OA 3 C++ questions/120 min (one bug-finding, two LC med-hard); 1-h technical: "write pseudocode to serialize a struct in binary and write it to a file" with endianness follow-ups (Shivam5022).
- [EXPERIENCED]: take-home then onsite extending it; recruiter: "no algo live coding round"; "tell me how TCP/IP works" (Blind). Chicago onsite for SWE: 5 rounds (1 coding, 3 technical, 1 HM). Glassdoor: hashmaps, mutexes, virtual memory, function pointers, real-time market-data dissemination design, schema design.

### Flow Traders
- HackerRank ~12 questions (>half programming) with C++11/14 snippets, ~2 h, "most people fail at this stage"; templates/metaprogramming, concurrency design patterns, websockets/socket programming; pair-programming hour with a senior; onsite with tech managers. One take-home: "Risk server — TCP server computing worst hypothetical net position per instrument from a binary order/trade feed" (Graduate C++ program). Trading-systems-engineer track: Linux/scripting screen (50 Q/60 min), speed-math test.

### Headlands, Radix, Old Mission
- Headlands: OA 2 questions, one must be C++, the other C++/Java/Python; Glassdoor 3.39/5 difficulty, 31% positive; described as "academic-driven, very high quality software". Radix: 60–90 min live coding + systems design with a senior engineer/researcher, then 5–7 onsite rounds in Chicago (coding, design, research-style problem, partners) — prep-site description only. Old Mission: no substantive public interview reports found; C++ and Python SWE postings.

## 3. Cross-cutting observations

- Difficulty vs FAANG: consensus on Blind and in first-hand posts is "FAANG algorithms plus C++/OS/networking on top" for HFTs (HRT, Jump, Citadel Securities, Tower, DRW-C++), "FAANG-hard DSA with less trivia" for Two Sigma/Jane Street, and "LC-medium coding but heavy OOP/design and cognitive tests" for Optiver/IMC/SIG. The one person who did Citadel Securities, HRT and Jane Street in the same season (2020) ranked Jane Street hardest on time pressure, Citadel Securities on novel math + "low level C++ stuff", HRT on sheer length (6.5-h onsite) and systems design.
- Code quality / tests / edge cases: repeatedly decisive. HRT and Citadel Securities reject correct-but-slow or edge-case-missing code (TLE; self-loop). Jane Street does not let you run code and expects "complete and correct" multi-step solutions with clean structure. Optiver's written feedback graded iteration speed and adaptability to escalating requirements. IMC rejected a candidate who passed all tests (style/approach).
- Time pressure: OAs are 60–150 min with 2–4 problems; live rounds 45–90 min; HRT onsite up to 6.5 h; Citadel Securities "obfuscated C++" round ~2 h.
- Proctoring / AI: Citadel Securities HackerRank OA monitors webcam/second monitor/focus loss; HRT job posts prohibit AI tools and "evaluate authenticity".
- Order book / matching engine: shows up as a coding problem (Optiver OA, IMC onsite skeleton-with-tests, Two Sigma screen, Citadel Securities NBBO/BBO) far more often than as a whiteboard "system design"; the design version is "make cancel O(1)", "single-threaded vs lock-free", "UDP multicast packet to strategy".
- Language: C++ mandatory only where the role says C++ (HRT C++ track, Jump, Citadel Securities C++ teams, Akuna, Flow Traders, Tower, Headlands one question, DRW bonus). Choice is genuinely free at Jane Street, HRT (C++ or Python), Two Sigma, Point72, Optiver (C++/Java/Python), IMC (Java or C++).

## 4. Intern vs full-time: summary of differences per firm

| Firm | Intern track | Full-time / experienced track |
|---|---|---|
| Jane Street | Phone + shorter onsite; same open-ended implementation style; streaming/encoding problem reported | 2 phone screens + 3–4 coding hours + project/system-design rounds, two interviewers, no behavioral |
| HRT | OA easier (binary strings, cipher, heap queries); systems intern phone is non-coding Linux/C++/Python | OA 3–4 problems in 2 h with edge-case-heavy parsing; 45-min systems phone (malloc/mmap/inline); onsite spec-to-implementation task + OS + design, 4–6.5 h |
| Citadel / CS | Campus: BFS, topological sort, resume (IIT-D); HackerRank 2 Q/75 min | Same OA, plus CoderPad C++-internals/networking, 2-h obfuscated-C++ debugging round, non-standard trading system design; single-fail policy |
| Optiver | 80-in-8 + games + 3 OOP-flavoured C++ trading problems; Amsterdam-to-Frankfurt design chat | New grad: 2 OOP coding + MCQ (DSA/OS/networking) + Zap-N, tech round, superday; experienced: 60-min graph coding under escalation, 90-min verbal design, experience review |
| IMC | HackerRank (Java/C/C++) + one-way video + phone + super day | Adds home assignment and 60–90 min matching-engine-with-tests round; C++ internals questions |
| SIG | C++ string/array OA, pandas phone, implement `std::vector` at superday | CodeSignal 4 Q; 60–90 min coding+optimize; OOD final; senior phone is discussion-based |
| Two Sigma | (not separately reported) | HackerRank 60–75 min; pair-programming debug round; three back-to-back LC-hard hours |
| D. E. Shaw | 3 DSA in 80 min; C++ graph + C++ class design (Banking System) | OA 4 LC med-hard; DSA + OS/DP/DB rounds; resume grilling (India-sourced) |
| Tower | 1-h HackerRank (DSA CF1600–1800 + probability + C++/arch); threads prefix-sum, branch prediction | Pod-specific; architecture trivia (TLB, pipelining), basic tricky coding even for experienced |
| Point72 | 45-min HackerRank 2 SQL + 3 Python | Superday LC-medium + OOP; C++ pointers, TCP sockets, IPC; 3-h timed project |
| DRW | Codility 3 Q/150 min | Off-campus C++: 3 Q/120 min incl. bug-find; serialization/endianness; experienced: take-home, no algo live coding |
| Virtu | Codility 75 min, LC-easy | Brainteaser-heavy; C++ core: 4 rounds on concurrency |
| Jump | OA hard DP/graph; (2013 superday: C++ trie + math + probability) | LC med/hard + C++ semantics (move, refcount, I/O); concurrency |

## 5. Synthesis: what the coding rounds test, by cluster, and what it implies for prep

HFT / market makers, C++-first (HRT, Jump, Citadel Securities, Tower, DRW-C++, Flow Traders, Akuna, Headlands, XTX-systems, Virtu-C++)
- Round 1 is a timed OA that is mostly parsing/simulation/edge-case correctness with strict time limits (HRT), or 2–3 genuinely hard DP/graph problems (Jump, XTX, IMC, Citadel Securities).
- Phone/onsite then pivots to "how the machine works": malloc/mmap/paging, inline, vtables, move semantics, smart-pointer costs, false sharing, atomics, TCP vs UDP/multicast, and implementing primitives from scratch (vector, hash map, SPSC queue, thread-safe LRU, order book). Citadel Securities adds a read-and-optimize-someone-else's-C++ round; HRT adds a long spec-to-code task and system design that adapts to new facts.
- Prep: LC medium–hard with a strong bias to simulation/parsing and complete edge-case handling under a clock; write production-quality C++ without an IDE; be able to implement `vector`, hash map, LRU, SPSC ring buffer, limit order book (O(1) cancel via id→node map, price levels in map/array) and explain complexity, cache behaviour and allocation; know OSTEP-level OS + Linux networking; expect no AI tools and proctoring.

Multi-strategy / systematic funds (Two Sigma, DE Shaw, Millennium, Point72/Cubist, Qube)
- Standard OA (HackerRank/CodeSignal, 60–90 min, LC easy–hard depending on firm); onsite is FAANG-like: several LC-hard DSA hours (Two Sigma), OOP/LLD in C++ (DE Shaw, Point72 "one focuses on OOP"), pair-programming or debug-a-broken-class rounds, pragmatic system design (slow web service, quote ingestion service, in-memory DB). Language usually your choice, with C++ questions only on C++ teams; SQL and Python data questions on data/quant-dev tracks (Point72, Millennium).
- Prep: Grind-75-plus into LC hard graphs/DP/binary search; clean OOP design with tests; SQL/pandas for quant-dev tracks; moderate C++ (smart pointers, containers) rather than lock-free internals.

Jane Street
- No OA, no puzzles for devs, any language, no behavioral round. Every hour is a collaborative, multi-step implementation problem (Tetris, Connect Four, stack machine, streaming decoder, video-player API) that keeps growing, graded on clarity, correctness without running code, and how you communicate with two interviewers. Time pressure is the main failure mode.
- Prep: practice writing complete, readable, well-decomposed code for underspecified simulations in ~45–60 minutes without an executor; talk while typing; ask clarifying questions early; do not learn OCaml for the interview.

Optiver / IMC / SIG (OOP-heavy market makers)
- Coding is LC-medium but framed as trading simulations (order book, checkout lines, dividends), with an OOP/design bias and a separate MCQ/CS-fundamentals or one-way-video component plus cognitive tests. Live rounds escalate requirements and grade iteration speed, data-structure justification and adaptability; a dedicated OOD/design round (SIG) or verbal systems-design chat (Optiver) is standard. C++ internals (vtable, smart pointers, false sharing, cache/TLB) appear conceptually rather than as implementation tasks.
- Prep: fast, clean OOP in C++/Java/Python; order-book and event-simulation drills; explain Big-O and container choice; basic OS/networking concepts; practice the neuro/mental-math components where present.

## 6. Key sources (accessible ones first)

First-hand accounts / primary compilations (GitHub, readable):
- https://github.com/Shivam5022/Interview-Experiences (HRT FT C++, DRW, Squarepoint, Graviton, QuantBox)
- https://github.com/ChinmayMittal/IITD-CSE/tree/HEAD/3rd-year/internship-season/interview-experiences (Optiver SWE intern; Tower Research intern)
- https://github.com/devclub-iitd/Intern-Prep-Series-25/tree/HEAD/Interviews (Citadel, DE Shaw, QRT, Millennium, Optiver, Tower 2025 intern write-ups)
- https://github.com/OneRaynyDay/oneraynyday.github.io/blob/HEAD/_posts/2020-09-30-Interviewing-During-Covid.md (Citadel Securities, HRT, Jane Street, 2020)
- https://github.com/ErrolMc/OptiverInterviewPrep (Optiver principal SWE loop with written feedback, 2026)
- https://github.com/saikumarmk/website/blob/HEAD/urara/guide-to-tech-3/+page.md (IMC 2024 grad loop, Australia)
- https://raw.githubusercontent.com/avinal/avinal.github.io/HEAD/src/content/posts/blogs/hrt-interview-1.md (HRT systems intern 2021)
- https://github.com/pushpa-kumar/placement-prep/tree/HEAD/raw-notes (sourced REAL/PRACTICE question lists per firm with URLs)
- https://github.com/ankitkushawaha1000/HFT/tree/HEAD/companies (labelled aggregation; use "anecdotal" items only)
- https://github.com/PavelGuzenfeld/pavelguzenfeld.github.io/blob/HEAD/content/posts/optiver-cpp-problems-order-books-dijkstra-dp.md
- https://github.com/Unays7/HFT-Interview-Prep (resource list: OSTEP, TCP/IP Illustrated, Effective Modern C++, CppCon low-latency talks)

Official pages (blocked for full read; excerpts via search):
- https://www.janestreet.com/preparing-for-a-software-engineering-interview/ ; https://www.janestreet.com/mock-interview/
- https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/ ; https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/
- https://www.optiver.com/join-us/stories/optiver-interview-tips-for-software-engineers/
- https://www.citadel.com/careers/career-perspectives/our-engineering-interview-process/
- https://www.deshaw.com/careers/interviewing

First-hand posts on blocked hosts (search excerpts only):
- https://useinterviewstudy.medium.com/my-software-engineer-interview-experience-at-citadel-january-2024-70d238371b01
- https://medium.com/@adityashrivastava2003/citadel-securities-swe-intern-singapore-interview-experience-386dc70fc1eb
- https://hiya31.medium.com/what-they-asked-me-in-the-citadel-securities-hackerrank-coding-round-ed3ceded3c04
- https://www.jointaro.com/interviews/companies/two-sigma/experiences/software-engineer-new-york-new-york-november-7-2025-no-offer-neutral-d1417978/
- https://www.jointaro.com/interviews/companies/optiver/experiences/software-engineer-internship-united-states-november-6-2025-no-offer-negative-97414d3e/
- https://www.tryexponent.com/experiences/jane-street-senior-software-engineer-interview-d9cb42
- https://www.teamblind.com/post/How-much-harder-are-trading-interviews-citadel-jump-js-optiver-hrt-ts-etc-on-average-compared-to-Googles-6arKn1xW
- https://www.teamblind.com/post/hudson-river-trading-interview-process-87mxp0h4 ; https://www.teamblind.com/post/jump-trading-interview-swe-ejhoj6l3 ; https://www.teamblind.com/post/xtx-markets-interview-experience-6tizwwo2
- https://leetcode.com/discuss/post/6754544/de-shaw-interview-experience-member-tech-0oa7/
- Glassdoor firm pages (HRT, Citadel Securities, Jane Street, Optiver, IMC, SIG, Five Rings, Akuna, DRW, Flow Traders, Tower, Headlands) as cited inside the placement-prep compilation (many via web.archive.org snapshots).

Limitations: no readable Reddit/Blind/Glassdoor threads directly; Radix, Old Mission and Headlands have almost no public first-hand SWE reports; DE Shaw and Tower evidence is India-campus-heavy; Jump intern evidence is old (2013/2020) apart from a Jan 2026 OA report.