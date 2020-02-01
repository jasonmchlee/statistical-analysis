# Probability for Winning the Lottery
Many people start playing the lottery for fun, but for some this activity turns into a habit which eventually escalates into addiction. Like other compulsive gamblers, lottery addicts soon begin spending from their savings and loans, they start to accumulate debts, and eventually engage in desperate behaviors like theft.

A medical institute that aims to prevent and treat gambling addictions wants to build a dedicated mobile app to help lottery addicts better estimate their chances of winning.

For the first version of the app, they want us to focus on the 6/49 lottery and build functions that enable users to answer questions like:

  - What is the probability of winning the big prize with a single ticket?
  - What is the probability of winning the big prize if we play 40 different tickets (or any other number)?
  - What is the probability of having at least five (or four, or three, or two) winning numbers on a single ticket?

The institute also wants us to consider historical data coming from the national 6/49 lottery game in Canada. The data set has data for 3,665 drawings, dating from 1982 to 2018.

Dataset available on Kaggle - [Dataset](https://www.kaggle.com/datascienceai/lottery-dataset)

## Building Functions
In the 6/49 lottery, six numbers are drawn from a set of 49 numbers that range from 1 to 49. A player wins the big prize if the six numbers on their tickets match all the six numbers drawn. If a player has a ticket with the numbers {13, 22, 24, 27, 42, 44}, he only wins the big prize if the numbers drawn are {13, 22, 24, 27, 42, 44}. If only one number differs, he doesn't win.

For the first version of the app, we want players to be able to calculate the probability of winning the big prize with the various numbers they play on a single ticket (for each ticket a player chooses six numbers out of 49).

## Historical Data
Earlier we wrote a function that can tell users what is the probability of winning the big prize with a single ticket. For the first version of the app, however, users should also be able to compare their ticket against the historical lottery data in Canada and determine whether they would have ever won by now.

Now, we'll focus on exploring the historical data coming from the Canada 6/49 lottery.

The data set contains historical data for 3,665 drawings (each row shows data for a single drawing), dating from 1982 to 2018. For each drawing, we can find the six numbers drawn in the following six columns:

- NUMBER DRAWN 1
- NUMBER DRAWN 2
- NUMBER DRAWN 3
- NUMBER DRAWN 4
- NUMBER DRAWN 5
- NUMBER DRAWN 6

## Function for Lotto Checker
We need to be aware of the following details:

  - Inside the app, the user inputs six different numbers from 1 to 49.
  - Under the hood, the six numbers will come as a Python list and serve as an input to our function.
  - The engineering team wants us to write a function that prints:
        - the number of times the combination selected occurred in the Canada data set; and
        - the probability of winning the big prize in the next drawing with that combination.
        
        
## Smaller Winning Options
In most 6/49 lotteries there are smaller prizes if a player's ticket match two, three, four, or five of the six numbers drawn. As a consequence, the users might be interested in knowing the probability of having two, three, four, or five winning numbers.

  - Inside the app, the user inputs:
      - six different numbers from 1 to 49; and
      - an integer between 2 and 5 that represents the number of winning numbers expected
  - Our function prints information about the probability of having the inputted number of winning numbers.

To calculate the probabilities, the specific combination on the ticket is irrelevant and we only need the integer between 2 and 5 representing the number of winning numbers expected. Consequently, we will write a function named probability_less_6() which takes in an integer and prints information about the chances of winning depending on the value of that integer.

The function below calculates the probability that a player's ticket matches exactly the given number of winning numbers. If the player wants to find out the probability of having five winning numbers, the function will return the probability of having five winning numbers exactly (no more and no less). The function will not return the probability of having at least five winning numbers.

## Final thoughts
We were able to define 4 functions that can understand probability of winning the lottery:

  - one_ticket_probability() — calculates the probability of winning the big prize with a single ticket
  - check_historical_occurrence() — checks whether a certain combination has occurred in the Canada lottery data set
  - multi_ticket_probability() — calculates the probability for any number of of tickets between 1 and 13,983,816
  - probability_less_6() — calculates the probability of having two, three, four or five winning numbers exactly
