# Food Delivery Time Analysis

## Project Overview
Exploratory data analysis of about 45,000 food delivery orders to find what causes delivery delays and to recommend ways to reduce delivery time.

## Dataset
Food Delivery Dataset from Kaggle (train.csv). It includes rider age and ratings, restaurant and delivery locations, order time, weather, traffic, vehicle type, festival flag, city type and time taken.
https://www.kaggle.com/datasets/gauravmalik26/food-delivery-dataset?select=train.csv

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Steps
1. Data Cleaning: fixed "NaN" text, filled missing values (median for numbers, mode for categories), cleaned text columns
2. Data Transformation: converted dates and times to datetime
3. Feature Engineering: distance in km (Haversine formula), order hour, weekday, prep time, peak hour, late-delivery flag
4. Analysis: average delivery time by traffic, weather, vehicle, festival, city and multiple deliveries
5. Visualization: histogram, box plot, bar chart and correlation heatmap

## Key Insights
- Average delivery time is 26.3 minutes, and 29.8% of orders take more than 30 minutes
- Multiple deliveries have the biggest effect: 22.9 min with no other orders vs 47.8 min with 3
- Festival days are about 20 minutes slower (45.5 vs 25.9 min)
- Jam traffic averages 31.2 min vs 21.3 min in low traffic
- Cloudy and Fog weather add about 7 minutes compared with Sunny

## Recommendations
- Add extra riders and incentives on festival days
- Cap riders at 1 extra order at a time
- Add rider incentives during Jam traffic and in Fog or Cloudy weather

## How to Run
1. Download train.csv from Kaggle and place it in the same folder
2. Install: pip install pandas numpy matplotlib seaborn
3. Open food_delivery_analysis.ipynb and run all cells
