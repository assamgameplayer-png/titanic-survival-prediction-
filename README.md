# 🚢 Titanic Survival Prediction

A Random Forest classifier that predicts passenger survival on the Titanic
with **83.24% accuracy** and **0.859 ROC-AUC** on unseen data.

## 📊 Results

| Metric | Score |
|--------|-------|
| Accuracy | 0.8324 |
| Precision | 0.7746 |
| Recall | 0.7971 |
| F1-Score | 0.7857 |
| ROC-AUC | 0.8591 |
| OOB Score | 0.8272 |

## 🎯 Approach

- Missing values → median imputation per (Pclass, Sex)
- Skew correction → log1p(Fare)
- Feature engineering → Title extraction, Age/Family buckets, Pclass×Sex interaction
- Encoding → One-hot for all categorical features
- Model → RandomForest (200 trees, depth 6, balanced classes)
- Validation → Stratified 80/20 split + OOB score

## 🔑 Top Features

1. Sex (0.160)
2. Title_Mr (0.144)
3. Fare (0.080)
4. Log_Fare (0.076)
5. PCS_pclass3_male (0.070)

## 🛠️ Requirements

pip install pandas numpy scikit-learn matplotlib

## 📜 License

MIT
