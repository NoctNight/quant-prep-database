# Coding in Quant Researcher (QR) vs Quant Trader (QT) interviews — findings with sources

(Report from QR/QT research agent. Source tiers: [FH] first-hand read in full; [FH-snip] first-hand via snippet/aggregator; [OFFICIAL]; [PREP] low-confidence prep-company; [SYNTH] secondary synthesis. Tracks: INTERN / FT / GRAD.)

## 1. Cross-cutting findings

### QT: coding light, usually one screen, sometimes absent
- Berkeley guide [FH]: "Programming is not usually tested for Quant Trading roles but is commonly needed for QR interviews... HRT, Headlands, Jump almost always test programming." https://github.com/sgoel97/blog/blob/main/content/blog/quant-interview/index.md
- Blind [FH-snip]: IMC QT "not about coding at all"; "Akuna QR has a very high leetcode bar"; hedge-fund QR = LC medium/hard. https://www.teamblind.com/post/coding-for-hedge-fund-quant-researcher-interviews-k8rzhsxo ; https://www.teamblind.com/post/quant-trader-imc-trading-interview-bydk6bcq
- SIG QT 2022 GRAD [FH]: no coding at all; 14-Q/20-min probability exam then probability phone. https://github.com/Leader-board/OA-and-Interviews/blob/main/Application%20experiences/2021-22/SIG/Quantitative%20Trader%20-%202022%20Programme.md
- Optiver Amsterdam QT/QR INTERN [FH]: 80-in-8 arithmetic, Zap-N, 10 prob Qs @90s, guesstimates, card games; no coding. https://github.com/devclub-iitd/Intern-Prep-Series-25/blob/main/Interviews/optiver_tirth.md
- QT with coding = OA screen: Virtu QTA FT Codility 5Q/75min low-medium [FH]; Maverick Junior QT HackerRank 75min 2 med + 2 hard DP, Python [FH]; Tibra Junior QT 48-hr HackerRank 2 med + approximate-solution interpolation Q [FH]; Akuna QT 3-problem OA (solve 2) + 30-min math video test [FH-snip: https://quantnet.com/threads/akuna-capital-quant-trader-interview.27690/]; Da Vinci Graduate QT: implement a trading strategy in 150 min [FH-snip Glassdoor].

### QR: coding a hard gate, three forms
1. Algorithmic OA (LC-medium, 60–120min): Akuna Junior QR 3 LC-mediums (simulation greedy, greedy, memoisation), C++/Py, do 2 [FH: https://github.com/Leader-board/OA-and-Interviews/blob/main/Application%20experiences/2021-22/Akuna%20Capital/Junior%20Quantitative%20Researcher.md]; Maven QR GRAD 7 math/ML MCQ 20min + LC-easy greedy/LC-med stack/LC-med 2D-DP strict timers [FH]; Rokos GRAD Codility 90min 3 mediums (greedy, binary search, tree) [FH]; Millennium QR INTERN OA math+prob+moderate CP then DSA live [FH]; Qube 3 LC-mediums [FH-snip]; Squarepoint ~1hr easy-med implementation-skewed (command parsing, bank-transaction simulation) [PREP: https://www.techinterview.org/post/3233477270/squarepoint-interview-quant-researchers-developers/].
2. Data/stat coding: Two Sigma QR intern OA "linear interpolation + predict daily temperature" [FH-snip: https://www.1point3acres.com/interview/thread/1150944]; TS hybrid 3-hr HackerRank: 1 LC med-hard + 2 scikit-learn regressions [FH-snip]; FastPrep TS bank: Online No-Intercept Linear Regression, Test the Hypothesis, Piecewise Linear Interpolation [PREP: https://github.com/perixtar/quant-interview-oa-bank]; HRT onsite pandas/prediction round [FH-snip via https://github.com/Lazar-Ilic/Lazar/blob/main/Notes/Computer%20Science/Algorithms/Interviews%20Coding%20Rounds/Hudson%20River%20Trading.txt]; Point72 Quant Analyst OA 180min: 3 Python (2 med 1 hard) + 1 SQL [FH-snip: https://www.teamblind.com/post/interviews-at-point72-m20njwvn]; Tibra QTD 2-hr Jupyter: stock + 8 unlabeled signals, find relationships, then 40-min pair backtest [FH].
3. Take-homes: Maven 4-hr ML take-home [FH]; Millennium two-week full research pipeline [FH-snip]; Mustard Systems horse-bets CSV with CIs and stake decision [FH]; Tower HFT orderbook data project [PREP]; Man AHL hackerrank + DS homeworks [FH-snip]; G-Research homework walked through as a code review [OFFICIAL: https://www.gresearch.com/news/what-to-expect-from-a-quant-platform-software-engineering-interview/].
4. Live math-to-code: Jump QR 1hr Python simulation/pricing/data-manipulation [PREP]; Jump QR FT Oct 2022 linked list + node swap in C++ [FH-snip WSO]; Citadel QR phone 3n-people grouping EV maximisation [FH-snip: https://leetcode.com/discuss/interview-question/427705/citadel-phone-interview-quant-researcher]; Jane Street QR generalist real-world coding (I/O optimisation, mixed datasets) with complexity, not isolated algo Qs [FH-snip: https://www.wallstreetoasis.com/company/jane-street-capital/interview/quantitative-researcher-2]; Two Sigma QR FT Nov 2025: model design (Manhattan rents) -> live coding -> stats proofs (OLS, Lagrange) [FH-snip].

### Languages
Python dominant; C++ optional at HFTs. Citadel [OFFICIAL summary]: Python and C++ core, any language welcome, CoderPad. HRT: C++ for SWE/algo, Python for research. Rokos finals in Java (candidate choice): addMonths(yyyymmdd,m); tree Dump() any traversal -> recursive DFS -> iterative BFS -> iterative DFS [FH]. SQL at multistrats (Point72, Man AHL, Qube). R essentially absent.

### Difficulty/style
OAs cluster LC-medium; hards at Maverick, HRT algo-dev CodeSignal (2hr/3Q, third above LC-hard, ALL tests must pass). Time pressure is the common complaint. Live QR = translate math into code fast. Complexity expected everywhere. Rokos rejection feedback: "jumped into answers before thinking" [FH].

### What candidates get wrong (interviewer-side)
- Akuna: proceeded with candidates stronger in prob/stats AND coding; OA explicitly graded on code cleanliness/readability [FH].
- Tibra debrief: wanted predictive-power functions not correlations; deeper stats, stronger pandas, better problem decomposition [FH].
- Mustard: univariate analysis insufficient; wanted combined-attribute model + Sharpe + consistency [FH].
- Citadel official: applied coding, clean working code quickly. G-Research: walkthrough shows how you think about program structure [OFFICIAL].
- QuantNet hiring manager (relayed): many math-whiz PhDs rejected for weak SWE background [FH-snip via https://github.com/giwankim/claude-learning-plans/blob/main/opus-4.6/hft.md].

### Weighting
First-hand QT rejections all attribute failure to probability, not code (SIG, Akuna, Virtu, Rokos). [SYNTH] weights: QT ≈ prob .25 / mental math .15 / MM game .25 / coding .20 / behavioural .15; QR = research case + prob + heavy coding. https://github.com/hieptran1812/my-website/blob/main/content/blog/trading/quant-careers/the-interview-loop-round-by-round.md
HRT [PREP]: biggest wash-out reason is stats/probability, not coding.

### Take-home grading
Modelling judgement + out-of-sample honesty first, write-up clarity second, code third. "Sharpe 3.0 in-sample presented triumphantly fails." https://github.com/hieptran1812/my-website/blob/main/content/blog/trading/quant-careers/the-research-case-and-take-home-how-to-ace-it.md

## 2. Firm-by-firm table (see full agent report for detail)
- Jane Street: QT no coding; QR generalist real-world coding + complexity [FH-snip WSO]. SWE OA Codility.
- Citadel/CitSec: QR CoderPad 45–60min first round; onsite 3–5x60 + research presentation + coding; CS QR stats-on-strategy + prob + small programming assignment; QT intern "make a market on sum of three dice"; SDE intern BFS/topological sort.
- Two Sigma: QR intern OA interpolation/regression; FT model design + live coding + stats proofs.
- DE Shaw: QA/QR prob/stats test + small data analysis; tech-dev intern 80-min OA, C++ graph/OOP.
- HRT: CodeSignal 2hr/3Q OA; loop with pandas/prediction round; Python or C++; order-router take-home (one report).
- Jump: QR 1-hr Python sim/pricing; FT linked-list C++ report; intern OA 2020: "a before b" string validity, tree-cost DP.
- Optiver: intern QT/QR no coding (80-in-8, Zap-N, prob, guesstimates); QR FT take-home central [PREP].
- IMC: QT no coding; OA mental arithmetic/prob/pattern; SWE 2 HackerRank/90min.
- SIG: QT no coding, 14Q/20min prob exam; QR 1-hr Mettl 15Q prob/stats/calculus; SWE/QD 2 problems/90min.
- Point72/Cubist: QA HackerRank 180min 3 Py + 1 SQL; ~10 rounds; Cubist take-home (Thinknum, TreasuryDirect scrape, P&L); classifier metrics, live-vs-backtest diagnosis.
- Millennium: intern OA + DSA live; FT 4–5 rounds + two-week take-home; OOP live coding, generators, LASSO vs ridge.
- Qube: OA 3 LC-mediums; intern QD 2 easy-mod Q + probability; 1 DSA + 1 SQL reported.
- XTX: QR hard OA, ML+prob test + small data analysis; crypto-ops take-home one track; 3 tech interviews, ML-heavy, ~2 months.
- Man AHL: HackerRank + DS homeworks; QD Python+SQL take-home then code discussion, pair programming.
- G-Research: phone -> coding test + quiz -> technicals; homework code-review walkthrough; 16-hr take-home one role.
- Squarepoint: ~1hr easy-med implementation OA; later prob puzzles, random walks, CLT, Markov.
- Tower: 5 rounds incl. live coding, stats, math, HFT orderbook data project; QD HackerRank ~1hr Python.
- Virtu: QTA Codility 5Q/75min; phone brainteasers (clock angle). FastPrep titles: FIX Message Reconciliation, Profit Analysis, Banking Transaction Exceptions.
- Five Rings: QT math/prob OA, 3–4 math rounds, no coding round in reports.
- Akuna: QR 3 LC-med OA + 5-Q math video + CodePair prob round; QT 3-Q OA (solve 2) + 30-min math.
- Da Vinci: GRAD QT 150-min implement-a-strategy; QR 150-min evaluate/modify a given algorithm.
- Flow Traders: 75Q/10min mental math OA, negative marking, 1-yr ban; "30 Qs in 20 min Python MCQ" report; SWE HackerRank 90min.
- Maven: QR HackerRank MCQ + 3 coding + 4-hr ML take-home.
- Rokos: Codility 3 mediums; 9Q/90min proctored maths; finals prob + trading round (25 horses) + coding (addMonths, tree traversals).
- Tibra: QT 48-hr HackerRank; QTD Jupyter signals + pair backtest.
- Maverick: IQ test; HackerRank 75min 2 med + 2 hard DP, Python.

## Intern vs FT differences
Intern loops at market-makers (Optiver, SIG, Graviton, Quantbox) drop coding for math/games. Intern QR at multistrats keeps data/regression OA + DSA live, no take-homes. FT/GRAD QR is where multi-day take-homes and code-review walkthroughs appear. Intern SWE OAs are purely algorithmic.

## 3. Synthesis / prep implications
- QT: 2 weeks of timed LC-easy/medium Python is sufficient; spend the rest on probability, EV/market-making games, mental arithmetic (all first-hand QT rejections were math-side).
- QR: (a) ~150–200 timed LC-mediums (arrays/hash, two-pointer, DP, graphs, trees); (b) implement OLS/logistic, rolling stats, interpolation, Monte Carlo, simple backtests from scratch in numpy/pandas; know when exact DP beats Monte Carlo; (c) one polished end-to-end research notebook with out-of-sample discipline and six-section write-up; (d) narrate approach + complexity before typing; (e) HFT QR: C++ capable + Python data round.

Key sources read in full: https://github.com/Leader-board/OA-and-Interviews ; https://github.com/devclub-iitd/Intern-Prep-Series-25/tree/main/Interviews ; https://github.com/pushpa-kumar/placement-prep/tree/main/raw-notes ; https://github.com/Lazar-Ilic/Lazar ; https://github.com/sgoel97/blog ; https://github.com/perixtar/quant-interview-oa-bank ; https://github.com/hieptran1812/my-website
