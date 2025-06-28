# Electric Vehicle Recommendation System

## 🔍 Introduction

This project develops a recommendation system for electric vehicles (EVs) that personalizes suggestions based on user-defined inputs. Users specify numeric and categorical vehicle attributes via an interactive interface, which are then processed through data transformation and similarity calculations to find the most comparable EVs from the dataset.

---

## 📦 Dataset Description

The dataset contains detailed specifications for various EV models, including:

- **Core Attributes:** Brand, Model, Car Body Type, Segment  
- **Battery & Range:** Battery Capacity (kWh), Number of Cells, Battery Type, Efficiency (Wh/km), Range (km)  
- **Charging:** Fast Charging Power (kW), Fast Charge Port Type  
- **Performance:** Top Speed (km/h), Acceleration 0-100 km/h (s), Torque (Nm)  
- **Practical Specs:** Towing Capacity (kg), Cargo Volume (L), Seats  
- **Dimensions:** Length, Width, Height (mm)  
- **Technical Info:** Drivetrain, Source URL  

The dataset has been cleaned for consistency, with numeric fields standardized and categorical variables encoded for model compatibility.

---

## 🎯 Project Objective

Build an interactive recommendation tool that:

- Collects user input with dropdowns for categorical variables and sliders (with automatic min/max) for numeric variables.
- Transforms inputs via one-hot encoding aligned with the dataset’s structure.
- Normalizes numeric values using MinMax scaling based on the original dataset ranges.
- Computes cosine similarity between user input and all dataset entries in a normalized, encoded feature space.
- Returns the top 5 most similar EVs with associated brand, model, and source URL information.


##  Conclusions

- The dataset was successfully cleaned and standardized, with missing or inconsistent entries handled through targeted imputation and parsing logic.
- Categorical and numeric features were preprocessed through one-hot encoding and MinMax normalization, preparing the data for vector-based similarity comparison.
- An interactive interface was created using `ipywidgets`, allowing users to input both numeric and categorical preferences with automatic min/max range extraction and valid option filtering.
- Cosine similarity was used to identify the top 5 most similar electric vehicles based on the user's specified criteria, returning clear and structured results that include brand, model, and source URL.
- The pipeline maintains alignment between transformed input data and the dataset’s encoded structure, ensuring accurate and meaningful comparisons.

This system provides a foundation for delivering user-personalized EV recommendations using clean data, interpretable logic, and scalable similarity-based methods.
