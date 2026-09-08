# HRT (Hudson River Trading) — What actually happens in the first technical interview

Research date: 2026-09-08. ~32 web searches.

---

## 0. READ THIS FIRST — access limitations and sourcing discipline

**What I could actually fetch in full (verbatim, high confidence):**

| Source | Status |
|---|---|
| `raw.githubusercontent.com` (GitHub raw markdown) | ✅ FULL TEXT RETRIEVED |

Everything else was **blocked at the network egress proxy**. I confirmed blocks on:
`hudsonrivertrading.com`, `teamblind.com`, `1point3acres.com`, `1o24bbs.com`, `leetcode.com`,
`news.ycombinator.com`, `jointaro.com`, `reddit.com`, `techinterview.org`,
`webcache.googleusercontent.com`, `web.archive.org`. `curl` through the proxy also 403s.

So for Blind / Glassdoor / LeetCode / 1point3acres / jointaro / HRT's own blog I have
**search-engine summaries only**. Those summaries are generally quoting real post text, but I
could not verify wording, date, or that the summarizer didn't blend two posts. I mark these
**[SUMMARY-ONLY]**.

**Labels used below:**
- **FIRST-HAND (verified)** — I read the candidate's own words in full.
- **FIRST-HAND [SUMMARY-ONLY]** — a specific, identifiable candidate post exists at a URL I can
  cite, but I only saw a search-engine summary of it.
- **OFFICIAL [SUMMARY-ONLY]** — HRT's own words, reached only via search summary of hrtbeat.
- **PREP-SITE** — a prep company asserting something. **Treat as unverified marketing.**

**Prep sites polluting this niche** (all appeared repeatedly, all appear to be AI-generated and
to copy each other): spacecomplexity.ai, techinterview.org, techprep.app, quantt.co.uk,
tradermath.org, hackerprep.io, prachub.com, myntbit.com, dataford.io, codejeet.com,
ghostinterview.co, quantblueprint.com, extern.com, linkjob.ai, oavoservice.com, programhelp.net,
coditioning.com, nodeflair.com. **I did not use any of these as a basis for a factual claim.**
Also: `sumitsingh4411/interview-rounds` on GitHub has five "hudson-river-trading-N.md" files —
I checked one and it is **generated/curated filler** ("source: curated", a fake full-stack React
loop). Discard it. Same for `NagarjunMa/Linux-Learning/HRT-Interview-Prep` (AI-written prep).

---

## 1. THE HEADLINE ANSWER — resolving the tension

**Both things are true, and the confusion comes from treating "the first technical interview" as
one fixed thing. It is not. HRT has two *named, structurally different* technical round types,
and which one you get first depends on your role, your track, and to a lesser degree the year.**

HRT's own blog names them (OFFICIAL [SUMMARY-ONLY], `hrtbeat/interview-at-hrt`):

> **"Technical Discussion"** — "usually a 45 minute discussion around one of the following
> topics: Knowledge of Systems / Data Structure / Problem Solving."
>
> **"Programming"** — "tests your programming skills more specific to the team you're
> interviewing for. For certain roles, you'll be asked to program in either C++ or Python, while
> others will give you the choice to pick any language you're comfortable with."

And the overall shape (OFFICIAL [SUMMARY-ONLY], same post):

> "At a high level, you can expect a take-home test, roughly two phone interviews, and a full day
> of back-to-back 'onsite' interviews (that can be conducted virtually or onsite)."

So: **OA → phone #1 → phone #2 → onsite.** The two phone rounds are usually *one of each type*.
The "pure C++/OS conceptual trivia with no algorithms" reports and the "CoderPad live coding"
reports are describing **different rounds of the same pipeline** — and the order is not fixed.

### The decisive evidence that the order varies

- **FIRST-HAND [SUMMARY-ONLY]** — jointaro, SWE, US, **October 15 2025**: process was
  **"OA → Coding Interview → CS Fundamentals Interview."** Coding came FIRST, fundamentals
  SECOND. Question in the coding round: *"write a program for a tic-tac-toe-like game."* He was
  rejected at the CS Fundamentals round, and says he failed it "due to the interviewer getting
  several facts about the C++ language wrong."
  https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-october-15-2025-no-offer-neutral-bd6da5f3/
- **FIRST-HAND [SUMMARY-ONLY]** — Blind, Algo Developer: *"1st phone consists of a quick CV
  walkthrough, then a couple of basic maths and stats brainteasers. The 2nd phone is mostly
  algorithm questions (no actual coding)."* → for this track NEITHER phone round has coding.
  https://www.teamblind.com/post/hudson-river-trading-hrt-algo-developer-phone-interview-what-to-expect-1nz00wah
- **FIRST-HAND [SUMMARY-ONLY]** — 1point3acres, HRT **Data Engineer round 1**: *"the interviewer
  provided a CoderPad and asked to code in Python."* → CoderPad IS round 1 for that role.
  https://www.1point3acres.com/bbs/thread-949902-1-1.html
- **FIRST-HAND [SUMMARY-ONLY]** — Blind, Algo Engineer: title is literally *"HRT (Hudson River
  Trading) Algo Engineer **2nd Round** CoderPad Interview"*, and the post says the CoderPad round
  is "45–60 minutes… immediately after the initial 45 minute phone interview."
  https://www.teamblind.com/post/HRT-Hudson-River-Trading-Algo-Engineer-2nd-Round-CoderPad-Interview-uH03BvKD

### The single best explanation of *why* it varies — from a candidate, not a prep site

**FIRST-HAND [SUMMARY-ONLY]** — Blind, HRT Algo Web Engineer thread. This is the cleanest
statement I found anywhere:

> "For the phone screening rounds, **if coding is involved, they'll explain some complicated
> system or data structure that you'll discuss implementing then you will implement it. If not
> coding, then it will be a typical behavioral/experience interview with typical
> probability-type brainteasers.** … Your recruiter will have the most relevant info for you and
> **will let you know what the focus and structure of each round will be beforehand.**"
>
> https://www.teamblind.com/post/HRT-Algo-Web-Engineer-Interview-Au8BSKNX

**Practical consequence: the recruiter tells you which type your round is. Ask.** Multiple
candidates report recruiter emails naming the format explicitly (see §4).

### Verdict on the hypotheses you posed

| Hypothesis | Verdict |
|---|---|
| (a) two separate early rounds, one conceptual one coding | **YES — this is the main answer.** Confirmed by HRT's own two round names and by the Oct-2025 "Coding Interview → CS Fundamentals Interview" report. |
| (b) conceptual questions happen inside a CoderPad session anyway | **PARTLY.** Some rounds mix them (LeetCode 4261724: vector internals + malloc/swap *and* an LRU-cache question in one 45-min call). But the purest conceptual rounds are audio-only Zoom with **no editor at all**. |
| (c) varies by role | **YES, strongly.** See §3 — Algo Dev round 1 is probability, SRE round 1 is Linux/Python trivia, Python SWE round 1 is Python-in-a-bash-shell, C++ SWE round 1 is OS/C++ concepts. |
| (d) varies intern vs full-time | **WEAKLY.** HRT says the intern process is "the same, just slightly abridged." Intern rounds skew slightly more algorithmic (see §3). Not a major axis. |
| (e) changed over time | **NOT MATERIALLY, for the interview itself.** The conceptual C++/OS round is documented from 2020 through 2025. What *did* change is the **OA platform**: Codility (2020–21) → HackerRank/CodeSignal (2022–24) → CodeSignal predominant (2024+). |

---

## 2. EXACT FORMAT OF TECHNICAL ROUND 1

### Length
- **45 minutes** is the dominant, near-universal number. Reported by: Shivam5022 (verified),
  avinal (verified), LeetCode 949535, LeetCode 4261724, Glassdoor Core Developer, 1point3acres
  Algo Dev, HRT's own blog ("usually a 45 minute discussion").
- **40 minutes** — Glassdoor Core Developer variant [SUMMARY-ONLY].
- **30 minutes** — reported for a **CoderPad-on-Zoom** phone screen, incl. Python SWE intern
  [SUMMARY-ONLY, Blind]. This is the short coding variant.
- **60 minutes** — reported for **Systems Engineering** ("60 minutes on CoderPad in Python") and
  for some SWE coding rounds [SUMMARY-ONLY, Blind].
- **90 minutes** — exists but is a later/onsite-style round ("HRT SWE Fullstack 90 min
  Coderpad"), not round 1.

### Platform — this is where the prior research went wrong
There is **no single platform**. Confirmed variants:

| Variant | Platform | Evidence |
|---|---|---|
| Pure conceptual round | **Zoom, audio only, no editor** | LeetCode 949535: "45 minutes long **on Zoom**"; Glassdoor Core Dev: "**no coding involved — just verbal answers**"; avinal (VERIFIED): "will be technical but **will not require coding**"; LeetCode 4103738 asker notes "the interview would be **audio only**" |
| Coding round | **CoderPad** | Blind Algo Eng 2nd round; 1point3acres DE round 1; Blind Python SWE intern ("30 minute CoderPad on Zoom"); Blind Systems Eng ("60 minutes on CoderPad in Python") |
| Python/SRE round | **Python in a bash shell on Linux** (shared terminal) | Blind, quoting recruiter: "For this round, you'll be asked to program in Python in a Bash shell on Linux" [SUMMARY-ONLY] |

**HackerRank / CodeSignal / Codility are the OA platform, not the interview platform.** Do not
conflate. (Codility 90-min/3-question in 2021 — avinal, VERIFIED; CodeSignal 90-min/4-question —
Shivam5022, VERIFIED; CodeSignal GCA and HackerRank both reported 2023–25.)

### Is code run/executed?
- In the CoderPad rounds: **yes** — CoderPad executes code, and multiple candidates describe
  being expected to produce code that compiles and runs. I could not verify a first-hand "I hit
  Run" quote; the strongest statements of this ("they want code that compiles and runs, not
  pseudocode") are **PREP-SITE only** and should not be relied on.
- In the conceptual rounds: **no code is written at all.**

### One interviewer or two?
**One.** Every first-hand account describes a single interviewer — "a working engineer,"
"the interviewer was very friendly." I found **no** report of a two-interviewer phone screen.
(Onsite is a sequence of 1-on-1s.)

### Camera on?
**Usually off / audio-only for the conceptual round.**
- **FIRST-HAND [SUMMARY-ONLY]**, LeetCode Discuss 4261724: *"45 minutes with the **camera off**."*
  https://leetcode.com/discuss/interview-question/4261724/HRT-Phone/
- LeetCode 4103738 (SWE Intern 2024): candidate notes the interview would be **audio only**.
- The CoderPad rounds are on Zoom; camera use is not consistently reported.

### A genuine HRT quirk worth knowing: the dictated problem statement
Multiple independent candidates report that **the interviewer reads the problem aloud and you
type it into the pad yourself** — there is no pasted prompt.
- Blind, "Weird HRT phone screen": *"the interviewer dictating the problem and making the
  candidate type it out."* The same thread's comments complain about "being asked to type out the
  entire question statement rather than having it pasted in a code editor."
  https://www.teamblind.com/post/weird-hrt-phone-screen-xy28awhz
- Another Blind report: *"spent 15 minutes of the 30-minute interview writing down a problem
  statement that was being dictated verbally"* — then still solved it optimally after hints.
[Both SUMMARY-ONLY, but two independent posts describing the same unusual behavior.]

---

## 3. WHAT IS ACTUALLY ASKED — concrete reported questions

### 3a. The conceptual C++/OS round (the "trivia" round) — CONFIRMED REAL

**FIRST-HAND (VERIFIED — I read the full file).** `Shivam5022/Interview-Experiences`, role:
**C++ Software Engineer**. Round: "Phone Screening — a 45-minute in-depth systems interview,
primarily on OS and C++." Questions, verbatim:
- "Use of `inline` functions in C++: pros and cons"
- "`vector` vs `list`: trade-offs and internal details"
- "Internal working of `malloc`, demand paging, etc."
- "How the kernel allocates memory to user processes"
- "System calls like `sbrk` and `mmap`"

Note: **this post does NOT mention CoderPad.** The prior research's list came from here, and the
CoderPad attribution was added from elsewhere. That is the origin of your tension.
https://github.com/Shivam5022/Interview-Experiences

**FIRST-HAND (VERIFIED).** `avinal/website`, role: **Systems Internship, Summer 2021**.
- Stage 1: 90-min **Codility**, 3 medium questions, C/C++/Python/Golang allowed.
- Stage 2, verbatim: *"This interview will last about 45 minutes and will be technical but
  **will not require coding**."*
- Content, verbatim: *"questions were mostly related to Linux/Unix, C++ (mainly pointers and
  memory), Python/Bash scripting, automation, knowledge of tools (IDEs, Editors, System
  Administration Tools) and previous experiences"* — plus "why do you want to work for this
  role?"
- Texture: *"not so tricky but practical and real-life"*; the interviewer *"would often explain
  why he is asking this question"* and kept referring back to the resume.
https://github.com/avinal/website/blob/main/content/posts/blogs/hrt-interview-1.md

**FIRST-HAND [SUMMARY-ONLY].** LeetCode Discuss 949535, **SWE New Grad**, rejected. 45 min on
Zoom. Intro + projects, then **stack vs heap**, **inline functions**, and some **computer
networks**. "More like a technical conversation than an interview." Reject 2 days later.
https://leetcode.com/discuss/interview-experience/949535/hrt-software-engineer-new-grad-telephonic-interview-reject/

**FIRST-HAND [SUMMARY-ONLY].** LeetCode Discuss 4261724 (~2023). 45 min, camera off:
- `vector` resizing — then follow-ups on the **amortized complexity if you grow by 10%, or by a
  constant K** instead of doubling
- **"What happens if you `malloc` 8GB on a machine with 4GB of RAM?"** → drills into system
  calls, overcommit, swap
- **an LRU-cache spin-off** ← note: this one *is* a coding/design question, in the same session
https://leetcode.com/discuss/interview-question/4261724/HRT-Phone/

**FIRST-HAND [SUMMARY-ONLY].** Glassdoor, **Core Developer**: *"The first phone screen was
approximately 45 minutes and focused on operating system and data structure basics, **with no
coding involved — just verbal answers to questions**."* Another Core Dev review: 40-min call,
"basic questions on algorithms & data structures, OS and C++." Others in the same page:
**virtual memory, paging, multi-threading; STL containers and how they're implemented, pros and
cons; inline functions.**
https://www.glassdoor.com/Interview/Hudson-River-Trading-Core-Developer-Interview-Questions-EI_IE470937.0,20_KO21,35.htm

**FIRST-HAND [SUMMARY-ONLY].** Glassdoor, **SWE Intern**: *"how `push_back` works in C++
(including time complexities and internal working)"*; *"differences between threads and
processes with follow-ups"*; a three-question round of *"hash maps / design a data structure /
an OS system application question"*; also **OS design questions + a LeetCode-Medium BFS problem**
in a first round.
https://www.glassdoor.com/Interview/Hudson-River-Trading-Software-Engineer-Intern-Interview-Questions-EI_IE470937.0,20_KO21,45.htm

### 3b. The coding round
- **Tic-tac-toe-like game** — jointaro, SWE, Oct 2025 (the round *before* CS fundamentals).
- **LRU cache spin-off** — LeetCode 4261724.
- **LeetCode-Medium BFS** — Glassdoor SWE Intern.
- Blind, Algo Web Eng: *"they'll explain some complicated system or data structure that you'll
  discuss implementing, then you will implement it"* — i.e. **implement-a-data-structure**, not
  a puzzle with a trick.
- Blind, general SWE: *"the first phone interview is quite practical and involves a lot of
  **system design trade-offs**, asking questions to help understand requirements, and some code
  — with the coding **not being the main focus** but used to demonstrate how you would implement
  a solution."*

⚠️ **Explicitly NOT verified:** the widely-repeated specifics "minimum excluded prime along paths
in a tree" and "process a stream of timestamped trades and compute running profit" come from
**techinterview.org and spacecomplexity.ai only** (prep sites). I found no candidate anywhere
reporting either. **Do not present these as real HRT questions.**

### 3c. Rough proportion
For the **C++/Core/Systems SWE track**, round 1 is roughly **70–90% conceptual OS + C++
internals + resume, 10–30% a light implement-this data structure**, and in a meaningful fraction
of reports **0% coding**. For the **Algo Dev track** round 1 is **~100% probability/statistics**.
For **general SWE**, one of the two phones is a real coding round. There is no debugging round
reported at phone-screen stage — debugging appears at onsite (OFFICIAL: onsite is "coding and
debugging rounds, technical design discussions, and team fit").

---

## 4. HOW IT DIFFERS BY ROLE — the most useful table here

| Track | What round 1 actually is | Source |
|---|---|---|
| **Software Engineer (C++)** | 45 min, OS + C++ internals, verbal, often no code | Shivam5022 (VERIFIED); LC 949535; Glassdoor Core Dev |
| **Core Developer / Low-latency C++** | 45 min OS + data structures, "no coding, just verbal answers"; virtual memory, paging, threading, STL internals | Glassdoor Core Dev; Blind low-level C++ threads [SUMMARY-ONLY] |
| **Software Engineer (Python)** | Coding — **Python in a bash shell on Linux**; Python syntax, bash commands, debugging errors. Or "30 minute CoderPad on Zoom" | Blind (recruiter text quoted); jointaro Singapore [SUMMARY-ONLY] |
| **Algorithm Developer / Algo Eng (quant research)** | **Round 1 = probability & statistics, no coding.** Self-intro + ~3 prob/stat questions in 45 min: coin-flip problems, i.i.d. standard normals, conditional probability / Bayes / distributions. **Round 2 = CoderPad coding**, Python allowed, "brush up on recursion." | 1point3acres 1025739 & 1032012; Blind 1nz00wah; Blind uH03BvKD [all SUMMARY-ONLY] |
| **Systems / SRE** | Linux + Python **oral trivia**. Verbatim from a July 2025 candidate: *"difference between `\|` and `>` in the Linux shell"*, *"hard link vs symbolic link"*, *"`kill -15` vs `kill -9`"*, *"what is `yield` used for in Python"*, *"what are a generator and a decorator"*. Also project-ownership questions. Some Systems Eng roles instead get "60 minutes on CoderPad in Python." | jointaro SRE, Jul 2025; avinal (VERIFIED, systems intern); Blind [SUMMARY-ONLY] |
| **Algo Web Engineer** | Either coding (implement a described system/data structure) **or** behavioral + probability brainteasers — recruiter tells you which | Blind Au8BSKNX [SUMMARY-ONLY] |
| **Data Engineer / Data Production Eng** | **Round 1 on CoderPad, Python.** One candidate expected LeetCode and got a different style of technical assessment from an SDE interviewer. | 1point3acres 949902 [SUMMARY-ONLY] |

### Intern vs full-time
- HRT (OFFICIAL [SUMMARY-ONLY]): the blog covers full-time campus recruiting and says it
  "applies to internship programs as well, just with a slightly abridged process."
- The one clear intern-specific difference: intern first rounds are somewhat **more likely to
  include an actual algorithm** (Glassdoor SWE Intern: OS design + LC-Medium BFS; Blind Python
  SWE intern: 30-min CoderPad).
- The Systems **internship** round 1 was explicitly *no coding* (avinal, VERIFIED). So this is a
  tendency, not a rule.

---

## 5. LANGUAGE

- **You pick at application time.** OFFICIAL: HRT's SWE postings are literally titled
  *"Software Engineer (C++ or Python) – 2027 Grads"* and *"Software Engineering Internship (C++
  or Python) – Summer 2027"*, and their Student Opportunities page has you **indicate a C++ or
  Python preference when you apply**. Your interviews then follow that track.
  https://www.hudsonrivertrading.com/student-opportunities/
- OFFICIAL [SUMMARY-ONLY], hrtbeat: on the Programming round — *"For certain roles, you'll be
  asked to program in either C++ or Python, while others will give you the choice to pick any
  language you're comfortable with."*
- **C++ is NOT universally required in round 1.** Python is fully allowed (and is the *expected*
  language for Algo Dev round 2, for the Python SWE track, for SRE, and for Data Engineering).
- But: if you picked the C++ track, **round 1 will interrogate C++ internals** whether or not
  you write code. And note the failure mode below.
- FIRST-HAND (VERIFIED), OneRaynyDay (2020, Algo Engineer): wrote solutions in Python and C++,
  and deliberately **avoided C++20 features** because "the online coding platforms (like
  coderpad) likely use stable distributions of GCC and clang." Prescient — see §6.

---

## 6. WHAT THE INTERVIEWER IS EVALUATING, AND WHAT CUTS PEOPLE

### HRT's stated criteria (OFFICIAL [SUMMARY-ONLY], hrtbeat)
- Is your code **idiomatic** for the language you chose (modern syntax)?
- Do you make **optimal use of resources** (memory, CPU)?
- Is your code **well-encapsulated, easy to read, well-commented**?
- Can you **break a problem down and work toward an answer incrementally**?
- **Teachability** — *"whether you applied ideas or approaches discussed earlier in the interview
  to subsequent questions or problems, as a way to show that you've learned something and that
  you're receptive to feedback."* ← This is the most under-appreciated criterion and it is
  HRT's own language. The interviewer gives you a hint; they are watching whether it propagates.
- Communication is rated **as much as** technical ability.

### HRT's stated philosophy (OFFICIAL [SUMMARY-ONLY], `hrtbeat/engineering-and-interviewing-at-hrt`)
> "We do our best to stray away from **'burst of insight' leet-code style questions**." Their
> ideal is that "a strong programmer from a competitive firm would ace their technical interview
> **with no studying**." They "want engineers with strong fundamentals but stay away from
> obscura and 'tricks'."

This is HRT explicitly disclaiming the LeetCode-grind framing that prep sites sell. It also
explains why round 1 is fundamentals-heavy: they believe fundamentals can't be crammed.

### What actually gets people cut at this stage
1. **Not knowing OS/C++ internals cold.** The single most common rejection story. Candidates who
   found the interviewer "friendly," felt it was "a technical conversation," and still got a
   reject 2 days later — because they missed a few fundamentals questions (LC 949535).
2. **Finishing the coding fast is not sufficient.** Blind, "Weird HRT phone screen" thread: a
   commenter *"finished the technical portion in half the time and spent the rest discussing
   HRT, then was rejected a few days later — feedback was that they didn't pass the technical
   portion."* Speed ≠ pass. Quality, idiom, and the follow-up discussion are scored.
3. **The dictated-problem tax.** Losing 15 of 30 minutes transcribing the problem is a real,
   repeatedly-reported hazard. Type fast, or ask to summarize back rather than transcribe.
4. **⚠️ Interviewer-quality variance — a genuine 2025 risk, and it is first-hand.** Two separate
   jointaro reports in 2025:
   - Apr 1 2025, SWE, US: *"interviewers … had little knowledge of the technical questions they
     were asking and were unable to adapt questions based on discussion. Even when I provided
     correct responses, they kept prompting until I guessed the one on **the answer key**. Their
     C++ questions were **woefully out of date** — they were confused when I answered based on
     C++20 features. Many interviewers were on different teams, had been at HRT **less than six
     months**, and were **less than a year out of college**."*
     https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-united-states-april-1-2025-no-offer-negative-2a2ca5aa/
   - Oct 15 2025, SWE, US: failed the CS Fundamentals round *"due to the interviewer getting
     several facts about the C++ language wrong."*
   **Implication for a candidate:** the conceptual round is scored against a crib sheet. Answer
   the *textbook* answer first (the one on the answer key), and only then add nuance or
   modern-C++ caveats. Leading with C++20 subtleties has demonstrably cost people the round.
5. **Feedback is slow and thin.** Reports of ~1.5 months for minimal feedback. HRT's overall
   median process is ~21–28 days (Glassdoor).

---

## 7. TIMELINE / FORMAT CHANGE OVER TIME (2020 → 2026)

| Year | OA platform | Round 1 shape |
|---|---|---|
| 2020 | — | 2 phone screens then a 6.5-hour onsite (OneRaynyDay, VERIFIED) |
| 2021 | Codility, 90 min / 3 medium | 45 min, technical, **no coding** (avinal, VERIFIED) |
| ~2021 | — | 45 min Zoom, stack vs heap / inline / networks (LC 949535) |
| 2023 | — | 45 min camera-off; vector resizing, malloc-8GB-on-4GB, LRU (LC 4261724) |
| ~2023–24 | CodeSignal, 90 min / 4 easy CP | 45 min OS + C++ internals (Shivam5022, VERIFIED) |
| 2024 | CodeSignal GCA / HackerRank | OS, DS, networking, projects; second phone = C++ pointers & references |
| 2025 | CodeSignal / HackerRank | **Coding round then CS Fundamentals round** (jointaro Oct 2025); SRE = Linux/Python oral (jointaro Jul 2025); Algo Dev = probability phone screen (jointaro Sep 2025) |

**Conclusion: the interview format has been stable for ~5 years.** The conceptual C++/OS round is
not a legacy artifact — it was alive and rejecting people in late 2025. What changed is the OA
vendor, and (per 2025 reports) the seniority of who is running the fundamentals round.

---

## 8. PRACTICAL BOTTOM LINE

1. **Ask your recruiter which type of round it is.** Candidates confirm HRT tells you the focus
   and structure in advance, and even names the language and environment ("Python in a bash
   shell on Linux", "60 minutes on CoderPad in Python").
2. **Do not assume CoderPad.** If it's the fundamentals round it may be audio-only Zoom, camera
   off, no editor.
3. **Prepare both, but weight by track.** C++/Core → OS internals + C++ object model. Algo Dev →
   probability. SRE/Systems → Linux tooling and Python idioms. Python SWE → bash + Python
   debugging.
4. **The specific conceptual questions to actually know** (all first-hand-sourced): `inline`
   pros/cons; `vector` vs `list`; `vector` growth/amortization incl. non-doubling growth factors;
   `push_back` internals; how `malloc` works; what happens when you `malloc` more than RAM
   (overcommit/swap); demand paging; how the kernel gives memory to a process; `sbrk` vs `mmap`;
   stack vs heap; threads vs processes; virtual memory & paging; STL container implementations
   and trade-offs; hash maps; a bit of networking; LRU cache.
5. **Answer the canonical answer first.** There is an answer key, and the interviewer may be
   junior.

---

## 9. SOURCE INDEX

**FIRST-HAND, FULLY VERIFIED (read in full):**
- https://github.com/Shivam5022/Interview-Experiences — C++ SWE; CodeSignal OA + 45-min OS/C++ phone screen; the origin of the inline/vector/malloc/demand-paging/sbrk-mmap list
- https://github.com/avinal/website/blob/main/content/posts/blogs/hrt-interview-1.md — Systems Internship Summer 2021; Codility + 45-min explicitly non-coding technical phone
- https://github.com/OneRaynyDay/oneraynyday.github.io/blob/master/_posts/2020-09-30-Interviewing-During-Covid.md — Algo Engineer 2020; coding challenge + 2 phone screens + 6.5h onsite; coderpad/GCC-version caution

**FIRST-HAND, SUMMARY-ONLY (domain blocked):**
- https://leetcode.com/discuss/interview-experience/949535/hrt-software-engineer-new-grad-telephonic-interview-reject/
- https://leetcode.com/discuss/interview-question/4261724/HRT-Phone/
- https://leetcode.com/discuss/post/4103738/HRT-Phone-Interview-in-coming-days-for-SWE-Intern-2024/
- https://www.teamblind.com/post/HRT-Algo-Web-Engineer-Interview-Au8BSKNX
- https://www.teamblind.com/post/hudson-river-trading-hrt-algo-developer-phone-interview-what-to-expect-1nz00wah
- https://www.teamblind.com/post/HRT-Hudson-River-Trading-Algo-Engineer-2nd-Round-CoderPad-Interview-uH03BvKD
- https://www.teamblind.com/post/hudson-river-trading-core-developerlow-level-c-interview-yuqksebo
- https://www.teamblind.com/post/weird-hrt-phone-screen-xy28awhz
- https://www.teamblind.com/post/hrt-swe-phone-screen-kncwpbrd
- https://www.teamblind.com/post/hrt-algo-software-engineer-technical-non-coding-phone-interview-k322paxw
- https://www.teamblind.com/post/hudson-river-trading-python-swe-intern-interview-tm0hz3li
- https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-october-15-2025-no-offer-neutral-bd6da5f3/
- https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/software-engineer-united-states-april-1-2025-no-offer-negative-2a2ca5aa/
- https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/site-reliability-engineer-united-states-july-1-2025-no-offer-positive-0b3bce6f/
- https://www.jointaro.com/interviews/companies/hudson-river-trading/experiences/algorithm-developer-new-york-ny-september-4-2025-no-offer-neutral-d2e0c827/
- https://www.1point3acres.com/bbs/thread-949902-1-1.html (DE round 1, CoderPad + Python)
- https://www.1point3acres.com/bbs/thread-1025739-1-1.html (Algo Dev round 1 = probability/stats)
- https://www.1point3acres.com/bbs/thread-1032012-1-1.html (Algo Dev first phone)
- https://www.1point3acres.com/bbs/interview/software-engineer-228118.html (电面 智力题，没算法)
- https://www.glassdoor.com/Interview/Hudson-River-Trading-Core-Developer-Interview-Questions-EI_IE470937.0,20_KO21,35.htm
- https://www.glassdoor.com/Interview/Hudson-River-Trading-Software-Engineer-Intern-Interview-Questions-EI_IE470937.0,20_KO21,45.htm

**OFFICIAL, SUMMARY-ONLY (hudsonrivertrading.com blocked):**
- https://www.hudsonrivertrading.com/hrtbeat/interview-at-hrt/ — "How to Prepare for Your Software Engineer Interview at HRT" (2021–22 campus season; round taxonomy; evaluation criteria; teachability)
- https://www.hudsonrivertrading.com/hrtbeat/engineering-and-interviewing-at-hrt/ — "Answers to Questions I Often Get" ("burst of insight" quote; ace-with-no-studying ideal)
- https://www.hudsonrivertrading.com/student-opportunities/ — C++ or Python preference at application

**PREP-SITE — cited nowhere as fact, listed so they can be recognized and excluded:**
spacecomplexity.ai/blog/hudson-river-trading-phone-screen-interview · techinterview.org ·
techprep.app · quantt.co.uk · tradermath.org · hackerprep.io · prachub.com · myntbit.com ·
dataford.io · codejeet.com · ghostinterview.co · quantblueprint.com · extern.com · linkjob.ai ·
oavoservice.com · programhelp.net · coditioning.com · nodeflair.com ·
github.com/sumitsingh4411/interview-rounds · github.com/NagarjunMa/Linux-Learning
