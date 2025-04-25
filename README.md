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

---

## Hypothesis

- **H1:** The average number of moviegoers differs significantly across seasons.  
  (No assumption is made on which season is highest; the hypothesis tests whether differences exist.)

- **H2:** Certain movie genres are more popular during specific seasons  
  (e.g., **Action** and **Adventure** during Summer, **Drama** and **Thriller** during Winter).

### Difference Testing Approach:
- One-way **ANOVA** is applied to test for significant differences in moviegoer numbers across seasons.
- Genre distribution is analyzed by season to identify popularity patterns.

---

## Data Visualization
- **Bar Charts:** Show average weekly movie attendance by season.
- **Heatmaps:** Visualize total viewership per genre across seasons.


---

##  Notes
This analysis focuses on the **Top 10 weekly movies**.  
Although this reflects the dominant commercial trends, niche genres or independent films outside of the Top 10 may not be fully represented.

---

