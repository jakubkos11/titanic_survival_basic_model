# Titanic Survival — Basic Prediction Model

This repository contains a **baseline survival prediction model for Titanic passengers**, built entirely without machine learning.  
It uses manually calculated group survival probabilities combined with feature importance weights to estimate survival likelihood.

This is **Version 1** of a planned two-part project. The current version offers a basic, interpretable approach to prediction  
and will later be expanded with numerical features and machine learning techniques.

---

## ⚙️ Method Overview

1. **Group Statistics**: Computes average survival rates for each category (e.g. `Sex`, `Pclass`, etc.)
2. **Feature Weighting**: Calculates how strongly each feature influences survival based on rate spread
3. **Prediction Scoring**: Combines weighted probabilities into a survival score
4. **Thresholding**: Applies the optimal classification threshold learned from training data

---

## 📊 Model Accuracy

- **Training Accuracy**: ~79.91%  
- **Kaggle Leaderboard (Public Test Set)**: ~76.55%

Accuracy is based on predicting survival labels (`0` or `1`) using calculated scores and threshold optimization.

---

## 📁 Files

| File                  | Description                                                    |
|-----------------------|----------------------------------------------------------------|
| `titanic_baseline.py` | Core script implementing the model logic and visualizations    |
| `submission.csv`      | Predicted survival labels for test passengers (for Kaggle)     |
| `requirements.txt`    | List of required Python libraries (`pandas`, `numpy`, etc.)    |

---

## 🔧 How to Run

1. Place Titanic dataset CSV files inside `/kaggle/input/titanic/`
2. Run the script:

```bash
python titanic_baseline.py
