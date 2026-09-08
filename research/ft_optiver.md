# Optiver — Full-Time / Graduate / Experienced-Hire Interview vs. the Internship Loop

**Scope:** all offices (Amsterdam, Chicago, Austin, Sydney, Shanghai). Focus is the **delta** from the internship loop, which the reader already knows.
**Research date:** 2026-09-08. Sources weighted 2023–2026.

---

## 0. Sourcing note — read this first (it constrains every claim below)

The network egress proxy in this environment **blocked every direct page fetch**: Glassdoor, Reddit, Blind (teamblind.com), LeetCode Discuss, 1point3acres, Wall Street Oasis, Medium, dev.to, jointaro.com, levels.fyi, builtin.com, spacecomplexity.ai, prachub, quantt, quantvault, interviewquery — and **optiver.com itself**. Confirmed via `curl -sS "$HTTPS_PROXY/__agentproxy/status"`, which logs `connect_rejected … 403 to CONNECT` for those hosts.

What I *could* use:
1. **GitHub over git/API** (worked fully) — two first-hand candidate repos, read end to end.
2. **~30 web searches**, whose engine-side synthesised answers quote the blocked pages. These are second-hand paraphrases; I mark them as such and never present them as verbatim quotes.

So: **the GitHub material is primary/first-hand. Everything else is a paraphrase of a source I could not read directly.** Confidence labels are attached throughout, and a summary confidence table is in §8. The search budget (200 calls) was exhausted at ~30 Optiver searches.

---

## 1. Pipeline: graduate/new-grad SWE loop vs. intern loop

### 1.1 The online assessment — largely the SAME battery, different problem shape

**HIGH confidence — the grad OA structure.** A first-hand GitHub write-up of the **Amsterdam Grad SWE 2023** process gives an exact table:

| Assessment | Questions | Time | Platform | Topics |
|---|---|---|---|---|
| Coding | **2** | **120 min** | HackerRank | LeetCode medium→hard |
| Knowledge test (MCQ) | **10** | **20 min** | HackerRank | OOP concepts |
| Neuro-assessment games | **9 games** | **~1 hr** | **Zap-N** | block building, PIN recall with escalating difficulty |

Source: https://github.com/vijaySadhuram/Optiver-Recruitment-Grad-SWE (repo README, first-hand, 2023)

More recent grad/NG reports (search-summarised from Glassdoor / jointaro / 1point3acres) converge on the same three-part shape with drift in the MCQ count: **2 coding (~2 h) + ~20 MCQ (20 min) + Zap-N (30–60 min)**. Some NG cycles report **3 questions in 90 min**; a 2024 NG cycle reported a **72-hour completion window**; a 2026 NG report describes **one 90-minute low-level design question**. Total advertised OA time across sources: **~3–4 hours**.

**→ DELTA vs intern: essentially none structurally.** Interns get the same HackerRank + knowledge-quiz + Zap-N battery. Multiple guides state flatly that *"the interview is largely the same as for the full-time graduate role."* The differences that do show up are in **problem flavour, not format**:

- Grad/NG problems skew toward **long object-oriented / low-level design simulations** (a 2026 NG OA is described as a single 90-min low-level design question) rather than pure algorithms.
- Intern 2026 OA reports include a **"news subscription system" practical design problem** on HackerRank — so interns get design-flavoured OA problems too. This weakens any claim of a clean grad-only design delta.
- Named OA problems recurring across both levels (from 1point3acres thread titles/summaries): *Worst Trader Reporter*, *Numbers Station*, *number of days between two dates*, *the giving tree*.

**MEDIUM–HIGH — proctoring is now tight, at both levels, and tighter than older intern accounts suggest.** 2026 reports describe the **HackerRank Desktop app**, **webcam + microphone recording**, **screen share**, and **process monitoring on your machine** for the whole session. If your internship mental model is "untimed-ish take-home HackerRank link", that is out of date for 2026 cycles.

**HIGH — language restriction (often surprises full-time candidates).** **Python is not permitted** on the OA coding section. Reported allowed sets: **C++, Java, C#, C, Ruby**; several 2025 grad candidates report only **C++ and Java** in the dropdown. This is a real bite for full-time candidates from Python-heavy backgrounds — and it is the same restriction interns face, so it is a *constraint* rather than a delta.

### 1.2 Zap-N and 80-in-8 — the important correction

- **Zap-N: YES, full-time SWE candidates still take it.** It is in the grad battery (9 games, ~1 hr) and in NG 2026 reports. Not intern-only.
- **80-in-8: NOT a software-engineering assessment at all — at either level.** The cleanest statement found (search-summarised from everythingquant / QuantVault): *software engineers do not take the 80-in-8 mental-math test; they get long object-oriented simulation problems and a CS-knowledge quiz, whereas quant candidates get the 80-in-8 arithmetic screen.* The 80-in-8 belongs to the **trader / QR track**, where it is used at **both intern and graduate level** (see §5).
- **CONFIDENCE: MEDIUM-HIGH.** Prep-farm sources, but consistent across several and consistent with the SWE OA tables above, which never list an arithmetic section. Treat "does my SWE loop include 80-in-8?" as a recruiter question, not a settled fact.
- Note the **trader-track OA sections** that are sometimes confused with Zap-N: **NumberLogic, Beat The Odds** (~30 hard probability questions at ~1.5 min each, no pause), sequences, processing speed, spatial reasoning, reaction time.

### 1.3 Onsite / superday structure

**The canonical full-time superday (MEDIUM confidence, aggregator-sourced but repeated consistently):** four consecutive rounds, **half a day**, feedback within ~a week:

1. **HR / SWE chat**
2. **Technology Fundamentals** — CS depth, *no live coding*: memory models, concurrency primitives, networking stack, OS internals
3. **System Design** — low-latency prompts, back-of-envelope math, unprompted failure-mode discussion expected
4. **Project Deep Dive** — every design decision you made is fair game for **adversarial questioning**

**Reported round counts, and an honest contradiction:**

| Level | Final-round shape | Source quality |
|---|---|---|
| **New Grad SWE** | **2 × 1-hour technicals** (one LC-medium coding/design, one system design) + HR wrap-up | Blind thread summary, MEDIUM |
| **SWE Intern (Amsterdam)** | **3 interviews**: Tech Fundamentals + System & Design + Project Deep Dive | Blind thread summary (older, ~2022), MEDIUM-LOW |
| **Generic "superday"** | 4 rounds as above | Aggregator, MEDIUM |

**⚠️ This contradicts the usual assumption.** At least one credible pairing has the **intern final round with MORE rounds (3) than the new-grad final round (2)**. I could not resolve this — the intern data point is older and Amsterdam-specific, and Optiver's loop clearly varies by office, cycle and headcount. **Do not treat "full-time = more onsite rounds" as established.** What *is* better supported is that the full-time rounds go **deeper**, not that there are more of them.

**Full pipeline, grad/NG, US/EU (MEDIUM):** behavioural phone screen with HR (~20–30 min) → OA (2–4 h) → 1 technical interview (a commonly reported prompt: *design a queue using a circular buffer*) → final round (2 × 1 h technicals). Some Amsterdam grads report **3–4 technical rounds** plus a final behavioural. **Total 3–5 stages, 2–6 weeks**; NG timelines report ~16–22 days. Recruiters push hard on speed — an HR invite can arrive **the day after** the OA.

**Shanghai (MEDIUM-LOW):** reported as **three consecutive technical interviews in one day**, with a local flavour — **Fermi estimation** (e.g. "how many milk-tea shops in Shanghai") and, in the quant-adjacent segment, **implementing Black-Scholes from scratch**. Fermi/derivations do not feature in Western SWE accounts.

**Sydney (MEDIUM, first-hand-attributed):** a May 2026 Glassdoor report describes a virtual HackerRank round with **two engineers observing simultaneously**, video and mic on throughout, probing **space-time complexity and Big-O**, then moving into **computer-systems knowledge and efficiency trade-offs**. Candidates describe it as materially more nerve-wracking than a standard coding interview.

**Career Kickstarter (a full-time side-door worth knowing):** a **five-day, all-expenses-paid** program for STEM students/recent grads (Amsterdam, Sydney; also a Women-in-Tech variant). Entry is via **online assessment → interview**; strong performance can convert to **a direct Graduate Software Engineer offer**, bypassing the standard grad loop. https://www.optiver.com/join-us/students/programs/career-kickstarter/

---

## 2. The C++ / systems delta

**The user's premise is broadly CONFIRMED in direction, with one correction.**

### 2.1 What is confirmed

**HIGH — a dedicated, code-free CS-fundamentals round exists in the full-time loop.** "Technology Fundamentals" drills **memory models, concurrency primitives, the networking stack, and OS internals** with **no live coding**. This is the structural home of the "C++ trivia" the user describes.

Confirmed topic areas across multiple sources:
- **CPU cache behaviour and cache locality** — explicitly named.
- **Struct memory layout and padding/alignment** — explicitly named. A concrete recurring question: *a linked list of 1000 nodes, each holding an `int` and a pointer — how much memory?* Testing `int` = 4 bytes, 64-bit pointer = 8 bytes, and **alignment/padding**; sources state that **ignoring alignment costs you points immediately**. Also tested: that **struct field ordering affects cache behaviour**.
- **Multithreading / concurrency primitives**, including **`notify_all` vs `notify_one`** semantics on `std::condition_variable`, the mutex pairing (check-and-wait must be atomic), spurious wakeups and predicate usage. Also **lock-free data structures**, locking/contention.
- **TCP vs UDP/multicast trade-offs in a trading context** — explicitly named as an Optiver question.
- **"Write your own vector"** — reported as a known Optiver C++ question (search-summarised; the underlying page is Glassdoor's C++ Developer filter, which I could not read directly). **MEDIUM confidence.**
- **Memory allocation, pointer semantics, "how it works under the hood"**, and *"when a naive implementation becomes a performance liability."*
- Prep guidance repeatedly names: **concurrency, lock-free programming, STL internals, static polymorphism, smart pointers, and how CPUs work (memory architecture, caches).**

**HIGH — C++ fluency is an asymmetric advantage at full-time level.** *Optiver's production systems are C++, and interviewers notice candidates who can discuss memory layout and cache behaviour.* Nothing equivalent is said about the intern loop.

### 2.2 Where I could NOT confirm the user's list

- **TLB specifically:** one aggregator (spacecomplexity, blocked) is summarised as naming **"CPU cache and TLB"** among tested topics. That is a **single, blocked, aggregator-grade source**. **LOW-MEDIUM confidence.** Cache: solid. TLB: plausible, unverified.
- **vtable / virtual dispatch specifically:** **NOT confirmed.** A search targeted directly at this returned: *"the search results don't specifically mention 'virtual table' questions."* Virtual-function overhead is a standard HFT-C++ topic and is tested at peer firms (HRT, Jump, Citadel Securities, Tower, Radix, DRW), but I found **no Optiver-attributed vtable question**. Prepare it — it is cheap — but the evidence is inferential.
- **Branch prediction / false sharing:** same status as vtable — named as generic low-latency-firm C++ topics, **not Optiver-attributed** in anything I could reach.

### 2.3 The system-design delta (the clearest full-time change)

**HIGH-ish.** For full-time, system design is **its own graded round** with a **low-latency, trading-specific** prompt set — not a light verbal chat:

- *"Design a system that aggregates market data from multiple exchange feeds and distributes it to trading algorithms with minimal latency."*
- Real-time **order management system**; **market-data distribution pipeline**; **risk engine evaluating positions in under a millisecond**; **order allocation**; **leaderboard under strict performance constraints**.
- A 2026 NG report: two real-time streams (inventory + order) → design a **leaderboard service pushing profitable orders in real time, sorted by profit**.
- Expected knowledge: **ring buffer vs queue and when each wins**, **kernel bypass** and when its operational complexity is justified, **when vertical scaling is the correct answer** at trading-system scale.
- **Back-of-envelope latency/throughput/memory math is expected on the fly, and you must defend the numbers when pushed.**

**→ DELTA:** the intern "system design conversation with no code" becomes, at full-time, a **defended architecture round with quantitative constraints and unprompted failure-mode analysis**. Sources note explicitly: *for experienced hires, system design expectations are higher, and production systems you have built under real constraints carry more weight than academic projects.*

**Recurring full-time coding/design artefacts** (as opposed to pure LeetCode): **circular-buffer / array-backed queue implemented without resizing**, **LRU cache**, **priority heaps**, **order-management and subscription-style systems**, **merge N sorted lists**, **max-profit-k-transactions**, **days between two dates**.

---

## 3. The experienced-hire loop — first-hand, in detail

**This is the strongest evidence in the whole report: a candidate's own live prep repo, updated *during* the process, quoting recruiter emails and recruiter-collated written feedback.**

**Source:** https://github.com/ErrolMc/OptiverInterviewPrep
**Role:** **Principal C# Software Engineer, Optiver Sydney** (APAC HQ), 2026. Windows desktop trading GUIs — WPF/WinForms/XAML, MVVM, async, threading, profiling — surfacing real-time trading data to traders and researchers.

### 3.1 The five rounds

| # | Round | Format | What it actually grades |
|---|---|---|---|
| 1 | **Coding** | ~60 min, **Zoom + HackerRank in parallel**, one Optiver engineer watching and talking throughout | **One in-depth problem**, not a multi-problem test. **No MCQs.** Reasoning aloud, clarifying questions, complexity, edge cases, **debugging speed**. Most likely a **graph/traversal** problem (parse → build → traverse; cycles; multiple paths). **AI not permitted.** |
| 2 | **Design** | **~90 min, verbal, NO whiteboard** | *"Design a real-time UI that ingests huge amounts of data per second."* Graded core = **UI rendering + aggregation/coalescing**; backend is bonus. Requirements-first; justify every decision; **evolve the design when pushed**; physical-constraint awareness (GC, single UI thread, network). **Fault tolerance + backpressure explicitly called out as "very important in a high-stakes live trading app."** They probe **performance/memory optimisation and *which tools* you use**. |
| 3 | **Experience Review** | ~60 min, with a **senior engineer / Head of Engineering** | Invite wording: *"we'll be keen to find out more about you from a technical point of view — your work experience, projects, problems you've solved, technical decisions."* Verbatim probe: **"Why did you make this design decision?"** plus rejected alternatives and **"I" vs "we"** individual contribution. |
| 4 | **Behavioural** | — | Decision quality, **learning velocity ("what *changed* in your thinking")**, collaboration, **authentic** motivation. |
| 5 | **Final (CTO)** | — | Casual fit + elevator pitch; *"often blurs into a design/project tangent."* |

### 3.2 Structural deltas vs. the campus loop

1. **No OA. No superday.** There is **no HackerRank take-home battery, no MCQ quiz, no Zap-N** in this loop. It opens directly on a **live coding interview**.
2. **Rounds are STAGED, not batched.** The recruiter scheduled the coding round first; **each subsequent round is only scheduled after you pass the previous one** ("Coding and Design rounds are passed. Your next step is an Experience Review"). This is a sequential gauntlet over weeks, versus the campus half-day. It also means **you get a pass/fail signal at every step**.
3. **Two rounds have no campus equivalent:** the **Experience Review** (a technical CV walk, distinct from behavioural) and a **final CTO round**.
4. **Design is 90 minutes and deliberately verbal** — *"they assess how you explain a complicated system without a visual reference; delivery is half the score."* An intern's "verbal system design with no code" is a lighter version of the same instinct; here it is a **90-minute defended architecture round**.

### 3.3 How the Experience Review is graded (recruiter-collated, first-hand)

Read as **one round on two axes**, both scored simultaneously:

- **Axis 1 — technical judgement:** did you *drive architecture and own ambiguous problems end-to-end*, or merely describe a system?
- **Axis 2 — trust/values:** the Head of Engineering spends the hour answering **"Would I trust this person to represent my team?"**

Four named behavioural themes: **Collaboration** (you'll sit with traders and researchers), **Communication** (*explain the trade-off, not just the verdict*; don't sound overly technical), **Conflict resolution** (they want *maturity*, not "I've never had conflict"; be willing to say you were wrong), **Technical leadership** (expected of a senior hire **even without direct reports** — mentoring, raising the bar, building systems that make others productive).

**Six explicit scoring signals:** calm under pressure · collaborative not argumentative · **gives *and* receives** feedback · influences without authority · passionate about quality · **takes ownership rather than waiting for direction**.

Two near-certain questions: **"Why leave [current employer]?"** (reframe as a pull, not an escape from bureaucracy/politics/money) and **"Why Optiver?"** (performance engineering, real-time systems, exceptional peers, ownership, immediate feedback, tools traders use directly — *not* money or "HFT is cool").

### 3.4 Other experienced-hire accounts (thinner, all search-summarised)

- **Senior SWE (India, Nov 2024)** — jointaro, negative outcome. Reported as **one screening coding round + four further coding rounds + a 1:1 with HR**. If accurate, that is a **coding-heavier, less design-heavy** senior loop than the Sydney one — plausibly a different office/team convention.
- **Senior Data Engineer (Shanghai, Jul 2025)** — jointaro, neutral/no offer: **HR phone screen → 1-hour online coding → onsite**. Praised as "professional and well-organised."
- **Senior SWE generally:** Glassdoor difficulty **3.2/5**; *"difficulty scales with level; senior roles add deep system design and performance optimisation."* Some senior/specialised roles use a **practical or take-home assignment** — pipeline design, data validation, structured analysis — **instead of** algorithmic puzzles.
- **Notable full-time opener:** *"Unlike many tech interviews that start with coding questions, Optiver's first round kicked off with an in-depth dive into technical projects."*
- **Sydney bar:** the Low Latency Execution Systems Engineer (C++) posting requires **5+ years on performance-critical high-throughput or low-latency systems**.

---

## 4. How grading differs at full-time level

### 4.1 Speed and adaptability are graded, explicitly — and they are what cut people

**HIGHEST-value finding, first-hand.** The ErrolMc repo distils **written feedback on 3–4 candidates who failed the technical stages**, collated by the recruiter. Verbatim fragments:

> *"iteration speed… below expectations"*
> *"progress on the problem was very slow"*
> *"execution speed below the level required"*
> *"spent a significant portion resolving **basic coding and parsing issues**"*
> *"**debugging efficiency**… below expectations"*
> *"required some prompting to move toward a suitable approach"*
> *"**limited ability to adapt as requirements became more complex**"*

And on the recurring technical theme:

> *"focused heavily on algorithm design and **graph/data structure concepts**… struggled to extend to more complex **traversal scenarios and edge cases**"*
> *"awareness of **graph traversal** concepts… struggled to develop a coherent/scalable solution… **loops and multiple paths**"*
> *"made a solid start on **parsing and handling direct conversions**"* — then couldn't extend it

The repo's own conclusion: **"Nobody failed for not knowing a fancy pattern. They failed for being slow."**

**→ Is speed weighted more heavily at full-time? YES, on this evidence.** Two distinct sub-signals, both graded:
- **Raw execution speed on the boring parts** — input reading, parsing, building the data structure, debugging. Time lost here is scored against you.
- **Adaptability under escalation** — the interviewer *deliberately escalates* ("now handle cycles", "now there are multiple paths", "now this case too"). You are graded on **evolving a working solution, not rewriting it**. Corroborated independently: *"later rounds focus on depth, correctness, and adaptability, with interviewers potentially changing assumptions mid-problem or introducing new constraints. **Speed is only rewarded when paired with clean reasoning and valid assumptions.**"*

**The method Optiver rewards (from their own guidance, per the repo):** ① get a working solution **fast** → ② demonstrate correctness (test it, walk edge cases) → ③ **then** iterate and optimise → ④ explain trade-offs and what you'd do with more time. Their stated **#1 candidate mistake is architecting the "perfect" solution upfront and running out of time.** **Do not over-engineer** — they want engineering judgement, not design-pattern bingo. Optimisations worth *naming aloud* even unimplemented (naming = signal): reducing allocations, algorithmic complexity, concurrency/threading, caching/memoisation, reducing locking/contention, better data structures, hot-path latency, edge cases, test coverage.

### 4.2 The seniority-specific rejection axis: ownership vs. maintenance

**First-hand, verbatim, from the written feedback on a rejected candidate** who *communicated well* and was still cut:

> *"…did not see enough evidence of the level of **technical ownership, architectural decision-making, and technical leadership**… examples tended to focus on **implementing or improving existing solutions** rather than navigating ambiguous technical problems, driving architectural direction, or leading complex initiatives from conception through delivery."*

This failure mode **cannot exist in an intern loop** — interns have no architecture to have owned. The repo's own filter:

| ❌ Sinks you (reads as mid-level) | ✅ Signals senior/principal |
|---|---|
| "I optimised a slow query / improved an existing service." | "I owned the architecture of X from a blank page through to production." |
| "**We** decided to…" (invisible individual contribution) | "**I** proposed and drove the decision to… over the alternative of… because…" |
| "The requirements were given to me and I built it." | "The problem was ambiguous — I framed it, aligned stakeholders, set the technical direction." |
| A story ending at "it shipped." | A story ending at "…and here's what I'd do differently / what it changed in how I think." |

### 4.3 The OA code-style scoring claim

**PARTIALLY CONFIRMED; the specific numbers are NOT.**

Confirmed (search-summarised, MEDIUM):
- **Every HackerRank submission is reviewed by an engineer before you advance** — **code quality is assessed directly, not just test pass rate.**
- Reviewers weigh **time and space complexity, readability, code quality, reusability**, and whether the solution is **overfitted to the visible tests**.
- **Hidden tests:** on final submission the code runs against **~100× more cases** than you saw.
- **Optiver publishes no pass threshold**; a strong score is explicitly not a guarantee of advancing.
- One report: *"a self-reported 90 percent score on the older eight-question test still ended in rejection."*
- A Blind thread exists titled *"rejected by optiver hackerrank after every single test case passes"* (blocked; title-level evidence only).

**NOT confirmed:** the paired **"90% rejected while 77.8% progressed"** comparison. I found the 90%-rejected half; I found **nothing** for 77.8%, and the two are not linked in any source I could reach. **Treat the pairing as unverified.** The defensible version of the claim is: *pass rate is necessary but not sufficient; a human engineer reads your code and scores style, complexity and generality, so a clean 78% can beat an ugly, test-overfitted 90%.* That mechanism is well supported; the exact figures are not.

**Also worth knowing about the FT rejection channel:** a LeetCode Discuss NG SWE 2024 (Chicago) write-up reports rejection two working days after the final round with an explicit *"we cannot give you reasons"* email — and the candidate later learned from recruiters at a career fair that **Chicago had stopped hiring SWE**, i.e. **headcount, not performance**. Optiver's loop has **more interviewer discretion than a rubric-driven process** (*"people doing the culling rather than objective assessments"*), so full-time rejections are noisier and less legible than intern ones. Full-time headcount is finite and team-specific; intern classes are sized in advance.

---

## 5. Quant Trader / Quant Researcher — full-time vs. intern

**The headline: for traders, the intern and graduate loops are the most similar of any track.** *"The interview is largely the same as for the full-time graduate role."* The 80-in-8 is not a full-time-only gate — it screens both, and it is described as **the hardest mental-arithmetic test in the industry**.

**The 80-in-8 itself:** 80 arithmetic questions in 8 minutes, no calculator — fractions, decimals, percentages, multi-step. **Most candidates 30–50; strong candidates 60+.** Community-reported pass line ~**55 net**, ~**70+** competitive. (Note: the 55/70 numbers come from a prep-farm source — **LOW-MEDIUM confidence** — and are inconsistent with "most score 30–50", so treat them as folklore.)

**The reported 7-stage loop covering both tracks (MEDIUM):** Online Assessment → Trading/Betting Game (Tech 1 & 2) → HR/Behavioural → Technical/Brain-Teaser (QR) → **Take-Home Data Project + Deep-Dive (QR)** → **Market-Making Game Day (QT)** → Final culture-fit.

**Trader-track OA sections:** 80-in-8, **NumberLogic**, **Beat The Odds** (~30 hard probability questions, ~1.5 min each, no pause between), **sequences** (arithmetic, geometric, two interleaved patterns, differences-of-differences, prime-based — *"reward flexible searching, not a memorised rule"*), plus **processing speed, spatial reasoning, reaction time**.

### What changes for GRADUATE traders vs interns

**MEDIUM confidence — the delta is depth and format, not gatekeeping.** Same 80-in-8, same reaction games, same probability. What gets added at the graduate final/superday:

- **Market-making simulation with real adverse selection.** You price a hidden quantity (e.g. the sum of face-down cards) and quote two-sided; the interviewer **or a competing group of candidates** trades against you. Graded on: **how you react to bad fills, whether you update prices, whether you manage inventory, and whether you communicate clearly under pressure.**
- **Group/competitive rounds:** groups of 3, very short time, challenging questions — you compete against other interviewees on the same day.
- **Options pricing theory** enters properly (not just probability).
- A reported superday block: **45 min behavioural → 30 min technical → 15 min behavioural**, with 1 HR person and a trader; technical content = **expected value / probability and finding risk-free arbitrage**.
- **→ The real change from the intern loop is the shift from "can you compute fast" to "can you make and defend prices, manage risk, and stay coherent while being adversely selected in front of competitors."**

### What changes for EXPERIENCED traders

**LOW confidence — genuinely thin data.** Reported: **OA (4 sections) → HR call that is a deep CV dive** where *"you should know your past experience very well to answer every follow-up question."* Candidates still describe receiving **separate challenges for sequences, probability (hard) and coding**. **No source I could reach describes a lateral trader loop that skips the OA.** Assume the quantitative gates persist and a **CV/track-record deep-dive is layered on top** — the trader analogue of the SWE Experience Review.

### Quant Researcher, full-time

**MEDIUM.** Loop: **OA (4 rounds) → HR behavioural → ~90-min technical with a QR → final day including a take-home.**
- **The take-home data project is the centre of gravity:** an **algo-trading dataset**; you build and **backtest a strategy**. Critically, it is **graded on realised profit, not R²** — *a clean linear model is enough to pass.*
- **~2 days after submission**, a **presentation / deep-dive** where they **probe methodology hard**, with heavy follow-ups on **pandas and time-series handling**.
- **Coding is minimal and secondary** to logical structure and correctness.
- Graduate QR is the **standard entry point for PhDs**; some BS/MS hires enter computational-research-flavoured roles. Standing themes: **time-series forecasting, signal extraction, feature engineering**; researchers who can **rewrite Python prototypes in production C++** are explicitly said to get outsized influence.
- **→ vs the intern QR loop, the added stage is the take-home + adversarial methodology defence.** The user's "intern QT loop = 80-in-8, reaction games, probability, no coding" holds for QT; **QR at full-time definitely has coding and a real research artefact.**

---

## 6. Return offers and intern-to-full-time conversion

- **Return-offer rate: ~70–80%** (community estimates, applied across tracks including SWE). Described as **comparable to Citadel, slightly below Jane Street**. **MEDIUM-LOW confidence** — these are forum aggregates, not company figures.
- **The decision is made in the final two weeks** of the internship, based on **manager and team feedback, what you shipped or traded, how you collaborated, and — for traders — continued performance on the trader test.** Note that last item: **the trader test keeps being administered during the internship**; conversion is not purely project-based.
- **Do returning interns skip stages? UNKNOWN — and I want to be explicit that I could not confirm it either way.** A search aimed squarely at this returned no evidence of a formal accelerated path. What the sources do say is that conversion is **performance-review-driven, not interview-driven** — the internship itself functions as the evaluation, which implies a return offer generally arrives **without re-running the loop** rather than via a shortened loop. **Treat "returning interns skip stages" as unverified.**
- **A separate direct route:** **Career Kickstarter** (5-day program) can produce a **direct Graduate SWE offer** without the standard grad pipeline.
- **US campus recruiting:** Optiver aims to give feedback **within one week** post-interview, and tells candidates to flag competing-offer deadlines to their recruiter for an expedited decision.

---

## 7. What full-time candidates get rejected for that interns don't

Ordered by evidence strength.

1. **Insufficient technical ownership / architectural leadership.** *(FIRST-HAND, verbatim written feedback.)* The single most seniority-specific cut. "I improved an existing system" is disqualifying at principal level. **Structurally impossible as an intern rejection reason.**
2. **Iteration and execution speed below the level required.** *(FIRST-HAND, verbatim.)* Includes time lost to **parsing, basic coding, and inefficient debugging**. Interns are graded on potential; full-time candidates are graded against a **production throughput expectation**.
3. **Failure to adapt as the interviewer escalates requirements.** *(FIRST-HAND, verbatim: "limited ability to adapt as requirements became more complex"; "required some prompting to move toward a suitable approach".)* Needing to be led is itself a negative score.
4. **Shallow system design — no back-of-envelope numbers, no unprompted failure modes.** Full-time system design must be **defended quantitatively**; *for experienced hires, expectations are higher and production systems outweigh academic projects*.
5. **Can't defend past design decisions under adversarial questioning.** The **Project Deep Dive** / **Experience Review** has no intern analogue with real stakes — interns are asked about coursework; full-timers are asked *"why did you make this design decision, and what did you reject?"* with **"I" vs "we"** scrutiny on individual contribution.
6. **Weak CS-fundamentals depth without the crutch of coding.** The code-free Technology Fundamentals round punishes candidates who can pass LeetCode but can't reason about **memory layout, alignment, cache behaviour, concurrency primitives, or TCP-vs-multicast**.
7. **Culture/trust failure at senior level.** *"Would I trust this person to represent my team?"* — scored via conflict maturity, giving **and receiving** feedback, influence without authority. An intern is not being assessed as a future team representative.
8. **Headcount, not performance.** *(LeetCode Discuss, NG SWE 2024 Chicago.)* Full-time reqs are team- and office-specific and can close mid-cycle; intern classes are sized ahead. This produces the characteristic Optiver full-time rejection: **a clean process, a fast "no", and an explicit refusal to give reasons.**
9. **Inauthentic motivation.** "Why Optiver?" answered with money or generic HFT enthusiasm. Graded harder when you're leaving an existing job, because **"why leave?"** is asked alongside it.

---

## 8. Confidence summary

| Claim | Confidence | Basis |
|---|---|---|
| Experienced-hire Sydney loop = Coding / Design / Experience Review / Behavioural / CTO, staged sequentially, **no OA** | **HIGH** | First-hand repo quoting recruiter emails |
| Verbatim rejection feedback: "iteration speed below expectations", "limited ability to adapt as requirements became more complex", ownership-vs-maintenance cut | **HIGH** | First-hand, recruiter-collated written feedback |
| Design round = 90 min, **verbal, no whiteboard**, backpressure + fault tolerance graded | **HIGH** | First-hand (from the coding interviewer) |
| Grad OA = 2 coding/120 min + 10 MCQ/20 min + Zap-N 9 games/1 hr | **HIGH** | First-hand GitHub repo (Amsterdam 2023) |
| Python banned on OA; C++/Java/C#/C/Ruby only | **HIGH** | Multiple independent reports |
| Full-time SWE candidates still take **Zap-N** | **HIGH** | Grad OA tables + 2026 NG reports |
| **SWE candidates do NOT take 80-in-8** (it is trader/QR, at both intern and grad level) | **MEDIUM-HIGH** | Consistent across guides; absent from every SWE OA table |
| Superday = HR chat / Tech Fundamentals / System Design / Project Deep Dive | **MEDIUM** | Aggregators, repeated consistently |
| Cache, struct padding/alignment, concurrency, TCP-vs-multicast tested | **MEDIUM-HIGH** | Multiple sources; concrete question reported |
| "Write your own vector" asked | **MEDIUM** | Single blocked Glassdoor-derived summary |
| **TLB** specifically tested | **LOW-MEDIUM** | One blocked aggregator |
| **vtable** specifically tested | **LOW / unconfirmed** | Explicitly absent from targeted search; peer-firm topic |
| OA judged on code quality by a human, not just pass rate | **MEDIUM** | Multiple guides |
| "90% rejected vs 77.8% progressed" | **UNVERIFIED** | 90%-rejected half found; 77.8% not found anywhere |
| Return-offer rate 70–80% | **MEDIUM-LOW** | Community aggregate |
| Returning interns skip stages | **UNVERIFIED** | No evidence either way |
| FT final round has *more* rounds than intern final | **CONTRADICTED** | NG reported at 2; intern Amsterdam reported at 3 |
| Experienced *trader* loop specifics | **LOW** | Very thin data |

---

## 9. Sources

**First-hand (read directly, in full):**
- https://github.com/ErrolMc/OptiverInterviewPrep — Principal C# SWE, Sydney, 2026. Live prep repo with recruiter emails and collated written rejection feedback. Key files: `README.md`, `docs/interview-feedback.md`, `docs/coding-round.md`, `docs/experience-review-cheatsheet.md`, `docs/design-interview-cheatsheet.md`, `docs/resources.md`
- https://github.com/vijaySadhuram/Optiver-Recruitment-Grad-SWE — Grad SWE, Amsterdam, 2023. OA structure table.
- https://github.com/sin-x/HackerRank-FPGA-Interview — Optiver FPGA engineer HackerRank solutions (adjacent track, not analysed in depth).

**Cited via search summaries only — direct fetch blocked by the egress proxy:**
- Optiver official: https://optiver.com/working-at-optiver/career-hub/optiver-interview-tips-for-software-engineers/ · https://www.optiver.com/join-us/students/programs/career-kickstarter/ · https://optiver.com/working-at-optiver/career-hub/us-campus-recruiting-faqs-2/ · https://www.optiver.com/insights/technology-blog/navigating-performance-challenges-as-a-c-software-engineer-at-optiver/ · https://www.optiver.com/insights/technology-blog/data-visualisation-at-optiver-streamlining-trading-decisions/
- Glassdoor: https://www.glassdoor.com/Interview/Optiver-New-Grad-Software-Engineer-Interview-Questions-EI_IE243355.0,7_KO8,34.htm · https://www.glassdoor.com/Interview/Optiver-Graduate-Software-Engineer-Interview-Questions-EI_IE243355.0,7_KO8,34.htm · https://www.glassdoor.com/Interview/Optiver-Senior-Software-Engineer-Interview-Questions-EI_IE243355.0,7_KO8,32.htm · https://www.glassdoor.com/Interview/Optiver-Software-Engineer-Intern-Interview-Questions-EI_IE243355.0,7_KO8,32.htm · https://www.glassdoor.com/Interview/Optiver-Interview-Questions-E243355.htm?filter.jobTitleExact=C+++Developer · https://www.glassdoor.com/Interview/Optiver-Quantitative-Trader-Interview-Questions-EI_IE243355.0,7_KO8,27.htm
- LeetCode Discuss: https://leetcode.com/discuss/interview-experience/4126574/Optiver-New-Grad-SWE-2024-(Chicago)-Interview-Process-Rejection/
- Blind: https://www.teamblind.com/post/Optiver-SWE-New-Grad-Final-Round-0W7JM5E4 · https://www.teamblind.com/post/Optiver-final-round---SWE-Internship-Y4zsXiGU · https://www.teamblind.com/post/Optiver-Behavioral-Interview-New-Grad-SWE-50iw5Ah1 · https://www.teamblind.com/post/rejected-by-optiver-hackerrank-after-every-single-test-case-passes-se5p18zz · https://www.teamblind.com/post/whats-the-most-common-reason-for-optiver-rejection-lrjduk02 · https://www.teamblind.com/post/optiver-career-kickstart-tech-interview-experience-dry34mr7
- 1point3acres: https://www.1point3acres.com/bbs/thread-925103-1-1.html (Graduate SWE) · https://www.1point3acres.com/bbs/thread-1005754-1-1.html (2024 NG OA) · https://www.1point3acres.com/bbs/thread-1135844-1-1.html (26 NG SDE OA) · https://www.1point3acres.com/bbs/thread-928000-1-1.html (NG 72-hour OA) · https://www.1point3acres.com/bbs/thread-1140149-1-1.html (2026 SWE intern OA) · https://www.1point3acres.com/bbs/thread-1087120-1-1.html (SDE intern AMS OA + HR + system design) · https://www.1point3acres.com/bbs/thread-1010313-1-1.html (最全总结 intern OA)
- Taro (jointaro.com): https://www.jointaro.com/interviews/companies/optiver/experiences/senior-software-engineer-india-november-5-2024-no-offer-negative-c1223406/ · https://www.jointaro.com/interviews/companies/optiver/experiences/senior-data-engineer-shanghai-shanghai-july-15-2025-no-offer-neutral-9bc37215/ · https://www.jointaro.com/interviews/companies/optiver/experiences/graduate-software-engineer-amsterdam-february-18-2025-no-offer-neutral-729f70b8/ · https://www.jointaro.com/interviews/companies/optiver/experiences/swe-new-grad-amsterdam-may-14-2025-no-offer-positive-a86313f2/ · https://www.jointaro.com/interviews/companies/optiver/experiences/graduate-software-engineer-united-kingdom-october-14-2025-no-offer-neutral-df447466/ · https://www.jointaro.com/interviews/companies/optiver/experiences/software-engineer-october-20-2025-accepted-offer-positive-8e21bf57/ · https://www.jointaro.com/interviews/companies/optiver/experiences/software-engineer-internship-united-states-november-6-2025-no-offer-negative-97414d3e/
- Wall Street Oasis: https://www.wallstreetoasis.com/company/optiver/interview · https://www.wallstreetoasis.com/company/optiver/interview/graduate-trader-0 · https://www.wallstreetoasis.com/forum/trading/optiver-interview-process
- Medium / dev.to: https://medium.com/@arpitjay099/what-i-learnt-after-interviewing-at-optiver-38f942d202ef · https://medium.com/@yourhome1106/optiver-sde-interview-experience-2026-3-rounds-6c3b6f85976c · https://dev.to/net_programhelp_e160eef28/optiver-ng-sde-interview-full-process-review-oa-3-technical-rounds-hfk
- Guides/aggregators (lowest evidential weight; several carry "may be inaccurate / not affiliated" disclaimers): https://spacecomplexity.ai/blog/optiver-onsite-interview · https://spacecomplexity.ai/blog/optiver-software-engineer-interview · https://spacecomplexity.ai/blog/optiver-behavioral-interview-questions · https://www.interviewquery.com/interview-guides/optiver-software-engineer · https://quantvault.org/optiver-interview-process.html · https://quantvault.org/optiver-online-assessment.html · https://www.quantt.co.uk/resources/optiver-interview · https://www.quantt.co.uk/resources/optiver-internship · https://everythingquant.com/guides/software-engineering-at-optiver/ · https://everythingquant.com/guides/quantitative-trading-at-optiver/ · https://everythingquant.com/guides/quantitative-research-at-optiver/ · https://www.techinterview.org/companies/optiver-interview-guide/ · https://www.techprep.app/blog/optiver-interview-process · https://prachub.com/companies/optiver/positions/software-engineer · https://www.extern.com/post/optiver-internship-guide · https://interviewfox.ai/interview-questions/optiver-oa-hackerrank-guide/ · https://newsletter.pragmaticengineer.com/p/optiver
