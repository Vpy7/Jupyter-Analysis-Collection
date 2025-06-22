# TEEN PSYCHOLOGY Dataset

## 📘 Introduction

Teen mental health is a growing concern in an increasingly digital and high-pressure world. The "Inside Teen Minds" dataset offers a detailed simulation of daily mood, stress levels, habits, and digital behavior among high school students across more than 40 countries in 2025. This project uses clustering techniques to explore patterns in the mental health and lifestyle behaviors of teens. The goal is to identify distinct behavioral profiles and gain insights into how daily habits and technology use relate to emotional well-being.

---

## 📊 Dataset Description

The dataset consists of several CSV files, with the main file containing daily time-series data for 30,000 students. It includes over 35 features related to:

- Mood and stress levels  
- Sleep patterns and screen time  
- Exercise, journaling, and social interaction  
- Study productivity and AI tool usage (e.g., ChatGPT, Gemini, Notion AI)  
- Demographic information such as age, gender, and country  

Supporting files provide aggregated statistics by country, gender, and AI tool usage frequency. The dataset is well-suited for unsupervised learning, behavioral analysis, and mental health research.

The files include:

* wellness_habits_distribution.csv
* average_mood_stress_by_gender.csv
* ai_usage_by_country.csv
* ai_tool_popularity.csv
* screen_vs_sleep_by_age.csv
* daily_mood_stress_trends.csv
* average_support_feeling_by_country.csv
* modern_teen_mental_health_main.csv

The dataset can be found here: https://www.kaggle.com/datasets/dakshbhatnagar08/inside-teen-minds-global-mental-health-and-habits

---

## 🎯 Objective

The objective of this project is to apply unsupervised learning methods to discover meaningful clusters among students based on their daily habits and mental health indicators. The specific goals are:

- Conduct exploratory data analysis to understand key trends and variable distributions  
- Select relevant features for clustering based on behavioral and psychological indicators  
- Apply clustering algorithms (e.g., K-Means, Hierarchical Clustering) to group similar students  
- Analyze and label the resulting clusters to interpret behavioral patterns  
- Visualize the cluster characteristics across demographics such as age, gender, and country  

The aim is to identify common lifestyle patterns and potential risk groups, providing a clearer understanding of the diverse ways teens cope with stress, manage technology, and maintain mental well-being.

### 🔍 Key Patterns

### Cluster Profile Interpretation (Top MI Features)

#### Cluster 0 (n = 678)
- Very low meditation on any day.
- High screen time (6.96), moderate stress (4.03).
- Strong support feeling (6.57), average mood and journaling.
- Age ~15.5.

**Interpretation**:  
This is the **baseline group** — students with **low mindfulness**, **high digital engagement**, and **average emotional indicators**. Its large size reflects a **common, unengaged behavioral pattern**.

---

#### Cluster 1 (n = 67)
- 100% meditate on Saturday, some on Sunday.
- High support (6.61), solid mood (6.18), average journaling.
- Slightly lower stress and screen time.
- Age ~15.4.

**Interpretation**:  
**Weekend meditators** with **high support and mood**, emotionally balanced.

---

#### Cluster 2 (n = 70)
- Very high meditation on Tuesday (0.94).
- High support and mood, most journaling on Thursday (0.56).
- Balanced screen time and stress.
- Age ~15.6.

**Interpretation**:  
**Structured weekday meditators**, emotionally healthy and reflective.

---

#### Cluster 3 (n = 67)
- Very high Friday meditation (0.91).
- Good mood (6.04), lowest journaling (0.21).
- Balanced support and screen time.
- Age ~15.6.

**Interpretation**:  
**End-of-week meditators** with strong mood but **low reflection habits**.

---

#### Cluster 4 (n = 63)
- Very high Monday meditation (0.98).
- Strong mood (6.17), lowest stress (3.86).
- High screen time (7.01), low journaling on Thursday.
- Age ~15.7.

**Interpretation**:  
**Routine-focused meditators** with **low stress** and positive regulation.

---

#### Cluster 5 (n = 55)
- Very high Sunday meditation (0.95).
- Highest screen time (7.11) and stress (4.20).
- Mood slightly lower (5.88), moderate journaling.
- Oldest group (~15.87).

**Interpretation**:  
**Reflective Sunday meditators** who show **higher stress and screen time**, possibly end-of-week burnout.

---

### Summary
- Clusters are clearly shaped by **day-specific meditation behavior**.
- Mood, support, journaling, and screen time follow distinct patterns.
- **Cluster 0** represents the **default profile** of non-meditators — large but meaningful.
