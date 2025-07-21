# Phase 4: Modeling

This phase applies deep learning models for arrhythmia classification using ECG scalogram images.

---

## 1. Model Training Using TensorFlow (Custom CNN)

- **Framework:** TensorFlow / Keras
- **Input:** 224x224 scalogram images (from previous phase), organized by class.
- **Model:** Custom CNN inspired by research (Mohonta architecture).
- **Process:**
  1. Load images using `image_dataset_from_directory`.
  2. Normalize images to `[0,1]`.
  3. Train the model for 10 epochs using SGD optimizer.
  4. Evaluate performance on test data.
  5. Save the trained model and training history.

---

## 2. Model Training Using PyTorch (AlexNet)

- **Framework:** PyTorch
- **Input:** 227x227 scalogram images (resized), organized by class.
- **Model:** Pre-trained AlexNet with output layer adjusted for arrhythmia classes.
- **Process:**
  1. Load images with `ImageFolder` and DataLoader.
  2. Use standard data transforms and normalization.
  3. Train AlexNet for 10 epochs using Adam optimizer.
  4. Evaluate performance on validation and test sets.
  5. Save the trained model and training history.

---

## Results

Both models can be used to classify ECG signals into arrhythmia classes.  
Model performance (accuracy, loss) is tracked and saved for comparison and further analysis.

---

**Note:**  
All images must be organized into `training`, `validation`, and `testing` folders by class for both frameworks.


