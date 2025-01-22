# Premier-League-Club-Investment-Analysis
Python Project 

## Introduction

This project is focused on analyzing the performance of Premier League clubs with the objective of identifying potential clubs for investment. The analysis utilizes data from 29 clubs that have participated in the Premier League, examining performance metrics such as the number of wins, losses, draws, goals scored, and historical success (including titles won and runner-up finishes). The goal is to identify lesser-known clubs that have the potential to perform well in the future, which would be suitable for investment.

## Objective

The main goal of this project is to provide data-driven insights into Premier League clubs that could be viable investment opportunities. The analysis helps decision-makers understand which clubs have the potential to succeed in the future, even if they have less experience or fewer accolades. By utilizing various data manipulation and visualization techniques, the project identifies clubs with high growth potential, based on their historical performance, winning rates, and recent form.

## Steps-by-Step Analysis

### 1. **Data Cleaning**

- **Removing Unwanted Characters:** The `Club` column contained numerical values at the beginning of the club names. We used a regular expression to clean these values, leaving only the club names.
  
- **Handling Null Values:** We identified and replaced missing values in the `Winners` and `Runners-up` columns. For the `Winners` column, we filled missing values with `0`, as these clubs have not won the Premier League. Similarly, the `Runners-up` column had some inconsistencies, with values such as `'-'` and `null`, which were also replaced with `0`.

- **Data Type Conversion:** The `Runners-up` column had an object data type and was converted into an integer. Additionally, the `TeamLaunch` and `lastplayed_pl` columns were cleaned and standardized into proper year formats to facilitate further analysis.

### 2. **Data Manipulation**

- **Normalization of Metrics:** To analyze the performance of each club, we normalized various performance metrics (e.g., wins, losses, draws, clean sheets, and goals) by dividing them by the number of matches played. This allowed us to calculate rates such as:
  - **Winning Rate**
  - **Loss Rate**
  - **Draw Rate**
  - **Clean Sheet Rate**
  - **Average Goals Per Match**

- **Scoring System:** A custom scoring system was created to rank clubs based on several performance factors. Each club was assigned scores based on:
  - **Experience (matches played)**
  - **Winning and Loss Rates (based on interquartile ranges)**
  - **Clean Sheet Rate**
  - **Recent Performance (i.e., last played in 2023, 2022, or 2021)**

### 3. **Data Visualization**

- **Histogram:** A histogram was used to visualize the distribution of the number of matches played by each club, revealing a few clubs with significantly higher experience in the Premier League.
  
- **Boxplot:** A boxplot was used to visualize the distribution of the winning rate, losing rate, drawn rate, and clean sheet rate. This highlighted outliers, such as clubs with exceptional winning rates and high drawn rates.

- **Bar Chart:** A bar chart was generated to display the clubs' performance scores after calculating the weighted scores based on various metrics.

### 4. **Final Recommendation**

- **Ranking of Clubs:** After analyzing the clubs' performance, we ranked the clubs based on their scores. Clubs with higher experience, a strong winning rate, low loss rates, and high clean sheet rates were given higher scores.

- **Focus on Recent Performance:** We gave higher priority to clubs that have played in recent years (2021, 2022, or 2023), as their current form is more indicative of future potential.

- **Investment Recommendation:** Based on the scores and the analysis, **Leicester City** was recommended as a top investment option due to their consistent top 10 finishes in recent years and their strong performance history, whereas clubs like **Blackburn Rovers**, who have not participated in the Premier League since 2012, were not recommended for investment.

## Conclusion

This project provides a comprehensive analysis of Premier League clubs, using data cleaning, manipulation, and visualization techniques to identify the best investment opportunities. By scoring each club based on key performance indicators, we can confidently recommend clubs with high potential for future success. Our recommendation highlights **Leicester City** as a promising investment, with their recent form and historical performance positioning them well for future growth in the Premier League.
