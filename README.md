# Hotel Booking Demand & Cancellation Analysis

A data science and business analytics project performing exploratory data analysis (EDA) and operational breakdown on a hotel booking dataset comprising **119,390 records** across **City Hotel** and **Resort Hotel** properties.

---

## 📌 Project Overview

This repository provides an end-to-end analysis of hotel booking demand, revenue metrics (ADR), cancellation dynamics, guest demographics, and distribution channel performance. The goal of this project is to uncover operational bottlenecks, evaluate revenue risk factors, and provide actionable business recommendations to optimize hotel occupancy and revenue management.

---

## 🛠️ Key Technologies & Libraries

- **Language**: Python 3.8+
- **Data Manipulation**: `pandas`, `numpy`
- **Data Visualization**: `matplotlib`, `seaborn`
- **Development Environment**: Jupyter Notebook / JupyterLab

---

## 📊 Dataset Summary

The dataset covers booking records spanning from **July 2015 to August 2017**:
- **Total Records**: 119,390 bookings
- **City Hotel Share**: 79,330 bookings (66.4%)
- **Resort Hotel Share**: 40,060 bookings (33.6%)
- **Overall Cancellation Rate**: 37.0%
- **Average Lead Time**: 104 days
- **Average Daily Rate (ADR)**: €101.83

---

## 🔑 Key Findings & Business Insights

1. **Lead Time Cancellation Risk**: Bookings made with lead times exceeding **60 days** face cancellation rates above **45%**, climbing to **54%** for bookings made 120+ days in advance.
2. **Channel Performance**: Online Travel Agents (OTAs) generate **47.1%** of total bookings but exhibit high cancellation rates (**41.1%**). Direct bookings carry the lowest cancellation rate (**15.3%**).
3. **Resort Seasonality**: Resort Hotel ADR experiences extreme seasonal variance, dropping from **€181 in August** down to **€48 in January**.
4. **Loyalty Opportunity**: Repeat guests represent only **3.2%** of total stays, highlighting a major opportunity for post-stay retention campaigns.

---

## 💡 Strategic Recommendations

- **Overbooking Strategy**: Implement dynamic overbooking limits (10–15%) for OTA channels with lead times >90 days to offset high cancellation rates.
- **Deposit Policy Updates**: Require non-refundable deposits for long lead-time reservations (>60 days) and peak-season bookings.
- **Direct Booking Incentives**: Offer immediate perks (e.g., free room upgrades, complimentary breakfast) for direct bookings to reduce reliance on commission-heavy OTAs.
- **Off-Peak Monetization**: Target remote workers, long-term stays, and regional corporate retreats to balance Resort Hotel revenue during Q1 and Q4.

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/hotel-booking-analysis.git](https://github.com/your-username/hotel-booking-analysis.git)
cd hotel-booking-analysis
