# Google Advanced Data Analytics Case study: What’s likely to make the employee leave the company?

This is my capstone project for Google's Advanced Data Analytics Professional Certificate.

Tools used:
- Python

# Table of Contents

1. [Introduction](#1-introduction)
2. [Scenario](#2-scenario)
3. [PACE stages](#3-pace-stages)
4. [Result](#4-result)

# 1. Introduction
This is a case study for completing [Google Advanced Data Analytics Professional Certificate](https://www.coursera.org/professional-certificates/google-advanced-data-analytics). In this case study, you work for a fictional company, Salifort Motors. The task is to deploy different models to analyze a dataset and generate business insights for your stakeholders. They have the following question: what’s likely to make the employee leave the company?

# 2. Scenario
The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. They refer to you as a data analytics professional and ask you to provide data-driven suggestions based on your understanding of the data.

Your goals in this project are to analyze the data collected by the HR department and to build a model that predicts whether or not an employee will leave the company.

If you can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.

The dataset that you'll be using contains 15,000 rows and 10 columns for the variables listed below, refer to its source on [Kaggle](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv).

Variable  |Description |
-----|-----|
satisfaction_level|Employee-reported job satisfaction level [0&ndash;1]|
last_evaluation|Score of employee's last performance review [0&ndash;1]|
number_project|Number of projects employee contributes to|
average_monthly_hours|Average number of hours employee worked per month|
time_spend_company|How long the employee has been with the company (years)
Work_accident|Whether or not the employee experienced an accident while at work
left|Whether or not the employee left the company
promotion_last_5years|Whether or not the employee was promoted in the last 5 years
Department|The employee's department
salary|The employee's salary (U.S. dollars)

# 3. PACE stages
![pace stage](images/pace-stage.jpg)
Detailed process in the Jupyter Notebook [Here](https://github.com/rhafaelc/Google-Advanced-Data-Analytics-Capstone/blob/main/Salifort%20Motors%20Study%20Case.ipynb).

# 4. Result
Executive summary [Here](https://github.com/rhafaelc/Google-Advanced-Data-Analytics-Capstone/blob/main/Executive%20summary%20-%20Salifort%20Motors%20Study%20Case.pdf)

### Summary of model results

**Logistic Regression**


The logistic regression model achieved precision of 80%, recall of 83%, d1-score of 80% (all weighted average), accuracy of 83%, and auc score of 89%.

**Tree-based models**


The random forest model achieved precision of 99%, recall of 90%, f1-score of 94%, accuracy of 98%, and auc score of 98%. Which is close to the result of the XGBoost model. The XGBoost model achieved precision of 98%, recall of 89%, f1-score of 94%, accuracy of 98%, and auc score of 98%.

**Feature Importance**


All of the models agree that the most important features are at least `satisfaction_level`, `number_project`, `tenure`, `average_monthly_hours`, and `last_evaluation`. Which is closely related to the insights from the EDA.

### Conclusion and Recommendations

The models and the feature importances extracted from the models confirm that employees at the company are overworked.

To reduce the number of employees leaving the company, the company should consider the following:
- Cap the number of projects an employee can work on at a time.
- Reward employees for working longer hours and for working on more projects, or don't require them to do so.
- High evaluation score shouldn't just be based on the number of projects and hours worked, but also on the quality of the work.
