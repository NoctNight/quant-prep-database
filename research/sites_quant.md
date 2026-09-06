# Websites & Platforms for Quant Interview Prep — Honest Evaluation

Research date: 2026-09-06

---

## 0. Methodology and its limits (read this first)

**What I could and could not access.** This sandbox routes outbound HTTPS through a strict
allowlist proxy. GitHub and `raw.githubusercontent.com` were reachable. **Almost nothing else
was** — every one of the following returned `EGRESS_BLOCKED`:

`quantguide.io`, `brainstellar.com`, `janestreet.com`, `quantt.co.uk`, `tradermath.org`,
`marketmakinggames.com`, `news.ycombinator.com`, `medium.com`, `careerdevelopment.princeton.edu`,
`reddit.com` / `old.reddit.com` (403 at CONNECT).

So: **I could not personally load a single one of the prep sites under review.** What follows is
built from (a) web-search result summaries, which do reach the live web, (b) primary documents on
GitHub that I fetched in full, and (c) triangulation between the two. Where a claim rests only on
a search summary I say so. Treat prices as "last verified by search index", not as quoted by me
off the vendor's page.

**The one genuinely first-hand document I read end-to-end** is
[github.com/Aniruddha-Deb/quant-prep](https://github.com/Aniruddha-Deb/quant-prep) — a public prep
log by someone who went through the cycle and ended up an Optiver SWE intern, with per-site
commentary and a plot of his own Zetamac scores. It is the most trustworthy source in this
document precisely because he is selling nothing. His own caveat, added May 2025: *"This is 3
years old at this point and sporadically updated - there may be better guides out there."* Some
of his pricing observations are stale (he lists quantguide.io as free; it now has a paid tier).

**Reddit r/quant, Glassdoor and QuantNet were unreachable**, exactly as the task anticipated.
Practitioner opinion below is therefore reconstructed from search-engine summaries of those
threads plus TeamBlind and Levels.fyi, which surfaced more readily. That is a real weakness and I
have flagged individual claims accordingly.

---

## 1. The single most important thing on this page: a name collision

**`quantguide.io` and `thequantguide.com` are different products. Do not confuse them.**

| | quantguide.io | thequantguide.com |
|---|---|---|
| What | LeetCode-style problem bank | Video "bootcamp" / course |
| Price | Free tier + ~$20–35/mo | **$3,500** |
| Reputation | Broadly positive | Repeated **scam** allegations |

Search summaries of TeamBlind threads on *thequantguide.com* report: questions apparently
**scraped from Glassdoor**, not spell-checked, **no solutions**, roughly **20% duplicates**;
videos comparable to free YouTube; and — most damning — that users **could not find the founders
on LinkedIn**, and that the founders gave **inconsistent accounts of their own employer, telling
one person Jane Street and another Citadel**. Marketing reportedly promises interviews at top
firms and a $450k salary. There are also positive testimonials claiming two internship offers.

The recurring line from actual quants in those threads is the useful one:
*"people who can get quant research jobs wouldn't resort to bootcamps like this — the green book
is more than enough."*

- Blind: [Thoughts on The Quant Guide?](https://www.teamblind.com/post/thoughts-on-the-quant-guide-1dhuuyj5)
- Blind: [Anybody try the quant guide?](https://www.teamblind.com/post/Anybody-try-the-quant-guide-tV46EByh)
- Blind: [$3.5k?](https://www.teamblind.com/post/the-quant-guide-worth-35k-larccmfr)
- Trustpilot: [thequantguide.com](https://www.trustpilot.com/review/thequantguide.com)

**Verdict on thequantguide.com: avoid.** Unverifiable instructors plus scraped questions plus a
$3,500 price is the classic shape of a prep scam.

---

## 2. QuantGuide — quantguide.io

**What it is.** The "LeetCode for quant": a large problem bank with difficulty tiers, company
tags, a daily question, an in-browser mental-math trainer ("Quantify", `quantguide.io/quantify`),
progress analytics and a discussion community.

**Free vs paid.** Search-indexed figures: a **free tier of roughly 400 problems with full
solutions**, plus analytics and the mental-math simulator. Premium unlocks firm-tagged "asked at
X" questions, step-by-step solutions and hints. **~$35/mo monthly, ~$20/mo billed annually**
(their [pricing page](https://www.quantguide.io/pricing) was not loadable from here — verify).

**Corporate footprint.** [Crunchbase lists "Quant Guide LLC"](https://www.crunchbase.com/organization/quant-guide-llc),
Providence RI, 1–10 employees, support@quantguide.io. Small, but a real registered entity —
unlike several sites in section 10.

**What practitioners actually say.** Aniruddha Deb, in his prep log: *"looks like a newer and
better brainstellar. Leetcode for quant. Problems organized by company."* His one concrete gripe
is a UX bug worth knowing: **the answer checker is finicky about numeric precision — give lots of
decimals or enter a fraction**, and some questions reject decimals entirely.

An independent credibility signal: **Sarah Chieng** — three trading internships (SIG, HRT, Peak6),
now widely followed for her free quant resources — collaborated with QuantGuide on a free curated
**500+ trading interview problem** list. That a real ex-SIG/HRT intern put her name on it is
worth more than any testimonial page.
([her Notion](https://milksandmatcha.notion.site/Free-Trading-Resources-v2-4456ae906000487181f3486dbd0dd631),
[X thread](https://x.com/SarahChieng/status/1723928783898722581))

**Honest verdict.** ⭐ **The strongest single paid platform in this space, and the free tier alone
beats most paid competitors.** The genuine edge is company tagging plus the mental-math trainer in
one place. Caveats: (1) company tags on any of these sites are crowd-sourced and drift out of date
— treat "asked at Jane Street" as folklore, not fact; (2) the specialisation is probability +
puzzles + arithmetic, so if you are targeting QR roles that test stats depth, ML and real coding,
this is one leg of the stool, not the stool. Buy a month, not a year.

---

## 3. Brainstellar — brainstellar.com

**What it is.** A free, static collection of quant-interview puzzles by a practitioner, organised
into Easy / Medium / Hard plus themed albums: Probability, Discrete Maths, Strategic Puzzles,
General Tricks. An [open-source mirror exists on GitHub](https://github.com/rudradesai200/BrainStellar).
Colour-coded so beginners can find the canonical logic puzzles first.

**Free vs paid.** **Entirely free**, no login, no upsell. Rare and admirable in this category.

**Quality.** Genuinely good taste in problem selection — several are true interview classics that
recur verbatim. One search summary reports Brainstellar problems being *"directly asked in
interviews"*. The honest limitations, from the practitioner log: *"good puzzles, but the hard ones
are not so hard, and they finish up rather quickly."* Answers are **terse — often closer to hints
than worked solutions**, which is fine if you can already close the gap and frustrating if you
can't. Coverage is puzzles only: no statistics, no OA formats, no coding, no market-making.

**Honest verdict.** ⭐ **Best free on-ramp in the category.** Do it first, finish it in one to two
weeks, then graduate. Anyone telling you Brainstellar is a *complete* prep plan is selling
something; anyone telling you to skip it because it's free is also selling something.

---

## 4. OpenQuant — openquant.co

**What it is.** Primarily a **quant job board** (QR / QT / quant dev / DS / MLE roles) with a
weekly [newsletter](https://openquant.substack.com) covering jobs, events and educational
opportunities. Prep content is a secondary offering — and better than that framing suggests.

**The prep tools, all free:**
- [openquant.co/questions](https://openquant.co/questions) — probability, statistics, brainteasers
- [openquant.co/questions/assessment](https://openquant.co/questions/assessment) — a timed mock OA (7 questions / 30 min)
- [openquant.co/math-game](https://openquant.co/math-game) — **the underrated part.** Modes include
  Arithmetic Game, Arithmetic Pro, Sequence Game, **Optiver 80-in-8**, Memory Game, Risk Game,
  Flexibility Game, Letter Speed.
- Blog: [Mental Math for Quantitative Traders](https://openquant.co/blog/math-for-traders),
  [Quant Trading Competitions](https://openquant.co/blog/trading-competitions)

**Why the game room matters.** Memory / Risk / Flexibility / Letter Speed are not arithmetic —
they are close analogues of the **gamified cognitive battery Optiver actually uses** (see §6.4).
This is the nearest thing to free Zap-N-style practice I found that isn't someone selling you a
JobTestPrep subscription.

**Legitimacy.** [ScamAdviser rates it legitimate](https://www.scamadviser.com/check-website/openquant.co);
it is indexed as an established board by [startup.jobs](https://startup.jobs/job-boards/openquant).
I found no substantive Reddit critique, partly because Reddit was blocked.

**Honest verdict.** ⭐ **Use it — it costs nothing.** Best-in-class as a job board and deadline
tracker; the free game room is a legitimate reason to visit even if you never apply through it.
Its written question bank is thin next to QuantGuide's. The business model is employer-side, so
the incentive to inflate prep content is low — a point in its favour.

---

## 5. The mental-maths tier

Ranked by how close each is to what firms actually administer.

### 5.1 Zetamac — arithmetic.zetamac.com ⭐ **the canonical tool**
Free, no login, no account, no ads, unchanged for years. Default is a 2-minute timer over
+ − × ÷ on integers; every parameter is configurable via the URL.

**Score bands** (community consensus, **not official** — no firm publishes a cutoff):
~**45–55** workable baseline · ~**55–70** competitive for most prop shops · **70+** comfortable
even at Optiver-tier firms. Another summary offers the blunter version: *"40 is good, ideally
above 60."*

The most useful calibration point I have is first-hand and outcome-linked: Aniruddha Deb recorded
a **baseline of 50 and a peak of 60** on default settings, published his score-progression plot,
and **got the Optiver offer**. That is a far better anchor than any prep site's aspirational chart.

**Verdict:** the default choice. Its weakness is that it drills *only* integer arithmetic — no
fractions, decimals, or missing-operand items, all of which appear in real OAs.

### 5.2 RFQJobs — rfqjobs.com/practice/math ⭐ **the sleeper pick**
Free. Singled out in the prep log above: *"Really liked the Optiver test here and the
Focus-Fractions and Focus-Decimals."* Fills exactly Zetamac's gap. Almost nobody mentions it,
which is itself informative — it isn't marketing itself.

### 5.3 TradingInterview — tradinginterview.com
Paid course platform, and the one place repeatedly described as **format-faithful to Optiver**:
sequential flow, **+1/−1 marking**, matching item types. Note the prep log's correction: the hard
test moved, and there is now a purpose-built
[Optiver math test](https://www.tradinginterview.com/courses/mental-arithmetic/quizzes/optiver-math-test/)
which is *more* representative (the old "hard" preset was harder than the real thing, and the real
one was MCQ).

[Trustpilot](https://www.trustpilot.com/review/tradinginterview.com) is genuinely mixed:
*"very close to Optiver test questions"* against *"quite expensive"* and — the sharpest criticism —
that the pool repeats until *"you're not thinking about the answer, you're just remembering the
question."* **Verdict: the +1/−1 sequential format is worth something real if Optiver is your
target; the price and the shallow question pool are not.**

### 5.4 TraderMath / tradermath.org
Free games (mental maths, market making) plus a question database.
**Read this warning:** *"decent, but the UI is off what I should expect — the ability to skim
through questions makes it very easy to cherry-pick easy ones to maximize score."* **Your
tradermath score is inflated relative to a real timed test.** Use for volume, never for
calibration.

### 5.5 RankYourBrain — rankyourbrain.com/mental-math
Free; leaderboards, configurable difficulty, and — usefully — **fractions and decimals**. The
consistent complaint is the UI (*"I don't like the UI"*). Fine as a secondary drill.

### 5.6 Matiks — matiks.in
Free, gamified head-to-head mental maths — "QuizUp meets mental math". Honest first-hand note:
*"my gut feel is most guests are bots/replays"*, and it skews away from division and large
multiplication, so it is **weakly trading-relevant**. Included because the competitive dopamine
does keep people drilling.

---

## 6. Firm-published material — the highest-signal, lowest-cost tier

This is the part of the market that is free, authoritative, and systematically under-used because
nobody runs ads for it.

### 6.1 Jane Street Puzzles — janestreet.com/puzzles ⭐⭐
Monthly puzzle with a full public [archive](https://www.janestreet.com/puzzles/archive/index.html)
and published solutions. Free.

The honest calibration: **these are harder than interviews.** *"If anything, these are a level
above what I think will be asked on the interview. Absolutely a pleasure to sink your teeth into:
need both deep insight and flexible thinking."* Grinding them is not efficient interview prep. It
is excellent for building the flexible-thinking muscle, and it is fun, which matters over a long
prep cycle. The most interview-adjacent ones named by a real candidate: *Robot Tug-of-war*,
*Bracketology 101*, *Circle Time*, *Alter/Nate*, *Candy Collectors*, *Single Cross*.

### 6.2 Jane Street's Probability & Markets Guide ⭐⭐ **the best free PDF in quant prep**
[janestreet.com/probability-markets](https://www.janestreet.com/probability-markets/) —
probability, expected value, and **how to make a market**, written by the firm that will
interview you, explaining *why* it cares. Recommended in the prep log specifically *"for market
making"*. Discussed on [Hacker News](https://news.ycombinator.com/item?id=41800699). Mirrors
circulate ([WSO copy](https://www.wallstreetoasis.com/files/jane_street_interview_guide.pdf)) but
take it from the source. **If you read one thing before a trading interview, read this.**

### 6.3 Jane Street Estimathon® ⭐
**13 Fermi problems in 30 minutes, in teams**, run as campus/public events (they appear on
[Jane Street's Greenhouse](https://job-boards.greenhouse1.io/janestreetevents)). The format's real
lesson is that the answer is not the point: interviewers grade decomposition, assumption quality
and sanity-checking. A candidate who is off by 50% with clean reasoning beats a confident number.
**The only structured Fermi practice with a real firm behind it** — attend if one comes to you.

### 6.4 Optiver's own tools — and a correction worth internalising
- **Ready Trader Go** ([readytradergo.optiver.com](https://readytradergo.optiver.com/)) — student
  algo-trading competition on Optiver's simulated exchange. Three weeks, two qualifying rounds
  plus a finale, teams up to three, **€30,000 first prize**, explicitly **no prior market-making
  knowledge required**. Reported honestly by eFinancialCareers: *"success won't guarantee you a
  job, but it will not be a bad thing for your CV."* Public editions ran 2021–2023 — **verify it
  is running before you plan around it.** Community solutions exist on GitHub, e.g.
  [russellstanley/optiver-trading](https://github.com/russellstanley/optiver-trading).
- **"80 in 8"** — 80 mental-arithmetic items in 8 minutes, **+1/−1 marking**, mixing integers,
  decimals, fractions and missing-operand questions. Practised via §5.
- **Zap-N — the correction.** Zap-N is **not a mental-maths paper.** It is a battery of short
  gamified cognitive tests — working memory, attention, risk-taking, planning. Optiver publishes
  **no official practice tool** for it. Sites selling "Zap-N prep" (JobTestPrep and similar) are
  selling reverse-engineered guesses; the free games at
  [openquant.co/math-game](https://openquant.co/math-game) get you equally far for £0. **Do not
  pay for Zap-N practice.**

### 6.5 Other firm competitions
| Competition | Cost | Shape | Recruiting value |
|---|---|---|---|
| **IMC Prosperity** ([prosperity.imc.com](https://prosperity.imc.com/)) | Free | Annual since 2023, global, online, teams ≤5, manual + algorithmic rounds, **$50k pool** | ⭐ Best entry point. Most accessible serious competition; a real crash course in microstructure. One documented solo participant hit 73rd worldwide with no prior quant-trading experience. |
| **Akuna Quant Trading Challenge** ([akunacapital.com](https://akunacapital.com/)) | Free | ~5–8 hours over a 1-week window; write **market-making bots** against Akuna's models and other entrants on a simulated exchange; Python; STEM students | Prizes are swag plus **expedited recruiting** for Chicago quant roles. Excellent effort-to-signal ratio. |
| **Citadel / Correlation One Datathons & Terminal** ([correlation-one.com](https://www.correlation-one.com/)) | Free, **invite-only** | Datathon: team data analysis + judged report. Terminal: algorithmic tower-defence. | **$15,000** prizes and explicit, direct recruiting into Citadel internships and full-time roles. The most direct competition-to-offer pipeline listed here. |

---

## 7. Market-making game practice

The thinnest-covered skill relative to how central it is: *"make me a market"* is the single most
common trading-interview exercise, and almost nobody drills it.

- **[marketmakinggames.com](https://marketmakinggames.com/)** — ⭐ the most interesting find.
  **Real-time multiplayer** market-making against other humans, tournaments, global leaderboards,
  private rooms with friends. Eight games spanning bid-ask pricing, probability calibration,
  arbitrage spotting, **Kelly-criterion sizing** and fast mental maths. Run by the
  TradingInterview team. *I could not load it (blocked) and could not verify free vs paid — check
  before committing.* The multiplayer element is genuinely hard to replicate solo and is the one
  thing here that a book cannot substitute for.
- **[tradinginterview.com "Make Me a Market"](https://www.tradinginterview.com/courses/market-making/quizzes/market-making-game/)**
  — drills the exercise across **550+ facts and guesstimates**: you quote two-sided without ever
  knowing the true answer. Paid.
- **[mikinty/Trading-Interview-Questions](https://github.com/mikinty/Trading-Interview-Questions)**
  — ⭐ **free and open-source.** I read this one directly. Chapters on Math, Brain Teasers,
  Probability, **Games and Betting**, **Market Theory**, plus the interview process and a firm
  list; and a companion free game site at
  [mikinty.github.io/Trading-Interview-Questions](https://mikinty.github.io/Trading-Interview-Questions/)
  for market making, gambling and market simulation. The author's motive is stated plainly and
  he takes coffee money, not subscriptions. **Best free market-making practice available.**
- **Best substitute for all of the above:** read §6.2, then play with two friends. Market-making
  intuition is built by being adversely selected by a human who knows something you don't.

---

## 8. Book-adjacent resources

**The Green Book — Xinfeng Zhou, *A Practical Guide to Quantitative Finance Interviews.***
Universally the most-recommended text: 200+ real problems across brainteasers, calculus, linear
algebra, probability, stochastic calculus, finance and programming.
*"Amazing book. Especially the brainteasers and Probability section. Must do."*
**There is no official companion site.** What exists is (a) unauthorised PDFs on GitHub and
elsewhere — buy the book, and (b) a swarm of SEO pages advertising "free worked solutions" and
"chapter-by-chapter guides", which are section-10 material. The book is ~$40 and, per the Blind
consensus quoted in §1, is *the* thing that makes $3,500 courses unnecessary.

**150 Most Frequently Asked Questions on Quant Interviews — Stefanica, Radoicic, Wang (FE Press).**
Real institutional lineage: built on 20+ years of Baruch College MFE placement.
[Third edition](https://www.fepress.org/150iqs-third-edition/) runs to 200+ questions and adds
**statistics and machine learning** for the first time — a meaningful update given where QR
interviews have gone. Spans C++, data structures, finance, brainteasers, stochastic calculus.
Answers are deliberately interview-length rather than exhaustive.
**Verdict: better for MFE / quant-analyst / QR-adjacent tracks than for pure trading brainteasers.**
Complements the Green Book rather than replacing it. Discussion threads on
[QuantNet](https://quantnet.com/threads/150-most-frequently-asked-questions-on-quant-interviews-third-edition.59976/).

**Mark Joshi's "Red Book"** — *"too broad to be very useful."*
**"Heard on the Street" (Crack)** — popular; one candidate declined to read it, comparing it to
Cracking the Coding Interview (*"I detest that book"*). Broad and dated in places.
**"50 Problems in Probability"** — actively disliked in the one first-hand review I have:
*"the questions felt very loosely worded... their key element was their ambiguity."*

---

## 9. Communities, and the data/stats angle

### 9.1 Communities
- **QuantNet** ([quantnet.com](https://quantnet.com)) — still active into 2026. Strongest on
  **MFE admissions, rankings and program ROI**; the interview value is in its long-running
  archive threads, e.g.
  [Big list of quant interview questions with answers](https://quantnet.com/threads/big-list-of-quant-interview-questions-with-answers.36240/)
  and the [Jane Street compilations](https://quantnet.com/threads/compilation-of-jane-street-interview-questions.17941/).
  **Verdict: a searchable archive first, a live community second.** *(Blocked from here; assessed
  via search summaries.)*
- **Wall Street Oasis** ([wallstreetoasis.com](https://www.wallstreetoasis.com/)) — **be honest
  about the decline.** WSO's *own* users document it: *"a real decline in quality, which has
  driven lots of long-term users either to post less or off the platform entirely"*; barriers to
  entry were removed and the audience diluted; and questions that once needed a forum are now
  answered by an AI query. See [What happened to WSO](https://www.wallstreetoasis.com/forum/off-topic/what-happened-to-wso).
  Broad-finance-first, quant second. **Verdict: mine the archive, don't expect the community.**
- **r/quant** — the most-cited source of candid practitioner opinion and the one I **could not
  reach at all** (403 at the proxy). Everything attributed to Reddit here is second-hand via
  search summaries. Its published score bands and resource threads are the de facto community
  standard; treat my §5 numbers as reported, not verified.
- **TeamBlind / Levels.fyi** — reachable via search, and unusually candid because posters are
  verified employees. The best available signal on paid courses (see §1, §10).

### 9.2 Data / stats interview platforms
These matter for **QR, data science and quant-adjacent** roles, not for trading.

| Platform | Price | Genuinely good for | Honest caveat |
|---|---|---|---|
| **DataLemur** ([datalemur.com/pricing](https://datalemur.com/pricing)) | **$15/mo or $60/yr** | ⭐ Best value. Tight curation with **verified company sourcing**; Nick Singh's solution videos are a real differentiator for video-first learners. | Premium bank is only **~150 questions**. A motivated candidate exhausts it in weeks — after which a monthly plan is renting problems you've already solved. **Buy the year only if you'll start soon.** |
| **StrataScratch** | ~**$39/mo or $159/yr** | Largest raw bank — 1,000+ real SQL/Python interview questions. | Most expensive monthly here, and the coverage is *only* SQL + Python: no system design, no data modelling, no pipeline architecture. |
| **Interview Query** | ~**$230/yr** | Broadest scope: stats, probability, ML, product sense, take-homes. | The **6,000+ "company guides" cannot all be current** — nobody keeps thousands of hiring loops verified while they change quarterly. Read any company guide as a snapshot of the past. |

**All three are legitimate businesses with real customers.** None is a quant-trading resource. If
you are prepping for Optiver, this row of the table is a distraction; if you are prepping for a
QR or DS loop with a SQL screen, DataLemur first.

---

## 10. 🚩 Red flags — the part of this market you should be most sceptical of

The largest single finding of this research is **not about any one site**: the quant-prep niche is
now **saturated with near-identical, apparently AI-generated SEO content farms**, and they crowd
out genuine practitioner discussion in search results. Across ~30 searches the same cluster kept
surfacing:

`quantvault.org` · `myntbit.com` · `leetquidity.com` · `spacecomplexity.ai` ·
`trademindapp.com` · `everythingquant.com` · `quantprep.io` · `quantbrainteasers.com` ·
`quantmatter.com` · `sqlquest.app` · `prachub.com` · `datainterview.com` ·
`quantquestions.app` / `quantquestions.io` / `quantquestions.com` / `quantquestion.com`

**How to recognise the pattern:**

1. **The rigged comparison.** Every one publishes "*X vs Y (2026): Honest Comparison*" pages —
   including comparisons **between two competitors neither of which is them** — and the verdict
   is always, eventually, their own product. `quantvault.org` alone hosts *QuantGuide vs
   QuantQuestions*, *QuantVault vs QuantGuide*, *QuantVault vs Brainstellar*, *QuantVault vs
   QuantQuestions*. To its slight credit it discloses authorship on some pages; the format is
   still an advertisement wearing a review's clothes.
2. **URL/title mismatch — the clearest tell.** `quantvault.org/quant-oa-census-2027.html` serves a
   page titled *"Green Book: Chapter-by-Chapter Solutions Guide"*. That is a **template being
   refilled with generated content**, not a document someone wrote.
3. **Year-stuffed titles at scale.** Every page on `quantt.co.uk` and much of `quantblueprint.com`
   is "…2026" or "…2027". Sites written by people don't re-title their whole catalogue annually;
   sites written by pipelines do.
4. **Domain-squatting on a competitor's name.** Four separate near-identical "QuantQuestions"
   domains (`.io`, `.com`, `.app`, plus singular `.com`) is not four companies solving a problem.
5. **AI generation stated openly.** `quantquestion.com` advertises *"AI intelligent assistance"*
   and question banks that *"dynamically generate"* problems; `quantquestions.app` advertises
   *"AI mock interviews"*. **A dynamically generated quant question is not an interview question**
   — it has no provenance, and the whole value proposition of a question bank is provenance.
6. **Unfalsifiable social proof.** Testimonial walls listing Jane Street / Citadel / Two Sigma
   logos with no verifiable identities.

### Specific verdicts on paid offerings

- **thequantguide.com — $3,500.** ⛔ **Avoid.** See §1: scraped questions, no solutions, ~20%
  duplicates, founders unfindable and inconsistent about their own employer.
- **Quant Blueprint ([quantblueprint.com](https://www.quantblueprint.com/)) — ~$4,800, no refunds.**
  ⚠️ **Legitimate but hard to justify.** It is a real business with a real product: lifetime access
  to 80+ videos (15+ hours) on probability, brainteasers, EV, betting, strategy games,
  market-making and estimation; 500+ questions; resume guides; mock interviews with feedback;
  ~3 months to complete; Affirm/Shopify Pay instalments. There is **corroboration outside its own
  site** — a [Levels.fyi thread](https://www.levels.fyi/community/thread/XIiCrE/anyone-use-quant-blueprint-s-program)
  and a [QuantNet thread](https://quantnet.com/threads/quant-blueprint-program.61406/) with
  someone reporting **two offers including DRW** — which puts it in a different category from
  §1. But: **~$4,800 with no refunds**, an "Investing.com Studios *contributor content*" review
  (that label means paid placement), and a blog that is unmistakably SEO-shaped. Against the
  Green Book at $40 plus free Jane Street material, the marginal value is resume help and
  accountability, not knowledge. **Only if money is genuinely not a constraint.**
- **Quantt ([quantt.co.uk](https://www.quantt.co.uk/)) — price unverified.** ⚠️ **Unproven.**
  Claims 60+ interactive courses across technology, mathematics and finance for aspiring quant
  devs, plus timed coding tests, mock exams, firm-by-firm prep and question banks. I could not
  load the site, found **no independent practitioner discussion whatsoever**, and no author
  bylines or credentials on any resource page. Its entire visible footprint is year-stamped SEO
  articles. **Not evidence of fraud — but nothing supports paying it either.** Read the free
  articles, buy nothing until someone you can identify vouches for it.
- **"Zap-N practice" from JobTestPrep and similar.** ⛔ **Don't pay.** See §6.4 — no official
  practice exists; free equivalents are as good.
- **`offertutoring.com` selling "2027 Optiver Online Assessment Exact Questions & Answers".**
  ⛔ Selling stolen live assessment content. Buying it is an integrity violation that gets offers
  rescinded. Avoid entirely.

---

## 11. Bottom line

**A genuinely good prep stack costs about £40.**

| Stage | Resource | Cost |
|---|---|---|
| Read first | **Jane Street Probability & Markets guide** | Free |
| Core text | **Green Book (Zhou)** | ~$40 |
| Free warm-up | **Brainstellar** — finish it, then move on | Free |
| Daily drill | **Zetamac** (target 55+) + **RFQJobs** for fractions/decimals | Free |
| Volume + company tags | **QuantGuide** free tier; upgrade **monthly** if you exhaust it | Free / ~$20–35/mo |
| Market making | **mikinty's repo + games**; §6.2; two friends and a whiteboard | Free |
| Cognitive/OA games | **OpenQuant math-game room** | Free |
| Stretch + enjoyment | **Jane Street puzzles archive** | Free |
| Signal to employers | **IMC Prosperity**, **Akuna Challenge**, **Citadel/Correlation One** | Free |
| Jobs + deadlines | **OpenQuant** job board | Free |
| MFE/QR track only | **Stefanica 150 (3rd ed.)**; **DataLemur** if there's a SQL screen | ~$40 / $15/mo |

Everything above £40 buys **accountability, resume review and mock-interview reps** — which are
real goods, and which you can also get from a study group for nothing. Nothing above £40 buys
knowledge that isn't in the Green Book and the Jane Street PDF.

**The one caveat I'd flag on the free stack:** it is strong on trading (probability, brainteasers,
mental maths, market making) and thin on modern **quant research** loops, which increasingly test
statistics, ML and real coding. For those, §9.2 plus ordinary CS/stats preparation matters more
than anything in §1–7.

---

## 12. Confidence and gaps

**High confidence:** the thequantguide.com / quantguide.io distinction; Zetamac's role and rough
bands; the value of Jane Street's free material; Brainstellar's strengths and limits; competition
formats and prizes; the existence and shape of the SEO-farm cluster; Zap-N being a cognitive
battery rather than arithmetic.

**Medium confidence:** all prices (search-indexed, not read off vendor pages); QuantGuide's exact
free-tier size; Quant Blueprint's $4,800 figure; whether Optiver Ready Trader Go is currently
running.

**Low confidence / gaps:** anything attributed to **Reddit r/quant, Glassdoor or QuantNet**, all
of which were unreachable — the single biggest weakness of this research, since they are exactly
the practitioner-opinion sources requested. I could not load **marketmakinggames.com**, so its
free/paid status is unverified. I found **no independent review of Quantt at all**. And I could
not read the Hacker News thread on the Jane Street guide, or the first-hand Medium review of
Quant Blueprint (both blocked).

**If you want these gaps closed,** the fastest path is opening r/quant, the QuantNet big-list
threads and the vendor pricing pages directly in a browser — they are all public, just not
reachable from this sandbox.

---

## Sources

**Primary documents I read in full (GitHub, unblocked):**
- [Aniruddha-Deb/quant-prep](https://github.com/Aniruddha-Deb/quant-prep) — first-hand prep log, ended at Optiver; [his retrospective blog post](https://aniruddhadeb.com/articles/2022/intern-inferno/)
- [mikinty/Trading-Interview-Questions](https://github.com/mikinty/Trading-Interview-Questions) — free open-source guide + [games](https://mikinty.github.io/Trading-Interview-Questions/)
- [rudradesai200/BrainStellar](https://github.com/rudradesai200/BrainStellar)

**Sites under review:** [quantguide.io](https://www.quantguide.io/) · [brainstellar.com](https://brainstellar.com/) · [openquant.co](https://openquant.co/) · [quantt.co.uk](https://www.quantt.co.uk/) · [quantblueprint.com](https://www.quantblueprint.com/) · [tradermath.org](https://www.tradermath.org/) · [tradinginterview.com](https://www.tradinginterview.com/) · [arithmetic.zetamac.com](https://arithmetic.zetamac.com) · [rankyourbrain.com/mental-math](https://rankyourbrain.com/mental-math/) · [rfqjobs.com](https://rfqjobs.com/practice/math/) · [marketmakinggames.com](https://marketmakinggames.com/) · [matiks.in](https://www.matiks.in/)

**Firm-published:** [Jane Street Puzzles](https://www.janestreet.com/puzzles/) · [Jane Street Probability & Markets](https://www.janestreet.com/probability-markets/) · [Jane Street Interviewing](https://www.janestreet.com/join-jane-street/interviewing/) · [Optiver Ready Trader Go](https://readytradergo.optiver.com/) · [Optiver RTG launch](https://optiver.com/its-ready-trader-go-time-optiver-launches-coding-competition-for-uk-and-eu-students/) · [IMC Prosperity](https://prosperity.imc.com/) · [Akuna Capital](https://akunacapital.com/) · [G-Research QR/ML reading list (PDF)](https://www.gresearch.com/wp-content/uploads/2025/07/Quantitative-research-and-machine-learning-interview-prep-recommended-reading.pdf)

**Community / practitioner:** [Blind: Thoughts on The Quant Guide](https://www.teamblind.com/post/thoughts-on-the-quant-guide-1dhuuyj5) · [Blind: Anybody try the quant guide](https://www.teamblind.com/post/Anybody-try-the-quant-guide-tV46EByh) · [Blind: worth $3.5k?](https://www.teamblind.com/post/the-quant-guide-worth-35k-larccmfr) · [Levels.fyi: Quant Blueprint](https://www.levels.fyi/community/thread/XIiCrE/anyone-use-quant-blueprint-s-program) · [QuantNet: Quant Blueprint](https://quantnet.com/threads/quant-blueprint-program.61406/) · [QuantNet: big list of quant interview questions](https://quantnet.com/threads/big-list-of-quant-interview-questions-with-answers.36240/) · [WSO: What happened to WSO](https://www.wallstreetoasis.com/forum/off-topic/what-happened-to-wso) · [WSO: mental math score for prop trading](https://www.wallstreetoasis.com/forum/trading/what-mental-math-score-is-needed-for-prop-trading-interviews) · [Sarah Chieng's free resources](https://milksandmatcha.notion.site/Free-Trading-Resources-v2-4456ae906000487181f3486dbd0dd631) · [Trustpilot: tradinginterview.com](https://www.trustpilot.com/review/tradinginterview.com) · [Trustpilot: thequantguide.com](https://www.trustpilot.com/review/thequantguide.com)

**Books:** [Green Book (Amazon)](https://www.amazon.com/Practical-Guide-Quantitative-Finance-Interviews/dp/1438236662) · [150 Questions, 3rd ed. (FE Press)](https://www.fepress.org/150iqs-third-edition/)

**Data/stats platforms:** [DataLemur pricing](https://datalemur.com/pricing) · [StrataScratch](https://www.stratascratch.com/) · [Interview Query](https://www.interviewquery.com/)

**Cited as examples of the SEO/AI-content pattern, not as evidence:** [quantvault.org](https://quantvault.org/) · [myntbit.com](https://myntbit.com/) · [leetquidity.com](https://www.leetquidity.com/) · [quantquestion.com](https://www.quantquestion.com/) · [quantquestions.app](https://quantquestions.app/) · [datainterview.com](https://www.datainterview.com/) · [quantmatter.com](https://quantmatter.com/best-quant-forum/)
