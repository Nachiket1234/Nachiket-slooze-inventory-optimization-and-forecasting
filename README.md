# Slooze Challenge: Inventory, Sales & Purchase Analysis and Optimization

**Submitted by: Nachiket**  
**Date: January 2026**

## Project Overview

This repository contains a complete, end-to-end data analytics solution for the Slooze take-home challenge. The goal is to analyze sales, purchase, and inventory data for a wine & spirits retail company to optimize inventory management, forecast demand, identify key trends, and improve procurement efficiency.

Despite the dataset covering only January (full) and February (partial) 2016 with a sharp post-holiday demand drop, the analysis delivers actionable insights using modern techniques, including deep learning-based forecasting (LSTM, LSTM+Attention, and Transformer).

## Key Objectives Achieved
- **Demand Forecasting**: Built and compared advanced time-series models (LSTM, LSTM+Attention, Transformer) to predict daily sales quantity.
- **ABC Analysis**: Classified products into A/B/C categories based on sales value (80/20 rule).
- **Inventory Optimization**: Calculated EOQ, Reorder Point (ROP), and safety stock recommendations.
- **Sales & Purchase Insights**: Identified top products, vendors, seasonality (strong weekend peaks), and supplier performance.
- **Process Improvement**: Recommendations to reduce stockouts/overstock, lower holding costs, and negotiate better vendor terms.

## Dataset
The analysis uses the public Kaggle dataset: [slooze-challenge](https://www.kaggle.com/datasets/sloozecareers/slooze-challenge)

Key files:
- `BegInvFINAL12312016.csv` – Beginning inventory snapshot
- `EndInvFINAL12312016.csv` – Ending inventory snapshot
- `SalesFINAL12312016.csv` – Sales transactions
- `PurchasesFINAL12312016.csv` – Purchase orders
- `InvoicePurchases12312016.csv` – Invoice-level purchases (freight, payment details)
- `2017PurchasePricesDec.csv` – Product master (prices, vendors)

## Technologies & Libraries Used
- **Python** (3.x)
- **Pandas**, **NumPy** – Data processing
- **Matplotlib**, **Seaborn** – Visualizations
- **Scikit-learn** – Scaling & metrics
- **TensorFlow/Keras** – LSTM & LSTM+Attention models
- **PyTorch** – Transformer model
```
## Project Structure
slooze-challenge-nachiket/
├── README.md                          # This file
├── Slooze_Main_Analysis.ipynb         # Primary notebook (data loading → final insights)
├── final_report.md                    # Executive summary with key findings & recommendations
├── requirements.txt                   # List of dependencies
└── plots/
├── transformer_forecast.png       # 30-day Transformer forecast plot
├── lstm_attention_forecast.png    # LSTM + Attention forecast plot
├── lstm_forecast.png        # Plain LSTM forecast plot
```

## How to Run
1. **Download the dataset** from the Kaggle link above and place files in a `data/` folder (or download directly in Colab using Kaggle API).
2. **Set up environment**:
   ```bash
   pip install -r requirements.txt

3. Run the notebook:
Open Slooze_Main_Analysis.ipynb in Jupyter/Colab.
Execute cells sequentially.
GPU recommended for Transformer (enable in Colab: Runtime → Change runtime type → T4 GPU).

Output: Visualizations, tables, and forecasts will appear inline. Key plots are saved/exported to plots/ folder.

Model Prediction Plots (30-Day Sales Quantity Forecast)
Transformer Forecast (Best Model – Most Stable)
Transformer 30-Day Forecast
<img width="1208" height="590" alt="image" src="https://github.com/user-attachments/assets/3e56f42b-052b-48bb-85e4-65cba6ce5b2e" />


LSTM + Attention Forecast
<img width="1208" height="590" alt="image" src="https://github.com/user-attachments/assets/ef4a767d-ff1f-4f00-977f-f692601684e6" />


LSTM Forecast
<img width="1208" height="590" alt="image" src="https://github.com/user-attachments/assets/adb71477-fadb-4008-8611-532ef6868541" />


Note: Transformer showed the lowest error (RMSE ~5,278 units) and the most realistic flat low-demand prediction after the post-holiday drop.
Key Findings

Top Products: Captain Morgan Spiced Rum, Ketel One Vodka, Jack Daniel’s No 7 dominate revenue.
ABC Results: ~20% of products (A-class) generate 80% of sales value.
Seasonality: Friday/Saturday sales significantly higher → plan weekend stock boosts.
Forecasting Winner: Transformer (RMSE ~5,278 units) provided the most stable low-demand forecast post-holiday drop.
Supply Chain: Reliable lead times (~7.6 days avg). Diageo is the dominant, reliable vendor.
Opportunities: Reduce C-class inventory, negotiate with slower high-volume vendors (e.g., Ultra Beverage).

Recommendations

Focus inventory control and forecasting on A-class items.
Use Transformer-based daily demand (~25–30k units) + ~5,300 unit safety stock + 20–30% weekend boost.
Prioritize fast/reliable vendors (Diageo, Jim Beam) and negotiate terms with high-volume slower ones.
Automate ROP/EOQ alerts to prevent stockouts and minimize holding costs.

Thank you for the opportunity! I enjoyed tackling this challenge with modern deep learning techniques despite the short dataset.
