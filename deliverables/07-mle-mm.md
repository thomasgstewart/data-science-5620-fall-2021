Modeling the unknown distribution with maximum likelihood and method of moments
===============================================================================

Maximum likelihood (MLE) and method of moments (MM) are two common
methods for constructing a model.

Assignment
----------

In this deliverable, you will write a tutorial in which you will explain
to the reader how one might use MLE and MM to model (a) Glycohemoglobin
and (b) Height of adult females. The data will be from National Health
and Nutrition Examination Survey 2009-2010 (NHANES), available from the
Hmisc package. You will compare and contrast the two methods in addition
to comparing and contrasting the choice of underlying distribution.

The audience of your blog post is a new comer to data science, who is
hoping to learn about these commonly used tools. Your tutorial should

1.  Show how you calculated estimates of parameters
2.  Provide visuals that show the estimated distribution compared to the
    empirical distribution (comment on the quality of the fit)
    -   Overlay estimated pdf onto histogram
    -   Overlay estimated CDF onto eCDF
    -   QQ plot (sample vs estimated dist)
3.  Explain how you calculated the median from the estimated
    distribution
4.  [SKIP] Demonstrate how to generate the median sampling distribution
5.  [SKIP] Calculated the range of middle 95% of sampling distribution, and
    explain why such a quantity is important.

At the end of your tutorial, provide the reader with a set of “take-home
messages”.

Data
----

``` r
require(dplyr)
Hmisc::getHdata(nhgh)
d1 <- nhgh %>% 
  filter(sex == "female") %>% 
  filter(age >= 18) %>% 
  select(gh, ht) %>% 
  filter(1:n()<=1000)
```

Checklist
---------

Do for both MLE and MM

|                                      | Normal | Gamma | Weibull |
|:-------------------------------------|:------:|:-----:|:-------:|
| Estimates of parameters              |        |       |         |
| Overlay estimated pdf onto histogram |        |       |         |
| Overlay estimated CDF onto eCDF      |        |       |         |
| QQ plot (sample vs estimated dist)   |        |       |         |
| Estimated Median                     |        |       |         |
| [SKIP] Median Samp Dist (hist)              |        |       |         |
| [SKIP] Range of middle 95% of Samp Dist     |        |       |         |

Submission instructions
-----------------------

1.  Within the repo
    `Probability and Inference Portfolio Lastname Firstname`, create a
    folder called `07-mle-and-mm`
2.  Within the folder, create an .html for your blog post
3.  **The name of the blog post file must be `writeup.html`**
4.  Within the folder, include code scripts or .rmd or some other
    document that will successfully generate the output of the
    simulation when executed from within the folder. (Do not use
    absolute file paths.)
5.  Edit the README to be an index for the portfolio.  
6.  Be prepared to share your blog post with the class when the
    deliverable is due.

Other instructions
------------------

1.  The deliverable should be your own work. You may **discuss**
    concepts with classmates, but you may **not share** code or text.
