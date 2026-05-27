1. **Data Ingestion Module:** Pull Historical daily OHLCV (Open, High, Low, Close, Volume) data for a highly volatile asset class (e.g., small-cap equities or derivatives)

2. **Strategy Generator (High Capacity):** Create an algorithm that evalutes a complex combination of dozens of technical indicators (e.g., varying periods of RSI, MACD, Bollinger Bands) to find an optimal trading rule.

3. **The Overfitter:** Intentionally tune the strategy parameters using a brute-force grid search until you achieve a pristine, flawless equity curve on training period (e.g., 2021-2024).

4. **The Auditor Engine (The Core Value):** Implement a validation framework based on Marcos Lopez de Prado's **Probability of Backtest OVerfitting (PBO) ** framework.

    - Use **Combinatorial Purged Cross-Validation (CPCV)** to split the historical data into non-contiguous matrix sub-intervals.

    - Run the strategy parameters across these permutations to measure exactly how fast performance degrades when the sequence of market regime shifts slightly.

5. **Regularization Layer:** Implement an information-theoretic penalty (like Akaike Information Creterion (AIC) or Bayesian Information Criterion (BIC)) directly into the strategy selection loop to penalty strategy configurations that use too many parameter rules.
