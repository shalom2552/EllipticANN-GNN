# EllipticANN-GNN

## Overview
**EllipticANN-GNN** is a project aimed at improving the classification of illicit transactions in the Elliptic++ dataset using a hybrid Graph Neural Network (GNN) enhanced with Approximate Nearest Neighbor (ANN) search. By leveraging both transaction network structure and feature-based similarities, this model seeks to improve accuracy and efficiency in classifying suspicious activities within the Bitcoin network.

## Project Structure
- **Data Preprocessing**: 
  - Normalize transaction features and create an ANN-based layer to enhance sparse or noisy regions in the graph.
  - Generate additional feature-similarity edges using FAISS or HNSW for integration into the GNN model.
- **Hybrid GNN Architecture**:
  - **Model**: Combines a Graph Convolutional Network (GCN) or Graph Attention Network (GAT) with ANN to expand message-passing beyond direct neighbors.
  - **ANN Integration**: Weight ANN-based neighbors alongside money flow connections to balance feature-based similarity and direct transaction relationships.
- **Experimentation**:
  - Compare baseline GNN and non-graph methods with the hybrid model.
  - Test various ANN neighbor counts and weight schemes.
  - Evaluate performance with metrics like accuracy, F1-score, and computational efficiency.

## Key Features
- **Hybrid GNN with ANN augmentation**: Combines structural and feature-based neighbors to improve transaction classification.
- **Configurable ANN Layer**: Allows control over the number of neighbors and weighting in the message-passing mechanism.

## Getting Started
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/EllipticANN-GNN.git

## Original Dataset and Research
This project is based on the **Elliptic++ Transactions Dataset** published by the **DISL Lab at Georgia Tech**. For the original dataset and research details, please visit the [EllipticPlusPlus GitHub Repository](https://github.com/git-disl/EllipticPlusPlus/tree/main).
