# Behavioral Biometrics for User Authentication: Analyzing Cursor Movements

This project explores an innovative approach to digital security by analyzing cursor movement patterns as a means of user authentication and categorization. The system leverages unique behavioral patterns in mouse movements to create a dynamic, unobtrusive security layer that operates continuously without requiring explicit user action.

## Overview

In today's digital landscape where cyber threats are constantly evolving, traditional authentication methods often show limitations. This project explores how distinctive cursor movement signatures can be used to:
- Categorize users based on their interaction patterns
- Detect potential security threats
- Enhance user experience through behavioral analysis
- Provide continuous authentication without user intervention

## Dataset Description

The project utilizes two combined datasets:
1. User Interaction Dataset (UID) by Chao Shen
2. Cursor Activity Dataset (MAD) by DFL

### Key Features
- Action Type: Encoded user actions (drag, drop, cursor movement, click)
- Distance Traveled: Total cursor movement distance
- Curvature Metrics: Average, standard deviation, min/max curvature
- Velocity Metrics: Average, standard deviation, min/max velocity
- Angular Velocity Metrics: Average, standard deviation, min/max angular velocity
- Deviation: Largest deviation in cursor trajectory

## Data Preprocessing

1. Feature Selection
   - Comprehensive assessment of 42 features
   - Removal of insignificant features

2. Data Preparation
   - Dataset randomization
   - Normalization of features
   - Anomaly detection using Isolation Forest
   - Dimensionality reduction using UMAP

## Models Implemented

1. Logistic Regression
   - Accuracy: 17.69%
   - Basic binary classification approach

2. Random Forest Classifier
   - Accuracy: 79.4%
   - Best performing model
   - Robust ensemble approach

3. Support Vector Machine (SVM)
   - Accuracy: 20.1%
   - Performance limited by multi-class nature of problem

4. AdaBoost
   - Accuracy: 74.24%
   - Iterative boosting approach

5. XGBoost
   - Accuracy: 75.1%
   - Enhanced performance through regularization

6. Multi Layer Perceptron (MLP)
   - Accuracy: 45.0%
   - Neural network approach

## Key Findings

- Ensemble methods (Random Forest, AdaBoost, XGBoost) showed the most promise for user classification
- Complex, non-linear patterns in cursor movements require sophisticated modeling approaches
- Traditional binary classifiers (Logistic Regression, SVM) struggled with the multi-class nature of the problem

## Setup and Installation

```bash
# Clone the repository
git clone [repository-url]

# Install required packages
pip install -r requirements.txt
```

## Usage

```python
# Example code for model training and prediction
# (Add specific implementation details)
```

## Future Work

- Further optimization of MLP with hyperparameter tuning
- Investigation of additional feature engineering approaches
- Enhancement of real-time prediction capabilities
- Integration with existing authentication systems

## Contributors

- Mayank Pandey (mayank21264@iiitd.ac.in)
- Sunny Dhaka (sunny21429@iiitd.ac.in)
- Tushar Goel (tushar21431@iiitd.ac.in)

## References

1. Bashira Akter Anima. "User authentication based on mouse movement data using normalized features." ResearchGate, 2017.
2. "Identifying user authentication and most frequently used region based on mouse movement data: A machine learning approach." ResearchGate, 2021.
3. "User activity anomaly detection by mouse movements in web surveys." Academia.edu, 2021.
