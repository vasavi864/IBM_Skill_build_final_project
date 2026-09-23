# Hotel Booking Demand & Operations Analysis

A comprehensive exploratory data analysis (EDA) and predictive modeling project examining 119,390 historical hotel booking records (2015–2017) across a **City Hotel** and a **Resort Hotel**. This repository provides insights into customer booking behaviors, revenue seasonality, cancellation drivers, and operational bottlenecks, along with actionable business strategies and predictive machine learning models.

## 📌 Project Overview

High cancellation rates and indirect distribution reliance present major revenue leakage risks in hospitality management. This project analyzes real-world hotel booking data to uncover core demand patterns and operational inefficiencies.

### Key Insights Summary

* **Dataset Size:** 119,390 bookings (66.4% City Hotel, 33.6% Resort Hotel)
* **Overall Cancellation Rate:** 37.0% (City Hotel: 41.7% vs. Resort Hotel: 27.8%)
* **Average Lead Time:** 104 days (Bookings >120 days in advance exhibit >54% cancellation probability)
* **Channel Distribution:** Online Travel Agencies (OTAs) drive 47.1% of total volume with a 41.1% cancellation rate.
* **Customer Retention:** Aggregate repeat guest rate is extremely low at 3.2%.

---

## 📁 Repository Structure

```text
.
├── data/
│   └── hotel_bookings.csv             # Primary raw dataset (119,390 records)
├── notebooks/
│   └── eda_hotel_demand.ipynb         # Complete Jupyter Notebook with data cleaning & visual EDA
├── models/
│   └── cancellation_prediction.pkl    # Trained Random Forest classifier pipeline
├── reports/
│   └── hotel_booking_report.html      # Print-ready HTML/PDF executive analysis report
├── src/
│   ├── data_loader.py                 # Data preprocessing and feature engineering scripts
│   └── train_model.py                 # Script to train and evaluate ML models
├── README.md                          # Project documentation
└── requirements.txt                   # Project dependencies
```

---

## 🛠️ Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/hotel-booking-analysis.git
   cd hotel-booking-analysis
   ```

2. **Create and Activate a Virtual Environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate        # On macOS/Linux
   # venv\Scripts\activate          # On Windows
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 Usage Guide

### 1. Run the Exploratory Data Analysis (EDA)

Launch Jupyter Notebook to interactively explore data distributions, correlations, and seasonality charts:

```bash
jupyter notebook notebooks/eda_hotel_demand.ipynb
```

Alternatively, run a quick summary in Python:

```python
import pandas as pd

df = pd.read_csv("data/hotel_bookings.csv")
print(df.groupby('hotel')[['lead_time', 'adr', 'is_canceled']].mean().round(2))
```

### 2. Train the Cancellation Prediction Model

Train a Random Forest classifier designed to flag high-risk cancellations:

```bash
python src/train_model.py
```

---

## 📊 Key Findings & Recommendations

1. **Implement Dynamic Deposit Policies:** Enforce non-refundable 1-night deposit rules for bookings made >60 days in advance or during peak summer months (July–August).
2. **Mitigate OTA Over-reliance:** Launch direct booking loyalty perks (free breakfast upgrades, late checkouts) to convert single-stay OTA guests into direct repeat customers.
3. **Overbooking Hedging Strategy:** Apply a 10–15% dynamic overbooking buffer for long lead-time transient bookings at City Hotels to protect against the ~50% cancellation rate in that bucket.

---

## ⚙️ Project Artifacts

* `hotel_bookings.csv`: Source dataset (Antonio, de Almeida, and Nunes, 2019).
* `eda_hotel_demand.ipynb`: Detailed EDA scripts covering feature engineering and statistical validation.
* `cancellation_prediction_model.pkl`: ML pipeline achieving an ROC-AUC of **0.88** in predicting cancellation risks.
* `hotel_summary_metrics.json`: Aggregated KPI exports for dashboarding (Tableau/Power BI).

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).