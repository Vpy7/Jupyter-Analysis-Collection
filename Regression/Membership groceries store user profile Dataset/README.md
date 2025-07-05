# Membership groceries store user profile Dataset

## Project Description  
This project focuses on analyzing annual behavioral data of members from a membership-based grocery store in China (2024) to predict membership auto-renewal and design targeted retention strategies. The dataset includes variables such as shopping frequency, app engagement, promotions usage, and customer demographics. The goal is to uncover behavioral patterns, build a predictive model, and derive actionable insights to improve customer loyalty and reduce churn.

---

## Objective  
**Predict membership auto-renewal** and **identify key drivers of customer retention** to optimize engagement strategies. Key questions include:  
- What behaviors correlate with higher auto-renewal rates?  
- How do app usage, reward points, and shared accounts impact retention?  
- Which customer segments are at risk of churn, and how can they be targeted effectively?

---

# Dataset Overview  
This dataset contains the annual behavioral records (2024) of members from a large membership-based grocery store in China. It summarizes key consumer activities, including shopping patterns, engagement with promotions and digital tools, loyalty metrics, and membership status. Each row represents a member's aggregated yearly behavior.  


Available at: https://www.kaggle.com/datasets/anselll09/membership-groceries-user-profile

---

## Variables  
- **`id`**: id
- **`gender`**: gender
- **`membership_tier`**: standard or premium.
- **`membership_fee`**: 188 for standard tier and 388 for premium tier.
- **`membership_start_date`**: membership start date. 
- **`membership_auto_renew`**: Whether the membership is set to auto-renew (`1 = Yes`, `0 = No`).  
- **`push_notification_enabled`**: Whether push notifications are enabled (`1 = Enabled`, `0 = Not enabled`).  
- **`shared_account`**: Whether the membership is shared with family/friends (`1 = Yes`, `0 = No`).  
- **`have_app`**: Whether the member uses the grocery store’s mobile app (`1 = Yes`, `0 = No`).
- **`app_engagement_score`**: Unexplained 
- **`bought_store_brand`**: Whether the member bought store-brand products (`1 = Yes`, `0 = No`). 
- **`promotion_participation_count`**: Amount of times the membership has participated in a promotion
- **`average_basket_size`**: Average spending per shopping trip (in CNY, ¥).  
- **`use_count`**: Number of times the member used their account to make a purchase.  
- **`reward_points_used`**: Total reward points redeemed during the year.  

## Conclusions

The analysis of the membership auto-renewal dataset revealed significant challenges in developing a reliable classification model due to the dataset's limitations. The results and precision-recall curves suggest that distinguishing between renewal and non-renewal cases is difficult, particularly for the minority class.

---

### Performance Limitations

- Despite hyperparameter optimization, the model achieved an AUC-ROC of only **0.53**, indicating weak separability between classes.  
- The precision for class 0 remained low (~**18%**), meaning the model struggled to accurately identify non-renewing members.

---

### Threshold Adjustment Impact

- The optimal threshold (**0.53**), chosen to minimize precision-recall differences, did not significantly improve overall performance.  
- Adjusting the threshold slightly improved recall for the minority class but did not enhance classification quality overall.

---

### Dataset Constraints

- The results suggest that the dataset does not contain sufficient distinguishing features to effectively model renewal behavior.  
- High imbalance between classes and potential noise (e.g., presence of outliers in renewal cases) might be affecting the model's learning capacity.

---

## Final Consideration

Given the observed limitations, the dataset may not be well-suited for predicting auto-renewal behavior with high confidence. Future improvements could involve:

- Collecting more representative data with better feature engineering.  
- Addressing data quality issues, including outlier removal.

At this stage, proceeding with this dataset may not yield meaningful results without additional refinements.

Note: **XGBoost**, **LightGBM** and other methods to handle imbalance were already implemented with no success.
