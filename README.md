Mantap 👍 Kalau begitu saya buatkan **README GitHub versi lengkap** dengan tambahan struktur folder + instruksi penggunaan.

---

# ⚽ English Premier League Match Prediction Analysis

## 📌 Project Overview

This project predicts match outcomes in the **English Premier League (EPL)** using **machine learning**.

Football results are often uncertain, with baseline prediction accuracy close to random guessing (\~50%). This project builds a predictive model that achieves **≥60% accuracy** and provides **insights into key factors influencing match results**.

**Business Relevance:**

* 📈 **Sportsbook** – reduce financial risks and optimize odds.
* ⚽ **Football Clubs** – support strategic planning and performance evaluation.
* 📱 **Fans & Fantasy Sports** – increase engagement through predictive insights.

---

## 📂 Dataset

* **Source:** English Premier League matches (2020–2023).
* **Size:** 1,140 rows × 40 columns.
* **Features:**

  * Match Info → Date, Home Team, Away Team, Attendance.
  * Performance Metrics → Goals, Shots, Shots on Target, Possession, Passes, Corners, Fouls.
  * Target → Match outcome (`Home Win`, `Away Win`, `Draw`).

---

## 🛠️ Data Preprocessing

* ✅ No missing values or duplicates.
* 🔄 Converted `date` column into datetime format.
* 🎯 Feature engineering: goal difference, shot difference, possession ratio.

---

## 📊 Exploratory Data Analysis (EDA)

* Attendance → Most matches <10K, big matches >50K.
* Goals → 0–2 goals common, home teams slightly more productive (*home advantage*).
* Correlation → Shots & shots on target strongly linked to goals; possession more related to passing volume.
* Class distribution →

  * Home Win: \~44%
  * Away Win: \~34%
  * Draw: \~22% (imbalanced).

---

## 🤖 Machine Learning Models

* **Baseline:** Multinomial Logistic Regression.
* **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score, ROC-AUC.

### Key Results

* **Home Win:** Precision 70%, Recall 75% (best).
* **Away Win:** Precision & Recall \~65%.
* **Draw:** Precision 20%, Recall <10% (weak due to imbalance).
* **ROC-AUC:**

  * Away Win: 0.81
  * Draw: 0.65
  * Home Win: 0.86

---

## 💡 Insights & Recommendations

* **Sportsbook & Betting:**

  * Optimize odds for Home/Away wins (higher reliability).
  * Use conservative odds for draws (lower reliability).

* **Sponsorship & Marketing:**

  * Highlight home advantage in campaigns.

* **Fan Engagement:**

  * Publish model predictions as match previews.
  * Frame “draw” as unpredictable to boost excitement.

---

## 🚀 Future Development

* Add tactical variables (fouls, cards, expected goals).
* Try advanced models (Random Forest, XGBoost, Neural Networks).
* Deploy as dashboard or API for live predictions.

---

## 📂 Repository Structure

```
📦 EPL-Match-Prediction
 ┣ 📂 data
 ┃ ┣ epl_matches.csv         # raw dataset (not included in repo, link in notebook)
 ┣ 📂 notebooks
 ┃ ┣ 01_data_preprocessing.ipynb
 ┃ ┣ 02_eda_visualization.ipynb
 ┃ ┣ 03_model_training.ipynb
 ┃ ┣ 04_evaluation.ipynb
 ┣ 📂 models
 ┃ ┣ logistic_regression.pkl
 ┃ ┣ random_forest.pkl
 ┣ 📂 reports
 ┃ ┣ figures/                # charts and plots from EDA and modeling
 ┃ ┗ final_report.pdf
 ┣ requirements.txt
 ┣ README.md
```

---

## ⚙️ Installation & Usage

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/epl-match-prediction.git
cd epl-match-prediction
```

### 2. Create Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Jupyter Notebook

```bash
jupyter notebook notebooks/01_data_preprocessing.ipynb
```

---

## 📦 Requirements

Example `requirements.txt`:

```
pandas  
numpy  
scikit-learn  
matplotlib  
seaborn  
jupyter  
```
