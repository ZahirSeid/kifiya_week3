# Task 1: Exploratory Data Analysis (EDA)
## Objective

The goal of Task 1 was to perform an Exploratory Data Analysis (EDA) on a dataset to gain insights into its structure, distribution, and relationships between variables. This task involved analyzing the dataset's summary statistics, identifying trends, and generating visualizations to support data understanding and decision-making.
Steps Performed

    Data Summarization
        Descriptive Statistics: Calculated the mean, standard deviation, minimum, and maximum values for numerical features like TotalPremium, TotalClaims, Age, etc.
        Data Structure: Reviewed the data types of each column to confirm if categorical variables, dates, and numerical values were correctly formatted.

    Data Quality Assessment
        Checked for missing or null values in the dataset to assess data completeness and quality.

    Univariate Analysis
        Distribution of Variables: Generated histograms for numerical columns and bar charts for categorical columns to visualize their distributions.
        Categorical variables such as CoverType and Gender were analyzed to understand how they are distributed across the dataset.

    Bivariate and Multivariate Analysis
        Explored relationships between key variables like TotalPremium, TotalClaims, and ZipCode using scatter plots and correlation matrices.
        Analyzed the impact of other variables like Age, VehicleAge, and SumInsured on the target variables through visualizations.

    Data Comparison
        Compared trends in insurance cover type, premium amounts, and vehicle-related features such as VehicleType and VehicleAge.
        Visualized trends over different geographical areas, such as by ZipCode, to identify any regional patterns.

    Outlier Detection
        Used box plots to detect outliers in numerical data, specifically focusing on TotalPremium, TotalClaims, and SumInsured.

    Visualization
        Created insightful and visually appealing plots to highlight key findings from the EDA, helping to communicate the results more effectively.

## Key Insights

    Premium Distribution: The analysis revealed a varied distribution of premiums, with some outliers significantly higher than others.
    Claims Relationship: There was a noticeable correlation between the TotalPremium and TotalClaims, with higher premiums generally corresponding to higher claims.
    Age vs Vehicle Age: There was an interesting relationship between a customer's age and the age of their vehicle, which could suggest patterns in vehicle purchasing behavior.
    Geographical Trends: Some geographical areas (represented by ZipCode) exhibited distinct trends in terms of claims and premium amounts.

## Tools and Libraries Used

    Pandas for data manipulation
    Matplotlib and Seaborn for visualization
    NumPy for numerical operations

## Conclusion

Through this EDA, we have gained a better understanding of the dataset's structure and key trends. The insights generated will be valuable for further modeling and decision-making, as well as for identifying areas that may require additional cleaning or transformation.


# Task 3: A/B Hypothesis Testing

## Overview

This task involves performing A/B hypothesis testing to evaluate the impact of various features on key performance indicators (KPIs). Specifically, we test for significant differences in risk and profit margins across different customer segments such as provinces, zip codes, and gender.
### Hypotheses Tested:

    Risk Differences Across Provinces: There are no significant risk differences across provinces.
    Risk Differences Between Zip Codes: There are no significant risk differences between zip codes.
    Significant Margin Differences Between Zip Codes: There are no significant margin differences between zip codes.
    Risk Differences Between Genders: There are no significant risk differences between men and women.

### Key Performance Indicators (KPIs)

    Risk Metrics: Total Claims, Total Premiums
    Margin Metrics: Calculated as: Margin = TotalPremium - TotalClaims

### Data Segmentation

    Group A (Control Group): Plans without the feature (e.g., gender, province, or zip code).
    Group B (Test Group): Plans with the feature being tested (e.g., male vs. female, different provinces, zip codes).

### Methodology

#### The following statistical tests were conducted:

    Chi-Squared Test for categorical data:
        Used to test the hypothesis for risk differences across provinces and genders.
    T-Test for numerical data:
        Used to test the hypothesis for margin differences between zip codes.

### Test Assumptions:

    Chi-Squared Test assumes that the data follows a categorical distribution.
    T-Test assumes that the data follows a normal distribution and that the variances are unequal across groups.

### Results

#### Based on the statistical testing, the following conclusions were drawn:

    Risk Differences Across Provinces:
        Chi-Squared Stat: 31.91
        P-Value: 9.68e-05
        Conclusion: Significant risk differences exist across provinces.

    Risk Differences Between Genders:
        Chi-Squared Stat: 13.57
        P-Value: 0.00023
        Conclusion: Significant risk differences exist between genders.

    Margin Differences Between Zip Codes:
        T-Stat: 2.32
        P-Value: 0.0246
        Conclusion: Significant margin differences exist between the selected zip codes.

## Conclusion

This analysis provides valuable insights into risk and profit margin differences across customer segments. The findings will help guide future business strategies related to pricing, risk management, and customer segmentation.