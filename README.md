# Car Prices

**_Case Study_**

Analysis of the most wanted attributes in the purchase of cars and construction of a Linear Regression Model to predict prices.

**_Data_**

The data were extracted from the following link: https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho

**EDA**

Data analysis using descriptive statistics.

First, let's check the data types using the _.dtypes_ function. There are three integer type columns and four object type columns. 
Analyzing the "fuel", "seller_type", "transmission" and "owner" columns, it can be seen that there is a predominance of car sales for diesel and petrol. As well as, individual seller type and cars with manual transmission and almost triple sales for cars with the first owner.

| ![](/Graphics/Fuel.png) | ![](./Graphics/Seller_type.png) |
|:-:|:-:|
| ![](/Graphics/Transmission.png) | ![](./Graphics/Owner.png) |

I used the _.describe()_ function to return the descriptive statistics values for the columns of the integer type. 

_Measures of central tendency:_

- **_Mean_**: indicates where the values are concentrated. 

1. Year: 2013;
2. Selling_price: 5.041273e+05;
3. Km_driven: 66215.777419;

- **_Median_**: is the value that separates the upper half from the lower half of a data distribution. By default, 50% can be adopted.

1. Year: 2014;
2. Selling_price: 3.500000e+0;
3. Km_driven: 60000.000000;

- **_Mode_**: is the most repeated value.

1. Year: 2017;
2. Selling_price: 300000;
3. Km_driven: 70000;

_Dispersion Measures:_

- **_Amplitude_**: returns the maximum and minimum values.

1. Year: 2020 - 1992;
2. Selling_price: 8.900000e+06 - 2.000000e+04;
3. Km_driven: 806599.000000 - 1.000000;

- **_Variance_**: expressed as the data of a set are far from its expected value.

1. Year: 17.769124530169517;
2. Selling_price: 334718640087.90295;
3. Km_driven: 2175672269.448949;

- **_Standard Deviation_**: expresses how far the data are away from the mean.

1. Year: 4.215344;
2. Selling_price: 5.785487e+0;
3. Km_driven: 46644.102194;

**_Correlation:_**

It is good to know if the variables are related to each other. For these cases, the correlation can be calculated. There is a considerable correlation between the variables:
- Selling Price x Year;
- Selling Price x Transmission Automatic;
- Owner first x Year;

**_Data Preparation_**

The object type variables were transformed into numerical ones with the function _get_dummies_ from the Pandas library.

**_Linear Regression Model_**

The predictive model was created to predict future values and standards, in order to generalize occurrences and make more efficient decisions.

**_Results_**

For regression problems, the model's performance metrics are calculated using errors.

The MAE (Mean Absolute Error) and MAPE (Mean Absolute Percentage Error) of the training and test data were quite high. I applied the _Cross-Validation_ that showed what was foreseen by MAE and MAPE. In other words, this model was unable to return a satisfactory result. 

In order to improve the model, it is proposed, in the next step, to perform _outliers_ analysis. Linear Regression is a very sensitive algorithm to _outliers_. And if the data set has too many anomalous values, tools like the _mean_ and the _variance_ may not work well.


