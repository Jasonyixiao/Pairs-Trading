**Project Objective:**

- The project implements and simulates a pairs trading strategy using Coca-Cola (KO) and PepsiCo (PEP) stocks.

**Key Assumptions:**

- Initial capital: $100,000 USD

- Interest rate: 5% annually

- Trade entered on Dec 29, 2023 by shorting KO and using proceeds to go long PEP

- Simulate 1,000,000 daily paths of this trade over 6 months

**Evaluate:**

- Expected value of the trade on Jan 16 if entered on Jan 9

- 5th and 95th percentile P&L

- Entry and exit thresholds based on spread

**Main Steps in the Notebook:**

1. Data Loading:
  - Historical data for KO and PEP (from 2019 onwards) is loaded and cleaned.

3. Spread Analysis:
   
  - Calculates the price spread between KO and PEP

  - Performs a linear regression of PEP on KO to determine hedge ratio

  - Analyzes distribution of spread and tests for normality

3. Simulation:

  - Simulates price paths using normal random walks with estimated daily mean and volatility

  - Includes correlation between KO and PEP

  - Simulates spread behavior and overlays simulated paths with actual price behavior

4. Trade Evaluation:

  - Estimates expected return and P&L distribution over selected dates

  - Sets entry/exit thresholds based on statistical spread deviations
