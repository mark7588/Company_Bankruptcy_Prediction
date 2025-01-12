# Motivation

I have been investing money in stock market. I invested my money in SMCI, it went up about 50% in 3 weeks. This made me feel really confident about investing. However, it fell down to 20% less than the average price I bought. My potential lifetime gain became negative, indicating that I will lose all of my investment profit if I need to sell the SMCI at the moment. At this moment, I got really anxious about the possibility that this stock might go even worse than this. I realized that I at least should know that the company that I invest money on will not go bankrupt within the near future to invest in underestimated stocks for long term gain. This made me want to learn about the factors that would lead to bankruptcy of the company. 

# Approach 

For Machine Learning models, there’s often a trade-off between interpretability and flexibility. Less flexible models generally have better interpretability but may not capture complex patterns as effectively. 

## Summary Table of Models:

| Model	     | Flexibility Level	     | Interpretability Level   |
|--------------|--------------|--------------|
| Logistic Regression	  | Low  | High  |
| k-Nearest Neighbors | Low | Medium |
| Decision Trees | Medium-Low  | High |
| Naive Bayes| Medium  | Medium  |

From my motivation, I would like to focus on interpretability of the model I use. Therefore, I am going to use ML algorithms such as logistic regression, decision trees, and K-Nearest Neighbors (KNN) to generate a model. 


## What is logistic regression and why people use it? 
Logistic regression is a method used to predict outcomes that fall into one of two categories, like whether a customer will buy a product or not. It looks at different factors, such as age, income, or previous purchases, and determines how likely each one is to influence the outcome. Think of it as creating a scoring system based on the data, where higher scores mean a higher chance of a specific result. The model gives a probability (e.g., 80% chance of a purchase), making it easy to decide where to focus efforts. It’s widely used because it’s simple, transparent, and helps identify which factors are the most important for making decisions.

## What is decision tree and why people use it? 
A decision tree is a way to make predictions by asking a series of simple yes-or-no questions, like "Is the customer older than 30?" or "Do they have a high income?" Each question splits the data into smaller groups until it reaches a decision, such as whether someone will buy a product. The process is easy to follow because it’s like tracing a path down a flowchart. It’s popular in business because the results are intuitive and can clearly show the factors leading to each decision.

## What is KNN and why people use it?
The k-Nearest Neighbors (kNN) algorithm predicts an outcome by looking at similar examples from the past, like asking, "What did other customers with similar characteristics do?" It compares a new case to its closest "neighbors" in the data and decides based on what most of them did. For example, if 7 out of 10 similar customers made a purchase, it predicts the new customer will likely buy too. This algorithm is popular since it is  straightforward and works well when you have data that’s easy to compare.

## About the source data 
## Link: https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction?resource=download
## Source: Deron Liang and Chih-Fong Tsai, deronliang '@' gmail.com; cftsai '@' mgt.ncu.edu.tw, National Central University, Taiwan
The data was obtained from UCI Machine Learning Repository: https://archive.ics.uci.edu/ml/datasets/Taiwanese+Bankruptcy+Prediction

## Similar Datasets
* The Boston House-Price Data: LINK
* Gender Pay Gap Dataset: LINK
* Spanish Wine Quality Dataset: LINK
## Context
The data were collected from the Taiwan Economic Journal for the years 1999 to 2009. Company bankruptcy was defined based on the business regulations of the Taiwan Stock Exchange.
## Attribute Information
Version 2: Updated column names and description to make the data easier to understand (Y = Output feature, X = Input features)
Bankrupt? (Class label): Indicates whether the company is bankrupt (1 for yes, 0 for no).
ROA (C): Measures return on total assets before interest and depreciation.
ROA (A): Measures return on total assets before interest and after tax.
ROA (B): Measures return on total assets after tax and depreciation.
Operating Gross Margin: Shows gross profit as a percentage of net sales.
Realized Sales Gross Margin: Represents realized gross profit as a percentage of net sales.
Operating Profit Rate: Indicates operating income as a percentage of net sales.
Pre-tax Net Interest Rate: Shows pre-tax income as a percentage of net sales.
After-tax Net Interest Rate: Indicates net income as a percentage of net sales.
Non-industry Income Ratio: Measures net non-operating income as a percentage of revenue.
Continuous Interest Rate (After-tax): Net income, excluding extraordinary gains or losses, as a percentage of sales.
Operating Expense Rate: Operating expenses as a percentage of net sales.
R&D Expense Rate: Research and development expenses as a percentage of net sales.
Cash Flow Rate: Cash flow from operations relative to current liabilities.
Debt Interest Rate: Interest-bearing debt as a percentage of equity.
Tax Rate: Effective tax rate paid by the company.
Net Value Per Share (B): Book value per share (version B).
Net Value Per Share (A): Book value per share (version A).
Persistent EPS: Earnings per share over the last four seasons.
Cash Flow Per Share: Operating cash flow distributed per share.
Revenue Per Share: Sales generated per share.
Operating Profit Per Share: Operating income earned per share.
Net Profit Before Tax Per Share: Pre-tax income allocated per share.
Sales Gross Profit Growth: Growth rate of gross profit from sales.
Operating Profit Growth: Growth rate of operating income.
Net Profit Growth: Growth rate of net income after tax.
Regular Net Profit Growth: Growth of continuing operating income after tax.
Continuous Net Profit Growth: Growth rate of net income excluding one-off gains or losses.
Total Asset Growth: Increase in total assets over time.
Net Value Growth: Growth in total equity value.
Asset Return Growth Rate: Increase in return on total assets.
Cash Reinvestment: Percentage of cash reinvested into the company.
Current Ratio: Measures short-term liquidity (current assets/current liabilities).
Quick Ratio: Indicates short-term liquidity excluding inventory.
Interest Expense Ratio: Interest expenses as a percentage of total revenue.
Debt to Net Worth: Total liabilities relative to equity.
Debt Ratio: Total liabilities as a percentage of total assets.
Net Worth to Assets: Equity as a percentage of total assets.
Long-term Fund Suitability: Measures whether long-term funding matches fixed assets.
Borrowing Dependency: Proportion of interest-bearing debt to total funding.
Contingent Liabilities to Net Worth: Ratio of potential liabilities to equity.
Operating Profit to Capital: Operating income relative to invested capital.
Net Profit Before Tax to Capital: Pre-tax income as a percentage of capital.
Inventory/Receivables to Net Value: Value of inventory and receivables as a percentage of equity.
Total Asset Turnover: Efficiency of asset usage to generate revenue.
Accounts Receivable Turnover: How quickly receivables are collected.
Average Collection Days: Average time to collect accounts receivable.
Inventory Turnover Rate: Frequency of inventory turnover in a period.
Fixed Assets Turnover: Efficiency of fixed assets in generating revenue.
Net Worth Turnover: Efficiency of equity in generating revenue.
Revenue Per Employee: Sales generated per employee.
Operating Profit Per Employee: Operating income earned per employee.
Allocation Rate Per Employee: Fixed assets per employee.
Working Capital to Assets: Percentage of working capital relative to total assets.
Quick Assets to Assets: Proportion of liquid assets to total assets.
Current Assets to Total Assets: Percentage of short-term assets in total assets.
Cash to Assets: Cash as a percentage of total assets.
Quick Assets to Current Liabilities: Liquid assets relative to short-term liabilities.
Cash to Current Liabilities: Cash as a percentage of short-term liabilities.
Current Liabilities to Assets: Short-term liabilities relative to total assets.
Operating Funds to Liability: Operating funds as a percentage of liabilities.
Inventory to Working Capital: Inventory relative to working capital.
Inventory to Current Liability: Inventory as a percentage of short-term liabilities.
Current Liabilities to Liability: Short-term liabilities as a percentage of total liabilities.
Working Capital to Equity: Working capital relative to equity.
Current Liabilities to Equity: Short-term liabilities as a percentage of equity.
Long-term Liability to Current Assets: Ratio of long-term liabilities to short-term assets.
Retained Earnings to Assets: Retained earnings relative to total assets.
Total Income to Total Expense: Ratio of income to expense.
Total Expense to Assets: Expenses as a percentage of total assets.
Current Asset Turnover: Efficiency of current assets in generating sales.
Quick Asset Turnover: Efficiency of quick assets in generating sales.
Working Capital Turnover: Efficiency of working capital in generating sales.
Cash Turnover Rate: Efficiency of cash in generating sales.
Cash Flow to Sales: Operating cash flow relative to sales.
Fixed Assets to Assets: Fixed assets as a percentage of total assets.
Current Liability to Liability: Ratio of short-term liabilities to total liabilities.
Current Liability to Equity: Short-term liabilities as a percentage of equity.
Equity to Long-term Liability: Ratio of equity to long-term liabilities.
Cash Flow to Assets: Operating cash flow as a percentage of total assets.
Cash Flow to Liability: Operating cash flow relative to liabilities.
CFO to Assets: Cash flow from operations as a percentage of assets.
Cash Flow to Equity: Cash flow from operations relative to equity.
Current Liability to Current Assets: Ratio of short-term liabilities to short-term assets.
Liability-Assets Flag: 1 if liabilities exceed assets, 0 otherwise.
Net Income to Assets: Net income relative to total assets.
Total Assets to GNP Price: Total assets relative to gross national product price.
No-credit Interval: Time a company can operate without external financing.
Gross Profit to Sales: Gross profit as a percentage of sales.
Net Income to Equity: Net income as a percentage of equity.
Liability to Equity: Total liabilities as a percentage of equity.
Degree of Financial Leverage: Measures financial leverage based on EBIT.
Interest Coverage Ratio: Ability to cover interest expenses with EBIT.
Net Income Flag: 1 if net income has been negative for the past two years.
Equity to Liability: Ratio of equity to total liabilities.

## Relevant Papers
Liang, D., Lu, C.-C., Tsai, C.-F., and Shih, G.-A. (2016) Financial Ratios and Corporate Governance Indicators in Bankruptcy Prediction: A Comprehensive Study. European Journal of Operational Research, vol. 252, no. 2, pp. 561-572.
https://www.sciencedirect.com/science/article/pii/S0377221716000412
