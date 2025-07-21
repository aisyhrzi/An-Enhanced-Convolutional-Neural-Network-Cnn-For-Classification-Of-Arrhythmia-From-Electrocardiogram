## Phase 1: Preprocessing

This phase prepares raw ECG data for further analysis by applying denoising, segmentation, and basic visualization.

---

### 1. Import Libraries

- Import all necessary libraries for data handling (`numpy`, `pandas`), signal processing (`pywt`), plotting (`matplotlib`), and file management (`os`).

---

### 2. Plot Settings

- Configure plot style settings to ensure all ECG visualizations are clear and consistent.

---

### 3. Denoising Function

- Define the `denoise()` function using the Daubechies wavelet (`db4`).
- This function removes noise from the ECG signal, resulting in smoother and cleaner data for analysis.

---

### 4. Visualization Function

- Define the `plot_denoised_vs_original()` function to compare the original ECG signal with its denoised version.
- This function helps verify the quality of the denoising process visually.

---

### 5. Locate ECG Data Files

- Set the directory paths for both input ECG data and output results.
- List all `.csv` and `.txt` files in the dataset folder.
- Filter files to only include those matching the selected training IDs.

---

### 6. Process Each ECG File

For each ECG file:
- Read the file (skip header rows as needed).
- Extract the MLII column, which contains the primary ECG channel.
- Apply the denoising function to the extracted signal.
- Plot the original and denoised signals for quality checking.

---

### 7. Segment the Denoised Signal

- Split each denoised ECG signal into fixed-length segments (1000 samples per segment).
- Collect all segments into a list for batch processing.
  - For example, a signal with 10,000 samples will result in 10 segments.

---

### 8. Save Segmented Data

- Combine all segments into a DataFrame structure.
- Save the segmented, denoised data as new CSV files for downstream processing.

---

