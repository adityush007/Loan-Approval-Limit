
# Key findings: People with the highest credit score, and who have a co-applicant, are more likely to receive a large loan amount.

## Table of Contents

  - [Business problem](#business-problem)
  - [Data source](#data-source)
  - [Methods](#methods)
  - [Tech Stack](#tech-stack)
  - [Quick glance at the results](#quick-glance-at-the-results)
  - [Lessons learned and recommendation](#lessons-learned-and-recommendation)
  - [Limitation and what can be improved](#limitation-and-what-can-be-improved)

## Business problem

This app predicts how much of a loan will be granted to an applicant. The app uses different information about the applicant profile and predict how much will be approved. Usually the applicant with a higher credit score, a co-applicant will be granted a larger loan amount. It depends also on how much the applicant has requested.
## Data source

- [Kaggle loan amount prediction](https://www.kaggle.com/phileinsophos/predict-loan-amount-data)

## Methods

- Exploratory data analysis
- Bivariate analysis
- Multivariate correlation

## Tech Stack

- Python (refer to requirement.txt and yml file in the assets folder for the packages used in this project)

## Quick glance at the results

Top 3 models (with default parameters)

| Model with the best hyperparameter     	                | RMSE (range between 0 and 400000) 	|
|-------------------	                                    |------------------	|
| Random Forest      	                                    | 20791.86 	            |
| Bagging   	                                            | 20780.02 	            |
| Gradient Boosting               	                        | 26974.42	            |


- ***The final model used is: Random Forest***
- ***Metrics used: RMSE***
- Why choose random forest while bagging yield the best results?:
Comparing the RMSE while tuning the parameters, random forest produced the lowest RMSE consistently.



## Lessons learned and recommendation

- Based on the analysis on this project, we found out that the loan amount that will be granted is determined mainly by the loan amount requested, credit score and a co-applicant. The least important features are expenses types and gender.
- Recommendation would be to focus more on the most predictive feature when looking at the applicant profile, and pay less attention on the least predictive features.
## Limitation and what can be improved

- The dataset lack a metadata about the features. (What expenses types mean? What does property type 1, 2, 3, 4 mean?)
- Retrain the model without the least predictive features
- Hyperparameter tuning: I used RandomSearchCV to save time but could be improved by couple of % with GridSearchCV.
