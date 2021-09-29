# If home field advantage exists, how much of an impact does it have on winning the world series?

The **home field advantage** is the edge which a team may have when
playing a game at its home stadium. For example, it is the edge the
Braves may have over the Yankees when the head-to-head match-up is in
Atlanta. It is the advantage the Yankees may have when the head-to-head
match-up is in New York.

The World Series is a first-to-4-wins match-up between the champions of
the American and National Leagues of Major League Baseball. In this
assignment, you are going to use simulation and analytic methods to
compare the probability of winning the World Series with and without
home field advantage.

## Assignment

In this assignment, you will write a blog post to answer a series of
questions related to the World Series. You will use simulation and
analytic probability calculations to answer the questions. The audience
of your blog post is an HR manager tasked with hiring a data scientist.
The HR manager is looking for candidates that can take a data science
concept and will explain the question and explain the solution in a way
that is accessible to a general audience. **Be sure** to mention any
assumptions of your solution.

Setup:

-   Suppose that the Braves and the Yankees are teams competing in the
    World Series.

-   The table below has the two possible schedules for each game of the
    series. (NYC = New York City, ATL = Atlanta)

| Overall advantage | Game 1 | Game 2 | Game 3 | Game 4 | Game 5 | Game 6 | Game 7 |
|:-----------------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
|      Braves       |  ATL   |  ATL   |  NYC   |  NYC   |  NYC   |  ATL   |  ATL   |
|      Yankees      |  NYC   |  NYC   |  ATL   |  ATL   |  ATL   |  NYC   |  NYC   |

-   Let *P*<sub>*B*</sub> be the probability that the Braves win a
    single head-to-head match-up with the Yankees, under the assumption
    that home field advantage doesn’t exist. Let
    *P*<sub>*B*</sub><sup>*H*</sup> denote the probability that the
    Braves win a single head-to-head match-up with the Yankees as the
    home team (H for home). Let *P*<sub>*B*</sub><sup>*A*</sup> denote
    the probability that the Braves win a single head-to-head match-up
    with the away team (A for away).

| Game location |   No advantage    | Advantage                                                            |
|:-------------:|:-----------------:|:---------------------------------------------------------------------|
|      ATL      | *P*<sub>*B*</sub> | *P*<sub>*B*</sub><sup>*H*</sup> = *P*<sub>*B*</sub> \* 1.1           |
|      NYC      | *P*<sub>*B*</sub> | *P*<sub>*B*</sub><sup>*A*</sup> = 1 − (1 − *P*<sub>*B*</sub>) \* 1.1 |

Questions to answer:

1.  Compute analytically the probability that the Braves win the world
    series when the sequence of game locations is {NYC, NYC, ATL, ATL,
    ATL, NYC, NYC}. (The code below computes the probability for the
    alternative sequence of game locations. **Note:** The code uses
    `data.table` syntax, which may be new to you. This is intentional,
    as a gentle way to introduce `data.table`.) Calculate the
    probability with and without home field advantage when
    *P*<sub>*B*</sub> = 0.55. What is the difference in probabilities?

2.  Calculate the same probabilities as the previous question by
    simulation.

3.  What is the absolute and relative error for your simulation in the
    previous question?

4.  Does the difference in probabilities (with vs without home field
    advantage) depend on *P*<sub>*B*</sub>? (Generate a plot to answer
    this question.)

5.  Does the difference in probabilities (with vs without home field
    advantage) depend on the advantage factor? (The advantage factor in
    *P*<sub>*B*</sub><sup>*H*</sup> and *P*<sub>*B*</sub><sup>*A*</sup>
    is the 1.1 multiplier that results in a 10% increase for the home
    team. Generate a plot to answer this question.)

### Submission instructions

1.  Within the repo
    `Probability and Inference Portfolio Lastname Firstname`, create a
    folder called `04-home-field-advantage`
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

1.  The deliverable should be your own work. You may **discuss**
    concepts with classmates, but you may **not share** code or text.

``` r
require(dplyr)
require(data.table)
# Get all possible outcomes
apo <- fread("./assets/all-possible-world-series-outcomes.csv")

# Home field indicator
hfi <- c(1,1,0,0,0,1,1) #{ATL, ATL, NYC, NYC, NYC, ATL, ATL}

# P_B
pb <- 0.55
advantage_multiplier <- 1.1 # Set = 1 for no advantage
pbh <- 0.55*advantage_multiplier
pba <- 1 - (1 - 0.55)*advantage_multiplier

# Calculate the probability of each possible outcome
apo[, p := NA_real_] # Initialize new column in apo to store prob
for(i in 1:nrow(apo)){
  prob_game <- rep(1, 7)
  for(j in 1:7){
    p_win <- ifelse(hfi[j], pbh, pba)
    prob_game[j] <- case_when(
        apo[i,j,with=FALSE] == "W" ~ p_win
      , apo[i,j,with=FALSE] == "L" ~ 1 - p_win
      , TRUE ~ 1
    )
  }
  apo[i, p := prod(prob_game)] # Data.table syntax
}

# Sanity check: does sum(p) == 1?
apo[, sum(p)] # This is data.table notation

# Probability of overall World Series outcomes
apo[, sum(p), overall_outcome]
```
