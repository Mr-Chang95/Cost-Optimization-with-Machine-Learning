# Project Cost Optimization
## Danny Chang and Joey Hernandez

## Introduction

In today's data-driven business landscape, accurate outcome predictions are critical. This project addresses the challenges associated with false positives and false negatives in predictive modeling, emphasizing the financial implications of prediction inaccuracies.

## Objective

The primary goal is to develop a binary classification model distinguishing between 'Yes' and 'No' outcomes with the highest accuracy. Considering a cost structure penalizing false positives five times more than false negatives, the model aims to minimize the total cost by balancing sensitivity and specificity.

## Data Inspection

### Target Distribution

The dataset comprises 160,000 observations, presenting a balanced distribution between 'No' (59%) and 'Yes' (41%) classes, conducive to unbiased model training.

### Missing Values

Out of 1% missing data, 1,608 instances were removed due to their negligible impact on model integrity.

### Numerical Variables

Normalization of numerical variables is necessary due to their varying magnitudes, preventing dominance of any single attribute during modeling.

### Categorical Variables

Key categorical variables like 'Country,' 'Month,' and 'Day' require encoding for effective utilization in predictive algorithms.

### Financial Values

Transformation of dollar figures and percentages ensures uniform scaling for statistical and machine learning methods.

## Modeling

### Preprocessing

- Data splitting into training (80%) and test (20%) sets ensures unbiased model evaluation.
- Feature scaling using StandardScaler enhances algorithm performance.
- Validation set creation aids hyperparameter tuning to prevent overfitting.
- Random state (12) ensures result reproducibility.

### Random Forest - Base Model

The Random Forest Classifier, with balanced class weights, serves as the baseline model. Achieving an overall accuracy of 91%, it provides a solid foundation for further exploration.

### XGBoost - F1 Optimized

XGBoost, known for speed and performance, is optimized using F1 score-based threshold determination. Achieving an accuracy of 93%, this model outperforms the Random Forest baseline.

### XGBoost - Cost Optimized

A cost-sensitive approach optimizes the threshold based on financial implications. This model prioritizes cost reduction, demonstrating the importance of aligning evaluation metrics with specific cost structures.

### Neural Network

A Deep Neural Network (DNN) explores the capabilities of deep learning. Cost-optimized thresholds lead to impressive results, with a total cost of $84,680, showcasing its efficacy in minimizing financial loss due to misclassifications.

## Conclusion

Cost analysis reveals the Neural Network model as the most economically viable option, aligning closely with business objectives. Cross-validation reinforces its suitability for diverse and extensive datasets, providing valuable insights into real-world effectiveness and reliability. This project underscores the significance of integrating cost considerations into model selection and optimization processes for practical applications.