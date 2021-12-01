# Course Calendar Fall 2021

## Deliverables

| Title | First Submission Due Date | Resubmission Due Date |
|---|:---:|---|
| <a class = "callink" href = "https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/00-getting-started.md">00 Student Profile</a> | 2021-08-30 | Not available |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-Fall-2021/blob/master/deliverables/01-roulette.md'>01 Roulette</a> | 2021-09-06  | 2021-09-24 |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-Fall-2021/blob/master/deliverables/02-monte-carlo-error.md'>02 Monte Carlo Error</a> | 2021-09-13 | 2021-10-04 |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-Fall-2021/blob/master/deliverables/02b-interview-question.md'>02b Interview Question</a> | 2021-09-20| 2021-10-11 |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-Fall-2021/blob/master/deliverables/03-probability-calcs.md'>03 World Series</a> | 2021-09-27 | 2021-10-19 |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-Fall-2021/blob/master/deliverables/EC1-birthday-problem.md'>Extra credit: Birthday Problem</a> | 2021-09-27  | Not available |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-Fall-2021/blob/master/deliverables/04-world-series-home-field.md'>04 Home Field Advantage</a> | 2021-10-04 | 2021-10-25 |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/05-log-transformation.md'>05 Log Transformation</a> | 2021-10-11 | 2021-11-03 |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/06-order-statistics.md'>06 Order Statistics</a> | 2021-10-25 | 2021-11-17 |
| Take a break / Get caught up | 2021-11-01 | Not available |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/07-mle-mm.md'>07 MLE ane MM</a> | 2021-11-08 | 2021-12-09 |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/08-coverage-probability.md'>08 Coverage Probability</a> | 2021-11-29 | 2021-12-? |
| <a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/09-method-comparison.md'>09 Methods not equally good</a> | 2021-12-6 | 2021-12-16  |
|<a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/10-clt.md'>10 Central Limit Theorem Shortcut</a>|  |  |
|<a class = 'callink' href ='https://github.com/thomasgstewart/data-science-5620-fall-2021/blob/master/deliverables/11-mvn.md'>11 Correlation and Inference</a> |  |  |

## Problem Set

| Due Date | Problem |
|:---:|:---|
| 2021-10-20 | (a) Generate, via simulation, a plot of the distribution of the 25th percentile of a sample of size 100 when the underlying distribution is gamma with shape = 3 and scale = 12 <br> (b) Overlay on the plot from (a) the analytic solution of the pdf |
| 2021-10-27 | (a) Read chapter 3. <br> (b) Complete problem 4 of Section 3.12 <br> (c) Complete problem 8 of Section 3.12 |
| 2021-11-01 | (a) Read chapter 7. <br> (b) Read chapter 8. <br> (c) Replicate figure 8.5 by following the example in section 8.4.2 <br> You can get the pima dataset by installing the `faraway` package and the command `data(pima)` <br> (d) Generate the same plot as Figure 8.5 for adult males using the NHANES dataset. <br> Recall you can use the command `Hmisc::getHdata(nhgh)` to retrieve the data. <br> (e) Replicate figure 8.6 by following the example in section 8.4.4 <br> You can use the following commands to retrieve the bike dataset from the UCI repository <br> <code>temp <- tempfile() <br> download.file("https://archive.ics.uci.edu/ml/machine-learning-databases/00275/Bike-Sharing-Dataset.zip",temp) <br>con <- unz(temp, "day.csv") <br> bike <- read.table(con, sep=",", header = TRUE) <br> unlink(temp) </code> |
| 2021-11-03 | (a) Do exercise 7 of section 8.10, overlay the estimated pdf on the histogram <br> (b) Add to the plot in (a) a kernel density estimate of the pdf <br> Recall, the dataset is in the faraway package.  Missing values are coded as zero. |
| 2021-11-10 | (a) Review the slides at https://biostatdata.app.vumc.org/tgs/13-bootstrap.html <br> (b) Replicate the figure on slide 32.  (The code is provided in slides 30 and 31.  Copy and paste.) |
| 2021-11-15 | (a) Read chapter 9 <br> (b) Complete questions 1, 2, 3, 6, 7 in section 9.13 |
| 2021-11-17 | (a) Read https://biostatdata.app.vumc.org/tgs/18-parallel-processing.html <br> (b) Read https://biostatdata.app.vumc.org/tgs/20-batch-processing-accre.html |

## Final Exam

The final exam will occur between 13 December 2021 and 18 December 2021.  Students will sign up for oral exam slots in early December.

## Topics

**PLEASE NOTE:** The slides are often changed before lecture (both major edits and minor tweaks).  

| Topic | Slides | Textbook sections | Videos |
|---|:---:|:---:|---|
| Class logistics | | | |
| **Definitions of Probability** | [slides](https://biostatdata.app.vumc.org/tgs/01-probability-definition-slides.html)  | | |
| **Simulation & Operating Characteristics** | <a class = 'callink' href ='https://biostatdata.app.vumc.org/tgs/01-simulation-slides.html'>slides</a><br>[review](https://biostatdata.app.vumc.org/tgs/02-simulation-review-slides.html) | 2 |  |
| **Basic Probability Ideas** | [slides](https://biostatdata.app.vumc.org/tgs/03-probability-basics-slides.html) <br> [slides part 2](https://biostatdata.app.vumc.org/tgs/04-probability-basics-part2-slides.html) | 1 |  |
|  → Belief vs Frequency  | | | |
|  → Notebook / data.frame definition  | | | |
|  → And, Or  | | 1.3 | |
|  → Conditional Probability | | 1.3 | |
|  → Law of Total Probability | [slides](./lectures/04-probability-bayes-rule.pdf) <br> [slides part 2](./lectures/04-more-bayes.pdf)|
|  → Bayes Rule | [slides](./lectures/04-probability-bayes-rule.pdf) <br> [slides part 2](./lectures/04-more-bayes.pdf) | 1.9 |  |
| **Discrete Probability Models** | | 3, 4, 5 | |
| → Bernouli Random Variables | [slides](https://biostatdata.app.vumc.org/tgs/05-binomial-prob.html) | |  |
| → Binomial Random Variables | [slides](https://biostatdata.app.vumc.org/tgs/05-binomial-prob.html)| |  |
| → Negative Binomial Random Variables | [slides](https://biostatdata.app.vumc.org/tgs/05-binomial-prob.html) | | |
| → Poisson Random Variables | [slides](https://biostatdata.app.vumc.org/tgs/06-poisson.html) | | |
| → Probability Mass Function | [slides](https://biostatdata.app.vumc.org/tgs/07-pmf-cdf.html)| | |
| **Continuous Probability Models** | | 6 | |
| → Cumulative Distribution Function | [slides](https://biostatdata.app.vumc.org/tgs/08-continuous-probability-models.html) | | |
| → Probability Density Function | [slides](https://biostatdata.app.vumc.org/tgs/08-continuous-probability-models.html) | | |
| → Uniform Random Variables  | [slides](https://biostatdata.app.vumc.org/tgs/09-continuous-probability-models-part2.html)| |  |
| → Normal Random Variables  | [slides](https://biostatdata.app.vumc.org/tgs/09-continuous-probability-models-part2.html) | | |
| → Exponential Random Variables  | [slides](https://biostatdata.app.vumc.org/tgs/09-continuous-probability-models-part2.html) | | |
| → Gamma Random Variables  | [slides](https://biostatdata.app.vumc.org/tgs/09-continuous-probability-models-part2.html) | | |
| → Beta Random Variables  | [slides](https://biostatdata.app.vumc.org/tgs/09-continuous-probability-models-part2.html) | | |
| → Mixture Distributions  | [slides](https://biostatdata.app.vumc.org/tgs/09-continuous-probability-models-part2.html) | | |
| **Expectation and Variance** | | 3.6, 4.1, 4.3, 6.5  | |
| → Data Types | [slides](https://biostatdata.app.vumc.org/tgs/10-expectation-variance.html) | | |
| → Categorical, Ordinal, Interval, and Ratio Variables | [slides](https://biostatdata.app.vumc.org/tgs/10-expectation-variance.html) | | |
| → Covariance | [slides](https://biostatdata.app.vumc.org/tgs/10-expectation-variance.html) | | |
| **Transformations of individual observations** | | |  |
| **Transformations of samples** | | 7 | |
| → Min and Max | [slides](https://biostatdata.app.vumc.org/tgs/11-transformations-order-statistics.html) | | |
| → Quantiles | [slides](https://biostatdata.app.vumc.org/tgs/11-transformations-order-statistics.html) | | |
| → Order Statistics | [slides](https://biostatdata.app.vumc.org/tgs/11-transformations-order-statistics.html) <br> [application](https://biostatdata.app.vumc.org/tgs/12-applications-order-statistics.html) | | | |
| → Sampling distributions | [slides](https://biostatdata.app.vumc.org/tgs/11-transformations-order-statistics.html) | | |
| **Methods of Fitting Models** | [Lots of pdfs](https://www.desmos.com/calculator/qgpfi00qnb) | 8 | |
| → QQ-plot | | |  |
| → Method of moments | [slides](https://biostatdata.app.vumc.org/tgs/15-fitting-continuous-models-mle.html) | | |
| → Maximum likelihood | [slides](https://biostatdata.app.vumc.org/tgs/15-fitting-continuous-models-mle.html)  | | |
| → Bayesian | | | |
| → Kernel Density Estimation | [slides](https://biostatdata.app.vumc.org/tgs/14-fitting-continuous-models.html) | | |
| **Sampling Distributions from Fitted Models**| | | |
| → Bootstrap | [slides](https://biostatdata.app.vumc.org/tgs/13-bootstrap.html) | | |
| → Simulation | [slides](https://biostatdata.app.vumc.org/tgs/16-sampling-distributions-from-Fhat.html) | | |
| → Central Limit Theorem | [slides](https://biostatdata.app.vumc.org/tgs/19-normal-distribution-clt.html) | | |
| **Simulation** | | | |
| → Parallel Computing | [slides](https://biostatdata.app.vumc.org/tgs/18-parallel-processing.html) | | |
| → Batch processing on ACCRE or AWS | [slides](https://biostatdata.app.vumc.org/tgs/20-batch-processing-accre.html) | | |
| **Inference**| | | |
| → Sampling and Inference | | | |
| → Inference with CI | [slides](https://biostatdata.app.vumc.org/tgs/inference2.pdf) | | |
| → Inference with Hypothsis testing | [slides](https://biostatdata.app.vumc.org/tgs/inference2.pdf) | |  |
| **Multivariate Normal Distribution** | | 12 | |
| → Properties | [slides](https://biostatdata.app.vumc.org/tgs/21-multivariate-normal-distributions.html) | | |
| → Correlation | [slides](https://biostatdata.app.vumc.org/tgs/21-multivariate-normal-distributions.html) | | |
| → Conditional Distribution | [slides](https://biostatdata.app.vumc.org/tgs/22-multivariate-conditional-distribution.html) | | |
| → Marginal Distribution | [slides](https://biostatdata.app.vumc.org/tgs/22-multivariate-conditional-distribution.html) | | |

<!-- 
## Lecture and Office Hours Videos

| Date | Description |
|---|---|
| 2020-08-24 | [Lecture - Simulation](https://vbiostat2.app.vumc.org/index.php/s/mTEyw4YZcLp9BCq) |
| 2020-08-26 | [Lecture - Course Policies](https://vbiostat2.app.vumc.org/index.php/s/BNNBgE4frZEaQC2) |
| 2020-08-31 | [Lecture - Roulette Deliverable Review](https://vbiostat2.app.vumc.org/index.php/s/wyzQBBJooN2EZGT) |
| 2020-08-31 | [Offic Hours - Plotting budget profile over time (roulette deliverable](https://vbiostat2.app.vumc.org/index.php/s/EBRyoKNSeziZk2d) |
| 2020-09-02 | [Lecture - Probability](https://vbiostat2.app.vumc.org/index.php/s/ZTp9GkFBqHzo5oG) |
| 2020-09-04 | [Lecture - Probability part 2](https://vbiostat2.app.vumc.org/index.php/s/HPgzdztncLnHqob) |
| 2020-09-05 | [Deliverable - Absolute and relative error](https://vbiostat2.app.vumc.org/index.php/s/29CpdaTTRicBp2p) |
| 2020-09-07 | [Lecture - Probability review](https://vbiostat2.app.vumc.org/index.php/s/pypYELcirmqzZFe) |
| 2020-09-09 | [Lecture - Bayes Rule](https://vbiostat2.app.vumc.org/index.php/s/QiGcZmD7Rk8C7k9) |
| 2020-09-11 | [Lecture - Probability practice questions](https://vbiostat2.app.vumc.org/index.php/s/W6dXZFjsop3HW8K)|
| 2020-09-11 | [Probability practice question - coin toss](https://vbiostat2.app.vumc.org/index.php/s/xRB9aMDC4AEn5di)|
| 2020-09-14 | [Lecture - Binomial, Negative binomial](https://vbiostat2.app.vumc.org/index.php/s/tfH5MayYYnaotk8) |
| 2020-09-16 | [Lecture - Binomial, Negative binomial (cont)](https://vbiostat2.app.vumc.org/index.php/s/H3wYDm89L5sp6qW) |
| 2020-09-16 | [Practice Problems - Binomial, Negative binomial](https://vbiostat2.app.vumc.org/index.php/s/ETed5MT7ycA6NQz) | 
| 2020-09-18 | [Lecture - Poisson distribution](https://vbiostat2.app.vumc.org/index.php/s/77iw36kT3YB5TfR) |
| 2020-09-21 | [Lecture - Deliverable 3 question 5](https://vbiostat2.app.vumc.org/index.php/s/HWEKG67wCAbrz9J) |
| 2020-09-23 | [Lecture - World Series distribution](https://vbiostat2.app.vumc.org/index.php/s/EmS88pZXriYTZPt) |
| 2020-09-25 | [Lecture - Continuous probability models](https://vbiostat2.app.vumc.org/index.php/s/93FxTFYLEc8LTdo) |
| 2020-09-28 | [Lecture - Uniform, Normal, Gamma, Beta, Finite Mixture](https://vbiostat2.app.vumc.org/index.php/s/MxBX2zMrHsz2RHL) |
| 2020-09-30 | [Lecture - Practice problems](https://vbiostat2.app.vumc.org/index.php/s/9GR9DyFAybmTxfZ) |
| 2020-09-30 | [Practice Problems - Uniform, Normal, Gamma, Mixture distribution](https://vbiostat2.app.vumc.org/index.php/s/qMqomiK8F7Cs55a) |
| 2020-10-02 | [Lecture - Data Types](https://vbiostat2.app.vumc.org/index.php/s/GsJdXHk5Lgo8NJH) |  
| 2020-10-05 | [Lecture - Expectation and Variance](https://vbiostat2.app.vumc.org/index.php/s/8KLXGFK9k38zyKB) |  
| 2020-10-07 | [Lecture - Covariance](https://vbiostat2.app.vumc.org/index.php/s/2kQNKji2i8FzfDC) |
| 2020-10-05 | [Lecture - Expectation and Variance](https://vbiostat2.app.vumc.org/index.php/s/8KLXGFK9k38zyKB) |  
| 2020-10-09 | [Lecture - Middle and Spread](https://vbiostat2.app.vumc.org/index.php/s/wp7ckAY7r4a688A) |
| 2020-10-10 | [Deliverable - Geometric Mean and Arithmetic Mean](https://vbiostat2.app.vumc.org/index.php/s/Na4BR9jZPCgNq2s) |
| 2020-10-12 | [Lecture - Samples](https://vbiostat2.app.vumc.org/index.php/s/SP37t3kDEmCQ3sw) |
| 2020-10-14 | [Lecture - QQ plot, application of ordinal statistics](https://vbiostat2.app.vumc.org/index.php/s/XKTL5mrqipYGMLt) |
| 2020-10-16 | [Lecture - Method of Moments](https://vbiostat2.app.vumc.org/index.php/s/wNJQqmcsrrDpqmf) |
| 2020-10-19 | [Lecture - MLE](https://vbiostat2.app.vumc.org/index.php/s/MAwTAxKLc4SSQ8F) |
| 2020-10-21 | [Lecture - MLE and MM Deliverable](https://vbiostat2.app.vumc.org/index.php/s/XW6ZcQjAMDZwaJq) |
| 2020-10-24 | [Lecture - Bootstrap](https://vbiostat2.app.vumc.org/index.php/s/k5K2qmpPxbDL2bL) |
| 2020-10-26 | [Lecture - Kernel Density Estimation](https://vbiostat2.app.vumc.org/index.php/s/3BBkLAFxESqLCXs) |
| 2020-10-28 | [Lecture - Sampling from Fitted Distributions](https://vbiostat2.app.vumc.org/index.php/s/Zbmi6Y7dFgYCGbb) |
| 2020-10-30 | [Lecture - Uniform + quantile](https://vbiostat2.app.vumc.org/index.php/s/gRbtbZPisscWWpa) |
| 2020-10-31 | [Practice Question - Quantile function for mixture distribution](https://vbiostat2.app.vumc.org/index.php/s/ycgcoPbMSicNgoQ) |
| 2020-11-02 | [Lecture - U + Q vs B + Q](https://vbiostat2.app.vumc.org/index.php/s/wcg22Y39ni48mdN) |
| 2020-11-04 | [Lecture - Breakout rooms (practice problems) ](https://vbiostat2.app.vumc.org/index.php/s/yFmWBfqkXiXWsQs) |
| 2020-11-06 | [Lecture - Parallel Computing](https://vbiostat2.app.vumc.org/index.php/s/bKoLZ66NnfiFAxG) |
| 2020-11-09 | [Lecture - CLT Shortcut](https://vbiostat2.app.vumc.org/index.php/s/5t5RperMFNKo4DA) |
| 2020-11-11 | [Lecture - CLT Shortcut continued](https://vbiostat2.app.vumc.org/index.php/s/fiPLN3pTdXRp27B) |
| 2020-11-13 | [Lecture - Sampling and Inference](https://vbiostat2.app.vumc.org/index.php/s/6Pbt7QijSmRowra) |
| 2020-11-14 | [Practice - Parallel Computing and ACCRE](https://vbiostat2.app.vumc.org/index.php/s/HGpKpjnX3NBtNi6) |
| 2020-11-16 | [Lecture - Inference with CI](https://vbiostat2.app.vumc.org/index.php/s/qa6o929zCR9agQP) |
| 2020-11-18 | [Lecture - Inference with Hypothesis Testing](https://vbiostat2.app.vumc.org/index.php/s/HnEHbeY8f9C7LKS) |
| 2020-11-20 | [Lecture - Inference with p-values](https://vbiostat2.app.vumc.org/index.php/s/tEeHi6obGmY5ePg) |
| 2020-11-30 | [Lecture - Multivariate](https://vbiostat2.app.vumc.org/index.php/s/bPzT6MorfwXknRX) |
| 2020-12-02 | [Lecture - Conditional Multivariate](https://vbiostat2.app.vumc.org/index.php/s/2wSkbWcfjDFQD39) |
| 2020-12-03 | [Office Hour - Final Exam](https://vbiostat2.app.vumc.org/index.php/s/LjdmXzFNYy3tzdN) |
| 2020-12-04 | [Office Hour - 7am](https://vbiostat2.app.vumc.org/index.php/s/M9ysHH4zoJbNFwE) |
| 2020-12-05 | [Office Hour - 10am](https://vbiostat2.app.vumc.org/index.php/s/GNLC3KzAXS5qNsz) |
| 2020-12-05 | [Office Hour - 11:30am](https://vbiostat2.app.vumc.org/index.php/s/HfNzmYGCKCFkon9) |
| 2020-12-06 | [Final Exam Hint](https://vbiostat2.app.vumc.org/index.php/s/o3BG6LCamr5cRH3) |
-->
