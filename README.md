# Proyect_m3 Machine Learning


EDA
====================
**An overlook of the dataset:**

- Entries: 40.455
- Columns: 16
- Float type: 7
- Object: 9 but 5 of them are index so we have 4 at end.

**Features:**

- Price: price in USD
- Carat: weight of the diamond
- Cut: quality of the cut (Fair, Good, Very Good, Premium, Ideal)
- Color: diamond colour, from J (worst) to D (best)
- Clarity: a measurement of how clear the diamond is (I1 (worst), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (best))
- x: length in mm
- y: width in mm
- z: depth in mm
- Depth: total depth percentage = z / mean(x, y) = 2 * z / (x + y) (43--79)
- Table: width of top of diamond relative to widest point (43--95)
- City: city where the diamonds is reported to be sold

**First impressions:**

- There are no missing instances in the dataset. That looks clean!
- clarity, color and cut don't have so many categories, but still, we will be having a much longer table (more columns) when encoding them.
- Looking for best correlation with price:
    - x, y, z have strong correlations with price
    - carat has the strongest correlation with price (0.92)
    - table and depth have the weakest correlations
- Most diamonds are roughly between 0.3 and 1.5 Carats
- Fair cuts are most weighed, but they aren't the most expensive diamonds. 
- Premium cuts weigh less than the fair and then cost more. 
- Ideal cuts weigh way less and they are least expensive. 
- The color J which is the most weighed is also the most priced
- The price of a diamond could fairly be relative to its clarity, to some extent.

Workflow
====================

We can identify 3 steps:

- **1º)** Obtaining Data: In this case we are talking about historical data because contains information on both the features of the observations and the outcome.
- **2º)** Analysis of the dataset chacking for nulls and looking for correlations
- **3º)** Data cleaning and feature engineering:

    - Unit conversion checking
    - Binning to group elements to reduce noise
    - Feature scaling aplying methods like Normalization, MinMax, Robust...
    - Checking missing values for several options like drop their rows and columns or fill them with any measure statistic
    - Analyzing categorical data to find a way to convert them into numbers. For example using one-hot encoding or label encoding.
- **4º)** Select & Train model:

    - Test set: Training 80% of the total data available and letting 20% left to test our model.
    - Fit and train de model
    - Fit and test de data_test
    - Obtain predictions
    - Evaluate comparing predictions with real result of the data_test using RMSE

- **5º)** Obtain & Present Results:

    - Repeating the 4 first steps using the data to predict
        

Best Model
================

Analysis
==============
