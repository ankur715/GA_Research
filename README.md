# GA_Research
### Research to create techniques to achieve greater terminal wealth over a fixed time horizon for adults 60 – 70 years old

### Abstract 

Goals Based Wealth Management is a novel framework where risk is understood as the probability of investors not attaining their goals, not just the standard deviation of investor portfolios. Das et. al. (2019) describe a dynamic programming algorithm which given a set of efficient portfolios constructs an optimal portfolio trading strategy that maximizes the probability of attaining an investors specified target wealth at the end of a designated time horizon. Das et. al (2019) created a hypothetical Target Date Funds (TDF) using three index funds representative of U.S. Bonds, International Stocks and U.S. Stocks along with typical glide path allocation (GPA) for investors transitioning from age 50 to age 80. We deploy their GPA as well as their TDF in our analysis. We conjectured an alternative technique to achieve greater terminal wealth over a fixed time horizon. We devised an algorithm which allows us to successfully side-step the vagaries of an economic life cycle. We apply machine learning techniques, due to Hauck(2014), such as k-means clustering, bayesian ridge regression, logistic regression, decision trees (random forest) and support vector machines (SVM). Time periods of “Recession” and “Pullbacks”, refer to Clearbridge (2020), are identified by our classification algorithms which utilize, ‘Treasury Yield Spreads, ISM Manufacturing Purchasing Managers Index, Change in Non-Farm Payroll and GDP QoQ as input variables. We overlaid our classification algorithm on the GPA for people between the ages of 60 and 70 years. Our benchmark GPA is simulated over a 5 year rolling horizon (60-65 & 65-70) as well as over a 10 year rolling horizon (60-70)(10Y6070). Assuming an initial investment of $100,000 dollars we estimated the mean return for our 5 year rolling horizon for the 60-65 year olds (5Y6065) at $144,508 and for the 65-70 year olds (5Y6570) at $ 141,676 respectively, while for 10Y6070 the mean return was $ 204,966. When we exited the market based on one of the classification algorithms, just before a recession and stayed out for a fixed time period of 11 months (average tenure of the last 4 recessions) we obtained no substantial difference in the mean value of terminal wealth (10Y6070, $204195, 5Y6065, $145063, 5Y6570, $140994) but if we re-entered the market based on one of our classification algorithms the results were (10Y6070, $208554, 5Y6065, $146189, 5Y6570, $142065) vastly improved. In the final analysis Machine Learning Classification Algorithms clearly add value as we obtain mean values for Terminal Wealth higher than a pure GPA based algorithm.

#### Code 
"benchmark_testing" is code for obtaining our benchmark results. Used glide path allocation the whole time. Allocation was not changed for recessions 

“rule_testing” is code for testing how our rules for predicting a recession fared. When a recession was predicted the allocation went to cash. Not in recession the allocation was the glide path allocation.  Other tests were run with the same code but when a recession was predicted the allocation was 50% gold 50% bonds on one test and the other test was 75% bonds 25% gold. 

“high_yield_cash” is code for testing how our rules for predicting a recession fared. When a recession was predicted the allocation went to cash. When the rules predicted not in a recession the allocation was a more aggressive allocation than the glide path allocation.  Other tests were run with the same code but when a recession was predicted the allocation was 50% gold 50% bonds on one test and the other test was 75% bonds 25% gold. 
