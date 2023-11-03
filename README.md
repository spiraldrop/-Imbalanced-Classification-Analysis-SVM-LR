# Imbalanced-Classification-Analysis-SVM-LR

# Project README

This is a concise README for a project worked on in a Jupyter Notebook. It provides a brief overview of the project and highlights the tasks completed. Below, you will find the code and visualizations for the tasks.

## Tasks Overview

### Task 1: Applying SVM

In this task, we observed how linear models work when dealing with imbalanced data. Four datasets with varying class imbalances were created. We applied Support Vector Machine (SVM) and Logistic Regression (LR) with different regularization strengths (C values - 0.001, 1, 100) to these datasets.

#### Hyperplane Plots

For each dataset and C value, we visualized the hyperplane created by the SVM model. We also considered different learning rates. In the plots, the support vectors are represented in different colors. These visualizations help understand the position of the hyperplane in the presence of class imbalance.

### Task 2: Applying LR

In this task, we repeated the same experiments conducted in Task 1.1, but instead of SVM, we applied Logistic Regression. We visualized the hyperplanes created by Logistic Regression for the given datasets and C values (0.001, 1, 100).

## Code and Visualizations

For the detailed code and visualizations, please refer to the Jupyter Notebook:

- 8A_LR_SVM.ipynb

The notebook contains code, plots, and observations from the experiments conducted on imbalanced datasets using SVM and LR.

### Hyperplane Plots

Below, you can find a representative example of the hyperplane plots from Task 1:

```
# Hyperplane plot for SVM
model = SVC(C=0.001, kernel='linear')
X_p = np.random.normal(0, 0.05, size=(i[0], 2))
X_n = np.random normal(0.13, 0.02, size=(i[1], 2))
y_p = np.array([1] * i[0]).reshape(-1, 1)
y_n = np.array([0] * i[1]).reshape(-1, 1)
X = np.vstack((X_p, X_n))
y = np.vstack((y_p, y_n))
model.fit(X, y)
plt.scatter(X_p[:, 0], X_p[:, 1])
plt.scatter(X_n[:, 0], X_n[:, 1], color='red')
plt.title('C = ' + str(c[k]) + str(i))
draw_line(coef=model.coef_[0], intercept=model.intercept_, ma=max(X[:, 1]), mi=min(X[:, 1]))
plt.show()
```

Please explore the notebook for more details.

### Observations
The observations and insights from the experiments are recorded in the Jupyter Notebook, along with the code and visualizations. Please refer to the notebook for a comprehensive understanding of the results.

Enjoy exploring the project!
