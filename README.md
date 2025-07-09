Capstone Project Overview

Objective:
To analyze product demand using features given and build a dynamic pricing model that adjusts prices based on demand and competitor pricing.

1. Dataset Overview:
The dataset consists of multiple product-related attributes such as:
Product id, product name
Category,sub category
Units sold, price, competitor price
rating, stock, discount
These features are used to predict demand and optimize pricing.
2. Demand Function:
I have define demand as a function of several variables, primarily:
Based on exploratory data analysis, a multiple linear regression (or tree-based models like Random Forest) is suitable to approximate this demand function:
I have also experimented with regularized regression (Ridge, Lasso) and tree-based models (Random Forest, Gradient Boosting).
3. Assumptions:
Price elasticity is linear within the range of values in the dataset.
Competitor price is considered constant in the short term.
Product quality is inferred from ratings and reviews.
Demand is only partially influenced by promotions and discounts.
The relationship between variables is assumed to be stable during the analysis period.
4. Pricing Strategy:
To determine dynamic pricing, I have adjust the  price using a rule-based logic:
High demand, low competition: Increase price by 5-10%
Low demand, high competition: Decrease price by 10-15%
Average demand, high competition: Match competitor price +/- 5%
Low stock: Slightly increase price to avoid stock-out
This price adjustment logic is implemented after training the demand model. The final price is:
Where is based on demand class and competitor comparison.
5. Tech Stacks Used:
Numpy
Pandas
Pathway
Matplotlib
Datetime
Bokeh
Panel




6. Visualizations:
Implemented using Bokeh:
Bar chart of predicted vs actual demand
Line chart for price vs units sold
Interactive scatter plots to explore correlation (price vs demand)
Histograms of demand class distribution
All graphs are dynamic and interactive, enhancing understanding of trends and model behavior.
8. Conclusion:
Machine learning models successfully predicted demand with good accuracy.
Pricing strategy aligned with demand signals increases potential revenue.
Future enhancements could include live data streams and reinforcement learning for real-time pricing.

