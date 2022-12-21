# Spectrogram-Audio-Generator

One file involves generating Mel-Spectrogram images in RGB given in GTZAN dataset using WGAN, and measuring their fidelity using Kernel Inception Distance(KID) metric.

Another file involves creating our own Mel-Spectrogram images in grayscale format from audio files given by GTZAN. These files can be converted back to audio using librosa.feature.inverse.mel_to_audio(), although it decreases the quality of original audio. Therefore we again train the WGAN on these images to generate images from similar distribution.
The fidelity of images is again compared using KID metric with "feature" hyperparametr been set to 4 different values

The generated spectrogram is converted to a form closer to the original images using otsu threshold value from cv2, resized to required size and converted to audio for inspection.
