# Popcorn Time!!! Fortune Movie Productions getting ready to entertain you

## Business Problem

Fortune Movie Productions have decided to make their First Movie studio, and exploring what types of films are currently best at Box Office. We aim to evaluate which movie genres are faster reach to Audience, what type of movies makes best revenue, and who are the best directors/writers/actor whose movie hit Box Office.

**Goals:**

   - *Popular Movie Genres in today's trend*
   - *Which movie genre makes good revenue domestically and worldwide*
   - *Production Budget risks*
   - *Best Release date*


## Dataset:

We are using movie datasets for our analysis from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

We used IMDB database which has 8 Tables, 3 of the tables had necessary columns such as Genres, NumVotes, AverageRating ... for analysis. Similarly, Dataset TheMovieDB & TheNumbers were used to find which genre made Box office hit, and collected high revenue domestically & worldwide. 

For additional info regarding genre names and their corresponding numbers used in TheMovieDB Dataset for Data Cleaning, following source was used:
<a href = https://www.themoviedb.org/talk/5daf6eb0ae36680011d7e6ee >

## Dataset Evaluation & Visualization:

**Tableau Dashboard:** https://public.tableau.com/app/profile/yamuna.umapathy/viz/FortuneMovieProject/Dashboard1?publish=yes
<p align="center">

**Top Genres:** We were filtering the dataset with mean `vote_count` and mean `vote_average` to avoid rows which has high voteaverage and less votecounts, TheMovieDB Dataset was used for visualizing top 10 genres based on their `vote_count` and `genre_list`. Analysis shows Action, Animation, Adventure and Science Fiction was the trending genres with highest votecounts.

<p align="center">
  <img src = "  " width="566" height="133"
</p>

Based on above analysis, we were analyzing Top 4 genres `genre_list` and `vote_average` standings using Boxplot.

<p align="center">
  <img src = "https://github.com" width="566" height="133"
</p>

**Top Principals:** Table movie_ratings from IMDB Database, we created filtered dataframe using SQL query. Filtering movie_ratings with mean `numvotes` and `averagerating` and joining Table principals & Table persons for famous movie principals with best votes. Visualizing Top 5 Principals versus Total numvotes, analysis shows Action and Science Fiction movies have high votes, and directors/actors/producer in those movies became famous. 

<p align="center">
  <img src = "https://github.com" width="566" height="133"
</p>

**Budget:**: Next, focussing on Production budget risks. How this number depends on Gross revenue domestically and worldwide. Dataset tn_moviesbudget was used to visualize `production_budget_million` versus `domestic_gross_million` revenue. Analysis shows that Budget more than 200 million chosen carried greater risk.

<p align="center">
  <img src = "https://github.com" width="566" height="133"
</p>

**Genre Vs Revenue:** We used SQL database Table movie_basics, and merging with dataset TheNumbers to have columns `genre` and `domestic_gross_million` together. Merging the data using movie & primary_title as primary key. Visualizing which genre made best revenue, our analysis showed Animation and Adventure
has high revenue domestically and worldwide. Movies released worldwide is best option to increase revenue for these genres.

<p align="center">
  <img src = "https://github.com" width="566" height="133"
</p>

**Release Day:** Finally, we want to see what day of the week works best for movie release and earns best revenue. We are using TheMovieDB dataset, and visualizing `popularity` vs `release_day`. Analysis shows FRIDAY is the best day of the week to make more revenue in movie industry. 

<p align="center">
  <img src = "https://github.com" width="566" height="133"
</p>

## Conclusion & Recommendations:

**Genres:** Based on our analysis, top 4 genres are Animation, Action, Adventure and Science fiction.
**Revenue:** Animation and Adventure has the most domestic gross revenue, and earns twice for worldwide gross revenue, distributing worldwide makes the most revenue for these genres.
**Production Budget:** Considering budget 200 million or below carries lesser risk based on our analysis.
**Release Day:** Friday is recommended to be best day for release day, earns more revenue in the movie industry.

## Next Steps:

We can dive into deep analysis if we have more data from Awards database or other sources regarding best directors in each genre, low vs high budgets movies, TV-shows and International movies. 

## Repository Structure

```
├── zippedData
├── Images
├── .gitignore
├── presentation.pdf
├── index.ipynb
└── README.md
```
