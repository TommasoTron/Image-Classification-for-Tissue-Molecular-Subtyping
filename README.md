# Tissue Molecular Subtyping Classification

This repository contains a deep learning solution for an **image classification challenge** focused on predicting the molecular subtype of diseased human tissue samples.

## Task

The goal is to classify high-resolution histological images into **four classes**:

- `Luminal A`
- `Luminal B`
- `HER2(+)`
- `Triple Negative`

The project addresses challenges such as high-resolution input, significant class imbalance, and the presence of uninformative background areas.

## Approach

The proposed solution leverages a **Transfer Learning** strategy with the following key features:

- **Tiling Strategy**: Generation of high-resolution crops focused on regions identified by binary masks to preserve morphological details.
- **Phikon Backbone**: A domain-specific foundation model (Vision Transformer) pre-trained on histology data.
- **Imbalance Management**: Use of Weighted Cross-Entropy Loss to handle underrepresented classes.
- **Multi-view Inference**: A voting strategy that averages probabilities from multiple tiles to determine the final class.

## Report

For full details on the methodology, architecture evolution, and experiments, see the accompanying **Image Classification Report.pdf**.
