# 🚦 Traffic Flow Prediction using Random Forest

## 📌 Project Overview

This project aims to **predict traffic flow** based on historical vehicle count data and temporal features such as time and day of the week. By leveraging machine learning techniques, particularly a **Random Forest Classifier**, the model categorizes traffic conditions and helps uncover patterns in urban mobility. These insights can aid city planners and traffic authorities in managing congestion, optimizing signal timings, and contributing to sustainability goals through reduced emissions and improved traffic control.

---

## 📊 Dataset Description

The dataset contains timestamped traffic flow records with the following features:

| Feature            | Description                                               |
|--------------------|-----------------------------------------------------------|
| `Time`             | Timestamp of the observation (HH:MM format)              |
| `Date`             | Date of the observation                                  |
| `Day of the week`  | Day corresponding to the observation (e.g., Monday)       |
| `CarCount`         | Number of cars observed                                   |
| `BikeCount`        | Number of bikes observed                                  |
| `BusCount`         | Number of buses observed                                  |
| `TruckCount`       | Number of trucks observed                                 |
| `Total`            | Total number of vehicles at the timestamp                 |
| `Traffic Situation`| Categorized traffic condition (e.g., Light, Moderate, Heavy) |

---

## 🛠️ Data Preprocessing

Key preprocessing steps:

- **Datetime Formatting**: Converted `Time` and `Date` columns to proper `datetime` objects.
- **Feature Engineering**: Extracted `Hour`, `Day`, and `Month` from timestamps.
- **Label Encoding**: Transformed `Day of the week` and `Traffic Situation` into numerical format.

---

## 📈 Exploratory Data Analysis (EDA)

Insights gathered from the data:

- **Peak Hours**: Morning and evening rush hours show spikes in `CarCount` and `BikeCount`.
- **Vehicle Distribution**: Cars dominate the traffic composition, followed by bikes, buses, and trucks.
- **Traffic vs Trucks**: Heavy truck traffic often corresponds with higher congestion levels.
- **Weekday Patterns**: While total traffic volume is fairly stable across the week, vehicle types show variability.

---

## 🤖 Model: Random Forest Classifier

A **Random Forest Classifier** was trained to predict `Traffic Situation` based on all other features.

### 🎯 Evaluation Metrics

- **Accuracy**: Satisfactory classification accuracy across all categories.
- **Confusion Matrix**: Provided insights into prediction accuracy per class.
- **Classification Report**: Includes **precision**, **recall**, and **F1-score** for each traffic category.

---

## 🔍 Feature Importance

The most influential features in predicting traffic conditions:

1. `CarCount`
2. `BikeCount`
3. `Day of the week`
4. `Hour of the day`

---

## 📊 Visualizations

- **Traffic Volume Over Time**: Highlights rush hours with spikes in vehicle counts.
- **Day-wise Spread**: Visualizes how each vehicle type contributes to daily traffic patterns.
- **Correlation Matrix**: 
  - Positive correlation between `CarCount` and `BikeCount`.
  - Negative correlation between `TruckCount` and `Traffic Situation`.

---

## ✅ Conclusion

This project demonstrates the potential of machine learning in urban traffic prediction. By identifying key patterns in traffic behavior:

- Authorities can better manage congestion.
- Signal timings and public transport schedules can be optimized.
- Environmental impact can be minimized through reduced idling and smoother flows.

The solution contributes to the vision of **smart cities** by using data-driven strategies to enhance urban mobility and sustainability.
