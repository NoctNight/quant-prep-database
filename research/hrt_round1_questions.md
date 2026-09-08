# HRT (Hudson River Trading) — Early-Stage Technical Interview Questions
### Phone screen / first technical round / first CoderPad round
Compiled 2026-09-08. Complementary web+GitHub research pass.

---

## 0. Sandbox access reality (read this before trusting any tier assignment)

The network egress proxy in this session **blocked** direct fetches to: Glassdoor, Reddit, Blind/teamblind, LeetCode, 1point3acres, dev.to, Medium, Quora, Wall Street Oasis, jointaro (Taro), nodeflair, prachub, quantt.co.uk, tradermath.org, techinterview.org, techprep.app, spacecomplexity.ai, hackerprep.io, avinal.github.io, **and hudsonrivertrading.com itself**.

What worked:
- **GitHub** (git clone + `raw.githubusercontent.com` + GitHub code search API) — full access. All GitHub sources below were read in full, locally.
- **WebSearch** — returns search-engine *summaries* of blocked pages. For Glassdoor in particular the *question title is in the URL slug and page title*, so verbatim question text does survive into search results. But I could not read the surrounding candidate narrative, date, or role for most of them.

Consequence: everything sourced only to a search-engine summary of a blocked page is marked **[SNIPPET-ONLY]**. Treat that as "the question text is probably real, the round/role/year attribution is not verified."

---

## Tier definitions used here

| Tier | Meaning |
|---|---|
| **FIRST-HAND** | Traceable to a named/identifiable candidate writing their own account, read in full, with URL. |
| **TRANSCRIBED** | A GitHub repo or aggregator that preserves the original source URL. The question text is second-hand but the pointer to the primary source survives. |
| **PREP/UNSOURCED** | A prep company or content site asserting the question with no candidate attribution. **Prep companies in this niche invent plausible questions. Do not treat these as real.** |

---

# TIER 1 — FIRST-HAND ACCOUNTS (read in full)

## 1.1 Shivam Verma (IIT Delhi), HRT **C++ Software Engineer**, full-time, ~2024–25
**Source:** https://github.com/Shivam5022/Interview-Experiences (file `Readme.md`, read in full)
This is the single best first-hand record of the HRT phone screen found anywhere.

> **Online Assessment:** "A 90-minute online assessment on CodeSignal, consisting of four easy CP questions."
>
> **Phone Screening:** "A 45-minute in-depth systems interview, primarily on OS and C++."
> Questions included:
> - **Use of `inline` functions in C++: pros and cons**
> - **`vector` vs `list`: trade-offs and internal details**
> - **Internal working of `malloc`, demand paging, etc.**
> - **How the kernel allocates memory to user processes**
> - **System calls like `sbrk` and `mmap`**

Notes:
- **No live coding at all in this round.** It was pure verbal systems/C++ Q&A for 45 minutes.
- Author's own prep notes: https://github.com/Shivam5022/Knowledgebase-SV
- This candidate's *other* firms' rounds (Squarepoint, DRW, Graviton, QuantBox) are in the same file and are useful as a difficulty calibration, but are **not HRT** — do not blend them.

## 1.2 Avinal Kumar, HRT **Systems Internship (Summer 2021)**, applied Dec 2020, written Jan 2021
**Source (blog blocked; read via GitHub source):**
- Post: https://avinal.github.io/posts/hrt-interview-1
- Markdown read locally from https://github.com/avinal/avinal.github.io — `src/content/posts/blogs/hrt-interview-1.md`

Round 1 (OA): **Codility, 2.5 hrs, 3 questions.** Choice of **C/C++, Python or Golang (no Java)**. Online references (documentation, man pages) explicitly allowed; copying code explicitly penalised. HRT's instructions quoted verbatim by the candidate:
> "While correctness and performance are the most important factors for evaluation, we will take test duration into account as well."
> "Please understand that this test is meant to be challenging. A perfect score is not necessary to move on to future interview rounds, so do the best you can!"

Round 2 (phone screen) — HRT's own invitation email, quoted verbatim:
> "This interview will last about **45 minutes and will be technical but will not require coding**. Interview topics may include your background, programming languages, and Unix/Linux concepts."

What was actually asked (candidate's description; he did not list verbatim prompts):
- Linux/Unix concepts
- **C++ — "mainly pointers and memory"**
- Python/Bash scripting, automation
- Knowledge of tools (IDEs, editors, sysadmin tooling)
- Previous experience, walked **directly off the resume** — "for the most part he did not ask anything that was not on my resume"
- Standard motivation questions: "why do you want to work for this role?", "what makes you fit for this role?"

Behavioural detail worth keeping: **the interviewer explained *why* he was asking each question**, and **gave short verbal feedback on performance at the end of the call**. Turnaround from OA to result was ~2 weeks.

## 1.3 "OneRaynyDay" (Ray Zhang), HRT **Algorithm Engineer**, 2020 cycle — **offer accepted**
**Source:** https://github.com/OneRaynyDay/oneraynyday.github.io — `_posts/2020-09-30-Interviewing-During-Covid.md` (read in full)

Signed an NDA, so deliberately gave no question text. But the **structure and the difficulty ranking are first-hand and specific**:
- Pipeline: **"a coding challenge and 2 phone screens before I moved to on-site"**. Onsite was ~6h30m; total ~10 hours of interviewing.
- **"Math questions — Citadel… HRT also asked some."** → confirms maths/probability appears at HRT for the algo track.
- **"Language specific questions — Citadel/HRT. Grilled me a lot on low level C++ stuff."**
- **"Systems design — HRT"** listed as one of the hardest components.
- **"General algorithm questions — Jane Street/HRT"** — notes "the flavor of algorithm questions are also different between these firms."
- Preparation that worked for him: **~50 LeetCode *hard* problems** at a 40-minute budget, written in both Python and C++17; Codejam rounds 1–2; Codeforces Div 2/Div 3. Explicitly: "Don't bother with medium or easy questions."
- On CoderPad specifically: he deliberately wrote **C++17, not C++20**, because "the online coding platforms (like coderpad) likely use stable distributions of GCC and clang" — a practical tip for the shared-editor round.
- Green book (Xinfeng Zhou, *A Practical Guide to Quantitative Finance Interviews*) used for the maths, one problem per section.
- **"I have not seen an interview question this cycle that was an exact question I've seen online or in books."**

## 1.4 HRT's own published exercise — `wwhrt-bookbuilder-workshop`
**Source:** https://github.com/hudson-trading/wwhrt-bookbuilder-workshop (cloned and read in full)

This is not an interview question, but it is **HRT's own artefact showing the shape of work they test**, and it is the closest thing to an official "here is the kind of problem we care about."

- Framing: *"This workshop will give you a taste of what it's like to work as a Core Developer at HRT."*
- Task: you are given `BookBuilder.cc` containing **"a very naive bookbuilder structure"** and you **optimise** it. It maintains order-book state processing **add / delete / modify** events for individual orders, delivered **via callbacks**, and must answer **queries about the current best orders to buy and sell**.
- Data is real crypto-exchange event data; three event types (add / delete / update-while-resting), defined in `Events.h`.
- The Makefile targets tell you exactly what HRT thinks the loop is: `make measure` (wall-clock to process the data), `make check` (correctness after **every** event), `make profile_functions`, `make profile_lines`, `make gdb_unoptimized` / `make gdb_optimized` (note: *"in case your bug depends on optimizations being enabled"*), and `make gdb SEQNUM=10` to break at a specific event sequence number.
- Requires **C++17**, x86_64 Linux, gdb + libunwind.

**Read-across:** the escalation pattern in HRT's own material is *correctness first (`check`), then measured latency (`measure`), then profile-guided optimisation (`profile_lines`)*, plus debugging under optimisation. That is the same ladder candidates report in live rounds.

## 1.5 Lazar Ilic — verbatim Glassdoor dump + candidate's own annotations
**Source:** https://github.com/Lazar-Ilic/Lazar — `Notes/Computer Science/Algorithms/Interviews Coding Rounds/Hudson River Trading.txt` (34 KB, read in full)

**Important sourcing caveat, stated by the author himself:** he labels the block *"Some GlassDoor Maybe Low Quality Copy Pasta From Like 12 Months Back"* and says it is from **"their August 2022 recruiting cycle … which are in fact live in public on GlassDoor."** So: this file is a **TRANSCRIPTION of Glassdoor items** (~60 of them), not Lazar's own rounds — except where he annotates. Treat the *questions* as Glassdoor-tier, and treat the file as the most complete surviving Glassdoor dump reachable from this sandbox. Full contents in §2.1 below.

---

# TIER 2 — TRANSCRIBED (source URL preserved)

## 2.1 The Lazar-Ilic Glassdoor dump — verbatim question text

These are quoted **exactly as they appear in the file**. Round attribution is mostly absent in the original Glassdoor entries; I have grouped them by category and flagged which ones are explicitly tagged to a phone round.

### 2.1a — OS / memory / kernel (explicitly a phone-screen cluster in several accounts)
> - **"Physical memory vs virtual memory. You have 4GB physical, but you allocate an 8Gb buffer. Is this possible? If so, how? How is the memory actually read as we traverse the memory?"**
> - **"Thread vs process, what's the difference? Talk about some common threading models."**
> - **"What are some methods of inter-process communication. Between threads. Between processes."**
> - **"Explain how a named pipe works (FIFO)."**
> - **"How does computer memory work?"**
> - **"How does OS allocate memory to each process?"**
> - **"Virtual mem vs physical mem?"**
> - **"What happens when virtual mem exceeds physical mem?"**
> - **"Stack vs heap. What stores in which?"**
> - **"How do you support multi-threading without kernel?"** (user-level vs kernel-level threads)
> - **"How can you run multiple processes on 1 computer?"**
> - **"Deep systems questions about memory management."**
> - **"Questions about memory, stack/heap, operating systems basics, networks (TCP/UDP)."**
> - **"2nd round was a technical interview asking me about various C++ and kernel concepts."**

**Corroboration:** the 8GB-on-4GB question also survives as a standalone Glassdoor question title: *"A bunch of C programming. How do you malloc 8GB on a machine with 4GB of memory? Why are you interested in HRT? (My answer to which was apparently not satisfactory for my interviewer)"* — https://www.glassdoor.com/Interview/A-bunch-of-C-programming-How-do-you-malloc-8GB-on-a-machine-with-4GB-of-memory-Why-are-you-interested-in-HRT-My-answer-QTN_2889562.htm [SNIPPET-ONLY]

### 2.1b — C++ conceptual, rapid-fire
> - **"What does the `inline` keyword do in C++? What are the pros and cons?"**
> - **"How do virtual functions work in C++? Explain how vtable lookup works."**
> - **"Map vs unordered_map in C++, how is each one implemented under the hood. What data structure is used."**
> - **"What Is The Difference Between A Map And An Unordered_Map In C++"**
> - **"Which is better and why: list vs vector vs array — what's your answer for that?"**
> - **"Some basic networks question such as difference between TCP and UDP. Some concept questions about data structures such as which is better list vs vectors vs array and why."**
> - **"Some in depth questions about polymorphism in C++."**
> - **"Are run time exceptions in C++ things you deal with through try/catch blocks? I would expect exceptions on out of bounds errors on vectors but NOT on arrays…"**
> - **"Phone interview deep C++ questions, including implementation details of STL and memory allocation for the run time. Also ask C++ code run time exceptions. No algo questions during phone interview, only C++ questions."** ← **explicitly tagged as the phone interview, and explicitly "no algo questions"**
> - **"Explain STL implementations and malloc."**
> - **"Quite a lot basic computer architecture knowledge… Like C thread versus process, DNS, smart pointer. Quite a lot of basic compiler information as well."**

### 2.1c — Hash tables (a coherent rapid-fire ladder, appears together)
> - **"How does hashtable works?"**
> - **"What happens in a lookup/insert operation when hashes of 2 different keys are the same?"**
> - **"What's the time complexity of hashtable ops (lookup/delete/insert)?"**
> - **"When does hashtable upsize/downsize? Runtime complexity?"**

This four-step escalation is the clearest documented *rapid-fire ladder* in the corpus.

### 2.1d — Python-specific (distinct from the C++ track)
> - **"How does Global Interpreter Lock work? What's the advantage versus disadvantage of Global Interpreter Lock?"**
> - **"How dictionary map works under the hood in Python."**
> - **"What's the purpose of 'yield' keyword?"**
> - **"Python decorators"**
> - **"Sql question has to deal with join concept and I used cte too. Python is about dataframe and need to join as well"**
> - **"Pandas Question"**

### 2.1e — Linux / SRE / systems-admin flavour
> - **"What do you know about Inode?"**
> - **"What is the difference between RAID 5 and RAID 6?"**
> - **"Any alternative to ls command?"**
> - **"Why du and df might have discrepancies?"**
> - **"What does the following command do? `mv *`"**
> - **"How to install Linux on 100 compute node easily?"**
> - **"What is the difference between soft and hard link?"**

### 2.1f — Live coding prompts (short, sharp; consistent with a 45–60 min screen)
> - **"Given an array of integers, find two numbers such that they add up to a specific target number. Follow up: what if it is the data type is double instead of int."** ← **this is the exact "what changes with doubles" escalation the brief asks about, and it is documented verbatim.**
> - **"Find 2 Numbers In An Array Summing To A Target"** … *"For the problem with finding two numbers in an array that add up to a target… How would you solve variation where you need to find two numbers whose sum is as close to the target as possible?"* ← **second documented escalation on the same base problem.**
> - **"Implement String To Integer In C++"** — with the interviewer's follow-up preserved: *"stoi implementation may sound trivial but is not when you take into account all corner cases. **What would you do if the input was 1234567890 and you had 16-bit integers to work with?**"* ← **third documented escalation.**
> - **"Using C to implement stoi."**
> - **"Given a string containing only the characters 'A' 'B' 'C' 'D', return the string when all adjacent "AB" / "BA" and "CD" / "DC" pairs have been removed."**
> - **"Given a graph (represented as an array) where nodes have value either 'A' or 'B', find the longest path where no two adjacent nodes have the same value."**
> - **"Find the smallest positive integer that does not occur in a given sequence. A=[1,3,4,5] return 2"**
> - **"Write an algorithm that returns if a string can be partitioned into k sized intervals with each k containing a specific amount of 1s [the string is binary]."**
> - **"Count Days Between 2 Dates Given"**
> - **"Write A Program That Can Add 2 Binary Strings"**
> - **"Complete The Calculator Class"**
> - **"Heap Sort: Almost Sorted Array"**
> - **"Determine How Many Squares And Rectangles Can Be Formed Given A Bunch Of Points"**
> - **"Given An Array, Determine If Each Number Can Be Written As A Sum Of 2 Fibonacci Numbers"**
> - **"Sum Of All 2 Digit Numbers Without 7 And 8"**
> - **"Basic algorithms question on deletion in an array."**
> - **"Questions related to the data structures binary trees, hash maps, and linked lists."**
> - **"Programming Question In C++ Based Around Stacks"**
> - **"Elite Code: Remove Comments, Number Of Atoms"** (i.e. LeetCode "Remove Comments" and "Number of Atoms")
> - **"What Is The Minimum Number Of Comparisons Needed To Find The 2nd Largest Element In A List?"**
> - **"Troll question: given a string which may or may not contain newline characters, print a substring in a very specific format with many edge cases."**
> - **"Normal questions: count frequencies of things that can have equivalent representations, recursively calculate score for a string."**
> - AlgoDaily-associated set the file reproduces: Detect A Cycle In An Undirected Graph; Shortest Path Distance In Matrix; Maximum Per Level; Swap Every Two Nodes In A Linked List; Implement A Binary Search Tree; Traverse A Matrix In Spiral Order; Levenshtein Edit Distance; Next Greater Element In A Circular Array. **⚠ These specific eight come from AlgoDaily's company page, which is a prep site with no attribution — see §3.**

### 2.1g — Probability / maths at the early stage (Algo Developer track)
> - **"Tech interview on math 45 minutes, probability question, Bayes Theorem, random variable distributions, normal distribution"** ← explicitly a 45-minute *maths* phone round.
> - **"Phone interview research + math; then 4 rounds of onsite interview: One round coding, one round data science [use pandas, prediction tasks], one round open-ended questions, one round behavioral. Signed non disclosure for the onsite part."**
> - **"3x3 Colored Cube [surface Red], P[5 White 1 Red]?"** (painted-cube probability)
> - **"Toss A Dice 100 Times And A Coin 400 Times, Compute P[Dice Sum > Coin Heads]"**
> - **"Given a race track with 5 lanes, 25 bunnies, and no timer, how many races are required to find the top 3 fastest bunnies?"** (25 horses / 5 tracks; answer 7)
> - **"Pearson coefficient definition and application"**
> - **"Optimisation problem, Statistics problem, Dynamic Programming problem."**
> - **"Brain Teasers And Statistics And Probability"**

### 2.1h — Interview-format statements from candidates (Lazar file)
> - **"The interview was 30 minutes. He asked me some questions about operating systems and object oriented programming and operating systems and some basic questions in algorithms and data structures. It was audio call."**
> - **"He asked me System architecture and Operating Systems questions."**
> - **"LeetCode questions were easy [similar to Quantitative Researcher/FAANG interviews]. Systems questions required deep knowledge on Operating Systems, memory, networking, etc."**
> - **"First round was a week long order router implementation. Then second round was an interview for checking concepts with respect to Linux, networking, and C++."**
> - **"4 Easy/Medium In 70 Minutes"** / **"4 Questions 90 Minutes"** / **"1 Hour to complete 4 coding questions: 1 Elite Code Easy and 3 Elite Code Mediums [or 2 Elite Code Mediums and a Hard]"** — OA formats.
> - **"Describe a recent interesting bug that you have resolved."** ← the closest thing to a *debugging* question at the early stage in this corpus.
> - Behavioural, recurring: **"Why Hudson River Trading?" / "Why are you interested in HRT?"** (appears 3× independently), **"Tell me about a time you had to work with someone different from you"**, **"Tell me about a time you made a mistake"**, **"Tell me about a time that you succeeded"**, **"Why did you choose your major?"**, **"Elaborate on x part of your resume"**, **"What kind of work environment you enjoy the most?"**

## 2.2 pushpa-kumar/placement-prep — aggregator that preserves source URLs
**Source:** https://github.com/pushpa-kumar/placement-prep (cloned; `raw-notes/company-hrt-citadel.md` 55 KB read in full, plus `generator/final_entries.json`, 239 HRT entries). Compiled 2026-08-27. Each entry carries `Status: REAL|PRACTICE` and a source URL.

**⚠ Critical caveat this repo's own compiler flagged and I am repeating:** a large block of its "REAL" HRT entries are sourced to **PracHub** (`prachub.com`), which is an aggregator that *claims* candidate sourcing but which the compiler noted as *"site claims sourced from real candidate interviews; unverifiable independently in this research pass."* **I have demoted every PracHub-only item to Tier 3 (§3.2).** What follows in this section is only what has a primary-source URL.

### 2.2a — Explicitly tagged as HRT **phone screen** (Blind, Algo/Web Engineer)
Source: https://www.teamblind.com/post/hudson-river-trading-oa-svkrykwf
- **Phone screen round 1:** *"First round covered OS internals and algorithms."* The OP had expected maths; a respondent said **"there was no math."**
- **Phone screen round 2:** *"Implement a game with many edge cases"* (live coding). Candidate's own summary of the difficulty: *"a lot of edge cases."*
- Same thread, the OA that preceded it (3 questions): a *"trivial"* pure-implementation question; a *recursive divide-and-conquer* problem; and *"a very annoying string parsing question"* that tests whether you enumerate edge cases.

### 2.2b — Glassdoor question titles with URLs (HRT-attributed)
- **"c++ questions, related to memory management and stl implementation"** — Software Engineer — https://www.glassdoor.com/Interview/c-questions-related-to-memory-management-and-stl-implementation-QTN_4298492.htm
- **"algorithms & data structures, OS and C++"** — https://www.glassdoor.com/Interview/algorithms-and-data-structures-OS-and-C-QTN_4142543.htm [SNIPPET-ONLY]
- **"C++ vector, constructor, push_back, copy constructor, vector dynamic growth, linux - malloc how it works, virtual memory etc"** — Senior Software Engineer — https://www.glassdoor.com/Interview/C-vector-constructor-push-back-copy-constructor-vector-dynamic-growth-linux-malloc-how-it-works-virtual-memory-et-QTN_2640754.htm [SNIPPET-ONLY] — **this is the single most complete verbatim rapid-fire C++ list found.**
- **"A short programming challenge with C++ questions."** — https://www.glassdoor.com/Interview/-A-short-programming-challenge-with-C-questions-QTN_3809393.htm [SNIPPET-ONLY]
- **"We draw a person at random from the street. Then we keep drawing people until we find someone taller than the first person. What is the expected number of draws we have to wait?"** — https://www.glassdoor.com/Interview/Hudson-River-Trading-Interview-Questions-E470937.htm (aggregate page; the aggregator marks stage as *"likely phone screen, probability"* — that stage tag is an inference, not a report). *Note the answer is the classic record-value result: the expectation is infinite.*
- **"How would you design a system to route network packets between one hub and multiple node servers?"** — Software Engineer — https://www.glassdoor.com/Interview/How-would-you-design-a-system-to-route-network-packets-between-one-hub-and-multiple-node-servers-QTN_8479239.htm — **onsite system-design round, not the phone screen.** Corroborated first-hand on Taro: https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-united-states-april-1-2025-no-offer-negative-2a2ca5aa/ — that candidate reported *interviewers were rigid about matching an answer key even when correct answers (incl. modern C++20 approaches) were given*; **no offer, negative rating**.

### 2.2c — Blind, HRT Core Developer / Low-Level C++
Source: https://www.teamblind.com/post/hudson-river-trading-core-developerlow-level-c-interview-yuqksebo
> - **"Lots of questions on STL containers, how it is implemented, pros and cons, stuff like that"**
> - **"general c++ stuff, like inline functions pros and cons etc"**
>
> A commenter added: *"any low level programmer is expected to write vectorized code"* (SIMD), and recommended studying **virtual memory/paging and multithreading** alongside STL internals.

### 2.2d — Blind, C++ Engineer, coding round formats
Source: https://www.teamblind.com/post/87MxP0h4
- *"2-hour coding session with 4 questions progressing from a warm-up parsing problem to full algorithm/data-structure challenges"* — **emphasis on real-world efficiency over theoretical complexity.**
- Onsite: *optimise/improve a backtracking problem*; a spec-driven system design where **new facts are injected mid-round and you must fold them into the design**. That candidate got an offer (~$600k TC after negotiation) and declined.

### 2.2e — OA questions with LeetCode Discuss URLs (context only — the brief excludes the OA, but these calibrate the phone screen, which candidates repeatedly describe as "similar in flavour to the OA")
- Two rooks on a valued chessboard, non-attacking, maximise sum — https://leetcode.com/discuss/interview-question/889638/hudson-river-trading-oa-two-rooks
- Two "roosters" on an m×n matrix, maximise sum of cells *excluding* their rows/cols — https://leetcode.com/discuss/general-discussion/498475/hudson-river-trading-oa
- Longest unique path in a binary tree; an "easy" stack-implementation question; a string fill-in-the-blank — https://leetcode.com/discuss/general-discussion/549526/hudson-river-trading-online-assessment/
- Grid of houses, count empty cells within Manhattan distance K of **all** houses — https://leetcode.com/discuss/interview-question/1458197/Difficult-Hudson-River-Trading-question-OA
- Eulerian-path feasibility from odd-degree vertex counts — https://leetcode.com/discuss/interview-question/2492212/Hudson-River-Trading
- 2023 SWE Intern: add two binary strings; diamond-pattern matrix cipher; min-value queries on a matrix with row/col removal — https://leetcode.com/discuss/interview-question/3078249/Hudson-River-Trading-2023-SWE-Intern-Test
- 2024 Intern: O(n) running-counter counting problem; word-search-in-grid; time-string→minutes with binary search over sorted times — https://leetcode.com/discuss/interview-question/4452641/hudson-river-trading-intern-2024/
- Variant of "remove comments from C++ source"; permutation-of-palindrome; balanced chemical equation — https://www.teamblind.com/post/hudson-river-trading-oa-what-to-expect-wy1hgi2m

## 2.3 ankitkushawaha1000/HFT — `round-02-technical-phone-screens/questions.md`
**Source:** https://github.com/ankitkushawaha1000/HFT — read in full.
**This repo self-labels every question `[anecdotal]` or `[inferred]`.** Its cited sources are HRT's two hrtbeat posts plus "Glassdoor (anecdotal), LeetCode Discuss (anecdotal), Blind (anecdotal)" with **no per-question URL**. → **Demoted to Tier 3, §3.3.** Its only load-bearing content is the format claim: *"Usually 1–2 live technical screens of 45–60 minutes each."*

---

# TIER 3 — PREP-SITE / UNSOURCED (do not treat as real)

## 3.1 The structural claims prep sites agree on (probably right, but nobody is citing a candidate)
Repeated across quantt.co.uk, tradermath.org, spacecomplexity.ai, techprep.app, techinterview.org, myntbit, hacktherounds, ghostinterview, dataford, hackerprep (all **blocked**; read via search summaries):
- Phone screen is **45–60 minutes**, **CoderPad** or similar, **1–2 rounds**.
- For the algo/quant track, the two calls **split maths+probability from live coding**.
- "First round is a **LeetCode-medium question and a follow-up**."
- HRT scores **teachability, communication, problem decomposition** — not just output.
- "They want code that **compiles and runs**, not pseudocode you promise to clean up later."

**HRT's own words** (hudsonrivertrading.com/hrtbeat/interview-at-hrt/ — blocked; via search summary) partly back this: *"you can expect a take-home test, roughly two phone interviews, and a full day of back-to-back 'onsite' interviews"*, and *"each stage of the interview process will have a particular focus/scope and a **standardized set of questions for the season**."* That last clause is the most useful single sentence in the whole corpus: **HRT runs a fixed question bank per recruiting season**, which is why the same items (inline, malloc/virtual memory, map vs unordered_map, two-sum-with-doubles) recur across years and why old Glassdoor items stay predictive.

## 3.2 PracHub-only items — ~45 HRT "technical screen" questions with no verifiable candidate
`https://prachub.com/companies/hudson-river-trading` (blocked; transcribed into pushpa-kumar/placement-prep). Every one is tagged "Technical screen". **No candidate account, no date, no thread URL.** Listed here so you can recognise them and *not* count them twice:

*Systems/C++:* Explain large memory allocation, swap behavior, and C++ inline trade-offs · Explain C++ inline, segfaults, virtual memory (MMU/TLB/page tables), and `std::string` internals (SSO) · Explain what a segmentation fault represents and how it relates to virtual-memory protection · Compare C++ pointers and references (initialization, nullability, reseating, arithmetic, ownership) · Compare stack and heap memory and describe how you'd probe/determine **stack growth direction** · Compare C++ `new`, `malloc`, and **placement new** — what happens when a new-expression is evaluated · Reason about C++ inlining, allocation strategies, and **static vs dynamic polymorphism** · Linux host and filesystem fundamentals · Troubleshoot a host that rejects SSH (layered: ping, traceroute) · Why `du` and `df` disagree · Unix signals, zombie processes, reaping.

*Python/other-language:* Discuss Python language and runtime fundamentals — should the answer describe CPython specifically or Python semantics generally? · Compare Python generators, decorators, and context managers · Explain Python and React performance fundamentals.

*Coding:* Design a deque-backed structure with push/pop front+back **and O(1) access by logical index** · Find a local minimum (element smaller than both neighbours) in 1D and 2D · Design a wrapper API `read(n)` returning any number of bytes over a fixed-chunk stream reader · Count matrix cells whose row and column neighbours match · Insert/Delete/GetRandom with **weighted** sampling · Minimize array amplitude (max−min) after removing one contiguous block · Longest common digit prefix across two arrays · Split a message into length-limited parts each ending `<X/Y>` · `flipdigits(x)` digit-reversal pair counting · Single-server 5-minute reactor queue simulation · Root-to-leaf path sum · Bird/nest alternating stick collection · 1-D road, simulate players/"watchers" moving to boundary L · Buffer parsers + a generic map class in low-level C++ · Count length-3 chat substrings containing a vowel · Implement order-modification for a C++ trading client/server · Count entities reaching boundary L · Wordle-style solver · Count inversions in a permutation · k smallest values ascending · Two Sum · Choose **mean or median** for a trading profit metric · Modular distribution of sums of independent dice · Baseline ML model predicting heart disease.

**Two of these are independently corroborated** (so they graduate to "probably real"): the **watchers-on-a-line simulation** and the **Wordle solver**, both of which surface independently in 1point3acres thread titles/summaries (threads 1173542 and 1145403). PracHub also names *"choose mean or median"*, which lines up with the corroborated Glassdoor mean/median estimator problem in §4.1.

## 3.3 Invented-looking items — flag and discard
- **ankitkushawaha1000/HFT** phone-screen list, self-labelled `[inferred]`: implement a rate limiter with a sliding window; median of two sorted arrays in O(log n); explain the C++ memory model / data races; `std::atomic<T>` and `memory_order_relaxed`; `epoll` vs `select`/`poll`; **what is a futex**; page faults and why a major page fault is catastrophic in HFT; thread pinning. These are plausible HFT questions but **there is no HRT candidate behind any of them**.
- **Dataford.io** (`Status: PRACTICE`, site explicitly does not claim candidate sourcing): two-threads-increment-a-counter race; running median with two heaps; 1ms-budget real-time risk system; P(X+Y<1) for two U[0,1]; E[flips] for two consecutive heads = (1+p)/p².
- **Tradermath.org**, explicitly labelled *"a representative HRT problem," not a confirmed real report*: **Romeo & Juliet** 15-minute-wait meeting probability (7/16). Also its "phone-screen brainteaser titles" — *Weighing Coins I, Trading Places, Christmas Cards, Rolling 1s and 2s* — **full text not published anywhere; these are Tradermath's own puzzle names.**
- **AlgoDaily** company page — the eight-problem practice set in §2.1f. No candidate attribution; AlgoDaily attaches generic sets to company pages.
- **TechPrep.app** — *"Maze with Portals"* and *"Longest Path With Different Adjacent Characters"*, labelled "representative". (The second is a distorted echo of the real Glassdoor item in §2.1f about A/B-valued graph nodes.)
- **techinterview.org / quantt.co.uk / hackerprep.io** low-latency sets (SPSC lock-free ring buffer with `alignas(64)`; false sharing; huge pages; SoA vs AoS; p99 regression triage; kernel-bypass packet walk-through; order-book with O(1) cancel). These are **onsite/senior-round material at best**, and none carries a candidate URL. techinterview.org does make one specific claim worth noting *as a claim*: that candidates who *"struggle to explain false sharing and its impact on lock-free counters will receive quick rejections."* Unverified.

---

# 4. Category-by-category answer to the brief

## 4.1 Live coding at the phone-screen stage

**Confirmed, first-hand or Glassdoor-verbatim:**
1. **Two Sum** — *"Given an array of integers, find two numbers such that they add up to a specific target number."* [Glassdoor via Lazar, TRANSCRIBED]
2. **Implement `stoi` / string-to-integer**, in C or C++ [Glassdoor via Lazar ×2, TRANSCRIBED]
3. **Remove all adjacent AB/BA and CD/DC pairs from a string over {A,B,C,D}** [Glassdoor via Lazar]
4. **Longest path in an A/B-valued graph with no two adjacent nodes equal** [Glassdoor via Lazar]
5. **Smallest missing positive integer** (`A=[1,3,4,5] → 2`) [Glassdoor via Lazar]
6. **Binary-string k-interval partition with a required count of 1s per interval** [Glassdoor via Lazar]
7. **Add two binary strings** [Glassdoor via Lazar; also the 2023 SWE intern OA]
8. **Days between two dates** [Glassdoor via Lazar + Quantt]
9. **"Implement a game with many edge cases"** [Blind, Algo Web Engineer, phone screen **round 2** — explicit stage tag]
10. **Design a connect-the-dots game and its challenges** [1point3acres thread 1149575, *C++ New Graduate Tech Phone Screen* — **explicit stage tag**, blocked, SNIPPET-ONLY]
11. **Wordle-style word-guessing solver** [1point3acres 1145403 + PracHub, two independent pointers]
12. **Watchers/players moving along a 1-D line to boundary L, with a continuous-case extension** [1point3acres 1173542 + PracHub, two independent pointers]

**The recurring meta-description from multiple Blind posts:** *"In coding rounds, they'll explain some complicated system or data structure that you'll chat about implementing, then implement it."* — i.e. the prompt is often **dictated verbally**, not pasted. One candidate reported spending **15 of a 30-minute screen just transcribing the dictated problem statement**, solving it optimally after hints, and still being rejected ~1.5 days later [Blind, SNIPPET-ONLY].

## 4.2 C++ conceptual rapid-fire — the consolidated real list

Ranked by number of independent sources:

| Question | Sources |
|---|---|
| **`inline`: what does it do, pros and cons** | Shivam5022 (FIRST-HAND) + Glassdoor/Lazar + Blind Core Dev + PracHub — **4 independent** |
| **`map` vs `unordered_map` — how each is implemented under the hood, which data structure** | Glassdoor/Lazar (×2 phrasings) + search corroboration — strong |
| **`vector` vs `list` (vs raw array) — trade-offs and internals** | Shivam5022 (FIRST-HAND) + Glassdoor/Lazar (×2) + Quantt — **3–4 independent** |
| **Virtual functions / vtable lookup; polymorphism in depth** | Glassdoor/Lazar (×2) |
| **`std::vector` internals: constructor, `push_back`, copy constructor, dynamic growth (amortised doubling)** | Glassdoor QTN_2640754 |
| **STL implementations generally + memory allocation for the runtime** | Glassdoor QTN_4298492 + Glassdoor/Lazar + Blind Core Dev |
| **C++ runtime exceptions — what throws and what doesn't (`vector::at` vs `operator[]` vs raw array OOB, which is UB)** | Glassdoor/Lazar — note the candidate's own confusion here is preserved verbatim; the *interviewer's* point is that raw-array OOB is UB with no diagnostic |
| **Smart pointers (`shared_ptr`, `unique_ptr`)** | Glassdoor/Lazar (in the "computer architecture" cluster) |
| Pointers and memory generally | Avinal (FIRST-HAND, systems intern) |

## 4.3 OS and memory — the consolidated real list

| Question | Sources |
|---|---|
| **"You have 4GB physical but allocate an 8GB buffer — possible? how? how is memory actually read as you traverse it?"** / **"How do you malloc 8GB on a machine with 4GB?"** | Glassdoor/Lazar + standalone Glassdoor QTN_2889562 — **the signature HRT phone-screen question** |
| **Internal working of `malloc`; demand paging** | Shivam5022 (FIRST-HAND) + Glassdoor QTN_2640754 + Glassdoor/Lazar |
| **How the kernel allocates memory to user processes** | Shivam5022 (FIRST-HAND) + Glassdoor/Lazar ("How does OS allocate memory to each process?") |
| **`sbrk` and `mmap`** | Shivam5022 (FIRST-HAND) — **only first-hand source; unusually specific, high signal** |
| **Virtual vs physical memory; what happens when virtual exceeds physical** | Glassdoor/Lazar (×3 phrasings) + Glassdoor QTN_2640754 |
| **Stack vs heap — what is stored where** | Glassdoor/Lazar |
| **Process vs thread; common threading models** | Glassdoor/Lazar (×3) |
| **IPC methods — between threads, between processes; how a named pipe (FIFO) works** | Glassdoor/Lazar |
| **User-level vs kernel-level threads ("how do you support multi-threading without kernel?")** | Glassdoor/Lazar |
| **TCP vs UDP** | Glassdoor/Lazar (×2) |
| **Hash table: implementation, collision handling, complexity, when it resizes and at what cost** | Glassdoor/Lazar 4-question ladder |
| **Hard vs symbolic link; `kill -15` vs `kill -9`** | Taro SRE experience, **explicitly "first round, 45-minute technical interview asking about Linux commands and systems"**, July 2025, no offer but rated positive — https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/site-reliability-engineer-united-states-july-1-2025-no-offer-positive-0b3bce6f/ [SNIPPET-ONLY] |
| Inode, RAID 5 vs 6, `du` vs `df`, soft vs hard link, `mv *`, provisioning Linux on 100 nodes | Glassdoor/Lazar (SRE/systems cluster) |

## 4.4 Debugging / code-reading at the early stage — **the honest answer is: barely any evidence**

- **No first-hand account places a "here is broken code, find the bug" round at the HRT phone screen.** The one first-hand C++ SWE account (Shivam5022) had zero coding in the phone screen. The debugging content that *is* documented sits **later**: HRT's own bookbuilder workshop (`make gdb_unoptimized` / `gdb_optimized`), and the onsite round repeatedly described as *"handed SSH credentials with the instruction 'There are bugs in this code. Find them'"* — but that description comes only from **prep sites** (spacecomplexity.ai, techinterview.org), which are blocked and uncorroborated. **Treat the SSH-debugging round as unverified.**
- The only early-stage code-reading-adjacent items with real sourcing:
  - **"Describe a recent interesting bug that you have resolved."** [Glassdoor/Lazar] — a *narrative* question, not a code-reading one.
  - Avinal's phone screen included **"deep investigation experience"** style resume probing.
  - The Algo Developer round-1 pattern (§4.6) explicitly includes **"debugging the corresponding simulation code"** after the probability question [SNIPPET-ONLY, multiple prep sites in agreement].
- **Caution for the parent brief:** Shivam5022's *Squarepoint* R1 ("debug a dummy `vector` implementation — missing destructor, needed a custom copy constructor, fixed memory leaks, added out-of-range checks") and his *DRW* OA ("finding a bug in a given code snippet") are **not HRT** and are frequently mis-attributed. Do not carry them over.

## 4.5 Follow-up escalation patterns — what is actually documented

Only three escalations survive verbatim, and all three are on the **same two base problems**:

1. **Two Sum → "what if the data type is double instead of int?"**
   Verbatim, Glassdoor via Lazar. The expected discussion is float equality: you cannot use `==` on the sum, so you need an epsilon tolerance `|a+b−target| < ε`, and the sorted-two-pointer approach still works while the hash-map approach breaks.
2. **Two Sum → "find two numbers whose sum is as close to the target as possible."**
   Verbatim, Glassdoor via Lazar. Sort + two pointers, tracking the best delta.
3. **`stoi` → "what would you do if the input was 1234567890 and you had 16-bit integers to work with?"**
   Verbatim, Glassdoor via Lazar. Overflow detection / saturation / wider accumulator.

**Not documented anywhere with a real source:** "now make it faster", "what if the input doesn't fit in memory". The external-merge-sort framing ("N large sorted log files that don't fit in memory — merge them") appears **only** in prep-site copy (dataford/techinterview) with no attribution. **Do not present it as an HRT question.**

**What *is* well-attested about escalation, in general terms:** multiple Blind/Glassdoor accounts describe the phone screen as *"a LeetCode-medium plus a follow-up"*, and HRT's own bookbuilder makes the ladder explicit — **correct → measured → profiled → optimised**. One Blind C++ Engineer account describes the OA/coding session as *"4 questions progressing from a warm-up parsing problem to full algorithm/data-structure challenges"* with *"emphasis on real-world efficiency over theoretical complexity"* — i.e. HRT escalates by **making the constant factor matter**, not by making the asymptotics harder.

## 4.6 Probability / maths at the early stage (Algorithm Developer / quant track)

**Yes — for the Algo Developer track, round 1 is often the maths round, and coding is round 2.**

- **"Tech interview on math 45 minutes, probability question, Bayes Theorem, random variable distributions, normal distribution"** [Glassdoor via Lazar] — explicit.
- **"Phone interview research + math; then 4 rounds of onsite"** [Glassdoor via Lazar].
- Blind post *"HRT Algo Developer phone interview, what to expect"* (https://www.teamblind.com/post/hudson-river-trading-hrt-algo-developer-phone-interview-what-to-expect-1nz00wah, blocked): **1st phone = quick CV walk-through then a couple of basic maths/stats brainteasers; 2nd phone = mostly algorithm questions, no actual coding.** [SNIPPET-ONLY]
- Blind post *"HRT Algo Software Engineer — technical (non coding) phone interview"* (K322pAXw): after passing **Codility**, a non-coding round on *"CS fundamentals like data structures, operating systems, developer tools, and memory"* — *"basic OS questions, threads, and memory."* [SNIPPET-ONLY]

**The one concrete, near-verbatim maths problem, and it is a good one:**
> A trading company receives daily profit X₁…Xₙ. **With probability 0.2, X = μ; with probability 0.8, X ~ N(μ, 1).** Is it better to use the **mean** or the **median** to estimate μ?
> Follow-up: **prove rigorously that P(|μ̂_median − μ| > 0.1) < P(|μ̂_mean − μ| > 0.1)**.
> A **CoderPad link was provided by email and used mainly to run NumPy simulations** to check the answer.

Sourced to a Glassdoor HRT interview experience (E470937 page P11 / Quantitative Researcher page) [SNIPPET-ONLY]. **Independently corroborated** by PracHub's *"Choose mean or median for a trading profit metric"* technical-screen entry. This is the highest-value single item in the whole quant-track corpus: it is the **derive-then-simulate-in-CoderPad** pattern in its purest form.

**Other early-stage maths/probability with real (Glassdoor-verbatim) sourcing:**
- **"We draw a person at random from the street, then keep drawing until we find someone taller. Expected number of draws?"** (answer: infinite)
- **Painted 3×3×3 cube:** probability a randomly chosen sub-cube has exactly one red face (6/27 = 2/9). Corroborated by a WSO account describing *"a probability question like the painted 3×3 cube type, requiring computation of probability and explanation of intuition."*
- **Roll a die 100 times, flip a coin 400 times — P(die sum > head count)?**
- **25 bunnies, 5 lanes, no timer — races to find the top 3** (answer 7).
- **Pearson correlation coefficient — definition and application.**
- **"Given a survey where each student reports their room size and nothing else, how would you estimate the average room size?"** (Quantt-sourced; selection-bias / size-biased-sampling reasoning.)
- WSO: **EV questions that are "variations of problems from the green book"** (Xinfeng Zhou). Corroborates OneRaynyDay's own prep choice.

**HRT-specific behavioural note on brainteasers, from HRT's public policy and echoed by Lazar:** HRT explicitly asks candidates to **say if they have seen a problem before**. Lazar's file says so directly: *"the firm says clearly on their website to be honest if you have seen a task before."*

## 4.7 Python roles vs C++ roles

**C++ track:** the screen is **systems depth**, and can be **entirely non-coding**. The Shivam5022 first-hand account is the template: 45 minutes, no editor, `inline` / `vector` vs `list` / `malloc` / demand paging / kernel memory allocation / `sbrk` / `mmap`. Corroborated by the Glassdoor line *"Phone interview deep C++ questions, including implementation details of STL and memory allocation… **No algo questions during phone interview, only C++ questions.**"*

**Python track:** the documented Python questions are a genuinely different set, and are far fewer:
- **"How does the Global Interpreter Lock work? Advantages vs disadvantages?"** [Glassdoor via Lazar]
- **"How does a dictionary/map work under the hood in Python?"** [Glassdoor via Lazar + Quantt — 2 sources]
- **"What's the purpose of the `yield` keyword?"** [Glassdoor via Lazar]
- **"Python decorators"** [Glassdoor via Lazar]
- **Pandas / DataFrame joins, and a SQL join question (CTEs)** [Glassdoor via Lazar]
- Prep-tier only, do not quote as real: how Python lists grow in memory; reference counting vs GC; list vs tuple vs deque under the hood; generators/decorators/context managers compared; "should you answer about CPython specifically or Python semantics generally?"
- Blind: *"Hudson River Trading Python Developer interview"* process = **CodeSignal → 2 phone rounds (1 hr each) → full-day onsite**; content skews to **probability, brainteasers, dice/card strategy games validated by simulation, and open-ended dataset exploration in a Python notebook.** [SNIPPET-ONLY]

**Cross-cutting, from prep sites but consistent across all of them:** *"If you interview for a Python role, you're still expected to understand systems, but with less granularity."* Unverified but plausible given the Avinal systems-intern account (Python/Bash + Unix + C++ pointers/memory in one 45-minute call).

**Systems/SRE/Linux track:** distinct again — Linux command-line and filesystem semantics (§4.3 bottom rows), plus tooling and automation. Avinal's account plus the Taro SRE account plus the Lazar sysadmin cluster all agree.

---

# 5. Pass/fail evidence and reported feedback

## 5.1 What is actually measurable

| Metric | Value | Source & tier |
|---|---|---|
| Glassdoor HRT interviews on file | **~493–510** across all roles | Glassdoor aggregate [SNIPPET-ONLY] |
| Positive-experience rate, all roles | **46.5%** (US); 60% in one earlier snapshot; 54.6% (CA), 42.9% (HK) | Glassdoor [SNIPPET-ONLY] — the spread across locales suggests small samples per locale; treat 46.5% as the headline |
| **Software Engineer** positive-experience rate | **32%** | Glassdoor SWE page [SNIPPET-ONLY] — **notably worse than the all-roles figure** |
| Difficulty | **3.45/5** (all roles, US); 3.4/5 (SWE); 3.82/5 (CA); 3.71/5 (HK) | Glassdoor [SNIPPET-ONLY] |
| Median process length | **21 days**, across 510 submitted interviews | Glassdoor [SNIPPET-ONLY] |
| Hardest-rated roles | Senior Software Engineer, Analyst | Glassdoor [SNIPPET-ONLY] |

**No credible stage-level pass rate exists.** Prep sites assert "OA pass rate 5–10% / 8–12%", "onsite pass rate after OA 30–40%", "resume-to-offer 1.5–3%" — these are **fabricated-looking round numbers from spacecomplexity.ai / oavoservice.com with no methodology and no source**. Do not repeat them.

## 5.2 Reported reasons for failing this round (with tier)

**FIRST-HAND / near-first-hand:**
- Taro, SWE, US, April 2025, **no offer, negative**: interviewers were *"rigid about matching an answer key even when correct answers (including modern C++20 approaches) were given."* (System-design round, not the phone screen — but the same complaint about answer-key rigidity plausibly applies earlier.)
- Blind: candidate spent **15 of a 30-minute screen transcribing a verbally-dictated problem**, solved it optimally after hints and bug fixes, **rejected ~1.5 days later**. → *the clock includes the time you spend understanding the problem.*
- Glassdoor QTN_2889562: candidate answered the malloc-8GB question and then **"Why are you interested in HRT?"** — and notes the motivation answer *"was apparently not satisfactory for my interviewer."* → **the "why HRT" answer is a real screening filter, not a formality.** Lazar's file independently records a reviewer's critique of a generic answer: *"The answer is reasonable but generic — it would work for any of their competitors just as well."*
- Lazar/Glassdoor, take-home variant: *"predicted to take 4–8 hours and it did… the project was self-checking, but the person reviewing got different results (incorrect) and there was no easy way of contesting this."*
- Lazar/Glassdoor, OA rant: *"the only way you can complete the test within the time span is if you are Red on CodeForces… Very frustrating experience because of the time limit."*
- Lazar/Glassdoor, applied to two tracks: rejected from **algo engineer** after failing the harder CodeSignal, immediately invited to the **software engineer** General Coding Assessment, scored **840+ with 20 minutes left**, and was **still rejected a week later "for no reason."** → **a strong OA score is not sufficient; conversion is opaque.**
- Avinal (FIRST-HAND, systems intern): received **verbal feedback at the end of the phone screen**. His own retrospective failure modes: talked too much, and **did not ask about the role** — *"you must do this at least once."*

**PREP-TIER (flagged, not verified):** "seven named failure modes"; "silence during technical rounds"; "candidates don't get offers because they ran out of time or their code didn't compile on the first try"; "freezing on false sharing = quick rejection."

---

# 6. Practical read for someone preparing this round

1. **Determine your track first.** C++ SWE/Core → the phone screen may contain **no coding at all** and be 45 minutes of `inline` / `malloc` / paging / STL internals. Algo Developer → round 1 is likely **probability + a NumPy simulation in CoderPad**. SRE/Systems → Linux semantics.
2. **The single highest-yield item is virtual memory.** "8GB on a 4GB machine" appears in more independent sources than any other HRT question, and every follow-up (demand paging, overcommit, swap, page tables, `mmap` vs `sbrk`, what a page fault costs) is documented.
3. **Second-highest: `inline` pros and cons.** Four independent sources. Have the real answer (it is a linkage/ODR hint, not an inlining command; icache bloat; why the compiler ignores you; why `static`/LTO changes the picture).
4. **Know the amortised-growth story for `vector` cold**, including copy vs move on reallocation — Glassdoor QTN_2640754 lists constructor → `push_back` → copy constructor → dynamic growth as a single chained sequence.
5. **Rehearse the two-sum escalations specifically**: with doubles (epsilon), and "closest to target". They are the only verbatim-documented follow-ups.
6. **HRT runs a standardised question bank per season** (their own words). Old Glassdoor items stay predictive across years — which is why 2022-era items still match 2025 accounts.
7. **Prepare the "why HRT" answer as a technical answer, not a fluff answer.** It is documented as a rejection cause.
8. **Say it if you have seen the problem before.** HRT asks you to, in writing.

---

# 7. Source inventory

**Read in full, locally (GitHub):**
- https://github.com/Shivam5022/Interview-Experiences — `Readme.md` — FIRST-HAND, HRT C++ SWE
- https://github.com/Lazar-Ilic/Lazar — `Notes/Computer Science/Algorithms/Interviews Coding Rounds/Hudson River Trading.txt` (34 KB) — TRANSCRIBED Glassdoor dump, Aug-2022 cycle
- https://github.com/avinal/avinal.github.io — `src/content/posts/blogs/hrt-interview-1.md` — FIRST-HAND, HRT Systems Intern Summer 2021 (blog itself blocked)
- https://github.com/OneRaynyDay/oneraynyday.github.io — `_posts/2020-09-30-Interviewing-During-Covid.md` — FIRST-HAND, HRT Algo Engineer 2020, offer accepted
- https://github.com/hudson-trading/wwhrt-bookbuilder-workshop — HRT's own published Core-Developer exercise
- https://github.com/pushpa-kumar/placement-prep — `raw-notes/company-hrt-citadel.md` (55 KB), `raw-notes/topic-*.md`, `raw-notes/wave2-*.md`, `generator/final_entries.json` (239 HRT entries) — TRANSCRIBED aggregator with source URLs
- https://github.com/ankitkushawaha1000/HFT — `companies/hudson-river-trading/round-02-technical-phone-screens/questions.md` — PREP/UNSOURCED (self-labelled `[anecdotal]`/`[inferred]`)
- https://github.com/perixtar/quant-interview-oa-bank — cloned; **contains no HRT question content** (only a company-domain mapping in `assets/company-domains.json`). Nothing to mine.
- https://github.com/hieptran1812/my-website — `content/blog/trading/quant-careers/online-assessments-and-screens-decoded.md` — general OA/screen essay; HRT mentioned only as a category example. No HRT questions.
- https://github.com/sgoel97/blog — HRT appears only in a list of firms. No questions.

**Primary sources named but NOT readable in this sandbox (search-summary only):**
Glassdoor E470937 + QTN pages · teamblind.com (svkrykwf, 87MxP0h4, yuqksebo, wy1hgi2m, 1nz00wah, K322pAXw, uH03BvKD, AKOjp7Ek, Au8BSKNX) · leetcode.com/discuss (889638, 498475, 549526, 1458197, 2492212, 3078249, 4452641, 628687) · 1point3acres threads 1149575, 1026717, 1173542, 1145403, 1137231, 1102726, 1143778, 1000120, 545431 · jointaro.com HRT experiences (SWE Apr-2025, SWE Oct-2025, SRE Jul-2025) · wallstreetoasis.com · hudsonrivertrading.com/hrtbeat/interview-at-hrt/ and /engineering-and-interviewing-at-hrt/ · dev.to · medium.com

**Prep sites (all blocked; treat all content as unsourced):**
prachub.com · quantt.co.uk · tradermath.org · techinterview.org · techprep.app · spacecomplexity.ai · hackerprep.io · hacktherounds.com · dataford.io · algodaily.com · myntbit.com · ghostinterview.co · linkjob.ai · oavoservice.com · nodeflair.com · datainterview.com
