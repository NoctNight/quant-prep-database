# Websites, Free Courses & Online Resources for Quant-Level Probability, Statistics, Econometrics, Time Series and ML

**Compiled:** 2026-09-06
**Audience:** someone preparing to work / interview as a **quantitative researcher** (buy-side systematic, market-making research, or QR at a bank).

---

## 0. Methodology and honesty note about sources

**Constraint you should know about before trusting the "practitioner opinion" claims below.**

This research ran inside a sandbox whose egress proxy blocks nearly all direct page fetches. Specifically:

- `reddit.com` / `old.reddit.com` — **blocked at the network gateway (403 on CONNECT)** and also excluded from the search backend (`API Error: 400 The following domains are not accessible to our user agent: ['reddit.com']`). **No r/quant, r/statistics or r/learnmath threads could be read directly.**
- `news.ycombinator.com` and `hn.algolia.com` — **blocked (403 on CONNECT)**. No HN threads read directly.
- Direct `WebFetch` was also blocked for: `ocw.mit.edu`, `otexts.com`, `statlearning.com`, `stat110.hsites.harvard.edu`, `gresearch.com`, `geoffruddock.com`. Effectively every page.

What *did* work: the **web search tool** (which returns synthesised summaries with quoted fragments from the underlying pages), and the **GitHub API** (repo metadata). So:

- Claims about **what a resource is, whether it's free, and what it covers** are sourced from search summaries quoting the official pages — reliable.
- Claims about **community sentiment** are sourced from (a) search summaries of blog posts and forum-adjacent pages that *were* indexed, (b) a small number of genuinely practitioner-written sources that survived (Headlands Technologies' quant blog, G-Research's own published reading list), and (c) my own prior knowledge of these communities. **Where a verdict is my judgement rather than a cited source, it is marked `[judgement]`.** Treat those as informed opinion, not evidence.

The single best *practitioner* sources that survived the block and are worth reading yourself:

- **Headlands Technologies blog** (a real quant trading firm; Max Dama, quant researcher) — book review series for new quants: https://blog.headlandstech.com/ ; the ESL review: https://blog.headlandstech.com/2022/02/16/elements-of-statistical-learning-8-10/ ; Max Dama's author page: https://blog.headlandstech.com/author/max/ ; the classic "Quant Trading Summary": https://blog.headlandstech.com/wp-content/uploads/2017/08/Headlands-Quant-Trading-Summary-Max-Dama.pdf
- **G-Research's own published prep guidance** (a top systematic fund telling you what it expects): https://www.gresearch.com/wp-content/uploads/2020/09/200630-quant-research-preparation.pdf and the 2025 ML-role reading list https://www.gresearch.com/wp-content/uploads/2025/07/Quantitative-research-and-machine-learning-interview-prep-recommended-reading.pdf , plus https://www.gresearch.com/career-guides/quantitative-researcher-interview-questions/

**The most important single data point in this whole document:** G-Research's published guidance states that **undergraduate-level probability and statistics is sufficient preparation**, with additional review of *portfolio optimization, time series analysis, and Monte Carlo methods*. That is a firm with a famously hard interview telling you the bar is "undergrad probability/stats, but genuinely solid" — not measure theory, not stochastic calculus, not deep learning. Calibrate everything below against that.

---

## 1. Probability

### Verdict table

| Resource | Cost | Rigour | Verdict for a quant candidate |
|---|---|---|---|
| Harvard Stat 110 (Blitzstein) | Free | High (calculus-based, proof-aware) | **Do this one.** Best single fit. |
| MIT 6.041 / 6.431x (Tsitsiklis) | Free (OCW) / free-audit (edX) | High, engineering-flavoured | **Excellent alternative / complement.** Best problem sets. |
| MIT 18.600 (Sheffield) | Free | Highest of the three | Optional. Do if 110 felt easy. |
| Brilliant.org | $240/yr | Low–medium | **Skip.** Not remotely sufficient. |
| Khan Academy | Free | Low (AP/HS) | **Skip** unless patching an actual gap. |

### Harvard Stat 110 — Joe Blitzstein ⭐ top pick

- Course home: https://stat110.hsites.harvard.edu/
- Lecture videos (34 hours, free): https://stat110.hsites.harvard.edu/youtube
- **Free textbook, 2nd ed.**: http://probabilitybook.net (confirmed: "A free online version of the second edition ... is available at probabilitybook.net")
- Math prerequisite review handout: https://projects.iq.harvard.edu/files/stat110/files/math_review_handout.pdf
- edX version (Stat110x) exists and is described by Harvard as *complementary* to the video lectures — animations and interactives, not a substitute: https://www.edx.org/bio/joseph-blitzstein

**Genuinely good for:** the exact style of thinking quant interviews test. Blitzstein's "story proofs" — proving an identity by counting the same thing two ways in words — is precisely the skill behind the classic interview questions (expected number of X, symmetry arguments, conditioning cleverly instead of grinding integrals). The full package is unusual: video lectures + free book + weekly problem sets + a **detailed solutions manual for 8–10 exercises per chapter**, which is what makes true self-study possible.

**Rigour:** calculus-based, covers joint/conditional distributions, MGFs, transformations, limit theorems, Markov chains. Not measure-theoretic. That is the correct level. `[judgement]` The frequently repeated claim that Stat 110 is "the" quant probability course is, for once, roughly true — it is the highest-yield-per-hour resource on this entire list.

**Honest weakness:** it is a *first* probability course. It will not by itself get you through a hard Jane Street / Optiver probability round; for that you also need volume of problems (Blitzstein's own exercises, then a puzzle book).

### MIT 6.041 / 6.431x — John Tsitsiklis

- OCW 6.041SC (Fall 2013, full self-contained version with solutions): https://ocw.mit.edu/courses/6-041sc-probabilistic-systems-analysis-and-applied-probability-fall-2013/
- OCW 6.041 (Fall 2010): https://ocw.mit.edu/courses/6-041-probabilistic-systems-analysis-and-applied-probability-fall-2010/
- OCW RES.6-012 "Introduction to Probability" (the polished video series): https://ocw.mit.edu/courses/res-6-012-introduction-to-probability-spring-2018/
- edX / MITx Online 6.431x (part of the Statistics & Data Science MicroMasters): https://www.edx.org/learn/probability/massachusetts-institute-of-technology-probability-the-science-of-uncertainty-and-data and https://mitxonline.mit.edu/courses/course-v1:MITxT+6.431x/
- Community solution repo: https://github.com/mitx-data-science/6.431x

**Rigour:** MIT's own description — "develops material in an **intuitive — but still rigorous and mathematically precise** — manner, rather than relying on a traditional theorem-proof format." Tsitsiklis himself: "more ambitious than the typical undergraduate probability class ... we aim to provide the crispest way of explaining the concepts."

**Genuinely good for:** stochastic processes (Bernoulli/Poisson processes, Markov chains) treated far more seriously than in Stat 110, plus a clean treatment of classical *and* Bayesian inference at the end. The problem sets are harder and more numerous than Harvard's.

**Free vs paid:** OCW versions are entirely free including solutions. The edX/MITx run is free to audit; the verified certificate (needed if you want the MicroMasters credential) is paid. **`[judgement]` Do not pay.** No quant firm cares about an edX certificate; they care whether you can solve the problems. Use OCW 6.041SC, which has the same content plus solutions, for $0.

**Verdict:** `[judgement]` Stat 110 and 6.041 are near-substitutes; the highest-return path is Stat 110 for the *conceptual* framing and 6.041's problem sets for *volume*. Doing both fully is ~250 hours and is over-investment unless you have the time.

### MIT 18.600 — Probability and Random Variables (Scott Sheffield)

- Subject page: https://math.mit.edu/academics/undergrad/subjects/186x.html

MIT's own catalogue says 18.600 "covers a broader range of topics in probability, at **greater depth** than either 18.05 or 6.3700 [=6.041], and it is the probability subject of choice for most Mathematics majors."

**Verdict:** `[judgement]` The most rigorous of the three and the closest to a maths-department treatment, but its incremental value over Stat 110 for interview and job performance is small. Do it if you enjoyed 110 and want the extra depth (or if you're heading toward derivatives pricing where you'll need measure-theoretic probability later). Otherwise it's a nice-to-have.

### Brilliant.org — **too basic, and it costs money**

- https://brilliant.org/
- Pricing verified: **$240/year, or $30/month** in the US; family plan $299.99/yr. The free tier "gives access to the first few lessons of most courses and one daily practice problem" and reviewers note "the free tier is too limited for significant progress — you'll hit paywalls within days."

**What it's genuinely good for:** puzzle-style engagement, and rebuilding a habit if you're rusty and unmotivated. The interactive format is good at the *first ten minutes* of a topic.

**Verdict: skip.** `[judgement]` This is the clearest "noise" item on the list. Brilliant's probability content stops well before joint distributions, transformations, MGFs, convergence, or anything you'd be asked in a QR interview — and you'd be paying $240/yr for it while Blitzstein's textbook, lectures, and solutions are free. The one defensible use: someone who genuinely cannot get started and needs gamification to build the habit. Even then, one month ($30), then move to Stat 110. Note also that Brilliant's own marketing leans on the "quantitative finance" association (it has historically had a QF-branded track); be sceptical — that's positioning, not curriculum depth.

### Khan Academy — **too basic for this purpose, but free and fine for what it is**

- AP Statistics: https://www.khanacademy.org/math/ap-statistics

Khan's own scoping confirms the level: the course "is focused on just the topics that are in the [AP] course and exam description," and there's a separate "Get ready for AP Statistics" for prerequisites. That is US high-school level.

**Verdict: skip for quant preparation.** `[judgement]` Legitimate uses: (1) you never did calculus-based probability and need to patch a specific mechanical gap (combinatorics, basic conditional probability, reading a normal table); (2) you're rusty on integration/series and want a fast refresher before Stat 110. Do not build a study plan around it. It is free, so the cost of dipping in is only time — but it is aimed at a completely different audience.

---

## 2. Statistics / Inference

This is where most candidates are actually weak, and it's where interviews increasingly probe. `[judgement]` Probability is well-trodden ground for applicants; *inference* — estimators, bias/variance, MLE properties, hypothesis testing done properly, what a p-value is not — separates people.

### MIT 18.650 Statistics for Applications — Philippe Rigollet ⭐ top pick

- OCW course: https://ocw.mit.edu/courses/18-650-statistics-for-applications-fall-2016
- Lecture videos: https://ocw.mit.edu/courses/18-650-statistics-for-applications-fall-2016/video_galleries/lecture-videos/
- Full download bundle: https://ocw.mit.edu/courses/18-650-statistics-for-applications-fall-2016/download/
- Archive.org mirror: https://archive.org/details/MIT18.650F16

MIT's description: "an **in-depth exploration of the theoretical foundations** for statistical methods that are useful in many applications. The goal is to understand the role of mathematics in the research and development of efficient statistical methods." Includes lecture notes, videos and problem sets. (Lecture 1 was re-recorded Fall 2017; the rest are Fall 2016.)

**Rigour:** high — this is a maths-department statistics course. Asymptotics, delta method, MLE and its asymptotic normality, Fisher information, method of moments, hypothesis testing, GLMs, PCA, regression. `[judgement]` **This is the single best free statistics course for a quant candidate.** Rigollet teaches you *why* estimators behave as they do, which is exactly what a QR interviewer probes when they ask "your estimator is biased — how much, and does it matter?"

**Free vs paid:** entirely free on OCW. There is also a paid MITx MicroMasters equivalent (18.6501x) — same reasoning as above: **don't pay.**

### "All of Statistics" (Wasserman) + CMU 36-705 ⭐ the reference pairing

- Free lecture notes for CMU 36-705 Intermediate Statistics (Wasserman's own course, ~27 sets of notes, publicly posted): https://www.stat.cmu.edu/~larry/=stat705
- Book PDF hosted on a CMU course page: https://www.stat.cmu.edu/~brian/valerie/617-2022/0%20-%20books/2004%20-%20wasserman%20-%20all%20of%20statistics.pdf (note: this is a course-page copy, not an author-authorised free release — the book is a paid Springer title)
- Self-study notes + solutions: https://github.com/telmo-correa/all-of-statistics
- More solutions: https://github.com/sajad13901/Statistics_Wasserman

The 36-705 course "covers Chapters 1–12 of *All of Statistics* plus supplementary material" and the notes are freely available.

**Genuinely good for:** *All of Statistics* is the density-optimal reference — probability, inference, and a fast tour of statistical learning in ~440 pages. **`[judgement]` It is a terrible first textbook and an excellent second one.** It compresses to the point of being a lookup table; if you learn from it cold you will "cover" MLE without understanding it. The right use is: learn from Rigollet or a proper course, then keep Wasserman as the thing you reread the week before interviews. The GitHub solution repos matter a lot — the book's exercises are good but unsolved without them.

`[judgement]` Companion **exercise solutions being community-maintained on GitHub rather than official** is a real limitation: quality varies, and some solutions are wrong. Use two repos and cross-check.

### Stanford STATS 200 — Introduction to Statistical Inference

- Archived lecture PDFs: https://web.stanford.edu/class/archive/stats/stats200/stats200.1172/Lecture01.pdf (Lectures 01–29 follow the same URL pattern)
- Current lecture index: https://web.stanford.edu/class/stats200/lectures.html
- Art Owen's version of the course: https://artowen.su.domains/courses/200/
- A syllabus (Sabatti, W2018): https://chiarasabatti.su.domains/Stat200/syllabus.pdf

Follows **Rice, *Mathematical Statistics and Data Analysis*** as the primary text with **Wasserman as supplementary**. Slides/notes are posted publicly; **problem sets are on Canvas and not publicly available.**

**Verdict:** `[judgement]` Good *notes*, but a weak *course* for a self-studier precisely because the problem sets are gated. Rigour is comparable to 18.650. Use as a second reference or a different explanation of the same material, not as your spine. If you want a Stanford-flavoured treatment, Rice's textbook (paid) is the real object here.

### StatQuest (Josh Starmer) — YouTube

- https://www.youtube.com/@statquest
- Code: https://github.com/StatQuest
- Paid extras (books, "Study Guides"): https://statquest.gumroad.com/

Starmer's own positioning: "I don't dumb down the material. Instead, I build up your understanding so that you are smarter." He's described in press coverage as "the Bill Nye of Statistics."

**Note: I could not find documented substantive criticism** — searches for critiques returned only positive/promotional coverage, and the relevant communities (r/statistics) were unreachable. So the following is `[judgement]`:

**Genuinely good for:** unsticking yourself on one specific concept in 15 minutes. His videos on bias-variance, ROC/AUC, PCA, regularisation, and random forests are the best "explain it once, clearly" content available. The step-by-step arithmetic walkthroughs are genuinely useful the first time you meet a method.

**Where it falls short:** StatQuest is **intuition delivery, not training.** There are no problem sets, no proofs, no asymptotics, and nothing that forces you to produce anything. Watching 40 StatQuest videos produces the *feeling* of understanding statistics and none of the ability. It is also pitched at the data-science audience, so it under-serves exactly the inference material (estimator properties, testing theory) a QR interview leans on.

**Verdict:** use it as a *supplement*, in "I am stuck on X" mode. Never as a spine. **`[judgement]` Zero hours of dedicated StatQuest time; unlimited on-demand time.**

### Seeing Theory (Brown)

- https://seeing-theory.brown.edu/
- Source: https://github.com/seeingtheory/Seeing-Theory

Built by Daniel Kunin as a Brown undergraduate, released 2017, D3.js interactive visualisations, six chapters from basic probability through regression. Won a Webby. **Important:** it is **no longer maintained** — Brown will keep hosting it but the code won't be updated.

**Verdict:** `[judgement]` Genuinely delightful and genuinely small. Total content is maybe two hours. The distributions and CLT visualisations are worth seeing once; the regression chapter is superficial. **Spend one evening on it, early, then never return.** It is intuition scaffolding, not a course, and it does not pretend otherwise. No cost, no downside — just don't confuse "I saw the CLT animate" with "I can state and use the CLT."

---

## 3. Regression / Econometrics

`[judgement]` **This section matters more for quant research than most candidates think, and in a specific way.** A QR job is overwhelmingly "fit a linear model to noisy, non-stationary, heteroskedastic, autocorrelated financial data and don't fool yourself." That is econometrics, not machine learning. Interview evidence backs this: "Regression shows up in nearly every quant and data interview because it's the workhorse for turning features into a prediction, and because it has assumptions that are easy to state and easy to violate" (https://www.techinterview.org/post/3233477272/statistics-questions-quant-data-science-interviews/).

The important caveat: **causal inference is not the quant's central problem.** Quants are mostly doing *prediction under distribution shift*, not policy evaluation. The causal-inference literature is fashionable and partially relevant (it teaches you rigour about confounding, selection, and what a regression coefficient means), but you can over-invest in it. `[judgement]`

### Bruce Hansen's textbooks ⭐ top pick

- **Probability and Statistics for Economists** (Vol. 1, 2022): https://www.ssc.wisc.edu/~bhansen/probability/ — PDF: https://www.ssc.wisc.edu/~bhansen/probability/Probability.pdf
- **Econometrics** (Vol. 2, 2022, Princeton UP): https://www.ssc.wisc.edu/~bhansen/econometrics/ — PDF: https://www.ssc.wisc.edu/~bhansen/econometrics/Econometrics.pdf
- Hansen's PhD courses ECON 709 / 710 with problem sets: https://users.ssc.wisc.edu/~behansen/709/Econ709.htm and https://users.ssc.wisc.edu/~bhansen/710/

These are the two volumes of a **one-year PhD econometrics sequence**, published by Princeton UP (hardcover $108) but with **author-authorised free PDFs** — "may be printed and reproduced for individual or instructional use, but may not be printed for commercial purposes."

**Rigour:** the highest on this list for regression. Proper asymptotic theory for OLS, heteroskedasticity-robust and clustered inference, the bootstrap, GMM, instrumental variables, quantile regression, nonparametrics. `[judgement]` **If you only read one econometrics source as a quant, read Hansen's Chapters on OLS asymptotics, robust standard errors, and the bootstrap.** That trio is what actually protects you from publishing a spurious signal.

**Honest caveat:** it's a PhD text and reads like one. Do not start here if your regression is rusty — start with Stock & Watson-level material (see the free R book below) and come to Hansen for the theory. Note there is no official solutions manual, and an EJMR thread confirms people go looking for one and don't find it (https://www.econjobrumors.com/topic/solutions-to-hansens-notes) — the ECON 709/710 course pages are the best source of problem sets.

### "Introduction to Econometrics with R" (Hanck, Arnold, Gerber, Schmelzer) ⭐ best free on-ramp

- https://www.econometrics-with-r.org/
- PDF: https://www2.cirano.qc.ca/~dufourj/Web_Site/ResE/ECON257_2026W/Hanck_etal_2024_Introduction_to_Econometrics_with_R.pdf
- Announcement / open-textbook listing: https://openeconomics.zbw.eu/en/2024/05/open-textbook-introduction-to-econometrics-with-r/

An **interactive free companion to Stock & Watson's *Introduction to Econometrics***, built with bookdown, fully reproducible, from the Chair of Econometrics at Duisburg-Essen. Used in university courses worldwide.

**Verdict:** `[judgement]` **The best free way to actually get regression into your hands.** Stock & Watson is the standard undergrad text but costs money; this book reproduces its empirical applications in R with runnable code and interactive exercises for free. Level is undergraduate — heteroskedasticity, panel data, IV, time series basics — which per G-Research's own guidance is the level required. If you're an R user this is a straight yes. If you're a Python shop, the concepts transfer but you'll be translating.

### "Mostly Harmless Econometrics" (Angrist & Pischke)

- Not free. MIT 14.32 (Angrist's undergrad econometrics course) **is** free on OCW: https://ocw.mit.edu/courses/14-32-econometrics-spring-2007/ — with syllabus (https://ocw.mit.edu/courses/14-32-econometrics-spring-2007/pages/syllabus/), assignments and data (https://ocw.mit.edu/courses/14-32-econometrics-spring-2007/pages/assignments/), and full download (https://ocw.mit.edu/courses/14-32-econometrics-spring-2007/download/).
- Angrist's graduate applied course, **14.387 "Applied Econometrics: Mostly Harmless Big Data"** (with Chernozhukov), is also on OCW and is the closer companion to the book.

External assessment found: MHE "presupposes statistical confidence" and is characterised as "a bit [more] demanding [than The Mixtape]" and **"also described as outdated."**

**Verdict:** `[judgement]` MHE is a genuinely great book that changed how a generation thinks about identification — and it is **not the right use of a quant candidate's time**. Its whole subject is treatment-effect estimation from observational data in labour/policy settings. Quants rarely have a treatment. Read the regression chapter (Ch. 3) for the "regression anatomy" formula and the discussion of what a coefficient means when the model is misspecified — that's genuinely useful — and skip the rest unless you're interested for its own sake. **MIT 14.32 (free, Angrist teaching, real problem sets with CPS/NBA/wine data) is better value than the book** if you want the same worldview at undergrad level.

### "Causal Inference: The Mixtape" (Scott Cunningham)

- Free online: https://mixtape.scunning.com/ (e.g. Ch. 1: https://mixtape.scunning.com/01-introduction)
- Gelman's blog discussion: https://statmodeling.stat.columbia.edu/2021/05/25/causal-inference-the-mixtape/

Positioned between Mastering Metrics and MHE in difficulty. Free online version exists and is "useful to do quick searches and copy some of the provided code."

**Verdict:** `[judgement]` Well-written, free, code in R/Stata/Python, good on DAGs, matching, DiD, RD, synthetic control. **Peripheral for quant research.** Its value to you is conceptual hygiene — understanding selection bias and why a regression coefficient isn't automatically causal — not the specific methods, most of which you will never run on price data. **If you're econ-curious, read it. If you're time-constrained, skip it entirely** and put those hours into Hansen's asymptotics chapters or time series.

### "The Effect" (Nick Huntington-Klein) — free, and the better first causal book

- Free in its entirety: https://theeffectbook.net/ and https://nickchk.com/causalitybook.html
- 2nd ed. review in *Technometrics*: https://www.tandfonline.com/doi/full/10.1080/00401706.2026.2652818

"Assumes almost nothing, as it was written explicitly for undergraduates and for social scientists in adjacent disciplines without needing a graduate econometrics sequence as a prerequisite." Heavy on DAGs and data-generating processes; Part II covers regression, matching, fixed effects, DiD, IV, RD. Code in **R, Python and Stata**.

**Verdict:** `[judgement]` If you're going to read one causal-inference book, read this rather than the Mixtape or MHE — free, clearer, and the Python code makes it usable without learning R. Still peripheral to the quant job; still worth 10 hours for the DAG-thinking alone.

### Wooldridge

Not free (Cengage). *Introductory Econometrics: A Modern Approach* is the standard undergrad text; *Econometric Analysis of Cross Section and Panel Data* is the graduate one. `[judgement]` **Verdict: no reason to buy it** given Hansen (free, more rigorous) and the free R book (free, same undergrad level, with code). Wooldridge's edge is exposition and exercise quality; if you already own it, fine. Don't spend money.

---

## 4. Time Series

`[judgement]` This is the topic where the standard free resources are **weakest relative to what a quant actually needs**, and you should know that going in. The best free material is oriented toward *business forecasting* (monthly sales, tourism, electricity demand) — signals with strong trend and seasonality. Financial returns have neither. They have near-zero autocorrelation in the mean, enormous autocorrelation in the *variance*, fat tails, and regime changes. G-Research explicitly names time series analysis as a review topic, so it matters — but you will need to bridge from the free material to the financial case yourself.

### "Forecasting: Principles and Practice" (Hyndman & Athanasopoulos) — fpp3

- **3rd edition, free online:** https://otexts.com/fpp3/
- 2nd ed (still up): https://otexts.com/fpp2/
- R package with all data: https://pkg.robjhyndman.com/fpp3/ , https://github.com/robjhyndman/fpp3 , CRAN: https://cran.r-project.org/web/packages/fpp3/fpp3.pdf
- Community exercise solutions: https://github.com/pedroafleite/fpp3
- Hyndman's own video/course notes: https://robjhyndman.com/uwafiles/fpp-notes.pdf and https://robjhyndman.com/hyndsight/fpp-video/

3rd edition (2021), all chapters updated, new chapter on time series features. Freely available at otexts.com/fpp3.

**Genuinely good for:** the best free, most professionally maintained time series resource in existence. Decomposition, exponential smoothing/ETS, ARIMA done properly, dynamic regression, hierarchical/grouped reconciliation, feature-based forecasting, and — crucially — **a genuinely rigorous treatment of evaluation: train/test splits for time series, time series cross-validation, and why in-sample fit lies.** That evaluation discipline transfers *completely* to quant work and is the highest-value part of the book for you.

**Honest limitations for quant use** `[judgement]`: it is an R/tidyverts book (fable, tsibble) — you'll be learning a specific R ecosystem. It has **essentially no GARCH / volatility modelling, no cointegration, no high-frequency or irregularly-spaced data, no multivariate VAR depth.** Its running examples are seasonal business series. If you work through fpp3 and stop, you will be well-equipped to forecast Australian tourism and poorly equipped to model a return series. (I searched specifically for published criticism on this point and found none — the finding is absence of critique, so treat this as my assessment rather than a sourced claim.)

**Verdict: yes, do it — chapters 2–3, 5 (evaluation), 8 (ETS), 9 (ARIMA), 10 (dynamic regression), 12–13.** Then bridge to financial time series via Tsay.

### Rob Hyndman's blog (Hyndsight)

- https://robjhyndman.com/hyndsight/
- Forecasting category: https://robjhyndman.com/categories/forecasting/
- His annotated list of forecasting/time series books: https://robjhyndman.com/hyndsight/forecasting-and-time-series-books/index.html
- Other forecasting blogs he rates: https://robjhyndman.com/hyndsight/seven-forecasting-blogs/
- Practitioner help page: https://robjhyndman.com/hyndsight/forecasting-help/

**Verdict:** `[judgement]` Free, high-signal, and the *right* kind of blog — a leading academic writing plainly about methodological mistakes practitioners make. Not a course; don't try to "study" it. The book-recommendations post and the "help for practitioners" page are the two highest-value entry points. Read opportunistically.

### Ruey Tsay — *Analysis of Financial Time Series* and course materials

- Booth faculty pages with **data sets and program commands** for the book: https://faculty.chicagobooth.edu/ruey-s-tsay/research/analysis-of-financial-time-series and 3rd ed: https://faculty.chicagobooth.edu/ruey-s-tsay/research/analysis-of-financial-time-series-3rd-edition

**Important correction to a common assumption:** Tsay's site hosts **data and code**, not free lecture notes or a free textbook. The book itself is a paid Wiley title (3rd ed., 2010). Software used is SCA, RATS, S-Plus and R. (PDFs circulating on university and personal sites are not author-authorised — e.g. https://cpb-us-w2.wpmucdn.com/blog.nus.edu.sg/dist/0/6796/files/2017/03/analysis-of-financial-time-series-copy-2ffgm3v.pdf — use at your own judgement.)

**Verdict:** `[judgement]` **This is the book that fills the fpp3 gap** — ARCH/GARCH and its whole family, stochastic volatility, extreme values and VaR, multivariate volatility, high-frequency data, cointegration. For a quant it is more relevant than Hyndman, but it is (a) not free and (b) a harder read. The realistic plan: fpp3 free for the foundation and evaluation discipline, then buy/borrow Tsay for the financial-specific chapters (3 on volatility, 5 on high-frequency, 7 on extreme values, 8 on multivariate). Tsay also ran a Coursera specialisation on financial time series in past years; check current availability — I could not verify it is still running.

---

## 5. Machine Learning / Statistical Learning

**The framing that matters:** for quant research, ML means *regularised regression, tree ensembles, cross-validation, and not overfitting.* It does not mean transformers. The Headlands (quant firm) review of ESL is explicit that the useful core is small.

### ESL — *The Elements of Statistical Learning* ⭐ (with a big caveat)

- **Official free PDF** (Springer has agreed to keep it on the web): https://hastie.su.domains/ElemStatLearn/ , download page https://hastie.su.domains/ElemStatLearn/download.html , direct 12th printing: https://hastie.su.domains/ElemStatLearn/printings/ESLII_print12_toc.pdf

*(Note: a common claim that "ESL isn't free" is wrong — it is officially free, with Springer's consent.)*

**The best practitioner verdict available**, from Headlands Technologies, a quant trading firm, in their book-recommendations-for-new-quants series (https://blog.headlandstech.com/2022/02/16/elements-of-statistical-learning-8-10/):

> - "**Chapters 1, 2, 3, and 7 are great**" and constitute "one of the best foundations for building empirical models from data."
> - "The framing of the model-building problem in ESL ... fits the trading domain better than other common entry points into statistical learning."
> - But it is "a massive tome with **many sections that aren't particularly useful**, reflecting older techniques, the authors' personal research agendas, or things not applicable to the trading domain."
> - "A major problem with ESL is that it **mostly misses the practicalities of building models** — not touching on developing fast or robust software, processes that minimize divergence between training and inference, or modular data cleaning and featurization pipelines."

They score it **8/10**.

**Verdict:** `[judgement]` **Read Chapters 2, 3 and 7 carefully. That is the assignment.** Ch. 3 (linear methods for regression — subset selection, ridge, lasso, PCR/PLS) and Ch. 7 (model assessment and selection — bias-variance, optimism of training error, cross-validation done right, bootstrap) are the two chapters that most directly describe a quant researcher's daily job. Then add Ch. 9/10/15 (trees, boosting, random forests) if you'll use ensembles. Do not read it cover to cover; it's a reference. G-Research explicitly names ESL for ML-focused roles.

### ISLR / ISLP — *An Introduction to Statistical Learning* ⭐ best starting point

- Site with free PDFs (R and Python editions): https://www.statlearning.com/
- Online courses page: https://www.statlearning.com/online-courses
- Free edX course (R): https://www.edx.org/learn/statistics/stanford-university-statistical-learning — Stanford Online listing: https://online.stanford.edu/courses/sohs-ystatslearning-statistical-learning-r
- Free edX course (Python): https://www.edx.org/learn/python/stanford-university-statistical-learning-with-python — https://online.stanford.edu/courses/sohs-ystatslearningp-statistical-learning-python
- ISLP (Python ed., 2023) publisher page: https://link.springer.com/book/10.1007/978-3-031-38747-0
- An independent review of the Stanford course: https://www.lucasallen.io/statistical-learning-stanford-online-review/

ISLR 1st ed. 2013, 2nd ed. 2021, ISLP 2023 (same material, Python labs). **Free companion courses on edX for both**, R version taken by 290,000+ learners. Courses may be audited free; certificates are paid.

**Verdict:** `[judgement]` **The right entry point, and the only "MOOC" on this list I'd endorse without hedging** — because it's taught by Hastie and Tibshirani themselves, it's free to audit, and the book is officially free. ISLR is "technically the introductory book to ESL"; it covers the same territory with the maths removed. Read ISLR/ISLP first (fast — it's designed to be read through), then use ESL Ch. 2/3/7 to get the theory underneath. Choose **ISLP if you work in Python**, which most quant shops do.

**Free vs paid:** everything you need is free. The verified certificate is not worth paying for. `[judgement]`

### Andrew Ng's courses

- Machine Learning Specialization (DeepLearning.AI + Stanford Online, on Coursera): https://www.deeplearning.ai/courses/machine-learning-specialization/ , https://www.coursera.org/specializations/machine-learning-introduction

Marketed as "**beginner-friendly**", "designed so you can gain a deep understanding of how machine learning works **without needing a heavy math background** or deep coding experience."

**Verdict:** `[judgement]` **Mostly noise for a quant candidate — this is the MOOC-marketing case you should be most sceptical of.** Ng's original 2011 ML course was genuinely important and is why the brand carries weight; the current Specialization is deliberately pitched *below* the level you need, and its "no heavy math" selling point is precisely the wrong feature for someone who needs the maths. Its content (linear regression, logistic regression, small neural nets, decision trees, clustering) is a strict subset of ISLR, taught less rigorously, and it's audit-free-but-nudge-you-to-pay on Coursera. **If you've done ISLR, Ng adds nothing.** The Deep Learning Specialization is a competent DL intro but DL is peripheral to most QR work.

Where he *does* earn time: `[judgement]` the practical "ML strategy" material (error analysis, how to diagnose whether you have a bias or variance problem, how to set up dev/test splits) in the DL Specialization's Course 3 is genuinely good and rarely taught elsewhere. That's maybe five hours of value.

### fast.ai — *Practical Deep Learning for Coders*

- https://course.fast.ai/ , https://www.fast.ai/posts/2022-07-21-dl-coders-22.html

Top-down: "you build state-of-the-art models in the first lesson and gradually understand the theory behind them." Free, including the 600-page book. Independently noted that "this top-down methodology is polarizing — some students love it, others feel lost", and it is contrasted as "fast.ai is top-down and practical; Ng is bottom-up and theoretical." It does cover tabular data alongside vision and NLP.

**Verdict:** `[judgement]` **Noise for a quant candidate.** Excellent course, wrong course. It optimises for getting a working deep-learning model quickly on images/text; quant research optimises for statistical validity on low-signal-to-noise tabular data where deep learning usually loses to gradient boosting. Do it if you're joining a team doing deep learning on alternative data (NLP on filings, imagery). Otherwise put the hours into ESL Ch. 7 and Hansen.

### Financial-ML specifics: López de Prado

- *Advances in Financial Machine Learning* (Wiley, paid): https://www.wiley.com/en-us/Advances+in+Financial+Machine+Learning-p-9781119482086 ; Ch. 1 free on SSRN: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3104847
- Good free study notes: https://reasonabledeviations.com/notes/adv_fin_ml/

Reviewers note LdP is himself anti-hype — "machine learning **amplifies** your understanding, it doesn't create it" — and the field's real hard problem is stated as "in finance, the hardest problem is not prediction, it's validation." At least one practitioner review concludes "HRP portfolios don't seem to be the panacea that Lopez de Prado implies."

**Verdict:** `[judgement]` The *ideas* — purged/embargoed cross-validation, the deflated Sharpe ratio, backtest overfitting, meta-labelling, sample weighting by uniqueness — are genuinely important and are the things that distinguish someone who understands financial ML from someone who doesn't. The *specific recipes* (triple-barrier labelling, fractional differentiation, HRP) are contested and shouldn't be treated as settled practice. Read the free Ch. 1 and the reasonabledeviations notes; buy the book only if you're going into systematic strategy research.

---

## 6. Financial-Specific: Microstructure, Trading, Portfolio Theory

### Market microstructure — Joel Hasbrouck (NYU Stern) ⭐ the free gem

- **Empirical Market Microstructure** — teaching notes from a one-semester PhD course (Fall 2003), free: https://pages.stern.nyu.edu/~jhasbrou/EMM%20Book/EMM%20Home.htm , intro sample: https://pages.stern.nyu.edu/~jhasbrou/EMM%20Book/Sample%20material/Introduction.pdf
- **Securities Trading: Principles and Procedures (STPP)** — full free draft manuscript, still actively updated (current draft dated 13 December 2025): https://pages.stern.nyu.edu/~jhasbrou/STPP/STPPindex.html , e.g. https://pages.stern.nyu.edu/~jhasbrou/STPP/drafts/STPPms13c.pdf
- Faculty page (root of everything): https://pages.stern.nyu.edu/~jhasbrou/
- The Microstructure Exchange talk (free video): https://www.youtube.com/watch?v=lABdveHMHTk

STPP "grew out of teaching notes for an undergraduate microstructure course, covering basic trading mechanisms (limit order books, auctions, dealer markets)." EMM covers "empirical approaches to market microstructure, the theory that motivated them, and time series analysis."

**Verdict:** `[judgement]` **This is the single best free resource in the financial-specific category and almost nobody uses it.** Hasbrouck is a founder of the empirical microstructure field, the material is free and author-maintained, and STPP in particular explains *how markets actually work mechanically* — order types, matching, auctions, dealer inventory — which is exactly the knowledge gap that gets candidates caught out in market-making interviews. EMM is harder (VAR models of trades and quotes, Hasbrouck information shares, Roll's model) and directly relevant if you're going into execution or HFT research. **Strong recommend.**

The standard theory complement is **O'Hara, *Market Microstructure Theory*** (1995, Blackwell) — paid, and the canonical reference for the economic theory (Glosten-Milgrom, Kyle).

### Portfolio theory — MIT 15.401 Finance Theory I (Andrew Lo)

- OCW: https://ocw.mit.edu/courses/15-401-finance-theory-i-fall-2008/
- Video lectures + slides: https://ocw.mit.edu/courses/15-401-finance-theory-i-fall-2008/pages/video-lectures-and-slides/
- YouTube playlist: https://www.youtube.com/playlist?list=PLUl4u3cNGP63B2lDhyKOsImI7FjCf6eDW
- Archive.org: https://archive.org/details/MIT15.401F08
- Lo's teaching page: https://alo.mit.edu/teaching/

Covers valuation of stocks/bonds/forwards/futures/options, and section (C): "portfolio theory, mean-variance optimization, and the Capital Asset Pricing Model." Free under CC BY-NC-SA. Taught by Andrew Lo.

**Verdict:** `[judgement]` **Free, taught by a genuinely serious person, and it covers exactly what G-Research names as a review topic (portfolio optimization).** Level is MBA/advanced-undergrad, not research-grade, and the lectures are from 2008 — but mean-variance optimisation, the efficient frontier, CAPM and APT have not changed. If you come from a maths/physics background with no finance, **this is the most efficient way to acquire the vocabulary.** ~20 hours. Do the portfolio theory and CAPM/APT lectures at minimum.

### Quantopian Lecture Series — **still available, verified**

**Confirmed via GitHub API on 2026-09-06:** `quantopian/research_public` **still exists, is not archived, has 2,868 stars / 1,723 forks, and was touched as recently as 2026-09-06.**

- Original repo: https://github.com/quantopian/research_public — lectures live at https://github.com/quantopian/research_public/tree/master/notebooks/lectures
- **"Quantopian Lectures Saved"** — a curated gist archiving **55 notebook-based lessons** with summaries, links to originals, ports to other platforms, and embedded videos: https://gist.github.com/ih2502mk/50d8f7feb614c8676383431b056f4291
- **The maintained modern fork** — `quantrocket-codeload/quant-finance-lectures`: "Learn quantitative finance with this comprehensive lecture series. Adapted from the Quantopian Lecture Series. **Uses free sample data.**" 680 stars, **last updated 2026-09-06** — https://github.com/quantrocket-codeload/quant-finance-lectures
- Python-3 / yfinance community rewrite: https://github.com/v3natio/quantopian_lectures
- Offline 2020 port: https://github.com/0xrushi/quantopian-offline-2020

**Verdict:** `[judgement]` **Yes — and use the QuantRocket adaptation, not the original.** The original notebooks are excellent pedagogically (spurious correlations, multiple comparisons / p-hacking in strategy search, stationarity, pairs trading and cointegration, factor risk models, Kalman filters, position concentration risk) but they call Quantopian's dead proprietary `get_pricing()` API, so they won't run. The QuantRocket version is actively maintained and uses free sample data, so it actually executes. The *statistical-pitfalls* lectures — especially on multiple comparisons and p-hacking in backtests — are among the best free treatments of the specific way quant research goes wrong. Strong recommend, and it's the closest thing to "what a junior quant researcher's first month looks like" that exists for free.

### QuantConnect Boot Camp

- Learning hub: https://www.quantconnect.com/learning/
- Announcement: https://www.quantconnect.com/announcements/15528/get-started-with-quantconnect-s-boot-camp/
- YouTube playlist: https://www.youtube.com/playlist?list=PLD7-B3LE6mz5jsEb127kdyJVMJrBNfbmI
- Also mirrored as a free Udemy course: https://www.udemy.com/course/quantconnect-boot-camp-in-python/ (Class Central listing: https://www.classcentral.com/course/udemy-quantconnect-boot-camp-in-python-36197)

Official description: "learn the tools for quantitative trading, building skills in finance, statistics, and software development **while learning about QuantConnect's API** with code-along tasks." Free tier includes years of data. A 2026 review calls QC "the strongest single platform for retail-to-small-fund use."

**Verdict:** `[judgement]` **Useful, but understand what it is: platform training, not education.** It teaches you the QuantConnect LEAN API — how to schedule, how universes work, how data flows — with light finance and statistics wrapped around it. The genuine value for a candidate is *engineering* value: it forces you to confront look-ahead bias, survivorship bias, slippage and transaction costs in a system that won't let you cheat, which is a real skill and hard to learn from books. The genuine limitation is that none of the QC-specific API knowledge transfers to a job. **Worth ~15 hours if you have no backtesting experience; skip if you've built your own.** Free, so the only cost is time.

### Hudson & Thames

**Verified via GitHub API:** `hudson-and-thames/mlfinlab` — 4,919 stars, 1,285 forks, actively updated (2026-09-06). Also `arbitragelab` (694 stars), `portfoliolab` (186), `meta-labeling` (104), `backtest_tutorial` (159), `definitive_guide_to_pairs_trading`, `guide_to_modern_portfolio_optimization`.

- Org: https://github.com/hudson-and-thames — site: https://hudsonthames.org/ — research blog: https://hudsonthames.org/research/
- Their own account of the business-model change: https://hudsonthames.org/10-learnings-from-open-source/

**Key fact, from their own writing:** they "**pivoted towards an open-core business model and away from their original dreams of pure open source**" because the team "couldn't support a team of 6, journal subscriptions, data, 3rd party services, a full-time employee, and bills that totalled over £20,000 on less than $2000 a month." Users now "receive the MlFinLab Client documentation **after their purchase is successful**."

**Verdict:** `[judgement]` **Peripheral, and be clear-eyed about it.** MlFinLab is essentially an implementation of López de Prado's book plus related papers; the historical criticism in the quant community — which I **could not verify through accessible sources** and therefore flag as recollection rather than citation — centred on code-quality/correctness concerns and on the pivot to paid access for a library that had been built on community goodwill. What is verifiable is that it *is* now paid for the current versions.

For a candidate: the **free blog posts and the public tutorial repos** (`backtest_tutorial`, `meta-labeling`, `arbitrage_research`) are worth browsing for ideas. **Do not spend money on the library, and do not treat "I used MlFinLab" as a credential** — implementing purged cross-validation or triple-barrier labelling yourself, from the paper, is far more impressive in an interview than importing it.

---

## 7. Visual / Intuition Builders

These are all free and all small. `[judgement]` Their correct total budget is **under 20 hours combined**, spent *early* (before the hard courses) or *tactically* (when stuck). The failure mode is spending 80 hours here and feeling educated.

### 3Blue1Brown

- Essence of Linear Algebra: https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab
- Channel: https://www.youtube.com/c/3blue1brown

The Essence of Linear Algebra series "provides viewers with intuition behind linear algebra, though **there are still many computations viewers need to do to truly master the subject**."

**Verdict:** `[judgement]` **Do watch Essence of Linear Algebra — it is 3 hours and it is the best 3 hours of maths video ever made.** Determinants as volume scaling, change of basis, eigenvectors as invariant directions: these become permanent intuitions and they matter constantly in quant work (PCA, covariance matrices, factor models). The Bayes/probability videos are also excellent.

**But:** it is explicitly a *complement* to computation, not a replacement. Watching it does not let you invert a matrix, diagonalise one, or reason about the conditioning of a covariance estimate. Pair it with **Strang's MIT 18.06** (https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/) — repeatedly named in quant reading lists as the linear algebra course — where you actually do the problems. **3B1B for the picture, Strang for the ability.**

### Seeing Theory

Covered in §2. One evening. Free. Unmaintained. https://seeing-theory.brown.edu/

### Distill.pub — **dead, but the archive is still worth it**

- Hiatus announcement: https://distill.pub/2021/distill-hiatus/ (HN discussion, which I could not read: https://news.ycombinator.com/item?id=27718054)
- Wikipedia: https://en.wikipedia.org/wiki/Distill_(journal)

Announced in 2021 "a **one year hiatus** ... **which may be extended indefinitely**"; after four years the team "no longer believed their original theory of impact" and it "was not sustainable to continue running the journal in its current form." It ceased operations "largely due to burnout" and **no longer accepts submissions**. The archive remains accessible and the template remains open source.

**Verdict:** `[judgement]` Not a learning path — a set of exceptional individual articles, now frozen in 2021 and therefore missing everything since. **Peripheral for a quant.** Its centre of gravity is deep-learning interpretability (feature visualisation, circuits, attention), which is not the quant's problem. The genuinely broadly useful pieces are "Why Momentum Really Works", the t-SNE article ("How to Use t-SNE Effectively"), and the Gaussian Processes explorable. Read those three; don't budget time for the rest.

---

## 8. Summary: what to actually do

### The core path (roughly 350–450 hours, all free)

1. **Probability** — Harvard **Stat 110**: watch the lectures, read the free book at probabilitybook.net, do the problem sets with the official solutions. Supplement with **MIT 6.041SC** problem sets for volume. *(~120 h)*
2. **Statistics/inference** — **MIT 18.650 (Rigollet)** on OCW, with **Wasserman's *All of Statistics*** as the compressed reference and the GitHub solution repos. *(~90 h)*
3. **Regression** — **"Introduction to Econometrics with R"** free to get it in your hands, then **Bruce Hansen's *Econometrics*** chapters on OLS asymptotics, robust/clustered inference and the bootstrap. *(~80 h)*
4. **Statistical learning** — **ISLP** (free PDF + free Stanford edX audit), then **ESL Ch. 2, 3, 7** (free PDF), guided by the Headlands review of which chapters matter. *(~70 h)*
5. **Time series** — **fpp3** (free), prioritising the evaluation and ARIMA/ETS/dynamic-regression chapters. Then bridge to financial specifics via Tsay. *(~50 h)*
6. **Finance context** — **Hasbrouck's STPP** for microstructure (free), **MIT 15.401** portfolio theory lectures (free), **QuantRocket's Quantopian lecture adaptation** for the statistical-pitfalls notebooks (free). *(~50 h)*
7. **Alongside, opportunistically** — 3B1B Essence of Linear Algebra (3 h), Seeing Theory (2 h), StatQuest when stuck, Hyndman's blog when curious.

### Explicitly too basic — don't build a plan around these

- **Khan Academy** (AP/high-school level by its own scoping) — gap-patching only.
- **Brilliant.org** ($240/yr, stops well short of the required depth) — skip; the free alternatives are better *and* free.
- **Seeing Theory / Distill / 3B1B** — excellent, but each is a few hours of intuition, not training. Distill is additionally frozen since 2021.
- **StatQuest** — supplement, never spine. No problems, no proofs.

### Explicitly noise for a quant specifically

- **Andrew Ng's Machine Learning Specialization** — deliberately below the required level ("without needing a heavy math background"); a strict subset of ISLR. The historic reputation exceeds current value.
- **fast.ai** — great course, wrong problem domain (DL on images/text vs. low-SNR tabular).
- **Mostly Harmless Econometrics / Mixtape** beyond the basics — read the regression chapters, skip the treatment-effect machinery unless you're personally interested.
- **Paying for any certificate** (edX verified, Coursera, MicroMasters) — no quant firm hires on these. Audit everything.
- **Hudson & Thames paid libraries** — implement the papers yourself instead; it's better preparation and it's free.

### The rigour test, stated plainly

`[judgement]` A resource is rigorous enough for quant research if it makes you **derive** things and then makes you **solve problems you can get wrong**. By that test: Stat 110, 6.041, 18.600, 18.650, Hansen, ESL, 36-705 and Hasbrouck's EMM pass. fpp3, ISLR, 14.32, the econometrics-with-R book and 15.401 are appropriately rigorous *for their level* and pass conditionally. StatQuest, Seeing Theory, 3B1B, Distill, Khan and Brilliant all fail — not because they're bad, but because none of them can tell you that you're wrong.

---

## Appendix: all URLs referenced

**Probability**
- https://stat110.hsites.harvard.edu/ · https://stat110.hsites.harvard.edu/youtube · http://probabilitybook.net · https://projects.iq.harvard.edu/files/stat110/files/math_review_handout.pdf · https://www.edx.org/bio/joseph-blitzstein
- https://ocw.mit.edu/courses/6-041sc-probabilistic-systems-analysis-and-applied-probability-fall-2013/ · https://ocw.mit.edu/courses/6-041-probabilistic-systems-analysis-and-applied-probability-fall-2010/ · https://ocw.mit.edu/courses/res-6-012-introduction-to-probability-spring-2018/ · https://www.edx.org/learn/probability/massachusetts-institute-of-technology-probability-the-science-of-uncertainty-and-data · https://mitxonline.mit.edu/courses/course-v1:MITxT+6.431x/ · https://github.com/mitx-data-science/6.431x
- https://math.mit.edu/academics/undergrad/subjects/186x.html
- https://brilliant.org/ · https://www.khanacademy.org/math/ap-statistics

**Statistics**
- https://ocw.mit.edu/courses/18-650-statistics-for-applications-fall-2016 · https://ocw.mit.edu/courses/18-650-statistics-for-applications-fall-2016/video_galleries/lecture-videos/ · https://archive.org/details/MIT18.650F16
- https://www.stat.cmu.edu/~larry/=stat705 · https://github.com/telmo-correa/all-of-statistics · https://github.com/sajad13901/Statistics_Wasserman
- https://web.stanford.edu/class/stats200/lectures.html · https://artowen.su.domains/courses/200/ · https://chiarasabatti.su.domains/Stat200/syllabus.pdf
- https://www.youtube.com/@statquest · https://github.com/StatQuest · https://seeing-theory.brown.edu/ · https://github.com/seeingtheory/Seeing-Theory

**Econometrics**
- https://www.ssc.wisc.edu/~bhansen/probability/ · https://www.ssc.wisc.edu/~bhansen/econometrics/ · https://users.ssc.wisc.edu/~behansen/709/Econ709.htm · https://users.ssc.wisc.edu/~bhansen/710/
- https://www.econometrics-with-r.org/
- https://ocw.mit.edu/courses/14-32-econometrics-spring-2007/
- https://mixtape.scunning.com/ · https://statmodeling.stat.columbia.edu/2021/05/25/causal-inference-the-mixtape/
- https://theeffectbook.net/ · https://nickchk.com/causalitybook.html

**Time series**
- https://otexts.com/fpp3/ · https://otexts.com/fpp2/ · https://pkg.robjhyndman.com/fpp3/ · https://github.com/robjhyndman/fpp3 · https://github.com/pedroafleite/fpp3
- https://robjhyndman.com/hyndsight/ · https://robjhyndman.com/hyndsight/forecasting-and-time-series-books/index.html · https://robjhyndman.com/hyndsight/forecasting-help/ · https://robjhyndman.com/uwafiles/fpp-notes.pdf
- https://faculty.chicagobooth.edu/ruey-s-tsay/research/analysis-of-financial-time-series-3rd-edition

**ML / statistical learning**
- https://hastie.su.domains/ElemStatLearn/ · https://hastie.su.domains/ElemStatLearn/printings/ESLII_print12_toc.pdf
- https://www.statlearning.com/ · https://www.statlearning.com/online-courses · https://www.edx.org/learn/statistics/stanford-university-statistical-learning · https://www.edx.org/learn/python/stanford-university-statistical-learning-with-python · https://link.springer.com/book/10.1007/978-3-031-38747-0
- https://www.deeplearning.ai/courses/machine-learning-specialization/ · https://course.fast.ai/
- https://blog.headlandstech.com/2022/02/16/elements-of-statistical-learning-8-10/
- https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3104847 · https://reasonabledeviations.com/notes/adv_fin_ml/

**Finance-specific**
- https://pages.stern.nyu.edu/~jhasbrou/ · https://pages.stern.nyu.edu/~jhasbrou/STPP/STPPindex.html · https://pages.stern.nyu.edu/~jhasbrou/EMM%20Book/EMM%20Home.htm
- https://ocw.mit.edu/courses/15-401-finance-theory-i-fall-2008/ · https://www.youtube.com/playlist?list=PLUl4u3cNGP63B2lDhyKOsImI7FjCf6eDW
- https://github.com/quantopian/research_public · https://gist.github.com/ih2502mk/50d8f7feb614c8676383431b056f4291 · https://github.com/quantrocket-codeload/quant-finance-lectures
- https://www.quantconnect.com/learning/ · https://github.com/hudson-and-thames · https://hudsonthames.org/10-learnings-from-open-source/

**Visual**
- https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab · https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/ · https://distill.pub/2021/distill-hiatus/

**Practitioner / firm sources**
- https://blog.headlandstech.com/ · https://blog.headlandstech.com/author/max/ · https://blog.headlandstech.com/wp-content/uploads/2017/08/Headlands-Quant-Trading-Summary-Max-Dama.pdf
- https://www.gresearch.com/wp-content/uploads/2020/09/200630-quant-research-preparation.pdf · https://www.gresearch.com/wp-content/uploads/2025/07/Quantitative-research-and-machine-learning-interview-prep-recommended-reading.pdf · https://www.gresearch.com/career-guides/quantitative-researcher-interview-questions/
- https://www.techinterview.org/post/3233477272/statistics-questions-quant-data-science-interviews/
