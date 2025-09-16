# MsDS-deep-learing-cnn-cancer-detection

## **Objective**
The goal of this project was to develop and evaluate a Convolutional Neural Network (CNN) for the binary classification of histopathologic images, specifically to detect the presence of metastatic cancer in image patches from the PatchCamelyon (PCam) dataset.

## **Methodology**
The solution was implemented in a Jupyter Notebook using TensorFlow and Keras.
- **Dataset:** The PCam dataset was used, which contains over 220,000 96x96 pixel color image patches for training and 57,000 for testing.
- **Preprocessing:** The data was loaded directly from a Kaggle competition source. Standard exploratory data analysis was performed to visualize the class distribution and sample images.
- **Architecture Experimentation:** 4 models were designed and tested, adding incrementally more complex functionality.
- **Final Model Architecture:** A sequential CNN was constructed with the following key layers:
  - Four Conv2D layers with increasing filter depths (32, 64, 128, 256) and relu activation.
  - MaxPooling2D layers following each convolutional block to downsample feature maps.
  - A Flatten layer to transition from convolutional to dense layers.
  - Two Dense layers, with the final output layer using a sigmoid activation function for binary classification.
- **Training and Compilation:** The model was compiled using the Adam optimizer and binary cross-entropy loss function. It was trained over a series of epochs, with performance monitored against a validation set to track generalization and prevent overfitting.
- **Subset of Training Data:** To manage computational resources and training time, each epoch was trained on a subset of 10,000 records from the full training dataset.

## **Results**
The model's performance was strong, demonstrating its effectiveness for this classification task.
- **Validation Accuracy:** The model achieved a final validation accuracy of **91.44%**.
- **Validation Loss:** The final validation loss was approximately **.2135**.
- **Epoches to Train:** 29

The training and validation curves for both accuracy and loss showed good convergence without significant signs of overfitting, confirming the model's robustness.

## **Conclusion**
The CNN model successfully classified the PCam image patches with high accuracy. The results validate the architecture and training methodology as a solid approach for this type of medical image analysis. The project serves as a practical demonstration of applying deep learning to a tangible problem in computational pathology, delivering a reliable proof-of-concept for automated cancer detection.
