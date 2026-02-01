# Databricks-Capstone-Project

# 🌡️ Air Quality Prediction Pipeline

## 🏗️ Architecture (Medallion)


## 📊 Tables Created
| Layer | Table | Purpose | Rows |
|-------|-------|---------|------|
| Bronze | `workspace.air_quality.bronze_air_quality` | Raw normalized data | 1.6M |
| Silver | `workspace.air_quality.silver_air_quality` | Clean types + dates | 15K+ |
| Gold | `workspace.air_quality.gold_daily_aqi` | Daily aggregates + AQI | 2K+ |

## 🔮 ML Model
- **Algorithm:** Random Forest Regressor
- **Features:** PM2.5 lag, temp, humidity, wind, day_of_week, month
- **Performance:** RMSE: 16.4, MAE: 11.9, R²: 0.854
- **Registry:** `workspace.air_quality.air_quality_forecast_micro`
- **Endpoint:** `air-quality-dashboard`

## 📈 Production Dashboard
🔗 [Live Dashboard](https://dbc-d3f5a3ae-d5c8.cloud.databricks.com/dashboardsv3/01f0ff7a538110dc973b2960a6daf4da/published?o=7474659613009107)
- Live PM2.5 trends by city
- AQI status (🟢🟡🟠)
- Pollution alerts
- Dataset statistics

## 🚀 Automated Pipeline
🔗 [Databricks Job](https://dbc-d3f5a3ae-d5c8.cloud.databricks.com/jobs/373321264172806?o=7474659613009107)
