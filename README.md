# Data Sampling 

## Overview
This project explores the impact of various sampling techniques on the performance of machine learning models. Sampling is an essential method for deriving insights from data without analyzing the entire population. The dataset used in this project initially had a severe class imbalance, which was addressed using oversampling.

## Dataset Details
- **Initial Distribution**:
  - Non-fraudulent cases: 763
  - Fraudulent cases: 9
- **After Oversampling**:
  - The minority class (fraudulent cases) was oversampled to match the majority class, resulting in a balanced dataset.

## Sampling Techniques
1. **Simple Random Sampling**: Random selection of samples from the entire population.
2. **Systematic Sampling**: Selects samples at regular intervals, starting from a randomly chosen initial point.
3. **Stratified Sampling**: Splits the population into distinct subgroups (strata) based on predefined criteria, ensuring proportional representation in the samples.
4. **Cluster Sampling**: Divides the population into clusters and randomly selects entire clusters for analysis.
5. **Bootstrap Sampling**: Creates multiple datasets by resampling the original data with replacement.

## Models Evaluated
The following machine learning models were used to evaluate the performance of the sampling techniques:
1. **Random Forest**
2. **Logistic Regression**
3. **Support Vector Machine (SVM)**
4. **XGBoost**
5. **AdaBoost**

## Results
The table below shows the accuracy scores of each model under different sampling techniques:

| Sampling Technique        | Random Forest | Logistic Regression  | SVM    | XGBoost        | AdaBoost |
|---------------------------|---------------|----------------------|--------|----------------|----------|
| Simple Random Sampling    | 0.9740        | 0.8442               | 0.6234 | 0.9610         | 0.9351   |
| Systematic Sampling       | 1.0000        | 0.8725               | 0.7353 | 0.9902         | 0.9804   |
| Stratified Sampling       | 0.9870        | 0.9481               | 0.6494 | 0.9870         | 0.9351   |
| Cluster Sampling          | 0.9655        | 0.7931               | 0.6552 | 0.9310         | 0.8621   |
| Bootstrap Sampling        | 1.0000        | 0.9481               | 0.6494 | 0.9870         | 0.9740   |

## Conclusion
- **Random Forest** demonstrated excellent performance across all sampling techniques and is the best model overall.
- When considering overfitting as a potential issue (e.g., Simple Random Sampling), **Decision Trees** proved to be the most stable model.
- Sampling techniques like **Stratified Sampling** and **Bootstrap Sampling** worked well in preserving the model's performance while ensuring data diversity.

## Key Insights
- **Data sampling** is crucial for balancing datasets and improving model robustness.
- Oversampling effectively addressed the class imbalance, enabling models to achieve high accuracy.
- The choice of model depends on the trade-off between accuracy and potential overfitting.
