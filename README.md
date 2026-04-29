# 🍄 Mushroom Edibility Classification

## ⭐ Project Highlights

- Built a neural network to classify mushrooms as edible or poisonous  
- Applied One-Hot Encoding to transform categorical features  
- Reduced dimensionality using PCA while retaining 95% variance  
- Compared model performance with and without dimensionality reduction  
- Analyzed tradeoffs between model complexity and computational efficiency  

---

## 📌 Overview

This project builds a machine learning model to classify mushrooms as edible or poisonous based on their physical characteristics. The dataset consists entirely of categorical features, making it a strong candidate for feature encoding and dimensionality reduction techniques.

The project demonstrates a full machine learning workflow, including preprocessing, neural network modeling, and performance analysis.

---

## 🎯 Objectives

- Transform categorical mushroom features into a usable numerical format  
- Train a neural network for binary classification  
- Apply dimensionality reduction using PCA  
- Compare model performance before and after PCA  
- Analyze computational and performance tradeoffs  

---

## 📊 Dataset

The dataset contains mushroom characteristics such as:

- Cap shape  
- Cap color  
- Odor  
- Gill size and spacing  
- Spore print color  
- Habitat  

Each observation is labeled as either:
- Edible  
- Poisonous  

The dataset is entirely categorical and required encoding prior to modeling.

---

## 📁 Project Structure

- notebooks/ → analysis and modeling notebook  
- data/ → raw dataset not included  
- reports/ → figures and outputs  
- src/ → reusable code (future expansion)  

---

## 🔍 Key Insights

- Mushroom classification can be performed with high accuracy using categorical features alone  
- Feature encoding significantly increases dimensionality (22 → 116 features)  
- Dimensionality reduction can preserve most information while simplifying the feature space  
- Model performance is influenced by both feature representation and architecture  

---

## 🧹 Data Preprocessing

The dataset required transformation from categorical to numerical format.

### Key steps:

- Applied One-Hot Encoding to categorical variables  
- Expanded feature space from 22 original features to 116 encoded features  
- Prepared training and testing datasets for modeling  

---

## 🤖 Modeling Approach

### Neural Network (Baseline)

A simple neural network was trained using the full One-Hot Encoded dataset.

- Input features: 116  
- Output: Binary classification (edible vs poisonous)  
- Output layer uses a single unit to represent class probability  

---

### Dimensionality Reduction with PCA

Principal Component Analysis (PCA) was applied to reduce dimensionality while retaining 95% of the dataset variance.

- Reduced features from 116 → 40  
- Simplified input space for modeling  

---

## 📈 Model Comparison

Two models were evaluated:

### 1. Original Neural Network
- Input features: 116  
- Training time: ~16.3 seconds  

### 2. PCA-Based Neural Network
- Input features: 40  
- Training time: ~17.3 seconds  

---

## 🧠 Interpretation

Although PCA significantly reduced the number of features, it did not result in faster training time. This highlights an important tradeoff:

- PCA produces dense numerical representations, which can increase computational complexity  
- The original neural network was already relatively simple  
- Reducing dimensionality does not always guarantee improved performance  

This demonstrates the importance of evaluating preprocessing techniques within the context of the specific model and dataset.

---

## ⚠️ Limitations

- Neural network architecture is relatively simple  
- No hyperparameter tuning was performed  
- PCA may not be optimal for all classification tasks  
- Dataset is synthetic and well-structured, which may not reflect real-world complexity  

---

## 🚀 Future Improvements

- Tune neural network architecture and hyperparameters  
- Test additional models (Random Forest, Gradient Boosting)  
- Explore feature importance and interpretability techniques  
- Evaluate alternative dimensionality reduction methods  

---

## 🛠 Tools & Technologies

- Python  
- Pandas / NumPy  
- Scikit-learn  
- TensorFlow / Keras  
