# NYC Traffic Congestion Prediction 🚖

This project explores NYC Yellow Taxi trip data and weather conditions to predict average vehicle speed during trips — used here as a proxy for traffic congestion. While the scale of Manhattan traffic is massive, this project was primarily a personal learning exercise aimed at sharpening my skills in:

>Data cleaning and preprocessing

>Feature engineering (temporal, spatial, weather)

>Exploratory data analysis (EDA)

>Regression modeling and performance tuning

The final model uses XGBoost with hyperparameter tuning to predict average speed (mph) from various features such as pickup/dropoff location, time of day, weather conditions, and trip characteristics.

This project was developed independently, from data preprocessing to modeling and evaluation, using a sample dataset (50,000 rows from January 2025). Though not meant for large-scale deployment, it demonstrates my ability to handle real-world data and build explainable models end-to-end.

## 📂 Project Structure

traffic-congestion-predictior/
├── notebooks/ # Jupyter notebooks
├── data/ # Raw and cleaned datasets
├── models/ # Saved model file (joblib)
├── Output #plots from EDA 
├── predict-function #final predictor(takes input)
├── requirements.txt
├── README.md

## ⚙️ Features

- Predicts average traffic speed from time, zone, and weather
- Uses XGBoost regression model
- Feature engineering: rush hour, zone frequency, weather handling
- Jupyter Notebook based workflow

## 🚀 How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt

##Model Info
Trained on 46904 samples of Jan 2025 taxi + hourly weather data

Model Performance Comparison
Model	        RMSE  R² Score

Linear Reg	4.630	0.369

Random Forest	3.843	0.565

XGBoost	        3.686	0.600

XGBoost (Tuned)	3.567	0.625

>The final model used is XGBoost with hyperparameter tuning, which achieved the best performance in terms of both RMSE and R².

Based on the performance XGBoost was selected for final prediction


##📁 Data Sources
NYC Yellow Taxi Trip Data: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

NOAA Weather Data: https://www.ncei.noaa.gov/data/local-climatological-data/

##References
https://pmc.ncbi.nlm.nih.gov/articles/PMC5282930/
https://www.ncei.noaa.gov/access/search/data-search/daily-summaries
https://nysfocus.com/2024/06/12/manhattan-traffic-record-congestion-pricing
