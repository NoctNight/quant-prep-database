# Quant Coding Rounds

What the coding rounds actually ask at 37 quant trading firms, and the most
time-efficient way to prepare for them. Every claim is linked to the report it
came from, tagged by role (developer / trader / researcher) and by track
(internship / full-time).

Compiled September 2026 from 13 parallel research passes.

## Contents

| Path | What it is |
|---|---|
| `dashboard/index.html` | The filterable dashboard. Open it in a browser — it is a single self-contained file, no build step. |
| `data/data.json` | The dataset: 37 firm profiles, 198 reported questions, the prep syllabus. |
| `research/` | The 13 raw research reports the dataset was distilled from, with source URLs throughout. |

## The dataset

- **198 reported questions** across **37 firms**, each with a source link.
- Evidence tiers: 6 official (firm's own page), 107 first-hand, 56 first-hand
  transcribed via a mirror, 27 aggregator, 2 prep-company.
- 110 carry a date; 89 are 2023 or newer.
- Split by track: 66 internship, 146 full-time (14 apply to both).
- Split by role: 142 developer, 42 researcher, 14 trader.

Topic distribution across all 198:

| Topic | Count |
|---|---|
| Design / OOP simulation | 38 |
| Arrays / strings / hashing | 34 |
| Low-level / systems / C++ | 30 |
| Probability → code | 31 |
| Take-home | 20 |
| Data / pandas / SQL | 13 |
| Graphs / trees | 9 |
| Recursion / DP | 9 |
| Math puzzles | 8 |
| Debug others' code | 6 |

## Engineering vs research vs trading

These are different hiring processes that happen to share a firm name. The
dashboard treats the role as a top-level mode rather than a filter, and each
firm profile shows its three loops separately.

- **Software engineering / quant dev** (142 questions, 32 firms) — the hardest
  coding bar plus systems depth. C++ object model, memory, concurrency.
- **Quant research** (42 questions, 31 firms) — a real coding gate plus
  statistics translated into code: regression, interpolation, Monte Carlo.
  Full-time loops are decided by take-homes.
- **Quant trading** (14 questions, 14 firms) — often no coding whatever. Jane
  Street, SIG, Optiver and IMC test none for trader candidates; probability,
  mental arithmetic and market-making games decide the outcome.

Where a firm has no reported evidence for a role, the profile says so rather
than guessing.

## Findings

### What works

1. **Class design and simulation from a loose spec.** The largest single
   category and the most under-prepared. Jane Street's entire loop is built on
   it — Tetris, Connect Four on an infinite board, a stack machine. Optiver's
   online assessments are long story-specs with starter classes where scope
   management, not algorithms, is the difficulty.
2. **Build the domain objects once.** An order book with O(1) cancel, a matching
   engine with price-time priority, an LRU cache, a ring buffer, `std::vector`
   from scratch. These are not analogies for interview questions — IMC's onsite
   is "always" a matching engine, HRT publishes its own book-builder exercise,
   and SIG asks for `std::vector` verbatim.
3. **Roughly 150–250 timed problems from one curated list.** Offer-holders
   converge on this figure. Returns collapse beyond it.
4. **For developer roles, treat C++ and OS internals as recall.** XTX asks about
   20 such questions in a 30-minute voice call with no time to think.
5. **Rehearse escalation, not just solutions.** The dominant format is one
   problem extended two or three times. Practise the second and third step.

### What doesn't

- **Grinding 500+ LeetCode problems.** No first-hand account credits raw volume.
- **Competitive programming to a high rating.** Prep sites claim 2400+
  Codeforces is needed. Tower's own intern assessment is calibrated at CF
  1600–1800, and every first-person report agrees. The prep sites are wrong.
- **Learning OCaml for Jane Street.** Officially counterproductive: *"We don't
  award bonus points for using a functional language like OCaml. Please don't
  use OCaml just because you think it will make us happy."*
- **Segment trees and advanced graph theory.** Absent from every first-hand live
  round in the dataset.
- **Brainteaser collections instead of writing code.** Traders need probability;
  developers and researchers need working code.

### The thing most candidates get wrong

Passing the tests is not passing the round. An IMC candidate passed 44 of 44
unit tests and was rejected for not following the interviewer's intended
approach. Optiver progressed a 77.8% submission and rejected a 90% one.
G-Research rejected a candidate who passed every test case. Code quality is
scored, not assumed.

### How candidates actually get cut

Most rejections in this dataset are not "couldn't solve it":

- Correct but slow (HRT rejects solutions that time out; Citadel gives no
  partial credit for TLE).
- Missing one edge case (a Citadel Securities senior SWE missed self-loops in a
  currency-graph problem).
- Over-explaining and never reaching the final step of a multi-part question.
- Freezing when requirements shift mid-problem.
- Shallow C++ or OS answers when C++ is on the résumé.
- In take-homes: univariate analysis, or presenting in-sample results without
  caveats.

## Role and track differences

- **Traders** often face no coding at all. Optiver, SIG and IMC do not test code
  for trader interns. Every first-hand trader rejection here was attributed to
  probability or mental arithmetic.
- **Researchers** get a genuine coding gate plus statistics-to-code work:
  regression, interpolation, Monte Carlo, backtests. Full-time loops are decided
  by take-homes; internship loops substitute a live DSA round.
- **Developers** get the hardest coding bar plus systems depth. Internship loops
  are online-assessment-gated and DSA-pure; experienced loops have fewer
  assessments, more C++, concurrency, debugging and design.

## Caveats

Research ran behind a proxy that blocked Glassdoor, Reddit, Blind, LeetCode and
1point3acres, so many rows come from search summaries or from GitHub mirrors
that preserve the original URL. Nothing here is invented, and every row carries
an evidence mark. Two firms are notably thin:

- **TGS Management** — two verbatim questions on record, one from 2014. Treat
  any confident guide about TGS with suspicion.
- **Quadrature Capital** — candidates cite an NDA; expect to be surprised by
  format.

Open the source before relying on any single row.

## Deploying the dashboard

The dashboard is one self-contained HTML file with no build step, so any static
host will serve it. `vercel.json` is already configured to serve the `dashboard/`
directory as the site root.

To put it on Vercel:

1. Go to [vercel.com/new](https://vercel.com/new) and sign in with GitHub.
2. Import `quant-prep-database`. Vercel will need permission to read it, since
   the repository is private.
3. Leave every build setting untouched — `vercel.json` already sets the output
   directory and disables the framework preset. Do not set a build command.
4. Deploy. You get `<project-name>.vercel.app` for free, and every push to
   `main` redeploys automatically.

**A deployed URL is readable by anyone who has it.** A private repository does
not make the deployment private; Vercel only offers password protection on paid
plans. `vercel.json` sends `X-Robots-Tag: noindex, nofollow` so search engines
skip it, which is not access control — it just keeps the page out of results.
Delete the `headers` block if you would rather it be indexed.
