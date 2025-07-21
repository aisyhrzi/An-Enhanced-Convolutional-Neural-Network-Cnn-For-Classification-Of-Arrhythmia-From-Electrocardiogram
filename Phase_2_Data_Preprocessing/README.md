1. Import Libraries
You import all the packages you need for data handling, signal processing, plotting, and working with files.

2. Plot Settings
You set some style options for your plots to make them look nice.

3. Denoise Function
You define a function called denoise() using the Daubechies wavelet ('db4').

This function cleans your ECG signal by removing noise, making the data smoother and easier to analyze.

4. Plot Function
Another function, plot_denoised_vs_original(), is defined to show a plot of the original ECG signal vs the denoised version so you can check if the cleaning works well.

5. Find All ECG Files
You set the path to your ECG data folder and make an output folder for results.

You then list out all the .csv and .txt files in your dataset folder, and only select the ones that match your chosen training IDs.

6. Loop Through Each File
For each ECG data file you found:

Read the CSV file (ignoring the header row).

Extract the MLII column (the important ECG channel).

Denoise the signal using the wavelet function.

Plot both original and denoised signals so you can see the difference.

7. Segment the Denoised Data
You split the denoised ECG signal into multiple segments, each with 1000 data points.

For example, if your data has 10,000 samples, you’ll get 10 segments.

All segments are collected in a list.

8. Save the Segmented Data
You combine all segments into a DataFrame.



