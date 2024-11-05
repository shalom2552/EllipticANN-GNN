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

**DATASET CAN BE FOUND HERE: [Google Drive](https://drive.google.com/drive/folders/1MRPXz79Lu_JGLlJ21MDfML44dKN9R08l?usp=sharing)**

## Dataset Summary 

The Elliptic++ dataset contains a transactions dataset and an actors (wallet addresses) dataset.

Elliptic++ Transactions Dataset:

|  |  |
|---|---|
| # Nodes (transactions) | 203,769 |
| # Edges (money flow) | 234,355 |
| # Time steps | 49 |
| # Illicit (class-1) | 4,545 |
| # Licit (class-2) | 42,019 |
| # Unknown (class-3) | 157,205 |
| # Features | 183 |

Elliptic++ Actors (Wallet Addresses) Dataset:

|  |  |
|---|---|
| # Wallet addresses | 822,942 |
| # Nodes (temporal interactions) | 1,268,260 |
| # Edges (addr-addr) | 2,868,964 |
| # Edges (addr-tx-addr) | 1,314,241 |
| # Time steps | 49 |
| # Illicit (class-1) | 14,266 |
| # Licit (class-2) | 251,088 |
| # Unknown (class-3) | 557,588 |
| # Features | 56 |

 

## Original Dataset and Research
This project is based on the **Elliptic++ Transactions Dataset** published by the **DISL Lab at Georgia Tech**. For the original dataset and research details, please visit the [EllipticPlusPlus GitHub Repository](https://github.com/git-disl/EllipticPlusPlus/tree/main).
