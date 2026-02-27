**Finding the Golden Era of Video Games**

This project explores whether video games have gotten better over time—and identifies which years could be considered the industry’s “golden era.” Using sales data and aggregated critic/user ratings for the top 400 games released since 1977, I analyze:

Which games sold the most

Which years had the highest average critic scores

Which years critics and users agreed were exceptional

The analysis is performed using SQL inside a Jupyter Notebook, and the dataset (game_sales.csv) contains curated video game records limited to 400 rows for this project.

**Project Objectives**

Using SQL, I generate three key tables:

1. best_selling_games

A table containing the top 10 best-selling games, sorted by games_sold in descending order.
All columns from the original game_sales table are included.

2. critics_top_ten_years

A table identifying the ten years with the highest average critic score, where:

At least 4 games were released in that year

Average critic scores are rounded to two decimals

Results include:

year

num_games

avg_critic_score

The years are sorted by critic score in descending order.
(For this query, I do not use the pre-computed critic ratings table.)

3. golden_years

This table identifies years where critics OR users rated games exceptionally highly.

A year is included if:

avg_critic_score > 9 OR

avg_user_score > 9

Using the pre-aggregated tables:

critics_avg_year_rating

users_avg_year_rating

I join both datasets and compute a new column:

diff → difference between critic and user averages

The final table includes:

year

num_games

avg_critic_score

avg_user_score

diff

Results are sorted by year (ascending).

**Background of the Study**

The global gaming industry is projected to surpass $300 billion by 2027, and major publishers are constantly trying to create the next big hit. This project aims to answer:

Are video games becoming better over time?

Did the industry experience a “golden age” where quality peaked?

How do user opinions align with critic reviews?

Which games achieved the highest commercial success?

By combining sales and ratings data, this analysis blends both business insights and consumer sentiment.

## Files Included

| File                          | Description                        |
| ----------------------------- | ---------------------------------- |
| **README.md**                 | Project documentation (this file)  |
| **notebook.ipynb**            | Full SQL analysis and DataFrames   |
| **game_sales.csv**            | Raw dataset of top 400 video games |
| **best_selling_games.csv**    | Output of query #1                 |
| **critics_top_ten_years.csv** | Output of query #2                 |
| **golden_years.csv**          | Output of query #3                 |
