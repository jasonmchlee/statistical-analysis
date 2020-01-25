# Fandango

## Overview
In October 2015, Walt Hickey from FiveThirtyEight published a popular article where he presented strong evidence which suggest that Fandango’s movie rating system was biased and dishonest.

[RPubs Publication](http://rpubs.com/jasonmchlee/fandango)

## Objective
In this project, we’ll analyze more recent movie ratings data to determine whether there has been any change in Fandango’s rating system after Hickey’s analysis.

## Results
Our analysis showed that there’s indeed a slight difference between Fandango’s ratings for popular movies in 2015 and Fandango’s ratings for popular movies in 2016. We also determined that, on average, popular movies released in 2016 were rated lower on Fandango than popular movies released in 2015.

## Dataset
This directory contains the data behind the story [Be Suspicious Of Online Movie Ratings, Especially Fandango’s](http://fivethirtyeight.com/features/fandango-movies-ratings/).

`fandango_score_comparison.csv` contains every film that has a Rotten Tomatoes rating, a RT User rating, a Metacritic score, a Metacritic User score, and IMDb score, and at least 30 fan reviews on Fandango. The data from Fandango was pulled on Aug. 24, 2015.

Column | Definition
--- | -----------
FILM | The film in question
RottenTomatoes | The Rotten Tomatoes Tomatometer score  for the film
RottenTomatoes_User | The Rotten Tomatoes user score for the film
Metacritic | The Metacritic critic score for the film
Metacritic_User | The Metacritic user score for the film
IMDB | The IMDb user score for the film
Fandango_Stars | The number of stars the film had on its Fandango movie page
Fandango_Ratingvalue | The Fandango ratingValue for the film, as pulled from the HTML of each page. This is the actual average score the movie obtained.
RT_norm | The Rotten Tomatoes Tomatometer score  for the film , normalized to a 0 to 5 point system
RT_user_norm | The Rotten Tomatoes user score for the film , normalized to a 0 to 5 point system
Metacritic_norm | The Metacritic critic score for the film, normalized to a 0 to 5 point system
Metacritic_user_nom | The Metacritic user score for the film, normalized to a 0 to 5 point system
IMDB_norm | The IMDb user score for the film, normalized to a 0 to 5 point system
RT_norm_round | The Rotten Tomatoes Tomatometer score  for the film , normalized to a 0 to 5 point system and rounded to the nearest half-star
RT_user_norm_round | The Rotten Tomatoes user score for the film , normalized to a 0 to 5 point system and rounded to the nearest half-star
Metacritic_norm_round | The Metacritic critic score for the film, normalized to a 0 to 5 point system and rounded to the nearest half-star
Metacritic_user_norm_round | The Metacritic user score for the film, normalized to a 0 to 5 point system and rounded to the nearest half-star
IMDB_norm_round | The IMDb user score for the film, normalized to a 0 to 5 point system and rounded to the nearest half-star
Metacritic_user_vote_count | The number of user votes the film had on Metacritic
IMDB_user_vote_count | The number of user votes the film had on IMDb
Fandango_votes | The number of user votes the film had on Fandango
Fandango_Difference | The difference between the presented Fandango_Stars and the actual Fandango_Ratingvalue


`fandango_scrape.csv` contains every film we pulled from Fandango.

Column | Definiton
--- | ---------
FILM | The movie
STARS | Number of stars presented on Fandango.com
RATING |  The Fandango ratingValue for the film, as pulled from the HTML of each page. This is the actual average score the movie obtained.
VOTES | number of people who had reviewed the film at the time we pulled it.
