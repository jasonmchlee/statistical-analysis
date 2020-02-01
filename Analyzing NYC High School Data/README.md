# Analyzing NYC High School Data

The SAT, or Scholastic Aptitude Test, is a test given to graduating high schoolers in the US every year. The SAT has 3 sections, each of which is worth a maximum of 800 points. The SAT is used by colleges to determine which students to admit. High average SAT scores are usually indicative of a good school.

New York City has published data on the SAT scores of students, along with additional demographic datasets.

  - SAT scores by school -- SAT scores for each high school in New York City.
  - School attendance -- attendance information on every school in NYC.
  - Class size -- class size information for each school in NYC.
  - AP test results -- Advanced Placement exam results for each high school. Passing AP exams can get you college credit in the US.
  - Graduation outcomes -- percentage of students who graduated, and other outcome information.
  - Demographics -- demographic information for each school.
  - School survey -- surveys of parents, teachers, and students at each school.

One of the most controversial issues in the U.S. educational system is the efficacy of standardized tests, and whether they're unfair to certain groups. Given our prior knowledge of this topic, investigating the correlations between SAT scores and demographics might be an interesting angle to take. We could correlate SAT scores with factors like race, gender, income, and more.

## Goal

The aim is to answer this question "Is there any correlation between the SAT score and demographics sich as race, gender income and more?"

## Correlations
How students and teachers percieved safety (saf_t_11 and saf_s_11) correlate with sat_score. This make sense, as it's hard to teach or learn in an unsafe environment.

## Exploring Schools With Low SAT Scores And Enrollment
There is an interesting cluster of points at the bottom left where total_enrollment and sat_score are both low. This cluster may be what is causing our r-value to be so high. It's worth extracting the names of the schools in this cluster, so we can research them more.

## Plotting Language Learning Percentage
From our research in the last screen, we found that most of the high schools with low total enrollment and low SAT scores are actually schools with a high percentage of English language learners enrolled. This indicates that it's actually ell_percent that correlates strongly with sat_score instead of total_enrollment. To explore this relationship more, let's plot out ell_percent vs sat_score.

## Mapping The Schools
It looks like ell_percent correlates with sat_score more strongly, because the scatterplot is more linear. However, there's still the cluster with very high ell_percent and low sat_score, which is the same group of international high schools that we investigated earlier.

In order to explore this relationship, we'll want to map out ell_percent by school district, so we can more easily see which parts of the city have a lot of English language learners.

## Calculating District Level Statistics
Unfortunately, due to the number of schools, it's hard to interpret the map we made in the last screen. It looks like uptown Manhattan and parts of Queens have a higher ell_percent, but we can't be sure. One way to make it easier to read very granular statistics is to aggregate them. In this case, we can aggregate based on district, which will enable us to plot ell_percent district by district instead of school by school.

## Safety And SAT Scores
There appears to be a correlation between SAT scores and safety, although it isn't that strong. It looks like there are a few schools with extremely high SAT scores and high safety scores. There are a few schools with low safety scores and low SAT scores. No school with a safety score lower than 6.5 has an average SAT score higher than 1500 or so.

## Racial differences in SAT scores
It looks like a higher percentage of white or asian students at a school correlates positively with sat score, whereas a higher percentage of black or hispanic students correlates negatively with sat score. This may be due to a lack of funding for schools in certain areas, which are more likely to have a higher percentage of black or hispanic students.

## Gender Differences In SAT Scores
We can see that a high percentage of females at a school positively correlates with SAT score, whereas a high percentage of males at a school negatively correlates with SAT score. Neither correlation is extremely strong.

## Ideas For Further Exploration
There's still quite a bit of analysis left to do. Here are some potential next steps:

  - Looking at class size and SAT scores.
  - Figuring out the best area to live in based on school performance.
  - If we combine this with a property values dataset, we could find the cheapest place where there are good school.
  - Looking into the differences between parent, teacher, and student responses to surveys.
  - Assigning a score to schools based on sat_score and other attributes.
