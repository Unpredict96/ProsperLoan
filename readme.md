# Prosper Loan Exploration
## by Ban Choon Chua


## Dataset

The Prosper Loan dataset consist of 113937 entries with 81 columns.

## Summary of Findings

When performing Univariate Exploration, We can see that there are a few outliers especially some who has a credit score of 0 which we will remove, majority of the borrower has a credit score of 700 +/- 50 , borrower rate lies between 0.14 - 0.16 %, and most loan are used for debt consolidation. The highest amount of people who has loan are those who are employed, while part-time, not employed and retired are the lowest. Those who earn from 25K to 74.9K applied for the most loans compared to the rest, while not employed and 0 income are the lowest which is understable. The LoanCurrentDaysDelinquent variable took on a large range of values, so I looked at the data using a log transform. Under the transformation, the data looked left skewed, with one peak between 1750 and 2000, and another around 2300. At the end of the univariate exploration, I removed several outliers such as Credit Score below 400 as most of the data was at the far right in the chart, indicating that there is strong outlier, and Borrower rate below 0.03% as there were many rates which were either 0% and number of loan at 0%-2% were insignificant.

When performing Bivariate Exploration, it was expected that there is a negative correlation between Credit Score and Borrower Rate since the lower the credit score, the higher the borrower rate in case of delinquencies. However, there is no significant correlation between LoanCurrentDaysDelinquent vs CreditScore and LoanCurrentDaysDelinquent vs BorrowerRate. It shows that a high Prosper Score leads to a lower Borrower Rate and tends to have a higher Credit Score. Not surprisingly that those with 0 or not displayed income are those with the most amount of days delinquent as they are unlikely to pay back the interest rate due to no income. However, those with 0 income has the best credit score among the rest which is interesting and required some further attention. Those who has EmploymentStatus as unknown has the most amount of days delinquent and may be also associated to those not displayed in income range. They also have the lowest mean in credit score among the rest. After some digging, it seems that majority of the borrower with 0 income are most likely errors as they are employed which is unlikely receiving nothing or work on commision basis. We found a negative correlation coff of 0.489 between Credit Score and Borrower Rate which is expected. The relationship between high Prosper Score and low Borrower Rate is higher, since Prosper Score takes more variable into consideration instead of just the Credit Score. For the rest, there is no significant relationship.

When performing Multivaraite Exploration, the above multivariate plot shows several indicators.
1. It seems that there is no correlation between high credit score leading to higher prosper score, as we can see that each prosper score has a range between 600-900.
2. We do see that the higher the borrower's credit score, the lower the borrower's rate is regardless of the borrower's employment status.

Using a pairgrid does not provide us much information, however, when we used a simple scatter plot Days of Delinquent vs Credit Score while using Borrower Rate as the color bar, it provides us a different view. The scatter plot shows that the higher the borrower's credit score the lower the borrower rate as shown the darker blue at the top indicating low rates and yellow/green at the bottom indicating higher rates. However, regardless of the credit score, the days of delinquent are spread out from 0 to 2500 days. Shows us that high credit score does not mean lower delinquent days. The scatter plot with the color bar helped us understand more with the relationship between credit score and delinquent days. Surprisingly, a good credit score and low borrower rate still has the range of delinquent days similar to those with worse credit score and high borrower rate

## Key Insights for Presentation

We explored several variable. We find a negative correlation between Credit Score and Borrower rate as expected. The interesting results was a good credit score combine with a low borrower rate does not reduce the number of delinquent days.
