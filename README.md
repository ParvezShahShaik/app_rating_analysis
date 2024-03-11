# Google Play Store App Rating Prediction

## Objective

The goal is to build a model that predicts the app rating based on various app features. This model will be particularly useful for the Google Play Store team's new feature, aiming to boost the visibility of promising apps.

## Problem Statement

The Google Play Store team is introducing a feature to enhance the visibility of certain apps, prioritizing them in recommendations and search results. The objective is to identify apps that are likely to receive high ratings, indicating their potential for success.

## Domain

General

## Analysis to be Done

The focus is on predicting app ratings based on customer-provided data. The dataset used for analysis is the Google Play Store data ( "googleplaystore.csv").

## Steps to Perform

1. **Load the Data:**
   - Use pandas to load the dataset.
   - Check for null values in each column.

2. **Data Cleaning:**
   - Drop records with null values.
   - Convert variables to correct types and formats.

3. **Sanity Checks:**
   - Ensure the average rating falls between 1 and 5.
   - Drop rows with ratings outside this range.
   - Drop records where reviews exceed installs.
   - For free apps (type = "Free"), drop rows with prices greater than 0.

4. **Univariate Analysis:**
   - Boxplot for Price to identify outliers.
   - Boxplot for Reviews to identify unusually high review counts.
   - Histograms for Rating and Size to understand their distributions.

5. **Outlier Treatment:**
   - Investigate and drop records with very high prices (e.g., $200).
   - Drop records with more than 2 million reviews.
   - Handle outliers in the 'Installs' field using percentiles.

6. **Bivariate Analysis:**
   - Scatter plots and box plots for Rating against various features.
   - Explore relationships with Price, Size, Reviews, Content Rating, and Category.

7. **Data Preprocessing:**
   - Create a copy of the dataframe (inp1).
   - Apply log transformation (np.log1p) to Reviews and Installs.
   - Drop unnecessary columns (App, Last Updated, Current Ver, Android Ver).
   - Get dummy columns for Category, Genres, and Content Rating (inp2).

8. **Train-Test Split:**
   - Split the data into training (70%) and testing (30%) sets.
   - Separate data into X_train, y_train, X_test, and y_test.

9. **Model Building:**
   - Use linear regression as the modeling technique.
   - Report the R2 on the train set.
   - Make predictions on the test set and report R2.

## Instructions for Use

1. Load the dataset using pandas.
2. Follow the data cleaning and preprocessing steps.
3. Perform univariate and bivariate analysis as directed.
4. Build and evaluate the linear regression model.
