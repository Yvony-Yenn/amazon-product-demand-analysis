# Notebooks

This folder contains the Jupyter notebooks used in the Amazon Product Demand Analysis project.  
The workflow follows a multimodal representation learning pipeline inspired by recent AI-based demand analysis research.

## Analysis Pipeline

The project consists of the following notebooks:

### 01_EDA.ipynb
Exploratory Data Analysis of the Amazon product dataset collected from the Keepa API.

Key tasks include:
- Inspecting dataset structure
- Handling missing values
- Exploring price distribution and sales rank
- Understanding product category distributions

### 02_text_embedding.ipynb
This notebook generates text embeddings from product titles and descriptions using a transformer-based language model (BERT).

Pipeline:
1. Extract product text features
2. Tokenize text using a BERT tokenizer
3. Generate contextual embeddings
4. Aggregate token embeddings to create product-level representations

These embeddings capture semantic relationships between product descriptions.

### 03_image_embedding.ipynb
This notebook generates image embeddings from product images using a vision encoder from a BERT-based multimodal representation model (e.g., CLIP / Vision Transformer).

Pipeline:
1. Download or load product images
2. Preprocess images
3. Encode images using a vision transformer
4. Generate fixed-length image embedding vectors

Image embeddings capture visual characteristics such as product style, color, and design.

### 04_feature_fusion.ipynb
This notebook combines multimodal features into a unified product representation.

Feature fusion includes:
- Text embeddings
- Image embeddings
- Structured product features (price, rating, reviews)

All embeddings are concatenated to form a comprehensive product representation vector.

### 05_clustering_analysis.ipynb
This notebook performs demand pattern discovery using dimensionality reduction and clustering techniques.

Pipeline:
1. Apply PCA for dimensionality reduction
2. Reduce embedding dimensionality
3. Apply KMeans clustering
4. Identify groups of products with similar demand characteristics

Sales rank is used as a proxy for product demand, allowing clusters to reveal different demand patterns across products.

## Multimodal Product Representation

Products are represented using multimodal embeddings derived from both product text and images.  
This approach allows the model to capture semantic and visual characteristics that influence consumer demand.

Final product representation:

Product Representation =
[Text Embedding + Image Embedding + Structured Features]

These embeddings enable downstream analysis such as clustering and demand pattern discovery.
