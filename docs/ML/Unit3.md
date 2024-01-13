# Unit 3

- [Unit 3](#unit-3)
    - [Supervised Learning:](#supervised-learning)
    - [Learning a Class from Example:](#learning-a-class-from-example)
    - [Linear Regression:](#linear-regression)
    - [Logistic Regression:](#logistic-regression)
    - [Naïve Bayes Classifier:](#naïve-bayes-classifier)
    - [Support Vector Machines (SVM):](#support-vector-machines-svm)
    - [K-Nearest Neighbors (KNN) Algorithm:](#k-nearest-neighbors-knn-algorithm)
    - [Decision Trees:](#decision-trees)
    - [Random Forests:](#random-forests)
    - [Model Evaluation: Overfitting \& Underfitting:](#model-evaluation-overfitting--underfitting)

### Supervised Learning:

**Definition:** Supervised learning is a type of machine learning where the algorithm is trained on a labeled dataset, meaning it is provided with input-output pairs. The goal is to learn a mapping from inputs to corresponding outputs, allowing the model to make predictions on new, unseen data. In supervised learning, the algorithm learns from examples, where the correct answers are already known during training.

**Application:** Supervised learning is widely used in various applications, including image and speech recognition, natural language processing, medical diagnosis, and many other tasks where the goal is to predict or classify based on historical data.

### Learning a Class from Example:

**Definition:** Learning a class from examples is a fundamental concept in supervised learning. In this process, the algorithm learns patterns and relationships in the data by being presented with examples that are already labeled with the correct output (class). The algorithm generalizes from these examples to make predictions on new, unseen instances.

**Process:** During training, the algorithm adjusts its parameters to minimize the difference between its predictions and the actual labels in the training set. The learning process involves iteratively updating the model based on the feedback provided by the labeled examples.

### Linear Regression:

**Definition:** Linear regression is a supervised learning algorithm used for predicting a continuous outcome variable based on one or more predictor variables. It assumes a linear relationship between the input features and the target variable. The goal is to find the best-fitting line (or hyperplane in higher dimensions) that minimizes the sum of squared differences between predicted and actual values.

**Use Cases:** Linear regression is commonly employed in scenarios such as predicting house prices based on features like square footage, estimating sales based on advertising expenditure, or forecasting stock prices.

### Logistic Regression:

**Definition:** Despite its name, logistic regression is a classification algorithm used for predicting the probability that an instance belongs to a particular class. It models the relationship between the independent variables and the probability of a specific outcome occurring. The logistic function is employed to map predictions to the range [0, 1], making it suitable for binary and multiclass classification.

**Use Cases:** Logistic regression is applied in various fields, including medical diagnosis (predicting whether a patient has a particular disease), spam detection, and credit scoring.

### Naïve Bayes Classifier:

**Definition:** The Naïve Bayes classifier is a probabilistic machine learning algorithm based on Bayes' theorem. It assumes that features are conditionally independent given the class label, which is a "naïve" assumption but often works well in practice. The algorithm calculates the probability of an instance belonging to a particular class and selects the class with the highest probability.

**Use Cases:** Naïve Bayes is frequently used in text classification tasks, such as spam detection and sentiment analysis. It's also employed in areas like document categorization and medical diagnosis.

### Support Vector Machines (SVM):

**Definition:** Support Vector Machines (SVM) is a supervised learning algorithm used for classification and regression tasks. The primary objective of SVM is to find a hyperplane that best separates data points into different classes while maximizing the margin between the classes. SVM can handle both linear and non-linear relationships through the use of different kernel functions.

**Use Cases:** SVM is commonly employed in image classification, text categorization, and bioinformatics. Its ability to handle high-dimensional data and non-linear decision boundaries makes it versatile in various domains.

### K-Nearest Neighbors (KNN) Algorithm:

**Definition:** The K-Nearest Neighbors (KNN) algorithm is a simple yet effective supervised learning algorithm used for classification and regression tasks. In KNN, predictions are made based on the majority class (for classification) or the average of the nearest neighbors' values (for regression) in the feature space. The "k" in KNN represents the number of neighbors considered.

**Use Cases:** KNN is often applied in recommendation systems, image recognition, and anomaly detection. It is particularly useful when the decision boundary is complex and non-linear.

### Decision Trees:

**Definition:** Decision Trees are a versatile and intuitive supervised learning algorithm used for both classification and regression tasks. They represent a flowchart-like structure where each internal node represents a decision based on a feature, each branch represents an outcome of the decision, and each leaf node represents the final prediction or decision.

**Use Cases:** Decision Trees find applications in fields like finance for credit scoring, medicine for disease diagnosis, and business for decision-making processes.

### Random Forests:

**Definition:** Random Forests is an ensemble learning method that builds multiple decision trees and merges their predictions to improve accuracy and robustness. Each tree in the ensemble is trained on a random subset of the data and features. The final prediction is often determined by a majority vote (for classification) or averaging (for regression) of individual tree predictions.

**Use Cases:** Random Forests are widely used in areas such as finance for fraud detection, ecology for species classification, and bioinformatics for gene expression analysis. They are known for their ability to handle noisy and high-dimensional data.

### Model Evaluation: Overfitting & Underfitting:

**Definition:** Model evaluation is a crucial step in machine learning, and it involves assessing a model's performance on new, unseen data. Overfitting and underfitting are two common issues encountered during model training:

-   **Overfitting:** Occurs when a model learns the training data too well, capturing noise or random fluctuations. As a result, it performs poorly on new data because it has essentially memorized the training set rather than generalizing.

-   **Underfitting:** Occurs when a model is too simple to capture the underlying patterns in the data, resulting in poor performance on both the training and test sets.

**Mitigation:** To address overfitting, techniques such as regularization, cross-validation, and reducing model complexity can be employed. Underfitting is addressed by increasing model complexity, using more relevant features, or choosing a more powerful model.

**Use Cases:** Understanding and mitigating overfitting and underfitting are essential for developing models that generalize well to real-world scenarios. Techniques like learning curves, validation sets, and hyperparameter tuning aid in the evaluation and improvement of model performance.

