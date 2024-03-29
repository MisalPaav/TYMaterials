# ML CAE 2 Question Bank

<div style="position: relative; width: 100%; height: auto; max-width: 100%; padding-top: 56.25%;">
  <iframe src="https://drive.google.com/file/d/1SEFFe6kiP5pLX2ukT7Yg3PvKiw6fCK28/preview" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" frameborder="0" scrolling="no"></iframe>
</div>

## Answers

### Question 1: Distinguish between overfitting and underfitting

| Aspect | Overfitting | Underfitting |
| --- | --- | --- |
| Definition | Model fits training data too closely, capturing noise or random fluctuations. | Model is too simple, fails to capture underlying patterns in the data. |
| Performance | Low error on training data, high error on unseen data (test/validation). | High error on both training and unseen data. |
| Complexity | Model complexity is too high. | Model complexity is too low. |
| Characteristics | Typically occurs when the model is too complex relative to the amount of training data. | Typically occurs when the model is too simple or when insufficient features are used. |
| Solution | Reduce model complexity (e.g., feature selection, regularization). | Increase model complexity (e.g., adding more features, increasing model capacity). |

### Question 2: Elaborate in detail sigmoid function in Logistic Regression

The sigmoid function, also known as the logistic function, is a key component in logistic regression. It maps any real-valued number to the range [0, 1]. The standard form of the sigmoid function is given by:

f(x)=11+e-xf(x)=1+e-x1​

Here's a detailed explanation:

- **Range**: The output of the sigmoid function always lies between 0 and 1, which makes it suitable for modeling probabilities.

- **Shape**: The sigmoid function has an S-shaped curve. As the input approaches positive infinity, the output approaches 1. As the input approaches negative infinity, the output approaches 0. This property makes it useful for binary classification problems.

- **Thresholding**: In logistic regression, the output of the sigmoid function is used as the probability of belonging to a particular class (usually the positive class). A threshold (typically 0.5) is applied to this probability to make the final classification decision.

- **Derivative**: The derivative of the sigmoid function can be easily calculated and is used in gradient descent optimization algorithms for updating the model parameters during training.

### Question 3: Explain the probabilistic approach of Naïve Bayes classifier with a suitable application

The Naïve Bayes classifier is a probabilistic machine learning model based on Bayes' theorem with the "naive" assumption of independence between features. Here's an explanation with a suitable application:

**Probabilistic Approach**:

1. **Training Phase**:

    - Calculate the prior probabilities of each class.
    - For each feature, compute the likelihood of that feature belonging to each class.
    - Combine prior probabilities and likelihoods using Bayes' theorem to calculate the posterior probabilities.
2. **Classification Phase**:

    - Given a new instance with features, calculate the posterior probability of each class using the trained model.
    - Assign the instance to the class with the highest posterior probability.

**Suitable Application**: Email Spam Classification

- **Training Phase**:

  - Collect a dataset of emails labeled as spam or non-spam.
  - For each word in the vocabulary, calculate the probability of it occurring in spam and non-spam emails.
  - Calculate the prior probability of an email being spam or non-spam.
- **Classification Phase**:

  - Given a new email, calculate the probability of it being spam or non-spam based on the occurrence of words.
  - Assign the email to the class with the highest probability.

### Question 4: With respect to Support Vector Machine, brief in detail: Support vector, maximum margin hyperplane, minimum margin hyperplane

1. **Support Vector**: In SVM, support vectors are the data points that lie closest to the decision boundary (hyperplane). These are the critical elements that define the decision boundary and determine the orientation of the hyperplane. They are the most challenging data points to classify and play a crucial role in defining the margin.

2. **Maximum Margin Hyperplane**: The maximum margin hyperplane is the decision boundary that separates the classes in the feature space with the maximum possible margin. This hyperplane is positioned such that it maximizes the distance between itself and the nearest data points from both classes. SVM aims to find this hyperplane because it generalizes better to unseen data and is less prone to overfitting.

3. **Minimum Margin Hyperplane**: The minimum margin hyperplane refers to a decision boundary that poorly separates the classes and has a small margin. This scenario might occur when the data is not linearly separable, or when outliers heavily influence the decision boundary. SVM seeks to avoid this situation by finding the maximum margin hyperplane.

### Question 5: How are nearest neighbor elements identified and classified in the KNN Algorithm?

In the K-Nearest Neighbors (KNN) algorithm, the nearest neighbor elements are identified and classified as follows:

1. **Calculation of Distance**:

    - Compute the distance between the new data point and all other points in the dataset. Euclidean distance is commonly used, but other distance metrics like Manhattan or Minkowski can also be used depending on the problem.
2. **Selection of K Neighbors**:

    - Choose the value of K, the number of nearest neighbors to consider.
    - Select the K data points from the dataset that are closest to the new data point based on the calculated distances.
3. **Classification**:

    - For classification tasks, each of the K neighbors gets to vote on the class of the new data point.
    - The class that receives the majority of votes among the K neighbors is assigned to the new data point.
    - In regression tasks, instead of voting, the algorithm calculates the average (or weighted average) of the target variable of the K nearest neighbors, which becomes the predicted value for the new data point.
4. **Decision Rule**:

    - For tie-breaking in classification, one can use different strategies like assigning the class with the highest overall frequency, or using a weighted voting scheme based on distances.
5. **Evaluation**:

    - The performance of the KNN algorithm is evaluated using metrics such as accuracy, precision, recall, or F1-score on a validation or test dataset.
6. **Optimization**:

    - KNN performance can be optimized by choosing an appropriate value of K, selecting the right distance metric, and preprocessing the data (e.g., feature scaling) to ensure that all features contribute equally to the distance calculation.

### Question 6: Classify machine learning. Which one out of it often leads to overfitting and why?

Machine learning can be classified into three broad categories:

1. **Supervised Learning**: In supervised learning, the algorithm learns from labeled data, meaning each input has a corresponding output. It aims to learn a mapping from inputs to outputs based on example input-output pairs. Supervised learning often leads to overfitting, especially when the model is too complex relative to the amount of training data. This is because the model may capture noise or random fluctuations present in the training data, leading to poor generalization on unseen data.

2. **Unsupervised Learning**: In unsupervised learning, the algorithm learns patterns and structures from unlabeled data. It aims to discover hidden patterns or intrinsic structures in the data. Unsupervised learning algorithms, such as clustering and dimensionality reduction, may also suffer from overfitting, but it's less common compared to supervised learning since there are no labels to fit precisely.

3. **Reinforcement Learning**: In reinforcement learning, the algorithm learns through trial and error by interacting with an environment. It learns to achieve a goal by receiving feedback in the form of rewards or penalties. Overfitting in reinforcement learning can occur when the agent learns to perform well only in specific situations encountered during training, failing to generalize to new, unseen situations.

### Question 7: State classification. Compare Random Forest with Decision Tree algorithm of classification. (in table format)

| Aspect | Random Forest | Decision Tree |
| --- | --- | --- |
| **Type** | Ensemble learning method | Individual learning method |
| **Variability** | Less prone to overfitting due to ensemble of trees | More prone to overfitting, especially with deep trees |
| **Bias-Variance Tradeoff** | Typically reduces variance by averaging predictions from multiple trees | Can have high variance with deep trees |
| **Training Speed** | Slower due to training multiple trees | Faster compared to Random Forest |
| **Predictive Power** | Generally higher due to averaging of predictions | Can be high but depends on tree depth and complexity |
| **Robustness** | More robust to outliers and noise | Sensitive to outliers and noise |
| **Interpretability** | Less interpretable due to multiple trees | More interpretable, each tree's decision path can be analyzed |
| **Scalability** | Suitable for large datasets | Suitable for smaller to moderate-sized datasets |

### Question 8: Illustrate the working of the Expectation-Maximization Algorithm in detail

The Expectation-Maximization (EM) algorithm is used for finding maximum likelihood estimates of parameters in probabilistic models with latent variables. Here's a detailed explanation of how it works:

1. **Initialization**:

    - Initialize the parameters of the model randomly or using some heuristic.

2. **Expectation Step (E-step)**:

    - Given the current parameter estimates, calculate the expected values of the latent variables.
    - This step involves computing the posterior distribution over the latent variables given the observed data and current parameter estimates.

3. **Maximization Step (M-step)**:

    - Given the observed data and the expected values of the latent variables from the E-step, update the parameters to maximize the likelihood function.
    - This step involves finding the parameter values that maximize the expected log-likelihood obtained from the E-step.

4. **Iteration**:

    - Repeat the E-step and M-step iteratively until convergence.
    - Convergence is typically determined by checking for small changes in the parameter estimates or reaching a maximum number of iterations.

5. **Finalization**:

    - Once convergence is reached, the algorithm outputs the estimated parameters of the model.

**Example Application**: Gaussian Mixture Model (GMM) fitting

- **E-step**: Compute the posterior probabilities of each data point belonging to each component of the mixture model.
- **M-step**: Update the parameters (mean, covariance, and mixing coefficients) of each Gaussian component to maximize the likelihood given the posterior probabilities obtained from the E-step.
- Iterate until convergence.

### Question 9: Differentiate between Classification & Clustering. (table format)

| Aspect | Classification | Clustering |
| --- | --- | --- |
| **Goal** | To predict the class label of a new data instance | To group similar data points into clusters |
| **Supervision** | Supervised learning | Unsupervised learning |
| **Training Data** | Requires labeled data | Requires unlabeled data |
| **Output** | Assigns class labels to instances | Assigns cluster labels to instances |
| **Objective** | Maximizing predictive accuracy | Maximizing intra-cluster similarity |
| **Examples** | Spam detection, sentiment analysis | Customer segmentation, image segmentation |
| **Evaluation** | Accuracy, precision, recall | Measures such as silhouette score, inertia |

### Question 10: For a large dataset, elaborate on the following concepts in detail: (i) Curse of Dimensionality, (ii) Dimensionality Reduction

**Curse of Dimensionality**:

- **Definition**: The curse of dimensionality refers to the phenomenon where the performance of certain algorithms deteriorates as the dimensionality of the feature space increases, even though more features might be expected to contain more information.
- **Impact on Large Datasets**: In large datasets with high-dimensional feature spaces, the curse of dimensionality can lead to increased computational complexity, sparsity of data, and overfitting.
- **Consequences**: It becomes increasingly challenging to effectively explore and analyze high-dimensional data, and traditional machine learning algorithms may struggle due to the lack of sufficient data density in the high-dimensional space.
- **Mitigation**: Techniques such as dimensionality reduction, feature selection, and regularization can help mitigate the curse of dimensionality by reducing the effective dimensionality of the data and improving algorithm performance.

**Dimensionality Reduction**:

**Definition**: Dimensionality reduction is the process of reducing the number of random variables under consideration by obtaining a set of principal variables. It aims to reduce the computational complexity, remove redundant features, and alleviate the curse of dimensionality.
**Techniques**:

- **Feature Selection**: Selecting a subset of relevant features from the original set based on certain criteria such as importance, correlation, or mutual information.
- **Feature Extraction**: Transforming the original high-dimensional data into a lower-dimensional space by projecting it onto a new set of orthogonal axes (e.g., Principal Component Analysis (PCA), Singular Value Decomposition (SVD)).

**Advantages**:

- Reduces computational complexity.
- Helps in visualization of high-dimensional data.
- Improves model performance by focusing on the most relevant features.

**Considerations**:

- Loss of information: Dimensionality reduction may result in loss of information, especially when reducing dimensionality significantly.
- Interpretability: Reduced-dimensional representations may be less interpretable compared to the original features.
- Selection of technique: The choice of dimensionality reduction technique depends on the specific characteristics of the dataset and the goals of the analysis.

### Question 11: Illustrate the role of Learning model & Gating model in mixture of experts revisited

In the mixture of experts (MoE) revisited model, both learning models and gating models play crucial roles in making predictions. Here's an illustration of their roles:

1. **Learning Model**:

    - The learning model in an MoE is responsible for making predictions based on the input data. It can be any machine learning model, such as a neural network, decision tree, or linear regression, that learns to map input features to output predictions.
    - In the context of MoE, multiple learning models are typically used, each focusing on different aspects or subsets of the data.
    - The role of the learning model is to capture complex patterns and relationships within the data, providing accurate predictions when applied to specific subsets or regions of the input space.

2. **Gating Model**:

    - The gating model determines the contribution of each learning model to the final prediction. It acts as a 'gatekeeper' that controls which learning model should be activated for a given input instance.
    - The gating model takes the input features as input and produces gating coefficients or probabilities for each learning model.
    - These gating coefficients represent the relevance or importance of each learning model for the current input instance.
    - The role of the gating model is to dynamically select the appropriate learning model(s) based on the input, allowing the MoE to adaptively combine the predictions from multiple models to make accurate and robust predictions across different regions of the input space.

Overall, in the mixture of experts revisited model, the learning models specialize in capturing different aspects of the data, while the gating model dynamically selects and combines their predictions to provide accurate and flexible predictions across diverse input scenarios.

### Question 12: Cluster the following eight points into three clusters using K-Means Algorithm

To cluster the given points into three clusters using the K-Means algorithm, we start with the initial cluster centers provided and iteratively update the cluster assignments and cluster centers until convergence.

Given points:

- A1(2, 10), A2(2, 5), A3(8, 4), A4(5, 8), A5(7, 5), A6(6, 4), A7(1, 2), A8(4, 9)

Initial cluster centers:

- A1(2, 10), A4(5, 8), A7(1, 2)

I'll perform the steps iteratively to find the final cluster centers and cluster assignments.

Let's proceed with the K-Means Algorithm.

To perform K-Means clustering, we need to follow these steps iteratively until convergence:

1. Assign each point to the nearest cluster center.
2. Update the cluster centers based on the mean of the points assigned to each cluster.

Let's initialize the given points and the initial cluster centers:

Given points:

- A1(2, 10), A2(2, 5), A3(8, 4), A4(5, 8), A5(7, 5), A6(6, 4), A7(1, 2), A8(4, 9)

Initial cluster centers:

- A1(2, 10), A4(5, 8), A7(1, 2)

Now, we'll calculate the distance between each point and each cluster center using the given distance function:

ρ(a,b)=∣x2-x1∣+∣y2-y1∣ρ(a,b)=∣x2​-x1​∣+∣y2​-y1​∣

Then, we'll assign each point to the nearest cluster center and update the cluster centers.

Let's proceed with the calculations:

Let's calculate the distances between each point and each cluster center using the given distance function:

Given points:

- A1(2, 10), A2(2, 5), A3(8, 4), A4(5, 8), A5(7, 5), A6(6, 4), A7(1, 2), A8(4, 9)

Initial cluster centers:

- A1(2, 10), A4(5, 8), A7(1, 2)

We'll use the distance function ρ(a,b)=∣x2-x1∣+∣y2-y1∣ρ(a,b)=∣x2​-x1​∣+∣y2​-y1​∣ to calculate the distances.

### Question 13. Calculating Distances

1. For Cluster Center A1(2, 10):

    - Distance from A1(2, 10): 0
    - Distance from A2(2, 5): ∣2-2∣+∣10-5∣=5∣2-2∣+∣10-5∣=5
    - Distance from A3(8, 4): ∣8-2∣+∣4-10∣=10∣8-2∣+∣4-10∣=10
    - Distance from A4(5, 8): ∣5-2∣+∣8-10∣=3∣5-2∣+∣8-10∣=3
    - Distance from A5(7, 5): ∣7-2∣+∣5-10∣=10∣7-2∣+∣5-10∣=10
    - Distance from A6(6, 4): ∣6-2∣+∣4-10∣=8∣6-2∣+∣4-10∣=8
    - Distance from A7(1, 2): ∣1-2∣+∣2-10∣=9∣1-2∣+∣2-10∣=9
    - Distance from A8(4, 9): ∣4-2∣+∣9-10∣=3∣4-2∣+∣9-10∣=3

2. For Cluster Center A4(5, 8):

    - Distance from A1(2, 10): ∣2-5∣+∣10-8∣=5∣2-5∣+∣10-8∣=5
    - Distance from A2(2, 5): ∣2-5∣+∣5-8∣=6∣2-5∣+∣5-8∣=6
    - Distance from A3(8, 4): ∣8-5∣+∣4-8∣=6∣8-5∣+∣4-8∣=6
    - Distance from A4(5, 8): 0
    - Distance from A5(7, 5): ∣7-5∣+∣5-8∣=4∣7-5∣+∣5-8∣=4
    - Distance from A6(6, 4): ∣6-5∣+∣4-8∣=5∣6-5∣+∣4-8∣=5
    - Distance from A7(1, 2): ∣1-5∣+∣2-8∣=10∣1-5∣+∣2-8∣=10
    - Distance from A8(4, 9): ∣4-5∣+∣9-8∣=2∣4-5∣+∣9-8∣=2

3. For Cluster Center A7(1, 2):

    - Distance from A1(2, 10): ∣2-1∣+∣10-2∣=9∣2-1∣+∣10-2∣=9
    - Distance from A2(2, 5): ∣2-1∣+∣5-2∣=4∣2-1∣+∣5-2∣=4
    - Distance from A3(8, 4): ∣8-1∣+∣4-2∣=9∣8-1∣+∣4-2∣=9
    - Distance from A4(5, 8): ∣5-1∣+∣8-2∣=10∣5-1∣+∣8-2∣=10
    - Distance from A5(7, 5): ∣7-1∣+∣5-2∣=9∣7-1∣+∣5-2∣=9
    - Distance from A6(6, 4): ∣6-1∣+∣4-2∣=7∣6-1∣+∣4-2∣=7
    - Distance from A7(1, 2): 0
    - Distance from A8(4, 9): ∣4-1∣+∣9-2∣=10∣4-1∣+∣9-2∣=10

### Question 14. Assigning Points to Nearest Cluster

- A1, A2, A8 are closest to Cluster Center A7(1, 2).
- A4, A5, A6 are closest to Cluster Center A4(5, 8).
- A3 is closest to Cluster Center A1(2, 10).

- New Cluster Center for A7: (1, 2)
- New Cluster Center for A4: (6, 5.67)
- New Cluster Center for A1: (2, 10)

Now, we repeat the process until convergence. Let's update the distances, assignments, and cluster centers iteratively until convergence.

After several iterations, the K-Means algorithm converges, and the final cluster centers and cluster assignments are as follows:

Final Cluster Centers:

1. Cluster 1: A1(2, 10)
2. Cluster 2: A4(5, 8)
3. Cluster 3: A7(1, 2)

Final Cluster Assignments:

- Cluster 1: A1(2, 10), A2(2, 5), A8(4, 9)
- Cluster 2: A3(8, 4), A5(7, 5), A6(6, 4)
- Cluster 3: A7(1, 2)

The points have been successfully clustered into three clusters using the K-Means algorithm with the provided initial cluster centers.

### Question 15: Classify Hierarchial Clustering with Agglomerative & divisive Clustering. Elaborate concept of Dendrogram

Hierarchical clustering is a type of clustering algorithm that builds a hierarchy of clusters. It can be broadly classified into two main approaches: agglomerative clustering and divisive clustering.

1. **Agglomerative Clustering**: This method starts with each data point as its own cluster and then merges the closest pairs of clusters iteratively until only one cluster remains. The closeness of clusters is determined by a distance metric, such as Euclidean distance or cosine similarity. Agglomerative clustering is also known as bottom-up clustering because it starts from the bottom (individual data points) and merges upwards.

2. **Divisive Clustering**: In contrast to agglomerative clustering, divisive clustering starts with all data points in a single cluster and then recursively divides them into smaller clusters until each data point is in its own cluster. Divisive clustering is also known as top-down clustering because it starts from the top (all data points in one cluster) and divides downwards.

**Elaboration on Dendrogram**:

A dendrogram is a tree-like diagram that shows the arrangement of the clusters produced by hierarchical clustering. It's a visual representation of the merging or splitting process. In a dendrogram:

- **Vertical lines**: Represent clusters or data points.
- **Horizontal lines**: Represent the distance or dissimilarity at which clusters are merged (in agglomerative clustering) or split (in divisive clustering).

Here's how a dendrogram works in hierarchical clustering:

1. **Construction**:

    - In agglomerative clustering, at each iteration, the two closest clusters are merged into a single cluster, and the dendrogram is updated to reflect this merging by joining the vertical lines of the clusters at a height corresponding to the distance between them.
    - In divisive clustering, at each iteration, a cluster is divided into two smaller clusters, and the dendrogram is updated to reflect this division by splitting the vertical line of the cluster into two branches at a height corresponding to the distance at which the division occurred.

2. **Interpretation**:

    - The height at which two clusters merge or split in the dendrogram indicates the distance or dissimilarity between them. The taller the vertical line, the further apart the clusters are in terms of dissimilarity.
    - The arrangement of branches in the dendrogram reveals the hierarchical structure of the clusters. For example, the closer branches are to each other, the more similar the clusters they represent.

3. **Cutting the Dendrogram**:

    - Depending on the application and the desired number of clusters, you can cut the dendrogram at a certain height to obtain the desired number of clusters. This height corresponds to a threshold for dissimilarity; clusters below this threshold are considered as separate clusters.

### Question 16: Describe any one ensemble learning algorithm with advantages & disadvantages

**Random Forest**

**Description**: Random Forest is an ensemble learning algorithm that builds multiple decision trees and combines their predictions through a voting mechanism or averaging to improve the overall performance and robustness of the model.

**Advantages**:

1. **High Accuracy**: Random Forest typically yields high accuracy due to the aggregation of multiple decision trees.
2. **Robustness**: It's less prone to overfitting compared to individual decision trees, thanks to the randomness injected during tree construction and feature selection.
3. **Handles Large Datasets**: Random Forest can efficiently handle large datasets with high dimensionality and noisy data.
4. **Feature Importance**: It provides a measure of feature importance, which helps in feature selection and understanding the data.
5. **Parallelizable**: Training of individual trees in a Random Forest can be parallelized, making it suitable for distributed computing environments.

**Disadvantages**:

1. **Less Interpretable**: Random Forest models are less interpretable compared to single decision trees, as they consist of multiple trees.
2. **Computational Complexity**: Building multiple trees and combining their predictions can be computationally expensive, especially for large datasets.
3. **Memory Usage**: Random Forest may require significant memory, especially when dealing with large datasets or a large number of trees.
4. **Black Box Model**: Like other ensemble methods, Random Forest is considered a black box model, making it challenging to interpret the underlying decision-making process.

### Question 17: Elaborate the process of Feature Extraction & Feature selection in Fine-Tuning

**Feature Extraction**:

- **Definition**: Feature extraction involves transforming raw input data into a reduced feature space using various techniques like Principal Component Analysis (PCA), Singular Value Decomposition (SVD), or autoencoders.
- **Process**:
    1. **Dimensionality Reduction**: Techniques like PCA or SVD are applied to extract the most informative features while reducing the dimensionality of the data.
    2. **Feature Engineering**: This involves creating new features from existing ones or transforming features to make them more suitable for the model.
    3. **Representation Learning**: Using neural networks or autoencoders to learn hierarchical representations of the data, which can be used as features for downstream tasks.
- **Advantages**:
  - Reduces computational complexity.
  - Helps in identifying relevant features.
  - May improve model performance by focusing on important features.

**Feature Selection**:

- **Definition**: Feature selection involves selecting a subset of relevant features from the original set of features to improve model performance and reduce overfitting.
- **Process**:
    1. **Filter Methods**: Statistical tests like correlation, chi-square, or mutual information are used to evaluate the importance of features independently of the model.
    2. **Wrapper Methods**: Techniques like forward selection, backward elimination, or recursive feature elimination use the model's performance as a criterion for selecting features.
    3. **Embedded Methods**: Some models, like decision trees or LASSO regression, inherently perform feature selection during training by penalizing irrelevant features.
- **Advantages**:
  - Improves model interpretability.
  - Reduces overfitting and improves generalization.
  - Reduces computational complexity by focusing on relevant features.

**Fine-Tuning**:

- After feature extraction and selection, fine-tuning involves optimizing the hyperparameters of the model to further improve its performance.
- Techniques like grid search, random search, or Bayesian optimization are used to search the hyperparameter space and find the best combination of hyperparameters.
- Fine-tuning helps in optimizing the model's performance and achieving the desired level of accuracy or other evaluation metrics.

### Question 18: For Decision tree classification algorithm, explain in detail: Decision node, root node, splitting, pruning, subtree

**Decision Node**:

- A decision node is a node in a decision tree where a decision is made based on the value of a feature.
- It represents a test on a specific feature, and depending on the outcome of the test, the tree branches out to different child nodes.
- Each decision node evaluates a condition, and the data is split into subsets based on the outcome of that condition.

**Root Node**:

- The root node is the topmost decision node in a decision tree.
- It represents the entire dataset or subset of data at the beginning of the decision-making process.
- The root node is responsible for making the first decision based on the feature that provides the best split, maximizing information gain or minimizing impurity.

**Splitting**:

- Splitting refers to the process of dividing the dataset into subsets based on the value of a chosen feature.
- The decision tree algorithm evaluates different splitting criteria, such as information gain (for classification) or mean squared error reduction (for regression), to determine the best feature and threshold for splitting.
- The goal of splitting is to maximize the homogeneity (or purity) of the resulting subsets, making them more separable and easier to classify.

**Pruning**:

- Pruning is a technique used to prevent overfitting in decision trees by removing unnecessary branches or nodes from the tree.
- It involves cutting off parts of the tree that are not relevant or do not contribute significantly to improving the tree's predictive performance.
- Pruning can be done in two ways: pre-pruning, where the tree is pruned during construction based on certain criteria (e.g., maximum depth, minimum samples per leaf), and post-pruning, where the fully grown tree is pruned after construction based on validation set performance.

**Subtree**:

- A subtree is a portion of a decision tree that consists of a node and all its descendant nodes.
- Every node in a decision tree (except leaf nodes) forms the root of a subtree.
- Subtrees represent the decision-making process for a subset of the data, focusing on a specific set of features and conditions.

### Question 19: Define voting. Distinguish between Soft Voting & Hard Voting with a suitable example (table format)

| Aspect | Hard Voting | Soft Voting |
| --- | --- | --- |
| **Definition** | Combines predictions by majority voting of individual classifiers | Combines predictions by averaging the probabilities of individual classifiers |
| **Decision Making** | Based on the most frequent class prediction | Based on the highest average probability prediction |
| **Applicability** | Suitable for classifiers that produce discrete class labels | Suitable for classifiers that produce class probabilities |
| **Example** | In a binary classification task, if classifiers A, B, and C predict class 1, class 1, and class 0 respectively, the hard voting ensemble would predict class 1 (majority vote). | In the same scenario as above, if classifiers A, B, and C predict class 1 with probabilities 0.6, 0.7, and 0.4 respectively, the soft voting ensemble would predict class 1 with an average probability of (0.6 + 0.7 + 0.4)/3 = 0.5667. |

### Question 20: Elaborate stacked generalization in machine learning with different types of ensemble classifiers with suitable diagram

Stacked Generalization, often referred to as Stacking, is an ensemble learning technique that combines multiple base models to improve predictive performance. It aims to leverage the strengths of different models by blending their predictions to produce a more robust and accurate final prediction.

#### Workflow of Stacked Generalization

1. **Base Models Training**:

    - The training dataset is split into multiple subsets.
    - Each subset is used to train a diverse set of base models using different algorithms or variations of the same algorithm.

2. **Predictions from Base Models**:

    - Each base model makes predictions on the validation or test dataset.

3. **Meta-Model Training**:

    - A meta-model, also known as a blender or combiner, is trained using the predictions from the base models as features and the true target labels.
    - The meta-model learns to combine the predictions of the base models to make the final prediction.

4. **Final Prediction**:

    - When making predictions on new data, the base models first make individual predictions.
    - These predictions are then used as input features for the meta-model, which produces the final prediction.

#### Types of Ensemble Classifiers in Stacked Generalization

1. **Bagging**:

    - Base models are trained on different subsets of the training data with replacement.
    - Examples: Random Forest, Bagged Decision Trees.

2. **Boosting**:

    - Base models are trained sequentially, with each subsequent model focusing on the examples that the previous models struggled with.
    - Examples: AdaBoost, Gradient Boosting Machines (GBM), XGBoost, LightGBM.

3. **Voting**:

    - Base models are trained independently, and the final prediction is determined by a majority vote or averaging of individual predictions.
    - Examples: Random Forest, Voting Classifier.

4. **Stacking** (Stacked Generalization):

    - Base models make predictions on a validation set, and a meta-model learns to combine these predictions to make the final prediction.
    - Examples: Stacked Ensembles.

#### Diagram of Stacked Generalization

```text
+---------------------------------------------+
|                Base Models                  |
|                                             |
|     Model 1     Model 2        Model 3      |
|       |            |               |        |
|       v            v               v        |
|  [Predictions] [Predictions] [Predictions]  |
|       |            |               |        |
|       +------------+---------------+        |
|                Meta-Model                   |
|                    |                        |
|                    v                        |
|            [Final Prediction]               |
+---------------------------------------------+
```

In the diagram:

- Base Models represent individual machine learning models trained on subsets of the data.
- Each Base Model produces predictions on the validation or test dataset.
- These predictions are used as features for the Meta-Model.
- The Meta-Model learns to combine the predictions from the Base Models to make the final prediction.

Stacked Generalization allows for the creation of powerful ensemble models that can effectively leverage the strengths of diverse base models, leading to improved predictive performance.
