# SCT_ML_01
Implement a linear regression model to predict the prices of houses based on their square footage and the number of bedrooms and bathrooms.  House Price Dataset



Advanced House Price Prediction
This repository contains the complete solution for the Kaggle House Prices: Advanced Regression Techniques competition. The objective is to accurately predict the final sale price of residential homes in Ames, Iowa, using a large feature set.

🏠 Methodology & Technical Stack
The core of this solution is a robust machine learning pipeline built with Scikit-learn, designed to handle the complexity and heterogeneity of the housing data.

Component	Technique	Details
Model	Gradient Boosting Regressor	An ensemble method chosen for its high predictive accuracy on structured data. Key hyperparameters include n_estimators=300, learning_rate=0.05, and max_depth=4.
Preprocessing	Scikit-learn Pipeline & ColumnTransformer	Ensures all data cleaning and transformation steps are applied consistently and correctly across different data types.
Numerical Data	Imputation & Scaling	Missing values are filled with the median, followed by Standard Scaling to normalize features (e.g., income, area).
Categorical Data	Imputation & Encoding	Missing values are filled with the most frequent value, and nominal features are converted to numerical format using One-Hot Encoding.


📐 Key Formulas and Transformations
The competition's primary metric and the target variable's nature require specific mathematical transformations, which are crucial for model performance and result interpretation.

Reverse Transformation: After prediction, the model output must be converted back to the original price scale.
Evaluation Metric (RMSLE): The model is judged based on the Root Mean Squared Logarithmic Error (RMSLE), which is sensitive to relative errors and heavily penalizes underestimating high-value house prices.

 
​⚙️ How to Replicate
To run the pipeline and generate the submission file:

Data Acquisition: Download train.csv and test.csv from the Kaggle competition page and place them in the root of this repository.

Install Dependencies:

Bash

pip install pandas numpy scikit-learn
Execute the Code: Run the Python script containing the pipeline.

A file named submission.csv will be created, ready for submission to the Kaggle platform.
