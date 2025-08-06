# 🛺 Uber NYC Data Analysis & Trip Prediction

This project analyzes Uber pickup data in NYC from April 2014 to June 2015, obtained via FOIL requests by FiveThirtyEight. The goal is to perform Exploratory Data Analysis (EDA), engineer time-based features, and build a regression model to predict the number of trips.

---

## 📁 Dataset Overview

The data was obtained via FOIL requests submitted by FiveThirtyEight to the NYC Taxi & Limousine Commission (TLC). It includes:

* Uber pickup data
* Dispatching & affiliated base numbers
* Trip volume statistics
* Location and time of pickups

**Key Files:**

* `uber-raw-data-apr14.csv` to `uber-raw-data-sep14.csv`
* `uber-raw-data-janjune-15.csv`
* `taxi-zone-lookup.csv`
* `other-FHV-data-jan-aug-2015.csv`

---

## 📌 Project Goals

* Perform Exploratory Data Analysis (EDA) to discover patterns in Uber usage.
* Engineer time-based features to enhance modeling.
* Build a regression model to predict the number of trips based on:
  * Date
  * Day of the week
  * Month
  * Week number
  * Active vehicles

---

## 🛠️ Project Steps

### 1. Data Preprocessing

* Merged and cleaned monthly datasets
* Checked for nulls and missing values
* Renamed columns for consistency
* Converted date strings to `datetime` objects

### 2. Feature Engineering

* Extracted new features from the date column:
  * `day`, `month`, `weekday`, `week`

### 3. Exploratory Data Analysis (EDA)

* Analyzed trip distributions over time
* Visualized activity by dispatch base
* Identified busiest days and trends using bar plots and line charts

### 4. Model Building (Linear Regression)

* Used `scikit-learn` to build a regression model with features:

```python
features = ['day', 'month', 'weekday', 'week', 'active_vehicles']

