# The Impact of Market Sentiment on extreme growth AI firms.

Welcome to the repository for my thesis work! This README provides an overview of the research topic, methodology, data, and instruments used. If you find this project helpful, please consider giving it a star. Thank you for visiting!

---

## Table of Contents
1. [Overview & Motivation](#overview--motivation)  
2. [Understanding Market Sentiment](#understanding-market-sentiment)  
   - [Sentiment Proxies](#sentiment-proxies)  
3. [Data Description](#data-description)  
4. [Econometric Methodology](#econometric-methodology)  
5. [Analytical Instruments & Tools](#analytical-instruments--tools)  
6. [References & Further Reading](#references--further-reading)

---

## Overview & Motivation

**Why This Thesis Matters**  
This thesis investigates the intricate relationship between market sentiment and asset prices. Market sentiment, broadly defined as the overall attitude of investors toward a particular market or security, can often explain anomalies and short-term price fluctuations. As Baker and Wurgler (2006) show, investor sentiment can influence asset prices, affecting returns and shaping overall market dynamics. By combining robust econometric techniques with advanced machine learning algorithms, this thesis aims to provide a new perspective on how market sentiment can be measured, modeled, and used in predictive frameworks.

**Main Objectives**  
- First, it seeks to adapt the Baker and Wurgler (2006) framework, which originally demonstrated that when beginning-of-period sentiment proxies are low, subsequent returns tend to be higher for small, young, high-volatility, unprofitable, non-dividend-paying, extreme growth, and distressed firms. Conversely, when sentiment is elevated, these categories of firms generally experience lower subsequent returns.
- Second, this study extends the existing analysis by incorporating additional proxies for investor sentiment, including the NASDAQ-100 Volatility Index (VXN) and momentum factors. These indicators capture recent stock price movements and are expected to yield deeper insights into how volatility and momentum patterns interact with or amplify, sentiment-driven anomalies in pricing and performance.
- Third, the study examines how these dynamics differ before and after the onset of the “AI hype” era, using the introduction of ChatGPT as a key temporal inflection point. The launch of ChatGPT represents a significant milestone in AI development, that dramatically heightened public and investor interest and directed substantial market attention and capital flows toward this technology class. By segmenting the analysis into pre- and post-ChatGPT periods, the study can more accurately capture shifts in investor sentiment and market dynamics. 
   
---

## Understanding Market Sentiment

Market sentiment is a **qualitative** measure of how investors feel about market conditions and specific assets, often influenced by behavioral biases, news flow, and macroeconomic events. In this thesis, sentiment is translated into **quantitative** proxies for more rigorous analysis.

### Sentiment Proxies

1. **CEFD (Closed-End Fund Discount)**  
   - Measures the difference between a closed-end fund’s Net Asset Value (NAV) and its market price.  
   - Interpreted as a proxy for investor sentiment because discounts/premiums often reflect behavioral factors rather than intrinsic value.
   \[
   \text{CEFD}_t = \frac{\text{NAV}_t - \text{Price}_t}{\text{NAV}_t} \times 100\%
   \]

2. **Share Turnover**  
   - Defined as the ratio of traded shares to total shares outstanding over a certain period.  
   - Reflects trading activity levels, which can serve as a barometer for market excitement or caution.
     \[
     \text{Share Turnover}_t = \frac{\text{Volume}_t}{\text{Shares Outstanding}_t}
     \]

4. **VXN (CBOE Nasdaq Volatility Index)**  
   - A volatility index for the Nasdaq 100.  
   - Captures implied volatility and investor expectations for near-term market movements.

5. **Momentum**  
   - Generally measures the rate of change or relative strength of a security’s price over a specified period.  
   - In this thesis, it serves as a sentiment proxy, assuming that sustained upward price trends indicate positive sentiment, and vice versa.


## Data Description

Data was collected from a variety of financial data providers and aggregated into a consistent format suitable for the analyses. Below are the main points regarding data collection and preprocessing:

- **Time Horizon**: *2021-2024*  
- **Frequency**: *Weekly*  
- **Data Sources**: *CRSP, Yahoo Finance, Bloomberg, etc.*  
- **Variables Collected**:  
  - **Prices** (for Momentum calculations)  
  - **Volume & Shares Outstanding** (for Share Turnover)  
  - **Closed-End Fund NAV & Market Price** (for CEFD)  
  - **Volatility Index (VXN)**

---

## Analytical Instruments & Tools

Multiple techniques were employed to ensure a comprehensive analysis:

1. **Random Forest**  
   - A machine learning approach for classification/regression.  
   - Helped capture non-linear relationships between sentiment indicators and target variables (e.g., returns).

2. **Ordinary Least Squares (OLS)**  
   - Baseline method for establishing linear relationships.  
   - Served as a benchmark for comparing more complex models.

3. **Principal Component Analysis (PCA)**  
   - Used to reduce dimensionality and extract underlying sentiment factors from the set of proxies (CEFD, Share Turnover, VXN, Momentum).
---



**Thank you for reading!**  
If this repository or the thesis is helpful to you, please consider citing or acknowledging this work in your own research. Don’t forget to star the repo if you find it useful!

> **Disclaimer:** This project is for academic and informational purposes only. The author is not responsible for any investment decisions or actions taken based on the content of this repository.
