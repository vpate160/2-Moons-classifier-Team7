## What We're Doing

This assignment focuses on building a *neural network classifier* to differentiate between two half-moon shaped datasets using PyTorch.

## The Problem

We have a dataset with two classes that resemble two crescents facing each other. A simple straight line cannot separate them. We need a neural network capable of learning the curved decision boundary.

## Our Approach

### 1. *Build the Model*
• Create a simple Multi-Layer Perceptron (MLP) with 2 inputs, 16 hidden neurons, and 1 output.  
• Use ReLU activation in the hidden layer and Sigmoid for the output.  
• Total parameters: only 65!  

### 2. *Train the Model*
• Use Adam optimizer with a learning rate of 0.001.  
• Binary Cross-Entropy loss function.  
• Train for 2000 epochs.  
• Split the data into 80% for training and 20% for validation.  

## Files Included

• *nonlinear_classification.ipynb* - Training the classifier with a validation split.  
• *optimizer_comparison.ipynb* - Compares 5 optimizers (Adam, SGD, RMSprop, AdamW, Adagrad).

### Documentation
• *README.md* - This file provides an overview of the project.  
• *QUICK_REFERENCE.md* - Quick lookup for all metrics and results.  

## Key Results

### Training Performance (from *nonlinear_classification.ipynb*)
• *Training Accuracy*: 95.16%  
• *Validation Accuracy*: 98.75%  
• *Convergence*: Reached 95% accuracy in 1569 epochs.  
• *Final Loss*: Training 0.1157, Validation 0.0821.  

### Optimizer Comparison (from *optimizer_comparison.ipynb*)
We tested 5 optimizers and their validation accuracies:  
• *Adam*: 98.75%  (Selected)  
• *AdamW*: 98.75%  
• *SGD*: 100.00%  
• *RMSprop*: 100.00%  
• *Adagrad*: 96.88%  

## Why Adam Optimizer?

We chose *Adam* even though SGD and RMSprop achieved 100% validation accuracy for several reasons:  
• *Generalization*: 100% on small validation sets (160 samples) may suggest overfitting.  
• *Stability*: Adam showed smooth and consistent convergence.  
• *Reliability*: It is better suited for real-world situations with new data.  
• *Industry Standard*: It is the most commonly used optimizer in deep learning.  
• *Test Performance*: Our final test accuracy of 95.50% supports this choice.
