# Machine Learning Question Bank Solution

- [Machine Learning Question Bank Solution](#machine-learning-question-bank-solution)
  - [1.  **Distinguish between Supervised Learning and Unsupervised Learning:**](#1--distinguish-between-supervised-learning-and-unsupervised-learning)
  - [2.  **Explain machine learning in medical diagnosis:**](#2--explain-machine-learning-in-medical-diagnosis)
  - [3.  **Explain machine learning in defense sector:**](#3--explain-machine-learning-in-defense-sector)
  - [4.  **Explain machine learning life cycle:**](#4--explain-machine-learning-life-cycle)
  - [5.  **Explain market basket analysis using association rule mining:**](#5--explain-market-basket-analysis-using-association-rule-mining)
  - [6.  **Classify machine learning. Which one out of it often leads to overfitting and why?**](#6--classify-machine-learning-which-one-out-of-it-often-leads-to-overfitting-and-why)
  - [7.  **Explain in detail: Training dataset vs testing dataset.**](#7--explain-in-detail-training-dataset-vs-testing-dataset)
  - [8.  **Explain geometric model and probabilistic model in detail.**](#8--explain-geometric-model-and-probabilistic-model-in-detail)
  - [9.  **Explain overfitting and underfitting with respect to machine learning.**](#9--explain-overfitting-and-underfitting-with-respect-to-machine-learning)
  - [10.  **Explain feature as split and feature as predictor with an example.**](#10--explain-feature-as-split-and-feature-as-predictor-with-an-example)
    - [Feature as Split](#feature-as-split)
      - [Example 1](#example-1)
    - [Feature as Predictor](#feature-as-predictor)
      - [Example 2](#example-2)
  - [11. The average score on a test is 80 with a standard deviation of 10. With a new teaching curriculum introduced it is believed that this score will change. On random testing, the score of 38 students, the mean was found to be 88. With a 0.05 significance level, is there any evidence to support this claim? (Z score at 0.05 significance level is 1.96)](#11-the-average-score-on-a-test-is-80-with-a-standard-deviation-of-10-with-a-new-teaching-curriculum-introduced-it-is-believed-that-this-score-will-change-on-random-testing-the-score-of-38-students-the-mean-was-found-to-be-88-with-a-005-significance-level-is-there-any-evidence-to-support-this-claim-z-score-at-005-significance-level-is-196)
  - [12. A genetics engineer was attempting to cross a tiger and a cheetah. She predicted a phenotypic outcome of the traits she was observing to be in the following ratio 4 stripes only: 3 spots only: 9 both stripes and spots. When the cross was performed and she counted the individuals she found 50 with stripes only, 41 with spots only and 85 with both. According to the Chi-square test, did she get the predicted outcome?](#12-a-genetics-engineer-was-attempting-to-cross-a-tiger-and-a-cheetah-she-predicted-a-phenotypic-outcome-of-the-traits-she-was-observing-to-be-in-the-following-ratio-4-stripes-only-3-spots-only-9-both-stripes-and-spots-when-the-cross-was-performed-and-she-counted-the-individuals-she-found-50-with-stripes-only-41-with-spots-only-and-85-with-both-according-to-the-chi-square-test-did-she-get-the-predicted-outcome)
  - [13. In the garden pea, yellow cotyledon color is dominant to green, and inflated pod shape is dominant to the constricted form. Considering both of these traits jointly in self-fertilized dihybrids, the progeny appeared in the following numbers: 193 green, inflated 184 yellow constricted 556 yellow, inflated 61 green, constricted Do these genes assort independently? Support your answer using Chi-square analysis](#13-in-the-garden-pea-yellow-cotyledon-color-is-dominant-to-green-and-inflated-pod-shape-is-dominant-to-the-constricted-form-considering-both-of-these-traits-jointly-in-self-fertilized-dihybrids-the-progeny-appeared-in-the-following-numbers-193-green-inflated-184-yellow-constricted-556-yellow-inflated-61-green-constricted-do-these-genes-assort-independently-support-your-answer-using-chi-square-analysis)
  - [14. **What is entropy? Explain information gain with the help of an example.**](#14-what-is-entropy-explain-information-gain-with-the-help-of-an-example)
    - [Entropy](#entropy)
    - [Information Gain](#information-gain)
      - [Example](#example)
  - [15.  **How will you handle Categorical data using the Scikit-Learn library? Explain with an example.**](#15--how-will-you-handle-categorical-data-using-the-scikit-learn-library-explain-with-an-example)
  - [16.  **Describe the feature selection algorithm which contributes best to the accuracy of the model?**](#16--describe-the-feature-selection-algorithm-which-contributes-best-to-the-accuracy-of-the-model)
    - [Feature Selection Algorithm](#feature-selection-algorithm)
  - [17. **Explain missing data preprocessing in machine learning using the given example dataset.**](#17-explain-missing-data-preprocessing-in-machine-learning-using-the-given-example-dataset)
  - [18.  **What is the curse of dimensionality issue? How does Principal Component Analysis help to reduce the dimensionality issue?**](#18--what-is-the-curse-of-dimensionality-issue-how-does-principal-component-analysis-help-to-reduce-the-dimensionality-issue)
  - [19.  **Explain Sparse PCA vs. Kernel PCA.**](#19--explain-sparse-pca-vs-kernel-pca)
  - [20.  **Explain the step-by-step application of PCA.**](#20--explain-the-step-by-step-application-of-pca)
  - [21.  **Explain one-hot encoding and label encoding.**](#21--explain-one-hot-encoding-and-label-encoding)
  
## 1.  **Distinguish between Supervised Learning and Unsupervised Learning:**

| Supervised Learning                         | Unsupervised Learning                       |
|---------------------------------------------|---------------------------------------------|
| Learning with labeled data, input-output pairs are provided | Learning with unlabeled data, no specific outputs are provided |
| Predicting output based on input features   | Extracting patterns, structures, or relationships from data |
| Training model using labeled data           | Training model using unlabeled data         |
| Feedback is provided during training        | No explicit feedback provided during training |
| Classification, regression                  | Clustering, dimensionality reduction         |
| Highly dependent on labeled data            | Not dependent on labeled data               |
| Accuracy, precision, recall                 | Silhouette score, inertia, reconstruction error |

**Example:** If we want to classify emails as spam or not spam, and we have a dataset where each email is labeled as spam or not spam, then it's a supervised learning problem. Conversely, if we want to group similar documents together without any prior labels, it's an unsupervised learning problem.

## 2.  **Explain machine learning in medical diagnosis:**

- Machine learning in medical diagnosis involves using algorithms to analyze medical data, such as patient records, medical images, or genetic information, to assist in diagnosing diseases or predicting patient outcomes.
- Algorithms can be trained on historical data from patients with known diagnoses to learn patterns and relationships between symptoms, test results, and diseases.
- Machine learning models can help doctors by providing insights into complex data, assisting in early detection of diseases, predicting patient outcomes, and personalizing treatment plans based on individual patient characteristics.
- Examples of machine learning applications in medical diagnosis include image classification for detecting tumors in medical images (like MRI or X-ray scans), predictive modeling for identifying patients at high risk of certain diseases, and natural language processing for extracting information from medical texts and records.

## 3.  **Explain machine learning in defense sector:**

- Machine learning in the defense sector involves leveraging algorithms and data analytics to enhance various aspects of defense operations, including threat detection, decision-making, cybersecurity, and resource optimization.
- Applications of machine learning in defense include image recognition for detecting objects of interest in satellite imagery or surveillance videos, anomaly detection for identifying unusual behavior in network traffic that could indicate cyberattacks, predictive maintenance for optimizing the maintenance schedules of military equipment, and autonomous systems for tasks such as unmanned aerial vehicle (UAV) operations or autonomous vehicles.
- Machine learning models can analyze vast amounts of data from sensors, surveillance systems, and other sources to provide actionable insights, improve situational awareness, and support military planning and operations.
  
## 4.  **Explain machine learning life cycle:**

The machine learning life cycle consists of several stages, including data collection, data preprocessing, model training, model evaluation, deployment, and monitoring.

- **Data Collection:** Gathering relevant data from various sources, which may include databases, APIs, or sensor data.
- **Data Preprocessing:** Cleaning the data, handling missing values, removing outliers, and transforming the data into a suitable format for training.
- **Model Training:** Selecting an appropriate machine learning algorithm and training it on the preprocessed data.
- **Model Evaluation:** Assessing the performance of the trained model using evaluation metrics and validation techniques to ensure it generalizes well to unseen data.
- **Deployment:** Integrating the trained model into a production environment where it can make predictions on new data.
- **Monitoring:** Continuously monitoring the deployed model's performance, retraining it periodically with new data, and updating it as needed to maintain its effectiveness over time.
  
## 5.  **Explain market basket analysis using association rule mining:**

Market basket analysis is a technique used in retail and e-commerce to uncover patterns in customer purchase behavior. It aims to identify relationships between items that are frequently bought together.

- Association rule mining is a data mining technique used to discover interesting relationships or associations between variables in large datasets.
- In market basket analysis, the dataset typically consists of transaction records, where each transaction contains a list of items purchased by a customer.
- Association rule mining algorithms, such as the Apriori algorithm, are applied to the transaction data to find rules of the form "If {item A} is purchased, then {item B} is also likely to be purchased."
- The output of market basket analysis is a set of association rules, along with measures such as support, confidence, and lift, which indicate the frequency and strength of the relationships between items.
- Retailers can use the insights gained from market basket analysis to optimize product placement, cross-selling, and targeted marketing strategies, ultimately increasing sales and customer satisfaction.

## 6.  **Classify machine learning. Which one out of it often leads to overfitting and why?**

Machine learning can be classified into three main categories:

- **Supervised Learning:** In supervised learning, the algorithm learns from labeled data, aiming to learn the mapping from input variables to the target variable.
- **Unsupervised Learning:** Unsupervised learning deals with unlabeled data, where the algorithm tries to find hidden patterns or structures in the input data.
- **Reinforcement Learning:** In reinforcement learning, the algorithm learns to make decisions by interacting with an environment to achieve some goal, receiving feedback in the form of rewards or penalties.

Among these, supervised learning often leads to overfitting. Overfitting occurs when a model learns to capture noise or random fluctuations in the training data rather than the underlying relationships. This happens because the model becomes too complex, having too many parameters relative to the amount of training data. As a result, the model fits the training data very well but fails to generalize to new, unseen data.

## 7.  **Explain in detail: Training dataset vs testing dataset.**

- **Training Dataset:** The training dataset is used to train the machine learning model. It consists of input-output pairs (in supervised learning) or just input data (in unsupervised learning). The model learns the patterns and relationships in the training data during the training process, adjusting its parameters to minimize the error between its predictions and the true outputs.

- **Testing Dataset:** The testing dataset is used to evaluate the performance of the trained model. It contains data that the model has not seen during training. The model makes predictions on the testing data, and its performance is assessed using evaluation metrics such as accuracy, precision, recall, or F1 score. Testing data helps assess how well the model generalizes to new, unseen data and provides an estimate of its performance in real-world scenarios.

## 8.  **Explain geometric model and probabilistic model in detail.**

- **Geometric Model:** Geometric models in machine learning represent decision boundaries or decision regions in the feature space. These models aim to separate different classes or clusters in the data using geometric shapes such as lines, planes, or hyperplanes. Examples of geometric models include linear classifiers like Support Vector Machines (SVMs) and decision trees. Geometric models directly model the relationships between features and target variables based on geometric properties of the data.

- **Probabilistic Model:** Probabilistic models, on the other hand, represent uncertainty in the data using probability distributions. These models estimate the probability of different outcomes given the input features. Examples of probabilistic models include Naive Bayes classifiers, logistic regression, and Gaussian Mixture Models (GMMs). Probabilistic models provide a principled framework for handling uncertainty and making decisions based on the likelihood of different outcomes.

## 9.  **Explain overfitting and underfitting with respect to machine learning.**

**Overfitting**

Overfitting occurs when a machine learning model learns the training data too well, capturing noise or random fluctuations in the data rather than the underlying pattern. This results in a model that performs well on the training data but poorly on unseen or test data. In other words, the model memorizes the training examples instead of learning the generalizable patterns, leading to poor performance on new, unseen data.

**Causes of Overfitting**

1. **Complex Models**: Models with high complexity, such as deep neural networks with many parameters, are prone to overfitting.

2. **Insufficient Training Data**: When the amount of training data is limited, the model may overfit by capturing noise rather than the underlying pattern.

3. **Irrelevant Features**: Including irrelevant or noisy features in the model can lead to overfitting, as the model may learn to rely on these features.

**Effects of Overfitting**

- High performance on training data.
- Poor generalization to unseen data.
- High variance in model performance across different datasets.

**Underfitting**

Underfitting occurs when a machine learning model is too simple to capture the underlying structure of the data. In other words, the model fails to learn the patterns present in the training data and performs poorly both on the training data and unseen data.

**Causes of Underfitting**

1. **Model Complexity**: Using a model that is too simple, such as a linear model for highly non-linear data, can result in underfitting.

2. **Insufficient Training**: When the model does not have enough capacity to capture the underlying patterns in the data, it may underfit.

3. **Ignoring Important Features**: If important features are not included in the model, it may not be able to capture the underlying relationships in the data.

**Effects of Underfitting**

- Poor performance on both training and test data.
- Low accuracy and high bias.
- Inability to capture the underlying patterns in the data.

## 10.  **Explain feature as split and feature as predictor with an example.**

### Feature as Split

In the context of decision trees or tree-based algorithms, a feature as a split refers to the process of selecting a feature and a threshold value to partition the dataset into smaller subsets. This partitioning is done based on the values of the chosen feature, with the aim of maximizing the homogeneity or purity of the resulting subsets with respect to the target variable.

#### Example 1

Consider a decision tree for classifying whether a fruit is an apple or an orange based on two features: "color" and "diameter". The decision tree algorithm selects a feature (e.g., "color") and a threshold value (e.g., "red") to split the dataset into two subsets: one subset containing fruits with red color and another containing fruits with colors other than red. This splitting process continues recursively until each subset contains samples belonging to the same class or until a stopping criterion is met.

### Feature as Predictor

In a broader context, a feature as a predictor refers to the role of a feature in predicting the target variable in a machine learning model. Features are the input variables used by the model to make predictions about the target variable. Each feature contributes to the model's prediction in some way, and the model learns the relationship between the features and the target variable during the training process.

#### Example 2

Suppose we have a dataset containing information about houses, including features such as "size", "number of bedrooms", and "location", and we want to predict the house price (target variable). In this case, each feature (e.g., "size", "number of bedrooms", "location") acts as a predictor, providing information that the model uses to make predictions about the house price. For instance, a larger house size or more bedrooms might be associated with a higher house price, and the model learns this relationship from the training data. During prediction, the model uses the values of these features for unseen houses to estimate their prices.

## 11. The average score on a test is 80 with a standard deviation of 10. With a new teaching curriculum introduced it is believed that this score will change. On random testing, the score of 38 students, the mean was found to be 88. With a 0.05 significance level, is there any evidence to support this claim? (Z score at 0.05 significance level is 1.96)

![ML QB 11](https://lh3.googleusercontent.com/d/1TSr8saCCEbB43xDmUdraPGX_kUzYhQTs)

## 12. A genetics engineer was attempting to cross a tiger and a cheetah. She predicted a phenotypic outcome of the traits she was observing to be in the following ratio 4 stripes only: 3 spots only: 9 both stripes and spots. When the cross was performed and she counted the individuals she found 50 with stripes only, 41 with spots only and 85 with both. According to the Chi-square test, did she get the predicted outcome?

![ML QB 12](https://lh3.googleusercontent.com/d/1qfXJWHgwbEMqPjVK9byY70PpOUgCkbbb)

## 13. In the garden pea, yellow cotyledon color is dominant to green, and inflated pod shape is dominant to the constricted form. Considering both of these traits jointly in self-fertilized dihybrids, the progeny appeared in the following numbers: 193 green, inflated 184 yellow constricted 556 yellow, inflated 61 green, constricted Do these genes assort independently? Support your answer using Chi-square analysis

![ML QB 13](https://lh3.googleusercontent.com/d/1bI4Dn7P9AFTlDPx99_3_RnEx7NVRAJQn)

## 14. **What is entropy? Explain information gain with the help of an example.**

### Entropy

Entropy is a measure of randomness or uncertainty in a dataset. In the context of decision trees and information theory, entropy is used to quantify the impurity or disorder of a set of examples. It measures the average amount of information needed to classify a random sample from the dataset.

### Information Gain

Information gain is a concept used in decision tree algorithms, particularly in the process of selecting the best feature to split the dataset. It measures the reduction in entropy or uncertainty that results from splitting the dataset on a particular feature. The feature that leads to the greatest information gain is chosen as the splitting criterion.

#### Example

Consider a dataset of weather conditions and corresponding decisions to play tennis or not. The target variable is whether to play tennis ("Yes" or "No"), and the features include "Outlook" (Sunny, Overcast, Rainy), "Temperature" (Hot, Mild, Cool), "Humidity" (High, Normal), and "Windy" (True, False)

## 15.  **How will you handle Categorical data using the Scikit-Learn library? Explain with an example.**

Scikit-Learn provides utilities to handle categorical data using techniques such as one-hot encoding and label encoding.

- **One-Hot Encoding:** It converts categorical variables into binary vectors where each category is represented by a binary attribute. Scikit-Learn provides the `OneHotEncoder` class for this purpose.

- **Label Encoding:** It converts categorical variables into numerical labels. Scikit-Learn provides the `LabelEncoder` class for this purpose.

  **Example:**

```python
from sklearn.preprocessing import OneHotEncoder, LabelEncoder
import pandas as pd

  # Sample dataset
  data = {'Color': ['Red', 'Blue', 'Green', 'Red']}
  df = pd.DataFrame(data)

  # One-hot encoding
  one_hot_encoder = OneHotEncoder()
  one_hot_encoded = one_hot_encoder.fit_transform(df[['Color']])

  # Label encoding
  label_encoder = LabelEncoder()
  label_encoded = label_encoder.fit_transform(df['Color'])
```

## 16.  **Describe the feature selection algorithm which contributes best to the accuracy of the model?**

### Feature Selection Algorithm

Several feature selection algorithms contribute to the accuracy of a model, depending on the dataset and the underlying problem. Some popular feature selection methods include:

1. **Filter Methods**: These methods select features based on their statistical properties, such as correlation with the target variable or variance. Examples include Pearson correlation coefficient and ANOVA F-test.

2. **Wrapper Methods**: These methods evaluate subsets of features by training and evaluating the model with different combinations of features. Examples include Recursive Feature Elimination (RFE) and Forward/Backward Selection.

3. **Embedded Methods**: These methods perform feature selection as part of the model training process. Examples include Lasso regularization and tree-based feature importance.

## 17. **Explain missing data preprocessing in machine learning using the given example dataset.**

Missing data preprocessing involves handling missing values in the dataset before training a machine learning model. Common techniques include:

- **Imputation:** Replace missing values with a sensible estimate. This can be done using statistical measures such as mean, median, or mode.

- **Deletion:** Remove rows or columns with missing values. This is suitable when the missing data is negligible compared to the size of the dataset.

**Example:**

For the given dataset:

```mathematica
A   B     C     D
0   1.0   2.0   3.0
1   5.0   6.0   NaN
2  10.0  11.0   4.0
3  12.0  14.0   Null
```

We can handle missing values in column C by imputing the missing values using the mean or median of the column, or by deleting the rows with missing values.

## 18.  **What is the curse of dimensionality issue? How does Principal Component Analysis help to reduce the dimensionality issue?**

The curse of dimensionality refers to the problem that arises when working with high-dimensional data. As the number of features or dimensions increases, the volume of the feature space grows exponentially, leading to sparsity of data and computational challenges.

Principal Component Analysis (PCA) is a dimensionality reduction technique used to address the curse of dimensionality. PCA transforms the original high-dimensional data into a lower-dimensional space while preserving most of the variance in the data. It achieves this by identifying the principal components, which are orthogonal linear combinations of the original features that capture the maximum variance.

PCA helps reduce the dimensionality issue by:

- Reducing the number of features while retaining most of the information.
- Removing redundant or correlated features.
- Simplifying the data representation, making it easier to visualize and analyze.
- Speeding up the training of machine learning models by reducing the computational burden.

## 19.  **Explain Sparse PCA vs. Kernel PCA.**

- **Sparse PCA:** Sparse PCA is an extension of PCA that encourages sparsity in the principal components. It aims to find a small number of principal components that have non-zero loadings, leading to a more interpretable and sparse representation of the data. Sparse PCA can be useful when dealing with high-dimensional data where only a few features contribute significantly to the variance.

- **Kernel PCA:** Kernel PCA is a nonlinear extension of PCA that utilizes kernel functions to implicitly map the data into a higher-dimensional space where it may be more linearly separable. Unlike traditional PCA, which operates in the original feature space, kernel PCA can capture complex nonlinear relationships between the data points. Commonly used kernel functions include polynomial, radial basis function (RBF), and sigmoid kernels.

## 20.  **Explain the step-by-step application of PCA.**

The steps involved in applying PCA are as follows:

1. **Standardize the data:** If the features have different scales, it's important to standardize them to have zero mean and unit variance.

2. **Compute the covariance matrix:** Calculate the covariance matrix of the standardized data.

3. **Compute the eigenvectors and eigenvalues:** Decompose the covariance matrix to obtain its eigenvectors and corresponding eigenvalues.

4. **Select the principal components:** Sort the eigenvectors by their corresponding eigenvalues in descending order and select the top k eigenvectors to form the principal components.

5. **Project the data onto the principal components:** Transform the original data onto the new lower-dimensional space spanned by the selected principal components.

## 21.  **Explain one-hot encoding and label encoding.**

- **One-Hot Encoding:** One-hot encoding is a technique used to convert categorical variables into binary vectors. Each category is represented by a binary attribute, where only one attribute is 1 (hot) and the rest are 0 (cold). One-hot encoding creates binary vectors for each category, making it suitable for algorithms that cannot handle categorical data directly.

- **Label Encoding:** Label encoding is a technique used to convert categorical variables into numerical labels. Each category is assigned a unique integer label. Label encoding transforms categorical variables into ordinal data, which can be used by algorithms that can interpret numerical data but may not handle categorical data directly.
