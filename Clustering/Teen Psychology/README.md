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

## Conclusion

While mathematically accurate (enough), the method exposed in this notebook is flawed when it comes to taking decisions regarding Teen Psychology. Therefore a second Method is exposed in a second Notebook: https://github.com/Vpy7/Jupyter-Analysis-Collection/tree/main/Clustering/Teen%20Psychology%20v2
