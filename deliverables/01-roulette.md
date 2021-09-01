Roulette
========

<img src="./assets/roulette-table.svg" style="width:50.0%" />

A roulette table composed of 38 (or 37) evenly sized pockets on a wheel.
The pockets are colored red, black, or green. The pockets are also
numbered. Roulette is a game of chance in which a pocket is randomly
selected. Gamblers may wager on several aspects of the outcome. For
example, one may place a wager that the randomly selected pocket will be
red or odd numbered or will be a specific number.

For this assignment, all one needs to know is that there are 38 pockets
of which 2 are green, 18 are red, and 18 are black. The payout for a bet
on black (or red) is $1 for each $1 wagered. This means that if a
gambler bets $1 on black and the randomly selected pocket is black, then
the gambler will get the original $1 wager and an additional $1 as
winnings.

Roulette strategies
-------------------

There are several *strategies* for playing roulette. (*Strategies* is in
italics because the house always wins, in the long run.) Consider one
such strategy:

![](./assets/martingale-strategy.svg)

This is a classic roulette strategy called the “Martingale” strategy.
Consider how the strategy playes out for a single sequence of spins
{Black, Black, Red}.

| Play | Wager | Outcome | Earnings |
|:----:|:-----:|:-------:|:--------:|
|   1  |   1   |  Black  |    -1    |
|   2  |   2   |  Black  |    -3    |
|   3  |   4   |   Red   |    +1    |

Now consider a sequence {Black, Black, Black, Red}.

| Play | Wager | Outcome | Earnings |
|:----:|:-----:|:-------:|:--------:|
|   1  |   1   |  Black  |    -1    |
|   2  |   2   |  Black  |    -3    |
|   3  |   4   |  Black  |    -7    |
|   4  |   8   |   Red   |    +1    |

The Martingale strategy appears to always end in positive earnings,
regardless of how unlucky a string of spins may be. Is the strategy
actually profitable?

Assignment
----------

In this assignment, you will write a blog post to explain how you used
computer simulation to understand the operating characteristics of the
above strategy.

-   The audience of your blog post is a sharp college freshman with
    little to no background in data science.

-   You should explain how you used computer simulation to calculate the
    average earnings of a gambler that uses this strategy. As part of
    the explanation, provide a figure (or a series of figures) that show
    how the gamblers earnings (or losses) evolve over a series of wagers
    at the roulette wheel. (The x-axis will be the wager number (or play
    number), the y-axis will be earnings.) The code below provides all
    the functions you’ll need to calculate average earnings.

-   Show your audience how changing a parameter of the simulation (see
    table below) does or does not have an impact on average earnings. A
    figure would be helpful.

-   See the stopping rule below. Explain to your audience how you used
    computer simulation to estimate the average number of plays before
    stopping. The code below will need to be modified to calculate this
    quantity.

-   Be sure to explain the limitations of the simulation; identify
    simplifications or other sources of uncertainty.

### Submission instructions

1.  Within your course repo, create a folder called `01-roulette-simulation`
1.  Within the folder, create an .html or .md file with the name
    `writeup`
1.  Be prepared to share your blog post with the class when the
    deliverable is due
1.  The deliverable should be your own work. You may **discuss**
    concepts with classmates, but you may **not share** code or text.

Additional assumptions for the simulation.
------------------------------------------

### Stopping rule

A player will use the above strategy and play until

1.  the player has **W** dollars
2.  the player goes bankrupt
3.  the player completes **L** wagers (or plays)

### Budget

The player starts with **B** dollars. The player cannot wager more money
than he/she has.

### Maximum wager

Some casinos have a maximum bet. Call this parameter **M**. If the
strategy directs the player to wager more than M dollars, then the
player will only wager M dollars.

Summary of parameters (Solution 1)
---------------------

| Parameter | Description                     |             Starting value             |
|:---------:|:--------------------------------|:--------------------------------------:|
|   **B**   | Starting budget                 |                  $200                  |
|   **W**   | Winnings threshold for stopping | $300 (Starting budget + $100 winnings) |
|   **L**   | Time threshold for stopping     |               1000 plays               |
|   **M**   | Casino’s maximum wager          |                  $100                  |

``` r
#' A single play of the Martingale strategy
#'
#' Takes a state list, spins the roulette wheel, returns the state list with updated values (for example, budget, plays, etc)
#' @param state A list with the following entries: 
#'   B              number, the budget
#'   W              number, the budget threshold for successfully stoping
#'   L              number, the maximum number of plays 
#'   M              number, the casino wager limit
#'   plays          integer, the number of plays executed
#'   previous_wager number, the wager in the previous play (0 at first play)
#'   previous_win   TRUE/FALSE, indicator if the previous play was a win (TRUE at first play)
#' @return The updated state list
one_play <- function(state){
  
    # Wager
    proposed_wager <- ifelse(state$previous_win, 1, 2*state$previous_wager)
    wager <- min(proposed_wager, state$M, state$B)
    
    # Spin of the wheel
    red <- rbinom(1,1,18/38)
    
    # Update state
    state$plays <- state$plays + 1
    state$previous_wager <- wager
    if(red){
      # WIN
      state$B <- state$B + wager
      state$previous_win <- TRUE
    }else{
      # LOSE
      state$B <- state$B - wager
      state$previous_win <- FALSE
    }
  state
}


#' Stopping rule
#'
#' Takes the state list and determines if the gambler has to stop
#' @param state A list.  See one_play
#' @return TRUE/FALSE
stop_play <- function(state){
  if(state$B <= 0) return(TRUE)
  if(state$plays >= state$L) return(TRUE)
  if(state$B >= state$W) return(TRUE)
  FALSE
}


#' Play roulette to either bankruptcy, success, or play limits
#'
#' @param B number, the starting budget
#' @param W number, the budget threshold for successfully stoping
#' @param L number, the maximum number of plays 
#' @param M number, the casino wager limit
#' @return A vector of budget values calculated after each play.
one_series <- function(
    B = 200
  , W = 300
  , L = 1000
  , M = 100
){

  # initial state
  state <- list(
    B = B
  , W = W
  , L = L
  , M = M
  , plays = 0
  , previous_wager = 0
  , previous_win = TRUE
  )
  
  # vector to store budget over series of plays
  budget <- rep(NA, L)
  
  # For loop of plays
  for(i in 1:L){
    new_state <- state %>% one_play
    budget[i] <- new_state$B
    if(new_state %>% stop_play){
      return(budget[1:i])
    }
    state <- new_state
  }
  budget    
}

# helper function
get_last <- function(x) x[length(x)] 


# Simulation
walk_out_money <- rep(NA, 10000)
for(j in seq_along(walk_out_money)){
  walk_out_money[j] <- one_series(B = 200, W = 300, L = 1000, M = 100) %>% get_last
}

# Walk out money distribution
hist(walk_out_money, breaks = 100)

# Estimated probability of walking out with extra cash
mean(walk_out_money > 200)

# Estimated earnings
mean(walk_out_money - 200)
```



Solution 2 [(Video solution)](https://youtu.be/Bz7c24aAObg)
----------

``` r
single_spin <- function(){
  possible_outcomes <- c(rep("red",18), rep("black",18), rep("green",2))
  sample(possible_outcomes, 1)
}

martingale_wager <- function(
  previous_wager
  , previous_outcome
  , max_wager
  , current_budget
){
  if(previous_outcome == "red") return(1)
  min(2*previous_wager, max_wager, current_budget)
}

one_play <- function(previous_ledger_entry, max_wager){
  # Create a copy of the input object that will become the output object
  out <- previous_ledger_entry
  out[1, "game_index"] <- previous_ledger_entry[1, "game_index"] + 1
  out[1, "starting_budget"] <- previous_ledger_entry[1, "ending_budget"]
  out[1, "wager"] <- martingale_wager(
    previous_wager = previous_ledger_entry[1, "wager"]
    , previous_outcome = previous_ledger_entry[1, "outcome"]
    , max_wager = max_wager
    , current_budget = out[1, "starting_budget"]
  )
  out[1, "outcome"] <- single_spin()
  out[1, "ending_budget"] <- out[1, "starting_budget"] + 
    ifelse(out[1, "outcome"] == "red", +1, -1)*out[1, "wager"]
  return(out)
}

one_series <- function(
  max_games, starting_budget, winning_threshold, max_wager
){
  # Initialize ledger
  ledger <- data.frame(
      game_index = 0:max_games
    , starting_budget = NA_integer_
    , wager = NA_integer_
    , outcome = NA_character_
    , ending_budget = NA_integer_
  )
  ledger[1, "wager"] <- 1
  ledger[1, "outcome"] <- "red"
  ledger[1, "ending_budget"] <- starting_budget
  for(i in 2:nrow(ledger)){
    #browser()
    ledger[i,] <- one_play(ledger[i-1,], max_wager)
    if(stopping_rule(ledger[i,], winning_threshold)) break
  }
  # Return non-empty portion of ledger
  ledger[2:i, ]
}

stopping_rule <- function(
  ledger_entry
  , winning_threshold
){
  ending_budget <- ledger_entry[1, "ending_budget"]
  if(ending_budget <= 0) return(TRUE)
  if(ending_budget >= winning_threshold) return(TRUE)
  FALSE
}

profit <- function(ledger){
  n <- nrow(ledger)
  profit <- ledger[n, "ending_budget"] - ledger[1, "starting_budget"]
  return(profit)
}

require(magrittr)

svg(filename = "loser.svg", width=16, height =9)
par(cex.axis=2, cex.lab = 2, mar = c(8,8,2,2), bg = rgb(222, 235, 247, max = 255))
set.seed(1)
ledger <- one_series(200,200,300,500)
plot(ledger[,c(1,5)], type = "l", lwd = 5, xlab = "Game Index", ylab = "Budget")
dev.off()

svg(filename = "winner.svg", width=16, height =9)
par(cex.axis=2, cex.lab = 2, mar = c(8,8,2,2), bg = rgb(222, 235, 247, max = 255))
set.seed(2)
l2 <- one_series(200,200,300,500)
plot(l2[,c(1,5)], type = "l", lwd = 5, xlab = "Game Index", ylab = "Budget")
dev.off()
```
