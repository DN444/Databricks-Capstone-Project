# Databricks-Capstone-Project-2

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
- **Performance:** 
   Log RMSE:     0.536
   PM2.5 RMSE:   56.4 µg/m³
   PM2.5 MAE:    28.4 µg/m³
   PM2.5 MAPE:   49.6%
   R² (log):     0.682
- **Registry:** `workspace.air_quality.air_quality_forecast_micro`
- **Endpoint:** `air-quality-dashboard`

- Pollution alerts
- Dataset statistics

## 🚀 Automated Pipeline
🔗 [Databricks Job](https://dbc-d3f5a3ae-d5c8.cloud.databricks.com/jobs/373321264172806?o=7474659613009107)
