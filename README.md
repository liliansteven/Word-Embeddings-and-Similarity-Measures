# Word Embeddings and Document Similarity Analysis

This repository contains a comprehensive purpose in Natural Language Processing (NLP), focusing on preprocessing and analyzing document similarity using `Word2Vec` embeddings and various similarity measures. it includes code for embedding words, computing document similarity, and visualizing the relationships between different texts using heatmaps and multidimensional scaling (MDS).


## Overview

### NLP Preprocessing:
1. **Tokenization:**
   - Utilizes the powerful `nltk` library for word tokenization (`word_tokenize`).
   - Breaks down text into individual words or tokens.

2. **Stopword Removal:**
   - Removes common English stopwords using the `stopwords` module from `nltk`.
   - Enhances the focus on meaningful words in document analysis.

3. **Word Embeddings (Word2Vec):**
   - Represents words as high-dimensional vectors in a continuous vector space.
   - Employs a vector size of 100, increased for richer embeddings.
   - Adopts a window size of 5, focusing on closer semantic relationships.
   - Sets a minimum count of 1 to consider less frequent words during training.
   - Trains the model over 1000 epochs for optimal word embeddings.

### Similarity Measures:

1. **Cosine Similarity:**
   - Measures the cosine of the angle between document vectors.
   - Provides a range from -1 to 1, indicating similarity or dissimilarity.

2. **Jaccard Similarity:**
   - Measures the intersection over the union of word sets in documents.
   - Suitable for situations where the order of elements doesn't matter.
   - Captures document similarity based on word overlap.
   - Offers a similarity range between 0 and 1.

3. **Euclidean Distance:**
   - Measures the straight-line distance between document vectors.
   - Provides a geometric interpretation of dissimilarity.


### Steps:
- Reads the content of three documents (`Document1.txt`, `Document2.txt`,` Document3.txt`).
- Tokenizes each document, applies stopword removal, and preprocesses the text.
- Calculates document embeddings using the Word2Vec model.
- Computes similarity values (**Cosine Similarity**, **Jaccard Similarity**, **Euclidean Distance**) between pairs of documents.
- Visualizes similarity matrices using **heatmaps**.
- Employs Multidimensional Scaling (MDS) to project document embeddings into a 2D space for visual inspection.
- Outputs and interprets the resulting 2D embeddings.

### Key Parameters and Configurations:
- **Vector Size:** 100-dimensional embeddings.
- **Window Size:** 5 for capturing semantic relationships in a smaller context window.
- **Min Count:** 1 to include all words during model training.
- **Epochs:** 1000 for robust training of the Word2Vec model.
