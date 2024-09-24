Bike Sharing Demand Prediction using Multiple Linear Regression

Predicting the daily demand for shared bikes to help BoomBikes optimize its business strategy post-COVID-19 lockdown.

Table of Contents
General Info
Technologies Used
Conclusions
Acknowledgements
General Information
BoomBikes, a US-based bike-sharing provider, experienced a dip in revenue due to the COVID-19 pandemic. The company aims to model the demand for shared bikes to better understand the factors influencing demand and optimize their business strategy post-lockdown.

This project builds a multiple linear regression model to predict the daily demand for shared bikes, based on various independent variables such as temperature, weather conditions, holiday status, and more.

The problem BoomBikes faces is predicting the number of bike rentals (cnt) based on features such as weather conditions, time factors (seasons, years, months), and other environmental variables. A reliable prediction model will help the company adjust its strategy to cater to anticipated demand fluctuations.

Dataset
The dataset contains several independent variables, including:

season: Categorical (spring, summer, fall, winter)
yr: Year (0 = 2018, 1 = 2019)
mnth: Month (1 to 12)
holiday: Whether the day is a holiday (0 or 1)
workingday: Whether the day is a working day
weathersit: Weather situation (clear, mist, light snow/rain, heavy rain/snow)
temp: Temperature in Celsius
hum: Humidity
windspeed: Wind speed
The target variable:

cnt: Total bike rentals (including casual and registered users)
Key Steps
Data Preparation:

Converted categorical variables like season and weathersit to string labels.
One-hot encoded categorical features.
Dropped irrelevant columns such as instant, dteday, casual, and registered.
Model Building:

Created a multiple linear regression model to predict cnt (total bike rentals).
Retained important features such as yr for better predictions.
Model Evaluation:

Evaluated the model using the R-squared metric to determine how well the model explains variance in the target variable.
Multicollinearity Check:

Calculated VIF (Variance Inflation Factor) to identify multicollinearity and dropped the atemp feature due to high collinearity with temp.
Residual Analysis:

Checked the residuals for randomness to ensure no patterns exist that violate linear regression assumptions.
Conclusions
The final model achieved an R-squared score of ~0.85 on the test set, meaning it explains around 85% of the variability in bike demand.
The model provides insights into how different weather conditions, seasons, and environmental factors impact bike demand.
This model helps BoomBikes to make data-driven decisions on managing their fleet and planning ahead for different seasons.
By adjusting to the anticipated demand, BoomBikes can optimize its business strategy post-pandemic.
Technologies Used
Python 3.x
Jupyter Notebook
Pandas
Scikit-learn
Matplotlib
Statsmodels
Acknowledgements
This project was inspired by BoomBikes' need to recover from the post-COVID market.
This project used publicly available datasets for training and testing.
The project was based on multiple tutorials and references from online resources about regression models.

Contact
Created by thetechiqbal@gmail.com - feel free to contact me!
