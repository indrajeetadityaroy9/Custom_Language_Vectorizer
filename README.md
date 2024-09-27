# Text Sentiment Analysis: A Comparison of Custom vs. Sklearn TF-IDF Vectorization Techniques

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
