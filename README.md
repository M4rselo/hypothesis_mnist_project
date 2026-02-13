# MNIST: From Linear Models to Regularized Neural Networks

This project explores how increasing model capacity influences performance on an image classification task, and how regularization helps control overfitting.

Rather than focusing solely on achieving the highest accuracy, the primary goal was to understand **why models behave the way they do**.

---

## Project Goals

- Build a strong linear baseline  
- Analyze the impact of hidden layers  
- Investigate overfitting and generalization  
- Evaluate the effect of dropout  
- Compare activation functions  
- Study how model capacity influences learning  

The project emphasizes experimentation and interpretation over blindly improving metrics.

---

## Models Implemented

- **Linear Classifier** — establishes a baseline and highlights the limitations of linear decision boundaries  
- **MLP (Non-regularized)** — demonstrates how additional capacity improves performance but increases overfitting risk  
- **Regularized MLP** — uses dropout to stabilize training and improve generalization  

---

## Key Observations

- Linear models perform surprisingly well but fail to capture non-linear patterns.
- Hidden layers significantly improve accuracy.
- Larger models do not automatically generalize better.
- Dropout reduces the generalization gap, even when peak accuracy is slightly lower.
- ReLU converges faster than Tanh in this setting.

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

A natural next step is exploring **Convolutional Neural Networks**, which are specifically designed for image data and should outperform fully connected architectures both in efficiency and generalization.

---

## Takeaway

Better models are rarely created by blindly increasing complexity — they emerge from careful experimentation and understanding the trade-offs between flexibility and generalization.
