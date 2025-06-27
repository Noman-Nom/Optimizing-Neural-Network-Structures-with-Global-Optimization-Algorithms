# 🧠 Neural Network Hyperparameter Tuning with Particle Swarm Optimization (PSO)

This project is part of my Master's research focused on optimizing neural network architectures and hyperparameters using **global optimization algorithms**. This specific implementation applies **Particle Swarm Optimization (PSO)** to tune hyperparameters of a simple neural network on the **MNIST** dataset.

---

## 📌 Project Goals

- Implement and compare global optimization methods for neural networks.
- Focus on PSO, Bayesian Optimization, Random Search, and others.
- Use a two-phase strategy:
  - **Exploration Phase**: Use PSO to find optimal hyperparameters.
  - **Exploitation Phase**: Retrain the best configuration for 15,000 epochs.

---

## ✅ PSO Progress Summary

### 🔍 Phase 1: Hyperparameter Tuning (Exploration)
- **Objective Function**: Minimize validation loss
- **Search Space**:
  - Learning Rate: `0.0001` to `0.1`
  - Hidden Size: `32` to `256`
  - Batch Size: `32` to `256`
- **PSO Settings**:
  - Particles: `5`
  - Iterations: `10`
  - Epochs per trial: `3`
- **Best Configuration Found**:
  - Learning Rate: `0.00934`
  - Hidden Size: `97`
  - Batch Size: `241`
  - Validation Loss: `0.3736`

### 📈 Convergence Plot:
> PSO showed smooth convergence with steady improvements in validation loss.

---

### 🔁 Phase 2: Exploitation (Training Best Config)
- **Training on Full MNIST Dataset**
- **Epochs**: 15,000  
- **Status**:
  - Trained up to 1600 epochs on Google Colab
  - Accuracy reached **99.6%**
  - Training time became a limitation on Colab (8+ hours for 1600 epochs)

---

## ⚠️ Current Challenge

Due to resource limits on Google Colab, full training is very slow. We are planning to:
- Use cloud GPU services or server for faster computation.
- Possibly introduce early stopping to avoid unnecessary training.

---

## 💾 Features Implemented

- PSO-based optimizer from scratchh
- Objective function with PyTorch
- Checkpoint saving (every 500 epochs)
- Google Drive integration for persistence
- Resume training functionality
- Training/Validation accuracy and loss tracking
- Convergence plotting

---



