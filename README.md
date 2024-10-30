# Content Recommendation System with LDA for Topic Modeling

## Project Overview
This project demonstrates a content recommendation system that utilizes Latent Dirichlet Allocation (LDA) for topic modeling. The system extracts latent topics from text data and recommends similar content based on topic distribution. The recommendations are generated by calculating cosine similarity on the topic distributions.

## Features
- Preprocesses text data by cleaning and tokenizing
- Vectorizes text data using TF-IDF
- Applies LDA for topic modeling
- Calculates topic distributions for each document
- Recommends similar content based on cosine similarity of topic distributions

## Installation

1. Clone this repository.
    ```bash
    git clone (https://github.com/varun82004/Topic-Modelling-and-Topic-Recommendation.git)
    ```
2. Install required libraries.
    ```bash
    pip install pandas scikit-learn nltk
    ```
3. Download NLTK stopwords and tokenizers if not already downloaded:
    ```python
    import nltk
    nltk.download('stopwords')
    nltk.download('punkt')
    ```

## Dataset
The dataset should be a CSV file with the following columns:
- `Id`: Unique identifier for each entry
- `Title`: Title or heading of the content
- `Body`: Text body of the content

Place your dataset (e.g., `train.csv`) in the project directory.

## Usage

1. **Data Loading and Preprocessing**:
    - The dataset is loaded, and `Title` and `Body` fields are combined for text analysis.
    - Preprocessing involves converting text to lowercase, removing punctuation, stopwords, and tokenizing.

2. **Vectorization and Topic Modeling**:
    - The `TfidfVectorizer` is used to convert text data into a TF-IDF matrix.
    - LDA is applied to extract latent topics.

3. **Recommendation Function**:
    - The `recommend_similar_questions` function recommends content similar to a specified `question_id`.
    - This function utilizes cosine similarity on topic distributions to find similar entries.

### Example Usage
To test the recommendation function on a sample question, run:
```python
recommend_similar_questions(question_id=34552656)
```

## Code Structure

- `preprocess_text`: Function to clean and preprocess text data.
- `display_topics`: Function to display keywords in each LDA topic.
- `recommend_similar_questions`: Function that takes `question_id` as input and returns the top 5 most similar entries based on topic distribution.

## Output
The output includes:
- Display of extracted topics with top keywords.
- List of recommended content similar to the input question.

### Sample Output
For `recommend_similar_questions(question_id=34552656)`, the output will display similar content with fields:
- `Question ID`: Identifier of the recommended content
- `Title`: Title of the recommended content
- `Tags`: Tags associated with the recommended content

---

## Requirements
- Python 3.x
- Required libraries: `pandas`, `nltk`, `scikit-learn`

## Author
This project was developed for educational purposes as a demonstration of content recommendation with LDA-based topic modeling.

