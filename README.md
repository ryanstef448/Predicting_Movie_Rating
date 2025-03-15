# Predicting_Movie_Rating
I used machine learning to predict movie rating off a set of features.

* Introduction

  * Objective: Understand how movie features (e.g., budget, revenue, popularity) correlate with ratings.
  * Use machine learning to predict movie ratings based on these features.

* Background & Related Work

  * Review of a similar project using MovieLens data, comparing K-means and SGD for rating prediction.
  * This project will focus on Principal Component Analysis (PCA) to reduce dimensionality and identify influential features.
    
* Data Description & Preprocessing

  * Dataset: 5000 movies from Kaggle (TMDB).
  * Predictor variable: "vote_average" (movie ratings).
  * Predictors: 6 numerical variables (budget, revenue, year, etc.).
  * Preprocessing steps:
Dropped rows with null values or errors.
Converted all data types to numerical.
Formatted the year variable to a usable form.

* Data Visualizations
  * Visualized mean, median, standard deviation of predictors.
  * Created histograms for budget and revenue variables.
    
* Modeling

  * Principal Component Analysis (PCA): Applied to reduce dimensionality and identify correlations between features.
Created a Scree plot to visualize variance explained by principal components.
Determined that the first 4 components explain 95% of the variance.
Analyzed contributions of variables to the principal components.
* XGBoost Model without PCA: Applied XGBoost to the full dataset and evaluated using RMSE (1.4359).
* XGBoost Model with PCA: Applied XGBoost to the dataset after reducing dimensionality with PCA and evaluated using RMSE (0.7353).
  
* Conclusion

  * PCA improved model performance by reducing RMSE from 1.4359 to 0.7353.
  * Identified important features using PCA, which improved the model's prediction accuracy.
  * PCA helped simplify the dataset and removed noise, enhancing XGBoost's predictive power.
    
* Discussion

  * PCA provided significant improvement even with only 6 predictors, possibly due to noise in the data.
  * PCA and machine learning models like XGBoost can work well together to improve predictive accuracy.

