# **Evaluating MLP Performance Across Tasks**  

This repository is dedicated to exploring the performance of Multilayer Perceptrons (MLPs) across various machine learning tasks and comparing them against alternative models such as Random Forests, Logistic Regression, and others. The focus is on understanding the strengths, limitations, and behavior of MLPs in different scenarios through quantitative and qualitative analyses.

---

## **Overview**

The repository contains implementations for evaluating MLPs and other models on diverse datasets. Key highlights include:  
- Comparative analysis of model performance using metrics like F1-score, accuracy, confusion matrices, and decision surfaces.  
- Regularization techniques (L1 and L2) for MLPs to study their impact on model generalization and feature importance.  
- Feature engineering and non-linear transformations to adapt simpler models for complex tasks.  
- Visualization of learned feature embeddings (e.g., using t-SNE) to understand representation learning.

---

## **Key Features**

### **1. Model Implementations**  
- **MLP**: Baseline implementation with configurable architectures and activation functions.  
- **MLP with Regularization**: Evaluates the effects of L1 and L2 penalties on sparsity, smoothness, and overfitting.  
- **Alternative Models**: Logistic Regression, Random Forest, and others for benchmarking.  

### **2. Datasets**  
- Tasks include standard classification datasets like MNIST and synthetic datasets such as XOR, with the flexibility to add more tasks in the future.  

### **3. Visualization Tools**  
- **t-SNE**: Visualizes embeddings from MLP layers to evaluate feature representations for trained and untrained models.  
- **Decision Surfaces**: Illustrates model decision boundaries for intuitive comparisons.  
- **Confusion Matrices**: Identifies patterns in misclassification.  

### **4. Extensibility**  
The repository is structured to allow easy addition of new tasks, datasets, and model comparisons.

---


## **Results and Observations**

### **General Observations**  
- **MLPs**: Strong performance in capturing complex patterns but require careful tuning of architecture and regularization.  
- **Regularization**: L1 promotes sparsity, while L2 enhances smoothness and generalization.  
- **Alternative Models**: Logistic Regression and Random Forests provide competitive benchmarks but may struggle with non-linear patterns without feature engineering.

### **Visual Insights**  
- Decision boundaries and t-SNE plots highlight how MLPs and other models learn task-specific representations.  
- Regularized models show distinct behavior in handling overfitting and feature importance.

---
