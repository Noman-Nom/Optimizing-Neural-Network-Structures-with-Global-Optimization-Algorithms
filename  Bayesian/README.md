# Neural Network Hyperparameter Optimization

## Objective
To optimize the hyperparameters of a neural network using **Bayesian Optimization** and evaluate the final model's performance on the MNIST dataset.

## Steps Taken
1. **Started with Bayesian Optimization:**
   - Defined the search space for hyperparameters:
     - Learning rate: `[0.0001, 0.1]`
     - Hidden size: `[32, 256]`
     - Batch size: `[32, 256]`
   - Ran the algorithm for **20 iterations** to find the best hyperparameters.

2. **Best Hyperparameters Found:**
   - Learning rate: `0.00494`
   - Hidden size: `256`
   - Batch size: `132`

3. **Trained the Final Model:**
   - Used the best hyperparameters to train a simple feedforward neural network on the MNIST dataset.
   - Trained for **10 epochs**.

4. **Evaluated the Model:**
   - Tested the model on the MNIST test set to measure its performance.

## Results
- **Training Performance:**
Epoch [1/10], Loss: 0.1234, Accuracy: 96.50%
Epoch [2/10], Loss: 0.1680, Accuracy: 94.86%
Epoch [3/10], Loss: 0.1345, Accuracy: 95.91%
Epoch [4/10], Loss: 0.1203, Accuracy: 96.29%
Epoch [5/10], Loss: 0.1084, Accuracy: 96.66%
Epoch [6/10], Loss: 0.1051, Accuracy: 96.78%
Epoch [7/10], Loss: 0.0953, Accuracy: 97.08%
Epoch [8/10], Loss: 0.0958, Accuracy: 97.07%
Epoch [9/10], Loss: 0.0908, Accuracy: 97.21%
Epoch [10/10], Loss: 0.0860, Accuracy: 97.36%

- **Test Performance:**
Test Loss: 0.1431
Test Accuracy: 96.48%


## Conclusion
- Bayesian Optimization successfully found hyperparameters that resulted in a **test accuracy of 96.48%**.
- The model achieved a **training accuracy of 97.36%** after 10 epochs.
- The results show that Bayesian Optimization is effective for hyperparameter tuning in neural networks.

---


