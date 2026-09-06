# Mock Interviews, C++/Low-Latency Learning, and Portfolio Projects — Quant Track

Research date: 2026-09-06. ~30 web searches + GitHub API queries.

## Methodology & sourcing caveat (read this first)

**Reddit and Hacker News were both hard-blocked in this sandbox.** Direct fetches to
`reddit.com`, `news.ycombinator.com`, `hn.algolia.com`, and the HN-comment mirror
`yahnd.com` all returned `EGRESS_BLOCKED`, and the search tool refuses `reddit.com` as an
allowed domain entirely. So there is **no first-hand r/quant / r/cpp / r/algotrading /
HN quoting in this report.** Several other useful domains were also blocked
(`quantnet.com`, `openquant.co`, `quantvault.org`, `hellointerview.com`,
`meetapro.com`, `readytradergo.optiver.com`, `quick-bench.com`).

What I *could* verify directly and treat as hard signal:

- **GitHub REST API** — real star counts, fork counts, and `pushed_at` (last-commit) dates.
  This is the most trustworthy data in this document and I lean on it heavily.
- Vendor pages and docs that were reachable (Databento, Massive, CppCon, isocpp, agner.org).
- Search-engine *summaries* of Reddit/Blind/QuantNet threads. These are second-hand and I
  mark them as such. Team Blind surfaced far more than Reddit did.

Where a claim rests only on a search summary or on a page that sells something, I say so.
A large fraction of the "review" pages that rank for these queries
(finalroundai.com, lodely, articuler, prachub, devinterview.ai, mockif, shadecoder,
lastroundai) are **competitor-owned SEO content**: they exist to rank for
"X review" and funnel you to their own product. I have used them only for price points,
which are checkable and which they have little incentive to fake, and discarded their verdicts.

---

# A. Mock interview and live-practice platforms

## Summary table

| Platform | Cost | Quant signal? | Verdict |
|---|---|---|---|
| interviewing.io | Free peer tier + AI; paid $179–$339/session; ~$2,000 for 3-session package | Weak — SWE/FAANG pool, not trading | Good for *quant dev* coding rounds. Overpriced for what a quant needs. |
| Pramp (now Exponent Practice) | Free, 5 peer credits/month | Very weak | Free, so cost/benefit is fine. ~20% no-show rate reported. |
| Exponent (paid) | $79/mo, $144/yr; coaching $249/hr; "Ace the Interview" $1,499 | Weak | Skip. PM/SWE-oriented. |
| Meetapro | Marketplace, interviewer-set; interviewers reportedly earn $100–$500/hr | Depends entirely on who is listed | Only worth it if you find an actual trading-firm interviewer. |
| Karat | Free via Brilliant Black Minds (eligibility-gated); otherwise you can't buy it | None | Karat is a B2B vendor. Not a prep product. |
| Hello Interview | Premium $47/mo, $79/yr, $279 lifetime | **None** | Excellent for SWE system design. Irrelevant to quant. **Mocks were discontinued May 2026.** |
| Discord / peer communities | Free | Variable, mostly dead | The old quant peer-mock Discord reportedly degraded into spam. |
| Quant-specific (Tradermath, QuantPrep, CoachQuant, WSQ) | Varies, mostly paid | **Highest** | Only category built for trading interviews. Heavy marketing — be skeptical. |

## interviewing.io

- <https://interviewing.io>
- Anonymous, voice-only mocks with engineers from named companies; sessions recorded with
  interviewer annotations. This is the genuinely differentiated feature — you can rewatch
  yourself, which almost nothing else offers.
- **Free tier exists and is underrated in most coverage**: an AI interviewer, a peer-matching
  queue, and 200+ problems from *Beyond Cracking the Coding Interview*. If you only ever use
  the free tier, this platform is a good deal.
- Paid: reviews consistently converge on ~$179 entry, $225–$300 for company-targeted,
  up to ~$339 for FAANG-branded, and ~$2,000 for a 3-session coaching package (periodic
  $200–$700 discounts).
  - <https://igotanoffer.com/blogs/tech/interviewingio-alternatives>
  - <https://medium.com/@mockingbird_71808/i-paid-225-for-interviewing-io-was-it-worth-the-money-fbc9aee76acb>
- **Quant relevance: limited.** The interviewer pool is FAANG/big-tech SWE. That maps onto
  a **quant developer** coding screen (C++/DS&A, live coding under pressure) but gives you
  essentially nothing on probability, mental math, market-making games, or EV reasoning —
  i.e. the part of a trading interview that actually filters people.
- Honest verdict: **use the free tier; buy 1–2 paid sessions at most, and only if your problem
  is delivery rather than knowledge.** A Blind commenter's framing is the right one — nobody
  guarantees you pass, and ~$5k of sessions against hundreds of hours of self-study is a bad
  trade unless you are specifically bad at performing.

## Pramp → Exponent Practice

- <https://www.tryexponent.com/practice> (Pramp was acquired by Exponent in 2021; new sessions
  have run on Exponent Practice since July 2024)
- **Free: 5 peer mock credits/month.** You alternate interviewer/candidate, platform supplies
  the question, shared editor, structured feedback form.
- Known failure modes reported across coverage: **~20% no-show rate**, and feedback quality
  is entirely a function of who you're matched with. You will often be interviewed by someone
  less prepared than you.
- **Quant relevance: near zero.** The question bank is standard SWE.
- Verdict: **free, so use it purely as reps for talking while coding.** Do not expect signal.
  Its real value is desensitizing you to being watched.

## Exponent (paid tiers)

- $79/mo, or ~$12/mo billed annually (~$144/yr). Expert coaching **$249/hr**.
  "Ace the Interview Program" (assessment + 5 mocks + 1yr courses) **$1,499**.
  - <https://igotanoffer.com/en/advice/tryexponent-alternatives>
  - <https://www.lodely.com/blog/exponent-pricing>
- Verdict: **skip for quant.** Its center of gravity is PM/SWE/data. The $1,499 program is
  the sort of bundle that exists because bundles convert, not because you need five mocks.

## Meetapro

- <https://www.meetapro.com> (site itself was blocked from this sandbox)
- Airbnb-style marketplace: individual interviewers list themselves and set prices;
  reporting suggests interviewers earn **$100–$500/hr**. No published candidate-side rate card —
  price varies per person.
- **Quant relevance: this is the one platform where it's *possible* to book an actual trading-firm
  interviewer**, because supply is individual rather than curated by a SWE-focused company.
  But there is no guarantee such a person is listed at any given time.
- Verdict: **worth 10 minutes of browsing to see who is actually on it.** If a current Optiver/IMC/
  Jane Street person is listed, one session is probably the highest-signal dollar in this whole
  section. If not, it's just a pricier interviewing.io.

## Karat

- <https://karat.com>
- **Karat is not a prep product.** Companies pay Karat to run their first-round technical
  interviews; candidates never buy it. There is no "Karat practice" you can purchase.
- The free path is **Brilliant Black Minds** (<https://karat.com/brilliant-black-minds/>) —
  100% free mock technical interviews plus company connections, but it is an
  eligibility-gated program for engineers underrepresented in tech, not open enrollment.
- Verdict: **if you're eligible, it's free and real** (you're interviewed by people who
  interview professionally). Otherwise not an option. Zero quant content either way.

## hellointerview.com

- <https://www.hellointerview.com>
- Premium is a **one-time purchase, no auto-renew: $47 (1 month) / $79 (1 year) / $279 (lifetime)**.
  Substantial free tier including one free Guided Practice problem, plus a free blog and
  YouTube channel.
  - <https://igotanoffer.com/en/advice/hello-interview-alternatives>
- **Important 2026 change: Hello Interview wound down its mock interview and mentorship
  programs on 31 May 2026.** It is now a self-serve courses + guided-practice + AI-tutor
  platform. So it no longer belongs in a "live practice" comparison at all.
- Reputation (via Blind thread summaries, second-hand): widely called the best system-design
  resource available; "HelloInterview + LeetCode" cited as best ROI; the "key technologies"
  section praised. One recurring criticism: **difficulty calibration is soft** — people suspect
  a mid-level engineer can pass a staff-level bar after enough of it, which means it teaches
  the *rubric* rather than the *engineering*.
- **Quant relevance: none.** Distributed-systems design is not what trading firms ask.
  For a quant developer role at a smaller shop you may get a systems-design conversation,
  but it will be about market data pipelines and latency, not consistent hashing.
- Verdict: **$79/yr is cheap and the product is good — but it is a big-tech SWE product.**
  Buy it if you are also interviewing at FAANG. Do not buy it *for* quant.

## Peer practice via Discord / Reddit

- **This channel has degraded.** The most concrete report found: there was an active
  peer-to-peer quant mock Discord several years ago, and it has since become spam; the
  recommended fallbacks are Meetapro, interviewing.io, or Pramp.
  - <https://www.jointaro.com/question/2AmOczfnBszQLotl3MzI/help-with-mock-interviews-for-quant-researchtrading/>
- Paid programs (WallStreetQuants) run their own Discord and use community access as a
  retention feature — that's a real benefit but it's inside a paywall.
  <https://www.thewallstreetquants.com/>
- Verdict: **free and worth trying, but do not build a plan around it.** The reliable free
  peer channel today is Exponent's 5 credits/month, not Discord.

## Quant-specific practice (the category that actually matters)

None of the above were built for trading interviews. These were:

- **Tradermath** — <https://www.tradermath.org/> — mental math under time pressure plus
  simulated cognitive/sequence tests. This is the single most *mechanically* relevant thing:
  Optiver/IMC-style arithmetic screens are a real, timed, pass/fail gate and they are trainable.
- **QuantPrep** — <https://quantprep.io/>
- **CoachQuant** — <https://coachquant.substack.com/> — markets itself as "hyper-realistic quant
  mock interviews," "developed with 100+ students." Treat that phrasing as marketing.
- **WallStreetQuants** — <https://www.thewallstreetquants.com/> — bootcamp; connects candidates
  with students who recently interviewed at target firms. That last part is the actual value
  (recent, specific question intel), and it is also the part you can sometimes get free.
- **Free and high-value**: `mikinty/Trading-Interview-Questions` —
  <https://github.com/mikinty/Trading-Interview-Questions> — **1,000 stars**, updated recently.
  A structured guide to preparing for quant trading roles out of college. Free.

## Do mocks actually improve outcomes, or is it just LeetCode volume?

Honest answer: **there is no controlled evidence either way.** Every source arguing "5 mocks
beat 500 LeetCode problems" is published by a company that sells mocks
(e.g. <https://medium.com/@mockingbird_71808/why-5-mock-interviews-outperform-500-leetcode-problems-d39a8327c214>).
That is a marketing claim, not a finding.

The one framing that recurs across *non-selling* sources and is mechanically sensible:

> **Do more mocks when your execution is off. Do more problems when your knowledge is
> thin.** Past ~100 solved problems, marginal pattern recognition drops and the binding
> constraint shifts to communication under pressure.
> — <https://www.jointaro.com/question/U4kohSE8g5LR7GD9cqYH/mock-interviews-vs-leetcode/>

Two things mocks genuinely train that solo grinding cannot: **thinking out loud** and
**recovering when you're wrong in front of someone**. Two things they do not: raw
probability fluency and mental-math speed.

**For quant specifically the ordering is different from SWE:**

1. Probability/stats and mental math are the actual filter. No amount of mock practice
   substitutes for knowing them. Green/Zhou-style problem volume dominates early.
2. Market-making and EV games *are* interactive and *do* need live practice — but a generic
   SWE mock partner cannot run one. You need a quant-specific partner or platform.
3. LeetCode volume matters mainly for the **quant developer** track, less for trading.
4. Interviewers are idiosyncratic — multiple accounts note questions "depend on the
   interviewer's background," which caps how much any single mock generalizes.

**Verdict: spend money on mocks last, not first, and spend it on quant-specific ones.**
Two well-chosen quant mocks late in prep beat six generic SWE mocks early.

---

# B. C++ and low-latency systems learning (quant DEVELOPER track)

Star counts and last-push dates below are from live GitHub API calls on 2026-09-06 and are
the most reliable signal in this section.

## Tier 1 — practitioners actually use these daily

**cppreference.com** — <https://en.cppreference.com/> — Free.
The reference. Community consensus, consistently, is that it is **more thorough than
cplusplus.com** (which is the site to avoid; it is stale and occasionally wrong). The
recurring criticism is verbosity — it documents the standard, not idioms.
**Verdict: non-optional. Bookmark it and stop using cplusplus.com.**

**Compiler Explorer / godbolt.org** — <https://godbolt.org/> — Free, open source.
Started 2012 to show how C++ constructs lower to assembly; now serves **~2,000,000
compilations/week** (<https://xania.org/202206/happy-birthday-ce>). For low-latency work this
is the primary feedback loop: you write the thing, you look at the asm, you find out whether
the branch survived or the call inlined. Self-hostable.
**Verdict: the single most important tool on this list for a latency-track developer.**
Learning to *read* the output is the actual skill; the site is just the window.

**learncpp.com** — <https://www.learncpp.com/> — Free.
Modular, incrementally-difficult lessons from basics through concurrency and memory
management, with quizzes and "advanced material" asides. Free and actively updated.
Its reputation as *the* free C++ tutorial is durable and I found no credible dissent.
**Verdict: if you don't already know C++, start here and finish it.** It is better than most
paid courses. It is a *language* tutorial, not a performance one — it will not teach you
anything about cache lines.

**Agner Fog's optimization manuals** — <https://www.agner.org/optimize/> — Free.
Five volumes covering C++ optimization, assembly, calling conventions, microarchitecture
(out-of-order execution, register renaming, pipelines, branch prediction), and instruction
tables (latency/throughput/µop breakdowns) for Intel/AMD/VIA.
**Still actively maintained — instruction tables last updated 2025-09-20.** Cited in academic
CPU-modeling work (e.g. the uiCA throughput-prediction paper).
**Verdict: the primary source, not a tutorial.** Nobody reads these cover to cover.
You read the microarchitecture volume for your target chip once, then use the instruction
tables as a lookup for the rest of your career. If someone in an interview asks why your
loop is 4 cycles slower, this is where the answer lives.

## Tier 2 — high-value structured learning

**perf-ninja (Denis Bakhvalov)** — <https://github.com/dendibakh/perf-ninja> —
**3,846 stars, 399 forks, last push 2026-09-06 (actively maintained).** Free (donations
requested via GitHub Sponsors/Patreon).
Lab-assignment format: each lab is a specific performance defect (cache misses, branch
mispredicts), 30 min to 4 hrs each, C++, and you **submit to GitHub for automated
benchmarking and verification.** Ported to Rust and Zig by others.
Author works at Intel on cross-stack performance; also writes <https://easyperf.net/> and
the *Performance Analysis and Tuning on Modern CPUs* book.
**Verdict: the best free hands-on low-level performance course that exists, and the
automated verification is what makes it stick.** For a quant-dev portfolio this is also
directly citable — "I completed the perf-ninja labs" is a concrete, checkable claim.
This is my top recommendation in section B after Compiler Explorer.

**Algorithmica / "Algorithms for Modern Hardware" (Sergey Slotin)** —
<https://en.algorithmica.org/hpc/> — Free, open-source
(<https://github.com/algorithmica-org/algorithmica>, **4,993 stars**;
code at <https://github.com/sslotin/amh-code>, **838 stars**).
Audience is explicitly "people who finished an advanced algorithms course and want
practical speedups rather than going from O(n log n) to O(n log log n)." Concrete results
in the text: binary search ~15x faster than `std::lower_bound` for small arrays / ~8x for
large; Floyd-Warshall ~50x over naive.
**Honest caveat: the book is unfinished and the author has said writing is slow and
non-sequential (6+ months idea-to-published-article).** Some chapters are stubs.
**Verdict: the best free HPC text for the "why is my code slow on this specific CPU"
question, with the caveat that it's incomplete.** The SIMD and memory chapters are the
strongest. Read it after perf-ninja, not before.

**Brendan Gregg** — <https://www.brendangregg.com/linuxperf.html> — Site free; books paid.
*Systems Performance* 2nd ed. (2020/2021) and *BPF Performance Tools* (2019), both
Addison-Wesley. The first edition of Systems Performance became required reading at many
companies and was translated into four languages — that's an unusually strong adoption
signal for a performance book.
**Verdict: the free site (flame graphs, USE method, the tool-map diagrams) is genuinely
sufficient for a while.** Buy *Systems Performance* if you end up owning production Linux
boxes. *BPF Performance Tools* is a 150-tool cookbook — reference, not reading.
This is the Linux-observability half of the skill set that Agner Fog doesn't cover.

**OSTEP — Operating Systems: Three Easy Pieces** —
<https://pages.cs.wisc.edu/~remzi/OSTEP/> — **Free** (individual chapters online; print
edition purchasable). Code: <https://github.com/remzi-arpacidusseau/ostep-code>,
**4,393 stars, 1,598 forks** (last push 2023 — the code is stable, not abandoned).
Featured on Teach Yourself CS; repeatedly cited as the best self-study OS book, with
projects included.
**Verdict: yes, do this.** Trading systems interviews *will* ask about scheduling, context
switches, page faults, NUMA, and why your thread got preempted. This is where that comes
from, and it's free and genuinely well-written. Higher priority for quant dev than most
people assume.

**Beej's Guide to Network Programming** — <https://beej.us/guide/bgnet/> — Free
(source: <https://github.com/beejjorgensen/bgnet>, **1,239 stars**, last push 2026-08).
Ground-up sockets in C, complete client/server examples, IPv4 and IPv6.
**Verdict: still the fastest path from zero to "I understand what a socket is."**
It is a *starting* text — it will not teach you kernel bypass, `io_uring`, busy-polling, or
`SO_BUSY_POLL`, which is where actual low-latency networking lives. Read it in a weekend,
then move to the real material.

## Tier 3 — good, but supplementary

**quick-bench.com** — <https://quick-bench.com/> — Free. (Site was blocked from this sandbox,
so I could not confirm current uptime — it has historically had outages.)
Runs Google Benchmark microbenchmarks in the browser and charts the comparison. Jason Turner
covered it in C++ Weekly ep. 70 (<https://isocpp.org/blog/2017/07/cpp-weekly-episode-70-c-iife-in-quick-bench.comjason-turner>),
which is also where you learn the **IIFE trick** needed to stop the optimizer from deleting
your benchmark.
**Verdict: useful for quick A/B intuition, but do not trust it for anything you'd act on.**
Shared cloud hardware, no control over frequency scaling, noisy neighbours. For real numbers
you need your own pinned, isolated core. Treat it as a conversation aid, not a measurement.

**Jason Turner's C++ Weekly** —
<https://www.youtube.com/channel/UCxHAlbZQNFU2LgEtiqd2Maw> — Free, 400+ episodes.
Short (5–20 min) single-topic episodes, heavy Compiler Explorer use.
**Verdict: excellent for breadth and for absorbing modern-C++ idioms by osmosis; weak as a
structured curriculum.** Best consumed as background while you learn elsewhere. The
constexpr and "compiler removes your code" episodes are the ones that matter for latency work.

**"Awesome Modern C++"** — <https://github.com/rigtorp/awesome-modern-cpp> —
**13,152 stars, 1,232 forks — but last push 2024-08-20, i.e. ~2 years stale.**
Note who maintains it: **Erik Rigtorp**, who is a genuinely respected low-latency
practitioner — his `SPSCQueue` (<https://github.com/rigtorp/SPSCQueue>, **1,286 stars**,
active) is a canonical lock-free single-producer/single-consumer ring buffer and is far more
worth your time than the list.
**Verdict on the list: mildly useful as a link dump, not a curriculum, and going stale.**
**Verdict on rigtorp's own repos and blog: read them.** That's where the actual signal is.

**AwesomePerfCpp** — <https://github.com/fenbf/AwesomePerfCpp> — **2,555 stars.**
Curated C/C++ performance talks, articles, books, tools. Better-targeted than
awesome-modern-cpp for this track.

## CppCon and conference talks — the specific ones worth watching

**Carl Cook, "When a Microsecond Is an Eternity: High Performance Trading Systems in C++"
(CppCon 2017)** — <https://www.youtube.com/watch?v=NH1Tta7purM> —
slides: <https://github.com/CppCon/CppCon2017>
Cook has a PhD (Canterbury, 2006) and worked at Optiver on the execution stack.
The framing is the useful part: **the critical path is a tiny fraction of the codebase, is
invoked infrequently and unpredictably, and must still execute without delay** — which is
why normal profiling advice fails in trading. Techniques covered: keep the hot path free of
anything not strictly needed, templates instead of runtime branches for configuration,
lambdas, memory reuse, cache warming.
**Verdict: this is the canonical talk and effectively required watching for the quant-dev
track.** If you can discuss the "cold code on the hot path" problem intelligently, you sound
like someone who has thought about trading systems rather than someone who has read a blog post.

**David Gross (Optiver), "When Nanoseconds Matter: Ultrafast Trading Systems in C++"
(CppCon 2024 keynote)** — <https://www.youtube.com/watch?v=sX2nF1fW7kI> —
<https://cppcon.org/2024-keynote-david-gross/> — 89 minutes.
Deep dive on **order book data-structure optimization**, industry-standard low-latency C++
patterns, multi-core/concurrency handling, and system tuning (**C-state and P-state,
shared-LLC optimization**).
Earlier version: "Trading at light speed: designing low latency systems in C++"
(Meeting C++ 2022) — <https://meetingcpp.com/2022/Talks/items/Trading_at_light_speed__designing_low_latency_systems_in_Cpp.html>
**Verdict: the best single modern talk, and it pairs directly with the order-book project in
section C.** Its central claim — that latency must be a design-phase constraint, not a
later optimization — is the thing interviewers want to hear you internalize.
Watch this one *after* you've attempted an order book yourself, so the optimizations land.

**Chandler Carruth, "Efficiency with Algorithms, Performance with Data Structures"
(CppCon 2014)** — <https://www.youtube.com/watch?v=fHNmRkzxHWs> — slides in
<https://github.com/CppCon/CppCon2014>.
The distinction in the title *is* the content: algorithms buy you efficiency (less work),
data structures buy you performance (work done faster, because of memory layout).
**Verdict: still the best conceptual reframing available, and it's 12 years old without
having aged much** — because the memory wall it describes only got worse. Watch it early;
it changes how you read every other talk on this list.

## Also worth knowing about (surfaced during research)

- **Sourav Ghosh, *Building Low Latency Applications with C++*** (Packt) — paid book; code at
  <https://github.com/PacktPublishing/Building-Low-Latency-Applications-with-CPP>
  (**710 stars, 211 forks**). Repeatedly recommended in HFT-resource discussions. Packt
  quality is inconsistent as a publisher, but this title has traction.
- **`0burak/imperial_hft`** — <https://github.com/0burak/imperial_hft> —
  **1,240 stars, 202 forks, active.** Low-latency techniques with benchmarks: cache warming,
  `constexpr`, loop unrolling, lock-free programming, short-circuiting. Concise and concrete.
- **"C++ design patterns for low-latency applications including high-frequency trading"**
  (arXiv) — <https://arxiv.org/pdf/2309.04259> — free, and a legitimate citable reference.
- **LMAX Disruptor** — <https://github.com/LMAX-Exchange/disruptor> — **18,463 stars.**
  Java, but the *design* (mechanical sympathy, ring buffer, single-writer principle) is the
  foundational text for low-latency trading architecture regardless of language.

## Section B verdict — the actual order

1. learncpp.com (if you need the language) → cppreference as reference
2. Compiler Explorer, continuously, forever
3. perf-ninja labs — the highest-leverage single item
4. Carruth 2014 → Cook 2017 → Gross 2024 (in that order)
5. OSTEP + Beej (systems substrate)
6. Algorithmica/HPC and Agner Fog as depth-on-demand
7. Brendan Gregg when you own real machines

Everything here except the Gregg and Ghosh books is **free**. Total cash cost of a
serious quant-dev C++ curriculum: **$0**.

---

# C. Project-based learning: data, frameworks, reference code, competitions

## C1. Market data

| Source | Cost | Best for | Verdict |
|---|---|---|---|
| yfinance | Free | Prototyping, EOD equities | Fine to start, fragile to depend on |
| Nasdaq Data Link | Free tier much reduced | FRED, some commodities | WIKI equities is dead; mostly a paid catalog now |
| Massive (ex-Polygon.io) | Free tier; paid $29–$3,500/mo | Real quotes/trades at retail prices | Best paid on-ramp; free tier is 1yr history only |
| Databento | $125 free credit; ~$199/mo Standard | **MBO / L3, nanosecond stamps** | The one that matters for microstructure |
| LOBSTER | Free samples; paid otherwise | Reconstructed NASDAQ LOB | Best free order-book data, period |
| Kaggle | Free | Curated competition datasets | Free real trading data via Optiver/Jane Street comps |

**yfinance** — <https://github.com/ranaroussi/yfinance> — **25,183 stars, 3,411 forks, active.**
Explicitly research/educational; it scrapes Yahoo. **Fails on rate limits, schema drift, and
commercial use.** Verdict: **use it for the first 48 hours of a project, then leave.**
Building anything you care about on top of an unofficial scraper is how projects die.

**Nasdaq Data Link (formerly Quandl)** — <https://data.nasdaq.com/> — Python package free;
most datasets premium. **The free WIKI equity time-series is discontinued** — a lot of old
tutorials still reference it and will not work. What remains free: FRED economic data, select
commodities, and free samples of premium sets. Verdict: **mostly a store now.** Fine for
macro series, not a general free-data source anymore.

**Massive (formerly Polygon.io)** — <https://massive.com/> — **Rebranded 30 Oct 2025;
`api.polygon.io` still works alongside `api.massive.com`, keys unchanged**
(<https://massive.com/blog/polygon-is-now-massive>).
Free tier is real but **capped at one year of history for stocks** — that is the binding
limitation and it kills most serious equity backtests. The **crypto free tier is materially
more generous** and is the sane way to use the free plan. Paid $29–$3,500/mo.
Verdict: **best value paid retail feed; free tier is a demo.** If you want a free order-book
project, do it in crypto here.

**Databento** — <https://databento.com/> — **$125 in free credits on signup, expiring after
six months**; usage-metered, or ~$199/mo Standard. Offers **MBO (market-by-order): every add,
cancel, execute, and snapshot, timestamped to the nanosecond**, plus DBN (compact binary),
CSV and JSON. Covers CME Globex MDP 3.0 and OPRA. First-class NautilusTrader integration
(<https://nautilustrader.io/docs/latest/integrations/databento/>).
Verdict: **if you are building anything that touches market microstructure, this is the
one to use, and $125 of free credit is enough for a real portfolio project.** Nothing else
at retail prices gives you L3 with nanosecond timestamps. Watch the credit expiry — plan
the project before you sign up, not after.

**LOBSTER** — <https://lobsterdata.com/> — Academic since 2013, now also commercial.
Reconstructs the NASDAQ limit order book to arbitrary depth from ITCH. Per ticker per day
you get a **message file** (event-by-event exchange messages) and an **orderbook file**
(event-by-event book snapshots), both CSV.
**Free sample files: AAPL, AMZN, GOOG, INTC, MSFT.**
Verdict: **the best free limit-order-book data available, and the samples are enough for a
genuine project.** The message/orderbook file pair is also a great forcing function — you
can rebuild the book from messages and diff against their snapshots, which is a
self-verifying exercise and an excellent portfolio piece.

**Kaggle** — free, and an underrated data source: the Optiver and Jane Street competition
datasets are real, firm-provided, well-documented trading data you cannot otherwise get.

## C2. Backtesting frameworks

Live GitHub data, 2026-09-06:

| Framework | Stars | Forks | Last push | Language | License |
|---|---|---|---|---|---|
| backtrader | 23,150 | 5,266 | **2024-08-19** | Python | GPL-3.0 |
| QuantConnect/Lean | 21,500 | 5,220 | 2026-09-05 | C# | Apache-2.0 |
| NautilusTrader | 28,520 | 3,715 | 2026-09-06 | Rust | LGPL-3.0 |
| vectorbt | 9,013 | 1,158 | 2026-08-02 | Python | Apache-2.0 + Commons Clause |
| backtesting.py | 8,937 | 1,531 | 2026-08-05 | Python | AGPL-3.0 |
| hftbacktest | 4,616 | 895 | 2026-09-06 | Rust | — |
| zipline-reloaded | ~1,900 | 331 | active | Python | Apache-2.0 |

**backtrader** — <https://github.com/mementum/backtrader> — Free, GPL-3.0.
23k stars, huge tutorial corpus. **But `pushed_at` is 2024-08-19 — no commits in ~2 years,
and issues are disabled on the repo.** It is a dead project with excellent SEO.
Verdict: **do not start new work here in 2026, regardless of how many tutorials say to.**
The star count is a historical artifact. The stale-tutorial problem is real and compounding.

**QuantConnect / LEAN** — <https://github.com/QuantConnect/Lean> — **LEAN engine is
Apache-2.0 and free to self-host**; the cloud platform is where the money is
(free tier: **unlimited backtesting** with community support and included historical data;
paid $60/mo Researcher up to $1,080/mo Institution).
Verdict: **the strongest "free tier that is actually usable" in this list**, and C# +
Python is a nice fit if you're on the developer track. The lock-in risk is real — LEAN is
open source but the data and broker integrations are what make it convenient.
For a portfolio, self-hosted LEAN reads as more serious than cloud.

**NautilusTrader** — <https://github.com/nautechsystems/nautilus_trader> —
**28,520 stars — the most-starred item in this entire report** — LGPL-3.0, free,
Rust core with Python control plane, actively developed (pushed today).
Its genuine differentiator is **research-to-live parity: the same strategy code runs in
backtest and live**, which kills the classic "backtest wins, live loses" failure.
**Honest caveat, and it's a real one: the learning curve is steep for beginners and experts
alike.** You need solid Python, you must bring your own market data, and there is no
point-and-click mode. Rust + Cython means build complexity.
Verdict: **the best thing to learn if you want the project to signal seriousness**, and the
Databento integration means data and engine fit together. Not the thing to learn first.

**vectorbt** — <https://github.com/polakowo/vectorbt> — 9,013 stars, active.
**License trap: Apache 2.0 *with Commons Clause* — free to use, but you may not sell a
product that is primarily this software.** The successor **vectorbt PRO** is proprietary and
invite-only via GitHub sponsorship.
Verdict: **excellent at what it does — massive vectorized parameter sweeps, thousands of
variants fast.** But that strength is also its hazard: it makes overfitting frictionless.
The open version is real and usable; be clear-eyed that the maintainer's attention has
moved to PRO.

**zipline-reloaded** — <https://github.com/stefan-jansen/zipline-reloaded> — ~1,900 stars,
331 forks, Apache-2.0, free. Stefan Jansen's revival of Quantopian's Zipline after the 2020
shutdown, maintained largely to support his *Machine Learning for Algorithmic Trading* book;
kept current with NumPy 2.0 / pandas 2.0+, Python 3.9+. Community forum at exchange.ml4trading.io.
Verdict: **a competent rescue of a dead project, and it's alive where original Zipline isn't** —
but it exists in a book's orbit. Use it if you're working through that book. Otherwise the
event-driven niche is better served by Nautilus or LEAN.

**backtesting.py** — <https://github.com/kernc/backtesting.py> — 8,937 stars, active,
**AGPL-3.0 (aggressive copyleft — matters if you ever want to show this to an employer's
legal department).** Small, readable, quick to learn.
Verdict: **best framework to read the source of**, precisely because it's small enough to
understand end to end.

**hftbacktest** — <https://github.com/nkaz001/hftbacktest> — **4,616 stars, 895 forks,
pushed today.** Rust. This is the specialist: it models **limit orders, queue position, and
latency** using full tick data with L2 *and L3* order books, with working Binance/Bybit examples.
Verdict: **the only one on this list that simulates the things that actually determine
whether a market-making strategy is real.** Queue position and latency modelling are where
naive backtests lie to you. For a market-making portfolio project this is the correct tool
and it will differentiate you.

## C3. Order book / matching engine reference implementations

Reading and then rebuilding a matching engine is, in my judgment, **the single highest-signal
portfolio project for the quant developer track** — it exercises data structure design,
cache behaviour, latency measurement, and domain knowledge simultaneously, and it maps
directly onto David Gross's talk.

Live star counts:

| Repo | Stars | Lang | Note |
|---|---|---|---|
| [LMAX-Exchange/disruptor](https://github.com/LMAX-Exchange/disruptor) | 18,463 | Java | The architectural ancestor |
| [exchange-core/exchange-core](https://github.com/exchange-core/exchange-core) | 2,617 | Java | Disruptor + ART, most complete |
| [enewhuis/liquibook](https://github.com/enewhuis/liquibook) | 1,499 | C++ | Modern C++ matching engine |
| [Crypto-toolbox/HFT-Orderbook](https://github.com/Crypto-toolbox/HFT-Orderbook) | 1,386 | C/Python | WK Selph design — read this first |
| [rigtorp/SPSCQueue](https://github.com/rigtorp/SPSCQueue) | 1,286 | C++ | Lock-free SPSC ring buffer |
| [0b01/tectonicdb](https://github.com/0b01/tectonicdb) | 753 | Rust | L2 order book database |
| [i25959341/orderbook](https://github.com/i25959341/orderbook) | 559 | Go | Clean, small, readable |
| [joaquinbejar/OrderBook-rs](https://github.com/joaquinbejar/OrderBook-rs) | 524 | Rust | Lock-free, thread-safe |
| [dyn4mik3/OrderBook](https://github.com/dyn4mik3/OrderBook) | 411 | Python | Oldest; clearest for learning |
| [brprojects/Limit-Order-Book](https://github.com/brprojects/Limit-Order-Book) | 204 | C++ | Claims 1.4M tx/sec, gtest, CMake |

**Suggested reading order:**
1. `dyn4mik3/OrderBook` (Python) — understand the data structure without fighting a language.
2. `Crypto-toolbox/HFT-Orderbook` — the **WK Selph** design (hash map to order nodes,
   doubly-linked list per price level, self-balancing tree over price levels). This is the
   canonical answer to "how would you build a limit order book" and you should be able to
   draw it from memory.
3. `enewhuis/liquibook` or `brprojects/Limit-Order-Book` — production-shaped C++.
   The latter is small enough to read fully, ships **googletest + CMake**, and its
   throughput claim gives you a benchmark target to beat.
4. `rigtorp/SPSCQueue` — how the threads actually talk to each other.
5. `exchange-core` and the LMAX Disruptor — for the *architecture* (single-writer principle,
   mechanical sympathy), even if you never write Java.

**Honest note:** `brprojects/Limit-Order-Book`'s "1.4 million transactions per second" is an
unaudited self-reported number on unspecified hardware. Treat every such claim in this space
as marketing until you reproduce it. Reproducing it is itself a good exercise.

## C4. Competitions that feed recruiting

**IMC Prosperity** — <https://prosperity.imc.com/> — **Free, fully online, global, teams of
up to five, run each spring since 2023.** Python program trading a virtual market
(the flavour is deliberately silly — wasabi roots, pineapples).
**Recruiting link is explicit and confirmed: standout performers can be fast-tracked to
final-round interviews for IMC's Summer Internship Programme in Trading.**
Verdict: **the single best accessible-to-anyone competition on this list.** Free, no
gatekeeping, multi-week, and the recruiting pipeline is stated rather than implied.
Reality check: thousands compete; the 70th-globally result cited by one university ACM
chapter is a strong finish, so calibrate expectations. Even a mediocre finish gives you a
concrete thing to talk about in an interview, which is most of the value.

**Optiver Ready Trader Go** — <https://readytradergo.optiver.com/> — Free.
Algorithmic market-making competition. **Important caveat: it has run intermittently rather
than annually — check Optiver's careers page rather than assuming a current edition exists.**
Verdict: **outstanding when it runs** (market making is exactly the skill trading firms
hire for), but you cannot plan around it. Do the past problems regardless if archives exist.

**Jane Street** — puzzles at <https://www.janestreet.com/puzzles/> — free, monthly.
Also the **Electronic Trading Challenge (ETC)**, which is **largely invitation-based and
tied to campus recruiting** — entry usually comes via your university, prior Jane Street
events, or engagement with the puzzles.
On the puzzles specifically: applications occasionally include math/logic puzzles, and while
optional, **solving them correctly is a signal that can get a borderline résumé a second look.**
Verdict: **puzzles are low-cost, low-probability, non-zero-value.** Do them because they're
good practice and because they're the documented on-ramp to ETC — not because a solved
puzzle gets you hired. ETC is the higher-value item and puzzles are how you become visible
enough to be invited.

**Citadel / Correlation One** — <https://www.correlation-one.com/> —
Citadel runs **Discover** and **Datathon** events in spring (sophomore-track deadlines
typically February/March) and **fast-tracks strong performers straight to final rounds.**
Cash prizes up to **$15,000** plus explicit recruiting access for internships and full-time.
**Terminal**, an algorithmic head-to-head strategy game built by Correlation One and
sponsored by Citadel, works the same way.
Verdict: **the most direct competition-to-final-round pipeline documented here.** Datathons
are data-science-shaped (a weekend, a dataset, a presentation), so they suit the
quant-research track more than quant dev. Team quality dominates the outcome — recruit
teammates seriously.

**Kaggle finance competitions** — free.
- Optiver — Trading at the Close: <https://www.kaggle.com/competitions/optiver-trading-at-the-close>
  (predicting US equity closing auction movements)
- Jane Street Real-Time Market Data Forecasting (launched 14 Oct 2024):
  <https://www.kaggle.com/competitions/jane-street-real-time-market-data-forecasting>
- Jane Street Market Prediction (earlier):
  <https://www.kaggle.com/competitions/jane-street-market-prediction>
Verdict: **the honest value here is the data and the public solutions, not the recruiting.**
Unlike Prosperity or Citadel Datathon, I found **no documented fast-track from a Kaggle
finish to an interview.** These competitions are firm-branded research and marketing. But
the datasets are real firm data, the winners publish their methods, and the top-solution
write-ups are one of the few honest windows into how these firms actually think about
signal. Compete for the education; don't expect a recruiter call.

**Recruiting-value ranking (highest to lowest, based on documented fast-tracks):**
1. Citadel Datathon / Terminal — explicit fast-track to final rounds
2. IMC Prosperity — explicit fast-track, and open to everyone
3. Jane Street ETC — real, but invitation-gated
4. Optiver Ready Trader Go — high value, unreliable availability
5. Jane Street puzzles — a tiebreaker signal, not a channel
6. Kaggle finance comps — great learning, no documented pipeline

## C5. Suggested portfolio projects, ordered by signal-per-hour

1. **Limit order book + matching engine in C++**, benchmarked, with tests.
   Rebuild from LOBSTER message files and diff against their orderbook snapshots — it is
   self-verifying, which is rare and which you can state credibly. Pair with Gross's talk.
2. **perf-ninja completion** — automated, verifiable, and specific.
3. **Market-making strategy in hftbacktest** with honest queue-position and latency modelling.
   The honesty is the differentiator; anyone can show a good backtest.
4. **IMC Prosperity entry**, whatever the finish.
5. **A microstructure study on Databento MBO or LOBSTER samples** — e.g. order-flow imbalance
   vs short-horizon returns. Well-trodden in the literature, which means you can check yourself
   against published results.

Note the through-line: **every one of these except Prosperity is doable for $0**, and the
one paid option (Databento) is covered by its $125 signup credit.

---

## Cost summary

**Free and sufficient for a complete curriculum:** learncpp, cppreference, Compiler Explorer,
perf-ninja, Algorithmica/HPC, Agner Fog, OSTEP, Beej, Brendan Gregg's site, all CppCon talks,
LEAN (self-hosted), NautilusTrader, hftbacktest, backtesting.py, zipline-reloaded, vectorbt
(non-commercial), LOBSTER samples, yfinance, Kaggle, IMC Prosperity, Jane Street puzzles,
Citadel/Correlation One events, interviewing.io free tier, Exponent's 5 peer credits/month.

**Worth paying for, in priority order:**
1. **Databento** — $125 free credit first; ~$199/mo only if a project demands it.
2. **1–2 quant-specific mock interviews**, late in prep, ideally via Meetapro if an actual
   trading-firm interviewer is listed.
3. **Brendan Gregg, *Systems Performance* 2nd ed.** — if you own production Linux boxes.
4. **Hello Interview at $79/yr** — *only* if you're also interviewing at big tech.

**Actively advise against:** Exponent's $1,499 "Ace the Interview" bundle;
interviewing.io's ~$2,000 3-session package; starting anything new on backtrader.

The uncomfortable summary: **the free resources in section B are better than anything sold
in section A.** The paid interview-prep market is large because interview anxiety converts
well, not because the product is scarce. Spend money on *data* (Databento) rather than on
*coaching* — data unlocks projects you can't otherwise build, whereas coaching mostly
repackages information that is already free.
