# Task_3-Linear_Regression-
Objective
The objective of this task is to implement and understand both Simple Linear Regression (SLR) and Multiple Linear Regression (MLR). This is done using the advertising_and_sales.csv dataset, which includes features related to various advertising methods (TV, radio, social media, and influencer marketing) and sales. 
The task includes:

Implementing Simple and Multiple Linear Regression models.

Evaluating model performance using metrics like MAE, MSE, and R² score.

Visualizing the regression line and understanding the model's coefficients.

Tools Used
Scikit-learn: For implementing Linear Regression models and calculating evaluation metrics.

Pandas: For data manipulation and processing.

Matplotlib: For plotting graphs and visualizing results.

Dataset Overview

The dataset advertising_and_sales.csv contains the following columns:

tv: Advertising budget allocated to TV ads.

radio: Advertising budget allocated to radio ads.

social_media: Advertising budget allocated to social media campaigns.

influencer: Advertising budget allocated to influencer marketing.

sales: The total sales that resulted from the advertising efforts.

Steps
1. Data Preprocessing

The first step was to load and preprocess the dataset:

Missing values were handled.

The data was split into features (X) and target variable (y), where sales is the target.

2. Model Implementation

Multiple Linear Regression (MLR):

A Multiple Linear Regression model was trained using all features (tv, radio, social_media, and influencer) to predict the sales. The evaluation metrics used were:
  
  MAE (Mean Absolute Error): Measures the average magnitude of the errors in a set of predictions, without considering their direction.
  
  MSE (Mean Squared Error): Measures the average of the squares of the errors.
  
  R² Score: Indicates how well the independent variables explain the variance in the dependent variable.

Simple Linear Regression (SLR):

For each feature (tv, radio, and social_media), a Simple Linear Regression model was implemented individually, where each feature was used to predict the sales independently. The model evaluation metrics were similar to MLR, and the regression line equation was displayed for each feature.

3. Model Evaluation

Multiple Linear Regression (MLR) Evaluation:

MAE: 2312.35

MSE: 8322554.75

R² Score: 0.999

Coefficients:

TV: 3.56

Radio: -0.0026

Social Media: -0.0144

Influencer: -34.81

These results suggest that TV is the strongest predictor of sales, with a positive relationship. However, Radio and Social Media have minimal or negative impacts on sales. The model has a very high R² score, suggesting that it explains 99.9% of the variance in the sales variable.

Simple Linear Regression (SLR) for Each Feature:

For TV:

MAE: 2310.85

MSE: 8313211.57

R² Score: 0.9990

Regression Line: Sales = -168.97 + 3.56 * tv

The regression line shows a strong positive correlation between tv advertising and sales, with an R² score close to 1, indicating a strong fit.

For Radio:

MAE: 36213.62

MSE: 2048159781.48

R² Score: 0.7565

Regression Line: Sales = 39505.90 + 8.38 * radio

The regression line for radio shows a positive correlation but with a lower R² score, indicating weaker predictive power compared to tv.

For Social Media:

MAE: 63991.23

MSE: 5965956885.76

R² Score: 0.2906

Regression Line: Sales = 118076.93 + 22.27 * social_media

The regression line for social_media suggests a positive relationship with sales, but with a very low R² score, indicating that social_media alone is a poor predictor of sales.

4. Results Interpretation:

  TV has the strongest effect on sales, as shown by the high R² score in both MLR and SLR, and the positive coefficient (3.56) in the regression line.
  
  Radio and Social Media have weaker relationships with sales, as evidenced by their lower R² scores in both models.
  
  Influencer marketing has a negative coefficient in the MLR model, suggesting it may have a negative impact on sales in the context of this dataset.

6. Visualization:

For each Simple Linear Regression model, a scatter plot of Actual vs Predicted Sales was plotted. These plots help visualize the accuracy of predictions. Additionally, the regression line was plotted to visualize the relationship between the independent variable and sales.

Conclusion:
  
  Multiple Linear Regression provided a comprehensive understanding of how different advertising methods contribute to sales.
  
  Simple Linear Regression models revealed the individual contributions of features like tv, radio, and social_media, with tv showing the strongest effect.
  
  The model's high R² score (0.999) indicates that, for this dataset, the features are very predictive of the target variable (sales).
