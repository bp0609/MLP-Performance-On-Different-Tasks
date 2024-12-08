## MNIST MLP and Comparative Analysis with RF & Logistic Regression

This repository contains an end-to-end implementation of a Multilayer Perceptron (MLP) for digit classification on the MNIST dataset. It also includes a comparative analysis with Random Forest and Logistic Regression models, visualization of learned embeddings using t-SNE, and an exploratory study on the transferability of the MLP to the Fashion-MNIST dataset.
Here's a summary of the work:

### **1. Dataset Preparation**
- **MNIST Dataset**: The original MNIST dataset consists of 60,000 training images and 10,000 test images. Due to compute limitations, we used a stratified subset of the training data while retaining the full 10,000 test images for evaluation. 
- **Preprocessing**: Images were normalized to ensure consistent model performance.

### **2. Models Implemented**
- **Multilayer Perceptron (MLP)**:
  - Architecture: 
    - First hidden layer: 30 neurons
    - Second hidden layer: 20 neurons
    - Output layer: 10 neurons (corresponding to the 10 digit classes)
  - Activation: ReLU for hidden layers, softmax for the output layer.
  - Training: Optimized using Adam optimizer with categorical cross-entropy loss.
- **Random Forest (RF)**:
  - Hyperparameters: Tuned to balance performance and computational efficiency.
- **Logistic Regression**:
  - Multi-class classification using one-vs-rest scheme.

### **3. Performance Comparison**
- Metrics:
  - **F1-Score**: Used to assess classification accuracy, considering both precision and recall.
  - **Confusion Matrix**: Visualized to identify commonly confused digit pairs.
- Observations:
  - The MLP outperformed RF and Logistic Regression on most metrics.
  - Digits such as "4" and "9", and "3" and "5" were frequently confused across models, indicating their close visual similarity.

### **4. t-SNE Visualization**
- For the trained MLP, we extracted the activations from the second hidden layer (20 neurons) for t-SNE visualization. The results were contrasted against:
  1. **Trained Model**: Clear clusters emerged for each digit, demonstrating effective feature learning.
  2. **Untrained Model**: The embeddings were random and lacked discernible clusters, highlighting the importance of training for meaningful representation learning.
- Conclusion: Training significantly enhances the model's ability to learn distinct representations, as evidenced by well-separated clusters in the t-SNE plots.

### **5. Cross-Dataset Prediction**
- **Fashion-MNIST Predictions**: The trained MLP, despite being trained on MNIST, was tested on the Fashion-MNIST dataset to examine transfer learning potential.
  - Observations:
    - The model performed poorly, confirming limited transferability due to the vastly different nature of the datasets.
    - Confusion among Fashion-MNIST classes was high, emphasizing the need for dataset-specific training.
- **t-SNE Visualization for Fashion-MNIST**:
  - The embeddings from the second layer showed less distinct clustering compared to MNIST, reflecting the MLP's inability to generalize to unseen image distributions.

### **6. Conclusion**
- The MLP demonstrated strong performance on MNIST, with meaningful embeddings in the hidden layers. 
- Cross-dataset performance revealed the importance of training on relevant data for effective predictions. 
- t-SNE visualizations highlighted the stark differences in learned feature representations between trained and untrained models and between MNIST and Fashion-MNIST datasets.

Explore the code and detailed results in this repository to dive deeper into the implementation and findings!