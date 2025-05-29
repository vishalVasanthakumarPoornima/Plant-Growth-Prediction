# 🌱 Plant Growth Prediction

This project uses machine learning models to predict whether a plant reaches its growth milestone based on environmental and agricultural factors such as sunlight, temperature, soil type, water frequency, and fertilizer type. We apply both classification and regression approaches to explore model performance.

---

## 📁 Dataset

The dataset contains the following features:

- `Soil_Type`: Categorical (e.g., loam, sandy, clay)
- `Sunlight_Hours`: Numeric (hours of sunlight per day)
- `Water_Frequency`: Categorical (daily, weekly, bi-weekly)
- `Fertilizer_Type`: Categorical (organic, chemical, none)
- `Temperature`: Numeric (°C)
- `Humidity`: Numeric (%)
- `Growth_Milestone`: Target (0 = No, 1 = Yes)

---

## 🧪 Models Used

- **Linear Regression**
  - Used to test continuous prediction but limited due to the binary nature of the target.
- **Logistic Regression**
  - Applied for binary classification of `Growth_Milestone`.
- **Random Forest Classifier**
  - Ensemble model used with hyperparameter tuning via `GridSearchCV`.
  - Provided the best balance between performance and generalization.

---

## ⚙️ Preprocessing Steps

- One-hot encoding of categorical variables using `pd.get_dummies()`.
- Feature engineering with polynomial and interaction terms.
- Boxplot and correlation matrix used to inspect feature behavior and relationships.
- Feature scaling with `StandardScaler`.

---

## 🔍 Model Evaluation

### Final Model: Random Forest (after GridSearchCV)

- **Best Parameters**:
  - `max_depth`: None
  - `min_samples_split`: 2
  - `min_samples_leaf`: 4
  - `n_estimators`: 50

- **Cross-Validation Accuracy**: ~60.3%
- **Test Accuracy**: ~71.8%

### Baseline Model (Default Random Forest)

- **Test Accuracy**: ~79.5%
- *Note: While accuracy is higher, this model lacks validation through cross-validation and may overfit.*

---

## 📈 Metrics

- Accuracy
- Precision, Recall, F1-Score (classification report)
- Confusion Matrix
- Correlation Matrix

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/plant-growth-prediction.git
   cd plant-growth-prediction
