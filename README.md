# Multimodal Movie Recommendation System

A multimodal movie recommendation project combining **computer vision, natural language processing, and graph neural networks** to investigate how different movie representations affect recommendation performance.

The project was developed as part of the **Neural Networks & Deep Learning** course at the National Technical University of Athens (NTUA).

## Overview

The system models users and movies as a heterogeneous graph, where user–movie interactions are represented as edges.

Different sources of movie information are used to construct feature representations:

- **Visual features** extracted from movie posters using convolutional neural networks
- **Textual features** derived from movie-related textual information
- **Multimodal features** combining visual and textual representations
- **Graph-based representations** using user–movie interaction data

These representations are evaluated within a **GraphSAGE-based link prediction framework** for movie recommendation.

## Project Components

### 1. Computer Vision

CNN-based models were explored for extracting information from movie posters.

The experiments included custom convolutional architectures as well as pretrained models, allowing visual information to be incorporated into movie representations.

### 2. Natural Language Processing

Textual movie information was processed to obtain semantic representations that capture information not directly available from poster images.

These representations were subsequently used as movie node features in the recommendation graph.

### 3. Graph-Based Recommendation

Users and movies were represented as nodes in a heterogeneous graph, with user–movie interactions defining the graph structure.

GraphSAGE was used for link prediction to estimate potential user–movie interactions.

Multiple feature configurations were compared, including:

- Baseline graph features
- Visual features
- Textual features
- Multimodal features
- Pretrained feature representations

The textual representation achieved the strongest validation performance, with an AUC of approximately **0.935**.

## Technologies

- Python
- PyTorch
- PyTorch Geometric
- Convolutional Neural Networks (CNNs)
- GraphSAGE
- Natural Language Processing
- Graph Neural Networks
- NumPy
- pandas
- scikit-learn

## Repository Structure

```text
multimodal-movie-recommendation/
├── README.md
├── multimodal_movie_recommendation.ipynb
├── requirements.txt
└── .gitignore
```
## Data & Reproducibility

The experiments use the publicly available MovieLens datasets together with prepared movie metadata, plot summaries, poster images, learned embeddings, and model checkpoints.

Large datasets, poster collections, intermediate embeddings, and trained model checkpoints are not included in this repository. The notebook retains the outputs of the original experiments so that the training process, evaluation metrics, and experimental comparisons can be inspected without rerunning the full pipeline.

The repository is therefore intended primarily as a documented presentation of the experimental workflow and results rather than as a fully self-contained reproduction package.

## Notes

This repository is a cleaned and reorganized version of a university course project. The original assignment provided parts of the experimental framework, including the GraphSAGE architecture and training pipeline. The project work focused on feature construction, multimodal representation, integration with the graph-based recommendation framework, experimentation, and evaluation.

## Authors

- **Eleni Amarantidi**
- **Efthimios Grizanitis**

Developed as part of the **Neural Networks & Deep Learning** course at the National Technical University of Athens (NTUA).
