# Google Play Store App Rating Prediction

## Objective

The goal of this project is to create a model that predicts the app rating based on various features provided in the Google Play Store dataset.

## Problem Statement

The Google Play Store team plans to boost the visibility of promising apps, and the boost will be influenced by various factors, including app ratings. The objective is to predict which apps will have high ratings to help Google promote them effectively.

## Dataset

The dataset, named "googleplaystore.csv," contains information such as App name, Category, Rating, Reviews, Size, Installs, Type, Price, Content Rating, Genres, Last Updated, Current Ver, and Android Ver.

## Steps to Perform

1. **Loading the Data:**
   - Use pandas to load the dataset.
   - Check for null values in each column.

2. **Data Cleaning:**
   - Drop records with null values.
   - Convert the 'Size,' 'Reviews,' 'Installs,' and 'Price' columns to numeric format.
   - Perform sanity checks to ensure data accuracy.

3. **Univariate Analysis:**
   - Create boxplots for Price and Reviews.
   - Create histograms for Rating and Size.
   - Identify outliers and note observations.

4. **Outlier Treatment:**
   - Drop records with very high prices.
   - Drop records with more than 2 million reviews.
   - Handle outliers in the 'Installs' field using percentiles.

5. **Bivariate Analysis:**
   - Create scatter plots and box plots to assess relationships between Rating and other features.
   - Explore patterns between Rating and Price, Size, Reviews, Content Rating, and Category.

6. **Data Preprocessing:**
   - Create a copy of the dataframe (inp1).
   - Apply log transformation to Reviews and Installs.
   - Drop unnecessary columns.
   - Get dummy columns for Category, Genres, and Content Rating (inp2).

7. **Train-Test Split:**
   - Split the data into training (70%) and testing (30%) sets.
   - Separate data into X_train, y_train, X_test, and y_test.

8. **Model Building:**
   - Use linear regression.
   - Report R2 on the train set.
   - Make predictions on the test set and report R2.

## Instructions for Use

1. Load the dataset using pandas.
2. Follow the data cleaning and preprocessing steps.
3. Perform univariate and bivariate analysis as directed.
4. Build and evaluate the linear regression model.

