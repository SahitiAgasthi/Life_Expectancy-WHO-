# Life_Expectancy-WHO-
This dataset is taken from Kaggle.
The dataset consists of 22 features and 2938 records. The shape of the dataset is 2938*22. We need to predict the life expectancy of different countries in different years based on the given features.

Approach taken:
1. Missing values are filled by grouping the 'year' column and filling the missing values using Median.
2. Outliers are detected using boxplots/histograms. Using Winsorizing method, we have taken care of outliers.
3. Categorical values are converted to numerical values using One-hot encoding.
4. The Data has been split to Training (70%) and Testing data (30%) and later standardized the data using MinMax scaler.
5. By using Scikit-learn's package, ran different regression models like K-neighbors regressor, Decision Tree Regressor, SVM etc.
6. Tuned the parameters using Grid search and 10-fold cross validation.
7. Found that SVM using RBF kernel gave the highest accuracy of 96% and least Root mean square error of 1.7822.
8. Checked if Adaboosting, Bagging and Pasting increased the accuracy.
9. Applied PCA on the dataset.
10. Using Keras library, developed Deep learning models with 20 nodes in the input layer, 10 nodes in the hidden layer and 1 node in the output layer.
11. I have used Adam and SGD optimizers with mse losses and Relu activation function, normal kernal initializer for the neural network.

# The data description
The data set has 1 file: Life Expectancy Data.csv.
The Life Expectancy Data.csv has 22 columns. We need to predict the life expectancy of different countries in different years based on the given features..
There are 2938 records.

The description of variables is as follows:

Format: variable (type) - description

1. country (Nominal) - the country in which the indicators are from (i.e. United States of America or Congo)
2. year (Ordinal) - the calendar year the indicators are from (ranging from 2000 to 2015)
3. status (Nominal) - whether a country is considered to be 'Developing' or 'Developed' by WHO standards
4. life_expectancy (Ratio) - the life expectancy of people in years for a particular country and year
5. adult_mortality (Ratio) - the adult mortality rate per 1000 population (i.e. number of people dying between 15 and 60 years    per 1000 population); if the rate is 263 then that means 263 people will die out of 1000 between the ages of 15 and 60;        another way to think of this is that the chance an individual will die between 15 and 60 is 26.3%
6. infant_deaths (Ratio) - number of infant deaths per 1000 population; similar to above, but for infants
7. alcohol (Ratio) - a country's alcohol consumption rate measured as liters of pure alcohol consumption per capita
8. percentage_expenditure (Ratio) - expenditure on health as a percentage of Gross Domestic Product (gdp)
9. hepatitis_b (Ratio) - number of 1 year olds with Hepatitis B immunization over all 1 year olds in population
10. measles (Ratio) - number of reported Measles cases per 1000 population
11. bmi (Interval/Ordinal) - average Body Mass Index (BMI) of a country's total population
12. under-five_deaths (Ratio) - number of people under the age of five deaths per 1000 population
13. polio (Ratio) - number of 1 year olds with Polio immunization over the number of all 1 year olds in population
14. total_expenditure (Ratio) - government expenditure on health as a percentage of total government expenditure
15. diphtheria (Ratio) - Diphtheria tetanus toxoid and pertussis (DTP3) immunization rate of 1 year olds
16. hiv/aids (Ratio) - deaths per 1000 live births caused by HIV/AIDS for people under 5; number of people under 5 who die due     to HIV/AIDS per 1000 births
17. gdp (Ratio) - Gross Domestic Product per capita
18. population (Ratio) - population of a country
19. thinness_1-19_years (Ratio) - rate of thinness among people aged 10-19 (Note: variable should be renamed to thinness_10-       19_years to more accurately represent the variable)
20. thinness_5-9_years (Ratio) - rate of thinness among people aged 5-9
21. income_composition_of_resources (Ratio) - Human Development Index in terms of income composition of resources (index           ranging from 0 to 1)
22. schooling (Ratio) - average number of years of schooling of a population

# Evaluation Metrics
The evaluation metric for this task is Root mean square error.

Root Mean Square Error (RMSE) is the standard deviation of the residuals (prediction errors). Residuals are a measure of how far from the regression line data points are; RMSE is a measure of how spread out these residuals are. In other words, it tells you how concentrated the data is around the line of best fit.
