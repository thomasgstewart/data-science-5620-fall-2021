Simulation study
================

Coverage probability is an important operating characteristic of methods
for constructing interval estimates, particularly confidence intervals.
(See the previous deliverable for definitions and examples.)

Idealy, a 95% confidence interval will capture the population parameter
of interest in 95% of samples. One can also calculate 80% or 90%
confidence intervals. In general, an X% confidence interval should
capture the population parameter of interest in X% of samples.

Not all methods are equally good
--------------------------------

In this assignment, you will perform a 2 × 4 × 2 factorial simulation
study to compare the coverage probability of various methods of
calculating **90%** confidence intervals. The three factors in the
experiment are

1.  True, underlying distribution
    -   standard normal
    -   gamma(shape = 1.4, scale = 3)
2.  Model
    -   method of moments with normal
    -   method of moments with gamma
    -   kernel density estimation
    -   bootstrap
3.  Parameter of interest
    -   sample min (1st order statistic)
    -   median

Other settings in the experiment that will not change are:

-   Sample size, *N* = 201
-   *Outside the loop* estimation

You will write a blog post to explain your simulation study and results.
The audience of your blog post is a Senior Data Scientist who you hope
to work with in the future. Think about how you will communicate the
results. Will you generate a table, a figure, or a table of figures?

Submission instructions
-----------------------

1.  Within the repo
    `Probability and Inference Portfolio Lastname Firstname`, create a
    folder called `09-simulation-study`
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
