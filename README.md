# Which Is the Best Team Ever in Italian Soccer?

**Advanced Data Science — Data Challenge**

This project explores Italian Serie A match results from the **1993/94 season onward** using data published by [Football-Data](https://www.football-data.co.uk/italym.php). The aim is to prepare a reproducible analysis of team performance over time and investigate what it means to be the “best” team.

**Repository:** [Team Serie A — GitHub](REPLACE_WITH_YOUR_GITHUB_REPOSITORY_URL)

> Replace `REPLACE_WITH_YOUR_GITHUB_REPOSITORY_URL` with the actual GitHub repository link after creating or identifying your repository.

## Original assignment

> **Which is the best team ever in Italian soccer?**
>
> This challenge explores all matches of Italian soccer Serie A league from 1993 to current year. The dataset is contained in the website [football-data.co.uk](http://www.football-data.co.uk/italym.php).
>
> ### Challenges
>
> 1. Think about how to scrape the data from the website, but write no code at this stage.
> 2. Ask AI to write code to import data by scraping the website. Select only columns Date, HomeTeam, AwayTeam, FTHG (home team goals), FTAG (away team goals) and filter rows with a valid (not NA) Date.
> 3. Using dplyr and tidyr packages (no for loops!), compute statistics for every team (matches, wins, loses, draws, points, points per match). Hint: mutate a column with the outcome of the match (for instance, H = home teams wins, A = away team wins, P = draw). Then group by team and outcome (home and away) and hence spread the outcome. Do this step without the use of AI.
> 4. Come up with at least 3 data questions on the data at hand. Just write the questions, do not find the answers.

## Data source and variables

Source: [Football-Data — Italian football results](https://www.football-data.co.uk/italym.php). The site provides season-level CSV files for Serie A (`I1.csv`). The analysis retains the following variables:

| Column | Description |
| --- | --- |
| `Date` | Match date |
| `HomeTeam` | Home team |
| `AwayTeam` | Away team |
| `FTHG` | Full-time home goals |
| `FTAG` | Full-time away goals |

Rows with missing match dates are removed. For performance statistics, only matches with recorded final scores should be counted. The current season may be incomplete.

## Project files

```text
serie-a-data-challenge/
├── README.md
├── TeamSerieA.Rmd      # Source code and analysis
├── TeamSerieA.html     # Rendered report (after knitting)
└── data/                # Optional local data/cache
```

## Requirements

- R and RStudio
- R packages: `tidyverse`, `rvest`, `rmarkdown`, `knitr`

Install packages in the RStudio Console if needed:

```r
install.packages(c("tidyverse", "rvest", "rmarkdown", "knitr"))
```

## How to run

1. Clone or download this repository.
2. Open `TeamSerieA.Rmd` in RStudio.
3. Execute the R code chunks in order and inspect the outputs.
4. Complete the team-statistics section independently using `dplyr` and `tidyr`, without `for` loops or AI-generated code, as required by the assignment.
5. Click **Knit** to produce `TeamSerieA.html`.
6. Review the HTML report before submitting it.

## Methodology

1. Inspect the source webpage and identify Serie A season CSV links.
2. Import and combine the season files.
3. Keep the five required fields and exclude rows with missing dates.
4. Calculate team-level matches, wins, losses, draws, points and points per match.
5. Formulate at least three research questions without answering them in Challenge 4.

**Comparability note:** Serie A changed from two to three points per win beginning with the 1994/95 season. Any cross-season comparison of points should explicitly define a consistent scoring convention.

## Submission

Submit the `.Rmd` source and knitted `.html` report in the same GitHub folder, then send the permanent folder link to the course instructor from your academic email, including your first and last name. Follow the assignment's seven-day submission deadline.

## Attribution

Data: [Football-Data.co.uk](https://www.football-data.co.uk/italym.php). The scraping/import code may be AI-assisted as permitted by Challenge 2; the team-statistics work in Challenge 3 must be completed independently.
