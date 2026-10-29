Advanced Learning Algorithms

These notes summarize key concepts from the second course of the Machine Learning Specialization by DeepLearning.AI and Stanford Online.

1. Neural Networks

A neural network is a machine learning model composed of interconnected units called neurons. It can learn complex patterns by combining inputs, weights, biases, and activation functions.

Basic Structure

A neural network typically consists of:

- Input layer: Receives the input features.
- Hidden layers: Learn intermediate representations of the data.
- Output layer: Produces the final prediction.

Each neuron calculates a weighted sum of its inputs, adds a bias, and applies an activation function.

[
z = \mathbf{w}\cdot\mathbf{x}+b
]

[
a = g(z)
]

Here, (g) represents an activation function.

2. Activation Functions

Activation functions introduce nonlinearity, allowing neural networks to learn more complex relationships.

Common activation functions include:

- ReLU: Returns zero for negative inputs and the input itself for positive inputs.
- Sigmoid: Maps a real-valued input to a value between zero and one.
- Linear activation: Returns the input unchanged and is often used for regression outputs.

Choosing a suitable output activation depends on the prediction task.

3. Forward Propagation

Forward propagation passes input data through the network to calculate a prediction.

For each layer:

1. Calculate the weighted sum of the inputs.
2. Add the bias.
3. Apply the activation function.
4. Pass the activation to the next layer.

The final layer produces the model's output.

4. Loss Functions

A loss function measures the error for a prediction or training example.

Examples include:

- Mean squared error: Commonly used for regression.
- Binary cross-entropy: Commonly used for binary classification.
- Categorical cross-entropy: Commonly used for multiclass classification.

Training aims to find model parameters that reduce the loss across the training dataset.

5. Backpropagation

Backpropagation computes gradients of the loss with respect to the network's trainable parameters using the chain rule.

These gradients indicate how changes to weights and biases affect the loss.

An optimizer, such as gradient descent, uses the gradients to update the parameters.

The process is repeated over training iterations until the model has learned useful patterns or a stopping condition is reached.

6. TensorFlow

TensorFlow is a machine learning framework used to build, train, and evaluate models.

A typical workflow includes:

1. Prepare the training data.
2. Define the model architecture.
3. Configure the optimizer and loss function.
4. Train the model.
5. Evaluate its performance on unseen data.
6. Use the trained model to make predictions.

TensorFlow provides tools for implementing neural networks without manually calculating every gradient.

7. Multiclass Classification

Multiclass classification predicts one class from more than two possible categories.

For example, an image classifier might distinguish between cats, dogs, and birds.

A neural network can produce a score for each class. Depending on the architecture and training setup, these scores can be converted into class probabilities, such as with softmax.

The predicted class is typically the class with the highest score or probability.

8. Decision Trees

A decision tree makes predictions by splitting data according to feature values.

Each internal node represents a decision, each branch represents an outcome, and each leaf provides a prediction.

Advantages

- Easy to interpret for relatively small trees.
- Can model nonlinear relationships.
- Can work with different types of features.

Limitations

- Deep trees can overfit the training data.
- Small changes in the training data can produce a different tree.
- A single tree may have lower predictive performance than an ensemble.

9. Tree Ensembles

Ensemble methods combine multiple models to improve predictive performance or robustness.

Random Forests

A random forest combines predictions from multiple decision trees trained with variation in their training samples and feature selection.

For classification, trees commonly vote on the predicted class. For regression, their predictions are commonly averaged.

Boosted Trees

Boosting builds a sequence of models in which later models focus on errors or residual patterns from earlier models.

Gradient-boosted trees are widely used for structured or tabular datasets.

10. Bias and Variance

Bias and variance describe different sources of model prediction error.

- High bias: The model may be too simple to capture important patterns.
- High variance: The model may fit training data too closely and generalize poorly.

Model evaluation, appropriate model complexity, regularization, and suitable training procedures can help balance these issues.

11. Evaluating Model Performance

A model should be assessed on data that was not used to fit its parameters.

Common evaluation practices include:

- Splitting data into training, validation, and test sets.
- Comparing models using metrics appropriate to the task.
- Checking for overfitting and underfitting.
- Avoiding data leakage between training and evaluation.

The appropriate metric depends on the application and the cost of different errors.

12. Key Takeaways

- Neural networks learn representations through layers of interconnected neurons.
- Activation functions help networks model nonlinear relationships.
- Forward propagation calculates predictions.
- Backpropagation computes gradients for learning.
- TensorFlow provides tools for building and training models.
- Decision trees use feature-based splits to make predictions.
- Random forests and boosting combine multiple trees.
- Careful evaluation helps determine whether a model generalizes to unseen data.

13. Practical Applications

- Image classification
- Handwritten digit recognition
- Customer churn prediction
- Fraud detection
- Sales forecasting
- Tabular data classification and regression

---

These notes are a personal learning summary and will be refined as I revisit the concepts and develop independent machine learning projects.
