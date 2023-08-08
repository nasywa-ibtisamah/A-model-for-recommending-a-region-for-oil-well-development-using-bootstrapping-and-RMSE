# Project Description

Hello there :wave:
I hope this project finds you well!

In this project, I will train a model that can predict suitable locations for drilling new oil wells. The data used includes sample oil data from three regions. The parameters of each oil in these regions are already known.


**Objective**

The objective of this project is to recommend a region for oil well development along with justification or reasoning for the region's selection. In this process, bootstrapping will be performed with 1,000 samples to discover the profit distribution. Additionally, profit and risk calculations will be carried out for each region.

**Used Model**
1. Linear Regression

# Steps

1. Data Overview
2. Data Preprocessing
3. Splitting Data and Training Model
4. Profit Calculation
5. Calculating Risk and Profit using Bootsrap Technique

## 1. Data Overview

**Features**
- `id` - Unique ID of the oil well
- `f0, f1, f2` - Three feature points

**Target**
- `product` - Oil reserve volume in the well (thousands of barrels).

## 2. Pre-Processing Data

The following are data preprocessing steps I did in this project:
1. Drop Unused Columns

## 3. Splitting Data and Training Model


**Analysis Results:**

1. Based on the average product reserves, Region 2 has the highest value.

2. Looking at the RMSE values, it can be observed that df1 has the smallest RMSE (Root Mean Square Error) value. This indicates that the exact average barrel value lies within the range of 67.81 (68.72 - 0.89) to 69.7 (68.72 + 0.89).


## 4. Profit Calculation

In the predicted data, the profit value for region 0 is 40M USD. However, when using the real data (samples_target), the profit value for region 0 is 33M USD. Therefore, there is an error of approximately 7M in the predicted data.

## 5. Profit Calculation using Bootstrap Technique

The highest average profit value is in region 0, both using predicted data and real data, although the level of risk of losses differs.

# General Conclusion

1. In the initial stage, accuracy calculation was performed on the predicted results of the Linear Regression model. Region 1 (37.75) had the lowest RMSE value (0.89), with a significant difference from regions 0 and 2 (40.23). This indicates that the actual average barrel value is between 67.81 (68.72 - 0.89) and 69.7 (68.72 + 0.89).

2. Profit calculation without bootstrapping technique, using predicted data, showed that region 0 had the highest profit value at 40M. However, when using real data (samples_target), the profit value for region 0 was 34M. This resulted in an error of about 6M in the predicted data.

3. The highest profit calculation using the bootstrapping technique, using predicted data, showed that region 1 had the highest average profit value. The highest average profit value using real data was also in region 1, with the lowest risk of losses (negative profit) value.

 
**Best Region Based on Analysis Results**

From the analysis results, **Region 1** is the best area for developing new oil wells. This is based on the small RMSE value of 0.89 and the low risk of losses value of 0.016, which is below the applied threshold (2.5%).
