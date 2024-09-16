# Heston Stochastic Volatiltiy Modelling 

## A full implementation of the Heston model to price European call options using historical data
This project implements the Heston Stochastic Volatility Model, where both the price and volatility follows a Brownian motion. The model captures the dynamics of asset prices with stochastic volatility, providing a more realistic framework compared to the traditional Black-Sholes model. Code is in Jupyter Notebook in the Heston_model_venv folder written in Python.

## Contents
- **Implementation**: Code for the Heston model including the characteristic function, inverse fourier transform and numerical integration to obtain closed form price for European options
- **Data Reading and Cleaning**: Reading a year of option data, cleaning and transforming the data using pandas 
- **Calibration**: Employing a least squares method for Heston objective function (error between model price and market price), calibrating parameters using scipy minimize on the objective function
- **Monte Carlo Simulation**: Validating implementation and calibration through simulations of asset price paths under the Heston framework.
- **Comparison with Black-Scholes Model**: Performance testing by forward testing (RMSE as performance metric) of Heston model compared to the Black-Sholes Model
  
## Requirements
To run this notebook, make sure you have the following Python packages installed:
- `numpy`
- `pandas`
- `matplotlib`
- `scipy`
- `plotly`

Options data (EOD) is obtained for free from https://www.optionsdx.com/
Fther calibration to code (sorting options to include in calibration and initial parameters guess) is needed depending on the option for better performance in modelling.
