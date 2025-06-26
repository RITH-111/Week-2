

 Water Quality Prediction Using Machine Learning

This project focuses on predicting key water quality pollutants (`O2`, `NO3`, `NO2`, `SO4`, `PO4`, `CL`) using a multi-output regression model. It performs exploratory data analysis (EDA), data preprocessing, and trains a `RandomForestRegressor` wrapped in a `MultiOutputRegressor`.

---

📁 Dataset

* **File**: `PB_All_2000_2021.csv`
* **Format**: Semicolon (`;`) separated
* **Features**:

  * Date of observation
  * Measurement site ID
  * Concentration levels of various pollutants

---

### ⚙️ Features

* Data cleaning (duplicate removal, outlier detection using Z-scores, and missing value imputation)
* Feature engineering (year, month extraction from date)
* Correlation analysis and pollutant distribution visualization
* One-hot encoding of categorical features (`id`)
* Standardization using `StandardScaler`
* Model training using `MultiOutputRegressor(RandomForestRegressor)`
* Evaluation using `R² score` and `RMSE`
* Model persistence using `joblib`

---

### 📈 Model Evaluation

* Individual R² and RMSE scores are printed for each pollutant
* An overall R² score is calculated as the average across all pollutant predictions

---

### 💾 Output

* **Trained Model File**:https://drive.google.com/file/d/1OsJIIelxoPBSQX1JwTePp1OooE5uWRa9/view?usp=sharing

---

### 🚀 Usage

```bash
pip install -r requirements.txt
```

```python
from joblib import load

# Load model
model = load('water_quality_model.joblib')

# Predict on new data
y_pred = model.predict(X_new)
```

---

### 🧰 Requirements (add to `requirements.txt`)

```
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

--
