# Women's National Basketball Association (WNBA)
The data set is about basketball players in WNBA (Women's National Basketball Association), and contains general information about players, along with their metrics for the season 2016-2017. The data set was put together by Thomas De Jonghe, and can be downloaded from Kaggle, where you can also find useful documentation for the data set.

## Overview
In this project I willl focus on using various sampling methods to assit with looking into frequency distributions.

## Simple Random Sampling
When we sample we want to minimize the sampling error as much as possible. We want our sample to mirror the population as closely as possible.

If we sampled to measure the mean height of adults in the US, we'd like our sample statistic (sample mean height) to get as close as possible to the population's parameter (population mean height). For this to happen, we need the individuals in our sample to form a group that is similar in structure with the group forming the population.

The US adult population is diverse, made of people of various heights. If we sampled 100 individuals from various basketball teams, then we'd almost certainly get a sample whose structure is significantly different than that of the population. As a consequence, we should expect a large sampling error (a large discrepancy between our sample's statistic (sample mean height) and the population's parameter (population mean height)).

In statistical terms, we want our samples to be representative of their corresponding populations. If a sample is representative, then the sampling error is low. The more representative a sample is, the smaller the sampling error. The less representative a sample is, the greater the sampling error.

To make our samples representative, we can try to give every individual in the population an equal chance to be selected in our samples. We want a very tall individual to have the same chance as being selected as an individual having a medium or short height. To give every individual an equal chance of being picked, we need to sample randomly - using a simple stratified sample.

 ( PICTURE)
 
We can notice that the sample means vary a lot around the population mean. With a minimum sample mean of 115 points, a maximum of 301.4, and a population mean of roughly 201.8, we can tell that the sampling error is quite large for some of the cases.

Because sample means vary a lot around the population mean, there's a good chance we get a sample that is not representative of the population.

This problem can be solved by increasing the sample size. As we increase the sample size, the sample means vary less around the population mean, and the chances of getting an unrepresentative sample decrease.

Because simple random sampling is entirely random, it can leave out certain population individuals that are of great interest to some of the questions we may have.

For example, players in basketball play in different positions on the court. The metrics of a player (number of points, number of assists, etc.) depend on their position, and we might want to analyze the patterns for each individual position. If we perform simple random sampling, there's a chance that some categories won't be included in our sample. In other words, it's not guaranteed that we'll have a representative sample that has observations for every position we want to analyze.

## Stratified Sampling
To ensure we end up with a sample that has observations for all the categories of interest, we can change the sampling method. We can organize our data set into different groups, and then do simple random sampling for every group. We can group our data set by player position, and then sample randomly from each group.

This sampling method is called stratified sampling, and each stratified group is also known as a stratum.

Approximately 72.7% of the players had more than 23 games for the 2016-2017 season, which means that the mean of the total points is probably influenced by this category of players who played a lot of games.

The ( character indicates that the beginning of the interval is not included, and the ] indicates that the endpoint is included. For example, (22.0, 32.0] means that 22.0 isn't included, while 32.0 is, and the interval contains this array of numbers: [23, 24, 25, 26, 27, 28, 29, 30, 31, 32].

When we compute the mean of the total points using the population (the entire data set), the mean will probably be signficantly influenced by those 72.7% players who played more than 23 games. However, when we sample randomly, we can end up with a sample where the proportions are different than in the population.

For instance, we might end up with a sample where only 2% of the players played more than 23 games. This will result in a sample mean which underestimates the population mean. Or we could have a sample where more than 95% of the players had 23 games in the 2016-2017 season. This will result in overestimating the population mean. This scenario of under or over estimation is common for small samples.

One solution to this problem is to use stratified sampling while being mindful of the proportions in the population. We can stratify our data set by the number of games played, and then sample randomly from each stratum a proportional number of observations.



(Pictrure)


The variability of the sampling was quite large, and many sample means were unrepresentative, being far from the population mean. In fact, this sampling method doesn't seem to perform better than simple random sampling.

The poor performance is caused by a bad choice of strata. We stratified the data by the number of games played, but this isn't a good approach. A player is considered as having played one game even if she only played for one or two minutes. But others play 30 or 40 minutes, and they're still considered as having played one game.

It makes more sense to stratify the data by number of minutes played, rather than by number of games played. The minutes played are a much better indicator of how much a player scored in a season than the number of games played.



## Frequency Distributions
One way to simplify this data set is to select a variable, count how many times each unique value occurs, and represent the frequencies (the number of times a unique value occurs) in a table. This is how such a table looks for the POS (player position) variable.

Because proportions and percentages are relative to the total number of instances in some set of data, they are called relative frequencies. In contrast, the frequencies we've been working with so far are called absolute frequencies because they are absolute counts and don't relate to the total number of instances.

### Position Frequency

### Years of Experience

### Points Scored

### Level of Experience


 ## Density Plots
 
 ## Stripplots
 
Patterns are now immediately visible. We can see on the graph that the shortest players are guards — in fact, all players under 180 cm are guards. The tallest players are centers — this is the only category with players above 2 meters. Among combined positions, we can see that F/C has slightly taller representatives — most likely because it requires center qualities (and we've seen that the tallest players are generally centers).


 ## Boxplots
 
 
The few dots we see for the box plots of centers and guards/forwards (G/F) represent values in the distribution that are much larger or much lower than the rest of the values. A value that is much lower or much larger than the rest of the values in a distribution is a outlier.


