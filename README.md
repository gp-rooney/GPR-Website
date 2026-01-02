TL;DR 
Data on some S&P names have low R² to SPY, so auto SPY betas can be noisy. Keep SPY as baseline; switch benchmarks only with a clear business rationale, and show WACC sensitivity.

Method: R² of each S&P 500 stock’s weekly return vs SPY as of past three years. Collected data via a python script. (dm if you are interested in looking at it)

A couple of days ago, I was looking at FUTU’s calculated WACC and Aaron and I realized that the beta used was calculated based on FUTU being indexed to the S&P 500. We thought that was strange considering it’s a company that makes their revenue from Southeast Asia and it made me wonder if there were other Equities in the S&P 500 that may not correlate with the index. This could be a problem because the calculations of the WACC that Bloomberg automatically provides may not be the best index to base it off of. 

Also, with the MAG 7 being 37% of the S&P 500, I was wondering what their level of correlation with SPY was. My hypothesis was that they would all be in the top 50, but it turns out I was slightly wrong. Ranked from highest R^2 to least: 

MSFT: 10 (R^2 = 0.547)
AAPL: 14 (R^2 = 0.524)
AMZN: 15 (R^2 = 0.522)
NVDA: 22 (R^2 = 0.514)
GOOG: 137, 145 (R^2 = 0.373)
TSLA: 248 (R^2 = 0.291)
META: 288 (R^2 = 0.248)

Make whatever hypothesis you want to make from that information. 

What stood out to me was the high R^2 were financial services and conglomerates; the low R^2 was healthcare and consumer defensive. I didn’t look beyond the ten, but I imagine that trend continues. 

Takeaway:
From the data, if you are creating your DCF and using Bloomberg’s automatically calculated WACC, it is likely correct for companies that are more B2B/industry focused. 

But if you are pitching a company that is more B2C with essential goods like foods and healthcare, be careful with the automatically calculated beta. The low R^2 means the beta estimate is noisy, and it would be prudent to cross-check against other relevant benchmarks, before using the default WACC in your model. 

Appendix:
Here are some additional charts that go into more detail on the distribution of R^2. 
