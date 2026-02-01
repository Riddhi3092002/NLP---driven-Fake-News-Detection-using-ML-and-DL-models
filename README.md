# NLP-Driven Fake News Detection

This project implements a robust system to combat digital disinformation by classifying news articles as either True or Fake using various Machine Learning (ML) and Deep Learning (DL) architectures.

## Project Overview
The rise of false news in digital media contributes to societal divide and disinformation. This project explores the effectiveness of multiple algorithms—ranging from traditional statistical models to advanced recurrent neural networks—to identify complicated language patterns and contextual clues in text.

## Project Files
- `Fake News Detection.ipynb`: Jupyter notebook containing the complete code for the project.
- `FakeNewsDetectionProjectReport.pdf`: Detailed project report including methodology, results, and conclusions.

## Dataset: ISOT News Dataset
The models were trained and evaluated using the ISOT Dataset, which contains over 44,000 articles:
- **True News**: Articles sourced from Reuters.com, a well-known provider noted for accurate reporting.
- **Fake News**: Gathered from untrustworthy sources identified by Politifact and Wikipedia.
- **Data Points**: Includes article title, full text, subject, and publication date.

## Technical Implementation

### Preprocessing & Feature Extraction
To prepare the textual data for the models, a rigorous preprocessing pipeline was implemented:
- **Text Cleaning**: Lowercasing, punctuation removal, and NLTK-based stopword removal.
- **ML Features**: TF-IDF Vectorization, limited to the top 5,000 frequent terms to reduce noise and improve efficiency.
- **DL Features**: Tokenization, padding to a fixed length of 100 tokens, and pre-trained GloVe word embeddings to capture semantic relationships.

### Models Evaluated
The research involved training and comparing nine different architectures:

| Machine Learning Models | Deep Learning Models |
| :--- | :--- |
| Logistic Regression | Simple Neural Network |
| Support Vector Machine (SVM) | Long Short-Term Memory (LSTM) |
| Random Forest | Bidirectional LSTM |
| Multinomial Naïve Bayes | CNN-LSTM Hybrid |
| | Gated Recurrent Unit (GRU) |

## Performance Results
The models were evaluated on Accuracy, Precision, Recall, and F1-Score.


### Top Performers
- **Best ML Model**: Support Vector Machine (SVM) achieved the highest overall accuracy of 99.30%.
- **Highest F1-Score**: Random Forest led with a score of 0.9973, showing a strong balance between precision and recall.
- **Best DL Model**: GRU outperformed other neural networks with 98.86% accuracy and 0.9892 F1-score.

## Future Work
- Integrate transformer-based architectures such as BERT for improved contextual understanding.
- Expand the system to handle multi-modal data, including images and videos that accompany news stories.
- Implement a real-time news monitoring system to flag disinformation as it is published.
