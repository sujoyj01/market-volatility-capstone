# market-volatility-capstone
Predictive Dynamics of Equity Volatility and Portfolio Optimization on the NSE
Market Volatility Capstone: Predictive Dynamics of Equity Volatility and Portfolio Optimization

This repository contains the code, models, and documentation for a Doctorate of Business Administration (DBA) capstone project evaluating machine learning architectures for short-term price volatility forecasting.

Project Overview

The primary objective of this study is to compare the predictive accuracy of advanced deep learning models (specifically Long Short-Term Memory or LSTM networks) against traditional econometric models (GARCH/ARIMA) in forecasting short-term market volatility. Furthermore, the project translates these forecasts into practical business applications by simulating optimized investment portfolios and measuring their risk-adjusted returns (Sharpe Ratios) during periods of macroeconomic shock.

Core Research Questions

Architectural Comparative Accuracy: Does an LSTM network demonstrate a statistically significant improvement in short-term price prediction accuracy (RMSE) compared to traditional econometric models for Indian equities?

Firm Fundamentals: What is the statistical relationship between a firm's financial fundamentals (Leverage, Size, P/E) and its baseline annualized equity volatility?

Computational Efficiency: What are the measurable trade-offs in computational efficiency and training time between standard and high-performance computing (GPU) environments for these time-series datasets?

Predictive Robustness: Does the predictive accuracy of the optimized deep learning model degrade significantly during historical periods of extreme market volatility?

Data Sourcing and Reproducibility

To ensure complete reproducibility and adhere to GitHub file size limits, large financial datasets are not hosted directly in this repository.

All data utilized in this study is sourced from the public domain via the Yahoo Finance API and Screener.in. To replicate this study and generate the necessary datasets locally:

Ensure all dependencies listed in requirements.txt are installed.

Execute the data ingestion notebook located at notebooks/01_data_ingestion_and_eda.ipynb.

This script utilizes the yfinance library to dynamically fetch historical daily pricing data (OHLCV) for the NIFTY 250 constituents, alongside the 10-Year Indian Government Bond yield (^IGB10Y) serving as the macroeconomic benchmark.

The script will automatically generate the required CSV files and populate the data/raw/ and data/processed/ directories on your local machine.

Repository Structure

The project is organized to separate data processing logic, exploratory analysis, and production models:

data/: Ignored by version control. Generated locally via ingestion scripts.

raw/: Unedited CSVs downloaded via APIs or Screener.in.

processed/: Cleaned, merged datasets ready for modeling.

notebooks/: Jupyter notebooks for interactive analysis, EDA, and step-by-step documentation of the modeling process.

src/: Reusable Python scripts containing core logic.

models/: Contains the architecture definitions for the GARCH and LSTM models.

data_loader.py: Reusable functions for data extraction and cleaning.

portfolio_optimizer.py: Logic for simulating portfolio performance and calculating Sharpe Ratios.

requirements.txt: A complete list of Python dependencies required to execute the code.
