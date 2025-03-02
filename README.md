# Financial Modeling for Option Pricing  

This project explores the application of the **Heston Stochastic Volatility Model** for option pricing, combining traditional finance theories with machine learning techniques. The project includes Monte Carlo simulations and model calibration for accurate option pricing.  

## Project Overview  

- **Objective**: Implement and analyze the Heston model for option pricing using Monte Carlo simulations and calibration techniques.  
- **Approach**:  
  1. Monte Carlo Simulation for option pricing using the Heston model.  
  2. Model calibration using market data to improve pricing accuracy.  

## Theoretical Background  

The **Heston Model** is a stochastic volatility model that assumes volatility follows a mean-reverting square-root process. It is defined as:  

\[
dS_t = \mu S_t dt + \sqrt{v_t} S_t dW_t^S
\]

\[
dv_t = \kappa (\theta - v_t) dt + \sigma \sqrt{v_t} dW_t^v
\]

where:  
- \( S_t \) is the asset price  
- \( v_t \) is the variance  
- \( W_t^S \) and \( W_t^v \) are two correlated Wiener processes  
- \( \mu, \kappa, \theta, \sigma \) are model parameters  

## Implementation  

### 1️⃣ Monte Carlo Simulation  
- **Methodology**: Simulated asset paths using the **Euler-Maruyama scheme** for numerical stability.  
- **Resources**: Python (`numpy`, `pandas`, `matplotlib`), `scipy`, `quantlib`.  
- **Results**: Obtained option prices but noticed discrepancies with expected market values.  

### 2️⃣ Model Calibration  
- **Methodology**: Optimized model parameters using real market option prices.  
- **Algorithm**: Used Least Squares to minimize errors between Heston model prices and observed prices.  
- **Results**: Improved accuracy but some discrepancies remained, likely due to:  
  - Approximation errors in numerical schemes  
  - Market frictions and liquidity effects  
  - Incorrect estimation of risk-neutral parameters  


## Results and Observations  

- Initial Monte Carlo pricing did not match expected values.  
- Calibration improved pricing accuracy but still had some errors.  
- Possible refinements:  
  - Using **Quasi-Monte Carlo** for variance reduction.  
  - Incorporating **Fourier Transform methods (COS/Fang-Oost)** for faster pricing.  
  - Adjusting risk-neutral drift correction.  

