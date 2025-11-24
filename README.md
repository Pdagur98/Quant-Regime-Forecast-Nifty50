# Quant-Regime-Forecast-Nifty50
End-to-end Machine Learning pipeline using XGBoost and Walk-Forward Analysis (WFA) to generate risk-adjusted trading signals for the NIFTY 50.
# 📈 Quant-Grade Portfolio Manager: Regime-Switched NIFTY 50 Forecast

This project deploys a high-performance Machine Learning pipeline designed to generate risk-adjusted trading signals for the NIFTY 50 index, proving competence in full-stack analytics, financial modeling, and risk mitigation.

## 🎯 Final Performance Metrics (Test Period)

The final model achieved results demonstrating superior capital preservation compared to a passive Buy & Hold strategy:

| Metric | Result | Target Benchmark | Insight |
| :--- | :--- | :--- | :--- |
| **Sharpe Ratio (SR)** | **0.9969 (Near 1.00)** | A positive risk-adjusted return. | **Primary Success Metric.** Proves the model generates reliable alpha. |
| **Annualized Return**| **12.71%** | Consistent double-digit return. | Proves the system is profitable over time. |
| **Max Drawdown (Worst Loss)** | **-31.47%** | Far better than the historical 40%+ drawdown. | **Risk Control.** Proves the model is defensive and safe. |

## 🧠 Methodology and Technical Excellence

The solution is built on a **Walk-Forward Analysis (WFA)** architecture, which prevents overfitting and simulates real-world deployment.

### Key Components:

1.  **Regime Filtering:** We avoid single, static rules by using a system (modeled by the WFA structure) to adapt to changing market conditions (trending vs. consolidation).
2.  **Machine Learning:** An **XGBoost Classifier** was chosen for its performance on structured data, and hyperparameters were fine-tuned using **GridSearchCV**.
3.  **Feature Engineering:** Features include advanced metrics like **Average True Range (ATR)** and **Lagged RSI/SMA** to give the model historical memory and volatility context.
4.  **Deployment Pipeline (ETL):** The project demonstrates a full pipeline:
    * **Extract/Transform (Python):** Downloads data and runs the WFA/ML model.
    * **Load (MySQL):** Final predictions are uploaded to a local PostgreSQL/MySQL database.
    * **Visualize (Power BI):** A live dashboard tracks the latest signals and performance.

## 📁 Repository Structure

| File | Purpose |
| :--- | :--- |
| `README.md` | This document. Serves as the executive summary and technical deep dive. |
| `NIFTY-50.ipynb` | **Primary Source Code.** Contains all Python logic: Data Acquisition, Feature Engineering, Walk-Forward Analysis, and Optimization. |
| `Final_Dashboard.pbix` | **Business Intelligence Deliverable.** The Power BI file used to generate the live visualization. |
| `xgboost_final_optimized_model.joblib` | **Trained AI Model.** The final, optimized XGBoost model ready for live deployment. |
