# Data Science Algorithms and Concepts with Numerical Examples

## Neural Networks (Biological Brain representation)

Neural networks are computational models inspired by the human brain's biological neural networks. They consist of interconnected nodes (neurons) that process information through weighted connections. Just as the human brain learns through adjusting synaptic connections, artificial neural networks learn by adjusting weights between neurons.

**Mathematical Example**: 
Consider a simple neuron with inputs x₁ = 0.5 and x₂ = 0.8, with weights w₁ = 0.4 and w₂ = 0.6. The weighted sum would be:
z = x₁w₁ + x₂w₂ = 0.5(0.4) + 0.8(0.6) = 0.2 + 0.48 = 0.68

## ANN (Artificial Neural Networks)

ANNs are structured implementations of neural networks used for machine learning tasks. They typically contain an input layer, one or more hidden layers, and an output layer.

**Mathematical Example**:
For a simple ANN with one hidden layer (2 neurons) and inputs x₁ = 2, x₂ = 3:
- Hidden layer calculation with weights w₁₁ = 0.1, w₁₂ = 0.2, w₂₁ = 0.3, w₂₂ = 0.4:
  - h₁ = σ(2(0.1) + 3(0.2)) = σ(0.2 + 0.6) = σ(0.8)
  - h₂ = σ(2(0.3) + 3(0.4)) = σ(0.6 + 1.2) = σ(1.8)
- If σ is sigmoid function: h₁ = 0.69, h₂ = 0.86

## Activation Functions

Activation functions introduce non-linearity into neural networks, enabling them to learn complex patterns. Common functions include sigmoid, tanh, and ReLU.

**Mathematical Example**:
For input z = 2:
- Sigmoid: σ(z) = 1/(1+e⁻ᶻ) = 1/(1+e⁻²) = 0.88
- tanh(z) = (e²-e⁻²)/(e²+e⁻²) = 0.96
- ReLU(z) = max(0,z) = 2

## Decision Tree ID3

Decision trees classify data by creating a flowchart-like structure based on features. The ID3 algorithm builds trees using entropy and information gain.

**Mathematical Example** from search result[9]:
For the "Buy Computer" dataset with attributes age, income, student, and credit rating:

1. Calculate entropy of the dataset:
   Entropy(S) = -9/14 log₂(9/14) - 5/14 log₂(5/14) = 0.94

2. Calculate information gain for the "age" attribute:
   - For age ≤30: 2 yes, 3 no
   - For age 31-40: 4 yes, 0 no
   - For age >40: 3 yes, 2 no
   
   Entropy(age) = 5/14(0.9709) + 0 + 5/14(0.9709) = 0.6935
   Gain(age) = 0.94 - 0.6935 = 0.2465

3. Similar calculations for other attributes show "credit_rating" has the highest gain (0.97), so it becomes the root node.

4. For the example (age≤30, income=medium, student=yes, credit-rating=fair), following the decision tree branches gives the prediction "Buys_computer = yes".

## SVM (Support Vector Machine)

SVM finds the optimal hyperplane that maximizes the margin between classes. It transforms data into higher dimensions using kernel functions when linear separation isn't possible.

**Mathematical Example**:
For two classes with points (1,2), (2,3), (3,1) in class A and (6,5), (7,3), (8,4) in class B:
1. The separating hyperplane might be described by w₁x₁ + w₂x₂ + b = 0
2. With optimal parameters w₁ = 0.6, w₂ = 0.8, b = -3.4
3. The margin equals 2/||w|| = 2/√(0.6² + 0.8²) = 2/1 = 2

## KNN (K-Nearest Neighbors)

KNN classifies new data points based on the majority class of their k nearest neighbors.

**Mathematical Example** from search result[3]:
For a paper tissue classification problem with attributes:
- X₁ = Acid Durability (seconds)
- X₂ = Strength (kg/square meter)
- Y = Classification (Good/Bad)

Training data:
1. (7,7) - Bad
2. (7,4) - Bad
3. (3,4) - Good
4. (1,4) - Good

New instance: (3,7)
For K=3:
1. Calculate squared distances:
   - d((3,7),(7,7)) = (3-7)² + (7-7)² = 16
   - d((3,7),(7,4)) = (3-7)² + (7-4)² = 25
   - d((3,7),(3,4)) = (3-3)² + (7-4)² = 9
   - d((3,7),(1,4)) = (3-1)² + (7-4)² = 13

2. Ranking: (3,4) rank 1, (1,4) rank 2, (7,7) rank 3
3. Classes of nearest neighbors: Good, Good, Bad
4. Majority vote: Good (2) > Bad (1)
Therefore, the new instance (3,7) is classified as "Good".

## Random Forest

Random Forest combines multiple decision trees to improve prediction accuracy and reduce overfitting.

**Mathematical Example** based on search result[7]:
Consider a dataset for predicting customer service usage:
1. Build multiple decision trees by randomly selecting observations and features
2. For classification with 100 trees:
   - 65 trees predict "Will use service" 
   - 35 trees predict "Will not use service"
   - Final prediction: "Will use service" (majority vote)
3. For regression with 5 trees predicting values (120, 115, 118, 125, 122):
   - Final prediction: (120+115+118+125+122)/5 = 120 (average)

## Classification

Classification involves categorizing data into predefined classes based on their features.

**Mathematical Example** from search result[8]:
Classification based on size:
- Objects: Small circle, Medium circle, Large circle
- Order: Small → Medium → Large

Classification based on color:
- Green circles: Small, Medium, Large
- Blue circles: Small, Medium, Large

## Regression

Regression predicts continuous values by establishing relationships between variables.

**Mathematical Example**:
For data points (1,2), (2,4), (3,5), (4,8):
1. Using linear regression: y = mx + b
2. Calculate m = Σ((x-x̄)(y-ȳ))/Σ(x-x̄)² = 1.9
3. Calculate b = ȳ - mx̄ = 0.25
4. Resulting model: y = 1.9x + 0.25
5. Prediction for x = 5: y = 1.9(5) + 0.25 = 9.75

## Simple Linear Regression

Simple linear regression models the relationship between two variables with a straight line.

**Mathematical Example**:
For housing data with house size (x) and price (y):
- Data: (1000 sq ft, $150k), (1500 sq ft, $200k), (2000 sq ft, $250k), (2500 sq ft, $300k)
- Correlation coefficient: r = 0.999
- Slope: m = r × (sᵧ/sₓ) = 0.999 × (61.2/645) = 0.095
- Intercept: b = ȳ - mx̄ = 225 - 0.095(1750) = 58.75
- Model: Price = 0.095 × Size + 58.75 (in thousands)
- For a 3000 sq ft house: Price = 0.095(3000) + 58.75 = $343,750

## Polynomial Regression

Polynomial regression models non-linear relationships between variables using polynomial functions.

**Mathematical Example**:
For data points (1,1), (2,4), (3,9), (4,16):
1. Fit a quadratic model: y = ax² + bx + c
2. Solving the system of equations yields a = 1, b = 0, c = 0
3. Model: y = x²
4. Prediction for x = 5: y = 5² = 25

## Confusion Matrix

A confusion matrix evaluates classification performance by showing true positives, false positives, true negatives, and false negatives.

**Mathematical Example**:
For a model predicting diabetes:
- True Positives (TP) = 85 (correctly predicted positive cases)
- False Positives (FP) = 15 (incorrectly predicted positive cases)
- True Negatives (TN) = 90 (correctly predicted negative cases)
- False Negatives (FN) = 10 (incorrectly predicted negative cases)

Metrics:
- Accuracy = (TP+TN)/(TP+FP+TN+FN) = (85+90)/200 = 0.875
- Precision = TP/(TP+FP) = 85/100 = 0.85
- Recall = TP/(TP+FN) = 85/95 = 0.89
- F1-Score = 2×(Precision×Recall)/(Precision+Recall) = 2×(0.85×0.89)/(0.85+0.89) = 0.87

## Unsupervised Learning

Unsupervised learning identifies patterns in unlabeled data without predetermined outputs.

**Mathematical Example**:
For customer segmentation with annual spending (x) and loyalty years (y):
- Customer A: (1000, 1), Customer B: (2000, 2), Customer C: (900, 1.5)
- Customer D: (5000, 5), Customer E: (5500, 4), Customer F: (6000, 6)
- Using distance metrics and clustering, identify 2 clusters:
  - Cluster 1: Customers A, B, C (lower spending, shorter loyalty)
  - Cluster 2: Customers D, E, F (higher spending, longer loyalty)

## K-means Clustering

K-means clustering partitions data into k clusters, assigning each point to the cluster with the nearest centroid.

**Mathematical Example**:
For 2D points (2,3), (3,3), (3,4), (8,8), (9,9), (10,8):

1. Initialize 2 centroids: C₁ = (2,3), C₂ = (8,8)
2. First iteration:
   - Assign points to nearest centroid:
     - Cluster 1: (2,3), (3,3), (3,4)
     - Cluster 2: (8,8), (9,9), (10,8)
   - Recalculate centroids:
     - C₁ = ((2+3+3)/3, (3+3+4)/3) = (2.67, 3.33)
     - C₂ = ((8+9+10)/3, (8+9+8)/3) = (9, 8.33)
3. Continue iterations until convergence

## Naive Bayes Classification

Naive Bayes uses Bayes' theorem to calculate probabilities, assuming feature independence.

**Mathematical Example** based on search result[5]:
For classifying car theft likelihood based on color and type:

1. Prior probabilities: P(Stolen=Yes) = 0.3, P(Stolen=No) = 0.7
2. Likelihood for a red SUV:
   - P(Red|Stolen=Yes) = 0.4, P(Red|Stolen=No) = 0.6
   - P(SUV|Stolen=Yes) = 0.4, P(SUV|Stolen=No) = 0.3
3. Posterior probability calculation:
   - P(Stolen=Yes|Red,SUV) ∝ P(Stolen=Yes) × P(Red|Stolen=Yes) × P(SUV|Stolen=Yes)
                            = 0.3 × 0.4 × 0.4 = 0.048
   - P(Stolen=No|Red,SUV) ∝ P(Stolen=No) × P(Red|Stolen=No) × P(SUV|Stolen=No)
                           = 0.7 × 0.6 × 0.3 = 0.126
4. Normalizing: P(Stolen=Yes|Red,SUV) = 0.048/(0.048+0.126) = 0.28
5. Prediction: Not stolen (since 0.28 < 0.5)

## Candidate Elimination Algorithm

The Candidate Elimination Algorithm maintains general and specific hypothesis boundaries as it processes examples.

**Mathematical Example** based on search result[4]:
For concept learning of "EnjoySport":

1. Initialize:
   - S = {⟨∅,∅,∅,∅,∅,∅⟩} (most specific hypothesis)
   - G = {⟨?,?,?,?,?,?⟩} (most general hypothesis)

2. Processing positive example ⟨Sunny,Warm,Normal,Strong,Same,Yes⟩:
   - Update S to match this example: S = {⟨Sunny,Warm,Normal,Strong,Same,Yes⟩}
   - G remains unchanged: G = {⟨?,?,?,?,?,?⟩}

3. Processing negative example ⟨Rainy,Cold,High,Strong,Change,No⟩:
   - G is updated to exclude this negative instance:
     G = {⟨Sunny,?,?,?,?,?⟩, ⟨?,Warm,?,?,?,?⟩, ⟨?,?,Normal,?,?,?⟩, ⟨?,?,?,?,Same,?⟩}
   - S remains unchanged since it doesn't match the negative example

4. After processing all examples, S and G converge toward the target concept.

## Mean Squared Error

Mean Squared Error (MSE) measures the average squared difference between predicted and actual values.

**Mathematical Example**:
For predicted values ŷ =[3][5][2][7] and actual values y =[2][4][3][8]:
MSE = (1/n)Σ(y-ŷ)² = (1/4)[(2-3)² + (4-5)² + (3-2)² + (8-7)²] = (1/4)[1 + 1 + 1 + 1] = 1

## Types of Distances in DS

Distance metrics measure similarity between data points, with common types including Euclidean, Manhattan, and Minkowski.

**Mathematical Example**:
For points p = (1,2,3) and q = (4,5,6):
- Euclidean distance: d = √[(1-4)² + (2-5)² + (3-6)²] = √[9 + 9 + 9] = √27 = 5.2
- Manhattan distance: d = |1-4| + |2-5| + |3-6| = 3 + 3 + 3 = 9
- Minkowski distance (p=3): d = (|1-4|³ + |2-5|³ + |3-6|³)^(1/3) = (27 + 27 + 27)^(1/3) = 3

## Logistic Regression

Logistic regression predicts binary outcomes by estimating probabilities using the logistic function.

**Mathematical Example**:
For predicting diabetes based on glucose level (x):
1. Model: P(diabetes) = 1/(1+e^-(β₀+β₁x))
2. With β₀ = -4, β₁ = 0.05
3. For glucose = 140:
   P(diabetes) = 1/(1+e^-(-4+0.05×140)) = 1/(1+e^-3) = 0.95
4. For glucose = 80:
   P(diabetes) = 1/(1+e^-(-4+0.05×80)) = 1/(1+e^0) = 0.5

## Over & Under Fitting

Overfitting occurs when models learn training data too well (including noise), while underfitting happens when models are too simple to capture patterns.

**Mathematical Example**:
For data points (1,3), (2,2), (3,4), (4,4), (5,6):
- Underfitting model: y = 3.8 (flat line)
  - Training error: MSE = 2.36
- Good fit model: y = 0.7x + 1.4 (linear)
  - Training error: MSE = 0.67
- Overfitting model: y = 0.5x³ - 4.9x² + 15.4x - 10 (5th degree polynomial)
  - Training error: MSE = 0 (perfect fit)
  - Test error on new data: Much higher than linear model

## Binary Classifier & Multi-classifiers

Binary classifiers predict one of two classes, while multi-classifiers handle three or more classes.

**Mathematical Example**:
For binary email classification (spam/not spam):
- Features: x₁ = word count, x₂ = suspicious links
- Classification boundary: 2x₁ - 3x₂ + 4 = 0
- For email with x₁ = 5, x₂ = 3:
  2(5) - 3(3) + 4 = 10 - 9 + 4 = 5 > 0 → Not Spam

For multi-class classification (documents: sports, politics, entertainment):
- Using one-vs-rest approach with 3 binary classifiers:
  - Sports vs. rest: w₁x + b₁
  - Politics vs. rest: w₂x + b₂
  - Entertainment vs. rest: w₃x + b₃
- Classify to class with highest score

## Hyperplane

A hyperplane is a decision boundary that separates different classes in a feature space.

**Mathematical Example**:
In 2D space with points from two classes:
- Class A: (1,1), (2,2), (3,2)
- Class B: (2,4), (3,5), (4,4)
- Separating hyperplane: 2x - y + 0.5 = 0
- For point (2,3): 2(2) - 3 + 0.5 = 4 - 3 + 0.5 = 1.5 > 0 → Class A
- For point (3,6): 2(3) - 6 + 0.5 = 6 - 6 + 0.5 = 0.5 > 0 → Class A

## Radial Basis Function

Radial Basis Functions (RBF) measure similarity to a central point, commonly used in RBF networks and SVMs.

**Mathematical Example**:
For Gaussian RBF: φ(x) = e^(-||x-c||²/2σ²)
With center c = (2,2), σ = 1:
- For point x = (2,2): φ(x) = e^(-0/2) = 1
- For point x = (3,3): φ(x) = e^(-2/2) = 0.368
- For point x = (5,5): φ(x) = e^(-18/2) = 0.0001

## Gaussian Function

The Gaussian function is a bell-shaped curve widely used in statistics and machine learning.

**Mathematical Example**:
For 1D Gaussian: f(x) = (1/σ√2π)e^(-(x-μ)²/2σ²)
With μ = 0, σ = 1:
- f(0) = (1/√2π)e^0 = 0.399
- f(1) = (1/√2π)e^(-1/2) = 0.242
- f(2) = (1/√2π)e^(-2) = 0.054

