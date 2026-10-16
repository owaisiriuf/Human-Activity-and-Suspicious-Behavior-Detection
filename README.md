# Human-Activity-and-Suspicious-Behavior-Detection
Video-based human activity and suspicious behavior detection using ResNet50 CNN feature extraction, SVM classification, and a planned LSTM temporal model.
Project Overview

This project focuses on video-based human activity classification and suspicious behavior recognition using Computer Vision, Deep Learning, and Machine Learning techniques. It uses a labeled video dataset containing 21 activity classes, including normal daily activities and suspicious or criminal activities.

The objective is to extract meaningful visual features from video frames, classify activities, and develop a system that can recognize different activity categories from surveillance-style videos.

Work Completed So Far

1. Dataset Preparation

* Collected the Human Activity & Suspicious Behavior Video Dataset from Kaggle.
* Organized the dataset into training, validation, and testing splits.
* Dataset distribution:
    * Training: 940 videos
    * Validation: 194 videos
    * Testing: 200 videos
* Worked on video metadata and activity labels.

2. Frame Sampling and Preprocessing

* Sampled 40 frames from each video.
* Resized the sampled frames to 224 × 224 pixels.
* Prepared the sampled frames for CNN-based feature extraction.

3. CNN Feature Extraction Using ResNet50

* Used a pretrained ResNet50 model with ImageNet weights.
* Extracted 2,048-dimensional visual feature vectors from each sampled frame.
* Represented each video as a sequence of 40 frame-feature vectors, with a shape of (40, 2048).
* Saved the extracted features for subsequent model training.

4. SVM Baseline Classification

* Developed a Support Vector Machine (SVM) baseline using the extracted ResNet50 features.
* Averaged the 40 frame-feature vectors to create one feature vector per video for SVM classification.
* Evaluated the baseline on the validation dataset.

Initial Validation Results:

* Accuracy: 44.33%
* Macro Precision: 43.59%
* Macro Recall: 41.73%
* Macro F1-score: 42.06%
* Generated a confusion matrix to examine classification performance across the 21 classes.

Current Project Pipeline

Video Dataset → Frame Sampling → Image Preprocessing → ResNet50 CNN Feature Extraction → SVM Baseline Classification → Evaluation

Planned Work

* Implement and train an LSTM-based temporal classification model using the sequential ResNet50 features.
* Integrate the CNN and LSTM components into the main deep-learning pipeline.
* Compare CNN-LSTM performance against the SVM baseline.
* Evaluate the final model using accuracy, precision, recall, F1-score, and a confusion matrix on the held-out test set.
* Develop a basic demonstration interface for video activity classification.

Technologies Used

* Python
* OpenCV
* NumPy
* TensorFlow / Keras
* ResNet50
* Scikit-learn
* Matplotlib
* Kaggle Notebooks

Project Status

In Progress — Dataset preparation, frame sampling, ResNet50 feature extraction, and initial SVM baseline evaluation have been completed. The CNN-LSTM model and final system evaluation are planned next.
