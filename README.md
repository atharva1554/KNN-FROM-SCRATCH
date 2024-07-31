# K-Nearest Neighbors (KNN) From Scratch

## Overview

This repository contains an implementation of the K-Nearest Neighbors (KNN) algorithm from scratch. KNN is a simple yet powerful machine learning algorithm used for classification and regression tasks. This project demonstrates the algorithm's core principles and provides a step-by-step implementation to help understand its inner workings.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Algorithm](#algorithm)
- [Usage](#usage)
- [Results](#results)
- [Installation](#installation)
- [Contributing](#contributing)
- [License](#license)

## Introduction

K-Nearest Neighbors (KNN) is a non-parametric, instance-based learning algorithm used for classification and regression. It classifies a data point based on the majority label of its `k` nearest neighbors or predicts a value by averaging the values of its nearest neighbors. This project implements KNN from scratch to help users understand how the algorithm works without relying on pre-built libraries.

## Project Structure

```
KNN-FROM-SCRATCH/
│
├── data/               # Dataset files
├── notebooks/          # Jupyter notebooks for analysis and testing
├── src/                # Source code for KNN implementation
│   ├── knn.py          # KNN implementation
│   └── utils.py        # Utility functions
├── results/            # Output results such as visualizations and reports
├── images/             # Images used in the project and README
├── README.md           # Project README file
└── requirements.txt    # List of dependencies
```

## Algorithm

The KNN algorithm involves the following steps:

1. **Calculate Distances**: Compute the distance between the test data point and all other data points in the training set.
2. **Sort Distances**: Sort the distances in ascending order.
3. **Select Neighbors**: Choose the `k` nearest neighbors based on the sorted distances.
4. **Vote or Average**: For classification, use the majority vote of the `k` nearest neighbors to assign a class label. For regression, calculate the mean of the `k` nearest neighbors' values.

## Usage

To use the KNN implementation, follow these steps:

1. **Import the KNN Class**:
   ```python
   from src.knn import KNN
   ```

2. **Initialize the KNN Model**:
   ```python
   model = KNN(k=3)
   ```

3. **Fit the Model**:
   ```python
   model.fit(X_train, y_train)
   ```

4. **Make Predictions**:
   ```python
   predictions = model.predict(X_test)
   ```

5. **Evaluate the Model**:
   ```python
   accuracy = model.score(X_test, y_test)
   print(f'Accuracy: {accuracy}')
   ```

## Results

The performance of the KNN algorithm is evaluated using various metrics such as accuracy, precision, recall, and F1-score. Visualizations, such as decision boundaries and error analysis, are included in the `results/` directory.

## Installation

To set up this project locally, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/atharva1554/KNN-FROM-SCRATCH.git
   ```

2. Navigate to the project directory:
   ```sh
   cd KNN-FROM-SCRATCH
   ```

3. Create a virtual environment and activate it (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```

4. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Contributing

We welcome contributions to this project. If you have suggestions for improvements, new features, or bug fixes, please open an issue or submit a pull request. For major changes, please discuss them with us first.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
