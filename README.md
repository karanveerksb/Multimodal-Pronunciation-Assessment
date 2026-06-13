# Multimodal Pronunciation Assessment

## Overview

This project implements a **Multimodal Pronunciation Assessment (MPA)** system by combining acoustic and textual information to automatically evaluate spoken English pronunciation quality. The system extends the **Speechocean762 baseline** by integrating speech representations from **Wav2Vec2** and textual features extracted using **BERT**.

The goal is to predict pronunciation quality scores using both audio and transcript information, enabling more comprehensive assessment than unimodal approaches.

---

## Features

* Speech feature extraction using **Wav2Vec2**
* Text feature extraction using **BERT**
* Multimodal fusion of acoustic and textual representations
* Multi-level pronunciation scoring
* Performance evaluation using:

  * Pearson Correlation Coefficient (PCC)
  * Root Mean Squared Error (RMSE)
* End-to-end training and evaluation pipeline

---

## Dataset

The project uses the **Speechocean762** dataset, a benchmark dataset for automatic pronunciation assessment.

Dataset components include:

* Audio recordings
* Transcriptions
* Human-annotated pronunciation scores

---

## Methodology

### 1. Acoustic Feature Extraction

Audio waveforms are processed using **facebook/wav2vec2-base-960h** to obtain rich speech representations.

### 2. Text Feature Extraction

Reference transcripts are encoded using **BERT** to capture linguistic and semantic information.

### 3. Multimodal Fusion

Acoustic and textual embeddings are combined to create a unified representation for pronunciation assessment.

### 4. Score Prediction

The fused representation is passed through regression layers to predict pronunciation quality scores.


## Evaluation Metrics

The model performance is evaluated using:

### Pearson Correlation Coefficient (PCC)

Measures the correlation between predicted and ground-truth pronunciation scores.

### Root Mean Squared Error (RMSE)

Measures prediction error magnitude.

Higher PCC and lower RMSE indicate better performance.

---

## Results

The multimodal approach demonstrates improved pronunciation assessment performance by leveraging both acoustic and textual information.

Performance was analyzed using PCC and RMSE across multiple pronunciation scoring dimensions.

---

## Future Improvements

* Incorporate attention-based fusion mechanisms
* Explore larger speech foundation models
* Add phoneme-level pronunciation assessment
* Deploy as a real-time pronunciation feedback system
* Support multilingual pronunciation evaluation

---

## References

1. Speechocean762 Dataset
2. Wav2Vec2: Self-Supervised Learning of Speech Representations
3. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
