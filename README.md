Sales Forecast: Unveiling the Future with Facebook Prophet
Project Overview
In today’s competitive retail landscape, accurate sales forecasting is crucial for optimizing inventory, staffing, and marketing strategies. This project leverages Facebook Prophet, an open-source time series forecasting tool, to predict future sales for a chain of approximately 1,100 stores based on historical transactional data. By incorporating seasonality, holidays, and store-specific factors, the model provides actionable insights to drive data-driven decision-making, making it a valuable addition to a Business Intelligence (BI) portfolio.
The dataset includes two main components:

Sales Data: 1 million transactions with features like sales, customers, promotions, and holidays.
Store Information: Details for 1,100 stores, including store type, assortment, and competition distance.

Objectives

Analyze historical sales data to identify trends, seasonality, and the impact of promotions and holidays.
Clean and preprocess data to ensure quality inputs for forecasting.
Build a robust forecasting model using Facebook Prophet to predict sales for individual stores.
Incorporate state and school holidays to enhance prediction accuracy.
Visualize insights to support strategic planning for inventory, staffing, and promotions.

Dataset Description
Sales Data

Rows: 1 million transactions (2013–2015).
Key Features:
store: Store ID (1,100 unique stores).
date: Transaction date.
sales: Daily sales in euros (target variable).
customers: Number of customers per day.
open: Binary (1 = open, 0 = closed).
promo: Binary (1 = promotion active, 0 = none).
state_holiday: Categorical (a = public, b = Easter, c = Christmas, 0 = none).
school_holiday: Binary (1 = school holiday, 0 = none).
day_of_week, day, month, year: Extracted from date.



Store Information

Rows: 1,115 stores.
Key Features:
store_type: Categorical (a, b, c, d; e.g., size or location).
assortment: Categorical (a = basic, b = extra, c = extended).
competition_distance: Distance to nearest competitor (meters).
competition_open_since_month/year: When competitor opened.
promo2: Binary (1 = participates in secondary promotion, 0 = none).
promo2_since_week/year, promo_interval: Details of secondary promotions.



Methodology
The project follows a structured pipeline to ensure robust analysis and forecasting:

Data Import and Libraries:

Used Python libraries: pandas, numpy, seaborn, matplotlib, and prophet.
Loaded datasets from CSV files stored in Google Drive.


Exploratory Data Analysis (EDA):

Visualized missing data with Seaborn heatmaps, confirming no missing values in sales data but identifying gaps in store data (e.g., 3 missing competition_distance values, 354 missing competition_open_since_month values).
Plotted histograms to analyze distributions (e.g., average sales €5,700, customers 600 per day).
Created line plots for average sales and customers by month, day, and day of the week, revealing peaks in December (holidays) and Sundays.
Used bar and violin plots to confirm promotions increase sales and customer visits.


Data Cleaning:

Filled missing competition_distance values with the mean (5,430 meters) to preserve distribution.
Set missing `promo2_since_week


