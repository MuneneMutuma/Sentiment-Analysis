# Sentiment Analysis Using NLTK - Jupyter Notebook

## Overview

This project implements a sentiment analysis pipeline using **Natural Language Toolkit (NLTK)** within a Jupyter Notebook. It classifies tweets as **Positive** or **Negative** using a **Naive Bayes Classifier**. The project includes data preprocessing, feature extraction, model training, and evaluation, all executed in an interactive Jupyter environment.

---

## Features

- **Data Loading**: Utilizes pre-classified tweet data from NLTK's `twitter_samples`.
- **Preprocessing**: Tokenization, Lemmatization, Noise Removal, and Stopword Filtering.
- **Model Training and Testing**: Employs a **Naive Bayes Classifier** to predict tweet sentiments.
- **Custom Sentiment Analysis**: Classify custom user-input sentences.

---

## Setup

### Prerequisites

- **Jupyter Notebook** or **JupyterLab**
- **Python 3.x**
- **NLTK** library

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/sentiment-analysis-nltk.git
   cd sentiment-analysis-nltk
   ```

2. **Install Dependencies:**
   In your terminal or command prompt, install the required libraries:

    ```bash
    pip install nltk jupyter
    ```

3. **Start Jupyter Notebook:**
    Launch Jupyter Notebook:

    ```bash
    jupyter notebook
    ```

4. **Run the Cells:**
   Open the notebook and run the cells sequentially. The NLTK datasets required for this project will be automatically downloaded when you run the preprocessing section in the notebook.

### Usage
- Test Custom Sentences: You can test custom sentences for sentiment analysis by running the test_sentiment function with your input:
  ```python
  test_sentiment("I love this!")  # Output: Positive
  test_sentiment("This is terrible.")  # Output: Negative
  ```

### Project Workflow
#### 1. Data Preprocessing:
- Lemmatization: Reduces words to their base forms (e.g., "running" -> "run").
- Noise Removal: Removes URLs, usernames, and punctuation.
- Stopword Removal: Filters common words like "is", "the", etc.

#### 2. Feature Extraction:
- Converts cleaned tokens into feature sets for the classifier.

#### 3. Model Training:
- Trains a Naive Bayes Classifier using labeled tweets from the twitter_samples dataset.

#### 4. Model Evaluation:
- Achieves 99.46% accuracy on the test set.
- Displays the most informative features (e.g., :), :(, goodnight, sad).


### Results
- Accuracy: 99.46% on test data.
- Most Informative Features:
    - Positive: `:)`, `goodnight`, `bam`
    - Negative: `:(`, `sad`, `aw`
