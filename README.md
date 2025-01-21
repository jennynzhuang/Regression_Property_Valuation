## README for Property Price Prediction Using Linear Regression

## Overview

This project develops a **linear regression model** to predict property sale prices using characteristics like the number of rooms, property taxes, and square footage.

## Contents

- **Writeup**: A report detailing the data, variable selection, model diagnostics, and results.
- **Codebase**: Python scripts for data analysis, model building, and evaluation.

## Features

- **Predictors**: Property attributes such as size, taxes, and rooms.
- **Methodology**: Exploratory data analysis, variable selection, and model diagnostics.
- **Framework**: Based on strategies from *Montgomery et al. (2021, p. 367)*.

## Tools

- **Python Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`, and `sklearn`.

## Key Findings

1. **Final Model**:  
   - Key predictors include **property taxes**, **living space**, **number of garage stalls**, and **number of fireplaces**.  
   - Interaction terms (e.g., taxes × living space) capture nuanced relationships and enhance predictive power.  
   - Excluded variables were found redundant or insignificant.

2. **Model Performance**:  
   - Adjusted \( R^2 \): **93%**, explaining a significant portion of variance in property prices.  
   - AIC and BIC values improved significantly after variable selection, reducing overfitting risks.  
   - PRESS statistic indicates better generalization to new data compared to the initial model.

3. **Validation**:  
   - Residual analysis confirms assumptions of linearity and constant variance, with minor deviations in the tails.  
   - K-fold cross-validation (mean \( R^2 \): **89.3%**) highlights strong generalization, though one fold showed reduced performance (\( R^2 \): **58.8%**).  

4. **Multicollinearity**:  
   - High multicollinearity detected in some variables (e.g., number of rooms vs. bedrooms). Addressed through interaction terms and variable elimination.

## Conclusion

The model effectively predicts property prices by focusing on key variables and accounting for interaction effects. While robust, minor deviations in residuals and cross-validation results suggest further refinements, such as addressing outliers and exploring non-linear models.

## Future Recommendations

- Address variability in cross-validation results by examining data quality in weaker folds.
- Explore Ridge or Lasso regression to reduce multicollinearity and improve generalization.
- Investigate advanced non-linear techniques or transformations to capture complex relationships.
- Expand the dataset for better validation in diverse market conditions.

## Reference

Montgomery, D. C., Peck, E. A., & Vining, G. G. (2021). *Introduction to Linear Regression Analysis*.  
