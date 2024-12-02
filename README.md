# Speech Command Recognition

This project implements a Speech Command Recognition system using Gaussian Mixture Models (GMMs). It involves audio feature extraction using MFCC, Delta, and Delta-Delta coefficients, training GMMs for classification, and predicting the correct command for test audio.

---

## Dataset

The dataset used for this project is the [Speech Commands Dataset](https://dagshub.com/kingabzpro/Speech_Commands_Dataset). It consists of 30 word utterances and noise audio. The dataset is used for training and testing the models.

---

## Features

### Key Highlights:
- **Audio Feature Extraction**:
  - Used MFCC (Mel-Frequency Cepstral Coefficients), Delta, and Delta-Delta coefficients for extracting meaningful features from audio signals.
  
- **Model Training**:
  - Gaussian Mixture Models (GMMs) were employed for classification.
  - Parameter estimation was achieved using the Expectation-Maximization (EM) algorithm.
  
- **Prediction**:
  - Trained a GMM for each word class and calculated the probability of test audio belonging to each class.

### Achievements:
- Achieved an average classification accuracy of **82\%**.
- Utilized GMMs with **10 components per word class** for the 30-word utterance dataset.

---

## Project Workflow

### Step 1: Dataset Preparation
1. Download the Speech Commands Dataset from the [official dataset link](https://dagshub.com/kingabzpro/Speech_Commands_Dataset).
2. Preprocess the dataset:
   - Split the data into training and testing sets.
   - Normalize and augment the data as needed.

### Step 2: Feature Extraction
1. Extract audio features using:
   - MFCC
   - Delta coefficients
   - Delta-Delta coefficients

2. Save the extracted features for model training.

### Step 3: Model Training
1. Train a Gaussian Mixture Model (GMM) for each word class using the extracted features.
2. Optimize model parameters using the Expectation-Maximization (EM) algorithm.

### Step 4: Prediction and Evaluation
1. For test audio, calculate the probability of the audio belonging to each word class using the trained GMMs.
2. Assign the word class with the highest probability as the predicted label.
3. Evaluate the model's accuracy and report the results.

---

## Requirements

### Python Libraries:
Install the required dependencies using `pip`:
```bash
pip install numpy scipy librosa sklearn
