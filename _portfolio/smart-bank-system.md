---
title: "Integrated Smart Bank System - ML-Powered Streamlit App"
excerpt: "End-to-end ML pipelines for fraud detection, customer attrition prediction, and credit card recommendations with real-time predictions dashboard."
tech_stack: ["Python", "scikit-learn", "XGBoost", "SMOTE", "Streamlit", "Machine Learning"]
collection: portfolio
---

## Overview
Built a comprehensive machine learning solution addressing critical challenges in banking risk management through intelligent automation. The system combines multiple ML models to provide real-time insights for financial institutions.

## Key Features
- **Fraud Detection**: Advanced ML pipeline achieving 85.6% accuracy with AUC of 0.91
- **Customer Attrition Prediction**: High-performance model with 97.3% accuracy and AUC of 0.9958
- **Credit Card Recommendation**: Intelligent recommendation system based on customer profiles
- **Real-time Dashboard**: Interactive Streamlit interface for instant predictions and insights

## Technical Implementation

### Data Engineering
- **Data Pipeline**: Robust preprocessing with feature engineering and data validation
- **Imbalanced Data Handling**: Advanced resampling techniques using SMOTE and SMOTETomek
- **Feature Engineering**: PCA implementation and pseudo credit score generation
- **Hyperparameter Tuning**: Grid search optimization for maximum model performance

### Machine Learning Models
- **Algorithms**: XGBoost, GradientBoosting, and ensemble methods
- **Model Validation**: Cross-validation and comprehensive performance metrics
- **Model Persistence**: Efficient model serialization using joblib

### Deployment
- **Real-time Interface**: Streamlit web application for instant predictions
- **Interactive Visualizations**: Dynamic charts and graphs for data insights
- **User Experience**: Intuitive interface designed for financial professionals

## Technologies Used
- **Core**: Python, scikit-learn, XGBoost, GradientBoosting
- **Data Processing**: pandas, numpy, imbalanced-learn (SMOTE/SMOTETomek)
- **Visualization**: Streamlit, plotly, matplotlib
- **Model Management**: joblib for model persistence

## Performance Metrics
- **Fraud Detection**: 85.6% accuracy, 0.91 AUC score
- **Customer Attrition**: 97.3% accuracy, 0.9958 AUC score
- **Processing Speed**: Real-time predictions under 100ms response time

## Business Impact
- Significant reduction in fraudulent transactions
- Proactive customer retention strategies
- Personalized financial product recommendations
- Enhanced decision-making through data-driven insights

## Future Development
- Integration with banking APIs for live data streams
- Advanced deep learning models for enhanced accuracy
- Mobile application development
- Regulatory compliance features for different markets