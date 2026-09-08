# HRT & Jump Trading — Full-Time / Experienced-Hire vs Internship: the DELTA

Compiled 2026-09-08. Scope: only what *changes* when you move from the intern loop to the
full-time (new-grad) and experienced-hire loops at Hudson River Trading and Jump Trading.

## 0. Method, tooling limits, and how to read the confidence tags

**Tooling constraint (important).** The session's egress proxy blocked *every* direct page
fetch attempted: `hudsonrivertrading.com`, `teamblind.com`, `1point3acres.com`,
`glassdoor.com`, `jointaro.com`, `efinancialcareers.com`, `oneraynyday.github.io`,
`news.ycombinator.com`, `tradermath.org`, `spacecomplexity.ai`. So **no primary page was read
verbatim in this pass.** Everything below comes from (a) web-search result *summaries* that
quote those pages, and (b) an existing first-hand-sourced research file in the user's own
repo, `NoctNight/quant-prep-database`, at `research/hft_cluster.md`
(https://github.com/NoctNight/quant-prep-database/blob/main/research/hft_cluster.md), which was
built from GitHub write-ups, LeetCode Discuss, Blind, Glassdoor and 1point3acres and carries
its own per-item provenance. Where this pass *corroborates* or *contradicts* that file, I say so.

The GitHub MCP tool is repo-scoped to `noctnight/*`, so first-hand GitHub write-ups
(`Shivam5022/Interview-Experiences`, `avinal/website`, `stanleywu111/jump-orderbook`) could not
be re-read directly this pass; their content is carried over from `hft_cluster.md`, which
quotes them.

Web-search budget was exhausted at 200/200 session-wide after ~18 queries in this pass.

**Confidence tags**

| Tag | Meaning |
|---|---|
| **[A]** | First-hand candidate write-up or official firm text, quoted in a source I could read |
| **[B]** | Forum report (Blind / Glassdoor / 1point3acres / WSO / LeetCode Discuss), single or few reports, reached via search summary |
| **[C]** | Prep-site / SEO content only — see the warning below |
| **[unclear]** | Level (intern vs FT) not stated by the source |

> **Warning on [C] sources.** A large share of 2025–26 search results for these two firms are
> AI-generated SEO content farms with no candidate behind them: `techinterview.org`,
> `quantt.co.uk`, `tradermath.org`, `quantblueprint.com`, `spacecomplexity.ai`,
> `oavoservice.com`, `getsmartresume.com`, `extern.com`, `hackerprep.io`, `dataford.io`,
> `myntbit.com`, `datainterview.com`, `thita.ai`, `everythingquant.com`, `prachub.com`,
> `nodeflair.com`, `techprep.app`. They confidently invent numbers, and they contradict each
> other and the first-hand record. Two concrete contradictions caught in this pass are called
> out in §1.1 and §1.6. Treat every [C] claim as a hypothesis, not a fact.

---

## 1. HUDSON RIVER TRADING

### 1.1 Intern OA vs full-time OA — the delta

**What the intern OA is** (baseline the user already has): 3 questions, roughly LC-medium,
90–150 min depending on year; platform has varied — Codility for the 2021 Systems intern
(90-min test inside a 2.5 h window, C/C++/Python/Go, no Java, docs allowed but "do not copy
code", "correctness *and* performance are the most important factors, test duration also
counts") **[A]**, CodeSignal in later cycles; some years C++-only, some C/C++/Java
(1point3acres threads 668765, 468863) **[B]**.

**What changes at full-time.** The clearest finding is that **"the full-time OA" is not one
test — it is two different tests, split by track**, and this is the single most important
structural delta:

1. **Algo Dev (quant-research) challenge — 2 hours, 3 questions.** Two LeetCode-medium plus a
   third described as *harder than LeetCode hard*; **all hidden tests must pass within the
   time/memory limits** (no partial credit for a correct-but-slow solution). This is a
   **custom HRT-authored challenge delivered through CodeSignal, not CodeSignal's off-the-shelf
   product** — which is why it has no 600-point score. **[B]**, corroborated by the user's
   prior file (Glassdoor via `Lazar-Ilic/Lazar`; ricsign playbook) and re-confirmed this pass
   by search summaries stating "the algorithm engineer challenge has a two-hour time limit to
   complete three questions … difficulty from LeetCode medium to hard, covering string
   manipulation, graphs, and backtracking, with a very tight 2-hour limit."
   → **CONFIRMED as reported.**

2. **SWE / SDE — CodeSignal General Coding Assessment (GCA), 4 questions, 600-point scale,
   ~70 min.** This is CodeSignal's standardised product, not HRT-specific. **[B]**

**The 600-point scale, and what a "pass threshold" actually means.** The 600 scale belongs to
the *GCA*, not to the Algo Dev challenge. Reported HRT thresholds:

- **~500/600 is the general bar**; **560+ for SDE and Algo Dev teams** specifically. **[C]**
  (`oavoservice.com`) — plausible and consistent with the broader CodeSignal market, but this
  is a prep-site number, treat as [C].
- CodeSignal's own docs confirm 600 is the GCA maximum and that companies set their own cut
  scores (https://support.codesignal.com/hc/en-us/articles/13408542717079-Understanding-Assessment-Score,
  https://support.codesignal.com/hc/en-us/articles/23458723018391-Guide-to-Setting-Cut-Scores). **[A, platform docs]**
- **A high score is not sufficient.** The prior file records a candidate who scored **840+ on
  the old CodeSignal scale and was still rejected** **[B]**, and this pass found repeated
  reports of clean OA runs followed by silent rejection **[B]** (Glassdoor). HRT appears to
  use the OA as one input, not a pure numeric gate.

**Delta summary (OA):**

| | Intern | Full-time |
|---|---|---|
| Tests | One test, 3 Q, ~LC-medium | **Two different tests by track** |
| Algo Dev | (intern Algo Dev OA = same 3 Q general test) | **2 h / 3 Q, third > LC-hard, all hidden tests must pass** |
| SWE | 3 Q | **CodeSignal GCA, 4 Q, /600, ~500–560 bar [C]** |
| Grading | correctness + performance + duration [A] | same, but **zero partial credit** on the Algo Dev third question |
| Platform | Codility (2021 systems) / CodeSignal | CodeSignal |

> **Contradiction flagged.** Several [C] sites (`getsmartresume.com`, `extern.com`) assert the
> HRT OA is "a 90–120 min **HackerRank** test with **4–6 LeetCode-hard** problems covering DP,
> graphs, **concurrency and low-level systems**, solve 80–100% to advance." **No first-hand
> report supports this.** Every first-hand account says Codility or CodeSignal, 3–4 problems,
> and no OA report mentions concurrency or systems questions on the OA at all. Discard it.

### 1.2 The full-time phone screen: pure C++/OS trivia. Do interns get this?

**Answer: no — this is the sharpest intern→FT delta at HRT.**

**Full-time phone screen 1 (30–45 min): frequently contains no algorithms whatsoever.** The
canonical first-hand account is `Shivam5022/Interview-Experiences` (C++ SWE, full-time, IIT-D
campus), which records the screen as: **`inline` pros and cons; `vector` vs `list` internals;
how `malloc` works; demand paging; how the kernel hands memory to a process; `sbrk` vs `mmap`**
**[A]**. → **CONFIRMED, and the specific question list in the brief is accurate and traceable
to that one write-up.**

Corroborating full-time reports: "Phone interview deep C++ questions … No algo questions"
**[A/B]**; Blind Core Developer thread (`yuqksebo`): "lots of questions on STL containers, how
implemented, pros and cons," expectation that low-level programmers can write vectorised
(SIMD) code, "study virtual memory/paging and multithreading" **[B]**; a 2022 Glassdoor dump
adds virtual memory vs physical (4 GB RAM, allocate an 8 GB buffer — possible? how is it
read?), thread vs process and threading models, IPC and named pipes, virtual functions and the
vtable, `map` vs `unordered_map`, hashtable collisions and resizing, the GIL, C++ exceptions vs
UB on out-of-bounds, user-level threads without kernel support, TCP vs UDP, smart pointers
**[B]**. This pass added a 2025 report of "classic C++ coding questions regarding pointers and
references" plus OS "deep, implementation ideas," networking, and prior-project deep-dives **[B]**.

**Full-time phone screen 2 (~60 min): live coding** in your primary language **[B]**. So the
full-time loop has **two** phone rounds, deliberately split: one conceptual, one coding.

**The intern equivalent.** Interns get **1–2 technical phone rounds, and the systems content is
role-gated rather than universal**:

- **Systems intern**: one **45-min explicitly no-coding call** on Linux/Unix, C++ pointers and
  memory, Python/Bash, tooling **[A]** (`avinal`). This is the *closest* intern analogue to the
  full-time trivia screen — but it exists only for the Systems track.
- **SWE intern**: a ~30-min OS/OOP/DS call plus a live-coding call **[B]**. Lighter, broader,
  and much less C++-specific than the full-time version.
- **Algo Dev intern**: the phone content skews math — basic probability and linear algebra
  **[B]** (Blind) — not `sbrk`/`mmap`.

**Delta:** the FT screen is *deeper on C++ object model and OS memory management*, is
*language-committed* (HRT posts "Software Engineer (C++)" and "(Python)" as separate roles, and
HRT's own text says a C++ interviewee is "expected to have a fair bit of low-level knowledge
about how computers work," while a Python interviewee needs "some systems knowledge … but less
specifics") **[A, official]**, and is *its own dedicated round* rather than a segment of a
general call.

### 1.3 Full-time onsite: 4–6 rounds, up to 6.5 hours. Round types. Intern version?

**Full-time onsite: 4–6 rounds in a single day**, New York strongly preferred (virtual
possible) **[A/B]**. The best-documented single data point remains the **algo-engineer
candidate with a 6.5-hour onsite after OA + two phone screens, ≈10 h total** **[A]**
(OneRaynyDay, 2020 — page itself now unreachable). Round types, with what each actually tests:

1. **Coding block** — reported as up to **2 hours / 4 questions** in one sitting **[B]**.
   Performance is graded, not just correctness: a candidate who "built a piece of a trading
   system in OO code that must be as performance-efficient as possible" solved it and **every
   test TLE'd → fail** **[B]** (LC 628687). "Correct but slow" is a rejection at FT; at intern
   level performance matters but the problems are LC-medium-shaped.
2. **The open-ended design / spec round** — "**take a spec, design a system, then absorb
   changing requirements on the fly**" **[B]** (Blind). → **CONFIRMED as a real, distinct
   full-time round.** This pass could not find a *new* first-hand corroboration; search
   summaries only reached the generic "technical design discussions" phrasing on HRT's own
   blog **[A, official]** and prep-site restatements **[C]**. Related first-hand FT design
   prompts on record: **design a system to route packets between one hub and many node
   servers** **[B]** (Glassdoor QTN_8479239); **implement an order-modification feature for a
   C++ client/server trading system** **[B-]**; **order book with add/cancel/match, then "now
   make cancel O(1)"** **[C→B]**. HRT's own public Core-Dev-style exercise is exactly this last
   shape: `hudson-trading/wwhrt-bookbuilder-workshop` — optimise a naive book builder over real
   crypto add/delete/modify events with `make measure / profile_functions / profile_lines /
   check` **[A, official]**.
3. **Data-science / pandas round** — pandas dataframe joins, prediction tasks, SQL joins with
   CTEs; and a rule several candidates report: "**a pandas question is expected if pandas is on
   your résumé**" **[B]** (Glassdoor). → **CONFIRMED.** Attached to Algo-Dev-adjacent and Data
   Scientist loops rather than every SWE loop.
4. **OS / systems round** — escalates past the phone screen into memory layout and cache
   behaviour for core roles: SPSC lock-free ring buffer, false sharing and `alignas(64)`,
   memory orderings **[C]**; "two threads increment a counter 1M times each, result < 2M — why,
   and fix it" **[B/C]**. A prep site claims HRT "devotes about a quarter of the loop to
   systems" and that candidates who cannot articulate false sharing are "rejected swiftly"
   **[C]** — directionally consistent with first-hand reports, but the quantity is [C].
5. **Probability / math round** — for Algo Dev: roll a die 100× and flip a coin 400×,
   P(dice sum > #heads), where **an exact DP/FFT answer is expected and Monte Carlo is
   criticised** **[B]**; expected draws until someone taller than the first person **[B]**;
   Bayes/normal-distribution 45-min math round **[B]**; 25 bunnies / 5 lanes / no timer → 7
   races, with HRT explicitly asking candidates to disclose if they have seen it **[B]**.
6. **Behavioural / team-fit** with a senior engineer or trader **[B]**.

**Do interns get a shorter version? Yes — substantially.** The intern loop as recorded is
**OA + 1–2 calls**, with no reported full-day onsite of the 5–6-round kind, and no reported
open-ended spec-design round, no data-science round, and no dedicated systems round outside the
Systems-intern track **[A/B]**. Reported intern perk: onsite candidates receive an Apple Watch
**[B]** (1point3acres) — implying some intern onsites do happen, but the round list is not
documented at anything like the FT depth.

**Total time:** FT ≈ **8–10 h** end-to-end, onsite **5–6.5 h**; intern materially less.
**Calendar:** FT ~**4–8 weeks** from first contact to offer (one candidate: 4 weeks; general
range 1–2 months) **[B/C]**.

### 1.4 Experienced hires: what changes again, and the week-long order-router take-home

This is the **weakest-evidenced area** of the HRT picture — flagging that honestly.

- **Week-long take-home: implement an order router**, followed by a Linux/networking/C++
  interview. Source: **Glassdoor [B]**, carried in the prior research file. Level is recorded
  as `[FULL-TIME]` and the "experienced" framing is an inference from the format (a week-long
  project is not a student-loop artifact) — **the source does not state a level or a title**.
  This pass **failed to re-corroborate it**: a targeted search for the order-router take-home
  returned no result mentioning it. **So: reported once, level unconfirmed, not re-verified.**
- **4–8 h Verilog take-home**, with a self-checking grader that disagreed with the human
  reviewer — FPGA-adjacent role **[B, unclear level]**.
- **2-hour multi-file Python project** as an onsite round for Systems/SysTrade roles **[C,
  unsourced prep notes]**; and SysTrade phone-2 reported to include **SSH-ing into HRT cloud
  hosts to diagnose a live issue** **[C, unsourced]**.
- **"Optimise/improve a backtracking problem"** as an onsite round, in a Blind thread reporting
  a **~$600k** C++ engineer offer — i.e. a senior/experienced band **[B]** (Blind `87MxP0h4`).
- What senior loops add, per [C] synthesis: deep discussion of past systems work plus design of
  a low-latency component or trading-adjacent system. Plausible, unverified.

**Honest summary for experienced hires:** the *structure* (OA → 2 phones → onsite) does not
clearly change; what changes is that **take-home projects appear** (order router at a week,
Verilog at 4–8 h), the **design round carries more weight and is grounded in your own past
systems work**, and the **coding round shifts from "solve it" to "optimise it."** Whether
experienced hires skip the OA is **not documented** in anything found.

### 1.5 Algo Developer (quant research) vs Software Engineer track — intern vs full-time

HRT's own postings and NUFT notes treat **Algo Dev as essentially the QR role**. Track
divergence is *larger at full-time than at intern level*:

| | Algo Dev | SWE |
|---|---|---|
| **FT OA** | Custom 2 h / 3 Q, third > LC-hard, all hidden tests **[B]** | CodeSignal GCA 4 Q /600 **[B]** |
| **FT phone** | Adds a **research/math screen**: probability, Bayes, distributions, linear algebra **[B]** | **C++/OS trivia screen**, often algorithm-free **[A]** |
| **FT onsite** | Adds the **data-science/pandas round** and probability-to-code (exact, not Monte Carlo) **[B]** | Adds the **systems/OS round**, TLE-graded coding, packet-routing / order-book design **[B]** |
| **Intern** | Phone skews to basic probability + linear algebra **[B]**; final round reported to touch randomized algorithms, ML system design, brainteasers, LC-hard **[B]** | OS/OOP/DS call + live coding **[B]** |

Also distinct at FT: **Core Developer / low-level C++** (STL internals, SIMD, virtual memory,
multithreading **[B]**), **Systems/SysTrade/SRE** (inode, RAID 5 vs 6, `du` vs `df`, `mv *`,
soft vs hard links, Unix signals/zombies, troubleshooting a host refusing SSH, Python
generators vs decorators vs context managers **[B]**), **Algo Web Engineer** (its own OA:
recursive divide-and-conquer, "very annoying string parsing with edge cases" ~60 min; phone-2
"implement a game with many edge cases" **[B]**), and **Data Scientist** (mean vs median for a
trading P&L metric, Pearson correlation, dice modular-sum distributions **[B-]**). **Interns do
not have this many distinct tracks** — the recorded intern tracks are SWE, Systems, and Algo Dev.

### 1.6 Return offers and whether returning interns skip stages

- **Return-offer rate: volatile and cycle-dependent.** Blind (Feb 2023): the offer rate for the
  last intern class "was a bit lower, but the count of interns had also gone up massively," and
  the reasons were "unrelated to HRT's overall performance" **[B]**
  (https://www.teamblind.com/post/HRT-core-intern-return-offer-rate-2KdBM4Xc). Many **summer
  2022** interns reported no return offer, attributed to firm performance **[B]**. A 2025-era
  figure of **~85%** for SWE interns circulates **[C]**, as does a **80–90% for strong interns**
  band **[C]** — both prep-site restatements, not first-hand.
- **Do returning interns skip stages? Not documented.** A targeted search for this returned
  nothing HRT-specific; every result was about other companies. **No evidence either way** —
  do not assume the intern loop is a shortcut into the FT loop.
- **Selectivity context**: acceptance below ~2% from roughly 5,000–10,000 applications for
  ~50–70 spots **[C]**; efinancialcareers reports HRT hires ~0.1% of applicants for the
  internship **[B]** (https://www.efinancialcareers.com/news/hudson-river-trading-intern-pay).
  Intern pay: **$5,800/week + $25k signing bonus + paid housing**, ≈$175k–$210k annualised
  **[B/C]** (Levels.fyi lists $145/hr).

> **Second contradiction flagged.** A LinkedIn post asserts "HRT accepts roughly 20 …" and
> "0.1% acceptance"; the [C] sites say "below 2%." These are not reconcilable and neither is
> sourced. Ignore precise acceptance-rate numbers entirely.

---

## 2. JUMP TRADING

The organising fact for Jump, and the thing that makes its intern→FT delta different in *kind*
from HRT's: **Jump is decentralised, and the loop is assembled per team/track rather than run
as one company-wide funnel.** See §2.5.

### 2.1 Intern loop vs full-time loop

**Intern baseline (already known to the user):**
- **QR intern: no OA, three rounds** — HR call; a round with coding plus a trading-strategy /
  game-theory problem; a further round **[B]** (1point3acres thread 1026654, "全集挂经").
  → **CONFIRMED** this pass: a search summary of that same thread states "generally three
  rounds total with no online assessment, and the process moves very quickly. The first round
  is an HR interview discussing background, followed by a second round involving coding and
  trading strategy."
- **Quant intern (2020)**: 3 questions in a 105-min window on **Codility** **[B]** (LC 870149) —
  so "no OA" is a QR-track property, not a Jump-wide one.
- **SDE intern (Cambridge, 2019)**: behavioural phone screen, then an in-person technical round
  on C/pointers/arrays and **implement a hash map from scratch** (`add`, `get`) with trade-off
  discussion **[B]** (WSO).
- **Campus SWE (2017)**: 45-min on-campus whiteboard with two engineers → full onsite day in
  Chicago, any language allowed **[B]**.
- **Algo-trading intern superday (2013, dated)**: four rounds — whiteboard math, pen-and-paper
  brainteasers, probability, and a pure C++ coding-on-laptop round **[B]**.

**Full-time loop — what is added:**
1. **A recruiter / HR-and-background round comes *first*, and it is substantive.** 1point3acres
   thread 1086311 (SDE, 2024–25): round 1 is an HR/background conversation on résumé and
   projects with follow-ups on *your specific contributions and methods*, before any technical
   round **[B]**. The recruiter screen is also where **which team and track you are being
   considered for** is settled **[C]** — which then determines everything downstream.
2. **An OA appears** for engineering tracks (HackerRank or Codility) where the QR intern loop
   had none. See §2.2.
3. **A full-day onsite.** 1point3acres FT reports describe **9am–5pm, continuous, interviewing
   through lunch**, each interviewer starting from the résumé and quick questions, then one or
   two coding problems or system-design/networking questions, **drilling progressively deeper
   until you hit the edge of what you know** **[B]**. Other reports: **four back-to-back 45–60
   min interviews** in Chicago **[B/C]**; a 2010 Glassdoor report of a 4-hour onsite "focused on
   concurrency in C/C++" **[B]**; one candidate reported **a 3-hour OA followed by a hiring-
   manager call and then two 4-hour interview days** **[B]**.
4. **Systems/low-level rounds** that the intern loop does not have. See §2.3.
5. **The take-home order book**, for some SWE hires. See §2.4.

**FT QR loop specifically**: strong candidates flown to Chicago for **four back-to-back 45–60
min rounds**, standard mix being **two quant/maths rounds** (pen-and-paper probability,
expected-value games, statistics, linear algebra), **one coding round** (Python with pandas and
NumPy on quant tracks), **one behavioural/fit** **[C]**. A more specific report: **3 hours with
2 quants and a trader, ~1 hr each — 1 hr Python coding assessed on data structures, 1 hr on
microstructure and HFT-strategy/backtesting knowledge, 1 hr conditional probability and
stats** **[B/C]**. Note the sharp delta from the QR *intern* loop: **market-microstructure and
backtesting knowledge is examined at FT and is absent from the intern loop.**

**Counter-intuitive finding worth flagging:** a **FT QR** candidate (Oct 2022) reported the
round being **pure C++ data-structure coding despite the QR title** — implement a linked list,
then swap two given nodes **[B]** (WSO). Jump's FT QR loop is not reliably a math loop.

### 2.2 Full-time OA: "hard DP and graphs" — confirmed?

**Partially confirmed, with an important caveat.**

- **The "hard DP and graphs" claim is real and traceable to Glassdoor**, in the same breath as
  the claim in §2.3: a HackerRank OA with "**hard DP and graph problems**," but interviews that
  "don't go beyond LeetCode-medium" **[B]**. Re-confirmed this pass by two independent search
  summaries. → **CONFIRMED as a reported claim.**
- **Format**: 90–120 min, **two or three hard problems** **[C]**; one FT report of a **3-hour**
  OA **[B]**; platform is **HackerRank or Codility depending on track** **[B/C]**.
  **Brute force that passes tests but has bad complexity does not pass** **[C]**.
- **Caveat — the first-hand OA record looks different from "hard DP and graphs."** The one
  fully first-hand FT OA on record (2025 SRE/infra code round, `Chao-Xi/jxtechbook`, four
  Codility-style problems in Python) is **implementation-heavy rather than algorithmically
  hard**: smallest missing positive integer (Codility `MissingInteger`, O(N)); a
  **trading-indicator simulation** (given a price series, a buy pattern such as two consecutive
  rises ignoring flat ticks, and a sell pattern, output the running position after each tick);
  a **file-sync diff** over (perm, user, size, mtime, name) listings subject to source-readable
  and dest-writable, O(N+M); and a **pandas CSV aggregation** **[A]**. Other Codility items:
  maximum distance between two unequal elements **[B]** (LC 686727) and a stream/
  `istream_iterator` parsing question with comment and delimiter handling **[B]**.
- **Resolution:** the OA content is **track-dependent**. Core/SWE tracks plausibly get the hard
  DP/graph HackerRank; SRE/infra gets Codility parsing-and-simulation. The [C] claim that
  Jump's algorithmic questions are "**Codeforces 2400+**" is unsupported by any first-hand item
  found and should be discarded.

### 2.3 "Interviews don't go beyond LeetCode medium, but core dev adds kernel / concurrency / CPU architecture"

**CONFIRMED — this is the most consistently reported thing about Jump's FT loop, and it is the
core intern→FT delta.**

- The "**don't go beyond LeetCode-medium; centred on your grasp of programming**" phrasing is
  Glassdoor's **[B]**.
- The additive clause is Blind's, verbatim in the prior file: interviews include "**kernel,
  concurrency, CPU-architecture questions in addition to the usual algorithms**" **[B]**
  (teamblind `ufqxesha`).
- Independent corroboration this pass: a FT technical phone screen on **CS fundamentals — OS,
  architecture, networks, undefined behaviour** **[B]**; and "coding questions were not typical
  LeetCode, nor math/stats, nor low-level hardware — **more realistic things you'd have to
  implement on the job**" **[B]**.
- Concrete low-level items on record: **concurrency in C/C++** onsite **[B]** (2010); "**struct
  with three 4-byte ints and a 1-byte flag — lay it out and why**" (padding / false sharing)
  **[C]**; prep-site consensus on the C++ memory model and `std::atomic` orderings on x86/ARM,
  `shared_ptr` cost, lock-free stack with CAS/ABA, SPSC ring buffer, arena/pool allocators,
  cache-hierarchy latency, kernel bypass **[C]**.
- Design prompts reported for FT core roles **[C]**: market-data feed handler; order gateway /
  in-memory order book; fast logging pipeline; a store for billions of market events per day
  for research replay; share data between one fast writer and many readers without locks;
  "**walk a packet from the NIC to your trading code with kernel bypass**"; when FPGA beats
  software; profile a slow market-data processor.

**The delta stated plainly:** the *algorithmic* bar barely moves from intern to FT (both sit
around LC-medium; intern content is DS-implementation — trie, hash map, linked list from
scratch in C++ — plus puzzles). **What moves is the systems axis.** Jump does not make you
solve harder puzzles at FT; it makes you explain the machine.

### 2.4 The take-home order book — at what level?

**Level: full-time SWE.** The artifact is `stanleywu111/jump-orderbook`
(https://github.com/stanleywu111/jump-orderbook), whose author describes it as a coding
exercise done for a Jump Trading interview **[A, artifact]**. It is **not** reported at intern
level anywhere.

**Spec** (from the artifact): parse a message stream — `A,<id>,<side>,<qty>,<price>` (add),
`X,…` (cancel), modify, and `T,<qty>,<price>` (trade); after **every** message print the
mid-price (`NAN` if one side is empty); every **10th** message print the book; after each trade
print cumulative volume at that price level; validate expected trades against fills. The
author's design: prices as `uint32_t` (×1000), per-side `std::map` + `unordered_map` price-level
map, intrusive order lists, id→iterator hash for **O(1) cancel**, a custom pool allocator, and
error counters instead of exceptions.

**Caveats:** the artifact is **undated**, and this pass found no second candidate reporting it,
so its current frequency is unknown. Jump also uses "order book keeping in C++" as an *online
test* for SDE roles **[C]**, and the same shape recurs as a live design round ("make
`cancel(order_id)` O(log N)" over two sorted maps with per-price-level doubly-linked lists and
an `order_id → (side, price, list_node)` hash) **[C]**. So treat "order book" as a **theme that
appears at FT in take-home, OA, and design-round form**, rather than as one fixed take-home.

### 2.5 Experienced hires and the pod/team structure — does the process vary by team?

**Yes, and this is the defining structural feature of Jump's FT process.**

- Jump is **"famously decentralised"**, with siloed teams and significant early autonomy; the
  process **"forks into tracks, with the content of every stage shifting depending on which one
  you are in"** **[C]**, and the recruiter screen exists partly to determine **which team and
  track** you are routed to **[C]**. The NUFT note in the prior file independently describes
  Jump as "**very engineering-focused with siloed teams**" and school-selective **[B]** — which
  corroborates the *structure*, if not the [C] phrasing about the loop.
- The first-hand evidence is consistent with per-team variation: an SRE/infra FT candidate got
  four Codility Python problems **[A]**; an SDE FT candidate got HR-first-then-technical
  **[B]**; a QR FT candidate got pure C++ DS coding **[B]**; another QR FT report is 3 hours
  with two quants and a trader **[B/C]**. These are not the same loop.
- **Practical consequence:** unlike HRT, **there is no single "Jump full-time loop" to prepare
  for.** Ask the recruiter which team and track, because the OA platform, whether there *is* an
  OA, the onsite length (3 h vs 4 h vs 9-to-5 vs two 4-hour days), and the systems depth all
  follow from it.
- **Experienced hires specifically:** engineering candidates are expected to show **clean modern
  C++ — RAII, sensible ownership, concurrency and low-latency structures** — and Jump "tests
  systems thinking as much as coding ability," expecting you to reason from application logic
  down through OS, network stack and hardware **[C]**. Onsite for experienced candidates is
  described as **2–3 back-to-back 45–60 min technical rounds** covering advanced C++, low-
  latency system design, mathematical problem-solving, and live implementation of a non-trivial
  algorithm **[C]**. Blind has a "jump trading tc for industry hire" thread confirming a
  distinct industry-hire channel exists **[B, content unread]**. Overall process length: ~24
  days average across 187 Glassdoor submissions; difficulty 3.19/5; 60.3% positive **[B]**.
- **Coverage gap to state plainly:** 2021–2026 first-hand Jump material is **thin**. Much of the
  concrete text is 2013–2020 or the single 2025 SRE round. The Blind "Jump Trading AI team
  interview process" thread exists but its content was not retrievable **[B]**.

### 2.6 Return offers

- **Historically ~80% for core-dev interns**, with meaningful variance by department: **TechOps
  historically ~60% but ~90% in the most recent Chicago class** **[B]**, from a Blind thread
  (`jump trading ro for interns`, https://www.teamblind.com/post/jump-trading-ro-for-interns-zr48mb1b).
- **The strategically important fact: "most of Jump's new-grad hires are intern converts, and it
  is very rare that they hire a new grad without an internship with them"** **[B/C]**. If true,
  the Jump FT new-grad loop is **not the primary entry path** — the internship is. This is a
  much stronger intern-dependency than anything reported at HRT.
- Context: Jump (with Jane Street) is named among firms that **overhired in 2021–22**, which
  depressed conversion in the following cycles **[B]**
  (https://www.efinancialcareers.com/news/2023/11/prop-trading-hft-internships-full-time-offers).

---

## 3. Side-by-side: the delta in one table

| Axis | **HRT: intern → full-time** | **Jump: intern → full-time** |
|---|---|---|
| **OA** | 3 Q ~LC-medium → **splits by track**: Algo Dev 2 h/3 Q with a >LC-hard third and *all* hidden tests required; SWE CodeSignal GCA 4 Q /600 (~500–560 bar [C]) | QR intern has **no OA** → an OA **appears** at FT (HackerRank "hard DP and graphs" [B], or Codility parsing/simulation for SRE [A]) |
| **Phone** | 1–2 mixed calls → **two dedicated rounds**: one algorithm-free **C++/OS trivia** screen (`inline`, `vector` vs `list`, `malloc`, `sbrk` vs `mmap`, demand paging) [A] + one live-coding | intern behavioural + one technical → **HR/background round first**, then technical screens on **OS, architecture, networks, UB** [B] |
| **Onsite** | 1–2 calls, no documented full-day loop → **4–6 rounds, up to 6.5 h**: TLE-graded coding block, **spec-design-with-changing-requirements**, **pandas/data-science**, systems/OS, probability, fit | campus whiteboard / single technical → **full day 9–5** or 4× 45–60 min, sometimes **two 4-hour days** [B] |
| **What actually gets harder** | **Systems depth + design + performance grading.** "Correct but slow" becomes a fail | **Systems depth only.** Algorithms stay ~LC-medium; **kernel, concurrency, CPU architecture** are the additive delta [B] |
| **Take-homes** | none at intern → **week-long order router** [B, level inferred, not re-verified]; 4–8 h Verilog [B] | none at intern → **order-book take-home** for SWE [A artifact, undated] |
| **Track fan-out** | 3 intern tracks → **many FT tracks** (SWE C++/Python, Core Dev, Algo Dev/QR, Algo Web, Systems/SysTrade/SRE, Data Scientist), each with its own rounds | already team-routed → **loop is assembled per team/track; no single FT loop exists** |
| **Return offer** | volatile by cycle; 2022 class largely no-offer [B]; ~85% claimed for 2025 [C]; **whether returners skip stages: undocumented** | **~80% core dev**, 60–90% TechOps by year [B]; **most new-grad hires are intern converts** [B/C] |
| **Total time** | ≈8–10 h; 4–8 weeks calendar | ~24 days average calendar [B] |

---

## 4. What is confirmed, what is not

**Confirmed against the record:**
- HRT FT Algo Dev OA = 2 h / 3 Q, third harder than LC-hard, all hidden tests must pass. **[B]**
- HRT FT phone screen can be entirely C++/OS trivia with no algorithms; the exact question list
  in the brief traces to one first-hand write-up (`Shivam5022`). **[A]**
- HRT FT onsite 4–6 rounds / up to 6.5 h, including a spec-design round that absorbs changing
  requirements and a pandas/data-science round. **[A/B]**
- Jump QR intern: no OA, three rounds. **[B]**
- Jump FT: "hard DP and graphs" on the OA, interviews not beyond LC-medium, core dev adds
  kernel/concurrency/CPU architecture. **[B]**
- Jump take-home order book is a **full-time** artifact. **[A]**
- Jump's process **does** vary by team. **[B/C]**

**Not confirmed / open:**
- The exact CodeSignal cut score (500 vs 560) — **[C] only**, and a high score demonstrably does
  not guarantee advancement.
- The HRT **week-long order-router take-home**: single Glassdoor report, **level inferred not
  stated**, and **not re-corroborated** this pass.
- Whether HRT **experienced hires skip the OA** — no evidence found.
- Whether HRT **returning interns skip stages** — no evidence found.
- Current frequency of the Jump order-book take-home — artifact is undated and unrepeated.
- All acceptance-rate and return-offer percentages: mutually contradictory across sources.

**Recommended next step given the blocked-egress limitation:** the three highest-value
unretrieved primary sources are the Blind threads
`https://www.teamblind.com/post/hrt-ng-algo-developer-interview-process-x0b1ybun`,
`https://www.teamblind.com/post/hrt-final-round-what-to-expect-algo-dev-summer-internship-8dap6s8j`
(these two straddle exactly the NG-vs-intern Algo Dev delta), and
`https://www.teamblind.com/post/jump-trading-interview-process-swe-k5k5jexb`. Reading those
three would settle most of §1.5 and §2.1. They need a session whose egress policy permits
`teamblind.com`, or manual retrieval.

---

## 5. Source URLs

**HRT — official**
- https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/ (blocked; quoted via search)
- https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/ (blocked; quoted via search)
- https://www.hudsonrivertrading.com/careers/ , https://www.hudsonrivertrading.com/student-opportunities/
- https://github.com/hudson-trading/wwhrt-bookbuilder-workshop (HRT's own Core-Dev-style exercise)

**HRT — forum / first-hand**
- https://www.teamblind.com/post/HRT-core-intern-return-offer-rate-2KdBM4Xc
- https://www.teamblind.com/post/hrt-ng-algo-developer-interview-process-x0b1ybun
- https://www.teamblind.com/post/hrt-final-round-what-to-expect-algo-dev-summer-internship-8dap6s8j
- https://www.teamblind.com/post/HRT-Algo-Engineer-Interview-AKOjp7Ek
- https://www.teamblind.com/post/hrt-algo-dev-programming-interview-6ayycr7u
- https://www.teamblind.com/post/HRT-Algo-Engineer-interview-prep-DwibfAD4
- https://www.teamblind.com/post/what-to-expect-on-an-algo-dev-interview-hrt-63lvv2cz
- https://www.teamblind.com/post/hrt-phone-interview-what-to-expect-zazppqbp
- https://www.teamblind.com/post/hudson-river-trading-hrt-algo-developer-phone-interview-what-to-expect-1nz00wah
- https://www.teamblind.com/post/hudson-river-trading-prescreen-codesignal-yhn0v4o0
- https://www.teamblind.com/post/hudson-river-trading-codesignal-screen-vlf28eew
- https://www.teamblind.com/post/hrt-oa-and-interview-process-85ofa3tc
- https://www.teamblind.com/post/hrt-interview-prep-zv1q21sk
- https://www.teamblind.com/post/hrt-london-interview-experience-RSjBf3ag
- https://www.teamblind.com/post/HRT-full-stack-interview-34r4UucU
- https://www.teamblind.com/post/Hudson-River-Trading-OA-Expectations-uXiLRhfE
- https://www.teamblind.com/post/data-production-engineer-interview-at-hrt-ce1argwz
- https://www.teamblind.com/post/Hudson-Rivers-OA-SDE-Intern-ePuPxWyv
- https://www.glassdoor.com/Interview/Hudson-River-Trading-Interview-Questions-E470937.htm
- https://www.glassdoor.com/Interview/Hudson-River-Trading-Software-Engineer-Interview-Questions-EI_IE470937.0,20_KO21,38.htm
- https://www.glassdoor.com/Interview/Hudson-River-Trading-Algorithm-Engineer-Interview-Questions-EI_IE470937.0,20_KO21,39.htm
- https://www.glassdoor.com/Interview/Hudson-River-Trading-Core-Developer-Interview-Questions-EI_IE470937.0,20_KO21,35.htm
- https://www.1point3acres.com/bbs/thread-926512-1-1.html (HRT CodeSignal)
- https://www.1point3acres.com/interview/thread/816923 (HRT OA – SWE intern)
- https://www.1point3acres.com/bbs/tag/hudson-river-trading-8698-5.html
- https://www.wallstreetoasis.com/company/hudson-river-trading-llc/interview
- https://www.wallstreetoasis.com/forum/trading/hudson-river-trading-algorithm-developer-interviewother-questions
- https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-october-15-2025-no-offer-neutral-bd6da5f3/
- https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-new-york-new-york-november-7-2025-declined-offer-positive-5465b02e/
- https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-united-states-april-1-2025-no-offer-negative-2a2ca5aa/
- https://oneraynyday.github.io/misc/2020/09/30/Interviewing-During-Covid/ (HRT algo-engineer loop, 2020)
- https://news.ycombinator.com/item?id=42576574
- https://github.com/Shivam5022/Interview-Experiences (FT C++ SWE phone screen — the `sbrk`/`mmap` source)
- https://www.efinancialcareers.com/news/hudson-river-trading-intern-pay
- https://www.levels.fyi/internships/Hudson-River-Trading/Software-Engineer-Intern/

**Jump — forum / first-hand**
- https://www.teamblind.com/post/jump-trading-interview-process-swe-k5k5jexb
- https://www.teamblind.com/post/jump-trading-ro-for-interns-zr48mb1b
- https://www.teamblind.com/post/Jump-Trading-Technical-Prep-j7FG8oEp
- https://www.teamblind.com/post/jump-trading-tc-for-industry-hire-ipanq8jr
- https://www.teamblind.com/company/Jump-Trading/posts/jump-trading-interview
- https://www.glassdoor.com/Interview/Jump-Trading-Interview-Questions-E251744.htm
- https://www.glassdoor.com/Interview/Jump-Trading-Quantitative-Researcher-Interview-Questions-EI_IE251744.0,12_KO13,36.htm
- https://www.glassdoor.co.in/Interview/Jump-Trading-Software-Engineer-Interview-Questions-EI_IE251744.0,12_KO13,30.htm
- https://www.1point3acres.com/interview/thread/1026654 (QR intern, no-OA 3-round loop)
- https://www.1point3acres.com/bbs/thread-1086311-1-1.html (SDE FT, HR-first)
- https://www.1point3acres.com/bbs/thread-1088584-1-1.html (QR full-time)
- https://www.1point3acres.com/bbs/tag/jumptrading-8699-1.html
- https://www.wallstreetoasis.com/company/jump-trading/interview
- https://www.wallstreetoasis.com/company/jump-trading/interview/quant-researcher
- https://github.com/stanleywu111/jump-orderbook (FT take-home artifact)
- https://www.jointaro.com/interviews/companies/jump-trading/experiences/software-engineer-united-states-june-24-2025-no-offer-negative-a4879dee/
- https://www.efinancialcareers.com/news/2023/11/prop-trading-hft-internships-full-time-offers
- https://www.levels.fyi/internships/Jump-Trading/Software-Engineer-Intern/

**Platform documentation (for the 600 scale)**
- https://support.codesignal.com/hc/en-us/articles/13408542717079-Understanding-Assessment-Score
- https://support.codesignal.com/hc/en-us/articles/23458723018391-Guide-to-Setting-Cut-Scores
- https://support.codesignal.com/hc/en-us/articles/13260678794775-Converting-Historical-Coding-Score-Thresholds-to-Assessment-Score

**Prior compiled research (this user's own repo)**
- https://github.com/NoctNight/quant-prep-database/blob/main/research/hft_cluster.md

**[C]-tier prep sites consulted, listed for traceability only — do not cite as fact**
- https://www.techinterview.org/companies/hudson-river-trading/ , https://www.techinterview.org/companies/jump-trading/
- https://www.quantt.co.uk/resources/hudson-river-trading-interview , https://www.quantt.co.uk/resources/jump-trading-interview
- https://www.tradermath.org/articles/hudson-river-trading-interview-guide , https://www.tradermath.org/articles/jump-trading-interview-guide
- https://www.quantblueprint.com/guides/how-to-get-a-job-at-jump-trading
- https://spacecomplexity.ai/blog/hudson-river-trading-onsite-interview , https://spacecomplexity.ai/blog/hudson-river-trading-phone-screen-interview
- https://oavoservice.com/en/articles/hrt-oa-2026-codesignal-guide
- https://www.getsmartresume.com/article/hrt-algorithm-development-software-engineering-intern
- https://www.extern.com/post/hudson-river-trading-hrt-internship-guide , https://www.extern.com/post/jump-trading-internship-guide
- https://prachub.com/companies/hudson-river-trading , https://algodaily.com/companies/hudson-river-trading
- https://www.datainterview.com/blog/jump-trading-quantitative-researcher-interview
