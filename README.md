# k-Nearest Neighbours (kNN) and Decision Trees

## About

This project aims to apply and evaluate two machine learning algorithms, kNN and Decision Trees, on the Iris dataset. The performance of both algorithms is assessed in terms of
accuracy, providing insights into their effectiveness in classifying Iris flowers.

## kNN Algorithm

A kNN algorithm classifies a data point by considering the majority class among its k-nearest neighbours. Euclidean distance is often used to measure similarity.

This kNN algorithm is designed to take the training data (`X_train`, `y_train`) and apply the kNN algorithm to predict labels for the test set (`X_test`). The `kNN_predict` function calculates the Euclidean distance between a test point and all training points. The labels of the k-nearest neighbours are then considered, and the most common label is assigned to the test point.

## Decision Trees Algorithm

A Decision Trees algorithm recursively splits the dataset based on feature values, creating a tree-like structure for decision-making. Decision Trees are trained using a dataset's features and labels, and they make decisions by traversing the tree from the root to a leaf node.

This Decision Trees algorithm is employed using the `scikit-learn` library. The `DecisionTreeClassifier` class is used to create the model, and the model is trained on the training set (`X_train`, `y_train`) using the `fit` method. Predictions for the test set are generated using the `predict` method.

## Results

The accuracy scores of the kNN and Decision Trees algorithms are calculated using the `accuracy_score` function from the sklearn.metrics module. The program was run 10 times with 10 different sets of data, and the results are shown below.

| **Test**    | **kNN Accuracy** | **Decision Trees Accuracy** |
| ----------- | ---------------- | --------------------------- |
| 1           | 1.0              | 0.96                        |
| 2           | 0.96             | 0.96                        |
| 3           | 1.0              | 0.96                        |
| 4           | 1.0              | 0.86                        |
| 5           | 0.93             | 0.93                        |
| 6           | 0.96             | 0.93                        |
| 7           | 0.96             | 0.93                        |
| 8           | 0.96             | 0.93                        |
| 9           | 0.96             | 0.9                         |
| 10          | 0.96             | 0.86                        |
| **Average** | **0.969**        | **0.922**                   |

## Evaluation

The kNN algorithm achieved an average accuracy score of 96.9%. The high accuracy implies that the kNN model effectively captures the underlying patterns in the Iris dataset and makes accurate predictions for the test set.

The Decision Trees algorithm, on the other hand, obtained an average accuracy score of 92.2%. The slightly lower accuracy may suggest that the decision boundaries within the dataset are not completely accurate, which led to some incorrect predictions for the test set.

## Conclusion

In conclusion, both the kNN and Decision Trees algorithm performed well in classifying Iris flowers. The implemented kNN algorithm, with an accuracy of 96.9%, made precise predictions based on the training data. The Decision Trees algorithm, with an accuracy of 92.2%, was proven to be less suitable for the dataset. The findings emphasise the importance of algorithm selection based on the specific characteristics of the dataset.

## References

1. Sklearn.datasets.load_iris. scikit. (n.d.-a). https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html
2. Sklearn.tree.decisiontreeclassifier. scikit. (n.d.-b). https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html
