## Project2_Bangkok_Housing_Price_Prediction

### Problem Statement

Bangkok housing data available in the Kaggle challenge presents the data of each housing item including its features and its pricing. The objective of this project is to create the appropriate model that will be able to predict the housing price with the best optimal score for the real-estate price calculator app. 

### Analysis
- District and Subdistrict are two features that significantly affect the housing price
- Floor area, Baths, Property type, Nearby Shops, Bedrooms, Province, Nearby stations, Nearby Supermarkets, Floor Level, Total Units, and Closest Station Distance are presented with essential relationships that can be implemented in price prediction together with District and Subdistrict
- The model of price prediction is built based on evaluating multiple models and regularizations that yield the best optimal score for its prediction capability
- Steps are:
  1. Feature Engineering: Target encoding for labeling categorical data based on the weight of the target variable which is price and Numeric Encoding for labeling month-built column. Target Encoder: Pros - Easy to implement. Cons - Target leakage problem
  2. Data Pre-processing: KNN Imputer for replacing the null values with features similarity among the defined neighbors and Standard Scaler for rescaling. KNN Imputers. Pros - More accurate than median/median/mode imputation. Cons - High memory / computational RAM depleted
  3. Model Building:
     1. Linear Regression: The model is not underfitting nor overfitting, predicted values follow the normal distribution, and train r-square, and validated r-square scores are quite resemblanced.
     2. Polynomial featured degrees2 Linear Regression: The model score is improved, the data is less varied
  4. Regularization: Ridge, Lasso, and ElasticNet evaluation.
     1. Ridge yields the most optimal score of all the regularization techniques compared
     2. Lasso yields the second-best score
     3. Elastic Net is the lowest performed regularization
  5. Final model and evaluation: Polynomial Featured Linear Regression combined with Ridge regularization

### Recommendation
- Features selected as the predictors should be the ones with high correlation coefficients such as district and subdistrict. Multiple features generate a better result than selecting only the most correlated x variables
- Data pre-processing and feature engineering are important steps in preparing the data, Standard Scaler combined with Polynomial Feature is great in preparing the data for model fitting
- Linear Regression combined with regularization techniques are needed for model improvement by eliminating unimportant features. The chosen regularization technique: Ridge eliminates the multicollinearity within the features selected

           
