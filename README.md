# Deep Learning From Scratch – Logistic Regression to Deep Neural Networks (NumPy)
Project Overview

This project explores the progression from linear models to deep neural networks, implemented entirely from scratch using NumPy, without high-level ML frameworks.

The goal was to understand how learning algorithms evolve when handling datasets of increasing complexity.

Datasets Used

Synthetic Blobs Dataset (Linearly Separable)

Low-dimensional dataset (2D/3D features)

Classes separable using a linear boundary

Used to validate basic classification algorithms

Circles Dataset (Non-Linearly Separable)

Requires non-linear decision boundaries

Demonstrates limitations of linear models

EMNIST Letters Dataset (H vs Y classification)

28×28 grayscale handwritten images

Converted to binary classification

Flattened into 784-dimensional feature vectors

Real-world, high-dimensional dataset

Phase 1 – Logistic Regression

I began with Logistic Regression, a linear classifier trained using gradient descent.

Why Logistic Regression?

Simple and interpretable baseline

Works well when data is linearly separable

Good starting point for understanding gradient-based optimisation

Observations

Achieved high accuracy on blobs dataset

Performed poorly on circles dataset due to non-linear structure

This revealed a major limitation:

Linear models cannot capture complex, non-linear patterns.

Phase 2 – Neural Network (1 Hidden Layer)

To overcome linear limitations, I implemented a feedforward neural network with:

1 hidden layer

Backpropagation from scratch

Stochastic Gradient Descent

Architecture

Hidden Layer Activation: tanh

Chosen because it is zero-centered

Helps gradient flow better than sigmoid

Output Layer Activation: sigmoid

Suitable for binary classification

Produces probability values between 0 and 1

Why Neural Networks?

Neural networks introduce non-linearity, enabling:

Learning curved decision boundaries

Solving non-linearly separable problems (e.g., circles dataset)

This significantly improved performance on the circles dataset.

Phase 3 – Deep Neural Network (Arbitrary Layers)

In Task 5, I extended the architecture to support:

An arbitrary number of hidden layers

Different number of nodes per layer

Configurable architecture via layer lists (e.g., [784, 64, 32, 1])

Deep Architecture

Hidden Layers: tanh activation

Output Layer: sigmoid activation

Loss Function: Binary Cross-Entropy (Log Loss)

Optimisation: Gradient Descent

Regularisation: L2 Weight Decay

Overfitting Prevention: Early Stopping

Why Deep Neural Networks?

As the input dimensionality increased (EMNIST with 784 features), deeper networks:

Learn hierarchical representations

Capture more complex feature interactions

Improve generalisation compared to shallow networks

Deep networks also allowed experimentation with:

Different layer depths

Regularised vs non-regularised models

Performance comparisons via training curves

Overfitting Prevention Techniques

Since EMNIST subset was relatively small:

Implemented L2 Regularisation (Weight Decay)

Implemented Early Stopping using validation accuracy

This reduced overfitting and improved generalisation on the test set.

Evaluation Strategy

70 / 15 / 15 Train–Validation–Test split

Hyperparameter tuning (learning rate, hidden units)

Compared:

Logistic Regression

1 Hidden Layer NN

Multi-layer Deep NN

With vs Without Regularisation

Visualised:

Training loss curves

Predicted vs True class distributions

Core Algorithms Used

Logistic Regression (Linear Classification)

Feedforward Neural Networks

Backpropagation

Gradient Descent Optimisation

L2 Regularisation

Early Stopping

Tools & Libraries

Python

NumPy (matrix operations, manual neural network implementation)

Matplotlib (visualisation)

scikit-learn (dataset generation: blobs, circles)

Jupyter Notebook / VS Code

Key Takeaways

Understood the mathematical foundation of neural networks by implementing backpropagation manually.

Demonstrated progression from linear to non-linear to deep architectures.

Explored generalisation and overfitting control techniques.

Built a flexible deep learning framework without using TensorFlow or PyTorch.
