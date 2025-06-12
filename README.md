# EEG Motor Imagery Classification

This project demonstrates basic preprocessing and classification techniques for EEG-based motor imagery data. It uses data from the [PhysioNet EEG Motor Movement/Imagery Dataset](https://physionet.org/content/eegmmidb/1.0.0/), where subjects perform imagined motor tasks such as left or right hand movement.

## Objectives

- Load and preprocess raw EEG data using MNE.
- Apply frequency filtering and standard electrode montage.
- Extract time-locked epochs around motor imagery events (T1: left hand, T2: right hand).
- Perform classification using:
  - **CSP + LDA** (feature extraction and linear classification).
  - **GRU-based RNN** for learning temporal patterns in EEG sequences.

## Techniques Used

- **MNE-Python**: For EEG preprocessing (filtering, epoching, montage assignment).
- **Common Spatial Patterns (CSP)**: Enhances discriminative spatial features between imagined left and right movements.
- **Linear Discriminant Analysis (LDA)**: Simple and effective classifier for CSP features.
- **PyTorch RNN (GRU)**: Captures temporal dependencies in EEG signal for binary classification.
- **Cross-validation**: 5-fold stratified to evaluate model generalization.

## Requirements
-**mne** >= 1.6.1
-**numpy** >= 1.24.0
-**scikit-learn** >= 1.2.0
-**matplotlib** >= 3.7.0
-**torch** >= 2.0.0

## Status

🧪 This project is a work in progress. Current results are suboptimal (42–47% accuracy), but reflect real-world challenges of EEG decoding. Planned improvements include better preprocessing, data augmentation, time-frequency analysis, and more advanced neural architectures.
