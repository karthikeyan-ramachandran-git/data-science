# Cleaning and Transforming data

## Understand the data
1. Find the number of observations and variables
2. Find info about the variables
    - whether they're *numerical/categorical*
    - whether categorical variables are available as numerical (and vice versa)
3. Use `head()` and `tail()` function to explore the data further
4. Check for missing values, typos, symbols (inplace of missing values)

## Cleaning the data
1. Fix typos
2. Impute missing values with median/mean values
3. If required the observation can be dropped, to avoid inaccurate results

## Transforming the data
1. Transform data to be on the same scale, as this can reduce the effects of outliers.
    - Standardization
    - Reciprocal transformation
    - Logarithmic transformation
2. Use plots to explore spread and outliers
    - **Overlapped histogram** - to compare spread and distribution of multiple variables
    - **Boxplot** - to identify univariate outliers
    - **Scatterplot** - to detect multivariate outliers
