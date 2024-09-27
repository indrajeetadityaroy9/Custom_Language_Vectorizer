# Natural Language Sentiment Analysis: Comparison of Custom vs. Sklearn TF-IDF Vectorization and Tokenization Techniques
The objective of this project is to develop a custom approach to vectorization and tokenization of natural language data and compare its performance to the baseline **sklearn** **TfidfVectorizer** implementation in a sentiment analysis task using IMDb movie reviews. The primary focus is on creating a custom TF-IDF vectorization technique that provides more control over how the text data is processed and represented. This custom approach is then benchmarked against the standard sklearn TF-IDF implementation to evaluate its effectiveness in capturing key features for classification.

## Features
### Full Control Over N-Grams:
- Unlike `sklearn`’s `TfidfVectorizer`, this custom implementation allows complete control over how n-grams are generated and the specific range of n-grams to use such as bigrams, trigrams, or higher-order n-grams, providing more contextual information from the text.

### Vocabulary Flexibility:
- A custom vocabulary can be specified for consistency across multiple datasets or the vocabulary can automatically be generated from the training corpus. This flexibility ensures that domain-specific terms or manually curated vocabularies can be used, enhancing the model’s relevance to particular tasks.

### Term Frequency and IDF Handling:
- The custom TF-IDF implementation allows for fine-tuned control over how term frequencies (TF) and inverse document frequencies (IDF) are computed. This enables the customization of the importance given to specific words or phrases in the dataset, making it adaptable to specific project needs, such as domain-specific weighting schemes.

### Efficient Sparse Representation:
- The custom implementation leverages sparse matrices, which are optimized for high-dimensional data, such as text with large vocabularies. This ensures that the vectorization process remains memory-efficient, especially when handling large datasets, while still enabling fast operations like matrix multiplications.

### Feature Selection:
- The `max_features` parameter provides direct control over the number of top features to include in the final TF-IDF matrix. This allows for dimensionality reduction by focusing only on the most important terms, which can improve model performance and reduce overfitting. The ability to filter out less important terms ensures that the classifier focuses on the most relevant parts of the data, making it more robust.

## Data Dictionary

| **Column Name** | **Data Type** | **Description**                              | **Variable Type**  |
|-----------------|---------------|----------------------------------------------|--------------------|
| `review`        | Text          | The text of the IMDb movie review            | Feature            |
| `label`         | Integer       | Sentiment label for the review (1: positive, 0: negative) | Target (binary)    |

## Dataset Overview

**Source**:  
- Sub-sampled from the **IMDB Dataset of 50K Movie Reviews** dataset available on [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)

**Features**:
- **Training Set**:  
  - 1,600 movie reviews  
  - 425,345 tokens  
  - 30,705 unique words  
  - Label Distribution: 804 positive (label = 1), 796 negative (label = 0)  

- **Validation Set**:  
  - 200 movie reviews  
  - 54,599 tokens  
  - 8,953 unique words  
  - Label Distribution: 105 positive (label = 1), 95 negative (label = 0)

- **Dataset Overlap**:
  - 6,574 words overlap between the training and validation sets.
