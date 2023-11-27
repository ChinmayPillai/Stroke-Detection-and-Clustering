# Stroke Onset Detection and Clustering
The goal of this project is to develop a ML model that detects the onset of musical instrument strokes and clusters the strokes from each instrumetent

## Results of Stroke Onset Detection
1. *Accuracy - 85.5%*
2. *F1 Score - 70%*
3. Loss - 0.33

## Method
1. Stroke Onset Detection
2. Isolating & Clustering detected strokes

### Stroke Detection: 
On analysing the spectrogram and the onset times, we can clearly observe each stroke visually just from the  spectrogram. Hence, the *spectrogram* and the *spectral flux* will be used as the input features for a *fully connected Neural Network*. \

On analysing the spectrogram in Praat, we can observe 512/22050 and 1024/22050 (sample rate = 22050) good window lengths. I chose 512 as window size since it gave the best results. I kept hop length to be equal to window Length in spectrogram in order to match the generated labels.

### Clustering: 
The segments with the detected strokes will now be isolated and then clustered using a *K-Means Clustering* algorithm to classify them as strokes of different instruments. The same input features, i.e the spectrogram and spectral flux are used for this.\

*Auto-Correlation* was initially implemented for clustering the audio segments but it took long to run to be practical.
