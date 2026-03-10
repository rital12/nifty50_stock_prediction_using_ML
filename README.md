# 📈 Nifty 50 Market Prediction using Machine Learning

## 📌 Project Overview

This project focuses on predicting the **future direction of the Nifty 50 index** using historical stock market data and machine learning techniques.

The project uses **Python, Pandas, and Scikit-Learn** to collect financial data, engineer predictive features, train a machine learning model, and evaluate its performance.

The goal is to predict whether the **Nifty 50 closing price will increase or decrease the next trading day.**

---

# 🎯 Objective

The objective of this project is to:

* Collect historical **Nifty 50 index data**
* Perform **data preprocessing and feature engineering**
* Build a **machine learning classification model**
* Predict **next-day market direction**
* Evaluate prediction accuracy using precision score

---

# 📊 Dataset

The dataset is obtained directly from **Yahoo Finance** using the `yfinance` library.

**Index Used**

* Nifty 50 (`^NSEI`)

The dataset contains historical market data including:

* Open price
* High price
* Low price
* Close price
* Volume

---

# 🧠 Feature Engineering

Several features were created to improve model performance.

### Target Variable

```python
Target = (Tomorrow > Close)
```

* `1` → Market expected to go **up**
* `0` → Market expected to go **down**

### Additional Features

Rolling averages were used to capture market trends:

* 2-day trend
* 5-day trend
* 60-day trend
* 250-day trend
* 1000-day trend

These indicators help the model identify **short-term and long-term market patterns.**

---

# 🤖 Machine Learning Model

The project uses:

**Random Forest Classifier**

Key parameters:

* `n_estimators = 100`
* `min_samples_split = 100`
* `random_state = 1`

Random Forest is chosen because it:

* Handles nonlinear relationships well
* Works effectively with financial datasets
* Reduces overfitting compared to single decision trees

---

# 🔄 Backtesting Strategy

A **backtesting function** is implemented to simulate real-world prediction scenarios.

The model is repeatedly trained on past data and tested on future unseen data.

This approach helps evaluate how the model would perform in **actual trading conditions**.

---

# 📈 Model Evaluation

The model performance is evaluated using:

**Precision Score**

Precision measures how many predicted upward movements were actually correct.

```python
precision_score(actual_values, predicted_values)
```

---

# 🛠 Technologies Used

| Tool             | Purpose                         |
| ---------------- | ------------------------------- |
| Python           | Programming language            |
| Jupyter Notebook | Development environment         |
| Pandas           | Data analysis and preprocessing |
| yfinance         | Financial data collection       |
| Scikit-Learn     | Machine learning library        |
| Random Forest    | Prediction model                |

---

# ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/nifty50-market-prediction.git
cd nifty50-market-prediction
```

Install required libraries:

```bash
pip install pandas numpy yfinance scikit-learn matplotlib
```

---

# ▶️ How to Run the Project

1. Open the notebook:

```
nifty50_prediction.ipynb
```

2. Run all cells sequentially in **Jupyter Notebook**.

The notebook will:

* Download historical Nifty 50 data
* Prepare the dataset
* Train the machine learning model
* Perform backtesting
* Evaluate prediction performance

---

# 📂 Project Structure

```
nifty50-market-prediction
│
├── nifty50_prediction.ipynb
├── nifty50_maxdata.csv
└── README.md
```

---

# 🚀 Future Improvements

Possible enhancements for this project:

* Add **technical indicators** (RSI, MACD, Bollinger Bands)
* Use **LSTM deep learning models**
* Train models on **multiple Nifty stocks**
* Perform **hyperparameter tuning**
* Build a **stock prediction dashboard**

---

# 👨‍💻 Author

**Rital Burile**
MBA – Data Science & Business Analytics

This project demonstrates the use of **machine learning techniques for financial market prediction** and is part of my learning journey in **data science and financial analytics**.
