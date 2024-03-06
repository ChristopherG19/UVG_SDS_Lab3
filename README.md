# Malware Detection Project

This project aims to develop a dynamic malware detection system using machine learning techniques. The focus is on analyzing the behavior of malware based on the order of function calls from different executables. Two models are developed for malware detection: a Multilayer Perceptron (MLP) neural network and a Support Vector Machine (SVM).

> **Note:**  
> This README summarizes the project and the code employed for dynamic malware detection using machine learning techniques. For more details, refer to the paper by Maniriho et al. referenced at the end. 📖

## Dataset
The dataset used in this project contains function call sequences from various executables, along with their corresponding labels indicating whether they are malicious or benign.

## Preprocessing
- The dataset is loaded, and an exploratory analysis is performed to understand its structure and characteristics.
- Categorical labels are encoded using LabelEncoder to transform them into numerical values.
- StandardScaler is applied to scale the feature data.
- The dataset is split into training and testing sets.


## Models
1. **Multilayer Perceptron (MLP) Neural Network**
   - A sequential model with multiple dense layers is built using TensorFlow/Keras.
   - The model is compiled with the Adam optimizer and binary cross-entropy loss function.
   - It is trained on the training data and evaluated on the testing data.
   - Performance metrics such as accuracy, precision, recall, and ROC AUC are calculated.

2. **Support Vector Machine (SVM)**
   - An SVM model with a radial basis function (RBF) kernel is employed.
   - The model is trained and evaluated using the training and testing data.
   - Accuracy, precision, recall, and ROC AUC are computed as performance metrics.

## Cross-Validation
K-fold cross-validation with k=10 is implemented to assess the generalization performance of both models. StratifiedKFold is used to ensure balanced class distribution in each fold.

## Conclusion
After comparing the performance of the MLP neural network and SVM models, it is observed that the MLP neural network generally outperforms the SVM model in terms of accuracy, precision, recall, and ROC AUC. These results suggest that the MLP neural network may be preferable for dynamic malware detection based on function calls from different executables.

## Reference
Maniriho, P., Mahmood, A. N., & Chowdhury, M. J. M. (2022). MalDetConv: Automated Behaviour-based Malware Detection Framework Based on Natural Language Processing and Deep Learning Techniques. arXiv (Cornell University). [https://doi.org/10.48550/arxiv.2209.03547](https://doi.org/10.48550/arxiv.2209.03547)


