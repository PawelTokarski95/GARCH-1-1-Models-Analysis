# GARCH-1-1-Models-Analysis

- **Language**: R


In this project, I analyze three versions of the popular financial volatility model: the standard GARCH(1,1) with a normal distribution, and two other with heavy-tailed distributions — Student’s t (std) and skewed Student’s t (sstd). These models show how volatility in time series, especially financial returns, changes over time.

The data comes from 5 different markets (ETFs), divided into two periods:

Pre-COVID period: from 2015 till 2020,
COVID and post-COVID period: from 2020 till today.

The goal is to check how volatility and risk changed on these markets in these different conditions, and to check if the simple GARCH(1,1) model with a normal distribution can be representative in terms of the existance of extreme events.

Before modeling, I analyzed the return distributions in both periods to see if they have the signs of a normal distribution. This is important because the presence of “black swan” events — that are rare and extreme market events — causes heavy tails and asymmetries, violating the normality assumption.

The term black swan was popularized by Nassim Nicholas Taleb in his book “The Black Swan.” It describes unpredictable events with huge impacts on financial markets, like the 2008 financial crisis or the COVID-19.

![51q4Y+EKElL _SY445_SX342_](https://github.com/user-attachments/assets/694ce5c1-31b4-4317-9797-6bb8d4601a27)



1. What is GARCH(1,1)?
   
The standard GARCH(1,1) model estimates and forecasts conditional volatility by assuming that today’s volatility depends on:
-The volatility from the previous period,
-The size of the shock (return) from the previous period.

2. Limitations of GARCH(1,1) with normal distribution
   
The biggest limitation is that the standard GARCH assumes symmetrical shocks and normal distribution of new events. In reality, financial returns often show heavy tails, meaning extreme values happen more often than in a normal distribution.
In that cases, the normal GARCH model underestimates risk, ignoring the chance of extreme market moves — in other words, it does not capture black swan events.

3. Extending the model with heavy-tailed distributions

To better capture real risk, I used GARCH(1,1) models with:
-Student’s t (std),
-Skewed Student’s t (sstd) distributions.
These allow modeling of heavy tails and asymmetry in return distributions, giving a more realistic estimation of the risk of extreme events.

4. Analysis on different markets

I used data from various markets (US, Europe and Asia) represented by ETFs. I split the data into pre-COVID and COVID/post-COVID periods to study changes in volatility behavior and model performance during major market shocks.

5. Results

The normal distribution was never proper — normality tests (Jarque-Bera) showed strong deviations from normality in all markets and periods.

Models with heavy-tailed distributions (std and sstd) fit better and gave more accurate volatility forecasts than the normal GARCH.

Diebold-Mariano test showed statistically significant improvement of heavy-tailed models (especially sstd) over the normal GARCH.

The simple GARCH(1,1) with a normal distribution is not representative for modeling volatility on markets affected by extreme events and black swans.

![kombinations](https://github.com/user-attachments/assets/308706ad-74d8-486f-b8ac-76c0dc8bf7ea)




