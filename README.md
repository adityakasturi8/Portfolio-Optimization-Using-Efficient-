# Portfolio Optimization Using Efficient Frontier
**ABSTRACT:**
In this project I am going to extract the stock data of five companies (from Feb 1st  2016 to March 26th  2021) listed in S&P 500 i.e., Amazon, Google, Facebook, General Electronic, and Tesla. then calculate their daily returns, portfolio returns, portfolio variance, and generate random portfolios using Monte Carlo Simulation. I will be using Markowitz model to find efficient frontier for the portfolio with minimum risk and the portfolio with maximum Sharpe ratio.

**Modern Portfolio Theory (MPT):**
It was formulated by Harry Markowitz in 1950s. He received noble prize in economics later. The main idea of the Modern Portfolio Theory is to combine several stocks to reduce the risk as much as possible.
Assumptions of modern portfolio theory:
1) The daily returns are normally distributed to describe the Mean(µ)  and variance (σ).
2) Investors are risk averse: They will take more risk if they expect more return.
Efficient Portfolio: The highest reward for a given level of risk or lowest risk for a given reward.

**Stock Data:** 
I have extracted the stock prices of Amazon (AMZN), Google ( GOOGL), Facebook(FB), General Electric (GE), and Tesla (TSLA) from 2016 Feb 1st to 2021 March 26th.  I have used Yahoo Finance to extract this data and have used Python Programming to plot and generate the data, shown in Table 1.
We can generate the expected rate of return and variance using the stock data. 
The extracted stock data contains everyday closing price of each stock.
Stock Graph:
Plotted the actual prices of the stocks which has been extracted. The plotted graph is shown below in Figure 1.

![stock_data](https://user-images.githubusercontent.com/95768375/160968861-89dc29e0-3e53-4e23-a794-38edadf2e8ec.JPG)

Table 1: Stock data of Everyday closing prices of individual stocks
 ![stock_data_graph](https://user-images.githubusercontent.com/95768375/160968909-4cb5f38a-a707-4edb-a96a-2addd89049e7.JPG)

Figure 1: Stock price variation from 2016 Feb 1st to 2021 March 26th 		
    

The above stock price variation graph shows that the Amazon and Google have the highest growth, while Facebook was stable and neutral. Tesla’s stock started to grow from early 2020’s. 
This graph was plotted based on everyday closing prices of individual stocks using matplotlib library of Python.

**Daily Returns: **

The Daily returns of the stock data was calculated using the following formula.
Daily return = (Today’s Price – Yesterday’s Price) / Yesterday’s price
It represents the percentage of the stock with respect to the yesterday’s price of the stock. The Table 2 shows the daily returns of every individual stock price.

![daily returns data](https://user-images.githubusercontent.com/95768375/160969075-201a3672-c44b-4306-8b73-7f198bd9faf5.JPG)
Table 2: Daily returns of the stocks 
  
The plot (Figure 2 & Figure 3) shows the daily returns of the assets combined and individual. From the below plot we can observe that the Google and Tesla are highly volatile and are the riskier assets to invest into.

<img width="596" alt="TSLA DAily" src="https://user-images.githubusercontent.com/95768375/160969155-a3c89b3d-14e6-4078-a00e-2bb56d03dc9f.png">
Figure 3: Combined Daily Returns Plot 
![graph returns](https://user-images.githubusercontent.com/95768375/160969183-deb2a800-6d7a-4cd7-8da8-986f4ef1585a.JPG)
Figure 4 : Individual Daily Returns Plot
          
**Expected Return of the protfolio:** 
The expected return of the portfolio depends on the percentage change of the daily returns of the individual sotcks.  Let r be the return for n stocks. And x be the investment such that (x=1 to n), then, E(Rp) be the expected return of investment x. 
Therefore, 
r = r1w1 + r2w2 + …. + rnwn
where r = rate of return

The Expected Portfolio Return formula: 
	E(Rp) = RT . W
Where R = Expected return of asset in an individual portfolio
	 W = weight of the an asset in an individual portfolio

**Variance of the Portfolio: **

The expected value of a random variable provides a useful summary of the probabilistic nature of the variable However, typically one wants, in addition, to have a measure of the degree of possible deviation from the mean. One such measure is the variance. The square root of the variance, denoted by a and called the standard deviation.
σp2 = WT . (cov W )
Where W = weight of an asset in an Individual portfolio.
	Cov = variance-covariance matrix
Covariance of matrix: 
It measures how much two random variables vary together. It gives the relation between the pair of variables. The diagonals of the covariance represent the variance of the matrix. 

![covariance matrix](https://user-images.githubusercontent.com/95768375/160969249-9a70b0ee-55d8-4059-b03a-047a1a801480.JPG)

Table 3: Covariance of Matrix
 

From the Figure 5, We can obtain that the tesla stock has high variance, i.e., it fluctuates, whereas google has low variance and is the most stable one.

**Correlation of matrix:**

![corelations_matrix](https://user-images.githubusercontent.com/95768375/160969306-24fa3f1a-20ee-4765-868c-759c56a3f782.JPG)

Table 4: Correlation of Matrix
 
∑ < 0 For a negative correlation, the returns would move inversely. ( if one stock      
 ij	goes up, other stock goes down as far as the price is concerned) . 

∑ > 0 For a positive correlation, the returns would move together. ( if we make 
 ij	profit with one stock we can also make profit with another ).
∑ >=0 There is no relation. i.e. whether one stock makes profit or loss, the other 
 Ij	 stock has no effect on it. 

Here, we have a positive correlation among all the stocks.

**Sharpe Ratio:**
The Sharpe Ratio is developed by William F. Sharpe.It is the important risk and/or returns measures which are used in Finance Sector. It describes how much excess return you receive for the extra volatility that you endure holding a riskier asset.

The Sharpe Ratio is calculated by using the following formula:
Sharpe Ratio = E(Rp) – Rf / σp
Where E(Rp) = average rate of return of an investment 
Rf = rate of return of risk-free rate
σp = standard deviation of the investment return
If Sharpe Ratio is > 1 it is considered to be good.
Monte-Carlo Simulation:
Monte-Carlo Simulation is an algorithm based which is used in the areas of optimization and numerical integration. This approach is based on random sampling. By using Mont- Carlo Simulation we can generate random portfolios and based on those portfolios we optimize Markowitz model and generate the efficient frontier.

![random portfolios](https://user-images.githubusercontent.com/95768375/160969493-3b8c6c55-32ef-4734-825c-ae881eaf134a.JPG)

Table 6 : Random portfolios generation using Monte-Carlo Simulation
 
We generate 10000 random portfolios with random weights , based on this we apply Markowitz model and form the efficient frontier. Using this approach we can find the portfolio with minimum volatility and portfolio with the maximum Sharpe ratio. 

Efficient Frontier: 
The Efficient Frontier shows the set of portfolios with a particular level of risk. The frontier line represents the optimal portfolios. The dots in the 2D plane represent different weights for different portfolios whereas the different colors represent different stocks.	
A frontier shows a set of portfolios that indicate the highest expected return for a given risk level or the lowest risk for a given level of expected return.
The Figure 9, represents the efficient portfolio with minimum volatility and portfolio with maximum Sharpe ratio. The Red Star represents the portfolio with minimum Volatility where as the Green star represents the portfolio with maximum Sharpe Ratio.

<img width="567" alt="eff" src="https://user-images.githubusercontent.com/95768375/160969584-a18fa58d-b466-450c-a2a9-974bd40c7cac.png">
Figure 5 : Efficient Frontier 

<img width="567" alt="Efficient Fronteir" src="https://user-images.githubusercontent.com/95768375/160969567-9f509a72-eff0-4e6a-9367-3efcbbca91a9.png">

Figure  6: Efficient Frontier with minimum volatility and maximum sharpe ratio
 
**Portfolio with maximum Sharpe Ratio:**

![max](https://user-images.githubusercontent.com/95768375/160969660-c61732da-2295-40c9-baf4-82a39ad89d0f.JPG)
Table 7: Portfolio with maximum Sharpe Ratio
 
The above portfolio has a returns of 119% with a Volatility of 44% and Sharpe Ratio of 2.72. The amount of investment for Amazon  (AMZN) is 21.85%, Google (GOOGL) is 4.79% , Facebook (FB) is 28.1%, General Electric(GE) is 2.2%, and Tesla(TSLA) is 68.2%
Portfolio with minimum Volatility: 

![min](https://user-images.githubusercontent.com/95768375/160969711-85439d2a-c73d-4ad5-96ab-0e5a7df98488.JPG)

 
The above portfolio has a returns of 21% with a Volatility of 23% and Sharpe Ratio of 0.88. The amount of investment for Amazon  (AMZN) is 29.3%, Google (GOOGL) is 45.5% , Facebook (FB) is 4.8%, General Electric(GE) is 19.6%, and Tesla(TSLA) is 0.5%

**Summary** 
Modern portfolio theory aims to make an investor invest in several stocks to reduce the risk, by using Monte Carlo simulation generated 10000 random portfolios. The Risk averse investors would invest in low-risk stocks with low return, i.e. 23% risk gave 21% returns from this project where as Risk seeking investor would invest in high-risk stocks with high returns, i.e. 44% risk and 119% returns from this project. 
I have considered 5 companies in this project, but this can be extended to n number of companies. Extending further, By using Time series analysis future prices of the stock could also be implemented.

**References:** 
1) D. Luenberger, Investment Science, 2nd Edition, 2014
2) Harry Markowitz. Portfolio selection. Journal of finance; Vol 7; 77-91
3) Cong, F., and Cornelis Oosterlee. “Multi-Period Mean–Variance Portfolio Optimization Based on Monte-Carlo Simulation.” Journal of Economic Dynamics and Control, Elsevier, 1 Jan. 1970,
4) “Multiobjective Extremal Optimization for Portfolio Optimization Problem.” IEEE Xplore, ieeexplore.ieee.org/document/5357781.




