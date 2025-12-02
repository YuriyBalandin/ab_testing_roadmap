# A/B Testing & Experimentation Roadmap

This roadmap is for analysts, data scientists, and product folks who want to go from “I know what an A/B test is” to running **trustworthy, advanced online experiments** (CUPED, sequential testing, quasi-experiments, Bayesian, etc.).

It’s organized by topics. You don’t have to go strictly top-to-bottom, but earlier sections are foundations for later ones.

---

## 0. Core References (Books & Long-Form)

**If you only read a couple of things end-to-end, start here.**

- **Book – Trustworthy Online Controlled Experiments: A Practical Guide to A/B Testing** – Ron Kohavi, Diane Tang, Ya Xu  
  <https://experimentguide.com/>
- **Book – Statistical Methods in Online A/B Testing** – Georgi Georgiev
  <https://www.abtestingstats.com/>
- **Open Guide – The Open Guide to Successful AB Testing (GrowthBook)**  
  <https://docs.growthbook.io/open-guide-to-ab-testing.v1.0.pdf>
- **Microsoft Experimentation Platform – Articles Hub**  
  <https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/>
- **Github - Experimentation Resources**  
  <https://github.com/DavisTrey/ExperimentationResources>


---

## 1. Why Experiments? Culture of A/B Testing

Understand *why* experimentation matters, how leading companies structure experimentation programs, and what an experimentation culture looks like.

**Key topics**

- Experiments as default decision-making
- “Learning over winning” mindset
- Experimentation flywheel & scaling experimentation
- Roles & responsibilities around tests

**Resources**

- Netflix – **“Netflix: A Culture of Learning”**  
  <https://netflixtechblog.com/netflix-a-culture-of-learning-394bc7d0f94c>
- Netflix – **“Experimentation is a Major Focus of Data Science across Netflix”**  
  <https://benedictxneo.medium.com/list/experimentation-40c2327e8667>
- Microsoft – **“It Takes a Flywheel to Fly: Kickstarting and Keeping the A/B Testing Momentum”**  
  <https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/it-takes-a-flywheel-to-fly-kickstarting-and-keeping-the-a-b-testing-momentum/>
- Booking.com / Lukas Vermeer – **“It takes a flywheel to fly” (talk/article)**  
  <https://medium.com/booking-product/it-takes-a-flywheel-to-fly-b79ad69a62ee>
- Statsig – **“An Introduction to A/B Testing”**  
  <https://www.statsig.com/perspectives/an-introduction-to-ab-testing>

---

## 2. Experiment Lifecycle & Metric Design

How to go from “idea” → “decision” via experiments. How to define good metrics and avoid metric traps.

**Key topics**

- Experiment lifecycle: hypothesis → design → implement → monitor → analyze → decide → learn
- Overall Evaluation Criterion (OEC) vs feature-level metrics
- Guardrail metrics (e.g., reliability, latency, safety)
- Leading vs lagging metrics, surrogate metrics
- Common metric interpretation pitfalls

**Resources**

- Microsoft – **“Patterns of Trustworthy Experimentation: Pre-Experiment Stage”**  
  <https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/patterns-of-trustworthy-experimentation-pre-experiment-stage/>
- Microsoft – **“Patterns of Trustworthy Experimentation: During-Experiment Stage”**  
  <https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/patterns-of-trustworthy-experimentation-during-experiment-stage/>
- Microsoft – **“Patterns of Trustworthy Experimentation: Post-Experiment Stage”**  
  <https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/patterns-of-trustworthy-experimentation-post-experiment-stage/>
- Paper – **“A Dirty Dozen: Twelve Common Metric Interpretation Pitfalls in Online Controlled Experiments”** (Dmitriev et al., KDD 2017)  
  <https://dl.acm.org/doi/10.1145/3097983.3098024>
- Paper – **“Data-Driven Metric Development for Online Controlled Experiments: Seven Lessons Learned”** (Deng & Shi, KDD 2016)  
  <https://www.microsoft.com/en-us/research/publication/data-driven-metric-development-online-controlled-experiments-seven-lessons-learned/>
- Paper – **“Online Experimentation with Surrogate Metrics: Guidelines and a Case Study”**  
  <https://www.researchgate.net/publication/352117572_Online_Experimentation_with_Surrogate_Metrics_Guidelines_and_a_Case_Study>

---

## 3. Statistical Foundations for A/B Tests

You should be comfortable with these before going deep into advanced topics.

**Key topics**

- Randomization, independence, sampling
- Null / alternative hypotheses, Type I & II errors
- p-values, significance level (α), power (1−β)
- Confidence intervals and their interpretation
- Basic tests: z-test, t-test, χ² test
- Bootstrap intuition & when to use it

**Resources**

- **Course – “A/B Testing” (Udacity)**  
  <https://www.udacity.com/course/ab-testing--ud257>
- **Article – “Statistical Significance in A/B Testing – a Complete Guide” (Analytics Toolkit)**  
  <https://blog.analytics-toolkit.com/2017/statistical-significance-ab-testing-complete-guide/>
- **Article – “Statistical Significance in A/B testing (Calculation, p-value…)” (Data36)**  
  <https://data36.com/statistical-significance-in-ab-testing/>
- **Article – “Confidence Intervals: A Guide for A/B Testing” (CXL)**  
  <https://cxl.com/blog/confidence-intervals/>
- **Article – “A/B Testing with Bootstrapping” (Getir)**  
  <https://medium.com/getir/bootstrapping-for-a-b-testing-893f01fa6700>
- **Intro – “Introduction to Bootstrapping in Statistics”**  
  <https://statisticsbyjim.com/hypothesis-testing/bootstrapping/>

---

## 4. Test Design, Sample Size & Stopping Rules

How to plan experiments that are feasible, interpretable, and not underpowered.

**Key topics**

- Minimum Detectable Effect (MDE) and power
- Sample size formulas for proportions & means
- Test duration vs traffic, seasonality, and business constraints
- Fixed-horizon tests vs sequential tests (peeking problem)
- A/A tests to validate implementation

**Resources**

- **Paper – All about Sample-Size Calculations for A/B Testing**  
  <https://arxiv.org/pdf/2305.16459>
- **Calculator – Statsig Sample Size Calculator**  
  <https://www.statsig.com/calculator>
- **Article – “How Not To Run an A/B Test”**  
  <https://www.evanmiller.org/how-not-to-run-an-ab-test.html>
- **Article – “A/B Testing Statistics: Why Statistics Matter in Experimentation” (Convert)**  
  <https://www.convert.com/blog/a-b-testing/decode-master-ab-testing-statistics/>
- **Report – “p-Hacking and False Discovery in A/B Testing” (Berman & Van den Bulte)**  
  <https://thearf-org-unified-admin.s3.amazonaws.com/MSI/2020/06/MSI_Report_18-130-1.pdf>

---

## 5. Ratio & Derived Metrics (CTR, ARPU, etc.)

How to correctly handle metrics like CTR, ARPU, conversion per active user, etc.

**Key topics**

- Ratios as functions of sums (delta method)
- Approximate variance and confidence intervals for ratio metrics
- When standard tests break on ratios
- Alternatives: delta method, Fieller, bootstrapping

**Resources**

- Paper – **“Applying the Delta Method in Metric Analytics: A Practical Guide with R” (Deng, 2018)**  
  <https://arxiv.org/pdf/1803.06336>
- Article – **“The Delta Method in A/B Testing”**  
  <https://www.aleksjpages.com/blog/delta-method-in-AB-testing>
- Article – **“Applying Delta Method for A/B Tests Analysis”**  
  <https://medium.com/%40ahmadnuraziz3/applying-delta-method-for-a-b-tests-analysis-8b1d13411c22>
- Datacamp snippet – **“Ratio metrics and the delta method”**  
  <https://campus.datacamp.com/courses/ab-testing-in-python/practical-considerations-and-making-decisions?ex=8>

---

## 6. Multiple Testing & False Discovery

What to do when you have many variants, many metrics, many segments.

**Key topics**

- Family-Wise Error Rate (FWER) vs False Discovery Rate (FDR)
- Bonferroni, Holm, Benjamini–Hochberg, Hochberg
- Multiple metrics and multiple slices per experiment
- Online / sequential multiple testing

**Resources**

- Article – **“Multiple Testing Corrections” (GrowthBook docs)**  
  <https://docs.growthbook.io/statistics/multiple-corrections>
- Paper – **“False Discovery in A/B Testing” (Berman & Van den Bulte)**  
  <https://ron-berman.com/papers/fdr.pdf>
- Paper – **“Online multiple hypothesis testing”**  
  <https://www.repository.cam.ac.uk/handle/1810/334657>
- Article – **“Hochberg procedure: controlling false discoveries” (Statsig)**  
  <https://www.statsig.com/perspectives/hochberg-procedure-false-discoveries>

---

## 7. Pitfalls & Data Quality: Peeking, SRM, Instrumentation

All the ways experiments can silently lie to you.

**Key topics**

- Peeking / optional stopping and inflated false positives
- Sample Ratio Mismatch (SRM): detection & root causes
- Instrumentation bugs and event tracking issues
- Metric churn, seasonality, env changes
- A/A tests and simulation as validation tools

**Resources**

- Talk/Slides – **“Trustworthy A/B Tests: Pitfalls in Online Controlled Experiments” (Kohavi)**  
  <https://exp-platform.com/Documents/2017-05-17EmetricsControlledExperimentsPitfallsKohaviNR.pdf>
- Paper – **“Seven Pitfalls to Avoid When Running Controlled Experiments on the Web”**  
  <https://dl.acm.org/doi/10.1145/1557019.1557139>
- Article – **“Diagnosing Sample Ratio Mismatch in A/B Testing” (Microsoft ExP)**  
  <https://www.microsoft.com/en-us/research/publication/diagnosing-sample-ratio-mismatch-in-ab-testing/>
- Wiki – **Sample Ratio Mismatch**  
  <https://en.wikipedia.org/wiki/Sample_ratio_mismatch>
- Tool – **SRM Checker (Lukas Vermeer)**  
  <https://www.lukasvermeer.nl/srm/microsite/>
- Article – **“A quick guide to sample ratio mismatch (SRM)” (Statsig)**  
  <https://www.statsig.com/blog/sample-ratio-mismatch>

---

## 8. Novelty, Primacy, & Network Effects (Switchback, Clustered Tests)

When the Stable Unit Treatment Value Assumption (SUTVA) breaks.

**Key topics**

- Novelty effect and primacy (short-term spikes vs long-term impact)
- Learning effects, habituation, long-term vs short-term metrics
- Interference between users (network effects, marketplaces)
- Cluster randomization (geo experiments, store-level tests)
- Switchback experiments (time-based randomization)

**Resources**

- Article – **“Novelty effects: Everything you need to know” (Statsig)**  
  <https://www.statsig.com/blog/novelty-effects>
- Paper – **“Novelty and Primacy: A Long-Term Estimator for Online Experiments”**  
  <https://arxiv.org/pdf/2102.12893>
- Article – **“Switchback experiments: Overview and considerations” (Statsig)**  
  <https://www.statsig.com/blog/switchback-experiments>
- Article – **“Switchback Tests and Randomized Experimentation under Network Effects at DoorDash”**  
  <https://careersatdoordash.com/blog/switchback-tests-and-randomized-experimentation-under-network-effects-at-doordash/>
- Paper – **“Design and Analysis of Switchback Experiments” (Bojinov et al.)**  
  <https://arxiv.org/abs/2009.00148>
- Blog – **“Introducing switchback testing: A/B testing for decision models with network effects”**  
  <https://www.nextmv.io/blog/introducing-switchback-testing-a-b-testing-for-decision-models-with-network-effects>

---

## 9. Variance Reduction (CUPED, Stratification, ML-based)

Tricks to get more power without more users.

**Key topics**

- Stratification / post-stratification
- Covariate adjustment via regression
- CUPED / CUPAC using pre-experiment data
- Combining pre-experiment and in-experiment covariates
- ML-based variance reduction (e.g., regression-adjusted treatment effect estimators)

**Resources**

- Microsoft ExP – **“Deep Dive into Variance Reduction”** (CUPED)  
  <https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/deep-dive-into-variance-reduction/>
- Statsig – **“CUPED Explained”**  
  <https://www.statsig.com/blog/cuped>
- Article – **“Understanding CUPED” (Matteo Courthoud)**  
  <https://matteocourthoud.github.io/post/cuped/>
- Spotify Confidence – **“Variance Reduction (CUPED)”**  
  <https://confidence.spotify.com/docs/stats/variance-reduction>
- Article – **“Online Experiments Tricks — Variance Reduction” (TopBots)**  
  <https://www.topbots.com/online-experiments-variance-reduction/>
- Paper – **“Machine Learning for Variance Reduction in Online Experiments” (NeurIPS 2021)**  
  <https://proceedings.neurips.cc/paper/2021/file/488b084119a1c7a4950f00706ec7ea16-Paper.pdf>

---

## 10. Sequential & Always-Valid Testing

Look early and often without completely breaking your Type I error.

**Key topics**

- Group sequential tests and alpha-spending
- Always-valid / anytime-valid p-values
- Sequential probability ratio tests
- Tradeoffs vs fixed-horizon tests
- Practical implementation in experimentation platforms

**Resources**

- Blog – **“Sequential Testing at Booking.com”**  
  <https://blog.booking.com/sequential-testing-at-booking-com-650954a569c7>
- Docs – **“Sequential Testing” (GrowthBook)**  
  <https://docs.growthbook.io/statistics/sequential>
- Article – **“Wish tackles peeking with always-valid p-values”**  
  <https://towardsdatascience.com/wish-tackles-peeking-with-always-valid-p-values-8a0782ac9654>
- Article – **“Calculating Always-Valid p-values in R”**  
  <https://rviews.rstudio.com/2019/08/22/calculating-always-valid-p-values-in-r/>
- Netflix – **“Sequential Testing Keeps the World Streaming”**  
  <https://netflixtechblog.com/sequential-testing-keeps-the-world-streaming-netflix-part-2-counting-processes-da6805341642>
- Spotify – **“Bringing Sequential Testing to Experiments with Longitudinal Data”**  
  <https://engineering.atspotify.com/tag/experimentation/>

---

## 11. Quasi-Experiments & Causal Inference (Beyond Classic A/B)

For when randomization is impossible or too expensive.

**Key topics**

- Difference-in-Differences (DiD)
- Synthetic control
- Regression discontinuity design
- Matching, inverse propensity weighting
- Causal graphs basics (DAGs) to reason about bias

**Resources**

- Online book – **“Causal Inference for the Brave and True” (Matheus Facure)**  
  <https://matheusfacure.github.io/python-causality-handbook/landing-page.html>
- Chapter – **“Difference-in-Differences” (same book)**  
  <https://matheusfacure.github.io/python-causality-handbook/13-Difference-in-Differences.html>
- Notebook – **“Difference in Differences in Python” (Kaggle)**  
  <https://www.kaggle.com/code/harrywang/difference-in-differences-in-python>
- Article – **“Difference-in-Differences” (Bukalapak Data Blog)**  
  <https://medium.com/bukalapak-data/difference-in-differences-8c925e691fff>
- PyMC example – **Bayesian Difference-in-Differences**  
  <https://www.pymc.io/projects/examples/en/latest/causal_inference/difference_in_differences.html>

---

## 12. Bayesian A/B Testing

Alternate paradigm with posterior probabilities and credible intervals instead of p-values.

**Key topics**

- Priors, likelihood, posterior
- Posterior probability of being best, uplift distributions
- Credible intervals vs confidence intervals
- Decision rules: expected loss, probability of beating control, etc.
- Early stopping & sequential nature of Bayesian updates

**Resources**

- Article – **“Beginner’s Guide to Bayesian AB Testing”**  
  <https://medium.com/%40ibtesamahmex/beginners-guide-to-bayesian-ab-testing-22f40988d5e6>
- PyMC – **“Introduction to Bayesian A/B Testing”**  
  <https://www.pymc.io/projects/examples/en/latest/causal_inference/bayesian_ab_testing_introduction.html>
- Article – **“Bayesian A/B testing — a practical primer”**  
  <https://uxdesign.cc/bayesian-a-b-testing-a-practical-primer-c0d4ab1c689e>
- Article – **“Bayesian A/B Testing: A Powerful Reasoning Model” (VWO)**  
  <https://vwo.com/blog/bayesian-a-b-testing-a-powerful-reasoning-model/>
- Notebook – **“Bayesian A/B Testing from Scratch” (Kaggle)**  
  <https://www.kaggle.com/code/cstorm3000/bayesian-a-b-testing-from-scratch>

---

## 13. Experimentation Platforms & System Design

How large companies architect experimentation as a platform: traffic splitting, logging, analysis, guardrails.

**Key topics**

- Randomization services, exposure logging, idempotency
- Assignment consistency (bucketing) and experiment namespaces
- Metrics pipeline & near-real-time aggregation
- Guardrail checks (SRM, data quality, metric sanity)
- Self-serve experiment configuration & approvals
- Feature flags vs experiments vs rollouts

**Resources**

- Uber – **“Under the Hood of Uber’s Experimentation Platform (XP)”**  
  <https://www.uber.com/blog/xp/>
- Uber – **“Supercharging A/B Testing at Uber”**  
  <https://www.uber.com/blog/supercharging-a-b-testing-at-uber/>
- Uber – **“Building an Intelligent Experimentation Platform with Real-Time Results”**  
  <https://www.uber.com/blog/experimentation-platform/>
- Spotify – **“Spotify’s New Experimentation Platform (Part 2)”**  
  <https://engineering.atspotify.com/2020/11/spotifys-new-experimentation-platform-part-2/>
- Spotify Confidence – **Experiment like Spotify blog**  
  <https://confidence.spotify.com/blog/experiment-analysis>
- Microsoft – **Experimentation Platform overview**  
  <https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/>
- Thesis – **“Key Platform Features for Trustworthy A/B-testing”**  
  <https://www.diva-portal.org/smash/get/diva2%3A1480057/FULLTEXT01.pdf>


---

## 14. Interview & Case Study Prep (Optional)

Not strictly “learning experimentation”, but useful if you use this roadmap for job prep.

**Key topics**

- Explain experiment lifecycle clearly and concisely
- Diagnose flawed experiment setups (peeking, SRM, bad metrics)
- Design experiments for funnels, pricing, ranking, notifications, etc.
- Discuss trade-offs between A/B tests, bandits, quasi-experiments

**Resources**

- Article – **“How to Ace A/B Testing Interview Questions”**  
  <https://www.tryexponent.com/blog/how-to-ace-ab-testing-interview-questions>
- Reddit – **A guide to passing the A/B test interview question in tech companies**  
  <https://www.reddit.com/r/datascience/comments/1fyrawz/a_guide_to_passing_the_ab_test_interview_question/>
- Article – **7 A/B Testing Questions and Answers in Data Science Interviews**  
  <https://towardsdatascience.com/7-a-b-testing-questions-and-answers-in-data-science-interviews-eee6428a8b63/>

---

## How to Use This Roadmap

1. **If you’re new to experiments**  
   Start with sections **0–4** (core references, culture, lifecycle, stats basics, sample size).

2. **If you already run A/B tests in production**  
   Deepen competence with **5–10** (ratio metrics, multiple testing, pitfalls, variance reduction, sequential testing).

3. **If you want to be “experimentation expert” / staff-level**  
   Add **11–13** (causal inference, Bayesian, platforms).  
   Use **14–15** to build a portfolio and prepare for senior interviews.
