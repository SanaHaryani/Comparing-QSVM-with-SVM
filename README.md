# QSVM_vs_SVM

Comparison of classical SVM and Quantum SVM using Iris dataset.

Project Overview

This project explores the application of quantum computing in machine learning by comparing Quantum Support Vector Machine (QSVM) with a traditional classical SVM using the well-known Iris dataset. The main goal is to understand how quantum feature mapping affects performance and to identify the practical constraints of quantum machine learning on small datasets.

Dataset

- Iris dataset (built-in in scikit-learn)  
- Reduced to binary classification for simplicity  
- Only two features used to make it compatible with quantum circuits.

Tools & Libraries

- Python 3.x
- scikit-learn – For classical ML Implementation.
- Qiskit Machine Learning – Quantum ML framework.
- Qiskit Aer – Quantum circuit simulator.
- Google Colab – For running the code.

Implementation

Classical SVM:

  - RBF kernel
  - Trained on 80% of the dataset
  - Tested on 20% of the dataset

Quantum SVM:

  - Features encoded using `ZZFeatureMap`
  - Quantum kernel computed via `FidelityQuantumKernel`
  - Classifier trained using scikit-learn `SVC` with quantum kernel
  - Simulated on Qiskit Aer

Both models follow identical preprocessing and evaluation steps to ensure a fair comparison.

Results

| Model | Accuracy |
 
| Classical SVM | 1.00 |
| Quantum SVM   | 0.95 |

Observations

- Classical SVM performs slightly better on this small dataset.
- QSVM demonstrates quantum feature mapping, showing potential for more complex datasets.
- Limitations include small dataset size and simulated environment.

How to Run

Install dependencies:

pip install qiskit qiskit-machine-learning scikit-learn
