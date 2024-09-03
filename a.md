# App Rating Prediction: Analyzing Success Factors for Google Play Store

## Introduction
Imagine a feature in the Google Play Store that can boost promising apps based on predicted ratings, helping new developers reach larger audiences. The Google Play Store team is working to improve app visibility for top-rated apps by promoting them in the "Similar apps," "You might also like," and search results sections. But how can they predict which apps will succeed? This project uses data analytics to build a model that predicts app ratings, helping Google identify which apps deserve a boost in visibility.

## Contributors
- **Project Leader:** Houssam Saleh Alrifaii
- **Team Members:** Mariana Saleh Alrifaii, Mohammad Kahwaji

## Project Overview
This project aims to develop a predictive model that forecasts app ratings based on multiple factors, including app category, number of installs, user reviews, and more. Using a dataset containing information about apps on the Google Play Store, we will clean, preprocess, and analyze the data to build a reliable model that helps determine which apps are most likely to receive high ratings.

## Dataset Overview
The dataset, sourced from the Google Play Store, includes the following fields:
- **App:** The name of the application
- **Category:** The app's primary category
- **Rating:** The overall user rating (target variable)
- **Reviews:** The number of user reviews
- **Size:** The size of the app in Kb or Mb
- **Installs:** The number of installs
- **Type:** Paid or free
- **Price:** Price of the app
- **Content Rating:** The age group the app is targeted at
- **Genres:** Additional genres the app belongs to
- **Last Updated:** Date when the app was last updated
- **Current Ver:** The app's current version
- **Android Ver:** Minimum required Android version

## Key Features
### Data Cleaning & Preprocessing
- Convert inconsistent formatting across fields (e.g., converting sizes in both Kb and Mb to numeric values, treating reviews as numeric, and fixing price formatting).
- Remove outliers (e.g., suspicious app prices, unusually high reviews or installs).
- Address missing values by dropping rows with nulls or imputing values where appropriate.

### Exploratory Data Analysis
- **Univariate Analysis:** Analyze the distribution of key variables like app size, price, reviews, and ratings. Use visualizations such as box plots and histograms to identify trends and outliers.
- **Bivariate Analysis:** Assess relationships between ratings and other variables using scatter plots and box plots. Investigate whether app size, price, or number of reviews correlates with higher ratings.

### Feature Engineering
- Transform categorical variables (e.g., app category, content rating) into numeric representations to prepare them for modeling.
- Normalize or scale features like app size and installs to improve model performance.

### Predictive Modeling
- Train regression models such as Linear Regression, Random Forest Regressor, and Gradient Boosting to predict app ratings.
- Use techniques like cross-validation to prevent overfitting and fine-tune model parameters.

### Model Evaluation
- Evaluate model performance using metrics like RMSE (Root Mean Square Error) and R² to determine how well the model predicts app ratings.
- Compare the performance of different models to select the best one for accurate prediction.

## Steps Taken to Train the Model
1. **Data Preparation:**
   - Cleaned the dataset by handling missing values and converting columns like "Size" and "Reviews" to appropriate formats.
   - Applied normalization techniques to handle outliers in features such as installs and price.

2. **Model Selection:**
   - Experimented with various regression algorithms, including Linear Regression, Decision Trees, and Random Forest, to identify the best-performing model.
   - Random Forest and Gradient Boosting were selected as the final models for further tuning based on their initial performance.

3. **Training Process:**
   - Used an 80-20 train-test split for the dataset.
   - Applied cross-validation techniques such as k-fold cross-validation to ensure robust performance across multiple data subsets.
   - Hyperparameter tuning was carried out to optimize model performance.

## Dataset
The dataset includes the following key fields:

| Variable            | Description                                  |
|---------------------|----------------------------------------------|
| App                 | Name of the application                     |
| Category            | The category the app belongs to              |
| Rating              | Overall user rating                         |
| Reviews             | Number of user reviews                      |
| Size                | Size of the app in Kb or Mb                 |
| Installs            | Number of user installs                     |
| Type                | Free or Paid                                |
| Price               | Price of the app                            |
| Content Rating      | Target age group                            |
| Genres              | Additional genres                           |
| Last Updated        | Last update date                            |
| Current Ver         | Current version of the app                  |
| Android Ver         | Minimum required Android version            |

## Key Objectives
1. **Predictive Model Development:** Build models that can accurately predict app ratings based on available app metadata.
2. **Feature Importance:** Identify the most influential factors contributing to higher app ratings (e.g., number of reviews, app size, content rating).
3. **Bias Detection:** Ensure that the model is fair and unbiased across different app categories and genres.

## Impact
The insights gained from this analysis will guide the Google Play Store team in identifying which apps deserve to be promoted, improving the visibility of high-potential apps and helping developers reach a larger audience. Additionally, this project provides a framework for ongoing evaluation of new app submissions, fostering a more dynamic and equitable ecosystem in the Play Store.
