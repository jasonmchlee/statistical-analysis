# Pet Adoption AB Test

# Overview
Currently the website has a static image of a cat on the home page. The cat is not smiling and looks rather sad. Next to the photo there is a CTA button saying "Adopt today" which would direct the user to a adoption application form. Our goal is to design a AB test to so we can understand if changing a photo on the landing page will increase conversions in users clicking the button. The scenario is we are analyzing the conversions for a pet adoption site.

For this experiment we will simply change the original cat photo, into a photo where the cat is smiling. Our hypothesis is "Changing the cat from a sad to happy photo will result in more people clicking on the "Adopt today" button".

![](https://github.com/jasonmchlee/statistical-analysis/blob/master/Pet%20Adoption%20AB%20Test/landing_page.png)

## Building the Experiment
When we look to create our control and test group we want to make sure we are accounting for factors such as seasonality. We see in our data that the summer would be when most conversion occurred.

We want to run the test and control simultaneously. Depending on we choose to run the AB test we will have different baseline conversions.

For example the conversions would be as follows if we were running it in:

- January - 20%
- July    - 33%
- August  - 54%
- October - 16%

As we can see there is a lot of fluctuations in our current conversions so we will want to take into account - POWER ANALYSIS.

### Power
How long do we run the experiment?

- Too short and we don't get enough insights
- Too long and we may be wasting resources
Power Analysis will tell you how many data points or sample size do we need to know to ensure the effect is real. Once we have the sample size you can figure how long we need to run the experiment to get the required data points.

For Power Analysis we should know:

- statistical test - statistical test we plan to run
- baseline value - value for the current control condition
- desired value - expected value for the test condition
- proportion of the data from the test condition (ideally 0.5)
- significance threshold / alpha = level where effect significant (generally 0.05)
- power / 1 -beta = probability correctly rejecting null hypothesis (generally 0.8)

## Analyzing Results

We have run the test and obtained the results from our control and test group. We have the information in a new CSV and we can explore the results below. We decided

![](https://github.com/jasonmchlee/statistical-analysis/blob/master/Pet%20Adoption%20AB%20Test/monthly%20conversions.png)

## Results
Looking at our results we can see the p-value is less than 0.05 our alpha so the results are still significant.

We can conclude that the new design on the landing page increased conversions, and we can roll it out to a larger population of our customers. For this we can determine that customers were accepting of the smiling cat photo and therefore went onto the next stage of clicking the button.

## Follow-Up Experiment
This is a continued project from our Pet adoption experiment. In this experiment we will follow up with the new design we implemented and see if we can build on the image that was used - a cat smiling.

Now, we want to see if an experiment that changes the smiling cat into a smiling kitten will improve conversion again.

Our hypothesis is "Changing the cat to a kitten will convert more users click on the "Adopt today" button".

From our previous experiment we saw that the increase in conversion was now ~38%. Going of intuition I believe that changing the photo from cat to kitten will have a significantly higher conversion. With that assumption I think the conversion rate will increase by 20% to 58%.

### Results
We can see the follow-up experiment didn't work (our p-value was about 0.29, which is not less than 0.05). This could be because kittens aren't actually that desirable, or because we went in with bad assumptions. We found our conversion results in our first experiment in January, but ran our second experiment in August, when conversion rates were already high. We have to remember to always consider what 'control' really means when building the follow-up experiments.

# Continued Experiment
## Plot 8 months data
Before starting the next experiment, let's take a second to look at the data so far from our original two conditions. Even though the happy cat did better initially, we decided to keep running both versions so you could see how results compared over more time.

![](https://github.com/jasonmchlee/statistical-analysis/blob/master/Pet%20Adoption%20AB%20Test/experiment_8months.png)

We can see there is a clear gap, with the happy cat performing better in conversions over the last 8 months. There is a slight dip from March to June, but relatively in the conversion range of ~47% to ~53%. Whereas it looks like the sad cat didn't break past the ~35% conversion mark.

# Follow up Experiment (Continued..)

Now we understand the month patterns in the data we can test out the power analysis to get the appropriate sample size and understand if our experiment performed well.

From our original experiment with the happy and sad cat the conversion rate was 38%. If we take the average of the 8 month difference and add it to the 30% we should get a baseline conversion.

The kitten landing page performed better, with a higher conversion rate at 75%. A 15% difference from the Cat photo, which is the close to the 18% average difference we had in the past.

Our follow-up experiment was successful! Now that we pulled the correct number of data points, we can see that there is a boost by using a kitten over a cat.

# Final Overview

With our goal to increase conversions in users clicking the "Adopt today" button on a pet adoption landing page we could see how the changes affected our results. In the first scenario we changed the original sad cat, to a happy cat and we saw our conversions performed better for the test group by 18% more (total 38% conversion).

After a successful test, we decided to roll out the happy cat to the entire population. We wanted to asses if could continue testing and improve conversions, so we looked into changing the happy cat to a happy kitten. We ran the test with a smaller samples size because we were hoping for a big jump in conversions with this change. Despite our assumptions, the result was not significant and there for we had to get a large sample size.

Before continuing with our follow up we decided to let our original happy/sad cat test continue to run over the next 8 months. We did this to see the longer term affects on the original test. After 8 months we say a relatively consistent conversion for the happy cat around 48-50% - continusouly outperforming the sad cat.

After gathering more data, we had better information to improve our assumptions on the baseline conversions. Now we tested the new converison baselines and got a more appropriate sample size for our follow up kitten test. Running the improved test, our results deemed to be significant and our Kitten group outperformed our cat group witha conversion of 75%. We now have a strong foundation to gradually keep building on our results.
