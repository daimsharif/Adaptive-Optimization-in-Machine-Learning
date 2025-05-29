# Adaptive Optimization in Machine Learning

This repository contains the final project for the CS7CS2: Optimisation for Machine Learning course at Trinity College Dublin for MSc in Computer science. The assignment investigates the use of Polyak's adaptive step size in mini-batch stochastic gradient descent (SGD), comparing its performance with constant step size SGD and Adam across various learning scenarios.

---
## 📄 Full Report

View the full technical report:

👉 [final_assignmentOA_report.pdf](./final_assignmentOA_report.pdf)

## 📌 Project Overview

The core goal is to evaluate the theoretical and practical behavior of adaptive step-size methods (PolyakSGD, PolyakAdam) under different settings:

- Convex regression (e.g., quadratic functions)
- Noisy linear regression
- Non-convex landscapes (two-well function)
- Realistic deep learning: Transformer model on child speech dataset

The project benchmarks optimizer behavior on convergence speed, stability, and sensitivity to batch size and gradient noise.

---

## 🧠 Key Experiments

| Scenario                     | Objective                                                   | Optimizers Tested                        |
|-----------------------------|-------------------------------------------------------------|------------------------------------------|
| Quadratic Regression        | Validate Polyak step-size convergence                       | PolyakSGD, Constant SGD                  |
| Noisy Linear Regression     | Compare optimizer stability under increasing noise          | PolyakSGD, Constant SGD                  |
| Two-Well Non-convex Loss    | Evaluate escape from local minima                          | PolyakSGD, Constant SGD                  |
| Transformer Speech Model    | Real-world generalization and convergence comparison        | PolyakSGD, Constant SGD, Adam            |
| PolyakAdam Experiment       | Combine Polyak with Adam momentum and analyze performance   | PolyakAdam, Adam, PolyakSGD, SGD         |

---


## 📂 Repository Structure

```text
/ (root)
├── final_assignmentOA_report.pdf     # Report (includes methodology and analysis)
├── exam_2025.pdf                     # Assignment specification
├── final_code.ipynb                  # Final PyTorch codebase (optimizers + plots)
├── OAfinal1d.ipynb                   # Transformer experiments (Q1d)
```


---

## ⚙️ Technologies & Tools

- **Python** (3.10+)
- **PyTorch** (optimizer subclassing)
- **Matplotlib**, **Seaborn**, **NumPy** for analysis and visualization
- **Jupyter Notebook** for reproducibility

---

## 📈 Key Findings

- PolyakSGD shows rapid convergence in low-noise, small-batch settings but suffers from step-size instability in high-noise scenarios.
- Adam performs robustly under noise and high-dimensional models like transformers.
- PolyakAdam's double adaptivity leads to erratic behavior in noisy conditions and underperforms others.
- In non-convex tasks, stochasticity (via small batches) is essential for escaping local minima.


---

---

## 🤝 Acknowledgments

Project submitted as part of MSc Computer Science (Data Science Strand) coursework at **Trinity College Dublin**.

Author: Daim Sharif
