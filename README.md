# 🇱🇰 Sri Lanka Tourism Forecast (2023–2025)

This project uses [Facebook Prophet](https://facebook.github.io/prophet/) to forecast daily tourist arrivals in Sri Lanka, using time series data from 2023 to mid-2025.

## 📊 Project Overview

We explore two forecasting models:

1. **Standard Prophet Model**  
2. **Prophet Model with Month as a Regressor** (One-hot encoded)

## 🗂 Dataset

- Contains daily tourist arrivals from `2023-01-01` to `2025-06-30`
- Columns:
  - `ds`: Date
  - `y`: Number of tourists

## 🧠 Modeling Approach

- Data split:
  - `2023–2024` for training
  - `2025` for testing
- Model 1: Basic Prophet
- Model 2: Prophet + month (seasonal) regressors
- One-hot encoded month used as additional features in the second model
- Evaluated using MAE and RMSE

## 📈 Visualization

Final plots include:
- **Actual tourist arrivals (2023–2025)** shown as a continuous black line
- **Forecasts for 2025** shown as colored markers (not lines) for:
  - Standard Prophet
  - Prophet with month regressors

## 🛠️ Tools & Libraries

- Python
- Google Colab
- Prophet
- pandas, matplotlib, scikit-learn

## 🧪 Evaluation Metrics

| Model                        | MAE     | RMSE    |
|-----------------------------|---------|---------|
| Standard Prophet            | 1107.42 | 1277.87 |
| Prophet + Month Regressor   |  746.17 |  889.97 |

✅ The model using month as a regressor significantly outperformed the standard Prophet model.

## 📌 How to Run

1. Open the Colab notebook
2. Upload your CSV file with `ds` and `y` columns
3. Run all cells to build models and view results

---

## 🧾 License

This project is licensed under the [MIT License](LICENSE).
