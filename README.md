# Hotel Booking Cancellation Prediction


## Main Notebook

[Open Notebook](./Hotel-Booking-Cancellation-Prediction_Fin.ipynb)
---

## Project Overview

This project builds machine learning models to predict whether a hotel booking will be canceled (`is_canceled`).

Hotel booking cancellations create major business problems because they affect revenue, occupancy planning, staffing, and operational efficiency. The notebook explores the data, identifies important cancellation drivers, and compares multiple classification models.

---
## Data:

119,390 hotel records where each record represents a single booking: hotel_bookings.csvDownload hotel_bookings.csv
Target Variable: ‘is_canceled’
Detailed descriptions of all variables can be found at https://www.kaggle.com/sanjana08/hotel-booking-cancellation-prediction/dataLinks to an external site.
## Goal: Classify a dataset using decision trees, explore pruning skills, and compare it with other models like KNN and logistic regression.

## Problem Statement

Hotel booking cancellations significantly impact:
- lost revenue from last-minute cancellations
- inefficient room allocation
- increased uncertainty in forecasting and operations

The goal of this project is to classify whether a booking will be canceled so hotels can make better business decisions in advance.

---

## Key Stakeholders

- **Revenue Managers** — pricing and forecasting
- **Operations Team** — staffing and room allocation
- **Marketing Team** — targeted promotions for at-risk customers

---

## Dataset Information

The dataset contains hotel reservation records with booking, customer, and stay-related features.

### Target Variable
- `is_canceled`

### Important Features
- `lead_time`
- `previous_cancellations`
- `booking_changes`
- `adr`
- `deposit_type`
- `customer_type`
- `market_segment`
- `required_car_parking_spaces`
- `total_of_special_requests`

---

## Data Cleaning and Exploratory Data Analysis

The notebook includes:
- missing value analysis
- correlation analysis
- target distribution analysis
- boxplots for lead time and ADR
- deposit type and customer type comparisons
- feature relevance discussion

### Key EDA Findings
- The dataset is imbalanced, with more non-canceled bookings than canceled bookings
- Longer `lead_time` is associated with higher cancellation risk
- `deposit_type` is strongly related to cancellations
- `customer_type` helps explain cancellation behavior
- `previous_cancellations` is a useful behavioral predictor

---

## Modeling Approach

The notebook compares three classification models:

- **Decision Tree** with pre-pruning
- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**

The Decision Tree model is also tuned using **Grid Search** with:
- `max_depth`
- `max_leaf_nodes`

---

## Selected Features Model

A smaller feature set was tested to improve interpretability.

Selected features included:
- `lead_time`
- `previous_cancellations`
- `booking_changes`
- `adr`
- `deposit_type`
- `customer_type`
- `market_segment`

This model showed high precision but lower recall, meaning it identified cancellations well when it predicted them, but it missed many actual cancellations.

---

## Model Performance Summary

### Decision Tree
- Accuracy: ~0.76
- Recall: ~0.38
- Precision: ~0.99

### KNN
- Accuracy: ~0.79
- Recall: ~0.66
- Precision: ~0.75

### Logistic Regression
- Accuracy: ~0.77
- Recall: ~0.45
- Precision: ~0.88

---

## Final Model Selection

The final model selected for this project is **KNN** because it achieved the highest recall.

### Why Recall Matters Most
For hotel cancellations, a false negative means a canceled booking is missed. That can cause:
- lost revenue
- poor room utilization
- staffing inefficiency

Because of this, recall is more important than accuracy for this problem.

---

## Business Insights

The model suggests that cancellation risk is influenced by:
- long lead times
- no deposit bookings
- transient customer behavior
- previous cancellation history

### Recommended Actions
- strengthen deposit policies
- flag high-risk bookings early
- target high-risk customers with reminders or incentives
- use predicted cancellation risk to improve overbooking and staffing decisions

---

## Conclusion

This project demonstrates how machine learning can help hotels predict cancellations and make more informed operational decisions.

The analysis shows that cancellation behavior is predictable to a useful degree, especially when focusing on variables like lead time, deposit type, and customer type.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---



---

## Author

Tanishtha Papadkar
