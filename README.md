# Risk Constrained Portfolio Optimizer

Have a list of stocks you want to invest in but you don't want to lose any money? Want to make sure you're cash doesn't fluctuate too much? Not a big gambler and want stability? You've come to the right place then. Here's a Risk Constrained Portfolio Optimizer that will create an optimal Capital Preservation Portfolio where the variance is as low as possible. 

<hr>

## Fully configurable!
1. Download portfolio-optimizer.ipynb
2. Import a CSV of the tickers you're considering
3. Change the configurations at the top of the file to match your CSV file and other preferences (diversification, budget, analysis range, etc)
4. Click run and recieve a full breakdown of the portfolio, other the possible portfolio combinations, and compare your new portfolio to benchmarks
5. Get a CSV that contains your new portfolio. Go buy it now! (Not financial advice btw)

<hr> 

### High stability, Low Variance
This optimizer creates portfolios that are significantly less volatile then benchmarks:
https://github.com/neilhaoyuan/risk-constrained-portfolio-optimizer/blob/main/images/metrics.png?raw=true

Even during the extreme stock market drops caused by The United States's April 2nd tarrifs, the optimized portfolio (of the sample tickers) didn't dip below 0% returns unlike the benchmarks!
https://github.com/neilhaoyuan/risk-constrained-portfolio-optimizer/blob/main/images/port_v_bench.png?raw=true

Here's a glimpse of the optimization algorithm as it continuously checks to see if it has met sector diversification requirements:
https://github.com/neilhaoyuan/risk-constrained-portfolio-optimizer/blob/main/images/optimization_process.png?raw=true

<hr>

### Algorithm Overview
1. Filtering Input: Finding only valid tickers from the CSV
2. Extracting Info: Fetching ticker info using yfinance
3. Optimization Models: Three layers of optimization models (unbounded, bounded, sector_limited) with each layer respects more of the bounds and constraints configured by the user
4. Purchase Portfolio: Buys shares and performs exchange rate calculations for optimal portfolio
5. Output: Displays Capital Preservation Portfolio, and outputs a CSV
6. Backtesting and Analysis: Graphs out plots and compares historical performance against benchmarks

<hr>

The base code was originally for a Group Competition for UW's CFM 101 course where teams competed to create a Risk-Free stock picker. This code has since been indepdently repurposed and optimized it. It is signficantly faster, and more configurable compared to before. If you wish to see the original code please reach out.
