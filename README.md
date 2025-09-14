## RNA Structure Prediction – Kaggle (Stanford)

This repository contains my work for the [Stanford-hosted Kaggle competition on RNA structure prediction
 (Ribonanza)]([url](https://www.kaggle.com/competitions/stanford-ribonanza-rna-folding)). The goal of the competition is to predict the 3D structure of RNA molecules from their nucleotide sequences.

## Overview

RNA structure prediction is a challenging task at the intersection of biology and machine learning. This repository explores two different approaches to predict RNA residue positions:

Graph Neural Network (GNN) Approach

Assumes fixed distance between successive RNA base pairs.

Trains the network to predict the 3D unit vectors connecting successive base pairs.

Builds structural consistency into the learning framework by constraining distances and focusing on directional prediction.

Boltzmann Model Approach (Hugging Face)

Uses the Boltzmann module from Hugging Face’s Boltz-1 repository
.

Leverages pre-trained embeddings to guide RNA structure prediction.

Combines competition data with large-scale pretrained knowledge for better generalization.

Both approaches are implemented in separate Jupyter notebooks (.ipynb files) within this repository.

## Repository Structure  
```
.
├── GNN_RNA_Structure.ipynb        # GNN-based RNA structure prediction
├── Boltzmann_RNA_Structure.ipynb  # Boltzmann model approach
└── README.md                      # Documentation
```
## Data

The dataset comes from the official Kaggle competition, hosted by Stanford. Due to competition rules, raw data files are not included in this repository. Please download them directly from the competition page
 if you’d like to reproduce the results.

##Requirements

To run the notebooks, install the required dependencies:
```bash
#!/bin/bash
pip install -r requirements.txt
```
Key libraries used:

torch, torch-geometric (for GNNs)

transformers (Hugging Face Boltzmann model)

numpy, pandas, matplotlib (data handling and visualization)

## Results & Insights

The GNN model captures structural constraints by focusing on geometric relationships.

The Boltzmann model benefits from transfer learning, leveraging large pretrained embeddings.

Together, these experiments provide insights into how physics-inspired constraints and pretrained models can complement each other in RNA 3D structure prediction.

## Acknowledgements

Stanford University and Kaggle for hosting the RNA structure prediction competition.

Hugging Face for providing pretrained Boltzmann models.




