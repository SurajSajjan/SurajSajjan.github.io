---
title: "American Community Survey Data: An Exploration"
date: 2018-12-14
tags: [R Programming, ACS, Programming, Data Science, Data Visualization, Data Analysis]
header:
  image: "/images/NathanPhillips.jpg"
categories: DataScience
---

Utilizing the power of R Programming to explore ACS Data.

The dataset can be found from the following webiste - https://factfinder.census.gov/faces/tableservices/jsf/pages/productview.xhtml?pid=ACS_pums_csv_2012_2016&prodType=document

Data Summary: The selected data set is the population data, which is a sample taken from the “2016 American Community Survey (ACS) 5-year Public Use Microdata Samples (PUMS)”. The samples are actual survey responses recorded by the ACS between the years 2012-2016. The data set contains over 360 variables and around 16,000,000 records distributed across 4 csv files. Here, we have used the data table library to import only the variables of our choice from each of these 4 csv files and combine them into one single dataset.

Exploratory analysis such as the distribution of Hindi speaking population based on their citizenship status, gender, level of education, etc has been performed. A statistical model has been built where we perform linear regression to check if a person’s total income is proportional to his salary income from the past year. Hypothesis testing has been performed with the null and alternate hypothesis as shown below:
Null Hypothesis: There is no relationship between the total income and the salary income in the past year. The slope of a regression line is zero.
Alternate Hypothesis: There exists a relationship between the total income and the salary income from the past year. The slope is not zero.

From the model, we observe a p-value of 2.2X10^−16. This is significantly less when compared to the alpha value of 0.05, Hence we reject the null hypothesis and say there exists a relation between the total income of a person to his salary income in the past year. We see that the intercept is 6.25X103 and the slope is 1.022. Hence the equation of regression can be formulated as: PINCP = 1.022(WAGP) + 6.25X10^3. According to the model, if the salary income for the year is zero, the total income would be 6.25X103. We observe that the coefficient t-value is 200.47. The further away from 0, the better. We observe an R-squared value of 0.8534. This value is used to determine how well the model fits the data. Hence the model can be accurate upto 85.34%. The F-statistic is 4.019X10^4 The further away the value from 0, the better.

Please refer the file ACSDataAnalysis_Report for the detailed project report here: [**ACS**](https://github.com/SurajSajjan/ACSDataAnalysis/blob/master/ACSDataAnalysis_Report.pdf){:target="_blank" rel="noopener" }