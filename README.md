# Amazon ML Challenge 2025 – Multi-Modal Price Prediction

## Overview

This repository contains our solution for **Amazon ML Challenge 2025**, where our team **Machine Learners** built a **multi-modal price prediction system** by combining textual, visual, and engineered numerical features.

Competing among **84,000+ participants nationwide**, we progressed from being completely off the leaderboard to reaching **Rank 13 during Day 2/3**, and ultimately secured a position in the **Top 125 teams** with a final **SMAPE score of 44.2**.

This project became an opportunity to explore large-scale machine learning pipelines, efficient experimentation, and collaborative model iteration under competition constraints.

---

## Problem Statement

Build a model capable of accurately predicting prices using information from multiple modalities.

The solution integrates:

* Product text information
* Product image information
* Engineered numerical attributes

The objective metric used for evaluation was **SMAPE (Symmetric Mean Absolute Percentage Error).**

---

## Architecture

### Multi-Modal Pipeline

#### Text Encoder

* **DeBERTa-v3-large**
* Generated contextual text embeddings from product metadata

#### Image Encoder

* **Vision Transformer (ViT)**
* Extracted semantic image representations

#### Feature Engineering

* Domain-inspired numerical features
* Data preprocessing and normalization

#### Fusion Layer

Outputs from all modalities were combined using a **custom regression head** to generate final price predictions.

---

## Training Strategy

Model optimization included:

* **SMAPE-aware hybrid loss**
* **EMA (Exponential Moving Average)**
* **Cosine Learning Rate Scheduling**
* **FP16 Mixed Precision Training**

These approaches helped improve training efficiency and model stability.

---

## Results

| Metric                | Result      |
| --------------------- | ----------- |
| Peak Leaderboard Rank | **13**      |
| Final Standing        | **Top 125** |
| Final SMAPE           | **44.2**    |
| Participants          | **84,000+** |

---

## Key Learnings

This competition helped us gain experience in:

* Designing end-to-end ML workflows
* Working with multi-modal architectures
* Handling large-scale real-world datasets
* Rapid experimentation and debugging
* Team collaboration under competitive timelines

As a first competitive ML experience, this project reinforced the importance of iteration, practical engineering decisions, and reproducible experimentation.

---

## Team

Team: **Machine Learners**

**Contributors:**
Anoosha Lad
Sofian Chicktay
Ayon Majumdar
Aadya Deshpande

## Repository Structure

```plaintext
├── data/
├── notebooks/
├── src/
│   ├── preprocessing/
│   ├── models/
│   ├── training/
│   └── inference/
├── configs/
├── outputs/
├── README.md
└── requirements.txt
```

---

## Future Improvements

* More efficient fusion architectures
* Improved feature engineering
* Better hyperparameter optimization
* Lightweight deployment-ready inference pipeline

---

## Acknowledgements

Thanks to the organizers of **Amazon ML Challenge 2025** and everyone involved in building and evaluating the competition.

---
