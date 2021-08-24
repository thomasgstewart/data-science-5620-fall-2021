Log transform
=============

It is common in the analysis of biological data to log transform data
representing concentrations or data representing dose response.

Assignment
----------

In this assignment, you will write a blog post to answer a series of
questions related to the transformation of data. You will use both
analytic methods and simulation to answer the questions.

The audience of your blog post is a Senior Data Scientist who you hope
to work with in the future. Your goal is to impress the data scientist
with your ability to explain the question and the solution in a way that
is accessible to the data scientist’s lab. **Be sure** to mention any
assumptions of your solution.

Part 1
------

-   For each distribution below, generate a figure of the PDF and CDF.
    Mark the mean and median in the figure.

-   For each distribution below, generate a figure of the PDF and CDF of
    the transformation Y = log(X) random variable. Mark the mean and
    median in the figure. You may use simulation or analytic methods in
    order find the PDF and CDF of the transformation.

-   For each of the distributions below, generate 1000 samples of
    size 100. For each sample, calculate the geometric and arithmetic
    mean. Generate a scatter plot of the geometic and arithmetic sample
    means. Add the line of identify as a reference line.

-   Generate a histogram of the difference between the arithmetic mean
    and the geometric mean.

### Distribution 1

*X* ∼ GAMMA(shape = 3, scale = 1)

[Interactive plot (link)](https://www.desmos.com/calculator/wgqdkl5ogl)

### Distribution 2

*X* ∼ LOG NORMAL(*μ* =  − 1, *σ* = 1)

[Interactive plot (link)](https://www.desmos.com/calculator/rueernwrhl)

### Distribution 3

*X* ∼ UNIFORM(0, 12)

Part 2
------

Show that if *X*<sub>*i*</sub> \> 0 for all *i*, then the arithmetic
mean is greater than or equal to the geometric mean.

Hint: Start with the sample mean of the transformation
*Y*<sub>*i*</sub> = log (*X*<sub>*i*</sub>).

Part 3
------

What is the correct relationship between *E*\[log (*X*)\] and
log (*E*\[*X*\])? Is one always larger? Equal? Explain your answer.

Submission instructions
-----------------------

1.  Within the repo
    `Probability and Inference Portfolio Lastname Firstname`, create a
    folder called `05-log-transformation`
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
