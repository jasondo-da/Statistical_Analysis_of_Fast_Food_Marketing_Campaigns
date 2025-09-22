# Statistical Analysis of Fast Food Marketing Campaigns

![image](https://github.com/jasondo-da/Fast_Food_Marketing_Campaign_AB_Test/assets/138195365/5dbb82c9-db2d-4b3b-99e6-4794a42ff113)

## Table of Contents

- [Project Introduction](#project-introduction)
    - [Code in Jupyter Notebook](#code-in-jupyter-notebook)
    - [Project Dataset](#project-dataset)
- [Objective](#objective)
- [Tools and Technologies Used](#tools-and-technologies-used)
- [Results](#results)

## Project Introduction

A rapidly growing fast-food chain is preparing to launch a new menu item and is evaluating three potential marketing campaigns to promote it. To determine the most effective strategy, the menu item will be introduced at several randomly selected locations, with each location randomly assigned one of the three campaigns. Weekly sales will be recorded over a four-week period.

Hypothesis:

Null hypothesis (H0): There is no significant difference in weekly sales among the three marketing campaigns.

Alternative hypothesis (H1): At least one marketing campaign results in significantly different weekly sales compared to the others.

This study aims to identify the marketing campaign that maximizes sales performance and informs strategic decision-making for the new menu launch.


### Code in Jupyter Notebook

Link: [Statistical Analysis of Fast Food Marketing Campaigns](https://github.com/jasondo-da/Statistical_Analysis_of_Fast_Food_Marketing_Campaigns/blob/main/statistical_analysis_of_fast_food_marketing_campaigns.ipynb)


### Project Dataset

Link: [Original Kaggle Dataset](https://www.kaggle.com/datasets/chebotinaa/fast-food-marketing-campaign-ab-test/data)


## Objective

The objective of this project is to statistically evaluate three marketing campaigns for a new menu item by analyzing aggregated sales from randomly assigned locations to determine which campaign maximizes sales performance.


## Tools and Technologies Used

| Tools and Technologies | Documentation |
| :--------- | :--------- |
| Languages | [![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/) |
| Libraries | [![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/) [![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)](https://scipy.org/) [![Statsmodels](https://img.shields.io/badge/Statsmodels-white?style=for-the-badge)](https://www.statsmodels.org/stable/index.html) [![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)](https://matplotlib.org/) [![seaborn](https://img.shields.io/badge/Seaborn-%09%23191970?style=for-the-badge)](https://seaborn.pydata.org/) |
| Data Visualization | [![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)](https://matplotlib.org/) [![seaborn](https://img.shields.io/badge/Seaborn-%09%23191970?style=for-the-badge)](https://seaborn.pydata.org/) |
| Tools | ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) ![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white) |


## Results

- Exploratory Data Analysis performed to get a quick general view of the data

- Conducted a Shapiro-Wilk test to check if the data for normality. This test resulted in the significance level being less than 0.05, indicating that one the assumptions is not met and that it is not a normal distribution
  <img width="916" height="196" alt="image" src="https://github.com/user-attachments/assets/78f5e465-10f5-4330-ac8b-e5b5ad3158f5" />

- Additionally, conducted a Levene test to check for equal variances between promotion groups. This resulted in the p-value being greater than 0.05 and does not violate variance of homogenity telling me the variances are equal across all promotion groups
  <img width="784" height="209" alt="image" src="https://github.com/user-attachments/assets/a9514786-f4f1-48f7-927b-4219fedf72ab" />

- In the case of non-normal distribution, we used the Kruskal–Wallis Test a non-parametric test. The p-value resulted being less than 0.05 giving reason to reject the null hypothesis showing there is a significant statistical difference in at least one of the promotion groups
  <img width="1037" height="188" alt="image" src="https://github.com/user-attachments/assets/80043309-8efd-4501-ac1b-5bdbca159e4b" />

- After discovering there is at least one statistical difference in the promotion groups compare the mean sales of each promotion group using Tukey’s Honestly Significant Difference test which tells me that promotion group 2 is the optimal promotion group to maximize sales
  <img width="872" height="309" alt="image" src="https://github.com/user-attachments/assets/7f067de8-50cb-4462-9ee7-bef6bf5df427" />
