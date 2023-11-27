# Stroke Onset Detection and Clustering
The goal of this project is to develop a ML model that detects the onset of musical instrument strokes and clusters the strokes from each instrumetent

## Method
1. Stroke Onset Detection
2. Isolating & Clustering detected strokes

### Stroke Detection: 
On analysing the spectrogram and the onset times, we can clearly observe each stroke visually just from the  spectrogram. Hence, the mel-spectrogram will be used as the input features for a fully connected Neural Network. We use the Mel-spectrogram (hop_size = window_size) to better represent our perception of sound. On analysing the spectrogram in Praat, we can observe 512/22050 and 1024/22050 (sample rate = 22050) good window lengths. We keep hop length to be equal to window Length in mel-spectrogram in order to match the generated labels.

### Clustering: 
The segments with the detected strokes will now be clustered using a Clustering algorithm to classify them as  strokes of different instruments. The same input features, i.e the mel-spectrogram can be used for this.
