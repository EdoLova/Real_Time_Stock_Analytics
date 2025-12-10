# Stock Market Streaming Analysis

This project performs a real-time analysis of stock market values using Apache Kafka and Apache Spark Structured Streaming.  
The system simulates a continuous market data flow and computes several key financial indicators over sliding and tumbling windows.

---

## Objectives
- Stream synthetic OHLC stock data through Kafka and process it with Spark Structured Streaming.
- Compute:
  - Daily price variance
  - Hourly and daily stock growth
  - Top-10 most traded stocks
  - Top-5 stocks by traded volume
  - Automatic stop-loss / take-profit strategy
  - Construction and tracking of a 5-stock portfolio
- Reproduce realistic market dynamics in a synthetic, high-frequency streaming environment.

---

## Tools and Technologies
- Python  
- Apache Kafka  
- Apache Spark Structured Streaming  
- Pandas, Matplotlib  
- Dataset: `stock.csv` (synthetic OHLC dataset)

Architecture:  
Kafka Producer → Kafka Topic → Spark Streaming Consumer

---

## Main Results
- Low-variance stocks such as DWDP and AES show minimal intraday price fluctuation.
- Strongest hourly and daily growth signals appear in ILMN, CHRW, and PRGO, with PRGO exceeding +120% daily increase.
- The most traded stocks by share count include BAC, AAPL, AMD, and MSFT.
- Capital flow (volume × price) is dominated by AAPL, AMZN, and Meta (FB).
- The stop-loss and take-profit mechanism demonstrates proper handling of risk under streaming volatility.
- A simulated 5-stock portfolio highlights real-time fluctuations and cumulative return behavior.

---

## Project Structure
Each task is implemented in a dedicated Jupyter notebook, since Spark Streaming queries produce continuous console output and cannot be executed simultaneously in a single notebook.

### Tasks
1. Daily Variance Analysis  
2. Hourly and Daily Growth Computation  
3. Top-10 Most Traded Symbols (by shares)  
4. Top-5 Stocks by Monetary Volume  
5. Stop-Loss / Take-Profit Strategy  
6. Construction and Monitoring of a 5-Stock Wallet  

---

## Author
Edoardo Lovato  
Université Claude Bernard Lyon 1  
Data Processing and Analytics (DPA)  
Academic Year 2025–2026  

---
