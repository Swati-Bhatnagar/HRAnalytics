# HRAnalytics
## Why we are doing this project and it’s importance?
The objective of this project is to predict the possible attrition of the organization, to find out who’s more likely to leave the organization.
To identify the factors that are influencing the attrition within the organization
To identify possible ways to retain high performers within the organization

## 10 Benefits of Employee Retention
1.	Cost Reduction
2.	Morale Improvement
3.	Experienced Employees
4.	Recruitment and Training Efficiency
5.	Increased Productivity
6.	Better Customer Experience
7.	Improved Corporate Culture
8.	Better Employee Experience
9.	Increased Revenue
10.	Improved Employee Engagement and Satisfaction

## DATA DESCRIPTION:
The shared files contain complete staff utilization reports for the fiscal year 2016-2018. 
The other file contains all the attrition in the organization for the years 2015-18 with details such as reason of attrition. 

## VISUALISATION:
We have done EDA and some visualization based on 4 important features:
Gender Wise - The attrition rate is more for male employees compared to female employees.
Age Wise - Employees between age group of 25 – 35 has maximum attrition compared to other age groups.
Leaving Reason - For most of the employees leaving reason is Career Growth, Personal Reasons, and further studies.
Time Series Attrition Rate Count - This plot is a general trend line between Year and no of employees attrition.

## FEATURE ENGINEERING:
After performing the EDA, we have merged both the data sets to create new features like, profit centre change, relocation and promotion.

#PROFIT CENTRE CHANGE: 
Profit centre attribute is the unigue combination of unique project id and unique manager id. Further for this one we have created a new feature that is Profit Centre Change
•	If the profit centre of one year is different from the next year then we have considered it as profit centre change.
•	If the profit centre is not available for any of the years, then we have considered the latest available data for it, and we have considered profit centre as not changed.
#RELOCATION:
We have created the new column Relocation from Location column and for that,
•	If the location of one year is different from the next year then we have considered it as relocation.
•	If the location is not available for any of the years, then we have considered the latest available data for it, and we have considered location as not changed.
#PROMOTION:
There is different hierarchy of designation within an organisation that being said Level – 1 is the highest and level 10 as lowest
•	We have considered level -1 as highest and level 10 as lowest.
•	If the level of one year is different from the next year then we have considered it as promotion.
•	If the level is not available for any of the years, then we have considered the latest available data for it, and we have considered the level as not changed and not promotion

##FEATURE SELECTION:
•	For categorical features we have chosen Chi Square Test.
Chi Square – This is used for hypothesis tests about whether your data is as expected. The basic idea behind the test is to compare the observed values in your data to the expected values that you would see if the null hypothesis is true.
This works by comparing the categorically coded data that you have collected (known as the observed frequencies) with the frequencies that you would expect to get in each cell of a table by chance alone (known as the expected frequencies).
With 95% confidence that is alpha = 0.05, we will check the calculated Chi-Square value falls in the acceptance or rejection region. Having degrees of freedom =1(calculated with contingency table) and alpha =0.05 the Chi-Square value is 3.84.
•	For numerical we have done forward feature selection
•	For employee levels, since it is ordinal, we have chosen to perform label encoding considering Level 10 as the least and level 1 as the highest.
•	For other categorical features we have done dummification.

##SPLITTING THE DATA INTO TRAINING AND TEST SET:
We have taken 80% data into training and 20% for testing.

##FEATURE SCALING:
For all numerical features we have done using standard scaler and only for training data set.
SMOTE – synthetic minority over-sampling technique
In the merged data set, the minority class belongs to the people who have left the organization, so because of this minority issue we have over-sampled the minority class.

##MODEL BUILDING:
The process of modeling means training a machine learning algorithm to predict the labels from the features, tuning it for the business need, and validating it on holdout data
We have used for employee attrition:
•	Logistic Regression  
•	Support vector machine – SVC
Metrics used for evaluation:
•	Recall
•	Confusion matrix

##KEY FINDINGS AND RECOMMENDATIONS
•	Based on the features from SVC model, it is clear from the plot that total working hours is one of the biggest reason for employee attrition, followed by promotion and profit centre.
•	Only Relocation and Training hours have negative correlation

##RECOMMENDATION:
•	Total working hours should be reduced to manhour basis Employees can be cross skilled within the teams by which works can be equally shared among the employees.
•	Employees should be recognized and to be valued with promotions basis skill set, knowledge, performance and experience
•	Employees after certain time duration tends to change the organization - New hires should be valued and treated properly. To make them feel that manager and company stands for them. Also should make them feel that even small work of him is important to the company
•	Option of relocation should be minimized/certain benefits should be given to relocated employee.
•	Training hours should be increased for new tools and technologies.


