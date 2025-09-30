# MICROSOFT MOVIE STUDIO INSIGHT

## PROJECT OVERViEW
- The aim of this project is to analyze which type of films are currently doing the best at the box office to help the company decide which type of films to create.

## BUSINESS PROBLEM
- A company has decided to create a new movie studio, but they don’t know anything about creating movies. We are charged with exploring what types of films are currently doing the best at the box office. We must then translate those findings into actionable insights that the head of this company's new movie studio can use to help decide what type of films to create.

## PROJECT GOAL

- To identify the key factors that drive movie success (financially and with audiences) in order to guide the new movie studio on what types of films to produce, invest in, and promote.

##  Objectives

1. **Identify high-performing movie genres** based on average viewer ratings and worldwide gross revenue.
2. **Determine which directors, writers, and actors** are associated with top-performing movies.
3. **Assess the impact of production budgets** on movie performance.

##  Datasets

- **IMDb (SQLite Database: `im.db`)**
  - `movie_basics`
  - `movie_ratings`
  - `directors`
  - `persons`

- ** (`tn.movie_budgets.csv.gz`)**
  - Contains data on production budgets and worldwide gross.

## Tools & Libraries
### python
`import pandas as pd`
`import gzip`
`import numpy as np`
`import sqlite3`
`import matplotlib.pyplot as plt`
`%matplotlib inline`
`import seaborn as sns`
`import scipy.stats as stats`

## Data Preparation Steps
- Loaded and merged IMDb and The Numbers datasets.

- Filtered top 10 genres based on frequency.

- Exploded multi-genre rows for genre-level analysis.

- Assigned experience levels to directors and actors.

- Binned production budgets and worldwide gross into Low, Medium, and High categories.

- Merged and cleaned all relevant tables for analysis.

## Exploratory Data Analysis (EDA)
**1. Genre vs. Performance**
### Research Question:
- Can average rating be used as an indicator of film performance?

### Hypotheses:

- H0: No significant difference exists between genres and average ratings.

- H1: A significant difference exists between genres and average ratings.

### Visualizations:

- Bar plot of average rating by genre

- Bar plot of average worldwide gross by genre

### ANOVA test to assess significance

 **Director, Writer, and Actor Influence**
### Steps:

- Calculated number of movies each director has made (experience count)

- Mapped experience to names

- Filtered data to top 10 genres for focused analysis

### Visualizations:
- **Box plot of Average ratings by Genre**
  ![image](https://github.com/user-attachments/assets/13fcb1af-dd55-474e-89a7-9508307dc9fe)



  
- **Bar plots of average rating by top directors per genre**
  ![image](https://github.com/user-attachments/assets/016cb8f7-9b75-48c6-aaa5-5482e2985c2c)





- **Bar plots of average rating by top actors per genre**
![image](https://github.com/user-attachments/assets/137c344d-afd9-42b2-a7a6-9a8b17513e38)





- **Heat map to visualize the association between production budget and worldwide gross categories**
  ![image](https://github.com/user-attachments/assets/2493d452-b8a3-457a-be8f-b96c57485575)



  
**2. Budget vs. Movie Performance**
### Hypotheses:

- H0: No association exists between production budget and worldwide revenue.

- H1: A significant association exists between production budget and worldwide revenue.

##3 Statistical Tests & Visuals:

- Pearson correlation between budget and gross

- Chi-squared test on binned budget/gross categories

- Heatmap showing the relationship between budget and gross


### Additional Visuals
- Distribution plots of production budgets and worldwide gross

- Binned budget and gross categories with corresponding bar plots

## Recommendations
To maximize profitability, Microsoft Movie Studio should:  
1. Prioritize investments in high-revenue genres (Animation, Adventure, Sci-Fi).
2. Leverage high-rated genres (Short Films & Documentaries) to strengthen industry credibility.
3. Collaborate with top directors and actors in these successful genres for higher audience engagement.
4. Focus on higher-budget movies while being strategic in its allocation

## Conclusion
This analysis provides valuable insights into movie success factors, helping Microsoft Movie Studio make data-driven decisions about film production

# Summary-:
## Interactive Dashboard "Tableau- Find below link"
https://public.tableau.com/app/profile/brian.arthur1141/viz/Microsoft_17460939619780/Dashboard1?publish=yes

## For More Information

Please review our full analysis in [our Jupyter Notebook](./student.ipynb) or our [presentation](./presentation.pdf).

For any additional questions, please contact:

- **Calistus Mwonga**, calistusmwonga@gmail.com  
- **Samwel Kipkemboi**, samkemboi201@gmail.com  
- **Brian Kanyenje**, bkanyenje@gmail.com  
- **Hannah Nyambura**, anngachuhipg1@gmail.com  
- **Kelvin Mutua**, kelvinmutua787@gmail.com  

## Repository Structure

```
├── zippedData                       
├── .gitignore                          
├── README.md  
├── presentation.pdf
├── presentation.pptx      
├── student.ipynb                               
└── student.pdf                           
```
