# analyze_china_discount
## Introduction:
Foreign investments in Chinese equities and debts have experienced a significant decline, with a staggering US$188 billion, or 17%, decrease from the peak in December 2021 to the end of June 2023, according to Bloomberg. This prompts an intriguing question: Does this decline impact the valuation of Chinese stocks when compared to their US counterparts? In this blog post, we would build a model for valuating US stocks, which will be later applied to estimate the “fair value” of corresponding Chinese stocks. By comparing this “fair value” against the actual valuation, we can determine whether Chinese stocks are trading at a premium or a discount.

## Project Outline:
1. Data Download and Cleansing with yfinance: We begin by obtaining the necessary data using the yfinance library and ensuring its cleanliness for accurate analysis.
2. Simple Data Analysis: Conducting an initial exploration of the acquired data to gain insights and identify potential trends or patterns.
3. Valuation Analysis using Linear Regression: Employing linear regression models to analyze the relationship between various parameters and valuation, providing a comprehensive understanding of the factors influencing the stock prices.
4. Valuation Analysis using Neural Network: Extending the analysis to incorporate more complex patterns and relationships by utilizing neural network models, enabling us to capture nonlinear dynamics and enhance the accuracy of our valuation estimates.
5. Evaluating the “China Discount” with the Neural Network model.
6. Comparing the current “China Discount” with a historical data point (2021) to evaluate any substantial changes, if any.

## Analysis
Step 1: Fitting a model to forecast market capitalization from a set of parameters
Scope: Top 500 listed US companies by market capitalization.
Data: Historical financials for the past 5 years
Parameters: Revenue, Revenue Growth, Earning Growth, Gross Margin, Operating Margin, Net Margin, EPS, Debt, Cash, Asset, Equity, Return on Asset, Return on Equity, Debt-to-Equity Ratio, Free Cash Flow, Operating Cash Flow, Dividend Yield
Model: Linear regression; Neural Network (3 hidden layer, layer size=50, no regularization, activation=relu (hidden layer)/linear (output layer))

Step 2:
Fitting the above model with data of Chinese listed companies. Observe the discrepancies between the predicted market capitalization and the actual market capitalization. Difference will be deemed as a discount / premium ("China Discount"). 

Step 3:
The current China Discount is compared with that two years ago, and observe if there is any material change. 

## Conclusion
In conclusion, the analysis highlights that 80% of the listed Chinese companies show a valuation discount compared to their US counterparts, while the valuation of companies from the two countries are in largely similar level two years ago. A negative correlation between company size and the discount level is observed, while premium-trading companies exhibit stronger growth and profitability. It is important to acknowledge that the analysis relies on historical financial metrics, which may not fully capture a company’s current valuation reflecting its future prospects. Additional factors and considerations are necessary for a comprehensive assessment.


