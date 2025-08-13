# 📰 Fake News Detection using LSTM & NLP

## 📌 Overview
This project implements a **Fake News Detection** model using **Natural Language Processing (NLP)** techniques and a **Long Short-Term Memory (LSTM)** neural network.  
The goal is to classify news articles as **real** or **fake** based on their textual content.

---

## 📊 Dataset
- **Source**: [Kaggle - Fake News Dataset](https://www.kaggle.com/c/fake-news)
- **Features**:
  - `title`: Headline of the news article
  - `text`: Body content of the news
  - `label`: Target variable (1 = Fake, 0 = Real)
- Dataset is preprocessed to handle:
  - Missing values
  - Stopwords removal
  - Tokenization
  - Padding for LSTM input

---

## 🛠️ Approach
1. **Data Preprocessing**
   - Removed missing values
   - Lowercased text for normalization
   - Removed stopwords & punctuation
   - Tokenized using `Tokenizer` from Keras
   - Converted tokens to sequences
   - Applied padding to ensure fixed-length input

2. **Model Architecture**
   - **Embedding Layer**: Converts words into dense vector representations
   - **LSTM Layer**: Captures sequential dependencies in text
   - **Dense Layers**: Fully connected layers for classification
   - **Activation Function**: Sigmoid for binary classification

3. **Training**
   - Optimizer: Adam
   - Loss Function: Binary Crossentropy
   - Metrics: Accuracy
   - Early stopping to prevent overfitting

4. **Evaluation**
   - Measured on accuracy, precision, recall, and F1-score
   - Confusion matrix visualization

---

**📈 Results**
Accuracy: 92.89%

Precision: 93%

Recall: 93%

F1 Score: 93%

---
**Classification Report:**
               precision    recall  f1-score   support

           0       0.94      0.93      0.94      2082
           1       0.91      0.93      0.92      1575

    accuracy                           0.93      3657
   macro avg       0.93      0.93      0.93      3657
weighted avg       0.93      0.93      0.93      3657

---
**Confusion Matrix:**

[[1940  142]

 [ 118 1457]]
