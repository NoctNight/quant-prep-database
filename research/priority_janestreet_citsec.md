# Jane Street & Citadel Securities — Interview Pipeline and Reported Questions (2023–2026)

Compiled 2026-09-01. Priority deep-dive for SWE / Quant Dev, Quant Trader, Quant Researcher; internship/new-grad vs experienced.

## 0. Method, coverage and caveats

- ~55 web searches (budget exhausted at 200/session), ~120 page-fetch attempts, GitHub code/repo search.
- Network egress in this sandbox blocked almost every primary host: janestreet.com, blog.janestreet.com, citadelsecurities.com, glassdoor.com, leetcode.com, teamblind.com, 1point3acres.com, reddit.com, news.ycombinator.com, quantnet.com, wallstreetoasis.com, medium.com, youtube.com, web.archive.org, and all prep-company sites. Only github.com / raw.githubusercontent.com were fully readable.
- Consequently: (a) official Jane Street / Citadel Securities pages are quoted from search-engine summaries of those pages, not full reads; (b) Glassdoor/LeetCode/Blind reports are quoted either from search summaries or from a GitHub repo (`pushpa-kumar/placement-prep`) that transcribed them with archived source URLs; (c) full page reads were achieved for ~20 GitHub-hosted documents (first-hand blog posts, a first-hand Citadel Securities OA question dump, company-wise LeetCode tag CSVs, a university guide to the Jane Street London SWE intern loop).
- Reliability tags used below:
  - **[official]** – the firm's own page/blog/video (via summary).
  - **[first-hand]** – a candidate's own report (Glassdoor/LeetCode/Blind/GitHub blog), with URL.
  - **[first-hand/transcribed]** – a candidate report quoted via a secondary transcription that preserves the original URL and date.
  - **[aggregator]** – PracHub/Dataford/1point3acres pattern summaries (paraphrased, not verbatim).
  - **[prep-company]** – Exponent, InterviewQuery, Quantt, TechInterview, AlgoMonster, etc. Useful for structure, unreliable for "exact" questions.
  - **[synthetic]** – GitHub "question banks" that self-label entries as `[anecdotal]`/`[inferred]` (e.g. `ankitkushawaha1000/HFT`, `kishanBhandary/...`). Included only where labelled; do not treat as real.
- Nothing below is invented; where a claim comes only from a prep company it is marked so.

---

## 1. JANE STREET

### 1.1 Software Engineer (intern / new grad / experienced)

#### Pipeline

| Stage | Intern / new grad | Experienced | Source |
|---|---|---|---|
| Application | Resume read by a person; no automated screen. "Tends to be more school-agnostic than other firms; offers a lot of first-round interviews." | same | [official summary] janestreet.com/join-jane-street/interviewing; [first-hand] quantprep/quantnewgrad2022 README |
| Online assessment | **Not standard.** Official page describes: technical interview over Zoom → final round in office. Isolated reports: a 1.5-hour HackerRank test before a phone interview (US, 2021) and "an OA, then a 1-hour phone screen with one problem, then a final round of three questions" (2025 intern, Taro). Most 2023–2025 reports: no OA, straight to a live 1-hour coding screen. | No OA | [official] janestreet.com/preparing-for-a-software-engineering-interview; [first-hand/transcribed] Glassdoor 2021 (Connect-Four report); [first-hand summary] jointaro.com 2025 intern report |
| Phone / Zoom screen | 1 round, ~45–60 min, one interviewer, shared editor (CoderPad reported 2024; earlier a "Google-Docs-style non-runnable editor" in London). One multi-part problem. Some experienced candidates report 2 phone screens. | 1–2 screens | [official]; [first-hand/transcribed] Glassdoor Feb 2024 NY offer ("One round of remote tech screen with a relatively straightforward (but fun!) coding question on Coderpad"); Glassdoor Apr 2024 NY offer (2 tech phone screens) |
| Final round | In-person (NY/London/HK) or Zoom. Interns (London): 3 × ~45-min coding rounds, two interviewers each, rejection possible mid-day. US reports: 3 × ~1-hour coding rounds + Q&A; "four technical rounds: one virtual, two onsite before lunch, one after lunch". | 3 coding rounds + 1 **project deep-dive** ("walk through a system you developed"), all with 2 interviewers; senior loops add a design-ish discussion | [first-hand] UTCN Jane_Street_Guide (London intern); [first-hand/transcribed] Glassdoor Nov 2021 Poland offer ("Three 1 hr coding interviews + 1 project discussion interview … 2 interviewers in each"); Glassdoor Apr 2024 NY offer ("2 implementation-heavy coding interviews + 2 system-design interviews, one being walk through a system you developed"); [first-hand] kipply blog ("five fantastic interview problems … two people per interview") |
| Turnaround | "Typically a response within 1 or 2 days after each stage; whole process often within 1–2 weeks of invitation" (London intern). 4–6 weeks overall for experienced. | | [first-hand] UTCN guide; [prep-company] InterviewQuery |
| Behavioral | "Jane Street doesn't have behavioral rounds for engineers in general." London 2024 full-day onsite had "some behavioural questions in the afternoon". | | [first-hand/transcribed] Glassdoor Apr 2024, Feb 2024 London |

**Language / OCaml expectation**
- [official] "We expect you to write code in a real programming language in these interviews, not pseudocode. You can use any programming language you'd like, but we strongly recommend you use the one you're most familiar with and that best suits the problem." Most hires come in with no OCaml or FP experience.
- [official] SWE interviews "don't involve mental math, math-olympiad questions, or logic puzzles" (those are trading/research roles).
- [first-hand/transcribed] Glassdoor HK Nov 2021 offer: "The language that the company uses, OCaml, wasn't needed."
- [prep-company, contradicting] AlgoMonster/Exponent claim "2–3 algorithmic problems in OCaml" and "one or two OAs" — this contradicts the official page and every first-hand report; treat as wrong.
- Reports of Python being the most common choice; the London editor is non-runnable, so you cannot rely on running tests.

**Official worked examples (the best guide to the style)**
- [official] Blog "What a Jane Street software engineering interview is like" — the retired phone-screen question **"Memo"**: (1) implement `memoize : (a -> b) -> (a -> b)` with a hash table (expected in the first 15–20 min); (2) memory is unbounded → bound the cache and implement **FIFO eviction in O(1)**; (3) FIFO is a poor policy → switch to **LRU**. Structure: part 1 everyone finishes; part 2 is "identify a problem with your part-1 solution (performance or memory) and fix it". Onsite questions "proceed much the same way as the phone interview".
- [official] Software Engineering Mock Interview video (janestreet.com/mock-interview) — retired question: **unit-conversion graph**: given facts like "1 m = 3.28 ft", answer queries "how many inches in a mile?" by treating conversions as weighted bidirectional edges and traversing the graph; return "not convertible" for disconnected units. (Confirmed by community reimplementation: github.com/Shannon-Barretto/mock_interview.) Advice in the video: talk to the interviewer, they care about code quality, practise with a timer.
- [official] Trading Mock Interview video (YouTube NT_I1MjckaU) — see trading section.

**Concretely reported SWE questions (with source, year, track)**

Arrays / strings / hashing / streams
- "Encoded moves": given a set of encoded moves (sequences of inputs), write `encode(move)` and a function that detects/executes a move once its full input sequence has streamed into memory, target O(n). Candidate used dict keyed by tuples and suffix checks; a commenter noted it is LeetCode "Stream of Characters"/Trie-style. — Intern, phone. [first-hand] leetcode.com/discuss/interview-question/882072 (2020, still cited).
- "Given a list of users and login events (Success/Fail), flag users who failed exactly k times consecutively" (like Max Consecutive Ones). Candidate missed an edge case, fixed it live, still rejected; attributed to JS expecting "flawless first-pass execution". — Data Engineer, HK, Round 1. [first-hand/transcribed] leetcode.com/discuss/post/7701675.
- "Transform string: repeatedly remove adjacent AB/BA or CD/DC pairs until none remain; return final string" (stack, LeetCode-1544 family). — OA, role unknown. [aggregator] fastprep.io/problems/janestreet-transform-string via placement-prep.
- LeetCode company tag (last 6 months, liquidslr CSV): only "Add Two Numbers". All-time tag: Count Common Words With One Occurrence, Walking Robot Simulation, Design a Text Editor (Hard), LRU Cache, Stream of Characters (Hard), Number of Orders in the Backlog, Add Strings, Valid Parentheses, Teemo Attacking, Longest Common Prefix, Two Sum. [aggregator] — note "Add Strings"/bignum-style, "Walking Robot Simulation" and "Text Editor" fit the design/simulation style.

Design / OOP / simulation (the dominant category)
- **Connect Four with infinite width** (pieces enter from the bottom; implement `move(index)` and `checkWin()` detecting runs of the same colour). — Phone screen; Feb 2024 NY (offer) and 2021 (HackerRank + phone, no offer). [first-hand/transcribed] Glassdoor archived 2022-09-02 & 2024-09-10.
- **Tetris**: implement game state and core logic, no UI (~75-min onsite). "Several questions. One involving Tetris. Generally fast paced. Implementation accuracy is important." — US, Feb 2024, no offer. [first-hand/transcribed] Glassdoor 2024 + interviewing.io.
- **Design a video-player API** (deliberately underspecified; ask clarifying questions, then implement). — onsite. [prep-company citing candidates] interviewing.io.
- **Stack machine**: "create a stack machine" in a 1-hour interview; "questions straightforward and interesting; selection is very hard after the interview, big emphasis on small details". — London, Dec 2023, no offer. [first-hand/transcribed] Glassdoor.
- **Custom stack with various operations**; "explain my process of implementing a data structure"; "minimal algorithmic knowledge required". — Poland, Nov 2021 phone. [first-hand/transcribed] Glassdoor.
- "Modified connect-four", "modified trading bot" — game-like/real-world scenarios that "start simple and keep layering requirements". — London SWE intern loop. [first-hand] UTCN guide.
- "Design a game with provided APIs" — 1point3acres SDE report (3 technical + 1 HR). [first-hand summary] 1point3acres thread-547993.
- Trading-domain design prompts reported at onsites: "sort trade executions into a canonical order", "validate order-book data across multiple databases", "design exchange-trading system message flow", "transform a sparse time-code stream into dense rows". [aggregator] PracHub/Dataford.
- Exponent's list (prep-company, unverified): "build a small type-safe parser", "functional cache design", "simulate a distributed messaging system", "implement an interval scheduler", "traverse a graph under constraints", "simulate a state machine".

Probability-to-code / math (rare for SWE, but reported)
- "Optimal solution for flipping-coin games with an opponent" — game-theory/EV problem, "no scratch paper allowed … expected me to show how I interpreted the question and how I will solve the problem". — HK onsite, Oct 2021, no offer. [first-hand/transcribed] Glassdoor.
- HN commenter: "Probability questions usually come in the form of a coding problem, and if you don't know the math to back up your DP algorithm you're going to flub it." [first-hand, older] news.ycombinator.com/item?id=33550840.
- "Estimate odd numbers from 0 to 60" — UK, Jan 2022. [first-hand/transcribed] Glassdoor (unclear intent).

Multi-step / "extend this code"
- "The questions they ask are in multiple steps. Make sure you make it to the final step if you even want a chance to proceed … values 'complete and correct code' without allowing the interviewee to run their code." — US, June 2024, no offer. [first-hand/transcribed] Glassdoor.
- Blind (intern): "Each round consisted of a software question (think Leetcode easy-medium), with multiple steps being added along the way (two-three steps in total)." [first-hand summary] teamblind.com/post/jane-street-swe-intern-interview-jvxfxtxv.
- 1point3acres experienced-hire collection thread (2024–25) exists: "全网最全Jane Street SWE面试资料收集 … 从junior到senior" (thread-1103369) and "JaneStreet三轮电面面经" (thread-985070, three phone rounds, "high original-question repetition rate"). Content not readable here.

Systems / low-level
- Not part of the standard SWE loop. Blind: "Jane Street's onsite interviews are not really system design focused; questions are usually not algorithmically challenging, but they expect patterns that cleanly handle all edge cases and code nearly bug-free from the start." [first-hand summary] teamblind.com/post/jane-street-onsite-interviews-gzraj6hn. Experienced loops include the project deep-dive and a "design a system"–style discussion (Glassdoor Apr 2024).
- "Production Engineer" is a separate track with different (systems/Linux) interviews (Blind threads exist; not covered).

Not attributed to Jane Street in any source found: "queue with two stacks", "bignum arithmetic", "weird base representation", "interval merging". (Company LeetCode tag contains "Add Strings"/"Add Two Numbers", which is the bignum family; no first-hand description found.)

**Difficulty, style, pass/fail signals**
- [official] Language-agnostic; "clean, obviously correct code and clear explanation matter as much as the final result"; interviewers give hints and expect questions.
- [first-hand] kipply: "hands-down the best technical interviews … five problems, not algorithmic or LeetCode-like, very representative of possible work … tested problem solving, thinking about edge cases and implementation … two people per interview." (No offer.)
- [first-hand] OneRaynyDay 2020: failed Jane Street on **time pressure** — "I probably spent too much time explaining and didn't have enough time to finish the code" — interviews "a bit longer than usual", questions "a bit harder".
- [first-hand/transcribed] Glassdoor Apr 2024 offer: "Coding problems seemed more implementation intense … strong emphasis on writing clean, understandable code. Communication and collaborating with the interviewer also appears important, solving the problem perfectly doesn't seem to be as important … criteria they're using to judge you is more holistic and stricter than other companies."
- [first-hand] UTCN guide (London intern): evaluated on "class design, data storage efficiency, code structure, execution speed"; "clean, readable code prioritized over optimization"; "Big-O discussion expected"; "avoid excessive focus on system design or design patterns"; can be rejected mid-superday.
- [first-hand/transcribed] Glassdoor Dec 2023 London: rejection decided on "small details which one does not think about during the interview" — i.e. bugs/edge cases in code that "looked fine".
- HN: "minimum expectation is a mostly complete and actually working implementation; there is a second, more advanced technical interview after lunch."
- Reddit/Blind consensus: no behavioral rounds; no LeetCode copy-paste; "they care a lot about the quality of the code and how it is to work with you".

**Intern vs full-time (SWE)**
- Interns: 1 screen + 3 coding rounds (London: 45 min each; US: ~1 h each), no project deep-dive, no design round. Reported rejection immediately after a weak early onsite round.
- Experienced: 1–2 screens + 3 coding rounds + project deep-dive ("why" questions on every decision) and, for senior, design/walk-through-a-system round. Same question style ("implementation-intense, multi-step").
- Jane Street "tends to run two to three rounds per stage"; most full-time seats come from converting interns (general quant-industry observation, [prep-company/GitHub blog]).

### 1.2 Quantitative Trader (intern / new grad / experienced)

Pipeline [official summary + first-hand]
- Resume read by a person. Phone stage: **2–3 conversational calls** "built around a linked series of betting and strategy games" (dice, cards, coins); one or two traders; "pen and paper allowed, no calculators or computers"; thinking aloud expected; hints/missed edge cases do not prevent advancing.
- Historic HackerRank math test (Fall 2016: 4 questions in 30 min — sum of four random primes; 8-sided-die stopping game with bust threshold; three coins Bayes; two urns of chips) [first-hand] github.com/ptmminh/quanttest. Current reports mostly describe no coding OA for trading; "several online tests for maths and logic" mentioned on Glassdoor QR pages.
- Final round: full day (office or Zoom), technical interviews with traders + HR conversation. Candidates report receiving **100 poker chips** at the start of the day and betting chips on their answers in each interview; "scores carry over so an early collapse follows you" (Tradermath; WSO "Jane Street Final Round – what to expect").
- Official prep material: "Probability & Markets guide" PDF (janestreet.com/static/pdfs/trading-interview.pdf) and the Trading Mock Interview video with Graham and Andrea.

Concretely reported QT questions
- **100-sided die game**: (1) roll once, receive face value in dollars — how much would you pay? (2) roll up to twice, keep the second if unsatisfied — price? (3) unlimited rolls, $1 per extra roll — strategy? Game 2: competing with two other players … [first-hand] Glassdoor QTN_1101123.
- **Four face-down cards**: player can walk away, take a pocket card, or pay $6 to peek at a table card — find the best strategy (2024–26 Glassdoor summary) [first-hand summary].
- "Keep rolling a fair die until you roll 3,4,5 consecutively; probability the number of rolls is odd?" [YouTube "Jane Street quant trading interview question", via GitHub cookbooks] (reliability: prep video).
- Recruiter phone screen: "standard probability, Bayes rule, expected value about dice" [first-hand summary Glassdoor].
- "Frog jumping" recursion/EV problem; market-making on card sums; betting games where "the interviewer changes the rules between rolls to test how you adapt" [Glassdoor/prep summary].
- Puzzled-quant substack "Turning cards" — a medium probability question asked for a Quant Strategist role [first-hand, blog].
- Practice-tier examples (hieptran1812 blog, explicitly illustrative): "make me a market on the digit sum of a random page of a 600-page book"; "die: 6 pays you $5, else you pay $1 — take it and how would you size it?".

Style/pass-fail: "Jane Street places very little emphasis on mental math and more on problem-solving and logical reasoning"; "interviewer may keep changing assumptions mid-problem"; Glassdoor reviewer advice: "Forget the green book — only do dice and card problems and scrape the whole Glassdoor" [first-hand, via Aniruddha-Deb/quant-prep].

Intern vs full-time: identical structure (3 phone games + full day). Full-time/experienced traders get more market-making and "explain your P&L reasoning" content; intern candidates report the chip-betting day. No coding for QT.

### 1.3 Quantitative Researcher (intern / PhD / experienced)

Pipeline [prep-company + Glassdoor summaries; official page blocked]
- Phone screen focused on math/probability (and for some tracks a Python coding component), then 1–2 further technical rounds, then full onsite (3–5 rounds). "Expect 4–8 weeks."
- 1point3acres "Jane Street Research Intern 电面第一轮面经" (quant-443565) exists; content not readable.
- Coding: Python common; "2–3 Python problems of LeetCode-medium difficulty with quantitative flavour: simulations, expected value, combinatorics"; Datainterview claims "2 Python problems, LeetCode-hard" (both prep-company). No take-home reported for QR; a take-home *is* reported for the separate **Trade Desk Operations Engineer (London)** graduate track: take-home test → math interview → coding interview, with a "getting started" Python doc [first-hand] leetcode.com/discuss/post/6340012 (Jan 2025).
- Topics: conditional probability, combinatorics, EV, Bayesian reasoning, time-series/hypothesis testing/experiment design, "the interviewer keeps changing assumptions". Blind "ML researcher intern final round" thread exists (not readable). 1point3acres MLE report: design challenge on image digit recognition.

Reliability: mostly prep-company/aggregator; only the TDOE and 1point3acres items are first-hand.

---

## 2. CITADEL SECURITIES

(Where a source says "Citadel" without "Securities", I note it; the two firms share recruiting infrastructure and the OA/superday shape is the same, but Citadel Securities is more C++/systems/market-making heavy.)

### 2.1 Software Engineer / Quant Developer

#### Pipeline

| Stage | Intern / new grad | Experienced | Source |
|---|---|---|---|
| OA | **HackerRank**, timed. Reported formats: 2 problems / 60 min (2024: "two graph questions, LC medium/hard, sliding window + DP"); 2 problems / 70–75 min (1point3acres 2023 SDE OA: "Sprint" problem + "are two points inside a triangle"); "OA of standard leetcode questions, none harder than medium" (Sep 2024 intern); "two questions: one LC-medium, one LC-easy, quite easy relative to onsite" (Glassdoor SWE); some reports 3 problems / 90 min. Campus 2020–21 OA: IPO share allocation. | Usually **no OA**; recruiter call → CoderPad phone screen(s) | [first-hand summary] Glassdoor New-Grad page; [first-hand summary] 1point3acres thread-955749, -453463, -657266; [first-hand/transcribed] LeetCode 750495; [official summary] citadelsecurities.com engineering-interview-process |
| Phone screen | 1–2 rounds, 45–60 min, **CoderPad**; "45-minute first round covers technical and behavioral: technical interests, past internship, school projects, why Citadel" + one coding problem. Intern 2024 (Singapore): "in-depth questions about C++ templates and advanced C++". | 1–2 rounds; C++ trivia + LC problem; some report "brain teaser round then 1-hour CoderPad with hiring manager". | [official summary] open-opportunities page; [first-hand summary] Medium (adityashrivastava, Jan 2024); Blind MvzsEgz0 |
| Superday | Virtual or in person; **3 × 45 min** (Blind: "cpp grilling on iterators, memory management, STL containers such as std::variant, std::vector") up to 4–6 × 30–45 min; mix of coding, C++/systems, design, behavioral. Glassdoor: onsite Round 1 = DSA built around order-book string parsing; Round 2 = **C++ debugging/optimisation round (~2 h): "given obfuscated C++ code full of loops/complex logic, comprehend and optimize it"** (Blind corroborates: "Got f***ed … nothing like [easy] happened"). | Same; Citadel (hedge-fund side, Jan 2024 Medium post) split the onsite over several days. Interviewer seniority matters: "younger folks love to ask LC medium/hard, older ones love multithreading/system-programming questions" (Blind). | [first-hand summary] Blind adtkpi5w, RLL5gFcL; Glassdoor SWE page; [first-hand] OneRaynyDay 2020 |
| Team matching | After round 2, hiring managers across Citadel and Citadel Securities review feedback; teams that are interested call you for a further interview; multiple teams → recruiter decides fit. Updates "within two weeks". | Same | [official summary] |
| Timeline | ~8 weeks total in one GitHub note; Glassdoor average ~19 days from application for QR. | | |

**"Datacenter / systems / C++ deep-dive" round — does it exist?** Yes, for SWE/QD at Citadel Securities: multiple first-hand reports of (a) a phone screen on "how specific std:: C++ library structures/functions are implemented under the hood, plus low-level networking" (Blind fhilphyk, SWE not hedge-fund side); (b) superday round grilling iterators, memory management, `std::variant`/`std::vector`, C++20/23; (c) a 2-hour "understand and optimise obfuscated C++" round; (d) questions on tcp/udp, heap, queue, thread/process plus a file-parsing coding exercise (Dataford candidate report); (e) Blind (Block employee): "one of the few companies that will ask conceptual knowledge in addition to the usual stuff — C++ trivia + LeetCode + system design in the same loop". Python-track candidates get "memory management, garbage collection, how code interacts with the OS". No separate "datacenter" round is named in any source; systems content is folded into the C++ round and a design round.

**Take-homes:** none reported for SWE/QD/QT/QR at Citadel Securities in 2023–2026 (searched explicitly).

**Concretely reported SWE/QD questions**

OA (HackerRank) — first-hand/transcribed unless noted
- IPO share allocation: bidders as `[id, shares, price, timestamp]`; allocate shares by higher price, ties by earlier timestamp; return IDs receiving zero shares. — Campus SWE OA 2020–21. leetcode.com/discuss/interview-question/750495.
- "Sprint" problem + "determine whether points lie inside a triangle". — 2023 SDE OA. 1point3acres thread-955749 (summary only).
- Print Roman numerals 1–1000; order words in a file by length, stable; implement a Stack class with specific operations. — HackerRank test (Glassdoor QTN_2294098), older.
- fastprep.io Citadel OA bank (aggregator, tagged Citadel; likely shared Citadel/CitSec pipeline): Process Scheduling (count assignments of n processes to n slots with no process in consecutive slots, mod 1e9+7); Price Check (hash map of correct prices, count wrong sales); Palindromic Substrings (LC 647); Social Media Suggestions (recommend non-friend with max mutual friends, tie → lowest index, ≤15 friends/user); Best Sum Downward Tree Path; Math with Lego Blocks (replace zeros in two arrays with positive ints to equalise sums, min equal sum); Get Max Throughput (pipeline of services, scaling cost, maximise bottleneck under budget — binary search); Maximize the Lottery ID (LCS with k edit budget DP); Count Stable Segments (prefix sums + hashing); Find Consistent Logs; Get Distinct Goodness Values (bitmask DP over increasing subsequences); Get Min Operations (binary search + greedy).
- LeetCode "Citadel" company tag, last 30 days (liquidslr, mid-2025): **Time Based Key-Value Store, Design Spreadsheet, Number of Orders in the Backlog**; last 6 months adds Parallel Courses III, Find Median from Data Stream, Word Ladder. All-time top: Sliding Window Maximum, Count Palindromic Subsequences, Palindromic Substrings, Best Time to Buy and Sell Stock, Find Median from Data Stream, Merge Intervals, Number of Orders in the Backlog, LRU Cache, Evaluate Division, Insert Delete GetRandom O(1), LFU Cache, Employee Free Time, Meeting Scheduler, Serialize/Deserialize Binary Tree, Design Circular Queue, Merge k Sorted Lists, Course Schedule II, Design Tic-Tac-Toe, Sudoku Solver, Trie, Meeting Rooms II, Trapping Rain Water. Older krishnadey30 1-year list: Consecutive Numbers Sum, Longest String Chain, Inorder Successor in BST, Different Ways to Add Parentheses, Knight Dialer, Longest Valid Parentheses, Maximal Square. [aggregator]

Phone / CoderPad
- "Simple asset reallocation algorithm" after resume questions (screening). [first-hand summary] Glassdoor New-Grad page.
- Max-profit single buy/sell over a price series, then a variation. [first-hand/transcribed] Glassdoor QTN_2294098; senior SWE screening "find the trade pair that gives maximum profit" leetcode.com/discuss/interview-question/1792523.
- "Given currency pairs and rates, find the best exchange rate from currency1 to currency2" (graph best-path; candidate rejected for missing self-loop edge cases). — Senior SWE, 2024. leetcode.com/discuss/interview-experience/5565531.
- Minimum path sum to target in a binary tree with tie-breaks (fewer nodes, then lexicographic). — New-grad phone screen. [aggregator] fastprep.
- Minimum image-processing cost (interval DP with bulk discount). — phone screen. [aggregator] fastprep.
- 1point3acres pattern summary: phone screens favour "merge-K sorted lists, ring-buffer implementation, stock DP ladder"; onsite is "single-fail" (a weak round cancels the next). [aggregator]
- Blind: "multiple questions on how std:: containers/functions are implemented underneath; specific low-level networking questions" (SWE phone screen). [first-hand summary] teamblind.com/post/citadel-hf-interview-questions-fhilphyk.

Onsite / superday
- **Order book design**: input `(exchange_id, price, quantity, side)`; implement `get_exchange_bbo(exchange_id)` and `get_nbbo()` across exchanges; discussion of heaps vs TreeMap for bid/ask; deep probing of trade-offs; separate in-depth behavioral round. [first-hand] dev.to Citadel SWE experience (2024–25).
- "Standard DSA question built around an order-book string-parsing problem" (onsite R1) then the 2-hour C++ comprehension/optimisation round (R2). [first-hand summary] Glassdoor CitSec SWE page.
- "Write a producer class that batches messages and sends them to a network endpoint once either a max message count or a max hold-time is reached." — SWE onsite NYC. [first-hand/transcribed] leetcode.com/discuss/interview-question/4138096 (Citadel Software Engineer All Rounds).
- Matching engine "similar to LeetCode 1801 Number of Orders in the Backlog, often with twists" — consistent with the tag data. [prep-company + tag]
- Implement an LRU cache with O(1) get/put — widely cited for Citadel; on the tag list; [synthetic] repo marks it `[anecdotal]`.
- Implement a `shared_ptr` class with reference counting. [prep-company] Quantt.
- PracHub Citadel SWE list [aggregator]: single-producer multi-consumer ring buffer; external merge sort with a heap; task queue with insert/delete/execute; **simulate 2048 and pack the board into a uint64**; thread-safe shared counter; top-K in every sliding window; statistics from a frequency array; design a low-latency trading system; design a stock-price time-series store; behavioral "project you're proud of".
- Campus (India OCS, Citadel hedge-fund side, 2024–25): R1 BFS, R2 implement topological sort, R3 projects/resume. [first-hand] devclub-iitd Citadel_Pritesh_Mehta.md.
- OneRaynyDay (2020, offer): "some really interesting math problems not related to finance at all … interviewer was ready with another once I solved one"; "grilled me a lot on low-level C++ stuff". [first-hand]
- C++ topics reported across sources: iterators, memory management, `std::variant`, `std::vector` internals, templates/metaprogramming, move semantics, rule of 0/3/5, smart pointers, vtable layout, false sharing, lock-free SPSC queue, `volatile` vs `std::atomic`, C++20/23 features. [first-hand summaries (Blind/Medium) + prep-company]
- `[synthetic]` banks (ankitkushawaha1000/HFT, kishanBhandary) list: lock-free SPSC queue, VWAP-over-interval data structure, matrix-multiplication optimisation, multicast feed handler with gap recovery, pre-trade risk system — plausible but not verified; use only as practice themes.

**Style / pass-fail**
- Official: "these aren't trick questions; they want to learn your strategy and process"; "talk about the intuition while coding".
- OA is auto-graded on hidden tests; "roughly 70% don't pass" (prep-company); efficiency matters as much as correctness.
- Onsite: correctness under grilling; interviewers escalate with "how would you make this faster / what happens under load"; C++ candidates are expected to know internals of what they list on the résumé.
- Team-matching means a good loop can still end without an offer if no team bites.

**Intern vs full-time (SWE/QD)**
- Intern/new grad: HackerRank OA (2–3 problems, 60–90 min) → 1–2 CoderPad rounds (technical + behavioral in the first) → superday 3–4 rounds → team matching. Python or C++ accepted; C++ trivia appears if C++ is on the résumé.
- Experienced: no OA; recruiter call → 1–2 phone screens (LC + C++ conceptual) → superday 4–6 rounds heavy on C++/systems/design plus behavioral → team matching.

### 2.2 Quantitative Trader

Pipeline [first-hand summaries + aggregator]
- OA ("Trader 101" on HackerRank): **30 minutes, four sections** of statistics/probability (Bayes, dice) [1point3acres citadel-quant-679561]; another report "20 minutes of counting, probability and logic"; Glassdoor: "probability, expected value and statistics questions". (A "50 questions in 12 minutes" mental-math sprint is described by a prep company — unverified for CitSec.)
- Phone round(s): 60 min, 2–3 problems mixing brainteasers/EV/applied trading; resume questions; Glassdoor "5 rounds: OA + 4 virtual rounds".
- **Market-making game**: "post bid-ask prices as prices evolve with several changing parameters"; quote a two-sided market on an uncertain value, interviewer trades against you, update quotes and manage inventory. [first-hand summary] Glassdoor QT pages.
- Superday: probability/statistics/algorithms; statistics such as linear regression and hypothesis testing; Python.

Concrete questions
- "Make me a market on the sum of three dice rolls." — Trading intern. [first-hand summary] Glassdoor CitSec Trading Intern page.
- First-hand HackerRank quiz dump (Armand-Morin/citadel-quizz, QT/QR intern & full-time): "Marty's gold bar — pay Shea X/15 of a bar each day for 15 days with no change available; minimum number of pieces?" (answer 4); "next number in 6, 3, 10, 5, 26, 13, 170, 85, …"; "bag of 8 fair dice and 2 rigged dice showing 4 on all faces; pick one, roll three times — P(all three are 4)"; "Poisson arrivals rate λ=1 observed on [0,T], exactly one arrival — P(it arrived in [0,T/4])" (=1/4); "two officers receive requests as Poisson(u1), Poisson(u2), refer fractions p1, p2 to a supervisor — mean time between referrals" (=1/(u1p1+u2p2)).
- Practice-tier (Quantt): expected flips to get HH; boy-born-on-Tuesday; price a die game with one re-roll; put-call parity.

Intern vs full-time: same shape; full-time adds more market-making depth and Python data questions.

### 2.3 Quantitative Researcher (intern / PhD / experienced)

Pipeline [official summary + first-hand summaries]
- Official page ("Our Quantitative Research Interview Process"): recruiter contact; first round 45 min technical + behavioral (interests, past internship/research, projects, why Citadel Securities); CoderPad link sent beforehand; updates within two weeks; second round onsite with **3–5 × 60-min** interviews; team matching afterwards.
- OA: HackerRank, ~80 minutes for QR (75 for other roles) — mix of coding (LC medium–hard), probability puzzles, and multiple-choice statistics/ML. [first-hand] Armand-Morin/citadel-quizz — 16 questions captured from the HackerRank platform for QT/QR intern/full-time:
  - Coding: "longest subarray with sum ≤ k" (`maxLength(a, k)`); "compute a value per string as product of char ordinals raised to power m, sum, report EVEN/ODD"; "max score after exactly k moves where each move takes arr[i] and discards the left or right partition".
  - Probability: rigged-dice Bayes; Poisson conditional uniform; superposed Poisson referrals.
  - Stats/ML MCQ: which regularizer gives sparse coefficients (L1); which assumption is NOT needed for OLS with homoskedastic errors (uncorrelated regressors); logistic regression on a unit-circle boundary (works if squared features added); VC dimension of unions of intervals/rays; k-medoids vs k-means (robust to outliers); best classifier for very few observations; techniques improving model fitting (scaling, regularization, random hyper-parameter search); factors when imputing nulls.
  - Puzzles: gold-bar pieces; number sequence.
- Phone: probability/EV problem then a coding question (2023); "LeetCode-style algorithm problems along with probability and statistics" (2024); Python or C++.
- Onsite topics (Glassdoor CitSec QR page): "statistics question about evaluating a trading strategy, plus probability questions and a small programming assignment"; "linear algebra and coding"; "explain how to compute the product of two very large matrices efficiently using their structure"; "problems at the intersection of optimization and classical ML"; Bayes applied to practical scenarios; ML design/debugging; 40-minute research deep-dive Q&A; "purely technical, no behavioral" in one Sep 2025 report.
- Rejection reason example (QR, firm not certain to be CitSec): asked "how individual points affect a fitted regression line" (leverage: far-from-mean x and large residuals move the line most). [first-hand] ngocuong0105/dendron-wiki.

Intern (PhD) vs full-time: both run OA → 45-min screen → 3–5-round onsite; PhD interns are asked to present research; full-time adds strategy-evaluation statistics and more production-code expectations.

---

## 3. Category map (what each firm actually asks, by evidence weight)

| Category | Jane Street SWE | Citadel Securities SWE/QD |
|---|---|---|
| Arrays/strings/hashing | Login-streak flagging; encoded-move stream matching; adjacent-pair string reduction; (tag) Add Strings/Add Two Numbers | OA staples: palindromic substrings, price check hashing, stable segments (prefix sums), consecutive-numbers-sum; sliding-window maximum; top-K in windows |
| Recursion/DP | Coin-game optimal play (EV → DP); Walking Robot Simulation (tag) | Buy/sell stock ladder; lottery-ID LCS with budget; image-processing interval DP; process scheduling combinatorics; Knight Dialer; Different Ways to Add Parentheses |
| Graphs/trees | Unit-conversion graph (official mock); "traverse a graph under constraints" (prep) | Currency best-rate graph; friend-recommendation (mutual friends); tree path-sum with tie-breaks; Word Ladder; Course Schedule/Parallel Courses; topological sort; BFS |
| Design/OOP/simulation | **Dominant**: Memo/LRU cache (official), Connect Four (infinite width), Tetris, stack machine, custom stack, video-player API, trading bot, game with given APIs; Text Editor/Spreadsheet (tag) | Order book with BBO/NBBO; matching engine (LC 1801); LRU/LFU; Time-based KV store; Design Spreadsheet; message-batching producer; 2048 + uint64 packing; ring buffer; task queue; IPO allocation |
| Probability-to-code | Occasional at onsite (coin-flip game); more in QR/QT | Math puzzles in SWE loops ("really interesting math problems not related to finance"); QT/QR OA probability |
| Low-level/systems/C++ | Not in standard SWE loop (Production Engineer track only) | **Core**: STL internals, iterators, `std::variant`, move semantics, smart pointers, vtables, templates, C++20/23, obfuscated-C++ optimisation round, tcp/udp, threads vs processes, lock-free queues, networking |
| Math puzzles coded | Rare | Rare for SWE; puzzles appear in QT/QR OA (gold bar, sequences) |
| Data manipulation | "Transform sparse time-code stream into dense rows"; validate order-book data | Frequency-array statistics; file parsing exercise; log consistency |
| Take-home | None for SWE/QT/QR; yes for London TDOE graduate track | None reported |
| Debug/extend this code | Every JS round is "extend your own code" through 2–3 escalating parts | Explicit "comprehend and optimise obfuscated C++" round (~2 h); "how would you make this faster" follow-ups |

## 4. Escalation patterns and what interviewers reward

Jane Street
- One problem per round, 2–3 layered parts; part 2 typically breaks part 1 (memory, performance, new rule). Interviewers hint freely; hints are normal and not fatal.
- Code must be complete and actually work without running it; rejections are traced to "small details", missed edge cases, or not reaching the final part in time. Clean naming/structure and talking through trade-offs ("don't implement something complicated to save small constant factors — say so") are explicitly valued.
- Two interviewers per onsite round; no behavioral rounds; project deep-dive for experienced hires is aggressive on "why".

Citadel Securities
- OA is a pure filter on hidden tests (speed + asymptotics). Phone screen mixes résumé/behavioral with one LC-medium and (for C++ résumés) internals trivia.
- Superday escalates from "solve it" to "make it faster / thread-safe / what happens under load"; senior interviewers pivot to multithreading and systems. A single weak round can end the day. After passing, a team must want you (team matching).

## 5. Source list (with reliability)

Official
- janestreet.com/preparing-for-a-software-engineering-interview/ [official; summary]
- janestreet.com/join-jane-street/interviewing/ [official; summary]
- janestreet.com/mock-interview/ and YouTube "A Jane Street Trading Mock Interview with Graham and Andrea" (NT_I1MjckaU) [official]
- blog.janestreet.com/what-a-jane-street-dev-interview-is-like/ (Memo problem) and /jane-street-interview-process-2020/ [official; summary]
- janestreet.com/static/pdfs/trading-interview.pdf [official]
- citadelsecurities.com/careers/career-perspectives/our-engineering-interview-process/, /our-quantitative-research-interview-process/, /candidate-faqs-quantitative-research/, /careers/open-opportunities/ [official; summary]

First-hand (read in full)
- github.com/Armand-Morin/citadel-quizz (16 CitSec HackerRank QT/QR questions) 
- github.com/How-to-faang-UTCN/How-to-faang-Guide/blob/master/guides/Jane_Street_Guide.md (London SWE intern loop)
- github.com/Shannon-Barretto/mock_interview (JS official mock problem)
- OneRaynyDay "Interviewing During Covid" (2020; JS fail on time pressure, Citadel offer, C++ grilling)
- kipply "job search love letters" (JS: five problems, two interviewers)
- github.com/ptmminh/quanttest (JS 2016 trading HackerRank test)
- devclub-iitd Intern-Prep-Series-25 Citadel_Pritesh_Mehta.md (Citadel campus, India)
- github.com/pushpa-kumar/placement-prep raw-notes (transcriptions of Glassdoor archived 2022-09-02 / 2024-09-10 JS SWE reviews, LeetCode Discuss 882072 / 7701675 / 6340012 / 4138096 / 5565531 / 1792523 / 427705 / 750495, Blind fhilphyk / Wzn5GACj / RLL5gFcL / MvzsEgz0 / adtkpi5w, dev.to order-book post, Glassdoor QTN_2294098) [first-hand/transcribed]

First-hand (summary only, host blocked)
- Glassdoor: JS SWE / SWE-intern / QT / QT-intern / QR pages; CitSec SWE / SWE-New-Grad / SWE-intern / Quant Developer / QT / Quant Trading Intern / QR / QR-intern pages; question pages QTN_1101123, QTN_932448
- LeetCode Discuss: 882072 (JS intern), 7701675, 6340012
- Blind: jane-street-swe-intern-interview-jvxfxtxv, jane-street-onsite-interviews-gzraj6hn, citadel-securities-swe-interview-adtkpi5w, citadel-hf-interview-questions-fhilphyk
- 1point3acres: software-engineer-439874, thread-985070, thread-1103369, software-engineer-547993, quant-443565, thread-1041752 (JS); thread-955749, thread-453463, citadel-quant-679561, thread-1015466, software-engineer-657266 (CitSec)
- Medium: adityashrivastava2003 (CitSec SWE intern Singapore, Jan 2024); useinterviewstudy (Citadel SWE Jan 2024)
- jointaro.com JS SWE-intern Oct 2025 report; puzzledquant.substack.com "Turning cards"
- HN threads 33550840, 13012303, 8504950, 24273357, 18039806

Aggregators / prep companies (structure only)
- liquidslr/leetcode-company-wise-problems (Citadel, Jane Street CSVs, mid-2025); krishnadey30 citadel CSVs (older)
- fastprep.io Citadel/Jane Street OA problem bank (via placement-prep)
- PracHub, Dataford, interviewing.io, Exponent/Aced, InterviewQuery, Quantt, TechInterview, Tradermath, AlgoMonster, QuantVault, Codemia, SpaceComplexity, interviewfox, linkjob (all blocked; summaries only)

Synthetic (labelled, not evidence)
- github.com/ankitkushawaha1000/HFT (entries tagged [anecdotal]/[inferred]); kishanBhandary/Projects-and-Interview-Question experiences.md ("anonymized reports", unverifiable)
