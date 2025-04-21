# IBM Applied Data Science Capstone SpaceX
This project is part of the Applied Data Science Capstone by IBM on Coursera, where key data science and machine learning techniques are applied to a real-world dataset.

# 🚀 SpaceX Falcon 9 First Stage Landing Prediction
This repository contains the completed capstone project for the **Applied Data Science Capstone** offered by IBM on Coursera. The goal of this project is to **predict whether the first stage of the SpaceX Falcon 9 rocket will successfully land**, leveraging real-world datasets and applying various data science and machine learning techniques.

---

## 📌 Project Objective
SpaceX significantly reduces launch costs by reusing the first stage of the Falcon 9 rocket. A successful landing means a more economical mission. This project aims to predict landing success using historical launch data and help stakeholders better understand the factors that influence mission outcomes.

---

## 📊 Key Project Components

### 1. Data Collection
- **API Source**: SpaceX API `https://api.spacexdata.com/v4/rockets/`
- **Web Scraping**: Launch data scraped from [Wikipedia](https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches)
- Datasets were filtered to include only Falcon 9 launches.
- Missing values were handled using mean imputation.

### 2. Data Wrangling & Preparation
- Cleaned, formatted, and merged datasets.
- Encoded categorical features using one-hot encoding.
- Added a new target column: `Class` (1 = Success, 0 = Failure).
- Final dataset: **90 rows × 83 features**

### 3. Exploratory Data Analysis (EDA)
Utilized **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**, and **SQL** to:
- Analyze distributions of payload, orbit types, launch sites, and mission outcomes.
- Investigate feature relationships, such as:
  - Payload vs. Mission Outcome
  - Launch Site vs. Success Rate
  - Orbit Type vs. Landing Success

### 4. Data Visualization
- **Folium**: Interactive map visualizations to display:
  - Launch site locations
  - Success/Failure markers
  - Proximity to cities, railways, highways, coastlines
- **Dash**: Interactive dashboard to visualize:
  - Launch success distribution per site
  - Correlation between payload and success rate

### 5. Predictive Modeling
Implemented four machine learning classification algorithms using **Scikit-learn**:
- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- K-Nearest Neighbors (KNN)

#### Methodology:
- Standardized data
- Performed train-test split
- Applied GridSearchCV for hyperparameter tuning
- Evaluated models using:
  - **Accuracy Score**
  - **Confusion Matrix**

#### Model Performance (Based on GridSearchCV Best Scores):
| Model               | Best Accuracy |
|--------------------|---------------|
| Decision Tree       | **87.5%**     |
| KNN                 | 84.82%        |
| SVM                 | 84.82%        |
| Logistic Regression | 84.64%        |

---

## 📌 Key Insights & Conclusion
- **Launch Site Impact**: *CCAFS LC-40* showed the highest success rate (43.7%).
- **Booster Reliability**: The *FT* booster variant had consistently high success rates.
- **Payload Mass**: No strong correlation with success/failure, suggesting other factors (e.g., site or booster) are more influential.
- **Decision Tree** was the most effective model for predicting mission outcomes.

> This project provides a robust framework for analyzing and predicting rocket launch success, which can be used to optimize strategy and inform competitive bidding in the commercial aerospace sector.

---

