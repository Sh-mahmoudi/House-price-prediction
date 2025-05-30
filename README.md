#  House Price Prediction – Washington State

This project uses a dataset of house listings in Washington State, USA to build and compare several machine learning models that predict house prices based on property features and location details.

Data Source: [Kaggle – House Sales in King County, USA](https://www.kaggle.com/datasets/shree1992/housedata/data)

The Jupyter notebook `House Price.ipynb` contains all data preprocessing, feature engineering, modeling, and evaluation steps.

The dataset includes typical housing features such as:  
`bedrooms`, `bathrooms`, `sqft_living`, `sqft_lot`, `floors`, `view`, `condition`, `yr_built`, and more.

As part of feature engineering, I created a new location variable by combining the `city` and `statezip` fields. I then applied target encoding with K-Fold cross-validation to convert this categorical location feature into a meaningful numerical format while avoiding data leakage.

I compared several machine learning models, including:  
`SVR`, `XGBRegressor`, `Ridge`, `ElasticNet`, `SGDRegressor`, `BayesianRidge`, `LinearRegression`, `RandomForestRegressor`, and a `PCA + LinearRegression` pipeline, to determine which model provided the best predictions.

Model performance was evaluated using Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and Adjusted R².

Through effective feature engineering, model selection, and hyperparameter tuning, the predictive power of the final model improved by approximately 85%.
