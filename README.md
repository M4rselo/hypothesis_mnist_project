# MNIST: From Linear Models to Regularized Neural Networks

This project investigates the impact of regularization techniques, model capacity and activation activation functions on image classification performance, using the MNIST dataset.
Furthermore, during this project we compare Linear Models to Multi-Layer-Perceptrons to analyze how architectural complexity and hyperparamaters shifts influence learning.

Rather than focusing solely on achieving the highest accuracy, the primary goal was to understand **why models behave the way they do**.

---

## Project Goals

- Build a strong linear baseline
- Analyze falsely predicted labels
- Compare linear baseline to MLP  
- Analyze the impact of hidden layers  
- Investigate overfitting and generalization  
- Evaluate the effect of dropout  
- Compare activation functions (Tanh/ReLU) 
- Study how model capacity influences learning  

The project emphasizes experimentation and interpretation over blindly improving metrics.

---

## Models Implemented

- **Linear Classifier** — establishes a baseline and highlights the limitations of the linear model
- **MLP (Non-regularized)** — demonstrates how additional capacity improves performance but increases overfitting risk  
- **Regularized MLP** — uses dropout to stabilize training and improve generalization  
- **Others** - all of the models implemented duting this project
---

## Key Observations

- Linear models provide a strong baseline, but their narrow capacity significantly limits their ability to distinguish non-linear relationships.
- Although introducing hidden layer increases the risk of overfitting, it significantly improves performnce by allowing the model to learn non-linear patterns.
- Regularization substantially improves model's stability and classification on validation set, however due to increasing training loss effect, it may slightly reduce performance leading to worse accuracy on particular examples.
- Activation functions strongly influence optimization speed, with ReLU converging faster than Tanh in this experiment.
- Increasing model capacity may negatively impact generalization, as the model begins to fit the training set more closely.
- Reducing model capacity tends to improve stability, but may slow convergence and limit overall performance (on given amount of epochs).

Overall, model performance emerged from balancing **capacity, regularization, and optimization** rather than maximizing a single parameter.

---

## Results

| Model | Test Accuracy |
|--------|--------------|
| Linear Baseline | 92.1% |
| MLP (No Regularization) | 98.1% |
| Regularized MLP | 97.9% |

---

## Technical Approach

Models were implemented in PyTorch with a custom training loop to better understand the mechanics of optimization and backpropagation.

The workflow focused heavily on controlled experiments — modifying one variable at a time to observe its effect on training dynamics.

---

## Future Work

Next is exploring **Concolutional Neural Networks**, which are specifically designed for image data, allowing the model to distinguish spacial features, patterns.

---

## Takeaway

Better models are rarely created by blindly increasing complexity — they emerge from careful experimentation and understanding the trade-offs between flexibility and generalization.
