# Jane Street: Full-Time / Experienced-Hire Interview vs. Internship Interview

**Research date:** 2026-09-08
**Scope:** What *changes* for full-time (FT) / experienced hires relative to the internship loop the reader already knows.

---

## ⚠️ Methodology & reliability caveat (read this first)

This sandbox blocked **all** outbound page fetches. Every attempted `WebFetch` and `curl` returned
`EGRESS_BLOCKED` / `CONNECT tunnel failed, 403`, including:
`blog.janestreet.com`, `www.janestreet.com`, `teamblind.com`, `1point3acres.com`, `tryexponent.com`,
`spacecomplexity.ai`, `four-leaf.ai`, `news.ycombinator.com`, `jointaro.com`, `interview.norahq.com`.

So **everything below is reconstructed from search-engine result summaries**, not from reading the primary
pages. URLs are given so the user can verify directly. Two consequences:

1. Where a claim comes from **Jane Street's own words** (their blog / careers pages), I mark it **[JS-OFFICIAL]**
   and it is high-confidence, since the search summary quoted the page.
2. Where a claim comes from an **SEO interview-prep aggregator** (spacecomplexity.ai, tryexponent/Aced,
   norahq, techprep, prachub, dataford, leonstaff, algo.monster, gitgood, deep-ml, getcracked, quantprep),
   mark it **[AGGREGATOR — LOW CONFIDENCE]**. These sites are largely LLM-written, they cite each other,
   and several of the crisp-sounding numbers below (e.g. "75 minutes", "40% of onsites end early",
   "four scoring criteria") appear only in that ecosystem and could not be corroborated against a
   first-hand candidate post. Treat those as *plausible folklore*, not fact.
3. **Blind / Glassdoor / 1point3acres / Reddit were only visible as titles + a summarizer's paraphrase.**
   I could not read individual threads. First-hand claims are labelled **[SECONDHAND]**.

The search-call budget (200/session) was consumed partway through, which cut short planned follow-ups on
(a) the exact scope of Jane Street's official "Deep Dive" page and (b) experienced *trader* laterals.

---

## 1. Pipeline differences (intern → full-time)

### The one difference Jane Street itself states

**[JS-OFFICIAL]** From *The Jane Street Interview Process — 2020 Edition* and *Interviewing At Jane Street*:

> "For more experienced candidates, we may do an **additional non-technical phone interview** to discuss
> what you're looking for and to give you a chance to ask any questions you have about Jane Street.
> On site, we may ask you to **talk about your past experience**, or conduct **interviews that aren't our
> standard technical questions**."

- https://blog.janestreet.com/jane-street-interview-process-2020/
- https://blog.janestreet.com/interviewing-at-jane-street/
- Third-party recap: https://four-leaf.ai/blog/jane-street-interview-process

That is the load-bearing, firm-sourced delta: **(a) an extra non-technical call, (b) a past-experience /
non-standard round on the onsite day.** Everything else in this document is community reconstruction of
what (b) has become in practice.

### Reconstructed shape of each loop

| | **Intern (SWE)** | **Full-time / experienced (SWE)** |
|---|---|---|
| Recruiter call | ~30 min | ~30 min, **plus** a separate non-technical call for experienced candidates **[JS-OFFICIAL]** |
| Technical screens | 1 screen, ~45 min, CoderPad/Zoom | **1–2** screens, ~45–60 min each **[AGGREGATOR/SECONDHAND]** |
| Onsite rounds | **3** collaborative coding rounds | **4** rounds (typically 3 coding + 1 project deep-dive for senior; 4 coding for new grad) **[AGGREGATOR]** |
| Onsite length | ~half day | **~5–6 hours**, rounds ~60–75 min **[AGGREGATOR]** |
| Interviewers/round | often 1–2 | ~2 per round ("one leads, one takes notes") **[AGGREGATOR / one first-hand-ish Exponent write-up]** |
| Dedicated system-design round | no | **still no** — design is folded into coding rounds |
| Behavioural | minimal | minimal; HR/"why Jane Street" exists but is light |
| Team matching | assigned | **after** the loop — centralized hiring, then matched **[AGGREGATOR]** |

Sources for the round counts:
- https://spacecomplexity.ai/blog/jane-street-onsite-interview ("onsite runs five to six hours across four
  rounds… senior candidates replace Round 4 with a project deep dive")
- https://www.tryexponent.com/guides/jane-street-software-engineer-intern-interview ("Interns skip the
  project deep dive that senior candidates face in the full-time … interview")
- https://www.tryexponent.com/guides/jane-street-software-engineer-interview
- https://interviewing.io/jane-street-interview-questions
- https://www.teamblind.com/post/jane-street-onsite-interview-swe-0uhhwcc2 (paraphrased: "four rounds in
  total … 3 rounds instead of 4 during the onsite for some candidates")

**Caveat on round counts:** the numbers wobble across sources (3–5 onsite rounds). The aggregators
themselves hedge: *"the exact number of onsite rounds varies by candidate, level, team, and office."*
The only stable signal is **FT loops are one round longer than intern loops, and the extra round is the
past-experience/deep-dive round**.

### System design specifically

- No standalone system-design round in the SWE loop, for intern **or** FT.
- Design shows up *inside* coding rounds: "they blend coding and system design so you might have to
  whiteboard out some pieces initially before jumping into code."
  https://interviewing.io/jane-street-interview-questions
- A Blind thread exists titled "Jane Street On-site System Design"
  (https://www.teamblind.com/post/Jane-Street-On-site-System-Design-6F2c4Jxk) — could not read it.
- Aggregator claim: the only design-flavoured questions logged are trading-domain
  (exchange message flow; validating order-book data across databases). **[AGGREGATOR]**

### Turnaround times

From https://leonstaff.com/blogs/jane-street-interview-response-time/ **[AGGREGATOR]**:
- Application → recruiter: a few days to a week.
- After a phone screen: **3–7 days**, because Jane Street batches decisions into a **weekly (or twice-weekly)
  debrief meeting**. Interviewers do not decide individually. So a Thursday interview with a Monday debrief
  = ~5 days regardless of performance.
- After onsite: **same-day decision, most hear within 24 hours.**
- End-to-end: 3–6 weeks typical. **SWE intern pipelines are reported as *slower* (~100 days, because they
  run on a campus calendar); experienced senior hires can go start-to-offer in under a week** when the
  recruiter prioritises it.
- Glassdoor-derived average across all Jane Street roles: ~17 days; SWE-Intern-specific: ~19 days.
  https://www.glassdoor.com/Interview/Jane-Street-Interview-Questions-E255549.htm

**Delta:** FT/experienced is *faster in wall-clock* than the intern cycle (no campus calendar), but has one
more batching gate (the extra non-technical call).

---

## 2. The project deep-dive / "walk through a system you built" round

This is the single biggest structural difference, and Jane Street has an **official page** for it:
**https://www.janestreet.com/join-jane-street/interviewing-deep-dive/**

**[JS-OFFICIAL]** (quoted through search summaries of that page):

- **Choose the problem yourself, in advance.** "Identify a problem you want to discuss" — pick a challenge
  where *you* contributed to meaningful solutions, and one **recent enough that the specifics are fresh**.
- **Prepare by re-walking the process, not the outcome.** "Be sure you can remember technical details,
  timelines, and interesting decisions and tradeoffs. The best way to prepare is to reflect on the process
  of solving that problem — from before you started (what motivated the team to tackle this problem?) to
  after you finished (what were the long-term effects of the solution?)."
- **Do NOT over-prepare.** "Please don't over-prepare. We don't want you to give us a PowerPoint
  presentation or consult a detailed set of notes. We'd much rather have a natural conversation with you."
- **IP / confidentiality:** "If intellectual property concerns may prevent you from sharing some details,
  let your interviewers know. If you need to keep many details of the problem and solution private, then it
  makes sense to choose a different topic for your deep dive interview."

(Note: I could not verify whether this page is scoped to the SWE track, the Strategy & Product track, or
firm-wide — one search hit associated the URL with S&P interviewing
(https://www.janestreet.com/join-jane-street/sp/interviewing). **Verify this before relying on it.**)

**Community layer on top [AGGREGATOR + one Exponent candidate write-up]:**
- Format: **conversational, on the onsite day, ~75 minutes, built around one past project**, two interviewers.
- Who gets it: "senior and staff candidates"; it **replaces a coding round** rather than adding to the day.
  Some sources describe it more loosely as "full-time" rather than strictly senior.
  https://www.tryexponent.com/experiences/jane-street-senior-software-engineer-interview-d9cb42
- **Aggression of follow-ups:** described consistently as *casual in tone, deep in probing*. Reported phrasing:
  "a pretty probing project discussion **full of why questions**"; "interviewers push hard on your decisions:
  why this data structure, what you'd change, what the tradeoffs were"; "what was happening in the systems
  next to yours."
- **The named failure mode:** *"If your answer to 'why did you choose this approach' is 'it was the first
  thing I thought of,' that's not good."* The round tests "whether you actually understand your own systems
  — or whether you're summarizing what your team built."
- **Bring more than one project.** "Interviewers may steer you toward one you haven't polished."
- **Being candid about gaps beats a scripted answer** — same "know what you don't know" calibration norm
  that runs through the whole Jane Street loop.

**Practical prep implication (synthesis):** the failure mode is *narrating* rather than *owning*. Prepare
2–3 systems; for each be able to state the motivating constraint, at least two design alternatives you
rejected and why, the specific data-structure/consistency/latency tradeoff, what broke in production, what
you'd change now, and one honest "I still don't know why X behaved that way." A slide deck or notes is
explicitly counter-signal.

**Related:** one 1point3acres FT report describes a five-round loop that included a **"resume deep dive"**
alongside a take-home, HR call, numeracy challenge and technical rounds —
https://www.1point3acres.com/interview/thread/1134748 **[SECONDHAND]**. That looks like a non-SWE or
non-US variant; flagging it because it shows the past-experience round is not uniformly implemented.

---

## 3. Difficulty delta: harder questions, or the same questions with a higher bar?

**The evidence points to: essentially the same question *style*, with the delta showing up in (a) how many
escalation steps you're expected to reach and (b) the resume/track-record bar, not in a different question bank.**

### The question format is level-invariant
Both loops use the same signature structure — one underspecified, multi-part problem that escalates:
- Part 1: base implementation "most passing candidates can do quickly."
- Part 2: interviewer points out a flaw in your Part 1 (usually memory or performance) — fix it.
- Part 3: "which you may or may not reach" — push to a more elegant/optimal solution.
- Canonical published example: **"Memo"** — write a memoized wrapper over an expensive function with a hash
  table → bound memory with **FIFO eviction in O(1)** → upgrade to **LRU**, as efficiently as possible.
  https://blog.janestreet.com/what-a-jane-street-dev-interview-is-like/
- New constraints land roughly **every 10–15 minutes**. **[AGGREGATOR]**

**So "more escalation steps for full-time candidates" is real but implicit**: the parts are the same;
FT/senior candidates are simply expected to get further into Part 2/Part 3 and to articulate the invariants.
I found **no source stating an explicitly different rubric or scored bar by level.**

### Stated evaluation criteria (same for everyone)
**[JS-OFFICIAL, paraphrased]**: what matters is "how you approach it, what you're able to learn, and how
you're able to apply that to something more complex" — plus courtesy: *"the smartest, most technically clever
person won't get hired at Jane Street if they aren't courteous and pleasant to talk to."*
Aggregators compress this into four criteria — **be nice, be clear, know your language, know what you don't
know** — with "process beats outcome: going silent or shipping a buggy Part 1 hurts more than not finishing
the hardest extension," and "hint responsiveness is scored: taking a nudge and running with it is a positive
signal, not a concession." **[AGGREGATOR — the four-item list is uncorroborated phrasing]**

### Where the bar genuinely differs
- **[SECONDHAND, Blind]** "The interview bar for interns and new grads at Jane Street is **about the same**,
  though most new grad hires are former interns."
- **[AGGREGATOR]** "The interview content is similar but **the bar on extracurricular signals (open source,
  competitive programming, prior internships) is lower for interns.**"
- **[SECONDHAND, Blind]** The *practical* bar is different because of supply: "it's much harder to get a
  full-time offer if you haven't interned at a quant firm first"; going straight for new grad "with no quant
  experience under your belt will be tough." Several posters explicitly reason that **taking the intern route
  is the easier path to the same destination** precisely because the FT funnel is thinner.
  https://www.teamblind.com/post/jane-street-swe-internship-instead-of-new-grad-0jsid3xz
  https://www.teamblind.com/post/jane-street-new-grad-offer-without-internship-riqak0yd

**Bottom line for the user:** don't prepare *harder* problems. Prepare to (i) reach Part 3 more often,
(ii) survive an hour of "why" on your own past work, and (iii) accept that resume screening is stricter.

### Round length
Intern coding rounds ≈ 60 min, intern screen ≈ 45 min; FT screens 45–60 min and FT onsite rounds reported at
60–75 min. So FT rounds are somewhat longer — consistent with "more escalation steps per problem."
**[AGGREGATOR]**

### One widely-repeated claim I could not verify
"Roughly **40% of onsites end early** — if morning rounds don't clear the bar the recruiter closes the day
after lunch and tells you on the spot." Appears in aggregator content only. **Treat as unverified.**

---

## 4. Experienced (2–5 yrs) vs. new-grad full-time; senior/staff loops

- **New grad FT ≈ intern loop + one round.** Aggregators consistently say new grads get **four coding
  rounds** and **no project deep dive** (they have no owned system to dive into); it is senior candidates who
  swap Round 4 for the deep dive. https://spacecomplexity.ai/blog/jane-street-onsite-interview
- **Experienced (industry) hires** get: the extra **non-technical call** **[JS-OFFICIAL]**, the
  **past-experience round** **[JS-OFFICIAL]**, and possibly "interviews that aren't our standard technical
  questions" **[JS-OFFICIAL]** — i.e. the loop is explicitly allowed to be *tailored to the individual's
  profile*, which is exactly what an experienced Blind poster was asking about
  (https://www.teamblind.com/post/jane-street-experienced-hire-interview-process-swe-riuyrkgz).
- **Quant researcher** loops are stated to be "**3–5 rounds, depending on role seniority and office**" —
  the clearest explicit seniority-scaling statement I found.
  https://www.datainterview.com/blog/jane-street-quantitative-researcher-interview
- **Levels:** Jane Street SWE is tracked on Levels.fyi as **L1–L4**, plus an "Experienced Hire" hiring
  category — so leveling does exist despite the firm's flat-title reputation.
  https://www.levels.fyi/companies/jane-street/salaries/software-engineer
- **Reapplication:** Jane Street encourages reapplying "after a year (for students) or after meaningful
  experience growth (for industry candidates)" — an explicitly *different* cooldown framing for experienced
  candidates. https://www.janestreet.com/join-jane-street/interviewing/
  Related Blind threads: https://www.teamblind.com/post/jane-street-swe-reinterview-nhksieh0 ,
  https://www.teamblind.com/post/jane-street-cooldown-ot6smada

**Gap:** I found **no** evidence of a distinct "staff" loop with e.g. an architecture or leadership round.
Everything above senior appears to be the same four-round day with the deep dive.

---

## 5. Return offers — conversion rate and whether returners skip stages

- **Conversion widely reported at >80%**, materially above the 50–70% typical of peer quant firms.
  - https://youngandcalculated.substack.com/p/how-to-land-a-quant-internship-in
  - https://www.quantt.co.uk/resources/jane-street-internship
  - https://www.extern.com/post/jane-street-internship-guide
  - Blind, May 2024, re: summer 2023 cohort — a reply paraphrased as *"I think it was like 80% last year"*:
    https://www.teamblind.com/post/did-jane-street-give-return-offers-to-interns-rwkvrtno
  - Some sources give 80–95% for "top interns"; broader community estimates as low as 50–70%.
  - **Office variance:** Hong Kong has reportedly run nearer **50%**. **[AGGREGATOR]**
- **Stated philosophy:** *"we hire interns we expect to convert"* — the bar is set at the internship
  interview so most interns are expected to succeed. **[AGGREGATOR paraphrase of JS positioning]**
- **Returning interns do NOT re-interview.** The decision is made in the **final two weeks** of the
  internship from manager feedback on what you shipped and its quality, peer feedback, and a formal
  end-of-internship review (~30-minute meeting with your manager plus one or two senior people).
  **The internship *is* the loop.** If offered, you typically have until the end of the calendar year to accept.
- **The internship is the dominant graduate-hiring channel** — "most new grad hires are former interns."
  This is the real reason the FT funnel is harder: fewer seats.

**Not established:** what happens to an intern who does *not* convert and reapplies FT, or to someone who
interned elsewhere. No source addressed stage-skipping for those cases.

---

## 6. What full-time candidates get rejected for (differing failure modes)

Evidence here is thin and mostly inferential. What exists:

**Failure modes shared with interns:**
- Solving silently. "Solving silently hides your reasoning and weakens the collaborative signal."
- Buggy or incomplete Part 1; missing major edge cases. A recruiter-sourced note reported on Levels.fyi
  community: *"the minimum expectation is a mostly complete and working implementation, and missing major
  edge cases means failing the interview."*
  https://www.levels.fyi/community/thread/5EXTXr/jane-street-interview-process
- Not converting stated reasoning into code. Glassdoor-derived reports describe candidates who "explained
  their thinking in detail but failed to translate it into code."
  https://www.glassdoor.com/Interview/Jane-Street-Software-Engineer-Interview-Questions-EI_IE255549.0,11_KO12,29.htm
- Being unpleasant / defensive when a hint or a requirement change arrives.
- **Misprepping the wrong track:** the most-cited prep error is treating the SWE loop like the trader loop
  (probability brainteasers, mental math). The SWE loop is *not* mathy.

**Failure modes that are FT-specific (all trace back to the deep dive):**
- **Cannot justify your own design decisions.** "It was the first thing I thought of" is called out
  explicitly as a bad answer.
- **Credit ambiguity / summarizing the team's work** rather than your own. The round is designed to
  distinguish "I built this" from "I was on the team that built this."
- **Stale project choice.** JS's own guidance to pick something *recent enough that specifics are fresh*
  implies candidates fail on forgotten details.
- **Over-rehearsal.** JS explicitly says no deck, no notes — a polished pitch reads as counter-signal.
- **IP wall.** Choosing a project you can't actually describe, then stonewalling.
- **Track record / resume bar** (pre-interview rejection): FT candidates without prior quant-firm experience
  are filtered much harder than intern applicants, who are not expected to have one.

**Onsite outcomes:** Glassdoor rates the SWE interview **3.5/5 difficulty** with **~58% positive** experience
sentiment. Rejections are commonly reported with **no feedback** — recruiter simply invites reapplication.

---

## 7. Quant Trader and Quant Researcher: FT vs. intern

### Quant Trader
- **Explicit statement found:** *"The interview content for the internship is the same as the full-time
  graduate process, so the preparation is the same."*
  https://www.quantt.co.uk/resources/jane-street-interview and
  https://www.janestreet.com/trading-interviews/
  → **For traders there is essentially no intern/new-grad-FT delta.** This is the sharpest contrast with SWE.
- Shape (both): 3-stage process — human resume read (not software-screened); **2–3 conversational phone
  calls built around a linked series of betting/strategy games**; then a full day (office or Zoom) of trader
  interviews plus an HR conversation. Recent intern reports: two interviews before lunch, three after
  (one behavioural).
- Content: probability, EV, combinatorics, estimation, market-making games ("I'm thinking of a number
  between 1 and 100 — make me a market"), game theory. Pen and paper. No finance background required.
- **Experienced/lateral traders:** **no evidence found.** Searches for lateral trader hiring returned only
  campus-track material. Genuine gap.

### Quant Researcher
- **3–5 rounds, scaling with seniority and office** — the clearest seniority signal in any track.
  https://www.datainterview.com/blog/jane-street-quantitative-researcher-interview
- Shape: phone screen on math/probability → 1–2 further technical rounds → full onsite.
  2–3 puzzles per 45–60 min round, plus mental math, intro market making, light behavioural.
- Content skews to probability, time-series analysis, experiment design; Python expected, willingness to
  learn OCaml valued.
- Timeline: **4–8 weeks** first contact → offer (slower than SWE).
- **[AGGREGATOR]** notes the same "calibration" norm the SWE loop has: *"I'm about 70% confident the answer
  is X, here's why"* outperforms a confident wrong answer.
- **No evidence of a research/publication deep-dive round** analogous to the SWE project deep dive. Searched
  for it specifically; nothing surfaced. Cannot rule it out for experienced QR hires.
- Relevant unread thread:
  https://www.teamblind.com/post/what-should-i-expect-in-a-jane-street-quantitative-researcher-onsite-interview-3thj8ftb

---

## Open questions / what I could not establish

1. Whether **janestreet.com/join-jane-street/interviewing-deep-dive/** applies to the SWE track or only to
   Strategy & Product. **Highest-value single thing to check.**
2. Whether new-grad FT candidates ever get the deep dive (sources split between "senior" and "full-time").
3. Whether the coding rubric is formally level-differentiated, or whether interviewers just calibrate.
4. Experienced/lateral **trader** hiring process — nothing found at all.
5. Whether an intern who didn't convert, or an intern from another firm, skips any FT stage.
6. Verification of the "40% of onsites end early" and "75-minute rounds" figures.

---

## Source index

**Jane Street primary (all blocked from fetch; quoted via search summaries)**
- https://blog.janestreet.com/jane-street-interview-process-2020/ — the experienced-candidate delta
- https://blog.janestreet.com/interviewing-at-jane-street/
- https://blog.janestreet.com/what-a-jane-street-dev-interview-is-like/ — the "Memo" problem
- https://www.janestreet.com/join-jane-street/interviewing-deep-dive/ — official deep-dive guidance
- https://www.janestreet.com/preparing-for-a-software-engineering-interview/
- https://www.janestreet.com/join-jane-street/interviewing/
- https://www.janestreet.com/trading-interviews/
- https://www.janestreet.com/join-jane-street/internships/
- https://www.janestreet.com/mock-interview/

**Community (titles + paraphrase only)**
- https://www.teamblind.com/post/jane-street-experienced-hire-interview-process-swe-riuyrkgz
- https://www.teamblind.com/post/jane-street-onsite-for-experienced-swe-dhrbm4ta
- https://www.teamblind.com/post/jane-street-onsite-interview-swe-0uhhwcc2
- https://www.teamblind.com/post/Jane-Street-On-site-System-Design-6F2c4Jxk
- https://www.teamblind.com/post/jane-street-swe-reinterview-nhksieh0
- https://www.teamblind.com/post/jane-street-cooldown-ot6smada
- https://www.teamblind.com/post/jane-street-swe-internship-instead-of-new-grad-0jsid3xz
- https://www.teamblind.com/post/jane-street-new-grad-offer-without-internship-riqak0yd
- https://www.teamblind.com/post/did-jane-street-give-return-offers-to-interns-rwkvrtno
- https://www.teamblind.com/post/what-should-i-expect-in-a-jane-street-quantitative-researcher-onsite-interview-3thj8ftb
- https://www.1point3acres.com/bbs/thread-1103369-1-1.html — "全网最全 Jane Street SWE 面试资料收集 | 社招 | junior→senior"
- https://www.1point3acres.com/interview/thread/1155567 — London FT SWE onsite (Nov 2025)
- https://www.1point3acres.com/interview/thread/1156657 — FT SWE video interview
- https://www.1point3acres.com/interview/thread/1134748 — five-round loop incl. resume deep dive
- https://www.1point3acres.com/interview/thread/945017 — NG VO + timeline
- https://www.levels.fyi/community/thread/5EXTXr/jane-street-interview-process
- https://www.glassdoor.com/Interview/Jane-Street-Software-Engineer-Interview-Questions-EI_IE255549.0,11_KO12,29.htm
- https://www.glassdoor.com/Interview/Jane-Street-Interview-Questions-E255549.htm
- https://www.wallstreetoasis.com/company/jane-street-capital/interview
- https://news.ycombinator.com/item?id=18039806

**Aggregators (treat as low confidence)**
- https://www.tryexponent.com/guides/jane-street-software-engineer-interview
- https://www.tryexponent.com/guides/jane-street-software-engineer-intern-interview
- https://www.tryexponent.com/experiences/jane-street-senior-software-engineer-interview-d9cb42
- https://spacecomplexity.ai/blog/jane-street-onsite-interview
- https://spacecomplexity.ai/blog/jane-street-software-engineer-interview
- https://interviewing.io/jane-street-interview-questions
- https://leonstaff.com/blogs/jane-street-interview-response-time/
- https://www.datainterview.com/blog/jane-street-quantitative-researcher-interview
- https://www.quantt.co.uk/resources/jane-street-interview
- https://www.quantt.co.uk/resources/jane-street-internship
- https://www.extern.com/post/jane-street-internship-guide
- https://youngandcalculated.substack.com/p/how-to-land-a-quant-internship-in
- https://four-leaf.ai/blog/jane-street-interview-process
- https://www.levels.fyi/companies/jane-street/salaries/software-engineer
