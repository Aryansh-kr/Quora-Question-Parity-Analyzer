# Quora Question Parity Analyzer

## Project Overview

The Quora Question Parity Analyzer aims to detect duplicate questions on Quora, enhancing content quality by identifying semantically similar questions. This project leverages a combination of traditional machine learning and deep learning techniques to achieve high accuracy in duplicate detection.

Dataset link-https://www.kaggle.com/competitions/quora-question-pairs/

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Results](#results)
- [Installation](#installation)


## Features

- **Text Preprocessing**: Tokenization, stop words removal, and stemming.
- **Vectorization**: Text to vectors using Word2Vec.
- **Custom Feature Generation**: Including average word length, word count, average sentence length, fog index, and complex word count.
- **Oversampling**: SMOTE for handling class imbalance.
- **Modeling**: Implementation of Random Forest, XGBoost, SimpleRNN, and Bidirectional LSTM.
- **Model Persistence**: Storing model weights using joblib.

## Data Preprocessing

We perform extensive text preprocessing to clean and prepare the data:

1. **Tokenization**: Splitting text into individual words or tokens.
2. **Stop Words Removal**: Removing common words that do not add significant meaning (e.g., "and", "the", "is").
3. **Stemming**: Reducing words to their base or root form (e.g., "running" to "run").

## Feature Engineering

To capture the nuances of text data, we generate several custom features:

1. **Word2Vec Embeddings**:
   - Window size: 5
   - Minimum word count: 2
   - Vector size: 30

2. **TextBlob Features**:
   - **Average Word Length**: Mean length of words in a question.
   - **Word Count**: Total number of words in a question.
   - **Average Sentence Length**: Mean length of sentences in a question.
   - **Fog Index**: A readability test indicating the complexity of the text.
   - **Complex Word Count**: Number of words with three or more syllables.

## Modeling

We implemented and evaluated multiple models to find the best performing ones:

1. **Random Forest**:
   - Achieved an accuracy of 85.66%

2. **XGBoost**:
   - Achieved an accuracy of 80.65%

3. **Deep Learning**:
   - **SimpleRNN**:
     - Loss function: `binary_crossentropy`
     - Optimizer: `Adam`
   - **Bidirectional LSTM**:
     - Achieved an accuracy of 93.17%

## Results

The Bidirectional LSTM model outperformed other models with an accuracy of 93.17%, demonstrating its effectiveness in capturing the sequential dependencies in the text data.

## Installation

Follow these steps to set up the project locally:

1. Clone the repository:
   ```sh
   git clone https://github.com/Aryansh-kr/Quora-Question-Parity-Analyzer.git
   
