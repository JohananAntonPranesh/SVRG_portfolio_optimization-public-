

---

# Hybrid Approaches to Portfolio Optimization: Integrating Bandit Algorithms and SVRG for Factor Exposures

## Overview

This project explores the combination of **Bandit Algorithms** and **Stochastic Variance Reduced Gradient (SVRG)** methods to enhance portfolio optimization. Specifically, it aims to optimize factor exposures in a portfolio by balancing exploration and exploitation using Bandit algorithms, while leveraging the efficiency of SVRG to handle large datasets and accelerate convergence.

### Key Objectives:
1. **Compare Portfolio Optimization Techniques:**  
   Evaluate the performance of portfolio optimization methods, comparing the integration of Bandit algorithms with SVRG to traditional approaches.
   
2. **Assess the Impact of SVRG:**  
   Understand how SVRG contributes to faster convergence and more effective handling of factor exposures and constraints.

3. **Factor Investing Strategy with Bandit Algorithms:**  
   Use Bandit algorithms to dynamically explore and exploit factor combinations that improve portfolio returns while managing downside risk.

## Approach

### 1. **SVRG (Stochastic Variance Reduced Gradient):**
   - **Efficient Convergence:**  
     SVRG reduces the variance in gradient estimates, which accelerates the convergence of optimization algorithms, especially when dealing with large datasets.
   
   - **Handling Constraints:**  
     SVRG effectively integrates portfolio constraints like transaction costs and weight limits, ensuring stable weight updates while reducing optimization complexity.

   - **Factor Exposure Exploration:**  
     The optimization process seeks factor combinations that provide better risk-adjusted returns and enhanced downside protection compared to a benchmark portfolio.

### 2. **Bandit Algorithms:**
   - **Exploration vs. Exploitation:**  
     The Bandit algorithm intelligently balances exploration (trying out new factor combinations) and exploitation (focusing on the best-performing factor combinations).
   
   - **Computational Efficiency:**  
     By prioritizing exploration early on and transitioning to exploitation later, Bandit algorithms help optimize computational resources while improving overall performance.

   - **Factor Selection:**  
     The Bandit framework guides the selection of factor combinations that maximize portfolio performance, focusing on risk-return trade-offs.

## Project Structure

This project is contained within a single file: `initial_data_processor.py`. The file includes three main components:

1. **Gradient Function:**  
   Implements gradient calculations required for optimization.

2. **SVRG Optimizer:**  
   Contains the implementation of the SVRG algorithm to optimize factor exposures while handling large datasets and constraints.

3. **Bandit Algorithm:**  
   A class-based implementation of the Bandit algorithm that explores and exploits various factor combinations to optimize the portfolio.

## File Overview

### `initial_data_processor.py`

This file contains all the necessary code to process the data, perform portfolio optimization, and evaluate the results.

- **Data Preprocessing:**  
  Initial data processing for asset returns and factor exposures is handled within the script. The data is prepared for both Bandit exploration and SVRG optimization.

- **Gradient Function:**  
  A function that calculates the gradient for portfolio optimization, helping to adjust factor weights effectively during the optimization process.

- **SVRG Optimizer:**  
  Implements the SVRG method for portfolio optimization. It works by reducing variance in gradient estimates and efficiently handling constraints like transaction costs, ensuring that portfolio weights converge faster.

- **Bandit Algorithm Class:**  
  The Bandit algorithm class handles the exploration-exploitation trade-off for selecting optimal factor combinations. It employs an epsilon-greedy strategy to explore factors in the beginning and exploit them later for better performance.


## Running the Project

1. **Preprocessing the Data:**  
   Begin by executing the `initial_data_processor.py` file, which handles the data preprocessing, gradient calculations, and portfolio optimization. The data will be processed and prepared for optimization.

2. **Portfolio Optimization:**  
   Use the Bandit algorithm to explore and exploit different factor combinations. The SVRG optimizer will then be used to optimize the portfolio by reducing variance in the gradient estimates.

3. **Evaluation:**  
   The performance of the optimized portfolio can be evaluated by examining the risk-return characteristics and comparing it against a benchmark (e.g., a simple equal-weight portfolio or a benchmark index).


```

## Performance Evaluation

After running the optimization process, evaluate the portfolio performance based on standard financial metrics such as:

- **Sharpe Ratio:** A measure of risk-adjusted return.
- **Max Drawdown:** The maximum observed loss from a peak to a trough.
- **Annualized Return:** The expected yearly return of the portfolio.

## Conclusion

This project demonstrates how the hybrid approach of using Bandit algorithms and SVRG optimization can enhance portfolio management. By intelligently balancing exploration and exploitation, and leveraging the speed and efficiency of SVRG, we can construct portfolios that are better suited to adapt to changing market conditions, with improved downside protection and optimized returns.
