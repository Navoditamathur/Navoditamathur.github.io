---
title: "PPG Paint Colors: Final Project"
excerpt: "This project focused on analyzing a dataset provided by PPG to identify key paint properties using R. <br/> ![Title](https://navoditamathur.github.io/files/R_title.png)"
tags: 
  - R
  - Machine Learning
  - Data Analysis
collection: portfolio
---

**Objective:**
-------
The objective of this project was to develop a comprehensive understanding of the factors influencing paint properties by analyzing a real dataset provided by PPG. The focus was on building predictive models to identify key inputs that significantly impact the outcomes in both regression and classification contexts.


**Purpose:**
-------
The purpose of this project was to provide PPG with data-driven insights that could enhance their tools for helping users select and design paint colors. By identifying the most important input factors, the project aimed to improve the accuracy and effectiveness of PPG's existing tools.

**Methodology:**
-------
- Conducted exploratory data analysis to understand the structure and distribution of the dataset.
- Developed and trained 25 different predictive models using R, focusing on both regression and classification tasks.
  * For Regression
   * Intercept-only model - no INPUTS!
   * Categorical variables only - linear additive
   * Continuous variables only linear additive
   * All categorical and continuous variables-linear additive
   * Interaction of the categorical inputs with all continuous input main effects
   * Add categorical inputs to all main effect and all pairwise interactions of continuous inputs
   * Interaction of the categorical inputs with all main effect and all pairwise interactions of continuous inputs
   * Splines of degree 2 with interaction of R,G and B
   * Splines of degree 2- additive with categorical variables
   * Interaction of the categorical inputs with all continuous input splines of degree 2
  * For Classification
   * Intercept-only model – no INPUTS!
   * Categorical variables only – linear additive
   * Continuous variables only – linear additive
   * All categorical and continuous variables – linear additive
   * Interaction of the categorical inputs with all continuous input main effects
   * Add categorical inputs to all main effect and all pairwise interactions of continuous inputs
   * Interaction of the categorical inputs with all main effect and all pairwise interactions of continuous inputs •Splines of degree 2 with interaction of G , B and Hue added to Saturation
   * Splines of degree 2 – additive with categorical variables
   * Splines of degree 5 – additive with categorical variables
- Employed resampling techniques to further refine the model
  * For Regression: 
   * Linear models:
      - All categorical and continuous inputs-linear additive features
      - Adding categorical inputs to all main effect and all pairwise interactions of continuous inputs
      - Splines of degree 2 with interaction of R, G and B.
      - Interaction of the categorical inputs with all main effect and all pairwise interactions of continuous Inputs
    * Regularized repression with Elastic net
      - Add categorical inputs to all main effect and all pairwise interactions of continuous inputs
      - Interaction of the categorical inputs with all main effect and all pairwise interactions of continuous inputs
    * Non-linear Models
      - Neural network
      - Random forest
      - Gradient boosted trees
      - Support Vector Machines
      - Generalized Additive Models
   * For Claasification
    * Linear Models:
      - All categorical and continuous inputs-linear additive features
      - Adding categorical inputs to all main effect and all pairwise interactions of continuous inputs
      - Splines of degree 2 with interaction of G , B and Hue added to Saturation
      - Splines of degree 5 – additive with categorical variables
    * Regularized repression with Elastic net
      - Add categorical inputs to all main effect and all pairwise interactions of continuous inputs
      - Splines of degree 5 – additive with categorical variables
    * Non-linear Models
      - Neural network
      - Random forest
      - Gradient boosted trees
      - Support Vector Machines
      - Generalized Additive Models  
- Evaluated the performance and robustness of the models.
  * For Regression:
      ![Regression Models Performance Evaluation](https://navoditamathur.github.io/files/R_PPG.png)
  * For Classification
      ![Classification Models Performance Evaluation](https://navoditamathur.github.io/files/R_PPG_C.png)
- Analyzed the impact of various color model inputs on the predicted paint properties.

**Methods, Tools, and Technologies Used:**
-------
- R for data analysis and model development
- Resampling techniques for model evaluation
- Statistical methods for feature selection

**Deliverables:**
-------
- A comprehensive report detailing the methodology, analysis, and findings.
- A set of trained models capable of predicting paint properties based on color inputs.

**Code:**
-------
Repo : [PPG paint Colors](https://github.com/Navoditamathur/PPGPaintColors)

---
