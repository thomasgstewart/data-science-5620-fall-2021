How often does the better team win the World Series?
====================================================

The world series is a best-of-7 match-up between the champions of the
American and National Leagues of Major League Baseball. In this
assignment, you are going to explain probability calculations related to
the world series.

Assignment
----------

In this assignment, you will write a blog post to answer a series of
questions related to the World Series. You will use the rules of
probability and discrete probability functions to answer the questions.
The audience of your blog post is an HR manager tasked with hiring a
data scientist. The HR manager is looking for candidates that can take a
data science concept and will explain the question and explain the
solution in a way that is accessible to a general audience. **Be sure**
to mention any assumptions of your solution.

Setup:

1.  Suppose that the Braves and the Yankees are teams competing in the
    World Series.
2.  Suppose that in any given game, the probability that the Braves win
    is *P*<sub>*B*</sub> and the probability that the Yankees win is
    *P*<sub>*Y*</sub> = 1 − *P*<sub>*B*</sub>.

Questions to answer:

1.  What is the probability that the Braves win the World Series given
    that *P*<sub>*B*</sub> = 0.55?
2.  What is the probability that the Braves win the World Series given
    that *P*<sub>*B*</sub> = *x*? This will be a figure (see below) with
    *P*<sub>*B*</sub> on the x-axis and *P*(Braves win World Series) on
    the y-axis.
3.  Suppose one could change the World Series to be best-of-9 or some
    other best-of-X series. What is the shortest series length so that
    *P*(Braves win World Series\|*P*<sub>*B*</sub> = .55) ≥ 0.8
4.  What is the shortest series length so that
    *P*(Braves win World Series\|*P*<sub>*B*</sub> = *x*) ≥ 0.8? This
    will be a figure (see below) with *P*<sub>*B*</sub> on the x-axis
    and series length is the y-axis.
5.  Calculate
    *P*(*P*<sub>*B*</sub> = 0.55\|Braves win World Series in 7 games)
    under the assumption that either *P*<sub>*B*</sub> = 0.55 or
    *P*<sub>*B*</sub> = 0.45. Explain your solution.

### Figure shells

![](./assets/probability-win-world-series.svg)

![](./assets/world-series-length-for-80pct-prob.svg)

### Submission instructions

1.  Within the repo
    `Probability and Inference Portfolio Lastname Firstname`, create a
    folder called `03-discrete-probability-calculations`
2.  Within the folder, create an .html for your blog post
3.  **The name of the blog post file must be `writeup.html`**
4.  Within the folder, include code scripts or .rmd or some other
    document that will successfully generate the output of the
    simulation when executed from within the folder. (Do not use
    absolute file paths.)
5.  Edit the README to be an index for the portfolio.  
6.  Be prepared to share your blog post with the class when the
    deliverable is due.

### Other instructions

1.  The deliverable should be your own work. You may **NOT** discuss
    this project with classmates.
