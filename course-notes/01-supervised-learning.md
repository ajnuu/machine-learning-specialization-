Supervised Learning: Regression and Classification

These notes summarize key concepts I learned in the first course of the Machine Learning Specialization by DeepLearning.AI and Stanford Online.

1. What Is Supervised Learning?

Supervised learning is a machine learning approach in which a model learns from labeled training data. Each training example contains input features and a known target value.

The trained model uses patterns learned from the training data to make predictions on new examples.

Types of Supervised Learning

- Regression: Predicts a numerical value, such as a house price.
- Classification: Predicts a category, such as whether an email is spam or not spam.

2. Linear Regression

Linear regression predicts a continuous numerical output from one or more input features.

For a single feature, the model is:

[
f_{w,b}(x) = wx + b
]

Where:

- (x) is the input feature.
- (w) is the model weight.
- (b) is the bias.
- (f_{w,b}(x)) is the predicted output.

Example

A model can learn the relationship between a house's size and its price using historical housing data.

Multiple Linear Regression

When there are multiple features, the model combines them to make a prediction:

[
f_{\mathbf{w},b}(\mathbf{x}) =
\mathbf{w}\cdot\mathbf{x}+b
]

Features could include house size, number of bedrooms, and age of the property.

3. Cost Function

A cost function measures how far a model's predictions are from the actual target values.

For linear regression, the mean squared error cost function is commonly expressed as:

[
J(w,b)=\frac{1}{2m}
\sum_{i=1}^{m}
\left(f_{w,b}(x^{(i)})-y^{(i)}\right)^2
]

Where:

- (m) is the number of training examples.
- (y^{(i)}) is the actual target.
- (f_{w,b}(x^{(i)})) is the prediction.

A lower cost generally indicates better fit on the training data, but performance on unseen data also matters.

4. Gradient Descent

Gradient descent is an optimization algorithm used to adjust model parameters to reduce the cost function.

The parameter update rule is:

[
w := w-\alpha\frac{\partial J(w,b)}{\partial w}
]

[
b := b-\alpha\frac{\partial J(w,b)}{\partial b}
]

Here, (\alpha) is the learning rate, which controls the size of each update.

- A learning rate that is too small can make training slow.
- A learning rate that is too large can cause the optimization to overshoot or diverge.

5. Logistic Regression

Logistic regression is used for classification tasks. It estimates the probability that an example belongs to a particular class.

The sigmoid function is:

[
g(z)=\frac{1}{1+e^{-z}}
]

For logistic regression:

[
f_{\mathbf{w},b}(\mathbf{x})=
g(\mathbf{w}\cdot\mathbf{x}+b)
]

The output lies between 0 and 1 and can be interpreted as an estimated probability for binary classification.

A classification threshold is then used to assign a predicted class.

Example

An email classifier can estimate whether a message is spam based on features extracted from its text.

6. Overfitting and Regularization

Overfitting occurs when a model fits the training data too closely and performs poorly on new, unseen examples.

Ways to address overfitting include:

- Collecting more representative training data.
- Selecting relevant features.
- Using appropriate model complexity.
- Applying regularization.
- Evaluating performance on separate validation and test data.

Regularization penalizes overly large parameter values to help control model complexity.

7. Model Evaluation

A model should be evaluated using data that was not used to fit its parameters.

Common metrics include:

Regression

- Mean absolute error (MAE)
- Mean squared error (MSE)
- Root mean squared error (RMSE)

Classification

- Accuracy
- Precision
- Recall
- F1 score

The best metric depends on the problem and the cost of different prediction errors.

8. Key Takeaways

- Supervised learning uses labeled examples.
- Regression predicts numerical values, while classification predicts categories.
- Cost functions measure prediction error.
- Gradient descent updates parameters to reduce cost.
- Logistic regression estimates probabilities for classification.
- Regularization can help reduce overfitting.
- Evaluation on unseen data helps measure generalization.

9. Practical Applications

- House price prediction
- Spam email detection
- Customer churn prediction
- Medical image classification
- Sales forecasting

---

These notes are a personal learning summary. I will continue refining them as I revisit the concepts and build independent machine learning projects.
