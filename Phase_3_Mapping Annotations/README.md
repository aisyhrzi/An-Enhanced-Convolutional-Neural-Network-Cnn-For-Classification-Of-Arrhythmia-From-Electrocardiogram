## Phase 3: Mapping Annotations

This phase assigns class labels to each segmented ECG sample based on the most frequent beat annotation present in that segment. The process follows the AAMI standard for arrhythmia classification.

---

### 1. Beat Class Definition

A function (`get_beat_class`) groups MIT-BIH annotation symbols into five classes according to the AAMI standard:

- `0`: Normal (`N`, `L`, `R`, `e`, `j`)
- `1`: Supraventricular (`S`, `A`, `J`, `a`)
- `2`: Ventricular (`V`, `E`)
- `3`: Fusion (`F`)
- `4`: Unknown (`/`, `f`, `Q`)

---

### 2. Annotation File Processing

- For each ECG record, the corresponding annotation file (`.txt`) is read.
- This file provides the sample indices and original beat types.
- The function converts each original beat label to a numeric class label.

---

### 3. Segment Label Assignment

- Each denoised, segmented ECG file is loaded.
- For every segment (of 1000 samples), the corresponding annotations are identified based on sample index.
- The most frequent class label (mode) within each segment is assigned as the segment’s label.
- If no annotation exists for a segment, the label is set to `-1`.

---

### 4. Saving Labeled Data

- Segment labels are added as a new column to the data.
- The labeled, denoised, and segmented data are saved as new CSV files.
- For each file, a summary table of segment counts per class is printed.

---

### 5. Total Class Count Across All Files

- The script maintains a total count of each class label across all files.
- A summary table is printed at the end to show the overall distribution of class labels.

---

