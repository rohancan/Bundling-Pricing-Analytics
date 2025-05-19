# Bundling-Pricing-Analytics


### Objective 

The goal of this project is to build a smarter, more accurate pricing strategy for a bundle of two P&G products—Tide (laundry) and Febreze (air freshener). We aim to understand how pricing affects sales, especially when both items are sold together, and find the best price that earns the most money. Instead of relying on assumptions or fixed formulas, this revised version uses actual sales data and machine learning models to forecast sales and recommend optimal bundle prices week by week. This approach better meets our professor’s expectations and the real-world needs of business stakeholders.

### Demand Forecasting 

Originally, we used a simple formula (OLS regression) to guess how many bundles would sell at different prices. That worked well for basic insights but missed real-world complexity. In this updated version, we kept the same variables—price, seasonality, and time trends—but added more powerful models to improve predictions.

What's New:

We used supervised machine learning models like Random Forest and Ridge Regression to improve accuracy.

The best model (Random Forest) could detect non-linear patterns in consumer behavior, which basic regression could not.

We trained these models using weekly Tide sales and simulated Febreze data to form a realistic view of bundle sales.

Instead of assuming how people react to prices, we let the computer learn from past data and then predict future sales. This gives us a much clearer idea of what works.


### Price Optimization 

We originally used Excel Solver to find the best price that would earn the most money, but Solver was based on a fixed formula and assumptions. It did not adapt well to real-world changes like seasonal sales trends or demand shifts.

What Changed:

We simulated prices between $20 and $35 for the next 13 weeks.

For each price, the Random Forest model predicted expected sales.

We then calculated revenue by multiplying price × predicted sales.

The price with the highest revenue for each week was chosen as the "optimal price."

Key Results:

Optimal prices mostly ranged between $31 and $32.

This aligned closely with real sales patterns and avoided the limitations of manual Solver adjustments.

Instead of guessing or testing prices by hand, we trained a smart model to try every possible price and tell us which one would make the most money. It gave us better answers in less time.

### Benchmarking vs. Baseline Performance 

Earlier, we said the bundle caused a $122K revenue loss due to lower sales. With better modeling, we now have stronger evidence to explain why:

Only 5% of customers buy both products, meaning the audience for the bundle is very small.

53% buy neither, which makes conversion extremely difficult even with discounting.

Giving the bundle too much shelf space took away visibility from core products.

Clarification:
Our model confirms that the loss was not because the price was wrong, but because the bundle had limited appeal and over-replaced more popular individual items.

The bundle didn’t fail because of pricing. It failed because not enough people wanted both products, and putting it on the shelf took attention away from products people actually wanted.

Section 8: Technical Reflection & Recommendations (Expanded)

In our original analysis, we used linear models and Solver-based assumptions. These were easy to understand but not powerful enough for real decision-making. Our revised version addresses these gaps.

What Improved:

Added supervised machine learning (Random Forest) for more realistic demand forecasts.

Detected patterns like non-linear price sensitivity that simpler models missed.

Replaced Excel Solver with a programmatic simulation that tested dozens of price points and selected the best ones.

Recommendations for Future Work:

Continue using Random Forest and explore other models like XGBoost for advanced forecasting.

Incorporate competitor pricing and promotions to improve predictions.

Use live market data for real-time A/B testing before national rollout.

In Simple Terms:
We upgraded from basic tools to smarter models that help us make better pricing decisions. These models are more accurate and flexible and provide a much better way to test ideas before launching them.


