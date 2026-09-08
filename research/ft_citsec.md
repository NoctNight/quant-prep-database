# Citadel Securities — Full-Time / Experienced-Hire Interview vs. Internship Interview

Research date: 2026-09-08. Emphasis on 2023–2026 reports.
**Focus: what CHANGES for full-time.** Intern-side detail included only as the baseline for contrast.

---

## 0. Method and a hard caveat on sourcing

**Direct page fetches were blocked for every primary forum and for the firm's own site.** The session egress proxy returned `EGRESS_BLOCKED` for `citadelsecurities.com`, `citadel.com`, `teamblind.com`, `1point3acres.com`, `interviewquery.com`, `jointaro.com`, and `spacecomplexity.ai`. Glassdoor, LeetCode Discuss and Wall Street Oasis were never directly readable either.

Everything below therefore comes from **search-engine summaries of those pages** — the indexed text of Blind posts, Glassdoor entries, 1point3acres 面经, LeetCode Discuss threads, and aggregator guides. That is weaker evidence than reading the threads. I have labelled each claim:

- **[STRONG]** — official-process language, or the same specific detail independently surfacing from more than one source family.
- **[MEDIUM]** — one candidate account or one aggregator that appears to be paraphrasing candidate accounts.
- **[WEAK]** — a single aggregator/SEO guide with no visible candidate provenance. Several of these ("techinterview.org", "techscreen.app", "dsaprep.dev", "interviewfox.ai", "linkjob.ai", "norahq", "dataford", "prachub") are AI-generated content farms. Treat their numbers as unverified.

**Firm attribution:** flagged inline as **[CitSec]**, **[Citadel HF]**, or **[SHARED]** where the evidence is about the joint campus pipeline.

---

## 1. Firm disambiguation — why the evidence blurs

Citadel (hedge fund) and Citadel Securities (market maker) are legally separate but run a **deliberately shared campus funnel**. **[STRONG, SHARED]**

Both firms' official process pages carry the identical sentence: *"Interviewing with us means having the opportunity to talk with two firms at once: Citadel and Citadel Securities."* The team-matching step is explicitly cross-firm: *"hiring managers across teams within Citadel and Citadel Securities have the opportunity to review your resume and interview feedback."* If both firms want you, you pick the offer.

- https://www.citadel.com/careers/career-perspectives/our-engineering-interview-process/ (campus engineering)
- https://www.citadelsecurities.com/careers/career-perspectives/our-quantitative-research-interview-process/ (campus QR)
- https://www.citadelsecurities.com/careers/career-perspectives/our-engineering-interview-process/ (**Experienced Professionals** — note this is a *separate page* from the campus one; the existence of a distinct experienced-hire process page is itself the cleanest evidence that the FT/experienced track is a different process, not a re-labelled campus one)

**Counter-evidence [MEDIUM]:** at least one guide asserts Citadel and Citadel Securities *"run separate recruiting pipelines and do not share candidates"* — https://simplify.jobs/blog/citadel-new-grad-job-2027. Reconciliation: the *shared* language is on the campus/new-grad pages; the separation likely applies to experienced-hire and to specific programs (e.g. Citadel's NXT). **So: for interns and new grads, expect the joint pipeline; for experienced hires, expect a single-firm process.** [MEDIUM]

**Practical consequence for FT:** a full-time candidate's superday feedback is circulated to a *pool* of hiring managers across two firms. That is the mechanism behind team matching (§5) and is much more consequential for FT than for interns.

---

## 2. Pipeline delta — the headline table

| Stage | Internship | Full-time / experienced | Confidence |
|---|---|---|---|
| Recruiter screen | 15–30 min | 20–30 min; explicitly triages you "into the right track" (level + target team) | MEDIUM |
| HackerRank OA | **Yes — described as "the defining filter for new grads and interns"** | **Present in the standard flow, but it is NOT the gate.** For experienced hires it is often skipped or replaced by a single refactor task | MEDIUM |
| Technical phone screen | **1 round**, 45–60 min, CoderPad, Python or C++, pure DS&A + resume | **1–2 rounds.** Same 45–60 min shape *plus* "targeted systems questions for experienced candidates". One Blind report: recruiter said **two phone screens then three onsite rounds** | MEDIUM |
| Onsite / superday | **3 × 45 min = ~2h15m**, independent unrelated problems | **~5 hours, one continuous problem**: 1h design → 2h coding → 1h code review → 1h behavioral. Alternatively described as 3–5 × 60 min, or 5–7 rounds | **STRONG** (see §3) |
| Team matching | Largely a placement exercise; team assigned | **A real gate with real interviews.** HMs review feedback; interested teams *call you back in*; multiple interested teams = multiple extra interviews | STRONG |
| Hiring committee / leadership | Lighter | Internal committee review + senior leadership call on motivation, fit, long-term alignment; can go "deep domain knowledge to test experience" | MEDIUM |
| End-to-end timeline | 6–10 weeks | 6–8 weeks new grad; **4–6 weeks experienced** (compressed for competing timelines) | MEDIUM |

Sources for the table:
- https://enginebogie.com/interview/experience/citadel-securities-software-development-engineer/1634
- https://www.teamblind.com/post/citadel-securities-onsite-mini-intership-0i4lizal
- https://www.teamblind.com/post/citadel-swe-interview-3hurnw5r
- https://www.citadelsecurities.com/careers/career-perspectives/our-engineering-interview-process/
- https://leonstaff.com/blogs/citadel-interview-response-time/
- https://quantvault.org/citadel-interview-process.html

### 2a. Does full-time skip the HackerRank OA?

**Not cleanly, but its role changes.** [MEDIUM]

The strongest phrasing found: the HackerRank OA (60–90 min, 2–3 algorithmic problems, **hidden test cases, suboptimal solutions fail**) is *"the defining filter for new grads and interns."* That wording implicitly de-emphasises it for experienced hires. Corroborating: LeetCode Discuss reports an experienced-hire OA of **15 multiple-choice questions + 1 easy-medium coding problem** — a very different, much lighter artifact than the intern OA, functioning as a formality rather than a filter.

Separately and importantly, a **60-minute OA consisting of a single complex refactoring task — optimising a slow C++ implementation for large-scale data processing** is reported. This is the same *genre* as the obfuscated-C++ onsite round (§4) and appears to be the C++-track variant of the OA.

- https://leetcode.com/discuss/interview-experience/5565531/Citadel-or-Senior-Software-Engineer-or-Reject/
- https://leetcode.com/discuss/post/7268790/ (Citadel Securities OA — C++ Engineer)
- https://www.interviewquery.com/interview-guides/citadel-software-engineer

**No source states that full-time candidates are formally exempt from the OA.** Plan on taking one; the delta is that passing it buys you far less than it does as an intern.

### 2b. How many CoderPad screens?

- **Intern:** 1. Official campus language — *"a 45- to 60-minute remote interview covering both technical and behavioral skills… we'll send a CoderPad link… core programming languages are Python and C++."* [STRONG]
- **Full-time:** the official/aggregator baseline is also 1, but **the extra content is systems questions layered onto the same slot** ("one algorithmic problem on CoderPad or HackerRank Live, **plus targeted systems questions for experienced candidates**"). [MEDIUM]
- **A Blind report has a recruiter stating two phone screens then three onsite rounds** for a Citadel Securities SWE loop. [MEDIUM] Treat 2 as a realistic possibility rather than the norm.

### 2c. How many superday rounds?

The two structures reported are genuinely different in kind, not just in count:

- **Intern:** 3 × 45 min, back-to-back, **independent** problems. ~2h15m. Also documented on 1point3acres as *"three-round video interview, 2 hours 15 minutes total, each round ~45 minutes, resume/behavioral + algorithm coding."* [STRONG]
- **Full-time:** either "3–5 × 60 min" (aggregator baseline) or, in the more specific and more consistent candidate accounts, the **single-problem 5-hour "mini internship"** described in §3. [STRONG for existence; MEDIUM for it being universal]

---

## 3. THE core structural delta: the "mini internship" onsite

This is the single most important difference and the best-evidenced finding in this report. **[STRONG]**

A Blind post — literally titled *"citadel securities onsite mini internship"* — describes the FT onsite as:

> **1 hr design, 2 hr coding, 1 hr code review, 1 hr behavioral**

https://www.teamblind.com/post/citadel-securities-onsite-mini-intership-0i4lizal

This is independently corroborated by LeetCode Discuss (*"the final onsite round involves working on a big problem done in three rounds: first you design it, second you implement it, third you discuss your solution"*) and by process guides describing it as:

> *"You define the problem, design a system, build it, and then defend and extend it as new constraints come in. **Early decisions compound: a choice you made in the design hour will shape what you can do in the code review.** You work one problem from design through code review, **with the same interviewers**, instead of cycling through unrelated questions with different people."*

And the problem domain is not abstract: *"something drawn from systems we actually run, such as order books, matching engines and market-data pipelines."*

**Why this matters more than the round count.** The intern superday is three independent shots — a bad round is one-third of your evidence. The FT onsite is **one shot with compounding state**. A weak abstraction chosen in hour 1 is still hurting you in hour 5, in front of the *same* interviewers, who watched you choose it. There is no reset. This is the structural reason the FT loop feels disproportionately harder than "45 more minutes of interview."

Round-by-round expectations reported:
- **Design (1h):** sketch end-to-end — components, interfaces, data flow, assumptions you're making *and the ones you're not*. Interviewer pushes edge cases and **adds requirements you did not plan for**.
- **Coding (2h):** *"whether it works, whether someone else could read and extend it, and if the abstractions you chose in the design hold up once they meet real input."* Note the explicit readability/extensibility bar — absent from intern reports.
- **Code review (1h):** see §4.
- **Behavioral (1h):** see §6.

---

## 4. The obfuscated-C++ round — confirmed, with caveats

**Confirmed. [MEDIUM–STRONG]** The user's premise is real, but the shape needs correcting on two points.

### What it is

The most direct candidate account found:

> *"They were shared an **obfuscated C++ code with lots of loops and complex logic** that was difficult to comprehend, with the **objective being to optimize it**."*

Surfaced from the Citadel Securities Glassdoor / Blind SWE interview corpus:
- https://www.glassdoor.com/Interview/Citadel-Securities-Software-Engineer-Interview-Questions-EI_IE1443495.0,18_KO19,36.htm
- https://www.teamblind.com/post/citadel-securities-swe-interview-adtkpi5w

Corroborating variants of the same genre:
- **1point3acres 面经:** *"candidates are given source code with **correct logic but poor performance** and asked to refactor and optimize it."* — https://www.1point3acres.com/interview/problems/company/citadel
- **Quant Developer superday:** *"one medium-hard algorithmic question **plus a practical 'clean up this messy code' refactor**." — https://everythingquant.com/forum/post/citadel-securities-quant-trader--developer-interview-guide/
- **OA variant:** a 60-min OA that is *"a single, complex refactoring task requiring optimization of a slow C++ implementation for large-scale data processing."*
- **General:** *"some candidates report experiencing heavy C++ debugging rounds."*

### Correction 1 — it is billed as **1 hour**, not 2

Every structural account puts **code review at 1 hour** and **coding at 2 hours**. The user's "~2-hour obfuscated C++ round" likely conflates the 2h *coding* block with the 1h *code review* block. If both run back-to-back on the same codebase the lived experience is ~3 hours of C++ under one problem, which plausibly generates the "2 hours" memory. **Plan for 1h of formal code review, embedded in a ~5h C++-heavy day.**

### Correction 2 — there appear to be TWO variants of the code-review hour

Sources split cleanly, and this is an unresolved fork:

| Variant | Description | Evidence |
|---|---|---|
| **(A) Review your own code** | You walk through what *you* built in the 2h coding block, explain tradeoffs and design decisions, defend and extend under new constraints | Process guides; "the same interviewers"; "a choice you made in the design hour will shape what you can do in the code review" |
| **(B) Review foreign obfuscated code** | You are handed unfamiliar, deliberately dense C++ and asked to comprehend then optimise it | Glassdoor/Blind candidate account; 1point3acres 面经; QD "clean up this messy code" |

Most likely reading: **(A) is the standard SWE onsite shape; (B) appears on C++-specific / low-latency / quant-dev tracks** and sometimes as the OA. Both exist. Prepare for both. **[MEDIUM — this fork is my inference from source clustering, not a stated fact anywhere.]**

### How it is scored — what candidates and guides say

No source gives an explicit rubric. The consistent signals:

- **Comprehension before optimisation.** The stated objective is "optimize," but the described difficulty is that the code is "difficult to comprehend." The round tests whether you can build a correct mental model of unfamiliar dense code fast — i.e. the actual daily job of joining a mature low-latency codebase.
- **Justify every decision.** *"You must be prepared to justify every design decision you make."*
- **Readability is a graded axis, not a courtesy.** *"whether someone else could read and extend it."*
- **Process over completion.** The official experienced-hire framing: *"we are less interested in whether candidates finish problems than in how their thinking holds up as problems get harder."* This is the closest thing to an official rubric statement and it is from the **experienced-hire** page specifically.
- **Anti-hero-engineer.** *"Citadel interviewers don't treat algorithm problems like abstract math games — they watch how you reason through concurrency, throughput, failure paths, and whether you avoid 'hero engineer' energy."*

### Nothing equivalent exists on the intern side

No intern account in any source surfaced a code-review or code-comprehension round. **The intern superday is three fresh-authorship coding rounds.** The comprehend-and-optimise round is, on this evidence, a full-time-only artifact. **[MEDIUM — argument from absence, but absence across every intern source found.]**

---

## 5. C++ depth delta — confirmed, and it is resume-triggered

**Confirmed. [STRONG]** This is the second-largest delta after the onsite structure.

### Intern baseline
Graph traversal (BFS/DFS/shortest path), **topological ordering**, heaps, hash maps, balanced trees, brute-force→optimal complexity work, plus resume/behavioral inside each 45-min round. Python **or** C++ accepted. Language-agnostic: *"we welcome any languages."* — https://www.citadel.com/careers/career-perspectives/our-engineering-interview-process/

The user's characterisation of the intern loop as BFS / topological sort / resume is **accurate and well-supported.**

### Full-time additions

> *"Candidate reports from 2024 describe one round covering **C++ specifics (iterators, std::variant, memory management)** for roles that explicitly use C++."*

> *"**If you list C++ on your resume, expect a thorough grilling on memory management, iterators, std::variant, and the latest standards including C++20 and C++23.**"*

> *"Superday interviews ranged from cpp grilling on **iterators, memory management, and stl containers such as std::variant, std::vector**."*

Every element of the user's premise — **STL internals, `std::variant`, move semantics, iterators** — is confirmed. Additional FT-only C++ surface found:

- **Move semantics and template metaprogramming** — *"for SWE and quant developer roles, C++ is heavily emphasised; expect questions on memory management, move semantics, and template metaprogramming."*
- **Variadic templates in anger** — *"some interviewers have expected candidates to know about using **variadic templating with tuples for high-performance trading signal handling**."* This is a notably specific and unusually deep ask. — https://algo.monster/interview-guides/citadel
- **STL implementation trivia** — *"the phone interview can include a series of trick questions about particular edge cases of C/C++ and the **underlying implementation details of STL**."* (e.g. iterator invalidation on `push_back` reallocation.)
- **Below the language** — *"interviewers dig into memory management, garbage collection, and **how your code interacts with the underlying operating system**."*
- **Low-latency systems C++** — *"refresh on **C++ memory model semantics, lock-free data structures (specifically SPSC and MPSC ring buffers), and the basics of kernel-bypass networking**."*
- Production stack cited as modern C++ (C++20/23; one guide claims C++26 on some teams — **[WEAK]**, likely SEO embellishment, but the "latest standards" expectation is real).

Sources:
- https://www.citadelsecurities.com/careers/career-perspectives/sea-change-in-c-why-opportunities-abound/
- https://www.quantt.co.uk/resources/citadel-interview
- https://www.techinterview.org/post/3233474597/cpp-quant-interviews/
- https://www.techscreen.app/articles/citadel-technical-interview-process-2026
- https://nodeflair.com/companies/citadel/interviews/c-developer

### The mechanism to internalise

**The C++ grilling is triggered by your resume, not by your level.** *"If you list C++ on your resume, expect a thorough grilling."* Interns typically list C++ as coursework and are treated as generalists; FT candidates list C++ as production experience and are treated as claiming expertise. **Full-time is where the claim gets audited.** A new-grad who genuinely used only Python may see less of this; a 3-year C++ engineer will see all of it.

**Counter-signal, worth weighing [MEDIUM]:** one candidate account states the technical rounds are run by *"actual SWEs who are pretty friendly and **more concerned with problem-solving than trivia or language depth**."* So the depth is not uniform — it is likely team-dependent (low-latency/market-data teams grill; platform/infra teams less so).

---

## 6. The single-fail policy — real, but the sourcing is thin

**Partially confirmed. Real as a phenomenon; the strongest phrasing traces to a low-quality source. [MEDIUM, with a caution]**

The exact claim surfaced:

> *"Citadel Securities (CitSec), the market maker, hires for HFT software, quant research and quant dev… **the loop is single-fail — any weak round and the next interview is cancelled within a day.**"*

This phrasing originates from **techinterview.org**, an aggregator with content-farm characteristics. **Do not treat "within a day" as fact.** — https://www.techinterview.org/companies/citadel-securities/

**Independent corroboration that the phenomenon is real:**
- A Blind thread exists titled **"citadel nxt interview canceled"** — https://www.teamblind.com/post/citadel-nxt-interview-canceled-skjvpdnc
- LeetCode Discuss, experienced SWE (3 yrs backend/infra, NXT): **"first round rejected the next morning."** — https://leetcode.com/discuss/interview-experience/6972253/
- LeetCode Discuss, senior SWE: eliminated at the **EM "vibe check"** before reaching later technicals.
- Blind: recruiter conveyed *"not positive feedback"* **3 business days after onsite**, signalling rejection. — https://www.teamblind.com/post/ghosted-by-citadel-securities-after-onsite-ejxpuxnd
- General superday convention: *"on superday, each round is typically eliminatory."*

**So:** fast elimination between *stages* (phone screen → onsite) is well-documented and rapid. Cancellation of remaining rounds *mid-superday* is asserted but I found **no direct Citadel Securities candidate account of it happening on the day.**

### Does it apply to interns?

**No intern-specific evidence was found in either direction.** [GAP]

Two structural arguments that it bites harder on FT:
1. The FT onsite is **one continuous problem with the same interviewers** (§3). "Cancelling remaining rounds" is coherent there in a way it is not for three independent intern rounds — if you have collapsed in the design hour, the coding hour is nearly pointless.
2. Every corroborating cancellation account found is **experienced-hire** (NXT, senior SWE), not intern.

Reasonable conclusion: **the single-fail dynamic is a full-time/experienced phenomenon in practice**, whether or not it is written policy. Interns are more likely to be carried through all three rounds and rejected afterward. **[MEDIUM — inference.]**

---

## 7. Team matching — and yes, you can fail it

**Confirmed as a real failure mode. [STRONG]**

Official mechanism (campus, but applied to FT): *"Following the second-round interviews, **hiring managers across teams within Citadel and Citadel Securities have the opportunity to review your resume and interview feedback** to determine where you would fit best. **If a team expresses interest in your profile, they will call you in for an interview.** If more than one team is interested, this round could consist of multiple interviews."*

Key structural point: **team matching contains additional real interviews**, not just a paperwork step. For SWE it is *"often a senior-engineer team match"* / *"team-specific leadership conversations."*

### Can you fail after passing everything? Yes.

Documented Blind cases:
- *"One candidate reported doing well on the onsite but never getting matched or rejected, and **their recruiter said no teams wanted them**."*
- *"There are some people that don't get a match after clearing tech rounds."*
- A candidate *"passed onsite but couldn't find any team matches, asking if they're rejected for a year."*

- https://www.teamblind.com/post/citadel-team-matching-2jyschlo
- https://www.teamblind.com/post/citadel-team-matching-pov4rrqm
- https://www.teamblind.com/post/citadel-nxt-team-matching-d06uwg38
- https://www.teamblind.com/post/what-happens-after-citadel-securities-intern-leadership-call-bqyofmlk

**Contested base rate.** Other Blind commenters push back hard: *"if you're in, you're in (unlike Google, which rejects people who pass all interviews)"* and one estimate of *"99% success rate for finding a match — it depends on past experience."* Note the qualifier: **"it depends on past experience"** is precisely the FT/intern delta. An intern with no production history is matched on raw signal; an experienced hire is matched on whether a *specific* team wants that *specific* background. **Niche or mismatched experience is a full-time-only way to fail.**

**Timing tell:** *"Citadel has a team-matching step after the Superday that most candidates do not know about, and that step is where the real delays happen… after the Superday expect 2 days to 2 weeks; **if your Superday triggers team matching, add another week**."* — https://leonstaff.com/blogs/citadel-interview-response-time/

### Intern vs FT
Interns are placed onto a team as part of the program; the matching risk is low and largely administrative. **For FT, matching is a genuine gate with its own interviews and its own rejection outcome.** [STRONG for FT; MEDIUM for the intern contrast, which is inferred.]

---

## 8. Experienced hires (2–8 years) — what changes again

The firm maintains a **separate published process page** for experienced professionals, distinct from the campus page. That is the top-line signal. — https://www.citadelsecurities.com/careers/career-perspectives/our-engineering-interview-process/

### 8a. System design becomes load-bearing
- Onsite: *"three to four rounds (3–4 hours): **two algorithmic coding rounds, one system design round, and for senior candidates a fourth round on team-specific systems depth or low-latency design**."* [MEDIUM]
- Content: *"**low-latency systems, market data ingestion, order routing, risk aggregation**"* — and drawn from *"systems we actually run, such as **order books, matching engines and market-data pipelines**."*
- Framing: *"The work is low-latency, high-throughput and rarely static: requirements shift, edge cases surface in production, and yesterday's design must absorb today's load."* → **expect the interviewer to mutate requirements mid-round on purpose.** That is the round's actual mechanic.
- Systems questions also leak *earlier*, into the phone screen: *"plus targeted systems questions for experienced candidates."*

**There is no system design round in any intern account found.** This is a clean addition.

### 8b. Behavioral becomes technical
The experienced behavioral round is not culture-fit chat. Reported prompts:
- *"Tell me about a **production incident you caused** or helped fix."*
- *"Tell me about a time **a system or pipeline you owned failed in production**."*

And the scoring signal is unusually specific:
> *"What distinguishes a good Citadel behavioral answer is **specificity about technical detail**. An answer that says '**I was wrong about the cause of a latency spike for two days because I was looking at p99 and not p99.9**' lands much better than generic responses. What they're listening for is **the opposite of blame diffusion** — they don't want 'the team ran into some challenges' or 'there were factors outside my control.'"*

- https://spacecomplexity.ai/blog/citadel-behavioral-interview-questions

Interns cannot answer these questions — they have no owned production system. **This is a category of round that only exists once you have a production history, and it is graded on metric-level precision, not narrative.**

### 8c. Resume depth is audited, not skimmed
- *"Resume screening is selective; reviewers look for evidence of **technically demanding settings** and proof that you can reason about **time complexity, memory tradeoffs, and failure cases**."*
- *"Include **specific performance improvements, latency reductions, and memory optimizations** rather than just listing what you built."*
- Leadership call *"digs deeply into motivation for joining their team and **deep domain knowledge to test experience**."*
- Every C++ claim on the resume becomes an exam topic (§5).

### 8d. The 1–2 year dead zone — a real trap
> *"When applying for an experienced hire position, candidates can be **rejected as 'too junior'**, while for new grad positions the company prefers candidates with previous internships there. For someone with **1 year of experience, they are essentially considered a new grad without having interned at Citadel**."*

- https://www.teamblind.com/post/Citadel-resume-rejected-me-Fc5dpB3g

**Practical:** at ~1–2 YOE you can be squeezed out of both tracks. The 2–8 year band the user asks about is safe on the low end only from roughly 2–3 years of *relevant* (low-latency / systems / market-data) experience.

### 8e. Timeline and compensation
- Experienced loop compresses to **4–6 weeks** for candidates with competing timelines (vs 6–8 for new grad, 6–10 campus). [MEDIUM]
- **No distinct "negotiation stage" exists as a formal pipeline step.** Offers arrive 1–2 weeks post-superday with comp included.
- Negotiation behaviour reported: *"Citadel does not lose candidates over money; candidates who show competing offers to their recruiters **will have offers matched immediately**."* Also reported: **exploding deadlines**. And post-onsite: *"Citadel Securities was still working on the offer and **does a lot of due diligence**"* — an experienced-hire-only background/reference step. New grad anchor cited around $175k base + ~$100k + ~$100k, negotiable toward ~$500k TC with a competing offer; one Blind account reached ~500k TC per the hiring manager.
- https://www.wallstreetoasis.com/forum/hedge-fund/new-grad-fundamentals-at-citadel-securities-vs-hedge-fund-0
- https://www.teamblind.com/post/citadel-securities-new-grad-swe-edupk1wx
- https://www.levels.fyi/companies/citadel/salaries

**The "due diligence" step is a full-time-only delay** and has no intern analogue.

---

## 9. Return offers and intern→FT conversion

- **Conversion rate: 65–75%** for Citadel interns → full-time. Explicitly benchmarked as *below* Jane Street's 80%+. [MEDIUM] — https://youngandcalculated.substack.com/p/what-actually-gets-an-intern-a-return
- Leadership has publicly said *"a majority of interns will receive a full-time work opportunity"*, and that **campus recruits are twice as likely to become a high performer** at the firm. — https://www.efinancialcareers.com/news/2023/07/interns-citadel
- **Selectivity context:** 2026 cycle — **~115,000 applicants, 350 interns hired, a 0.36% acceptance rate.** — https://fortune.com/2026/06/11/115k-young-people-applied-citadel-internships-350-made-cut-acceptance-rate-0-36/

### Do returning interns skip stages?

**No source confirms a formal skip.** [GAP — this is the weakest-evidenced item in the report.]

What *is* documented is the reverse direction: *"It's typically easier to convert a **full-time offer to an intern** offer than vice-versa. However, they'll be willing to work with you if you pass their intern hiring bar. **It might require another round of interviews, or they may re-evaluate your performance with a different threshold**."* — https://www.teamblind.com/post/converting-intern-offer-to-full-time-kmwh617k

Read carefully, that quote says the **intern bar and the full-time bar are different thresholds**, and that crossing from intern to full-time may require **additional interviews**. This directly contradicts a clean "returning interns skip stages" story.

**Best reconstruction [MEDIUM]:** a *successful summer intern* converts on **performance review, not interviews** — the internship itself replaced the loop. But an intern who did **not** convert, or who converts off-cycle, re-enters a pipeline calibrated at the higher FT threshold. Strong corroborating signal: the firm *"prefers to pick new grads from top schools for internships and give them return offers"*, which is why external new-grad seats are scarce and the external FT bar is correspondingly brutal.

---

## 10. Quant Trader and Quant Researcher tracks

Evidence here is thinner and more intern-weighted. Flagging honestly.

### Quant Trader [CitSec]
- Pipeline: **OA → two phone interviews (1st behavioral+technical, 2nd predominantly technical) → superday.** [MEDIUM]
- OA: **15 questions in 30 minutes**, multiple choice, probability + logic brainteasers + math, **no calculator**; *"far from hard, but the time pressure is high."*
- Separate **mental-math screen: 60–80 questions in 8 minutes, no calculator, no scratch paper, pass bar ~70–85%.** [WEAK — techinterview.org; the specific numbers are unverified.]
- Superday: **market-making games where you track your orders and PnL under time pressure**; two-ropes-burning, EV dice. Notably: *"trading game rounds involve a **sequence of competitive games where your score accumulates across multiple rounds, with the end state of each game feeding into the start of the next**."*
- **That accumulating-state game structure is the trading-track mirror of the SWE "one continuous problem" onsite** — same design philosophy: compounding consequences, no reset. [My inference, MEDIUM.]
- **No FT-vs-intern trader delta found.** One source states plainly: *"the search results don't explicitly distinguish differences between full-time and intern interview structures; they appear to follow similar stages."* [GAP]
- https://www.tradinginterview.com/courses/company-preparations-course/lessons/citadel-securities/
- https://everythingquant.com/guides/quantitative-trader-at-citadel/

### Quant Researcher [CitSec]
- Campus QR first round: **45–60 min, CoderPad, Python or C++**, technical + behavioral. Official. [STRONG]
- Campus QR second round: **onsite, three to five 60-minute interviews**, technical + behavioral mix. Official. [STRONG] — note this is **longer than the 3×45 campus SWE superday**, so QR is already heavier at campus level.
- Technicals commonly: **two ~60-min sessions — first probability/statistics, second coding in a shared editor.** Plus statistics on **evaluating trading strategies**.
- **The research presentation:** *"Candidates are asked to **share their research experience followed by Q&A**, and one candidate reported **discussing their research for approximately 40 minutes**."* — https://www.glassdoor.com/Interview/Citadel-Securities-Quantitative-Researcher-Interview-Questions-EI_IE1443495.0,18_KO19,42.htm
- **Crucially, the ~40-minute research deep-dive was found on the Quantitative Researcher (full-time/PhD) page, not the PhD Intern page.** The intern-side QR advice is softer: *"reflect on how your past internship or research experience contributed to business outcomes."*
- **Verdict on the user's question:** the evidence is **consistent with** a substantive research presentation being an FT/PhD-graduate feature, and it is at minimum far more heavily weighted there. But I could **not** find a source stating PhD interns are exempt. **[MEDIUM — do not treat as settled.]**
- FT QR PhD base salary band published at **$235,000–$300,000**; PhD internship is **11 weeks, $4,500–$5,800/week**.
- https://www.citadelsecurities.com/careers/details/quantitative-researcher-phd-graduate-us/
- https://www.citadelsecurities.com/careers/details/quantitative-researcher-phd-intern-us/

### CitSec vs Citadel HF flavour
*"Citadel Securities interviews tend to be **heavier on coding and systems thinking**, compared to Citadel hedge fund interviews which lean more towards **statistics**; the coding depth / markets / probability mix shifts by team."* [MEDIUM]

---

## 11. What full-time candidates get rejected for that interns don't

Synthesised. Items 1–6 are FT-only failure modes with no intern analogue.

1. **No team wants you.** Post-superday team matching is a genuine terminal state — recruiter says "no teams wanted them." Driven by *fit of specific past experience* to a specific desk. Interns are placed. **[STRONG]**
2. **Your resume's C++ claim doesn't survive audit.** Listing C++ invites `std::variant`, iterator invalidation, move semantics, template metaprogramming, variadic templates, STL implementation internals, memory model, C++20/23. An intern is not assumed to own these; **an FT candidate who wrote "C++" is.** **[STRONG]**
3. **Design decisions that compound.** The one-problem onsite means a poor hour-1 abstraction is still being punished in hour 5 by the same interviewers. Interns get three independent shots. **[STRONG]**
4. **Cannot comprehend unfamiliar code.** The code-review / obfuscated-C++ hour has no intern equivalent. **[MEDIUM]**
5. **System design failure.** Especially failure to absorb mid-round requirement changes — the round is explicitly built to mutate. Not tested on interns. **[MEDIUM]**
6. **Behavioral: blame diffusion and vagueness.** "The team ran into challenges" / "factors outside my control" is an explicit negative. Interns are not asked to own a production failure. **[MEDIUM]**
7. **"Too junior for experienced hire"** while also disadvantaged for new grad — the 1–2 YOE squeeze. **[MEDIUM]**
8. **Faster, earlier elimination.** Rejection the next morning after round 1; EM "vibe check" screen-outs; the single-fail dynamic. **[MEDIUM]**
9. **Background/reference due diligence at offer stage** — *"does a lot of due diligence"* — a late-stage FT-only risk. **[WEAK]**
10. **Shared with interns (not a delta, but still the top killer):** suboptimal-but-correct solutions fail hidden test cases; ~36% hard question mix; live CoderPad with no autocomplete or test harness; and you must narrate while typing.

---

## 12. Confidence summary and open gaps

**Well-supported:**
- The FT onsite is a single continuous ~5h problem (1h design / 2h code / 1h code review / 1h behavioral) with the same interviewers, vs 3×45min independent intern rounds. **This is the central delta.**
- C++ depth (STL internals, `std::variant`, iterators, move semantics, memory model) is FT-loop content and is triggered by your resume.
- Team matching is a real post-superday gate that FT candidates genuinely fail.
- An obfuscated / messy-code comprehend-and-optimise task exists on the C++ track.
- 65–75% intern conversion.
- Experienced hires add a system design round and a technically-graded ownership behavioral round.

**Under-supported — treat as hypotheses:**
- The obfuscated round is **1 hour**, not 2. The "2-hour" figure is almost certainly the *coding* block.
- Whether the code-review hour reviews *your* code or *foreign* code (both are attested; likely track-dependent).
- Whether interns face the single-fail policy — **no evidence either way.**
- Whether returning interns skip stages — **no evidence; the one relevant quote suggests thresholds differ and extra interviews may be required.**
- Whether QR PhD interns get the research presentation — the ~40-min deep-dive is attested on the FT/graduate side only.
- FT vs intern delta for Quant Trader — **no evidence found.**

**Sourcing health warning:** because every forum was fetch-blocked, all Blind / Glassdoor / LeetCode / 1point3acres material here is **second-hand via search snippets**. Several supporting aggregators are AI-generated. The claims I marked STRONG are those that appear in official process language or recur across independent source families; anything MEDIUM or WEAK should be re-verified by reading the linked threads directly from an unrestricted network before acting on it.

---

## Source index

**Official (fetch-blocked; quoted via search snippets)**
- https://www.citadelsecurities.com/careers/career-perspectives/our-engineering-interview-process/ — Experienced Professionals: Engineering
- https://www.citadel.com/careers/career-perspectives/our-engineering-interview-process/ — Campus Engineering
- https://www.citadelsecurities.com/careers/career-perspectives/our-quantitative-research-interview-process/ — Campus QR
- https://www.citadelsecurities.com/careers/career-perspectives/sea-change-in-c-why-opportunities-abound/ — C++ at CitSec
- https://www.citadelsecurities.com/careers/details/quantitative-researcher-phd-graduate-us/
- https://www.citadelsecurities.com/careers/details/quantitative-researcher-phd-intern-us/
- https://www.citadelsecurities.com/careers/details/software-engineer-university-graduate-us/
- https://www.citadelsecurities.com/careers/details/c-market-data-engineer/

**Blind (candidate accounts)**
- https://www.teamblind.com/post/citadel-securities-onsite-mini-intership-0i4lizal — **the 1h/2h/1h/1h onsite**
- https://www.teamblind.com/post/citadel-securities-swe-interview-adtkpi5w — obfuscated C++
- https://www.teamblind.com/post/citadel-swe-interview-3hurnw5r — 2 phone screens + 3 onsite
- https://www.teamblind.com/post/citadel-team-matching-2jyschlo — matching success rate debate
- https://www.teamblind.com/post/citadel-team-matching-pov4rrqm
- https://www.teamblind.com/post/citadel-nxt-team-matching-d06uwg38
- https://www.teamblind.com/post/citadel-nxt-interview-canceled-skjvpdnc — cancellation
- https://www.teamblind.com/post/ghosted-by-citadel-securities-after-onsite-ejxpuxnd
- https://www.teamblind.com/post/Citadel-resume-rejected-me-Fc5dpB3g — "too junior"
- https://www.teamblind.com/post/converting-intern-offer-to-full-time-kmwh617k — differing thresholds
- https://www.teamblind.com/post/what-happens-after-citadel-securities-intern-leadership-call-bqyofmlk
- https://www.teamblind.com/post/Citadel-Securities-SWE-Intern-Return-Offer-Rate-sOWqSwTi
- https://www.teamblind.com/post/Citadel-conversion-rate-of-intern-to-full-time-VWFDa2uq
- https://www.teamblind.com/post/citadel-securities-new-grad-swe-edupk1wx
- https://www.teamblind.com/company/Citadel-Securities/posts/citadel-securities-interview

**LeetCode Discuss**
- https://leetcode.com/discuss/interview-experience/5565531/Citadel-or-Senior-Software-Engineer-or-Reject/
- https://leetcode.com/discuss/interview-experience/6972253/ — NXT, rejected next morning
- https://leetcode.com/discuss/post/7268790/ — CitSec OA, C++ Engineer
- https://leetcode.com/discuss/post/7503262/ — CitSec OA

**Glassdoor**
- https://www.glassdoor.com/Interview/Citadel-Securities-Software-Engineer-Interview-Questions-EI_IE1443495.0,18_KO19,36.htm
- https://www.glassdoor.com/Interview/Citadel-Securities-Quantitative-Researcher-Interview-Questions-EI_IE1443495.0,18_KO19,42.htm
- https://www.glassdoor.com/Interview/Citadel-Securities-Software-Engineer-Internship-Interview-Questions-EI_IE1443495.0,18_KO19,47.htm
- https://www.glassdoor.com/Interview/Citadel-Securities-Quant-Trading-Intern-Interview-Questions-EI_IE1443495.0,18_KO19,39.htm
- https://www.glassdoor.com/Interview/Citadel-Securities-Quant-Developer-Interview-Questions-EI_IE1443495.0,18_KO19,34.htm

**1point3acres (面经)**
- https://www.1point3acres.com/interview/problems/company/citadel — 122 questions
- https://www.1point3acres.com/interview/company/Citadel%20Securities
- https://www.1point3acres.com/bbs/thread-1119707-1-1.html — CitSec backend 店面挂经
- https://www.1point3acres.com/bbs/thread-1056342-1-1.html — Citadel Sec 面经
- https://www.1point3acres.com/bbs/interview/citadel-software-engineer-487988.html — 实习 oncampus + onsite
- https://www.1point3acres.com/bbs/thread-685594-1-1.html — Trading onsite
- https://learncswithus.com/2025/08/05/citadel-vo-virtual-onsite/ — NG VO 面经

**Wall Street Oasis / trading**
- https://www.wallstreetoasis.com/company/citadel-securities/interview
- https://www.wallstreetoasis.com/company/citadel-securities/interview/quant-trader-internship
- https://www.wallstreetoasis.com/company/citadel-securities/interview/quant-research-intern
- https://www.wallstreetoasis.com/forum/hedge-fund/new-grad-fundamentals-at-citadel-securities-vs-hedge-fund-0
- https://www.tradinginterview.com/citadel-securities-internship-how-to-land-an-offer/
- https://everythingquant.com/forum/post/citadel-securities-quant-trader--developer-interview-guide/
- https://everythingquant.com/guides/quantitative-trader-at-citadel/
- https://www.quantt.co.uk/resources/citadel-interview
- https://www.quantblueprint.com/guides/how-to-get-a-job-at-citadel-securities

**Press / data**
- https://fortune.com/2026/06/11/115k-young-people-applied-citadel-internships-350-made-cut-acceptance-rate-0-36/
- https://www.efinancialcareers.com/news/2023/07/interns-citadel
- https://youngandcalculated.substack.com/p/what-actually-gets-an-intern-a-return
- https://www.levels.fyi/companies/citadel/salaries

**Aggregators (lower confidence; several AI-generated)**
- https://www.interviewquery.com/interview-guides/citadel-software-engineer
- https://spacecomplexity.ai/blog/citadel-onsite-interview
- https://spacecomplexity.ai/blog/citadel-behavioral-interview-questions
- https://enginebogie.com/interview/experience/citadel-securities-software-development-engineer/1634
- https://quantvault.org/citadel-interview-process.html
- https://leonstaff.com/blogs/citadel-interview-response-time/
- https://algo.monster/interview-guides/citadel
- https://nodeflair.com/companies/citadel/interviews/c-developer
- https://simplify.jobs/blog/citadel-new-grad-job-2027
- https://medium.com/@adityashrivastava2003/citadel-securities-swe-intern-singapore-interview-experience-386dc70fc1eb
- https://www.techinterview.org/companies/citadel-securities/ — source of "single-fail" phrasing; treat with caution
- https://www.techscreen.app/articles/citadel-technical-interview-process-2026
