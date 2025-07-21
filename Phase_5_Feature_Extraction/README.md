# Phase 2: Feature Extraction (Scalogram Generation)

This phase transforms each ECG segment into a time-frequency image (scalogram) using Continuous Wavelet Transform (CWT), and then resizes the images for use in deep learning models.

## Steps

1. **Scalogram Generation**
   - Each denoised, segmented ECG signal is converted into a 2D image (scalogram) using CWT.
   - Scalograms are saved as PNG files in class-specific folders (`0`, `1`, `2`, `3`, `4`).

2. **Image Preprocessing & Resizing**
   - All scalogram images are resized to 224x224 pixels to match the input size requirements of common CNN models (e.g., AlexNet, VGG).
   - Images are organized in folders by class.

## Input
- Balanced and labeled ECG data (CSV from Phase 3).

## Output
- PNG scalogram images, resized to 224x224, stored by class.

Below is an example of a balanced scalogram segment:


![Balanced Scalogram Segment](https://github.com/aisyhrzi/An-Enhanced-Convolutional-Neural-Network-Cnn-For-Classification-Of-Arrhythmia-From-Electrocardiogram/blob/1e95b695c04d46c0fb379e291e0b444c3f89253e/balanced_scalogram_segment_1.png?raw=true)

---

*These images are ready to be used for CNN model training in the next phase.*

