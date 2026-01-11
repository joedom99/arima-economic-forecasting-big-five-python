# Economic Forecasting using ARIMA in Python

A hands-on Python example showing how to build a **momentum-based economic forecast** using **ARIMA (AutoRegressive Integrated Moving Average)** time-series models for key macroeconomic variables.

This repository accompanies the blog post:

**[How to Create a Big-Picture Economic Forecast Using Time-Series (ARIMA) Models in Python](https://blog.marketingdatascience.ai/how-to-create-a-big-picture-economic-forecast-using-time-series-arima-models-in-python-08093acfa6f1)**

![Python](https://img.shields.io/badge/python-3.9%2B-blue)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1gBfFlwkRcwkgzYRAv91HDyRPbO_8dlfb?usp=sharing)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-notebook-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📌 Overview

While structural regression models tell us *why* spending changes, time-series models like ARIMA tell us *where* the individual economic drivers are headed based on their own internal momentum.

This project demonstrates how to:
- Use **ARIMA** to forecast the "Big Five" economic variables: GDP/Income, Inflation, Unemployment, Sentiment, and Interest Rates.
- Automate parameter tuning (p, d, q) for multiple time series using `pmdarima`.
- Bridge the gap between **statistical momentum** and **institutional consensus** (Goldman Sachs, CBO, etc.).
- Generate objective, data-driven inputs to power secondary regression models.

The goal is to move from subjective guesswork to **Scenario Intelligence**.

---

## 📊 What This Project Does

- Pulls historical macroeconomic data directly from the **Federal Reserve (FRED) API**.
- Conducts stationarity testing (ADF) and automated data transformation.
- Iteratively fits and optimizes ARIMA models for five distinct economic indicators.
- Compares pure statistical "momentum" forecasts against professional institutional consensus.
- Visualizes the "Momentum Gap" using a consolidated dashboard of fan plots.

---

## 🧠 Model Concept

Conceptually, ARIMA ignores external "causes" and focuses strictly on the pattern of the data itself. It identifies the economy's "DNA" by analyzing three components:

1. **AR (Autoregression):** The relationship between an observation and a specific number of lagged (past) observations.
2. **I (Integrated):** The differencing of raw observations to make the time series "stationary" (stable mean/variance).
3. **MA (Moving Average):** The dependency between an observation and a residual error from a moving average model applied to lagged observations.



By forecasting the "Big Five" variables independently, we create a statistically sound baseline for 2026 that can be used as a standalone forecast or as the validated input for more complex structural models.

---

## 📁 Repository Files

* `economic_forecast_using_ARIMA_ver3.ipynb`: The main notebook containing the data pipeline, ARIMA optimization, and visualization dashboard.
* `economic_data_snapshot.csv`: The "Time Capsule" dataset used for the analysis in the blog post.
* `README.md`
* `LICENSE`

---

## 👨🏻‍💻 Reproducibility & Data Integrity

This analysis was originally generated on **January 10, 2026.**

Because this project relies on live economic data from the Federal Reserve (FRED), results generated in the future may differ slightly due to official government data revisions and updates.

* **Live Mode (Default):** The notebook is set to query the FRED API for the most current data.
* **Static Mode (Reproducible):** To reproduce the exact results and the "Momentum Gap" dashboard found in the article, load the provided `economic_data_snapshot.csv` file.

---

## ▶️ How to Run the Notebook

### Option 1: Run Locally
1. Clone the repository using your preferred Git client.
2. Install the necessary Python dependencies: pandas, matplotlib, statsmodels, pmdarima, and fredapi.
3. Launch your Jupyter environment.
4. Open the `economic_forecast_using_ARIMA_ver3.ipynb` file.

### Option 2: Run in Google Colab
Click the "Open in Colab" badge at the top of this README to run the code in a cloud environment with no local setup required.

---

## 🔭 Related Projects

This project is the second part of a series on DIY econometrics. If you are interested in how these ARIMA forecasts can be used to predict consumer behavior, check out the first project:

* **[Economic Forecasting with Multiple Regression in Python](https://github.com/joedom99/basic-economic-forecasting-multiple-regression-python)**

---

## 📜 License

MIT License. See `LICENSE` for more details.
