
# Findings: People with the best credit and a co-applicant are more likely to get approved for a large loan.

## Table of Contents

  - [Problem Statement](#problem-statement)
  - [Data source](#data-source)
  - [Steps](#steps)
  - [Tech Stack](#tech-stack)
  - [Results](#results)

## Problem Statement

This model forecasts how much of a loan an applicant will receive. The model forecasts how much will be permitted based on various variables about the applicant profile. A co-applicant with a higher credit score is usually awarded a larger loan amount. It also depends on how much the applicant has asked for.

## Data source

- [Kaggle loan amount prediction](https://www.kaggle.com/phileinsophos/predict-loan-amount-data)

## Steps

- Exploratory data analysis
- Bivariate analysis
- Multivariate correlation

## Tech Stack

- Python (refer to requirement.txt for the packages used in this project)

## Results

Top 3 models (with default parameters)

| Model with the best hyperparameter     	                | RMSE (range between 0 and 400000) 	|
|-------------------	                                    |------------------	|
| Random Forest      	                                    | 20784.89 	            |
| Bagging   	                                            | 20723.30 	            |
| Gradient Boosting               	                        | 26674.35	            |


- ***The final model used is: Random Forest***
- ***Metrics used: RMSE***
- Why choose random forest while bagging yields the best results?:
Comparing the RMSE while tuning the parameters, random forest produced the lowest RMSE consistently.



## Lessons learned and recommendation

- Based on the analysis of this project, we found out that the loan amount that will be granted is determined mainly by the loan amount requested, credit score, and a co-applicant. The least important features are expense types and gender.
- Recommendation would be to focus more on the most predictive feature when looking at the applicant profile and pay less attention to the least predictive features.
