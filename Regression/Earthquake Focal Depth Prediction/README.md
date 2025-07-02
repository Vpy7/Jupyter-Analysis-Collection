# 🌍 Earthquake Focal Depth Prediction

## 📌 Introduction
This project aims to apply machine learning techniques to predict the **focal depth** of earthquakes based on geographic and magnitude-related features. We use the **Quakes** dataset, a real-world collection of seismic events, to build and evaluate regression models that help uncover patterns influencing earthquake depth.

## 🗂️ Dataset Description
The dataset originates from the book *Smoothing Methods in Statistics* by J.S. Simonoff (1996) and is publicly available on Kaggle. It contains information on seismic events with the following variables:

| Variable      | Description                                      |
|---------------|--------------------------------------------------|
| `latitude`    | Latitude of the earthquake epicenter             |
| `longitude`   | Longitude of the earthquake epicenter            |
| `richter`     | Earthquake magnitude on the Richter scale        |
| `focal_depth` | Depth of the earthquake focus (target variable)  |

- **File size**: ~44 KB  
- **Format**: CSV  
- **License**: CC0 (Public Domain)

## 🎯 Project Objective
Develop a predictive model to estimate the **focal depth** of earthquakes using:
- Latitude (`latitude`)
- Longitude (`longitude`)
- Magnitude (`richter`)

## Conclusion

This project explored the use of machine learning to predict earthquake focal depth using the Quakes dataset, which includes only three features: `latitude`, `longitude`, and `richter` magnitude. Given the weak linear correlations between these features and the target variable, we selected XGBoost for its ability to model nonlinear relationships and feature interactions.

After training a baseline model and performing hyperparameter tuning, we achieved the following:

- **Baseline XGBoost RMSE**: 90.67
- **Tuned XGBoost RMSE**: 77.58
- **Tuned XGBoost MAE**: 41.61
- **Best parameters**: `n_estimators = 312`, `learning_rate = 0.055`, `max_depth = 6`

These results represent a **~17% improvement in MAE** and a **~14% improvement in RMSE** over the baseline model.

Visual analysis of the predictions and residuals confirmed that:
- Most predictions are close to the actual values, especially for shallow and mid-range depths.
- The model tends to underpredict deeper events, which is expected given the skewed distribution of the target variable.
- Residuals are mostly centered around zero, with a slight right skew.

Despite the limited feature set and lack of temporal or tectonic context, the model performs reasonably well and serves as a strong baseline for future improvements. Potential next steps include incorporating additional geophysical data, applying log transformations to reduce skew, or reframing the problem as a classification task using depth bins.
