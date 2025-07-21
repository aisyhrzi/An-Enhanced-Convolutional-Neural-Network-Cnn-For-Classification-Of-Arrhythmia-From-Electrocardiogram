# Phase 3: Data Balancing

This phase addresses class imbalance in the ECG dataset using different resampling techniques: SMOTE, SMOTEENN, and SMOTE + Tomek Links.

## Methods

- **SMOTE**: Synthetic Minority Oversampling Technique to generate new samples for minority classes.
- **SMOTEENN**: Combination of SMOTE oversampling and Edited Nearest Neighbours (ENN) undersampling.
- **SMOTE + Tomek Links**: Combination of SMOTE and removal of Tomek links to clean overlapping class boundaries.

## Scripts

- `smote.py`: Balances the dataset using SMOTE only.
- `smoteenn.py`: Balances the dataset using SMOTEENN.
- `smotetomek.py`: Balances the dataset using Tomek Links + SMOTE .

Each script:
1. Loads the denoised and labeled ECG segments.
2. Removes invalid labels (`-1`).
3. Applies the selected balancing method.
4. Saves the balanced dataset as a new CSV file.
5. Prints the new class distribution.

---

**Output:**  
Balanced ECG dataset ready for model training, with improved representation of minority arrhythmia classes.

