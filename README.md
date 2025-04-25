# Seasonal Trends in Movie Viewership and Movie Genres

## Project Overview
This is the DSA210 Term Project by **Hilal Öngel**, a Sophomore Computer Science student at Sabancı University.  
The project analyzes the relationship between **seasons**, the **number of moviegoers**, and the **popularity of movie genres** in Turkey.

---

## Motivation
The film industry experiences fluctuations in moviegoer attendance throughout the year.  
Understanding how **seasons affect movie preferences and audience numbers** can provide valuable insights for movie studios, distributors, and marketers regarding their release strategies.  

Additionally, this topic is personally meaningful to me as I am interested in **data analysis, cinema, and human behavior patterns**.

---

## Data Sources
- **Box Office Turkey**  
  Weekly Top 10 movies and their audience numbers.  
  [https://boxofficeturkiye.com/](https://boxofficeturkiye.com/)

- **TMDB (The Movie Database) API**  
  Movie genre classification data.  
  [https://developer.themoviedb.org/reference/intro](https://developer.themoviedb.org/reference/intro)

---

## Data Collection
- Extract weekly **Top 10 movie data** from Box Office Turkey, including the number of moviegoers.
- Retrieve **movie genre information** from TMDB API.
- Categorize weekly data into four Turkish seasons:
  - **Winter:** Weeks 1–8 and 49–52  
  - **Spring:** Weeks 9–21  
  - **Summer:** Weeks 22–34  
  - **Autumn:** Weeks 35–48  

---

## Data Analysis
- **Viewership Trends:**  
  Identify seasonal fluctuations in the **average number of moviegoers**.
- **Genre Popularity:**  
  Determine which **genres perform better in different seasons**.
- **Difference Testing (ANOVA):**  
  Test whether **seasonal differences** in attendance are statistically significant.

  The analysis is based on weekly Top 10 box office data (raw data) scraped from Box Office Turkey.
The raw data was preprocessed by adding movie genre information from TMDB API, categorizing weeks into seasons, and exploding multi-genre entries into separate rows for proper analysis.

---

## Hypothesis

- **H1:** The average number of moviegoers differs significantly across seasons.  
  (No assumption is made on which season is highest; the hypothesis tests whether differences exist.)

- **H2:** Certain movie genres are more popular during specific seasons  
  (e.g., **Action** and **Adventure** during Summer, **Drama** and **Thriller** during Winter).

### Difference Testing Approach:
##  Difference Testing Approach

- One-way **ANOVA (Analysis of Variance)** was applied to test whether the average weekly movie attendance differs across seasons.
- **F-statistic:** 8.08  
- **p-value:** 0.0000
- Since the p-value is below 0.05, the null hypothesis was rejected, confirming that **seasonal differences in average weekly movie attendance are statistically significant**, which supports **Hypothesis 1**.

The **F-statistic** reflects the ratio of between-group variance (seasonal differences) to within-group variance (weekly fluctuations).  
The result indicates that at least two seasons significantly differ in their average audience numbers.  
This conclusion was visually supported by the **boxplot**, showing **Winter** as the season with the highest median weekly attendance and relatively low variability.

---

##  Hypothesis 2 Evaluation: Genre Popularity Patterns

To assess **Hypothesis 2**, the distribution of movie genres across seasons was analyzed after exploding multi-genre entries. The results showed clear seasonal genre preferences:

- **Action** and **Adventure** genres dominated **Summer**, aligning with blockbuster release strategies.
- **Drama** and **Thriller** genres were more popular in **Winter**, matching seasonal audience preferences for serious and emotional narratives.
- **Comedy** maintained stable popularity across the year but slightly increased in **Spring** and **Summer**.

Although no formal statistical test (e.g., chi-square) was applied to genre-season relationships in this project, the descriptive analysis strongly supports Hypothesis 2.  
Future work may apply statistical tests to validate these patterns formally.

---

##  Data Visualizations

-  **Bar Charts:** Show average weekly movie attendance by season.
-  **Heatmaps:** Visualize total viewership per genre across seasons.
-  **Stacked Bar Charts:** Display how each genre contributes to total viewership within each season.
-  **Boxplots:** Show weekly attendance distribution across seasons, supporting the variance analysis.


---
## 🔎 EDA (Exploratory Data Analysis) Methods Used

This project applies several **Exploratory Data Analysis (EDA)** techniques to understand the relationship between seasons, movie attendance, and genre popularity.

###  1. Grouping and Aggregation
- Calculated **average weekly moviegoer attendance** across seasons.
- Summarized **total viewership by genre and season**.
- **Tools:** `groupby()`, `mean()`, `sum()`, `pivot()`.

###  2. Data Cleaning and Preprocessing
- **Movie title cleaning** (removal of release dates, extra spaces).
- **Genre matching** using TMDB API.
- **Exploding multi-genre entries** so that each genre appears in a separate row.
- **Season categorization**: Assigned each week to one of the four seasons (Winter, Spring, Summer, Autumn).

###  3. Descriptive Statistics
- Used basic statistical measures like **mean, sum, and median**.
- Supported the identification of seasonal fluctuations and genre preferences.

###  4. Data Visualization
- **Bar Charts:** Visualized average weekly attendance by season.
- **Heatmaps:** Showed total viewership per genre across seasons.
- **Stacked Bar Charts:** Illustrated genre contribution to seasonal attendance.
- **Boxplots:** Displayed weekly viewership distribution across seasons.
- **Tools:** `matplotlib`, `seaborn`.

###  5. Statistical Testing (Supporting EDA)
- Applied **one-way ANOVA (Analysis of Variance)** to statistically test whether the seasonal differences in attendance are significant.
- Interpreted **F-statistic** and **p-value** to confirm or reject the null hypothesis.
- This statistical testing strengthened the insights obtained from the visual analysis.


---
##  Notes

This analysis focuses on the **Top 10 weekly movies**.  
Although this reflects the dominant commercial trends, niche genres or independent films outside of the Top 10 may not be fully represented.  
The methodology can be extended to larger datasets (Top 20, Top 50) or applied to streaming data for future research.

---



