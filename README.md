# 🎬 Netflix Movies & TV Shows Data Analysis (Python)
<p align="center">
  <img src="https://github.com/Mazen-Alattar/netflix-eda-python/blob/main/netflix-eda-python/images/netflix.jpg?raw=true" width="1000">
</p>

## 📌 Project Overview
This project performs an **Exploratory Data Analysis (EDA)** on the *Netflix Movies and TV Shows* dataset to uncover content trends, distribution patterns, and insights related to Netflix’s catalog.

The project focuses heavily on **data cleaning, feature engineering, and insightful visual analysis** using Python libraries, making it a strong portfolio project for **Data Analyst Internship** roles.

---

## 🗂 Dataset Information
- **Source:** Kaggle
- **Dataset:** Netflix Movies and TV Shows
- **Domain:** Entertainment / Streaming Content

### Original Columns
- show_id  
- type  
- title  
- director  
- cast  
- country  
- date_added  
- release_year  
- rating  
- duration  
- listed_in  
- description  

---

## 🔄 Data Cleaning & Preparation

### Missing Values Analysis
Initial missing values per column:
director 2634
cast 825
country 831
date_added 10
rating 4
duration 3

### Rating & Duration Issues
- Some records had **incorrect values swapped between `rating` and `duration`**.
- These mismatches were manually identified and corrected.
- Missing `rating` values were filled by **researching each title individually** to ensure accuracy.

### Date Issues
- There were **10 unknown or invalid dates** in the `date_added` column.
- These dates were manually retrieved by searching based on the movie or TV show title.

### Handling Missing Categorical Data
- `country` was filled using the **mode** (most frequent value).
- `director` and `cast` missing values were filled with **"Unknown"** to preserve records.

### Data Type Fixes
- Converted `date_added` from object to **datetime**.
- Ensured numeric consistency for duration-related fields.

---

## 🧱 Feature Engineering

### Rating Grouping
- The original `rating` column contained many unclear or inconsistent categories.
- A new column **Rating Group** was created to map ratings into clearer, high-level categories suitable for analysis.

### Genre Simplification
- The `listed_in` column contained multiple genres per title.
- A new column **Main Genre** was extracted to represent the primary genre only.

### Date-Based Features
From the cleaned `date_added` column, the following features were created:
- **Year Added**
- **Month Name Added**

---

## 🗑 Columns Removed
The following columns were dropped after cleaning and feature extraction:

- `show_id`
- `date_added`
- `description`
- `rating`

These columns were either redundant, replaced by engineered features, or not required for analysis.

---
## 📊 Analysis Preview
<table>
  <tr>
    <td>
      <img src="https://github.com/Mazen-Alattar/netflix-eda-python/blob/main/netflix-eda-python/images/dist_of_netflix_titles_by_type.png?raw=true" width="400">
    </td>
    <td>
      <img src="https://github.com/Mazen-Alattar/netflix-eda-python/blob/main/netflix-eda-python/images/dist_of_rating_groups_on_netflix.png?raw=true" width="400">
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/Mazen-Alattar/netflix-eda-python/blob/main/netflix-eda-python/images/netflix_titles_by_release_year&type.png?raw=true" width="400">
    </td>
    <td>
      <img src="https://github.com/Mazen-Alattar/netflix-eda-python/blob/main/netflix-eda-python/images/top_10_countries_by_number_of_titles.png?raw=true" width="400">
    </td>
  </tr>
</table>


---

## 📊 Exploratory Data Analysis & Insights

### Key Analyses Performed
- **Distribution of Netflix Titles by Type** (Movies vs TV Shows)
- **Content Added to Netflix per Year**
- **Distribution of Content by Rating Group**
- **Top 10 Countries by Number of Titles (Movies vs TV Shows)**
- **Distribution of Movie Durations (Minutes)**
- **Trend of Netflix Titles by Release Year and Type**
- **Trend of Netflix Titles by Release Month and Type**

### Insights Highlights
- Movies significantly outnumber TV Shows in Netflix’s catalog.
- The number of titles added per year has increased sharply in recent years.
- Certain rating groups dominate Netflix content, reflecting target audience strategy.
- A small number of countries contribute the majority of Netflix titles.
- Most movies fall within a specific duration range, indicating standardized content length.
- Seasonal and yearly trends show clear patterns in content release strategies.

---

## 📈 Visualizations
The analysis includes a variety of visualizations using:
- Bar charts
- Line charts
- Distribution plots
- Comparative charts (Movies vs TV Shows)
- Interactive plots using **Plotly** where appropriate

---

## 🛠 Tools & Libraries Used
- **Python**
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- Jupyter Notebook

---

## 🎯 Project Goal
This project was created as part of a **data analytics portfolio** to demonstrate:
- Strong data cleaning and preprocessing skills
- Feature engineering for better analysis
- Exploratory data analysis using Python
- Insight-driven storytelling with data visualizations  

Designed for **Data Analyst Internship** and entry-level data roles.

