# Quadrature Capital (London) — Internship Research

**Research date:** 2026-09-08

## Method and reliability caveat (read first)

**Direct page fetching was almost entirely impossible in this session.** The egress proxy blocked
every relevant host: `quadrature.ai`, `glassdoor.com`/`.co.uk`, `teamblind.com`, `levels.fyi`,
`reddit.com`, `thestudentroom.co.uk`, `wallstreetoasis.com`, `leetcode.com`, `1point3acres.com`,
`gradcracker.com`, `brightnetwork.co.uk`, `targetjobs.co.uk`, `builtin.com`, `openquant.co`,
`greenhouse.io`, `linkedin.com`, `efinancialcareers.com`. Only `github.com` /
`raw.githubusercontent.com` were reachable.

So almost everything below comes from **search-engine result summaries** that quote or paraphrase
those blocked pages, plus **two GitHub READMEs** I fetched in full. That means:

- Quotes marked "verbatim" are verbatim *as relayed by the search summary*, not as I read them on the
  source page. Treat them as high-confidence-but-one-step-removed.
- I could not count Glassdoor entries, read full review text, or verify per-job-title statistics.
- The web-search budget ran out at ~35 searches, so a handful of planned queries (Quadrature's own
  internships page wording, application deadlines, Gradcracker/Bright Network/TargetJobs listings)
  went unrun.

**The evidence base is genuinely thin.** Quadrature has ~19 Glassdoor reviews and roughly 24
interview entries *company-wide, across all roles*. Intern-specific data points number in the
single digits. Where I found nothing, I say so rather than generalising.

---

## 1. The internship programme (facts)

| Item | Detail | Source confidence |
|---|---|---|
| Duration | 11 weeks, summer | High — stated on Quadrature's own site, repeated across job boards |
| Locations | London and New York | High |
| Tracks | Quant Development (Research; Technology) and Core Technology (Systems Engineering, Platform Engineering) | High |
| Eligibility | Undergrad and postgrad | High |
| Hiring window | Applications Sept → Dec/Jan (sources disagree: "September until January" vs "September–December") | Medium |
| Pay | Paid, "competitive"; levels.fyi lists SWE Intern at **$117.39/hr ≈ $20,348/mo**, Summer 2024, undergrad sophomore level, London | Medium (single levels.fyi datapoint) |
| Housing | Fully serviced apartments near the office, provided | High |
| Mentoring | "Every intern has two mentors and one or two real projects (no toy projects)" | Medium (single Glassdoor review) |

Notable eligibility signal from a candidate report: **Quadrature "does not accept first-year
students, especially if not studying computer science."** Programming experience is described as
mandatory for the Quant Developer internship, but markets/finance background explicitly is not.

Sources:
- https://www.quadrature.ai/careers/internships/ (blocked; via summaries)
- https://www.levels.fyi/internships/Quadrature-Capital/Software-Engineer-Intern/
- https://openquant.co/job/2026-internships-quant-developer-research-quadrature-capital/2526

---

## 2. The intern pipeline — what I could establish

Reconstructed pipeline (composite; **no single source describes the whole intern loop**):

1. **CV + cover letter** via Greenhouse. Quadrature says it aims to respond within 48 hours but
   warns it cannot always respond individually given volume.
2. **Phone/video screen, 15–45 min.** Quadrature's own "How we hire" page: 20–45 min with Strategic
   Growth (their recruiting team) or the hiring team; covers experience, aspirations, interest in
   Quadrature; "some roles include a few technical questions."
   - One candidate report is more specific and shorter: **"a 15-minute phone call ... asked basic
     questions about their background and CV statements,"** then candidate Q&A about the internship.
   - Another intern report describes this stage as a straight **HR interview**: CV, why the job,
     previous experience, why Quadrature, how you heard about them.
3. **A coding assessment.** Two conflicting descriptions:
   - **"Supervised coding task"** — reported as the round following the HR screen for an intern
     (Aug 2025 interview).
   - **"Skills test"** — prior research finding; consistent with the above.
   - I found **no evidence of a HackerRank / CodeSignal / Codility branded OA** for Quadrature.
     Searches for this returned nothing Quadrature-specific. The evidence points to a *live,
     supervised* coding exercise rather than an unproctored platform test.
4. **Onsite / interview loop.** Quadrature's own site: London office, a morning or afternoon,
   meeting **2–3 people** from the team on technical or case-study questions; **"two or three rounds
   of onsite interviews"** overall.
   - Prior research's **"four interviews consisting of algorithmic and implementation questions"**
     is consistent and I found nothing contradicting it.
   - One summary of the intern path: **"1–2 rounds with Quants, a coding test, and a final
     interview."**

**Take-home for interns: unresolved.** One summary listing intern-relevant topics mentions "a
take-home project, HR interview, and calls with researchers from different teams," but I could not
confirm the take-home applies to the internship rather than being pulled from full-time entries on
the same Glassdoor page. See §4.

### Timeline

- Quadrature company-wide Glassdoor average: **49 days**, from only **6 user-submitted interviews**
  across all job titles. The same 49-day figure is *also* reported on the Software Engineer
  Internship page — most likely because Glassdoor shows the company-wide average there, not an
  internship-specific one.
- **The "~21 days for quant-dev interns" figure in prior research looks wrong.** When I probed it,
  the 21-day number that surfaced was **Apple Inc.'s** hiring average, shown on Glassdoor as a
  comparison tile on the Quadrature page. I would not report 21 days as a Quadrature figure without
  someone reading the page directly.
- One candidate reported the whole process took **2 weeks** (London, Aug 2025).
- Difficulty: **3.2 / 5** company-wide; **50% positive** experience rating. Software Engineer
  Internship interviews were rated **the easiest** of Quadrature's role types; Quantitative
  Developer Intern also flagged as among the easier ones.

Sources:
- https://www.quadrature.ai/careers/how-we-hire/ and https://quadrature.ai/careers/recruitment
- https://www.glassdoor.com/Interview/Quadrature-Interview-Questions-E1013879.htm
- https://www.glassdoor.com/Interview/Quadrature-Software-Engineer-Internship-Interview-Questions-EI_IE1013879.0,10_KO11,39.htm
- https://www.glassdoor.co.uk/Interview/Quadrature-Capital-Interview-Questions-E1013879_P2.htm

---

## 3. Actual reported questions

This is the complete set I could find. It is small.

**Intern-attributed:**

1. **"Code up a queue implementation of a streaming median estimator."** — the closest thing to a
   verbatim intern question in the whole corpus. (Standard solution: two heaps, max-heap/min-heap
   balanced to size difference ≤ 1, O(log n) insert, O(1) median. The "queue" framing implies a
   *sliding-window* median, which is harder — you need lazy deletion or an indexed structure.)
2. **Binary search vs. hash map trade-offs, and how the answer changes with CPU cache behaviour.**
   (Confirmed; this is the signature Quadrature-style question — they want you to reason that a
   contiguous sorted array can beat a hash map at small n because of cache locality and pointer
   chasing, not just recite O(log n) vs O(1).)
3. **A system-design question about a stock buying/selling system.** Confirmed as an intern topic.
4. **"An implementation question related to trading."** Confirmed, no further detail found.
5. **HR/behavioural:** why this job, why Quadrature, how did you hear about us, walk through your CV,
   previous experience.

**Full-time / unattributed (useful as a proxy for style):**

6. **"A sort of LeetCode question"** — implement a data structure, with follow-ups about **working
   with files on a given machine** (i.e. moving from the abstract DS to real I/O, syscalls, page
   cache).
7. Category list from Glassdoor: **algorithms and data structures, simple maths problems, simple
   coding/programming-language questions, questions on past experience.**
8. Onsite topics: **data-structure internals, performance/memory estimation, language specifics.**

**Explicitly reported as absent:** no finance-background questions for interns; "no specific
questions on finance background" holds up — nothing I found contradicts it.

---

## 4. Intern loop vs. full-time loop

**This is the weakest part of the evidence base and I want to be blunt about it.**

What is well-supported for **full-time**:

- A **take-home test before the onsites.** But the best-documented full-time account says it was
  **1–2 hours, not 8.** Verbatim from that account: the first stage was *"a 1-2 hour test to complete
  at home"*, described as *"small but pleasant and more about tackling some real problem and
  understand/modify the code rather than the usual 'take this algorithm and write some code and unit
  tests.'"* **The "up to 8 hours" figure in prior research is not corroborated by anything I found.**
  Possible explanations: a different role, a different year, or a candidate who spent 8 hours on a
  2-hour task. Flag it as unverified.
- **Two onsite stages, 3–4 interviews per day.** Verbatim: *"2 stages of onsite interviews (3-4
  interviews a day)."* Another account: *"3 onsite interviews during one day (1 hour each) and 2
  additional interviews with directors the next day — all 5 technical."*
- **The final round ends with the CEO.** Quadrature's own site: if the first onsite round goes well,
  *"you'll be invited back to meet a few more people, ending with Aidan"* — Aidan Devane, CEO
  (ex-Boston Consulting Group). The site adds: *"you'll be meeting the leaders of the business so
  bring some questions"* and *"there's nothing you need to prepare unless specifically asked to."*

What I could establish for **interns**: a shorter loop — HR screen → supervised coding task →
roughly four technical interviews, described elsewhere as "1–2 rounds with Quants, a coding test,
and a final interview." Intern interviews are rated the easiest of any Quadrature role type.

**Do interns get the take-home?** *Unresolved.* One summary lists a take-home among intern-page
topics, but Glassdoor pages mix roles and I could not read the page to attribute it. My reading of
the balance of evidence: the intern equivalent is the **supervised/live coding task**, not the
at-home project — but this is inference, not evidence.

**Do interns meet the CEO?** *No evidence either way.* The CEO round is described on Quadrature's
general "How we hire" page, which is not internship-specific. I found no intern report of meeting
Aidan Devane. Given interns get a shorter loop with fewer rounds, I would guess not, but I have
nothing to support that.

---

## 5. The collaborative interview style

Quadrature's own framing (verbatim from their careers site):

> "You work with your interviewer to solve these problems, with the interviewer there to guide and
> brainstorm with you."

They explicitly tell candidates to **ask questions and be receptive to hints.** A candidate account
independently corroborates the tone: most questions were **open-ended** and felt like
**"sensible 2-party discussions,"** with heavy emphasis on the candidate's background, previous
projects, interests, and what they'd want to work on.

**The two-on-one session.** Fuller version of the report than prior research had:

> "A single tech interview, two-on-one, that started with a simple problem statement and continued
> with ever-shifting requirements ... no clarity about what they were looking for (tolerance for
> being messed around by non-technical people)."

Note that last parenthetical is the *candidate's own sardonic guess* at what was being tested, not
Quadrature's stated intent. But the mechanic is clear and it is the single most distinctive thing
about their process:

**How to prepare for it, based on the mechanic:**
- Expect the problem to be deliberately underspecified at the start. **Asking clarifying questions is
  scored, not tolerated.** Establish inputs, scale, latency budget, and failure modes before coding.
- Expect requirements to change mid-solution. Do not over-commit to a rigid design early. Build in a
  way that survives a new constraint — talk aloud about which parts of your design are load-bearing
  and which are swappable.
- Do not go silent. The interviewer is participating; treating them as an examiner is the failure
  mode here.
- Take hints. Multiple sources emphasise receptiveness to hints as an evaluated signal.
- Be able to justify data-structure choices on **hardware** terms (cache, memory layout,
  allocations), not just big-O — that's the through-line of their known questions.

Sources:
- https://www.quadrature.ai/careers/how-we-hire/
- https://www.glassdoor.com/Interview/Quadrature-Interview-Questions-E1013879.htm

---

## 6. Conversion and the intern experience

**No hard conversion rate exists in public.** I found no percentage, no "X of Y interns converted."
Anyone quoting one is guessing.

The one substantive signal, from a Glassdoor intern review — and it is a meaningful one:

> **"Return offer chances are dependent on which mentor you get."**

Same review set, cons: **"lack of clear feedback, especially at the end of the internship"** and a
wish to *"learn more about how internal frameworks and strategies work."*

Pros reported by interns: interesting real projects (explicitly "no toy projects"), two mentors each,
several presentations on aspects of quantitative trading, an "remarkably open" culture, approachable
colleagues, good salary and housing, game nights and monthly socials, transparent management.
Quadrature's overall Glassdoor rating is **4.7/5 across 19 reviews** (4.8 culture & values, 4.3
career opportunities) — very high, but on a tiny and probably self-selected sample.

---

## 7. The Fullhouse Hackathon

**Yes, it is a recruiting funnel, and Quadrature is the lead sponsor.** This is the best-evidenced
item in this report because I could read the source repos directly.

From the official engine repo README (verbatim):

> "The UK's first quantitative poker bot competition — 1-5 June 2026, London.
> **£4,000 prize pool · Sponsored by Quadrature Capital**"

Mechanics:
- Submit **one file, `bot.py`, with one function**: `decide(game_state: dict) -> dict`.
- 6-max, 100BB No-Limit Texas Hold'em, **Swiss tournament format**.
- Game state dict gives hole cards, community cards, street, pot, your stack, amount owed,
  can_check, current bet, min raise, and public info on all seats.
- Sandbox: **2 seconds per decision, 768 MB RAM, no network, no threads, read-only filesystem.**
- Reference stack: `eval7`, numpy, scipy, treys, scikit-learn; local demo UI with live leaderboard.

Scale and selectivity: **500+ entrants, top 64 to the international final.** Participants came from
Oxford, Cambridge, Imperial, UCL, KCL and internationally. Winning approaches were serious —
the 12th-of-500 entry used **Deep CFR with external-sampling MCCFR**, Numba-JIT training and
pure-NumPy inference to fit the sandbox.

Recruiting angle: sponsors across editions include **Quadrature, Jane Street, Susquehanna, Five
Rings, Teza, QRT, Jump Trading, Da Vinci**. The advertised non-cash prizes are **"office tours at top
quant firms" and "career introductions that actually matter."** eFinancialCareers covered it
explicitly as *"the new path to a job at an electronic trading firm."*

**Caveat:** "career introductions" and office tours are documented; a **guaranteed interview or
fast-track into the Quadrature internship is not.** I found no evidence of a formal pipeline link.
Treat it as a high-signal networking/CV event, not a back door.

Sources:
- https://fullhousehackathon.com/
- https://github.com/mbatv/fullhouse-engine (README read in full)
- https://github.com/advitrocks9/fullhouse-bot (README read in full)
- https://github.com/BouillieAnonymous/4fullhousehackathon
- https://www.efinancialcareers.com/news/quant-poker-the-new-path-to-a-job-at-an-electronic-trading-firm

---
---

# Part II — How to actually get into Quadrature

## 8. Who they hire

**The single most important structural fact**, from eFinancialCareers:

> Quadrature "doesn't seem to employ any quant researchers at all." Instead the firm has a
> **"unified team of quant developers"** who work on both research and development tasks.

Consequences for a candidate:
- **There is no researcher/developer split to hide behind.** Everyone is expected to "program to a
  high level" in order to "develop and test their ideas independently," and to develop systematic
  trading models using statistical and machine learning methods.
- **Programming ability is the gate, for every role**, including the Research track of the
  internship. Their elite programmers "have the opportunity to do research" — note the direction:
  programming skill earns research work, not the reverse.
- Stack: **Python, C++, Rust.** But "they care more about how you think than the languages you've
  used." They also look for **sharp design instincts** and **experience building or operating
  distributed systems.**

**Backgrounds of actual staff** (the only two named examples I found, both team leads):
- **Paul Smith** — team lead; formerly quant researcher at **Jump Trading** and **NatWest**.
- **Mateusz Kapka** — team lead; joined from **Balyasny** as a software engineer.

eFC's framing is that *few* of Quadrature's developers previously worked in quant research — i.e.
the modal hire is a **strong engineer**, not a PhD researcher.

**Founders/leadership:** Founded **2008** (some sources say 2010) by **Greg Skinner** (previously
D. E. Shaw, Salomon Brothers, DPFM) and **Suneil Setiya** (physics, Worcester College, Oxford), who
met at **G-Research**; the firm was started by five G-Research alumni. CEO is **Aidan Devane**
(ex-Boston Consulting Group). Offices on floors 31–34 of the Leadenhall Building, London. Reported
average revenue per head is extraordinary — figures of **$2.5m** and **$4.75m per head** appear in
eFC coverage.

**On PhD vs undergrad ratio, and university distribution: I have no data.** LinkedIn was blocked and
I could not read team pages. One prep site asserts a profile of "First-Class honours in CS/Maths/
Physics/Engineering from a top-tier university, often with master's or PhD" plus competitive
programming (ICPC/Codeforces) and FAANG-or-elite-trading internships — **but see the reliability
warning in §9; I do not consider this sourced.**

## 9. How people got noticed — and a warning about one source

**What is actually documented:**
- **Direct application via Greenhouse** is the main documented route. Quadrature's own "Join us" page
  notes they're always looking for talented people *even when no specific role is posted* — i.e.
  speculative applications are explicitly invited.
- **The Fullhouse Hackathon** (§7) is a real, Quadrature-led touchpoint with 500+ students and
  advertised "career introductions."
- **On-campus recruiting, referrals, and agency recruiters: no evidence found either way.** I could
  not confirm a campus milk-round presence.

**The "thousands of CVs in under 30 seconds" claim — do not trust it.** It comes from
`intervyo.co.uk/firms/quadrature-capital`, a "2027 Application Guide." That same page's CV advice
tells you to use **"the vocabulary of the graduate scheme world (DCF, comps, LBO, league tables,
deal flow)"** and to name **"the deals you observed"** and **"clients you worked on."** That is
investment-banking boilerplate and is *actively wrong* for a systematic trading firm that hires quant
developers and has no client business. The page reads as templated SEO content with the firm name
swapped in. **Treat every specific claim on it — including the 30-second CV figure and the candidate
profile in §8 — as unsourced.**

What Quadrature themselves say about volume, which is the defensible version: they receive **"a high
number of applications every week,"** aim to respond within 48 hours, and warn they cannot always
respond individually.

## 10. What they say they value

From Quadrature's own careers pages:

- **"Founded by programmers"** in 2010; a systematic trading firm of "smart, collaborative people
  passionate about using technology to solve complex problems."
- Committed to a culture promoting **"learning, creativity, kindness, and mutual trust and respect."**
- On cultural fit, verbatim: they assess **"how people think, behave and communicate"** to understand
  what it would be like to work with you — and explicitly say this **does not mean hiring only people
  similar to existing staff.** Diversity is named as a deliberate goal, with an aim to "remove
  barriers."
- They "prioritise growing thoughtfully to shape and protect the culture."

**The charitable angle.** Quadrature is unusual: co-founders Skinner and Setiya launched the
**Quadrature Climate Foundation (QCF)** in 2019 and committed **~$1 billion** to climate and
sustainable development. Quadrature maintains a Corporate Social Responsibility page.
**Does it feature in hiring? No direct evidence.** It is not mentioned in any interview account I
found. My read: it is a genuine and distinctive part of the firm's identity and a legitimate,
non-generic answer to "why Quadrature" — but there is no sign it is tested or scored.

## 11. Practical advice grounded in the evidence

Only advice I can tie to a source:

- **Prepare to justify data structures on hardware terms.** The one distinctive technical theme
  across their known questions is cache behaviour, memory layout, and performance/memory estimation.
  Being able to say *why* a sorted array beats a hash map at n=32 is more Quadrature-shaped than
  grinding LeetCode Hard.
- **Practise being interrupted.** Rehearse the two-on-one shifting-requirements format specifically
  (§5). This is the format candidates found most disorienting.
- **Be ready to talk at length about your own projects.** Multiple accounts stress heavy emphasis on
  background, previous projects, interests, and what you want to work on. This is not filler for them.
- **Take Quadrature at their word on prep for the final round:** *"there's nothing you need to
  prepare unless specifically asked to"* and *"bring some questions."* The CEO round appears to be
  genuinely a two-way conversation.
- **Don't lead with finance.** They "proactively look for people that might not have considered a
  career in quantitative finance"; no markets background is required. Programming is the gate.

## 12. Comparison signal, and downsides

**Bar vs. Jane Street / Optiver / HRT / Citadel Securities: no direct comparative data exists.** What
can be said:

- Quadrature is **far less known** to students than those firms, and its Glassdoor footprint (19
  reviews, ~24 interview entries) is a tiny fraction of theirs. Lower applicant awareness plausibly
  means less competition per seat, but I have no offer-rate data for anyone.
- Quadrature's own interview difficulty rating (**3.2/5**) is moderate, and **intern interviews are
  rated its easiest role type** — notably softer than the reputation of Jane Street or HRT loops.
- Compensation is in the same elite tier: SWE base ranges cited around **$230K–$313K+**, revenue per
  head of $2.5m–$4.75m. levels.fyi intern rate of ~$117/hr is competitive with the top US firms.
- Wall Street Oasis commentary: interviewers **"extremely personable and smart"**, the firm
  **"takes work-life balance seriously"**, strategy is largely **statistical arbitrage** with a
  **"tech firm vibe"**, primarily hiring quant developers.
- **Headcount and hires-per-year: unknown.** No source I reached gives an intern cohort size.

**Reported downsides / red flags:**
1. **Opacity.** This research task exists because candidates cite an NDA. The public record is
   genuinely sparse and skewed.
2. **Slow process** — 49 days company-wide average, though one candidate reported 2 weeks. High
   variance.
3. **Mentor lottery for return offers** — the most actionable negative: *"return offer chances are
   dependent on which mentor you get."*
4. **Weak end-of-internship feedback** — explicitly called out by an intern.
5. **The shifting-requirements interview is polarising** — at least one candidate came away feeling
   there was "no clarity about what they were looking for."
6. **Only 50% positive** interview experience rating company-wide, against a 4.7/5 employee rating —
   a gap suggesting the process itself is rougher than the workplace.

---

## 13. What I could NOT find (stated honestly)

- Any named online-assessment platform (HackerRank/CodeSignal/Codility) for Quadrature.
- Whether interns receive the take-home, or meet the CEO.
- Any intern-to-full-time conversion rate, or intern cohort size.
- Any TheStudentRoom, Reddit, or LeetCode Discuss thread on Quadrature internships — searches
  returned nothing Quadrature-specific from these communities.
- Any 1point3acres Quadrature interview write-up content (the company page exists at
  https://www.1point3acres.com/interview/company/quadrature but was unreadable).
- Confirmation of the "~21 days quant-dev intern" figure — and I have positive reason to think it is
  a misattributed Apple statistic (§2).
- Corroboration of the "8-hour take-home" — best evidence says **1–2 hours** (§4).
- Employee-background distribution (PhD ratio, universities, prior firms) beyond two named team leads.
- Any evidence of on-campus recruiting or a formal hackathon→interview fast track.
- NY-vs-London differences in the intern process.

## 14. Source list

**Quadrature's own (blocked; content via search summaries):**
- https://www.quadrature.ai/careers/internships/
- https://www.quadrature.ai/careers/how-we-hire/ · https://quadrature.ai/careers/recruitment
- https://www.quadrature.ai/careers/join-us/ · https://quadrature.ai/careers/working-here
- https://www.quadrature.ai/corporate-social-responsibility/
- https://job-boards.greenhouse.io/quadraturecapital

**Glassdoor (blocked; via summaries):**
- https://www.glassdoor.com/Interview/Quadrature-Interview-Questions-E1013879.htm
- https://www.glassdoor.com/Interview/Quadrature-Software-Engineer-Internship-Interview-Questions-EI_IE1013879.0,10_KO11,39.htm
- https://www.glassdoor.com/Interview/Quadrature-Capital-Quant-Developer-Interview-Questions-EI_IE1013879.0,18_KO19,34.htm
- https://www.glassdoor.co.uk/Interview/Quadrature-Capital-Interview-Questions-E1013879_P2.htm
- https://www.glassdoor.com/Reviews/Quadrature-Reviews-E1013879.htm
- https://www.glassdoor.com/Reviews/Employee-Review-Quadrature-RVW18024952.htm (Quant Dev Intern)
- https://www.glassdoor.co.uk/Reviews/Employee-Review-Quadrature-E1013879-RVW84593089.htm (Internship)

**Blind (blocked; via summaries):**
- https://www.teamblind.com/post/Quadrature-Capital-Quant-Dev-onsite-interview-sPu8HeXx
- https://www.teamblind.com/post/Quadrature-Onsites-nZxGyWEK
- https://www.teamblind.com/post/quadrature-onsite-iqf4hbxf
- https://www.teamblind.com/post/quadrature-capital-interview-uym1nwuq
- https://www.teamblind.com/post/Quadrature-Capital-pay-London-xjnsF2EH

**Other:**
- https://www.levels.fyi/internships/Quadrature-Capital/Software-Engineer-Intern/
- https://www.levels.fyi/companies/quadrature/salaries
- https://www.efinancialcareers.co.uk/news/high-paying-quant-development-jobs-quadrature
- https://www.efinancialcareers.com/news/quadrature-new-york-office-hiring-jpmorgan
- https://www.efinancialcareers.com/news/quant-poker-the-new-path-to-a-job-at-an-electronic-trading-firm
- https://www.wallstreetoasis.com/forum/hedge-fund/thoughts-on-quadrature
- https://en.wikipedia.org/wiki/Quadrature_Capital · https://en.wikipedia.org/wiki/Suneil_Setiya
- https://www.qc.foundation/about-us/
- https://fullhousehackathon.com/ · https://github.com/mbatv/fullhouse-engine
- https://www.intervyo.co.uk/firms/quadrature-capital — **low reliability, see §9**
