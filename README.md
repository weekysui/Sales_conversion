# Object: Facebook Ads Analysis and Prediction for Company
## Steps:
1.	Load Data
2.	Data understanding
- Categorical features and their unique values
- Numerical features, outliers
- Find the features correlation matrix
3.	Observation from Data Visualization
- There 3 different campaigns that this company is using, and campaigns # 1178 has the most count, while campaign #916 has the least.
- We have 4 different age groups, and age 30-34 has the most count here.
- Age group 40-44 has most engagement in campaign #916, while age group 30-34 has the most engagement in campaign #1178. Campaign # 936 has relative the same engagement among all 4 age groups, and 30-34 is relatively higher.
- Gender wise, more male than female in this dataset, and #916 & #936 male engagement is slightly higher than female group, while #1178 female has higher engagement.
-	Gender vs. Age: for group 1 (30-34) and group 2 (35-39): more male; while group 3 (40-44) and group 4 (45-49): more female
-	the more you spent on ads, the more impression of the ads and clicks it will get.
4.	Data cleaning:
-	Categorical features engineering: transform with one-hot encoding or dummy variable
5.	Plotting the KPIs: Our goal is to optimize sales conversion (Approved_Conversion) and predict future sales, first we need to understand some KPIs：
-	Return on ad spend (ROAS): but we don't have the revenue data here
-	Cost per conversion (CPA): is a great indicator of ROI, able to see which campaign is the most effective. For facebook ads CPA is defined as cost to Per New User Registration. CPA = Spent / approved_conversion
-	Click Through Rate （CTR）= Clicks/Impressions
-	Conversion rate （CvR） = Approved_conversion / Clicks
-	Cost per click（CPC） = Spent / Clicks
6.	Modeling: 
-	Linear regression
-	Random forest regressor – based model
-	Random forest regressor – optimized by RandomizedSearchCV
-	Random forest regressor – optimized by GridSearchCV
-	It turns out that random forest regressor - optimized by RandomizedSearchCV returns the highest R2 score 76%
