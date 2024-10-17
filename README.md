# **PimaDiabetes Dataset Analysis Report **

| Contents 											 	   	|
| -------- 											 	   	|
| [Introduction](#Introduction)			   	|
| [Project Objective](#Project-Objective)			   	|
| [Dataset Overview](#Dataset-Overview) 		   		|
| [Exploratory Data Analysis](#Exploratory-Data-Analysis) 		   		|
| [Feature Engineering](#Feature-Engineering)							|
| [Subset Analysis](#Subset-Analysis)							|
| [Visualisatiion of Outcomes](#Visualisatiion-of-Outcomes)					   		|
| [Modelling and Predictions](#Modelling-and-Predictions)						   	|
| [Key Findings and Insights](#Key-Findings-and-Insights)					|
| [Conclusion](#Conclusion)									|
| [Built with](#Built-with)							   		|


# Probabilistic Modelling for Diabetes Prediction: Feature Engineering and Logistic Regression

## Introduction
No doubt, diabetes remains a chronic health concern that is best managed through prediction of one’s propensity, early diagnosis and preventative care. The PimaDiabetes dataset comprises diagnostic features collected from women of Pima Indian heritage with the ultimate aim of predicting the likelihood of developing Type 2 diabetes given  specific factors such as BMI, glucose level, pregnancies, and other health indicators.

## Project Objective 
The goal of the executed analysis is to develop a probabilities model using logistic regress to predict the likelihood of diabetes among Pima Indian women based on demographic and medical factors. It builds on a thorough exploration of the dataset and incorporates feature engineering and advanced statistical modelling to identify associations between health metrics and diabetes outcomes as well as to enhance model accuracy.

The project was motivated by a goal to not only highlight the technicalities of data processing and modelling, but to extract actionable, relatable insight. Thus, a key focus is on understanding how pregnancy history correlates with the risk of developing diabetes. 

## Dataset Overview 
The Pima Indians Diabetes dataset consists of medical records collected from 768 female participants aged 21 years and above. This dataset contains 8 predictor variables and 1 binary target variable (‘outcome’), where Outcome = 1 indicates the presence of diabetes and Outcome = 0 represents the absence of diabetes. 
The following are the attributes recorded in the dataset. 

1.	Pregnancies: number of times pregnant
2.	Glucose: plasma glucose concentration (mg/dL)
3.	Blood pressure: diastolic blood pressure (mm Hg)
4.	SkinThickness: triceps skinfold thickness (mm)
5.	Insulin: 2-hour serum insulin (mu U/ml)
6.	BMI: Body Mass Index (weight in kg/(height in m)^2)
7.	DiabetesPedigreeFunction: diabetes pedigree function (genetic likelihood of diabetes)
8.	Age: age in years
9.	Outcome: class variable (0 = No diabetes, 1 = Diabetes).

## Exploratory Data Analysis (EDA)
Extensive exploration of the PimaDiabetes dataset was carried out to uncover the distribution and relationships between variables. Descriptive statistics and visualisations tools including  histograms, boxplots, and correlation heatmaps were used to identify trends and correlations.

### Key Observations from EDA:
•	Glucose Levels and Diabetes: Higher glucose levels were strongly correlated with positive diabetes outcomes (r = 0.47).

•	BMI Impact: Body Mass Index (BMI) also showed a significant positive correlation with diabetes.

•	Pregnancy and Age Relationship: A moderate positive correlation was observed between pregnancies and age, suggesting older women had more pregnancies.

## Feature Engineering
An additional feature, ThreeOrMoreKids, was created to differentiate women who had three or more pregnancies from those who had fewer. This binary feature served as a key variable, aiding deeper analysis of how pregnancy history impacts diabetes risk as subsequent analyses revealed notable differences between women based on this characteristic. 
The rationale behind creating this feature stems from research suggesting that a higher number of pregnancies may be correlated with a higher risk of developing diabetes due to gestational diabetes.

## Subset Analysis
Using the ThreeOrKids feature, the dataset was split into two subsets, videlicet; 

• Diab3: represnting women with three or more pregnancies who developed diabetes (Outcome = 1)

• NonDia3: representing women with three of ore pregnancies who did not develop diabetes (Outcome = 0)

## Visualisation of Outcomes
Visualisations were generated to present the distribution of pregnancies and diabetes outcomes.

1. Pregnancies Distribution for Women with Three or More Pregnancies: A histogram was plotted to display the distribution of pregnancies among women with three or more pregnancies.

2. Comparison by Outcome: Separate histograms were created for women with diabetes (Outcome=1) and women without diabetes (Outcome=0), showing distinct distributions between the groups.

3. Boxplot of Pregnancies by Outcome: A boxplot was used to further illustrate the differences in pregnancies between diabetic and non-diabetic women.

## Modelling and Predictions
A logistic regression model was trained using specific, relevant diagnostic features including BMI, glucose levels, and diabetes pedigree function to predict diabetes outcomes. This regression model was evaluated on its ability to accurately classify whether or not a woman would develop diabetes. 

### Model Accuracy:
•	The logistic regression model achieved an accuracy of 74%, suggesting that the model generalises reasonably well.

## Key Findings and Insights
•	Pregnancy and Diabetes Risk: Women with three or more pregnancies showed a higher likelihood of developing diabetes. In particular, women in the Diab3 group had higher pregnancy counts and showed distinct patterns compared to the non-diabetic group.


•	Significant Predictors: Glucose levels and BMI remained the strongest predictors of diabetes. However, the addition of the ThreeOrMoreKids feature provided further insight into lifestyle and demographic factors affecting diabetes risk.


•	Risk Differences: Women with fewer pregnancies were less likely to develop diabetes compared to those with a higher pregnancy count, suggesting that pregnancy history might be a useful predictor in medical assessments.

## Conclusion
In summary, this analysis highlights the relationship between pregnancy history and diabetes risk among women in the PimaDiabetes dataset. The feature ThreeOrMoreKids serves as an informative predictor of diabetes, reinforcing existing medical research that links pregnancy count with the risk of developing diabetes.
This repository demonstrates the use of feature engineering, subset analysis, and visualisations to derive insights from data and tackle real-world problems. Future analysis may explore additional interactions between variables to further refine predictions of diabetes risk.

## Built With
- JupyterNotebook	
- Python	   	
- Pandas		
- Numpy			
- Matplotlib	
- Seaborn
- Scikit-learn
- StatsModels
