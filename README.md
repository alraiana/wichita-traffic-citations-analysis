# wichita-traffic-citations-analysis
Understanding and Modeling the Outcomes of Police Traffic Citations in Wichita Kansas using Stanford Open Policing Project Data from 2018-2020

## Project Description: 
The Stanford Open Policing Project dataset for Wichita, Kansas was used to create a binomial model to determine what the strongest factors are for a severe disposition outcome (“Guilty”, “Nollo Contendre”, etc.) after interaction with the Wichita police. 26 variables were selected that provided statistical soundness, predictive contribution, and were supported with domain knowledge. It should be noted that officer, court, and judge information were not provided, and Hispanic was no longer recorded as a race due to policy changes. The resulting binomial model had these metrics.


| Metric                  | Value   | Interpretation                                    |
|-------------------------|---------|---------------------------------------------------|
| Pseudo R² (Cox & Snell) | 0.03046 | Low explanatory power, typical for social science |
| AUC                     | 0.681   | Weak discriminatory ability                       |
| Recall                  | 1.0     | All severe outcomes captured                      |
| Precision               | 0.906   | High accuracy for severe predictions              |

The high recall and precision along with the low AUC show that the model has a high skew towards the “severe” outcome. Future work would entail taking a deeper look into each category and attempting to improve the model from there.

## Dataset:
The dataset used for this project was from the [Stanford Open Policing Project](https://openpolicing.stanford.edu/data/) site for Wichita, KS, and the .csv version was downloaded and used for this project.

A data dictionary was compiled from the researchers’ [README file](https://github.com/stanford-policylab/opp/blob/master/data_readme.md), which can also be found here.

Data dictionary excerpt: 
<img width="975" height="502" alt="image" src="https://github.com/user-attachments/assets/4c0a71e3-80c2-44ae-9be1-ea8a0b9b7c4a" />

Dataset cleaning was done to filter down the years, categorize variables, and drop unnecessary columns. New variables were also created to be in line with the project goals. The attached Python file can be used to recreate the clean dataset, or it can be found here.

## Requirements: 
Python version 3.10 was used for this project. 
Key libraries were statsmodels, pandas, re, numpy, sklearn, matplotlib

## Installing and Running the Project:
Download and run the attached Python file (Wichita KS Clean.py)

## Contributors: 
Ryan Abdelrahim, Alex Bevan, Akshaya Ganesh


