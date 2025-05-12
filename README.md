# Stress Detection Using ECG (WESAD Dataset)

This project applies machine learning techniques to classify stress levels based on ECG signals from the WESAD dataset.

## Dataset
- **WESAD**: A public dataset including physiological and motion signals from wearable devices.
- Focused only on **ECG signal** from the **RespiBAN chest-worn device**.
- Binary classification: `0 = Not Stressed`, `1 = Stressed`.

## Methodology
- Fixed windowing: 5-minute segments (300 seconds) with 50% overlap.
- Sampling frequency: 700 Hz.
- Extracted features:
  - Mean, Std Dev, Min, Max
  - Skewness, Kurtosis
- Cleaned data using median imputation and normalized with `StandardScaler`.

## Models Used
- `XGBClassifier` (XGBoost)
- `BaggingClassifier` with Decision Tree

| Model   | Accuracy |
|---------|----------|
| XGBoost | 92%      |
| Bagging | 89%      |

## Project Structure

```
notebooks/           → Jupyter Notebook with full processing and modeling
models/              → Saved trained XGBoost & Bagging model
report/              → Full report explaining project
requirements.txt     → Python libraries needed
README.md            → Project overview and instructions
```

## 📄 References
- [WESAD Dataset Paper](https://archive.ics.uci.edu/ml/datasets/WESAD+%28Wearable+Stress+and+Affect+Detection%29)
- Research Paper: [“From lab to real-life: A three-stage validation of wearable technology for stress monitoring 2025”](https://doi.org/10.1016/j.mex.2025.103205)
