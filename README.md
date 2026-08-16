# 🌱 AgriSense – Smart Agriculture Platform

AgriSense is a smart agriculture web platform built with Django to help farmers make informed decisions using soil, weather, crop, and market information. It combines machine learning-based crop recommendations with soil analysis, fertilizer guidance, irrigation insights, government schemes, market prices, and agricultural analytics in one platform.

## 🚜 Key Features

### 🌾 Crop Recommendation
- Uses a Machine Learning model based on Random Forest.
- Analyzes:
  - Nitrogen (N)
  - Phosphorus (P)
  - Potassium (K)
  - Temperature
  - Humidity
  - Soil pH
  - Rainfall
- Recommends suitable crops based on the given conditions.

### 🧪 Soil & NPK Analysis
- Analyzes soil pH and NPK values.
- Identifies whether soil is acidic, neutral, or alkaline.
- Provides information about nitrogen, phosphorus, and potassium levels.
- Gives actionable soil health recommendations.

### 💊 Fertilizer Recommendations
- Provides fertilizer suggestions based on soil nutrient levels.
- Considers pH, temperature, humidity, and rainfall.
- Provides recommendations for improving soil health and nutrient availability.

### 🌦️ Weather Information
- Provides weather information based on the selected location.
- Uses weather conditions to provide agricultural insights.
- Calculates estimated soil moisture using temperature, humidity, wind, and weather conditions.

### 💧 Irrigation Support
- Provides irrigation-related information based on soil moisture and environmental conditions.
- Helps farmers understand when irrigation may be required.

### 💰 Market Prices
- Stores and displays crop market prices.
- Provides crop price information based on location/state.
- Uses a database to manage crop price records.

### 🏛️ Government Schemes
- Provides information about agricultural government schemes.
- Helps farmers discover available government support and benefits.

### 📊 Agricultural Analytics
- Tracks soil moisture, temperature, and humidity data.
- Provides hourly analytics for agricultural monitoring.
- Supports visualization and analysis of environmental conditions.

### 👨‍🌾 User Authentication
- Farmer registration and login.
- Custom user model.
- Separate admin and farmer access.
- Secure session-based authentication using Django.

### 👨‍💼 Admin Portal
- Dedicated administrator functionality.
- User and crop-related data management.
- Dashboard statistics and analytics.

---

## 🤖 Machine Learning

AgriSense uses a **Random Forest Classifier** for crop recommendation.

### Input Parameters

| Parameter | Description |
|-----------|-------------|
| N | Nitrogen level |
| P | Phosphorus level |
| K | Potassium level |
| Temperature | Environmental temperature |
| Humidity | Relative humidity |
| pH | Soil acidity/alkalinity |
| Rainfall | Rainfall level |

The trained model is saved using `joblib` and loaded by the Django application for predictions.

---

## 🛠️ Technologies Used

### Backend
- Python
- Django 5.2.7
- SQLite

### Machine Learning
- Scikit-learn
- Random Forest Classifier
- Pandas
- Joblib

### Frontend
- HTML
- CSS
- JavaScript
- Django Templates

### APIs
- OpenWeather API for weather information

### Data
- Crop recommendation dataset
- Crop market price dataset
- Agricultural analytics data

---

## 📂 Project Structure

```text
AgriSense/
└── new_project/
    ├── manage.py
    ├── db.sqlite3
    ├── load_analytics.py
    ├── load_crop_prices.py
    │
    ├── model/
    │   └── model.pkl
    │
    ├── new_app/
    │   ├── dataset/
    │   │   ├── Crop_recommendation (1).csv
    │   │   └── dataset (1).csv
    │   │
    │   ├── migrations/
    │   ├── static/
    │   ├── templates/
    │   │   ├── farmer_home.html
    │   │   ├── gov_schemes.html
    │   │   ├── market_price.html
    │   │   ├── irrigation.html
    │   │   ├── weather.html
    │   │   ├── analytics.html
    │   │   ├── login.html
    │   │   └── register.html
    │   │
    │   ├── models.py
    │   ├── views.py
    │   ├── urls.py
    │   └── train_model.py
    │
    └── new_project/
        ├── settings.py
        ├── urls.py
        ├── asgi.py
        └── wsgi.py
