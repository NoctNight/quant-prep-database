# DSA Practice Sites & Platforms — for quant-firm coding assessments (LC-medium / CF 1600–1800)

Research date: 2026-09-06. ~22 web searches + direct page fetches.

---

## 0. Sourcing caveat — read this first

This sandbox's egress proxy blocked almost every primary source I wanted:

- **Blocked outright (403 from egress policy):** `reddit.com`, `teamblind.com`, `codeforces.com`, `leetcode.com`, `news.ycombinator.com`, `cses.fi`, `techinterviewhandbook.org`, `usaco.guide`, `interviewing.io`, `jeffe.cs.illinois.edu`, `redgreencode.com`, `blog.samarthgoel.com`, `exercism.org`, and every Medium/Substack/dev.to URL I tried.
- `reddit.com` is additionally **not accessible to the search crawler at all** (hard 400: "domains are not accessible to our user agent").
- **Only `github.com` was fetchable.** Everything else here comes from **search-engine summaries** of those pages — i.e. I can see what the thread/blog said, but I could not read the full thread, the vote counts, or the dissenting replies.

**Practical consequence:** treat every Reddit/Blind opinion below as second-hand paraphrase, and every price as "verify on the site before paying."

**Second caveat — the listicle problem is real and worse than you'd think.** A large share of results for these queries are affiliate/SEO/LLM-generated review farms: `prachub.com`, `quantvault.org`, `codeintuition.io`, `lodely.com`, `leetcopilot.dev`, `crackr.dev`, `lastroundai.com`, `beyz.ai`, `interviewfox.ai`, `linkjob.ai`, `myntbit.com`, `algocademy.com`, `toolradar.com`, `coddy.tech`, `guruscoach.com`. Several of these invent oddly specific numbers ("41 firms surveyed", "18 of 20 question banks recur") with no methodology. I've marked anything sourced only from those as **[low confidence]**. Note also that `educative.io`'s blog reviewing its own competitors is a vendor comparing itself to rivals.

---

## 1. LeetCode

**URL:** https://leetcode.com · Premium: https://leetcode.com/subscribe/

**Price (reported, unverified — site blocked):** ~**$35/month** or **~$159/year** (some 2026 sources say $179/yr). https://www.designgurus.io/blog/is-leetcode-premium-worth-it · https://toolradar.com/tools/leetcode/pricing

### What it's genuinely good for
- The **problem archive is the moat**. ~3,500+ problems, and it is still the de facto standard: the recurring line in 2026 threads is "LeetCode is still the meta even now in 2026." https://www.teamblind.com/post/whats-the-meta-for-interviewing-in-2025-2026-8bkk5nc0
- **Community solutions/discuss** — often better than the official editorial.
- **Contests** (free, biweekly + weekly) give you a rated, timed signal. LeetCode's contest rating is an Elo adaptation explicitly modelled on Codeforces' open rating system. https://leetcode.com/discuss/post/468851/

### Premium: what actually earns the money
- **Company tags with a recency filter** (last 30 days / 3 months / 6 months / 1 year / all) sorted by frequency. This is the single feature people say is worth it. https://www.jointaro.com/question/bC78DsNeHfidfH303yW7/best-leetcode-premium-filters-for-company-questions/
- **Editorials** on problems that lack a good community writeup.
- Priority judging and extra AI credits — marketing filler.

### Do the company tags work? Are they accurate?
Honest answer: **partially, and only for high-frequency entries.**
- Tags are **crowdsourced from self-reported interview experiences**, so a high-frequency problem (many independent reports) is usually real; a low-frequency one is often one person's anecdote. https://leetcopilot.dev/blog/how-to-use-leetcode-premium-company-tags-for-targeted-interview-prep
- Consistent Blind sentiment: **works well for Meta/Amazon/Bloomberg-style repeat-question shops, poorly for Google**, which deliberately avoids reusing questions. https://www.teamblind.com/post/leetcode-company-tagged-questions-qgfjhruu
- Multiple reports of "the company specific questions don't seem that accurate or great."
- **For quant firms specifically the tags are thin.** These firms interview a few hundred people a year, not tens of thousands, so the sample behind a "Jane Street" or "Optiver" tag is small and stale. Do not build a quant plan around them.

**Free workaround worth knowing:** community-scraped snapshots of the premium company lists are on GitHub, organised into the same 30-day/3-month/6-month/1-year buckets as CSVs, 200+ companies, 7.8k stars, snapshot dated 12 July 2026. https://github.com/snehasishroy/leetcode-companywise-interview-questions · also https://github.com/xizhang20181005/Leetcode_company_frequency

### Explore cards
Mixed-to-mediocre. The recurring complaints: **difficulty ramps too fast** (the first backtracking example is N-Queens), **text-only with no video**, and weak at simplifying recursion for people who don't already get it. https://leetcode.com/discuss/explore/recursion-ii/2674461/Decent-explore-card-but-there's-room-for-improvement/ They're free and fine as a topic index; they are not a curriculum. NeetCode's roadmap or Grind 75 is a better spine.

### What wastes time
- Grinding **Easy** past the first ~40. Zero marginal value for a quant OA.
- Buying Premium **months before** interviews. Consensus: buy **one month during the final sprint**, not a year.
- Chasing a problem count instead of a pattern count (see §11).

### Verdict for your use case
**Essential, but as the *volume* half of a two-platform plan.** Free tier + contests covers ~90% of what you need. Buy one month of Premium only in the 4–6 weeks before a specific interview loop, and expect the company tags to help for the FAANG-adjacent parts of your search more than for the quant firms. LeetCode alone will *not* calibrate you to CF 1600–1800 — its Mediums cluster well below that. **8.5/10.**

---

## 2. NeetCode / neetcode.io

**URL:** https://neetcode.io · YouTube: https://www.youtube.com/c/neetcode (500k+ subs)

**Price (reported):** free tier is large. **NeetCode Pro ~$119/year, ~$219 lifetime** (one source observed **$297 lifetime** on the official page 2026-08-06 — so this has moved). Earlier reporting said $25/mo or $175/yr. https://prachub.com/resources/neetcode-pro-review-2026-is-the-paid-upgrade-worth-it · https://www.codeintuition.io/blogs/neetcode-pro-review

### The lists
- **Blind 75** — the original curated list by Yangshun Tay. Lean, still the fastest "am I ready?" checklist.
- **NeetCode 150** — Blind 75 reorganised + 75 more. **~85% overlap: 64 of the Blind 75 problems appear in NeetCode 150.** The additions are concentrated where Blind 75 was thin: **Graphs +12, DP +10, Greedy +8 (Blind 75 has zero greedy), Backtracking +7.** https://www.codeintuition.io/blogs/neetcode-150-vs-blind-75
- **Greedy being entirely absent from Blind 75 matters for you** — greedy/constructive is *the* dominant Div-2-B/C archetype in the CF 1300–1700 band.
- Also **NeetCode 250 / "NeetCode All"** for more volume. All lists are free.

### The videos
This is the actual product. Free, on YouTube, and the near-universal verdict is that they **rival or beat AlgoExpert's paid explanations**. Clear, concise, whiteboard-then-code, consistent format.

### The paid courses
- Pro adds: structured courses, extra problems, company tags, NeetBot/AI hints, cloud sync, private community.
- The blunt community read: **"NeetCode's free YouTube videos contain 90% of the core value — the Pro features are nice-to-have, not must-have"** and *"if NeetCode YouTube works for you, stick with free. Pro adds convenience, not content."* https://leetcopilot.dev/blog/best-neetcode-pro-alternatives-2025
- **The system design videos are the weak spot** and draw real criticism: "chicken scribble diagramming instead of clear computer graphics," "content on YouTube is superior." https://www.teamblind.com/post/neetcode-premium-system-design-videos-is-a-total-rip-off-hnkorw17
- Recurring nostalgia complaint: "the main thing that made neetcode great was because it was free."

### What it isn't
Not a learning *system*. The sharpest criticism I found applies to both lists: *"Neither list teaches you why a problem is a counting problem and not a sorting problem."* It gives you problems in a good order; it does not build the classification reflex. And it tops out around LC-Hard — nothing here calibrates you to CF 1700+.

### Verdict
**Use the free lists + free videos. Do not pay.** NeetCode 150 is the single best free spine for the LC-medium half of your prep, and its greedy/graph coverage is the reason to pick it over Blind 75. Pro is a convenience purchase; for the same money, one month of LeetCode Premium plus a quant-specific site buys you more. **9/10 free, 5/10 paid.**

---

## 3. Codeforces — the calibration engine

**URL:** https://codeforces.com · EDU: https://codeforces.com/edu/courses

**Price:** free, all of it. No paid tier. Ads-free, run by ITMO-affiliated organisers.

### Why it matters for quant specifically
This is the platform quant firms implicitly calibrate against. The evidence I could gather:
- A widely-circulated quant roadmap targets **CF 1700–2100+** with emphasis on DP, greedy, graphs, trees, bit manipulation. (Source is a scraped roadmap doc — **[low confidence]** on provenance, but the number matches everything else I saw.)
- **CF rating on a resume is a real signal at these firms.** Reports that a Codeforces link on a resume produced a Jane Street interview; that **red (2400+) overrides GPA/non-target school**; that Grandmasters (2600+) get fast-tracked. https://youngandcalculated.substack.com/p/how-to-get-a-quant-job-a-comprehensive — anecdotal but directionally consistent across sources.
- **Your 1600–1800 target is the right one.** It is comfortably above the LC-medium ceiling, and it is where Div-2 C/D live.

### Which ratings to actually solve
- **Difficulty ordering:** `div2A ≤ div2B << div1A < div2C < div1B << div1C << div1D`. https://codeforces.com/blog/entry/74822
- **Div 2 A averages ~1016 rating.** So A/B are warm-ups once you're near 1600; **C is your working set, D is your stretch.**
- The consensus practice rule: **solve ~200 above your current rating.** "If your rating is 1400 solve problems with 1500, 1600, 1700 rating." https://codeforces.com/blog/entry/116371 · Um_nik's version: solve problems "slightly above your level… but not too much above, because otherwise you can't solve them yet." https://codeforces.com/blog/entry/98806
- For someone *at* 1600 targeting 1800: live mostly in **1600–1800**, with a weekly stretch at 1900. A CF blog documents people at this band solving **4–5 problems/day in the 1600–1800 range.** https://codeforces.com/blog/entry/130239
- The problemset filter (by rating + tag) is the whole tool. There is also a rating-distribution-by-problem-index analysis worth a look: https://codeforces.com/blog/entry/147348

### EDU section
**https://codeforces.com/edu/courses** — the ITMO Academy pilot course. Free video lectures + graded problem steps, built by ITMO staff and students. Segment trees, two pointers, binary search, suffix structures. **This is the best free structured treatment of the "advanced but interview-adjacent" data structures anywhere**, and it's graded, so you can't fool yourself. Segment trees are borderline for a quant OA but show up in the harder ones. https://codeforces.com/blog/entry/82217

### Gym & virtual contests
- **Gym** = archived contests (ICPC regionals, university sets) you can run as a team or solo.
- **Virtual contest** = replay any past round on the original clock with a simulated leaderboard. **This is the single most useful feature on the site for OA preparation** — it reproduces the exact failure mode of a timed OA (panic, wrong ordering, no debugger, hidden tests).
- The discipline that goes with it: *"take every Codeforces contest you miss that would be rated for you as a virtual contest,"* and **"upsolve within 24 hours or you wasted the contest."** https://codeforces.com/blog/entry/116371

### Practice ladders
A2OJ ladders (100 problems each, by rating band) are the classic scaffold but the originals are 4–5 years stale. Refreshed versions exist:
- https://a2oj.online/ladder/11/ and https://earthshakira.github.io/a2oj-clientside/server/Ladders.html
- Community rebuilds: https://github.com/sanjitcodes/A2OJ-Ladder-codeforces · https://github.com/rishabhdeepsingh/A2OJ-Ladder
- 85 ladders (28 by rating, 35 by topic) generated from the live problemset: https://codeforcesladders.firebaseapp.com/

### What it isn't
- Problem statements are **deliberately obfuscated with flavour text** — the opposite of an OA prompt, which is usually blunt. Reading speed is a separate skill you'll have to build.
- **Almost no emphasis on clean code, naming, or OOP design** — which is exactly what the Optiver-style OA grades (see §5). CF makes you fast and sloppy.
- Ratings are contest-relative, so early progress is noisy and demoralising.

### Verdict
**The most important platform on this list for your specific goal, and free.** LeetCode gets you to "can implement a known pattern"; Codeforces gets you to "can invent an argument under a clock," which is the actual quant screen. Use the problemset filter at 1600–1800, do virtual contests weekly, upsolve within 24h, and work the EDU segment-tree/two-pointer courses. **10/10.**

---

## 4. CSES Problem Set

**URL:** https://cses.fi/problemset/ (by Antti Laaksonen, author of the *Competitive Programmer's Handbook*)

**Price:** free.

### What it is
The official framing: *"create a comprehensive high quality problem set for learning competitive programming… the current collection has 300 problems."* In practice the live set has grown past that — a solutions repo tracking the full set lists **400 problems** across these sections:

| Section | Problems |
|---|---|
| Introductory | 24 |
| Sorting and Searching | 35 |
| Dynamic Programming | 23 |
| Graph Algorithms | 36 |
| Range Queries | 25 |
| Tree Algorithms | 16 |
| Mathematics | 37 |
| String Algorithms | 21 |
| Geometry | 16 |
| Advanced Techniques | 25 |
| Sliding Window | 11 |
| Interactive | 6 |
| Bitwise Operations | 11 |
| Construction | 8 |
| Advanced Graph | 28 |
| Counting | 18 |
| Additional I & II | 60 |

(https://github.com/Jonathan-Uy/CSES-Solutions — 328/400 solved as of Aug 2025)

### What it's genuinely good for
- **Systematic, gap-free coverage.** Unlike CF's problemset (a firehose) or LC (interview-shaped), CSES is a *syllabus*. Finish "Dynamic Programming" and you have actually met every standard DP formulation — knapsack, coin change, edit distance, bitmask DP, digit DP — once each.
- **The DP (23) and Graph (36) sections are the best single-sitting DP/graph drills that exist for free.** This is precisely the material quant OAs draw from.
- Clean, unadorned statements. No flavour text.
- Mirrored as Codeforces gym contests (each category = one gym contest), so you can run a section under a clock. https://codeforces.com/blog/entry/87912

### What it isn't
- **No editorials, no hints, no official solutions.** You get AC/WA/TLE and nothing else. For a self-studier this is either the best feature or a wall — plan on using community solution repos (https://github.com/TamimEhsan/CSES-Solutions, https://github.com/Jonathan-Uy/CSES-Solutions) as your editorial.
- **Not rated per problem**, so you can't calibrate difficulty inside a section. The later problems in a section jump hard.
- **No interview framing whatsoever.** Nobody asks you to do this in 20 minutes while talking.
- Sections like Geometry, Interactive, and String Algorithms (suffix automata) are **irrelevant to a quant OA** — skip them.

### Verdict
**Do the DP, Graph Algorithms, Sorting & Searching, Range Queries, and Tree sections — roughly 135 problems — and skip the rest.** That's the highest-density technique coverage per hour available anywhere for free, and it plugs exactly the gap that NeetCode 150 leaves. **9/10, with the caveat that you must pair it with a solutions repo.**

---

## 5. HackerRank — the OA platform, not a study platform

**URL:** https://www.hackerrank.com

**Price:** free for candidates.

### The honest case for using it
**Familiarity with the harness is a real, non-trivial edge, and it's the only reason to be here.** Quant OAs are overwhelmingly hosted on HackerRank:

- One survey claims **HackerRank hosts 11 of 41 quant firms, CodeSignal 5, proprietary 4, take-home 3** — **[low confidence, SEO source]** https://quantvault.org/quant-oa-census-2027.html — but the direction is uncontroversial across every source I saw.
- Reported formats: **Akuna ~3 coding questions in 60–90 min** (C++ track adds ~10 MCQs); **IMC ~120 min**; **Optiver SWE ~90 min, often a single OOP/design-style question on the HackerRank *desktop* app**; **Five Rings a very short (~17 min) screen**. All **[low confidence]** — these come from `interviewfox.ai`, `prachub.com`, `linkjob.ai`, which are AI-content sites — but the *shape* (short clock, few questions, desktop-app proctoring) is consistent.

### What specifically to rehearse there
- **STDIN/STDOUT boilerplate.** HackerRank hands you raw stdin, not LeetCode's pre-parsed function signature. Fumbling `sys.stdin.readline` parsing under a 17–90 minute clock is a genuinely common way to fail. https://candidatesupport.hackerrank.com/articles/8758620864-using-stdin-for-inputs-and-stdout-for-outputs
- **I/O performance.** Reported failure mode: *"A low score almost always means hidden cases hit TLE… if your IO templates are not yet fluent, hidden cases keep hitting TLE."* Use buffered I/O by default.
- The **desktop app / proctoring** flow (Optiver) — do the official sample test once so the environment isn't new.
- Their **Interview Preparation Kit** exists and is free, but as *problems* it's weaker and staler than LeetCode/CSES.

### What it isn't
Not a place to learn algorithms. Editorials are thin, the problem quality is inconsistent, difficulty labels are unreliable, and the "1-star to 5-star" progression teaches nothing.

### Verdict
**Spend 3–5 hours here, total, and only on harness fluency.** Write and memorise a stdin-parsing + fast-I/O template in your OA language, run the official sample test, do a handful of their timed problems to feel the editor. Then leave. Practising *algorithms* on HackerRank instead of LeetCode/CF is a clear waste. **4/10 as a learning site, 8/10 as a two-evening dress rehearsal.**

---

## 6. The rest — quick verdicts

### AlgoExpert — https://www.algoexpert.io
**~$99/year, annual only (no lifetime, no monthly).** ~200 hand-picked problems with polished video explanations.
- **Genuinely good at:** production values, curation, and the **system design content**, which is the part people actually defend on Blind. https://www.teamblind.com/post/algoexpert-review-ubbww0pn
- **The problem:** NeetCode gives you the same curation with comparable-quality videos **for free**. The recurring Reddit line is that the algorithms content is "not worth the cost" and "NeetCode is way better." Per-problem cost is higher than every alternative.
- **Verdict: skip.** Zero quant relevance (no CP calibration, no probability). **3/10 for your goal.**

### Educative.io / Grokking the Coding Interview — https://www.educative.io
**~$79–80 for the course, on a subscription model** (you lose access when you stop paying).
- **Good at:** the **pattern taxonomy** — sliding window, two heaps, merge intervals, topological sort, fast/slow pointers. This is genuinely the thing NeetCode's lists *don't* teach (the "why is this a counting problem" gap). Text-based, so it's fast to skim.
- **Real criticisms:** *"the code and solutions are taken directly from LeetCode"* — you're paying for curation only; *"too superficial"*; and importantly **the platform doesn't do real runtime checking, so you can submit a suboptimal solution it accepts and LeetCode would reject.** That's a bad property for a prep tool.
- DesignGurus sells the same-lineage course as a **lifetime** purchase, which several people prefer to Educative's subscription. https://www.designgurus.io
- **Verdict: the pattern list is worth internalising; you can get it free from Sean Prashad's grouping (below). Don't subscribe.** **5/10.**

### InterviewBit — https://www.interviewbit.com
Core DSA path is **free**, structured with checkpoints and hints. It's a lead-gen funnel for Scaler's paid bootcamp.
- Decent as a *guided* path if you're rebuilding from scratch; the problem quality and discussion depth are well below LeetCode's, the archive is far smaller, and it's aimed at the Indian campus-placement market rather than quant.
- **Verdict: redundant if you have NeetCode 150 + CSES. Skip.** **4/10.**

### Codewars — https://www.codewars.com
Free (optional paid tier). Crowd-sourced "katas," community solutions not paywalled, gamified ranking.
- **Good at:** high-volume reps for **language fluency** — idioms, string handling, stdlib. Genuinely fun, low friction.
- **Bad for you:** the kata culture rewards clever one-liners and golf over clear O(n log n) reasoning; difficulty ("kyu") is community-voted and noisy; there is essentially no complexity-analysis pressure and no timed-contest mode. It will not move a CF rating.
- **Verdict: recreational. Not prep.** **3/10 for quant OA.**

### Exercism — https://exercism.org
**Free forever, open source, non-profit.** ~83 language tracks, 8,100+ exercises, automated analysis, and **free volunteer human mentorship** giving you idiomatic code review.
- **Good at exactly one thing you might need: learning a new language properly.** If your OA is in C++ and you're a Python native, an Exercism C++ track is the single best free way to become idiomatic.
- **Not an algorithms platform.** Exercises are language-teaching, not complexity-teaching. No contests, no ratings.
- **Verdict: use it only if you have a language gap. Otherwise irrelevant.** **7/10 for its actual purpose, 2/10 for DSA.**

### AtCoder — https://atcoder.jp
Free. Japanese; contests fully translated to English.
- **ABC (AtCoder Beginner Contest)** runs weekly, 8 problems, and the **D/E/F range maps closely onto CF 1400–1900**. Problem statements are **short, precise, and free of flavour text** — much closer to an OA prompt than Codeforces is.
- **Better editorials than Codeforces**, and the tasks are more "clean insight," less "implementation slog."
- Downside: fewer contests per week than CF, contests run at awkward hours for US/EU (typically 21:00 JST), and the rating is on its own scale so it doesn't directly serve the "CF 1600–1800" number if that's the literal target.
- The standard advice is **pick one platform and stay on it** rather than splitting. https://codeforces.com/blog/entry/79310
- **Verdict: an excellent CF substitute or supplement. Use ABC D/E as *virtual* contests for timed practice even if you never do them live.** **8.5/10.**

### Project Euler — https://projecteuler.net
Free, 900+ problems.
- **It's a number-theory and math-insight site, not a DSA site.** The community view is that it's *"more about math"* and that many problems are unpleasant to implement even for experienced competitive programmers. Problems get to the point where math PhDs struggle.
- **Small but real quant angle:** the early 100 problems exercise the modular-arithmetic / combinatorics / brute-force-then-optimise muscle that quant *math* screens use. That's a different interview than the coding OA.
- **Verdict: not prep for a coding OA. Marginally useful as math warm-up. Don't spend a month here.** **3/10 for DSA, 5/10 for the quant math screen.**

### Advent of Code — https://adventofcode.com
Free, annual (December), 25 days × 2 parts.
- **Good at:** input parsing under time pressure (every puzzle starts with a messy text blob — very OA-like), grid/graph intuition, and the **part-2-is-a-refactor-of-part-1** structure, which one writer argues is a *better* interview format than LeetCode. https://blog.devcrisis.com/software-atoms/interviews-should-copy-advent-of-code
- **Bad at:** it's not algorithmically calibrated — days 1–10 are trivial, days 20–25 are idiosyncratic puzzles that reward pre-built utility libraries. Time cost is high relative to signal, and people with template repos have a large unearned advantage.
- **Verdict: fun, mildly useful for parsing speed, wrong tool for a rating target.** **4/10.**

### Grind 75 — https://www.techinterviewhandbook.org/grind75/
**Free.** By **Yangshun Tay** (ex-Meta Staff Engineer) — **the author of Blind 75 itself**, explicitly built as "Blind 75 2.0."
- **The fix over Blind 75:** Blind 75 is static, unprioritised and unpersonalised. Grind 75 **generates a schedule from your available hours/weeks**, ranks by priority, and balances breadth vs depth. Progress tracking built in.
- Sits inside the **Tech Interview Handbook** (142.5k GitHub stars — https://github.com/yangshun/tech-interview-handbook), which also gives you free **algorithm cheatsheets by topic** and coding best-practice guides. The handbook's own advice: **~3 months at 2–3 hrs/day** for a holistic prep. https://www.techinterviewhandbook.org/coding-interview-study-plan/
- **Verdict: the best free *scheduler*. Use it to plan, use NeetCode 150 to study. Highest-credibility free resource in the interview-prep category.** **9/10.**

### Sean Prashad's LeetCode Patterns — https://seanprashad.com/leetcode-patterns/
**Free, open source** (13.7k stars — https://github.com/seanprashad/leetcode-patterns).
- Problems **grouped by pattern/subtopic** with a searchable, filterable table (by company, difficulty, pattern) and completion tracking. Java solutions on a branch.
- This is the **free substitute for Grokking the Coding Interview's taxonomy** — you get the pattern grouping without the $80.
- Caveat: some listed problems are LeetCode-Premium-locked.
- **Verdict: use it as your pattern index alongside NeetCode 150.** **8/10.**

### Structy — https://www.structy.net (Alvin Zablan)
**~$30/month, ~$51–60/year; ~25% of the course free to try.**
- **Genuinely the best "I don't actually understand recursion" resource.** Strong sense of progression, endpoint that actually exists, and the most consistently praised explanations of any paid DSA course ("your explanations are the best"). It's cheap, it's finite, and it's honest about being beginner-to-intermediate.
- **But:** it stops well short of where you need to be. Nothing here touches CF-1600 material.
- **Verdict: worth the ~$51 *only* if you have a genuine foundations gap (recursion, trees, DP base cases). If you're already at LC-medium, skip it entirely.** **8/10 as a foundations course, 2/10 as quant prep.**

### Algorithms — Jeff Erickson (free book) — https://jeffe.cs.illinois.edu/teaching/algorithms/
**Free PDF** (also in print, ~$25; mirror: https://archive.org/details/Algorithms-Jeff-Erickson, GitHub copy: https://github.com/mleoking/LeoReference)
- Covers recursion, backtracking, **dynamic programming (the best DP chapter in any textbook — full stop)**, greedy, graphs, DFS, MST, shortest paths, APSP, max-flow/min-cut, NP-hardness.
- **Why practitioners rate it over CLRS:** it *"emphasises intuition and the problem-solving process"* rather than proof-first formalism. Reviewers: *"clearer and better written than any other algorithm book out there."* Hundreds of battle-tested exercises. Grew out of UIUC lecture notes.
- Prerequisites: discrete math (esp. induction) and basic DS/algos.
- **Verdict: read the recursion + backtracking + dynamic programming chapters. That's maybe 150 pages and it will do more for your CF 1600→1800 push than 100 extra LeetCode problems.** **9.5/10.**

### VisuAlgo — https://visualgo.net
**Free** (by Steven Halim, NUS — author of *Competitive Programming*).
- Step-through animations of every standard DS/algo, and crucially **you can feed it your own input** rather than only canned examples. Peer-reviewed academic pedigree.
- **It's a debugging aid, not a curriculum** — "best used alongside course materials."
- **Verdict: 20 minutes when segment trees / Fenwick / union-find / Dijkstra's relaxation order won't click. Not a study plan.** **7/10 as a targeted tool.**

### USACO Guide — https://usaco.guide
**Free**, CC-BY-NC-SA, run by the Competitive Programming Initiative (joincpi.org), authored by top USACO finalists incl. Benq. https://github.com/cpinitiative/usaco-guide
- **The best free structured CP curriculum in English.** Bronze → Platinum, each module = curated external resources + a graded problem list, in C++/Java/Python.
- **Explicitly usable if you don't do USACO**: *"feel free to use this guide even if you don't do USACO, and you will still learn a lot."* Suggested load 5–10 hrs/week.
- **For you: the Gold and Platinum modules are the right target.** Gold ≈ CF 1500–1900 and covers exactly your gap — DP on trees, shortest paths, DSU, prefix sums, binary search on answer.
- **Verdict: the best free *syllabus* for the CP half of your prep. Use it to decide what to learn; use CSES/CF to practise it.** **9/10.**

### Quant-specific: QuantGuide — https://www.quantguide.io
**~$35/mo, ~$20/mo billed annually; generous free tier** (non-premium questions, analytics, mental-math simulator).
- 1,000+ real quant interview questions with hints, full solutions, company tagging, and a **mental-math simulator**.
- **Honest limitation: "coding coverage is lighter"** — its strength is probability, brainteasers, and market-making, not DSA.
- Worth flagging because **this is the actual gap most CS-background candidates have.** As one summary put it: coming from CS you *"can't just leetcode your way through quant interviews."* A first-hand Optiver-internship prep log confirms it — the resource list is Zetamac, quantguide, Xinfeng Zhou's green book, Jane Street's probability guide, Jane Street puzzles, Putnam — **and almost no DSA sites at all.** https://github.com/Aniruddha-Deb/quant-prep
- **Verdict: not a DSA site, but if you're optimising for a quant offer rather than for a DSA rating, the marginal hour here probably beats the marginal LeetCode problem.** **8/10 for its lane.**

---

## 7. How to actually use these — the methodology people agree on

### The 30-minute rule (really 30–45)
Standard practice: **attempt independently, then take a hint or partial solution at 30–45 minutes.** Sitting on a problem for 3 hours feels virtuous and teaches almost nothing per unit time; looking at 10 minutes is worse. Um_nik's framing is the useful one: **you must work in the band of problems you *don't* know how to solve but *could* invent** — too far above and the time is wasted.

For CP specifically the threshold is tighter: **upsolve within 24 hours or you wasted the contest.** https://codeforces.com/blog/entry/116371

### Redoing problems / spaced repetition
This is the highest-leverage habit and the most under-practised.
- The core insight: *"If you only solve a problem once, you'll never practise recalling the details of the solution from memory, which means you probably won't remember how to solve it."* https://www.redgreencode.com/leetcode-tip-10-planning-a-spaced-repetition-schedule/
- And: *"If you stare at a solution for 10 minutes, then put it away and start typing it into LeetCode, you still probably won't be able to recall the full solution from memory"* — you must reconstruct it from understanding, which is the point.
- The 80/20 approach: **shrink to a core set of problems, then use spaced repetition to shrink that set until you permanently know it.** Alex Bowe's "Effective LeetCode" is the canonical writeup. https://www.linkedin.com/posts/alexbowe_effective-leetcode-the-8020-guide-to-using-activity-7049833400114839553-9czS
- **Realistic cadence:** unlike vocabulary cards, a LeetCode problem is a 20–40 minute review. You can do **2–4 reviews/day**, not 50. Intervals in the days-to-weeks range. https://www.redgreencode.com/leetcode-tip-13-spaced-repetition-interval-lengths/
- Tooling if you want it: https://leetrepeat.com/ · https://www.leetcycle.com/ (both third-party; neither is necessary — a spreadsheet with `problem, last_solved, next_due, confidence` works.)

### Timed practice — the part most people skip
For a quant OA with a 17–90 minute clock, **untimed practice is training the wrong skill.** Concretely:
- **Codeforces virtual contests** are the best free simulator. Replay a Div 2 on the original clock.
- **AtCoder ABC** as a virtual, D/E/F only, 70 minutes.
- **Do at least a few sessions in the actual OA harness** (HackerRank, stdin parsing, no debugger, hidden tests).
- The recurring quant-OA advice: *"prep that drills recurring patterns under strict time limits beats grinding sheer problem volume."*

### How many problems is enough — the only real data I found
From **interviewing.io's study** (~700 surveyed users cross-referenced against 100,000+ technical interviews — the single best-powered dataset on this question). https://interviewing.io/blog/how-well-do-leetcode-ratings-predict-interview-performance · summary mirror: https://www.mikemroczka.com/blog/how-well-do-leetcode-ratings-predict-interview-performance-heres-the-data

- **Correlation of problem count with interview performance: 0.27.** With merely *working at a FAANG*: **0.17.** Both are weak-to-moderate. Problem count is a *real* but *modest* predictor.
- **Difficulty dominates volume:** **50 Mediums ≈ +3 percentage points** on interview score; **50 Hards ≈ +7 points.** Roughly **2.3× the return per problem for Hards.**
- **~65% of FAANG engineers have done fewer than 350 problems; ~55% fewer than 300.**
- **Going from 350 → 800 problems moves you from the 65th to the 85th percentile.** More than doubling your effort for 20 points. **Diminishing returns are severe past ~350–500.**
- Reported ranges for people with offers span **150 to 1,400** — one person converted two top-tier offers in six weeks on 150 problems; another was at 1,400 without a phone screen.

**The synthesis:** **~300 well-chosen problems, redone until automatic, with a Medium/Hard skew, beats 800 done once.** The most-quoted version: *"If you actually learn the 10 core patterns, you don't need to do 400 problems. You're just re-solving the same 10 algorithms with different problem statements."* Counting problems solved is the classic failure mode — the metric that feels like progress and isn't.

---

## 8. Recommended stack for your exact goal

| Purpose | Tool | Cost |
|---|---|---|
| Pattern spine (LC-medium) | **NeetCode 150** (free lists + free videos) | $0 |
| Schedule / prioritisation | **Grind 75** | $0 |
| Pattern taxonomy index | **Sean Prashad's LeetCode Patterns** | $0 |
| Systematic technique coverage | **CSES** — DP, Graphs, Sorting/Searching, Range Queries, Trees (~135 problems) | $0 |
| Calibration to 1600–1800 | **Codeforces** problemset filtered 1600–1800 + weekly **virtual contest** + **EDU** | $0 |
| Alternative/supplement calibration | **AtCoder ABC** D/E/F as virtuals | $0 |
| Theory where you're stuck | **Erickson** (recursion/backtracking/DP chapters), **USACO Guide** Gold/Platinum, **VisuAlgo** | $0 |
| OA harness rehearsal | **HackerRank** — stdin template + sample test, ~4 hours total | $0 |
| Volume + company targeting | **LeetCode**, free tier; **one month** of Premium in the final sprint | $0 → ~$35 |
| The gap you'll actually fail on | **QuantGuide** free tier + Zetamac + Xinfeng Zhou (probability/mental math) | $0 → ~$20/mo |

**Total defensible spend: ~$35–75.** Everything else on this page — AlgoExpert ($99/yr), Educative ($80), NeetCode Pro ($119–219), Structy ($51), InterviewBit/Scaler — is optional convenience, and the free alternatives above are at least as good for this specific target.

**The one thing I'd emphasise:** for quant firms the coding OA is usually the *filter*, not the *differentiator*. The prep logs of people who actually got quant offers are dominated by probability, EV, mental math, and market-making — not by DSA sites. Get to CF-1700-comfortable, then move your marginal hour to the math.

---

## Full source list

**Fetched directly (GitHub only — everything else was blocked):**
- https://github.com/seanprashad/leetcode-patterns
- https://github.com/yangshun/tech-interview-handbook
- https://github.com/snehasishroy/leetcode-companywise-interview-questions
- https://github.com/Jonathan-Uy/CSES-Solutions
- https://github.com/cpinitiative/usaco-guide
- https://github.com/Aniruddha-Deb/quant-prep
- https://github.com/cybergeekgyan/Quant-Developers-Resources
- https://github.com/mleoking/LeoReference (Erickson PDF mirror)

**Via search-result summaries only (pages blocked):**
- https://interviewing.io/blog/how-well-do-leetcode-ratings-predict-interview-performance
- https://www.mikemroczka.com/blog/how-well-do-leetcode-ratings-predict-interview-performance-heres-the-data
- https://codeforces.com/blog/entry/116371 (how to practise CP)
- https://codeforces.com/blog/entry/98806 (Um_nik on practice)
- https://codeforces.com/blog/entry/130239 (1600–1800 grind)
- https://codeforces.com/blog/entry/147348 (Div 2 problem-rating analysis)
- https://codeforces.com/blog/entry/74822 (Div1/Div2 difficulty ordering)
- https://codeforces.com/blog/entry/87912 (CSES on Codeforces gym)
- https://codeforces.com/blog/entry/82217 · https://codeforces.com/edu/courses (ITMO EDU)
- https://codeforces.com/blog/entry/79310 (AtCoder ABC)
- https://codeforces.com/blog/entry/80438 (USACO Guide announcement)
- https://cses.fi/problemset/
- https://www.techinterviewhandbook.org/grind75/about · /coding-interview-study-plan/
- https://www.redgreencode.com/leetcode-tip-10-planning-a-spaced-repetition-schedule/ · /leetcode-tip-13-spaced-repetition-interval-lengths/
- https://www.linkedin.com/posts/alexbowe_effective-leetcode-the-8020-guide-to-using-activity-7049833400114839553-9czS
- https://blog.samarthgoel.com/quant-interview/ (first-hand quant prep; recommends Grind 75 as the LC benchmark)
- https://blog.devcrisis.com/software-atoms/interviews-should-copy-advent-of-code
- https://leetcode.com/discuss/post/468851/ (contest rating algorithm)
- https://leetcode.com/discuss/explore/recursion-ii/2674461/... (Explore card criticism)
- https://www.jointaro.com/question/bC78DsNeHfidfH303yW7/best-leetcode-premium-filters-for-company-questions/
- https://www.quora.com/Do-the-Project-Euler-problems-predominantly-test-Mathematics-knowledge-or-coding-skills
- https://www.wallstreetoasis.com/forum/trading/request-leetcode-resources-prep-advice-for-quant-trading
- https://quantnet.com/threads/prepare-for-quant-interviews-coding-wise.53521/
- Blind threads (all blocked, summaries only): teamblind.com posts on LeetCode Premium, NeetCode Pro, AlgoExpert, Grokking, "what's the meta in 2025/2026", Jane Street SWE prep.

**Low-confidence / likely SEO or AI-generated — used only for price points and OA formats, flagged inline:**
- https://prachub.com/... · https://quantvault.org/... · https://www.codeintuition.io/... · https://www.lodely.com/... · https://leetcopilot.dev/... · https://interviewfox.ai/... · https://www.linkjob.ai/... · https://toolradar.com/... · https://algocademy.com/... · https://crackr.dev/... · https://www.designgurus.io/blog/is-leetcode-premium-worth-it (vendor) · https://www.educative.io/blog/... (vendor)

**Not reachable at all:** reddit.com (r/leetcode, r/cscareerquestions, r/quant, r/csMajors), news.ycombinator.com, teamblind.com, codeforces.com, leetcode.com, interviewing.io, cses.fi, usaco.guide, techinterviewhandbook.org, exercism.org, structy.net, medium.com, substack.com, dev.to.
