# West Nile Virus Outbreak Prediction

### Introduction and Problem Statement

In urban environments, the proliferation of mosquito populations poses significant public health risks, notably the transmission of vector-borne diseases such as West Nile Virus (WNV). Where in many individuals WNV do not present symptoms, infection can lead to serious neurological disease and there is no vaccination avaliable for use in humans. Chicago, with its diverse ecosystems ranging from urban landscapes to natural water bodies, experiences seasonal surges in mosquito populations, leading to increased instances of WNV infections among its residents. The dynamic and often unpredictable nature of mosquito population growth, influenced by factors such as weather conditions, urbanization, and ecological changes, complicates efforts to control the spread of WNV.

The necessity for an effective strategy to mitigate the health risks associated with WNV in Chicago underscores the importance of a data-driven approach to vector surveillance and control. Traditional methods of mosquito monitoring and disease prevention have relied on generalized, reactive measures. By analyzing data on mosquito populations, environmental conditions, and historical WNV outbreaks, we can uncover patterns and predictors in order to develop proactive strategies mitigating WNV outbreaks. 

The problem, therefore, can be addressed through predictive modelling that can accurately forecast WNV outbreaks based on mosquito population dynamics and environmental variables. Such models would enable public health officials to implement targeted vector control strategies, optimize resource allocation, raise public awareness and ultimately reduce the incidence of WNV among the population. The objective of this project is to identify key factors relating to mosquito population growth, particularly of the Culex genus which are deemed to be the principal vector of the disease, employing machine learning techniques to enhance our understanding and management of WNV transmission associated with mosquito populations in Chicago.

### Project Overview

1. [Datasets](#1-Datasets)
2. [Exploratory Data Analysis](#2-Exploratory-Data-Analysis)
3. [Data Manipulation & Cleaning](#3-Data-Manipulation-&-Cleaning)
4. [Modeling & Evaluation](#4-Modeling-&-Evaluation)
5. [Insights & Discussion of Results](#5-Insights-&-Discussion-of-Results)
6. [Conclusion & Recommendations](#5-Conclusion-&-Recommendations)
7. [Python Libraries](#7-Python-Libraries)

### Overview of Exploratory Data Analysis (EDA) & Data Manipulation

- Data Visualisation: Identify distribution patterns, outliers, and variable relationships, employing visualizations like histograms and scatter plots highlighting imbalances between classes of species and trap type.
- Data Imputation & Aggregation of Data: Handling of missing values, including geographical coordinates of traps and consolidation of duplicate records resulting from sampling limitations, ensuring accurate mosquito count representation per trap, date, and species.
- Feature Engineering & Creation of Dummy Variables: Derived new variables (e.g splitting the date into separate features for day, month, and year) to capture temporal dynamics affecting mosquito populations and WNV transmission. Dummy variables created for categorical data like mosquito species and trap types, facilitating their inclusion in regression models.
- Correlation Analysis: To investigate relationships between variables and identify potential predictors for the regression models, including the use of heatmaps for visualizing multicollinearity.
- Feature Engineering: Derived new variables (e.g splitting the date into separate features for day, month, and year) to capture temporal dynamics affecting mosquito populations and WNV transmission.

### Overview of Regression Analysis

- Iterative Feature Selection: Linear regression was used to find contributors to high mosquito numbers, while logistic regression identified predictors of WNV presence. Iterative feature selection and model refinement were selecting or excluding variables based on their statistical significance (P values of correlation) and contribution to model performance (accuracy). 
- Model Evaluation Metrics: Employed classification matrices and measures such as accuracy, precision, specificity, and sensitivity, alongside the odds ratio for logistic regression, providing an assessment of model performance.
- Statistical Analysis: Chi-square test for differences between species and ANOVA assessing differences between annual mosquito populations. 
- Assumption Testing: Conducted Breusch-Pagan and Shapiro-Wilk tests to check homoscedasticity and normality, ensuring the validity of regression model assumptions.

### Conclusions:

- Linear Regression Insights: Identified month, latitude, longitude and trap type as significant. Noting proximity to water features and increased numbers in urban areas likely to reflect trap distribution, heat island effect of developed residential areas and domestic water containers providing habitats for mosquito larvae.
- Logistic Regression Insights: Year, longitude, mosquito count, and species (notably C.Pipiens) as strong predictors of WNV, high multicollinearity between two species emphasizing survey identification challenges and class imbalances' effect on model predictions.

- Overall Findings: The analysis stressed the ecological and seasonal factors' importance in mosquito population dynamics, guiding mosquito control strategies and WNV prevention. Future directions include incorporating insecticide spraying data, and creating weather time-lag features to assess climate impact on mosquito breeding.
