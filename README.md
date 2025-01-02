**Audio Deepfake Detection using Vision Transformer**


**Overview**
This project focuses on detecting audio deepfakes using a pretrained Vision Transformer model. Deepfake audio detection is a critical task in combating misinformation and ensuring the authenticity of voice recordings. The dataset used comprises histograms of audio data representing various spoofed and bona fide trials.

With this approach, the model achieved 94% training accuracy in 3 epochs and an impressive 99% accuracy on the testing dataset.

**Key Features**
1. Utilized Vision Transformer (ViT) as the primary model for feature extraction and classification.
2. Achieved state-of-the-art accuracy with minimal training epochs.

**Project Details**
1. *Dataset Description*: H-Voice: Fake voice histograms (Imitation+DeepVoice)
Link to access dataset: https://data.mendeley.com/datasets/k47yd3m28w/4
This data set consists of (6672) histograms of original voice recordings and fake voice recordings obtained by Imitation [1, 2] and Deep Voice. The histograms provided in this dataset can be used to train a machine learning system to classify original and fake voice recordings obtained with the imitation and Deep Voice algorithms.

Each directory has the following composition:
-> Training_fake: 2088 histograms of fake voice recordings (2016 with Imitation and with 72 Deep Voice)
-> Training_original: 2020 histograms of original voice recordings 
-> Validation_fake: 864 histograms of fake voice recordings (all with Imitation)
-> Validation_original: 864 histograms of original voice recordings 
-> External_test1: 760 histograms (380 original + 380 fake with Imitation)
-> External_test2: 76 histograms (4 original + 72 fake with Deep Voice)


2. *Model*
Architecture: Pretrained Vision Transformer (ViT) fine-tuned for binary classification.
Input Format: 256x256 grayscale histograms of audio data

3. *Results*
Training Accuracy: 94% (3 epochs)
Testing Accuracy: 99%

4. *Why Use Histograms?*
Histograms summarize audio features efficiently, allowing the Vision Transformer to process the data as images. This approach bypasses the need for raw audio processing while maintaining high accuracy in detecting subtle anomalies in spoofed audio.


**Future Work**
1. Incorporate raw audio or spectrogram-based analysis for comparative evaluation.
2. Extend the model to multi-class classification for detecting various types of spoofing.
3. Optimize the model for deployment in real-time audio authentication systems.
