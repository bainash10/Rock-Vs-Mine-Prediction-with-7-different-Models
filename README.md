In this project, I evaluated multiple machine learning models on the Sonar dataset to classify objects as either **rock** or **mine** using different train-test splits (90%-10%, 80%-20%, and 70%-30%). The models used were:

1. **Logistic Regression**
2. **Support Vector Classifier**
3. **Decision Tree Classifier**
4. **Random Forest Classifier**
5. **Gradient Boosting Classifier**
6. **Extra Trees Classifier**
7. **K-Nearest Neighbors (KNN)**

I assessed each model based on **Accuracy**, **Precision**, **Recall**, and **F1 Score** to determine their performance.

---

## 1. My Observations on Model Performance

- **Random Forest Classifier** delivered the most consistent and best overall performance across all data splits. It maintained high **Accuracy**, **Precision**, and **F1 Score**, proving to be both reliable and robust.
  
- **Gradient Boosting Classifier** also performed very well, especially in terms of **Precision**, where it consistently scored 1.000. However, it showed slightly lower **Recall**, specifying that it might miss some positive cases.

- **Support Vector Classifier** had excellent **Precision** but a drop in **Recall**, specifying that it favors precision over identifying all positive cases.

- **Logistic Regression** performed reasonably well, showing improvement with a larger training set (80%-20%). It’s simpler and more interpretable, but not as powerful as the tree-based models in this case.

- **Decision Tree** and **K-Nearest Neighbors** were the weakest performers overall. Their metrics lagged behind the other models, especially when I used less training data.

---

## 2. Impact of Train-Test Splits

- Increasing the training data from 70% to 80% helped most models improve their performance. For instance, **Logistic Regression** saw noticeable gains in **F1 Score** and **Accuracy** with the 80%-20% split compared to 90%-10%.

- **Random Forest** remained stable and strong regardless of the split, showcasing its robustness.

- A smaller training size (70%) generally led to lower performance, especially in models that depend more on data coverage like **KNN** and **Logistic Regression**.

- Among the different splits, the **80%-20% split** provided the best balance of training data size and testing effectiveness. This split allowed for enough data to train the models adequately while also providing a sufficiently large test set to evaluate performance reliably.

---

## 3. My Ranking of the Models

1. **Random Forest Classifier** – Best balance of accuracy, precision, recall, and F1 score. Very consistent.
2. **Gradient Boosting Classifier** – Excellent precision, slightly lower recall.
3. **Support Vector Classifier** – High precision, moderate overall performance.
4. **Logistic Regression** – Decent results, great for interpretability.
5. **KNN & Decision Tree** – Lower reliability and performance in this dataset.

---

## 4. Final Takeaways

Based on my experiments:
- I would **recommend Random Forest Classifier** for this classification task due to its strong overall performance.
- If precision is the top priority (e.g., reducing false positives), **Gradient Boosting** would be a solid alternative.
- **Logistic Regression** is a good lightweight option when simplicity and speed are more important than accuracy.
- **KNN** and **Decision Tree** might be useful for quick experiments, but I wouldn’t rely on them for production deployment on this dataset.

---

Overall, this project helped me understand how different classifiers behave with varying data splits and feature distributions. It also reinforced the strength of ensemble models in handling real-world classification problems effectively. The **80%-20% train-test split** proved to be the most effective for the models tested in this project.

**Developed by:** Nischal Baidar
