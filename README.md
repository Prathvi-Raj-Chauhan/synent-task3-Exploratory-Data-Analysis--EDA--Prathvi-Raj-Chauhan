# Netflix Movies and TV Shows Data Analysis

## Problem Statement

The objective of this project is to perform exploratory data analysis (EDA) on Netflix's catalog of movies and TV shows to identify content trends, distribution patterns, duration characteristics, ratings distribution, and country-wise content production.

The analysis aims to provide insights into Netflix's content library and understand how content characteristics have evolved over time.

---

## Dataset Details

**Dataset:** Netflix Movies and TV Shows Dataset

**Source:** Kaggle

**Link:** https://www.kaggle.com/datasets/muqaddasejaz/netflix-movies-and-tv-shows-dataset

### Dataset Overview

* Total Records: **8,807**
* Total Features: **12**
* Content Types:

  * Movies
  * TV Shows

### Features

| Feature      | Description                              |
| ------------ | ---------------------------------------- |
| show_id      | Unique identifier for each title         |
| type         | Movie or TV Show                         |
| title        | Name of the content                      |
| director     | Director(s) of the content               |
| cast         | Main cast members                        |
| country      | Country of production                    |
| date_added   | Date added to Netflix                    |
| release_year | Original release year                    |
| rating       | Content rating (TV-MA, PG, etc.)         |
| duration     | Duration in minutes or number of seasons |
| listed_in    | Genres/categories                        |
| description  | Brief description of the content         |

---

## Data Exploration and Cleaning

### Missing Values Analysis

The dataset contains missing values in several columns:

| Column     | Missing Values |
| ---------- | -------------- |
| director   | 2634           |
| cast       | 825            |
| country    | 831            |
| date_added | 10             |
| rating     | 4              |
| duration   | 3              |

The missing values were identified to understand data quality before performing further analysis.

---

## Feature Engineering

Since the duration column contains different formats for movies and TV shows, separate processing was performed.

### Movie Duration Extraction

Movie durations were extracted from strings such as:

```text
90 min
120 min
150 min
```

and converted into numerical values representing minutes.

A new feature was created:

```text
duration_min
```

### TV Show Seasons Extraction

For TV shows, season counts were extracted from values such as:

```text
1 Season
2 Seasons
5 Seasons
```

and stored as a numerical feature:

```text
num_seasons
```

---

## Exploratory Data Analysis

### 1. Movie Duration Distribution

A histogram was generated to analyze the distribution of movie lengths.

#### Observations

* Most movies fall between 80 and 120 minutes.
* Extremely short and extremely long movies are relatively rare.
* The distribution is concentrated around standard feature-film durations.

---

### 2. TV Show Season Distribution

A bar chart was created to visualize the number of seasons for TV shows.

#### Observations

* Most TV shows have only 1 or 2 seasons.
* Multi-season shows exist but become increasingly less common as season count increases.
* Long-running series represent a small portion of the catalog.

---

### 3. Correlation Analysis

#### Movies

Correlation between release year and movie duration:

| Variable Pair            | Correlation |
| ------------------------ | ----------- |
| Release Year vs Duration | -0.206      |

#### Interpretation

* Weak negative correlation.
* Newer movies tend to be slightly shorter on average.
* Release year is not a strong predictor of movie duration.

---

#### TV Shows

Correlation between release year and number of seasons:

| Variable Pair                     | Correlation |
| --------------------------------- | ----------- |
| Release Year vs Number of Seasons | -0.090      |

#### Interpretation

* Very weak negative correlation.
* Almost no relationship exists between release year and season count.
* Release year does not significantly influence the number of seasons.

---

### 4. Content Release Trends Over Time

The number of titles released each year was analyzed.

#### Observations

* Netflix content production increased significantly in recent years.
* The highest concentration of titles appears in the modern streaming era.
* Older content represents a smaller portion of the catalog.

This trend reflects Netflix's rapid expansion of original and licensed content.

---

### 5. Movies vs TV Shows

A comparison was performed between the number of movies and TV shows available on Netflix.

#### Findings

* Movies constitute the majority of Netflix content.
* TV shows represent a smaller but substantial portion of the catalog.

Based on the dataset:

| Content Type | Approximate Count |
| ------------ | ----------------- |
| Movies       | 6131              |
| TV Shows     | 2676              |

Movies account for roughly 70% of the available content.

---

### 6. Content Ratings Analysis

The most frequently occurring content ratings were analyzed.

#### Observations

* TV-MA is the most common rating.
* Mature audience content dominates the platform.
* Family and children's ratings appear less frequently compared to adult-oriented content.

This indicates Netflix's strong focus on content targeted toward older audiences.

---

### 7. Country-wise Content Production

The top content-producing countries were identified.

#### Observations

* The United States contributes the largest amount of content.
* India is among the leading content-producing countries.
* Several countries contribute international movies and TV shows, highlighting Netflix's global reach.

The analysis demonstrates Netflix's investment in both domestic and international content production.

---

## Key Findings

1. Netflix's catalog contains more movies than TV shows.
2. Most movies have durations between 80 and 120 minutes.
3. Most TV shows consist of only 1 or 2 seasons.
4. Release year has little influence on content duration.
5. Content production has increased substantially in recent years.
6. TV-MA is the most common content rating.
7. The United States is the leading content-producing country.
8. Netflix maintains a diverse international content library.

---

## Results Summary

| Analysis                    | Result        |
| --------------------------- | ------------- |
| Total Titles                | 8,807         |
| Movies                      | 6,131         |
| TV Shows                    | 2,676         |
| Movie Duration Correlation  | -0.206        |
| TV Show Seasons Correlation | -0.090        |
| Most Common Rating          | TV-MA         |
| Largest Producing Country   | United States |

---

## Conclusion

This project explored the Netflix Movies and TV Shows dataset through comprehensive exploratory data analysis. The study examined content distribution, duration characteristics, release trends, ratings, and country-wise production patterns.

The results reveal that Netflix is primarily movie-focused, with movies making up approximately 70% of its catalog. Most movies follow standard feature-length durations, while TV shows are typically limited to one or two seasons. The analysis also showed that release year has little effect on content duration and that Netflix's content library has expanded rapidly over time.

Additionally, the platform is dominated by mature-audience content, with TV-MA being the most common rating, and the United States serving as the largest contributor of titles.

Overall, the analysis provides valuable insights into Netflix's content strategy and the composition of its global streaming catalog.

## Future Work

Possible extensions of this project include:

* Genre-wise content analysis
* Recommendation system development
* Sentiment analysis of descriptions
* Director and actor network analysis
* Country-wise growth trend analysis
* Content addition trends over time
* Machine learning models for content popularity prediction
