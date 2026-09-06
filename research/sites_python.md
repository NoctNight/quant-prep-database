# Websites & Platforms for Quant-Grade Python, NumPy, pandas and SQL

Research date: 2026-09-06. Target level: quant researcher — vectorised thinking, fast/correct data manipulation, analytical SQL.

---

## 0. Methodology and its limits — read this first

**Sandbox restriction (important caveat on this whole document).** This session's network egress is restricted by organisation policy to a small allowlist. Concretely:

- `reddit.com` / `old.reddit.com` — **blocked** (both the HTML site and the `.json` endpoints).
- `news.ycombinator.com` and `hn.algolia.com` — **blocked** (the HN Algolia search API returns `CONNECT tunnel failed, 403`).
- Direct page fetches to `realpython.com`, `numpy.org`, `pandas.pydata.org`, `pgexercises.com`, `datalemur.com`, `stratascratch.com`, `selectstarsql.com`, `wesmckinney.com`, `labri.fr`, `kaggle.com`, etc. — **all blocked**.
- Working: the **web search tool** (returns engine-generated summaries plus result URLs), **`raw.githubusercontent.com`** via curl, and the **GitHub search API** for repository metadata.

So: repo-level facts below (stars, last-push dates, licences, README text) are **directly verified**. Everything else comes from search-engine summaries of the target pages, which quote the pages but which I could not open myself. **Prices in particular should be re-checked on the vendor page before you pay anything** — several were reported inconsistently across sources, and I flag those inline.

**Bias warning on the SQL sources.** A large share of "best SQL practice site" pages that surface in search are written *by competing SQL products*: `sqlquest.app`, `sqlmarrow.com`, `builder.ai2sql.io`, `tutorials-db.com`, plus the `datalemur.com/blog/datalemur-vs-stratascratch` post (DataLemur reviewing its own competitor). Their factual claims (e.g. "SQLBolt hasn't been updated since 2018") are plausible and mutually corroborating, but they are marketing. I mark those claims as *unverified-competitor-sourced*.

**Content-farm flags (avoid as primary sources).** GeeksforGeeks, W3Schools, TutorialsPoint, JavaTpoint, Simplilearn, most `medium.com` "Top N profilers / Top N pandas tricks" posts, `daily.dev`, `techjury.net`, `index.dev`, `tech-insider.org`, `alternativeto.net`, `saashub.com`, `classcentral.com` roundups. The documented complaints are consistent: uneven, community-dumped content, occasional outright errors presented next to correct material, and heavy ad load — which is exactly the failure mode you cannot afford while learning something as trap-laden as pandas indexing. Source: [HN discussion on GfG/W3Schools quality](https://news.ycombinator.com/item?id=44595411), [comparison writeups](https://www.saashub.com/compare-w3schools-vs-geeksforgeeks).

---

## 1. Python fluency

The quant-relevant target here is not "can write a for loop" — it's *knowing which construct is cheap*, comfort with iterators/generators/comprehensions, `__array__`-style protocols, and enough profiling instinct to know when you have written accidentally-quadratic code.

### Real Python — https://realpython.com/
- **Good for:** the single best-organised free tutorial archive in the Python world. Deep, well-edited articles on specific topics (descriptors, `asyncio`, `itertools`, memory model, dict internals). Excellent as a *lookup* resource: when you hit "how does `functools.cache` actually behave", their page is usually the best free write-up.
- **Free vs paid:** hybrid. A very large fraction of written tutorials is free and ad-light. Video courses, quizzes, learning paths and exercises are behind a membership ([join page](https://realpython.com/account/join/)); annual billing is discounted vs monthly ([support article](https://support.realpython.com/article/10-is-there-a-discount-for-the-membership)).
- **Price:** *could not verify*. Search results surfaced a [python.org discussion thread](https://discuss.python.org/t/unclear-about-real-python-subscription/105143) where a claim of "$49/month / $599/year" was explicitly denied as wrong, without stating the real figure. Check the join page yourself. Historically it has been in the ~$20–30/month band.
- **Verdict:** **Use the free articles heavily; you almost certainly do not need the membership.** Not a structured curriculum — it's an encyclopaedia. Zero content-farm risk; editorial quality is genuinely high.

### The official Python tutorial — https://docs.python.org/3/tutorial/
- **Good for:** correctness. It is the authoritative statement of language semantics, and its stdlib tour (`itertools`, `collections`, `functools`, `dataclasses`) is exactly the vocabulary that separates fluent Python from translated-MATLAB.
- **Free:** yes, entirely.
- **Honest caveat, from the docs themselves:** it is aimed at *programmers new to Python*, not people new to programming, and it explicitly "does not attempt to be comprehensive". If you already code, this is a weekend read. If Python is your first language, it will feel arid.
- **Verdict:** **Read it once, cover to cover, early.** Then keep the [Library Reference](https://docs.python.org/3/library/) open forever. Free, canonical, no substitute.

### Fluent Python (Luciano Ramalho) + https://www.fluentpython.com/
- **Good for:** the "why" layer — data model, sequences, dunder protocols, iterators/generators, concurrency. This is the book that turns a competent user into someone who can read library source.
- **Free vs paid:** the book is paid (O'Reilly, 2nd ed. 2022). **The companion site is free** and is more than a stub: it hosts sections and chapters cut from the 2nd edition to keep the print book "luggable", collected at [fluentpython.com/extra](https://www.fluentpython.com/extra/). Code is free and open: [github.com/fluentpython/example-code-2e](https://github.com/fluentpython/example-code-2e); the site itself is open-sourced at [fluentpython/book-site](https://github.com/fluentpython/book-site).
- **Verdict:** **The best single Python book for this purpose, and the companion site is a legitimately good free resource in its own right.** Buy the book if you can; the free extras are worth reading regardless.

### Exercism — Python track — https://exercism.org/tracks/python
- **Good for:** the one thing almost nothing else free offers — **human code review**. You submit a working solution and a volunteer mentor tells you it isn't idiomatic. Track structure: ~146 exercises across ~17 concepts, split into "concept" exercises (language building blocks in prerequisite order) and "practice" exercises (canonical algorithmic problems).
- **Free:** **100% free, permanently, by policy.** Exercism is a not-for-profit funded by donations and grants ([about](https://exercism.org/about), [supporters](https://exercism.org/about/supporters/organisations)). ~80+ language tracks.
- **Verdict:** **Highest free-value item in this entire section.** Do the concept track, then submit 10–15 practice exercises for mentoring specifically to get told your loops should have been comprehensions. Weakness: exercises are algorithmic toys, not data work — it builds language fluency, not vectorised thinking.

### Effective Python (Brett Slatkin) — https://effectivepython.com/
- **Good for:** 125 short, self-contained "items" of the form *here is the wrong way, here is why, here is the right way*. Now in its 3rd edition. Extremely high signal-per-page for someone who already writes Python and wants to stop writing bad Python.
- **Free vs paid:** book is paid. The site publishes the **full item list free** (useful as a self-audit checklist) and all code snippets are free on GitHub.
- **Verdict:** **Buy it, or at minimum read the free item list and look up the ~20 you can't already explain.** Complements Fluent Python: Slatkin = practice rules, Ramalho = mental model.

### Python Morsels (Trey Hunner) — https://www.pythonmorsels.com/
- **Good for:** deliberate practice on small, sharply-designed exercises with multiple graded solutions and screencast walkthroughs. 279 exercises across five skill levels, each with hints, automated tests and a walkthrough of *different* solutions ([pricing page](https://www.pythonmorsels.com/pricing/)).
- **Price:** **~$240/year**; ~$87 for 3 months; a lifetime tier appears in Black Friday sales at ~$600 ([2025 sale post](https://treyhunner.com/2025/11/lifetime-access-sale-2025/)). **Free tier:** first 3 exercises plus dozens of screencasts.
- **Verdict:** **Genuinely good, but hard to justify at $240/yr when Exercism is free and gives you a human mentor.** Trey Hunner's teaching is excellent and the "here are four solutions, here's the tradeoff" format is rarer than it should be. If money is not the constraint and you learn well from drills, it's the best paid Python-practice product. Otherwise: skip, use his [free blog](https://treyhunner.com/) which contains a lot of the same thinking.

### Talk Python (podcast + training) — https://talkpython.fm/ , https://training.talkpython.fm/
- **Podcast:** free, weekly, broad ecosystem coverage. **Good for:** ambient awareness of what tooling exists — you learn that Polars/DuckDB/`uv`/`ruff` exist and roughly why. **Not** good for skill-building; you cannot learn vectorisation by listening.
- **Training:** 286+ hours of courses, **$19–$49 per course, buy-once-own-forever, no subscription** ([pricing](https://training.talkpython.fm/policies/pricing)). Mobile apps free.
- **Verdict:** **Podcast: free, worth having on in the background, low priority.** Courses: honestly-priced and competent, but nothing here is quant-specific and the free written resources above cover the same ground better for a reader.

**Python section ranking (free-first):** official tutorial → Exercism (with mentoring) → Real Python free articles → Fluent Python free extras → *then* consider buying Fluent Python / Effective Python.

---

## 2. NumPy — the vectorisation layer

This is the section that matters most for a quant researcher, and the free material here is unusually strong.

### Official NumPy documentation — https://numpy.org/doc/stable/
Key pages:
- [NumPy quickstart](https://numpy.org/doc/stable/user/quickstart.html)
- [NumPy: the absolute basics for beginners](https://numpy.org/doc/stable/user/absolute_beginners.html)
- **[Broadcasting](https://numpy.org/doc/stable/user/basics.broadcasting.html) — read this until you can predict shapes in your head.** The docs state the point directly: broadcasting "provides a means of vectorizing array operations so that looping occurs in C instead of Python … without making needless copies of data."
- [Indexing on ndarrays](https://numpy.org/doc/stable/user/basics.indexing.html) and [Copies and views](https://numpy.org/doc/stable/user/basics.copies.html) — the two pages that prevent the most common silent bugs.
- **Free.** **Verdict: the broadcasting + indexing + copies/views trio is mandatory reading and is the highest-value free NumPy content that exists.** The docs are weaker as a *narrative* teacher; pair them with Rougier below.

### "From Python to NumPy" — Nicolas P. Rougier
- Site: http://www.labri.fr/perso/nrougier/from-python-to-numpy/ · Source: https://github.com/rougier/from-python-to-numpy
- **Verified repo facts:** open-access book, 2017, licence CC-BY-NC-SA (`NOASSERTION`/other in GitHub metadata), 2,149 stars, repo last pushed 2025-05-06. Topics tagged: `book`, `numpy`, `vectorization`, `open-access`.
- **Good for:** *exactly the thing you asked about.* The book is organised around vectorisation as a way of thinking, with three named categories — **code vectorisation**, **problem vectorisation**, and **custom vectorisation** (structured/record arrays, ufuncs) — worked through real examples (Game of Life, particle systems, Mandelbrot, boids, fractals, artificial neural nets). It is the only free text I found that treats "reformulate the *problem* so it is vectorisable" as a teachable skill rather than a talent.
- **Free:** yes, fully, in HTML/PDF/EPUB.
- **Honest caveat:** it's a 2017 book. The NumPy API it uses is essentially unchanged and the ideas are timeless, but it predates NumPy 2.0 and won't mention modern alternatives (Numba, `np.einsum` tricks are light, no NumPy-2 `copy` semantics).
- **Verdict: the single best free resource on this list for "vectorised thinking". Do it after the official broadcasting docs.**

### numpy-100 (100 NumPy exercises) — https://github.com/rougier/numpy-100
- **Verified repo facts:** MIT licence, **14,426 stars**, **last pushed 2026-08-26** — actively maintained. Ships as `.md` and `.ipynb` (with and without solutions) plus a Binder launcher.
- **Good for:** drilling. Assembled from the NumPy mailing list, Stack Overflow and the docs, graded roughly easy→hard. Doing all 100 without looking is a decent proxy for "I can express this without a loop."
- **Free.** **Verdict: do this. It is short, free, active, and directly builds the reflex.** Weakness: exercises are atomic puzzles, so they build *code* vectorisation but not *problem* vectorisation — which is why you also read Rougier's book.

### Scientific Python Lectures (formerly "Scipy Lecture Notes") — https://lectures.scientific-python.org/
- **Note the URL change.** The old `scipy-lectures.org` is legacy; the maintained home is `lectures.scientific-python.org`, repo at [scipy-lectures/scientific-python-lectures](https://github.com/scipy-lectures/scientific-python-lectures). Last tagged stable release 2024.1 (April 2024) with 2025.x in development — so: maintained, but slowly.
- **Good for:** the **[Advanced NumPy](https://lectures.scientific-python.org/advanced/advanced_numpy/index.html)** chapter, which is the best free explanation of *why* NumPy is fast — memory layout, strides, dtypes, views vs copies, and writing your own ufuncs. Also good: the [SciPy chapter](https://lectures.scientific-python.org/intro/scipy/index.html) (optimisation, interpolation, linalg, stats) and [optimizing code](https://lectures.scientific-python.org/advanced/optimizing/index.html).
- **Free** (CC-BY). **Verdict: skip the beginner half; the Advanced NumPy strides/memory chapter is a genuine gem and is what will let you reason about performance instead of guessing.**

**NumPy path:** official broadcasting/indexing/views docs → Rougier's *From Python to NumPy* → numpy-100 for drills → Scientific Python Lectures "Advanced NumPy" for the memory model.

---

## 3. pandas

### Official pandas docs — https://pandas.pydata.org/docs/
- [10 minutes to pandas](https://pandas.pydata.org/docs/user_guide/10min.html) — the official on-ramp. **Honest verdict: it is a tour, not a tutorial.** It shows you that operations exist; it does not build a model of how indexing/alignment works, which is where every pandas bug lives. Useful for one hour on day one, then discard.
- **[The User Guide](https://pandas.pydata.org/docs/user_guide/index.html) is the real resource, and it is underrated.** For a quant specifically, these sections repay slow reading:
  - **Indexing and selecting data** (`.loc`/`.iloc`, chained-assignment and `SettingWithCopyWarning`)
  - **MultiIndex / advanced indexing** — unavoidable for panel data (date × instrument)
  - **Merge, join, concatenate and compare** — join cardinality bugs are the most expensive class of error in research code
  - **Group by: split-apply-combine** — `transform` vs `apply` vs `agg` is *the* pandas fluency test
  - **Time series / date functionality** — resampling, `asof` merges, business-day offsets, timezone handling
  - **Windowing operations** — rolling/expanding/EWM, i.e. most of a signal pipeline
  - **Enhancing performance** and **Scaling to large datasets** — where `eval`/`query`/Numba/dtype choice live
- **Free.** **Verdict: the User Guide *is* the pandas course. Nothing paid teaches these sections better.** Its weakness is that it is organised as reference, so it never tells you what a good pipeline *looks like* — hence Augspurger/Harrison below.

### "Python for Data Analysis", 3rd ed. — Wes McKinney — https://wesmckinney.com/book/
- **Free:** yes — the **full 3rd edition is Open Access HTML on the author's site**, updated for pandas 2.0 / Python 3.10. Code and datasets are **MIT-licensed** at [wesm/pydata-book](https://github.com/wesm/pydata-book) (**24,892 stars**, default branch `3rd-edition`, last pushed 2025-10-17 — actively maintained). Note the site text says the *prose* may not be copied/reproduced; the *code* is MIT.
- **Good for:** the canonical, written-by-the-author reference path through NumPy → pandas → data loading/cleaning → joins/reshaping → groupby → time series. Chapters 8 (join/combine/reshape), 10 (aggregation & group operations) and 11 (time series) are the quant core.
- **Verdict: the best free structured pandas book, full stop.** Honest caveat: it teaches pandas as a *toolkit*, in a somewhat imperative/assignment-heavy style. It will make you competent, not elegant.

### "Modern Pandas" — Tom Augspurger (free blog series)
- Part 1 (intro/indexing): https://tomaugspurger.net/posts/modern-1-intro/ · Part 2 (**method chaining**): https://tomaugspurger.net/posts/method-chaining/ · Index: https://tomaugspurger.net/tags/pandas/
- Seven parts: intro, method chaining, indexes, performance ("Fast Pandas"), tidy data, visualisation, time series.
- **Good for:** the missing *style* layer. Augspurger was a core pandas dev; this is the series that taught a generation of practitioners to write `df.assign(...).query(...).groupby(...).agg(...)` instead of ten reassignments to `df`. The "Indexes" and "Fast Pandas" posts are the ones with the most quant carry-over.
- **Free.** **Honest caveat:** written ~2016 and not fully updated; a few APIs have moved (`.ix` is gone, some `pd.rolling_*` forms are long dead) and the perf numbers are stale. The *ideas* have aged extremely well.
- **Verdict: read it right after McKinney. Free, short, and it's what makes your pandas readable.** Mentally s/deprecated API/modern equivalent/ as you go.

### "Effective Pandas 2" — Matt Harrison
- https://store.metasnake.com/effective-pandas-book (also Leanpub / Amazon). 2nd edition 2024, ~594 pages.
- **Good for:** the most sustained argument for a chaining-first, `assign`-driven, dtype-conscious pandas style; strong chapters on categoricals/memory, pivoting, grouping and debugging chains.
- **Paid** (roughly $40–50 range depending on format/vendor; verify).
- **Verdict: the best *paid* pandas book, but it substantially overlaps free Augspurger.** Buy it only if you've read Modern Pandas, liked the style, and want it systematised with exercises. Not a prerequisite for anything.

### pandas-cookbook — Julia Evans — https://github.com/jvns/pandas-cookbook
- **Verified repo facts:** 7,112 stars, last pushed 2024-10-24. **Runs in the browser with no install via JupyterLite:** https://jvns.github.io/pandas-cookbook/lab/index.html — and it "comes with batteries (data) included."
- **Good for:** messy *real* data, which is its explicit selling point ("examples with real-world data, and all the bugs and weirdness that entails"). Three datasets: NYC 311 calls, Montréal bike-path counts, Montréal hourly weather. Chapter 4 (groupby/aggregate) and Chapter 5 (combining dataframes + scraping) are the useful ones.
- **Honest caveat:** it's old material given a 2024 refresh, and **several chapters have known link-rot** — the upstream data URLs changed, producing 404s ([issue #50](https://github.com/jvns/pandas-cookbook/issues/50), [issue #67](https://github.com/jvns/pandas-cookbook/issues/67)). The bundled copies mostly save you.
- **Verdict: charming, free, zero-setup, and good for the "data is dirty" lesson — but it is a beginner cookbook, not a route to quant-level pandas.** Two evenings, no more.

### Kaggle Learn — pandas — https://www.kaggle.com/learn/pandas
- **Free.** 6 lessons, browser-based, no setup, hints and solutions for every exercise: creating/reading/writing, indexing & selecting, summary functions & maps, grouping & sorting, dtypes & missing values, renaming & combining.
- **Verdict: a well-designed micro-course and a fine *first* four hours — but it stops well short of what you need.** No MultiIndex, no serious time series, no rolling windows, no performance. Treat it as a warm-up before McKinney, not as pandas training. (Kaggle Learn's Python and Intro to SQL courses are similarly competent-but-shallow.)

### Free drilling: pandas_exercises — https://github.com/guipsamora/pandas_exercises
- **Verified:** 13,069 stars, BSD-3, last pushed 2025-10-17. Notebook exercises grouped by topic (filtering, apply, grouping, merge, time series, visualisation), each with a solutions notebook.
- **Verdict: the pandas analogue of numpy-100. Free, active, and the fastest way to convert reading into recall.**

### One forward-looking note: Polars
Not in your brief, but it belongs in an honest answer. Reporting indicates new Python analytics/ETL work in 2025–26 increasingly defaults to **[Polars](https://docs.pola.rs/)**, with pandas retained for exploratory notebooks and for libraries that only speak DataFrame; one widely-cited example is a bank quant team cutting an intraday VaR job from ~22 min to ~3 min on identical hardware by moving off pandas. **Caveat: this specific anecdote circulates via SEO-heavy comparison blogs and I could not verify it at source — treat the number as illustrative, not factual.** The defensible version: **learn pandas properly first (it is what interviews and existing research codebases use), then learn Polars' expression API**, which is closer to SQL/Spark semantics and will make you better at both. [DuckDB](https://duckdb.org/docs/) is the third piece of that modern stack and doubles as your local analytical-SQL sandbox — see below.

---

## 4. SQL — with an explicit verdict on window functions

Window functions are the dividing line. Almost every free SQL site teaches SELECT/JOIN/GROUP BY well; most stop right before the thing a quant actually needs (`ROW_NUMBER`/`RANK`, `LAG`/`LEAD`, `SUM(...) OVER (PARTITION BY ... ORDER BY ... ROWS BETWEEN ...)`, and frame clauses).

### Window-function verdict table

| Resource | Free? | Teaches window functions? | Verdict |
|---|---|---|---|
| **PostgreSQL Exercises** | Free | **Yes — properly** | Best free window practice |
| **Mode SQL Tutorial** | Free | **Yes — dedicated Advanced section** | Best free window *explanation* |
| **SQLZoo** | Free | **Yes** (`Window_functions`, `Window_LAG`) | Good, terse, ugly |
| **8 Week SQL Challenge** | Free | **Yes, in context** | Best free *applied* practice |
| **DataLemur** | Freemium | **Yes — heavy emphasis** | Best interview drilling, paywalled |
| **StrataScratch** | Freemium | Yes | Largest bank, aggressive paywall |
| **LeetCode SQL 50** | Free | Yes, some | Fine supplement |
| **HackerRank SQL** | Free | Thin | Volume, low depth |
| **PostgreSQL docs** | Free | **Yes — authoritative** | Read the tutorial + ref |
| **SQLBolt** | Free | **No** | Good basics only; then leave |
| **Select Star SQL** | Free | **No — explicitly omitted** | Great mental models, no windows |

### PostgreSQL Exercises — https://pgexercises.com/
- **Free.** 81 exercises on one small, coherent dataset (a country club: members, bookings, facilities), progressing Basic → Joins/Subqueries → Modifying data → **Aggregation (including window functions)** → Timestamps → String ops → **Recursive queries**. Every question has a full worked answer *with prose explanation*, not just a solution dump.
- **Good for:** the best free hands-on window-function practice available, on real Postgres semantics, with recursive CTEs as a bonus. The single-dataset design means you stop re-learning the schema and start thinking about the query.
- **Verdict: do this one first among the practice sites.** Its own framing is right — it is a companion to the Postgres docs, not a standalone course. Weakness: no query performance/EXPLAIN content, and the dataset is tiny.

### Mode SQL Tutorial — https://mode.com/sql-tutorial/
- **Free**, in-browser query editor against real datasets. Three tiers: Basic, Intermediate, **Advanced** — the Advanced section explicitly covers data types, date formats, subqueries, **window functions**, performance tuning, and pivoting, each with practice problems runnable in Mode's app.
- **Good for:** the clearest *narrative explanation* of window functions in the free tier — it builds `PARTITION BY` and frame clauses up conceptually rather than by example-dumping. Widely described as the most beginner-friendly comprehensive free tutorial.
- **Verdict: best free written window-functions teaching. Pair it with pgexercises for drilling.**
- **Risk flag:** Mode was acquired by ThoughtSpot, and content is now mirrored at [thoughtspot.com/sql-tutorial](https://www.thoughtspot.com/sql-tutorial/sql-window-functions) with the legacy `sqlschool.modeanalytics.com/advanced/` still floating around. Assume link rot; grab what you need.

### SQLZoo — https://sqlzoo.net/
- **Free.** Confirmed window coverage: [Window functions](https://sqlzoo.net/wiki/Window_functions) (RANK, PARTITION BY over election data) and [Window LAG](https://sqlzoo.net/wiki/Window_LAG) (LAG/LEAD over COVID data — a genuinely time-series-shaped exercise, which is unusual and useful).
- **Good for:** fast, no-signup drilling across multiple engines (MySQL/Postgres/SQL Server dialect notes). The LAG tutorial in particular is close to what you'd do to a price series.
- **Verdict: legitimately good and free; the UI is dated and the hints are terse.** Use for reps, not for learning concepts cold.

### 8 Week SQL Challenge (Danny Ma) — https://8weeksqlchallenge.com/
- **Free** — all eight case studies plus bonus content, e.g. [Case Study #1 "Danny's Diner"](https://8weeksqlchallenge.com/case-study-1/). Paid course *Serious SQL* is separate at **$49 (USD), $29 student** ([datawithdanny.com](https://www.datawithdanny.com/courses/serious-sql)).
- **Good for:** the gap everything else leaves — **applied, business-shaped SQL**. You are handed a schema and an analytical question ("customer loyalty and spending behaviour") and must reach for CTEs, window functions, joins and aggregation *because the problem demands it*, not because it's chapter 7. That is the actual skill.
- **Verdict: the best free "am I ready to do analytical SQL for a job" test.** Hundreds of public GitHub solution repos mean you can compare your answer against many others — use that deliberately.

### DataLemur — https://datalemur.com/
- **Freemium.** Reported: free tier ~30–50 questions; premium ~$10–15/month, with a lifetime option around $300 ([pricing](https://datalemur.com/pricing)). Reported that 60%+ of hard/premium questions are paywalled. **Prices from secondary sources — verify.** Built by Nick Singh (ex-Facebook/Google), author of *Ace the Data Science Interview*.
- **Good for:** real interview questions from Meta/Google/Amazon etc., with **deep, deliberate emphasis on window functions** — `DENSE_RANK`, `LAG`/`LEAD`, and explicit window-frame calculations — plus tiered hints and full solutions.
- **Verdict: the best-targeted free tier for interview-shaped window-function practice; the paywall is real but the price is modest.** The site's own comparison blog posts are marketing — ignore those.

### StrataScratch — https://www.stratascratch.com/
- **Freemium.** Free tier ~50 questions (some sources say 75+). Paid tiers reported from ~$8.25/month billed annually (Learner) up to ~$39/month, plus ~$159/year and interview-prep/projects tiers ([pricing](https://platform.stratascratch.com/pricing)). **Verify — figures varied a lot across sources.**
- **Good for:** raw volume — reportedly 500–700+ SQL and Python problems sourced from real interviews, in multiple dialects, plus Python-pandas versions of the same questions (useful: solving one problem both ways is excellent for a quant).
- **Honest verdict:** the community description that stuck is "a LeetCode clone focused on data folks", and even favourable reviews call the paywall aggressive — the free ~50 is enough to evaluate, not enough to prepare. **Good if you're actively interviewing and want a month of it; not a learning resource.**

### LeetCode SQL — https://leetcode.com/studyplan/top-sql-50/
- **Free** (the SQL 50 study plan is free; LeetCode Premium exists for company-tagged questions). Covers basic selects, joins, aggregation, subqueries and window functions.
- **Verdict: fine, free supplementary reps, and the "SQL 50" list is a sane curated sequence.** But problems are puzzle-shaped and the schemas are artificial — it trains syntax recall, not analytical judgement. Do it *after* pgexercises and the 8-Week Challenge.

### HackerRank SQL — https://www.hackerrank.com/domains/sql
- **Free.** Large problem bank, clean UI, used by employers for screening — which is the main reason to touch it.
- **Verdict: high volume, low depth. Historically weak on window functions and CTEs relative to the others here.** Use it only to acclimatise to the platform if a firm screens on it.

### SQLBolt — https://sqlbolt.com/
- **Free**, interactive, no signup. Excellent, gentle first two hours on SELECT/WHERE/JOIN/GROUP BY.
- **Honest verdict: it stops before everything that matters here.** Multiple sources state it has had no meaningful content update since ~2018 and covers neither window functions nor CTEs — **note that those sources are competing SQL products, so treat the "since 2018" date as unverified**; the *absence* of window-function lessons is checkable from its own lesson list and is the real point. **Use for day one, then leave.**

### Select Star SQL — https://selectstarsql.com/
- **Free, no ads, no registration, no downloads.** Interactive, built on a genuinely interesting dataset (Texas death-row executions, 1976–present, partly hand-extracted from scanned documents). Chapters: individual rows → aggregation ("Claims of Innocence") → GROUP BY and nested queries ("The Long Tail") → joins → challenge questions. Source: [zichongkao/selectstarsql](https://github.com/zichongkao/selectstarsql).
- **Good for:** it is explicitly *not a reference page — it conveys a mental model for writing SQL*, and it's the best free resource for the semantics people get wrong (NULL behaviour, what a join actually does to cardinality, how aggregation interacts with filtering).
- **Critical honest finding — it does NOT teach window functions.** The book says so itself in its ["The Long Tail"](https://selectstarsql.com/longtail.html) closing section: window functions and CTEs are named as things worth learning but were **omitted because SQLite did not support window functions at the time of writing**.
- **Verdict: excellent and free for *thinking* in SQL; useless as your window-functions source. Read it early, then go to Mode + pgexercises for windows.**

### Authoritative references (free, and better than any tutorial once you're past beginner)
- **[PostgreSQL: Window Functions tutorial](https://www.postgresql.org/docs/current/tutorial-window.html)** and the [window function reference](https://www.postgresql.org/docs/current/functions-window.html) — short, precise, and the definitive statement of frame semantics. **Read this once you can already write a `RANK()`; it's what turns "I copied a pattern" into "I know what the frame does."**
- **[modern-sql.com](https://modern-sql.com/)** — free, standards-focused, excellent on what's actually in SQL:2003/2011/2016 and which engines implement it. Best free resource on the *edges* of window functions and CTEs.
- **[DuckDB](https://duckdb.org/docs/)** — free, `pip install duckdb`, runs analytical SQL directly over pandas DataFrames and Parquet files. **This is the practical recommendation: it gives you a zero-setup local engine with full modern window-function support, so you can practise analytical SQL on your own price data instead of on toy schemas.**
- Paid, for completeness: Itzik Ben-Gan, *T-SQL Window Functions* (2nd ed.) is the deepest treatment in print, but it is T-SQL-specific — only worth it if you land somewhere SQL-Server-shaped.

**SQL path:** SQLBolt (2 hrs) → Select Star SQL (mental model) → Mode Advanced (window concepts) → pgexercises (window drilling + recursive) → 8 Week SQL Challenge (applied) → DataLemur free tier (interview shape) → Postgres docs + modern-sql.com as reference. Practise everything locally in DuckDB against your own data.

---

## 5. Numerical / scientific computing

### Scientific Python Lectures — https://lectures.scientific-python.org/
Covered above. For this section specifically: the **[SciPy chapter](https://lectures.scientific-python.org/intro/scipy/index.html)** (linalg, optimisation, interpolation, statistics, signal processing) and **[Optimizing code](https://lectures.scientific-python.org/advanced/optimizing/index.html)** are the relevant parts. Free, CC-BY, maintained (last stable release 2024.1). **Verdict: the best free bridge between "I know NumPy" and "I know numerics".**

### fast.ai — Computational Linear Algebra for Coders
- Course announcement: https://www.fast.ai/posts/2017-07-17-num-lin-alg.html · Notebooks: https://github.com/fastai/numerical-linear-algebra · Video playlist on YouTube.
- **Verified repo facts:** 10,965 stars, last pushed 2024-04-16. Free online textbook of Jupyter notebooks + Rachel Thomas's lecture videos, originally a USF masters course.
- **Good for:** the framing is exactly right for a quant — *"How do we do matrix computations with acceptable speed and acceptable accuracy?"* Covers randomised SVD, PageRank/eigen methods, QR/LU and stability, NMF, CT reconstruction, with PyTorch and Numba used throughout. Floating-point stability and conditioning get real attention, which is rare and directly relevant to covariance estimation and regression.
- **Free.** **Honest caveat: it's 2017 material with a 2024 touch-up; the library APIs (old PyTorch, old sklearn) will need fixing as you go.** The mathematics is unaffected.
- **Verdict: the best free applied numerical-linear-algebra course, and better suited to a quant than a pure-maths treatment.**

### Trefethen & Bau, *Numerical Linear Algebra*
The classical reference (conditioning, stability, QR, SVD, iterative methods). **Paid book, no free official site.** Worth it if you want the theory properly; fast.ai's course is the practical complement, not a replacement. Many universities post free lecture notes following it — search for course pages rather than PDF-mirror sites.

### "Compiler Explorer for Python" — the honest answer
There is no true Godbolt equivalent for Python (no interesting machine code to show — CPython bytecode is the closest, via `dis.dis()`, which is genuinely worth knowing). What you actually want is a **profiling stack**:

| Tool | Use it for | Link |
|---|---|---|
| **`py-spy`** | Sampling profiler that **attaches to a running process** (incl. in Docker, any venv) with low overhead. Start here. | https://github.com/benfred/py-spy |
| **Scalene** | Line-by-line **CPU (Python vs native) + memory + GPU**, and flags I/O waits. The one that tells you *"this line is slow because it left NumPy and went back to Python."* | https://github.com/plasma-umass/scalene |
| **`line_profiler`** | Surgical line-by-line timing of one decorated function once you know where to look. | https://github.com/pyutils/line_profiler |
| **SnakeViz** | Interactive visualisation of `cProfile` output. | https://jiffyclub.github.io/snakeviz/ |
| **`pyinstrument`** | Low-overhead call-stack profiler with very readable output. | https://github.com/joerick/pyinstrument |
| **`%timeit`** / `timeit` | Microbenchmarking single expressions in Jupyter. The one you'll use hourly. | stdlib |

Consensus workflow across sources: **py-spy (or pyinstrument) to find the hot path → Scalene to see Python-vs-native-vs-memory → line_profiler to zoom in.** All free and open source. If you only learn two, learn **py-spy and Scalene**. Curated list: [msaroufim/awesome-profiling](https://github.com/msaroufim/awesome-profiling).

For the "why is this slow" layer above profiling: the pandas [Enhancing performance](https://pandas.pydata.org/docs/user_guide/enhancingperf.html) guide, the Scientific Python Lectures optimizing chapter, and [Numba](https://numba.readthedocs.io/) for the cases where vectorisation genuinely cannot express the loop.

---

## 6. Practice data — real financial data, free

Blunt framing first: **free financial data is either low-quality, low-frequency, rate-limited, or all three.** For *learning data manipulation*, that is completely fine — you need messy, awkward, real data, not clean institutional data. For *learning research methodology*, free data will actively teach you bad habits (survivorship bias above all). Know which you're doing.

### Free and genuinely usable

**FRED (Federal Reserve Economic Data)** — https://fred.stlouisfed.org/ · API docs: https://fred.stlouisfed.org/docs/api/fred/
- ~800,000+ economic time series, **free, with a free API key**. Python wrapper: [`fredapi`](https://github.com/mortada/fredapi) (also handles **ALFRED**, i.e. *vintage/point-in-time* data — which is the single most underrated free thing on this list, because it lets you avoid look-ahead bias in macro).
- **Verdict: the best free data source here, full stop.** Clean, documented, permanent, no scraping, and vintages available. Ideal for pandas time-series practice (resampling, `merge_asof`, releases vs revisions).

**yfinance** — https://github.com/ranaroussi/yfinance
- **Free.** The default starting point, and the most convenient.
- **Honest verdict: unreliable by construction.** It is a **scraper of an unofficial, undocumented, unsupported Yahoo endpoint**. Consistently reported problems: aggressive undocumented rate limiting, IP bans, silently inconsistent data, and breakage whenever Yahoo changes its site. Adjusted-close handling and splits/dividends have historically been inconsistent, and it has survivorship bias (delisted tickers largely absent).
- **Use it for:** learning pandas on price data, prototyping, throwaway analysis. **Never** for backtest results you'd show anyone.

**Nasdaq Data Link (ex-Quandl)** — https://data.nasdaq.com/
- **Important, verified:** the free **WIKI Prices** US equity feed is **frozen — it only goes to March 2018 and is discontinued for new users**, because its upstream community source disappeared. Nasdaq's own help page says they **no longer recommend using it for investment or analysis** ([source](https://help.data.nasdaq.com/article/506-why-does-wiki-prices-only-go-up-to-march-2018)).
- Free content that remains: FRED mirrors, some commodity/central-bank series, and free samples of paid feeds (Sharadar SEP/SF1 etc. are paid).
- **Verdict: largely a dead end for free equity prices now. Historical WIKI is still fine as a static practice dataset** (a mirrored copy lives on [Kaggle](https://www.kaggle.com/datasets/marketneutral/quandl-wiki-prices-us-equites)) — just never treat it as current.

**Alpha Vantage** — https://www.alphavantage.co/
- **Free tier, but severely limited: widely reported at ~25 API calls per day** (it was 500/day historically — this has been cut). Covers equities, FX, crypto, fundamentals, technical indicators. Well-documented REST API, officially supported (unlike yfinance).
- **Verdict: fine for a small, well-defined educational project; useless for anything universe-wide.** Its virtue over yfinance is that it's a real, sanctioned API that won't ban you — its vice is that 25 calls/day means you'll spend your time writing caching logic.

**Tiingo** — https://www.tiingo.com/
- Free tier includes daily EOD for most US stocks; paid tier is cheap (~$10/month) and there is **academic pricing**. Explicitly positions itself toward quantitative research; reputation is "clean, reliable EOD at a low flat rate."
- **Verdict: the best value-for-money step up from free, and the one I'd actually recommend if you're willing to spend $10/month.**

**Polygon.io** — https://polygon.io/ — free tier reported at ~5 calls/minute, end-of-day only; real strength is WebSocket streaming and minute bars on paid tiers. **Verdict: free tier is a demo, not a dataset.**

**Databento** — https://databento.com/ — paid, metered ($1–5/GB; ~$199/mo standard tier reported). Tick and L2 depth. **Verdict: not a learning resource — but it's what you'd actually use later, and their [docs](https://databento.com/docs) are free and instructive about market-data structure (MBO/MBP/OHLCV), which is worth reading even if you never buy.**

**Kaggle Datasets** — https://www.kaggle.com/datasets
- **Free**, huge, zero-friction, and runs in free notebooks with the data mounted.
- **Honest verdict: excellent for pandas practice, hazardous for finance methodology.** Most financial datasets on Kaggle are (a) scraped from the same unreliable sources, (b) undocumented as to adjustment methodology, and (c) **survivorship-biased** — they contain today's listed tickers only. The standing rule from practitioners: *if a dataset does not explicitly state that delisted securities are included, assume they are not*, and treat any unusually smooth equity curve as a red flag. Survivorship bias is measured at roughly 0.9%/yr even in mutual-fund studies and is materially worse for individual-stock selection.
- **Use Kaggle for:** dirty CSVs, missing values, joins, groupbys, time zones — i.e. the actual manipulation skill.

### Institutional

**WRDS (Wharton Research Data Services)** — https://wrds-www.wharton.upenn.edu/
- **Institution-only.** Access requires affiliation (faculty/student/staff) with a subscribing university, verified through that institution's WRDS administrator. CRSP and Compustat are paid subscription resources within it. There is **no individual free tier**.
- **If you have university access, use it** — CRSP is survivorship-bias-free and is the reason academic finance results are trustworthy.
- **If you don't:** WRDS publishes **dummy/pseudo data** with the same table and column structure, so you can write and test WRDS-shaped code without access. Best entry point: [Tidy Finance — WRDS Dummy Data with Python](https://www.tidy-finance.org/python/wrds-dummy-data.html).

### The resource that ties this whole section together

**Tidy Finance with Python** — https://www.tidy-finance.org/python/
- **Free, complete book online** (print edition via Chapman & Hall/CRC), by Scheuch, Voigt, Weiss and Frey. Open-source, plus a companion [`tidyfinance` Python package](https://python.tidy-finance.org/).
- **Good for:** exactly your stated goal — it starts from tidy-data principles and coding style **using pandas, numpy and plotnine**, then does real empirical asset pricing: connecting to WRDS, preparing **CRSP, Compustat, Mergent FISD and TRACE**, building a local database, and running beta estimation, portfolio sorts, Fama-MacBeth, and factor models. See [WRDS, CRSP and Compustat with Python](https://www.tidy-finance.org/python/wrds-crsp-and-compustat.html).
- **Verdict: the single best free resource for "quant data manipulation on real financial data with correct methodology".** It is the bridge between "I know pandas" and "I do research". If you only add one thing from this section, add this.

---

## 7. Recommended free path (condensed)

**Phase 1 — language (2–3 weeks)**
[Official Python tutorial](https://docs.python.org/3/tutorial/) → [Exercism Python track](https://exercism.org/tracks/python) with mentoring → [Real Python](https://realpython.com/) articles as needed → skim [Fluent Python free extras](https://www.fluentpython.com/extra/).

**Phase 2 — vectorised thinking (3–4 weeks) — the differentiator**
[NumPy broadcasting](https://numpy.org/doc/stable/user/basics.broadcasting.html) + [indexing](https://numpy.org/doc/stable/user/basics.indexing.html) + [copies/views](https://numpy.org/doc/stable/user/basics.copies.html) → **[From Python to NumPy](http://www.labri.fr/perso/nrougier/from-python-to-numpy/)** → [numpy-100](https://github.com/rougier/numpy-100) → [Advanced NumPy (strides/memory)](https://lectures.scientific-python.org/advanced/advanced_numpy/index.html).

**Phase 3 — pandas (4–6 weeks)**
[Kaggle Learn pandas](https://www.kaggle.com/learn/pandas) (warm-up) → **[Python for Data Analysis 3E, free](https://wesmckinney.com/book/)** ch. 8/10/11 → **[Modern Pandas](https://tomaugspurger.net/posts/modern-1-intro/)** for style → pandas User Guide sections: MultiIndex, merge, groupby, time series, **windowing**, enhancing performance → drill on [pandas_exercises](https://github.com/guipsamora/pandas_exercises).

**Phase 4 — SQL (3–4 weeks)**
[SQLBolt](https://sqlbolt.com/) (2 hrs) → [Select Star SQL](https://selectstarsql.com/) (mental model; **no windows**) → [Mode Advanced](https://mode.com/sql-tutorial/) (window concepts) → **[pgexercises](https://pgexercises.com/)** (window + recursive drilling) → **[8 Week SQL Challenge](https://8weeksqlchallenge.com/)** (applied) → [Postgres window docs](https://www.postgresql.org/docs/current/tutorial-window.html) + [modern-sql.com](https://modern-sql.com/) as reference. Do it all locally in **[DuckDB](https://duckdb.org/docs/)** against your own price data.

**Phase 5 — numerics & performance (ongoing)**
[fast.ai Computational Linear Algebra](https://github.com/fastai/numerical-linear-algebra) → [py-spy](https://github.com/benfred/py-spy) + [Scalene](https://github.com/plasma-umass/scalene) on your own slow code → [pandas Enhancing performance](https://pandas.pydata.org/docs/user_guide/enhancingperf.html).

**Phase 6 — real data**
[FRED](https://fred.stlouisfed.org/) + [`fredapi`](https://github.com/mortada/fredapi) (incl. ALFRED vintages) → yfinance for convenience, knowing its flaws → **[Tidy Finance with Python](https://www.tidy-finance.org/python/)** end to end → WRDS if you have institutional access, [WRDS dummy data](https://www.tidy-finance.org/python/wrds-dummy-data.html) if not.

**Total spend if you buy nothing: £0.** The only purchases I'd defend are *Fluent Python* and *Effective Python* (books, one-off), and possibly one month of DataLemur or StrataScratch immediately before interviews. Python Morsels at $240/yr and Effective Pandas are good products that are hard to justify against the free alternatives above.

---

## Appendix: verified repository metadata (fetched via GitHub API, 2026-09-06)

| Repo | Stars | Last push | Licence |
|---|---|---|---|
| [wesm/pydata-book](https://github.com/wesm/pydata-book) | 24,892 | 2025-10-17 | Other (code MIT) |
| [rougier/numpy-100](https://github.com/rougier/numpy-100) | 14,426 | 2026-08-26 | MIT |
| [guipsamora/pandas_exercises](https://github.com/guipsamora/pandas_exercises) | 13,069 | 2025-10-17 | BSD-3-Clause |
| [fastai/numerical-linear-algebra](https://github.com/fastai/numerical-linear-algebra) | 10,965 | 2024-04-16 | (none stated) |
| [jvns/pandas-cookbook](https://github.com/jvns/pandas-cookbook) | 7,112 | 2024-10-24 | (none stated) |
| [rougier/from-python-to-numpy](https://github.com/rougier/from-python-to-numpy) | 2,149 | 2025-05-06 | CC-BY-NC-SA |

## Appendix: sources

Search-derived, listed by section.

Python: [docs.python.org tutorial](https://docs.python.org/3/tutorial/index.html) · [Real Python membership](https://realpython.com/account/join/) · [Real Python discount FAQ](https://support.realpython.com/article/10-is-there-a-discount-for-the-membership) · [python.org pricing discussion](https://discuss.python.org/t/unclear-about-real-python-subscription/105143) · [fluentpython.com extras](https://www.fluentpython.com/extra/) · [fluentpython/book-site](https://github.com/fluentpython/book-site) · [effectivepython.com](https://effectivepython.com/) · [Exercism Python track](https://exercism.org/tracks/python) · [Exercism about](https://exercism.org/about) · [Python Morsels pricing](https://www.pythonmorsels.com/pricing/) · [Trey Hunner lifetime sale](https://treyhunner.com/2025/11/lifetime-access-sale-2025/) · [Talk Python Training pricing](https://training.talkpython.fm/policies/pricing) · [Talk Python podcast](https://talkpython.fm/)

NumPy: [quickstart](https://numpy.org/doc/stable/user/quickstart.html) · [absolute beginners](https://numpy.org/doc/stable/user/absolute_beginners.html) · [broadcasting](https://numpy.org/doc/stable/user/basics.broadcasting.html) · [From Python to NumPy](http://www.labri.fr/perso/nrougier/from-python-to-numpy/) · [numpy-100](https://github.com/rougier/numpy-100) · [Scientific Python Lectures](https://lectures.scientific-python.org/) · [its releases](https://github.com/scipy-lectures/scientific-python-lectures/releases)

pandas: [10 minutes to pandas](https://pandas.pydata.org/docs/user_guide/10min.html) · [User Guide](https://pandas.pydata.org/docs/user_guide/index.html) · [Python for Data Analysis 3E](https://wesmckinney.com/book/) · [pydata-book](https://github.com/wesm/pydata-book) · [Modern Pandas pt.1](https://tomaugspurger.net/posts/modern-1-intro/) · [pt.2 method chaining](https://tomaugspurger.net/posts/method-chaining/) · [Effective Pandas 2](https://store.metasnake.com/effective-pandas-book) · [pandas-cookbook](https://github.com/jvns/pandas-cookbook) · [its JupyterLite build](https://jvns.github.io/pandas-cookbook/lab/index.html) · [Kaggle Learn pandas](https://www.kaggle.com/learn/pandas) · [pandas_exercises](https://github.com/guipsamora/pandas_exercises) · [Polars docs](https://docs.pola.rs/)

SQL: [pgexercises](https://pgexercises.com/) · [Mode SQL Tutorial](https://mode.com/sql-tutorial/) · [ThoughtSpot mirror, window functions](https://www.thoughtspot.com/sql-tutorial/sql-window-functions) · [SQLZoo window functions](https://sqlzoo.net/wiki/Window_functions) · [SQLZoo Window LAG](https://sqlzoo.net/wiki/Window_LAG) · [SQLBolt](https://sqlbolt.com/) · [Select Star SQL](https://selectstarsql.com/) · [Select Star SQL "The Long Tail" — window functions omitted](https://selectstarsql.com/longtail.html) · [selectstarsql repo](https://github.com/zichongkao/selectstarsql) · [DataLemur pricing](https://datalemur.com/pricing) · [StrataScratch pricing](https://platform.stratascratch.com/pricing) · [LeetCode SQL 50](https://leetcode.com/studyplan/top-sql-50/) · [HackerRank SQL](https://www.hackerrank.com/domains/sql) · [8 Week SQL Challenge](https://8weeksqlchallenge.com/) · [Serious SQL](https://www.datawithdanny.com/courses/serious-sql) · [PostgreSQL window tutorial](https://www.postgresql.org/docs/current/tutorial-window.html) · [modern-sql.com](https://modern-sql.com/) · [DuckDB](https://duckdb.org/docs/)

Numerics/profiling: [fast.ai course announcement](https://www.fast.ai/posts/2017-07-17-num-lin-alg.html) · [numerical-linear-algebra repo](https://github.com/fastai/numerical-linear-algebra) · [KDnuggets writeup](https://www.kdnuggets.com/2020/07/computational-linear-algebra-free-course.html) · [py-spy](https://github.com/benfred/py-spy) · [Scalene](https://github.com/plasma-umass/scalene) · [line_profiler](https://github.com/pyutils/line_profiler) · [SnakeViz](https://jiffyclub.github.io/snakeviz/) · [pyinstrument](https://github.com/joerick/pyinstrument) · [awesome-profiling](https://github.com/msaroufim/awesome-profiling)

Data: [FRED](https://fred.stlouisfed.org/) · [fredapi](https://github.com/mortada/fredapi) · [yfinance](https://github.com/ranaroussi/yfinance) · [Nasdaq: why WIKI stops at March 2018](https://help.data.nasdaq.com/article/506-why-does-wiki-prices-only-go-up-to-march-2018) · [Alpha Vantage](https://www.alphavantage.co/) · [Tiingo](https://www.tiingo.com/) · [Polygon](https://polygon.io/) · [Databento](https://databento.com/) · [Kaggle datasets](https://www.kaggle.com/datasets) · [QuantRocket primer on survivorship bias](https://www.quantrocket.com/blog/survivorship-bias/) · [WRDS](https://wrds-www.wharton.upenn.edu/) · [Tidy Finance with Python](https://www.tidy-finance.org/python/) · [Tidy Finance WRDS/CRSP/Compustat](https://www.tidy-finance.org/python/wrds-crsp-and-compustat.html) · [Tidy Finance WRDS dummy data](https://www.tidy-finance.org/python/wrds-dummy-data.html)
