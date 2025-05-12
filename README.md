# App Store Game Monetization Insight & Prediction

This project aims to predict the **in-app purchase (IAP) value** of mobile games on the App Store by exploring different machine learning models. By analyzing key app features (e.g., genre, languages, size), this project aims to support mobile developers in their **pricing and monetization strategy** through EDA and predictive models and evaluate models' performance using metrics such as MAE and R². This project's goal is to provide actionable insights to app developers who seek to maximize revenue without compromising user retention or overall user experience.


## Problem Statement

Mobile game developers face different challenges in a competitive app market:
- Determining the **right price** that balances user acquisition and profitability
- Designing **in-app purchases** that enhance monetization while maintaining user satisfaction
- Leveraging **historical app store data** to make informed decisions about pricing and revenue models


## Aims and Objectives

- Visualize the relationships between key features and the target variables (IAP Mean)
- Build and evaluate ML models for:
  - Predicting **average IAP value**
- Interpret feature influence on monetization strategy


## Justification for Excluding Price

The original dataset included a `Price` column, but this was excluded from model training and evaluation because:
- Approximately **84% of apps were free**, leading to severe class imbalance
- Paid apps mostly clustered around $0.99–$4.99, providing little variability
- Models trained to predict `Price` overwhelmingly defaulted to "free" and offered little meaningful insight
- The focus was shifted to `IAPMean` as a more representative and informative monetization target


## Tools and Technologies

- **Language**: Python ≥ 3.9
- **Dataset**: [17K Apple App Store Strategy Games](https://www.kaggle.com/datasets/tristan581/17k-apple-app-store-strategy-games)


## Models and Techniques Used

### Supervised Learning

**Regression**
- Random Forest Regressor
- XGBoost Regressor
- AdaBoost Regressor
- Linear Regression
- Support Vector Regressor (SVR)
- K-Nearest Neighbors Regressor

**Classification**
- Random Forest Classifier
- XGBoost Classifier
- AdaBoost Classifier
- Logistic Regression
- Support Vector Classifier (SVC)
- K-Nearest Neighbors Classifier

**Evaluation Metrics**
- Regression: MAE, RMSE, R²
- Classification: Accuracy, Precision, Recall, F1-score, ROC-AUC


## Project Structure

- `main.ipynb`: Contains data preprocessing, EDA, model building, and evaluation
- `appstore_games.csv`: Raw dataset used for analysis and modeling

## Credits

- Author: Shek Arnald
