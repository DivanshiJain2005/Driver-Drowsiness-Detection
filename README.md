# Driver Drowsiness Detection Using CNN-LSTM Fusion Model

## Overview

This project aims to develop a real-time driver drowsiness detection system using a hybrid approach that combines Convolutional Neural Networks (CNN) and Long Short-Term Memory (LSTM) networks. The system leverages facial landmark detection and physiological signals to monitor driver fatigue and provide timely alerts, thereby enhancing road safety.

## Key Features

- **Real-time Monitoring**: The system processes live video frames to detect facial landmarks and determine the eye status (open or closed).
- **Hybrid Model**: Combines Haar Cascade for face detection, CNN for spatial feature extraction, and LSTM for temporal pattern recognition.
- **High Accuracy**: Achieves an accuracy of 95.1% in detecting driver drowsiness.
- **Adaptive Learning**: Utilizes data augmentation and adaptive learning rate adjustments to improve generalization.
- **Alert System**: Generates visual and auditory alerts to warn drivers when drowsiness is detected.

## Methodology

1. **Face and Eye Detection**: Haar Cascade is used to detect the driver's face and eyes in real-time video frames.
2. **Spatial Feature Extraction**: CNN extracts spatial features from the detected face and eye regions.
3. **Temporal Pattern Recognition**: LSTM captures temporal dependencies across multiple frames to detect prolonged eye closure or irregular blinking patterns.
4. **Alert Generation**: If drowsiness is detected, the system triggers visual and auditory alerts to notify the driver.

## Datasets

- **Drowsiness Prediction Dataset**: Contains labeled images of individuals in drowsy and non-drowsy states, focusing on eye features and head position.
- **Prediction Images Dataset**: A supplementary collection of images depicting individuals in both drowsy and active states, used to enhance the diversity of the training set.

## Data Preprocessing

- **Image Resizing and Normalization**: All images are resized to 145x145 pixels and normalized to facilitate effective model training.
- **Facial Landmark Extraction**: Key facial points, especially around the eyes, are extracted using facial detection models.
- **Data Augmentation**: Techniques like rotation, shift, zoom, and flip are applied to enhance the model's robustness and generalization ability.
- **Data Splitting**: The preprocessed data is divided into training and validation sets to ensure effective model evaluation and prevent overfitting.

## Model Architecture

The model architecture is a hybrid design that combines CNN and LSTM networks for classification into two categories: Fatigue Subjects and Active Subjects.

- **CNN Component**: Extracts spatial features from input data using convolutional layers, batch normalization, and dropout layers.
- **LSTM Component**: Captures temporal dependencies across sequential frames, enabling the model to detect patterns over time.
- **Output Layer**: Uses a sigmoid activation function to return binary predictions (fatigue or alertness).

## Training

- **Hyperparameter Tuning**: Optimal learning rates, dropout rates, and batch sizes are tuned for effective model training.
- **Dynamic Learning Rate Adjustment**: The learning rate is automatically reduced when validation performance plateaus, enhancing efficiency and generalization.
- **Callbacks**: Techniques like ReduceLROnPlateau are used to monitor validation loss and adaptively reduce the learning rate.

## Evaluation Metrics

- **Accuracy**: 95.1%
- **Precision**: 98.7%
- **Recall (Sensitivity)**: 93.1%
- **Specificity**: 98.1%
- **F1-Score**: 95.1%

## Results

The model was trained for over 70 epochs and achieved high accuracy and low loss values. The confusion matrix showed a low rate of misclassifications, indicating the model's reliability in identifying facial fatigue-related cues.

## Comparison with Other Models

- **MobileNet + LSTM**: Achieved an accuracy of about 80%.
- **CNN + Haar Cascade**: Achieved an accuracy of 94%.
- **Proposed Model (Haar Cascade + LSTM + CNN)**: Achieved an accuracy of 95.1%, outperforming the above architectures.

## Conclusion and Future Work

The proposed system marks a significant step toward the development of intelligent driver monitoring systems that can help prevent accidents and improve road safety. Future work may include expanding the system to include additional physiological signals, such as heart rate and pupil dilation, or exploring more advanced neural network architectures.

## Acknowledgments

We would like to express our sincere gratitude to everyone who supported us throughout this project, including our academic supervisors, colleagues, and friends. Their valuable insights, expertise, and unwavering support have been instrumental in the success of this project.
