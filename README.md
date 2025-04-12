# NLP Assignment 2 – Hate Speech and Offensive Language Detection


##  Problem Statement
With the rise of social media, user-generated content has increased drastically, and so has the spread of offensive and hate speech. Manual moderation is inefficient due to the sheer volume and subjective nature of content. This project aims to automate the classification of tweets into:

- **Hate Speech** (Label 0)
- **Offensive Language** (Label 1)
- **Neither** (Label 2)

---

##  Objective

- Develop a system to classify tweets into three categories.
- Compare two approaches:
  - Traditional Machine Learning: **TF-IDF + Logistic Regression**
  - Deep Learning: **GloVe Embeddings + LSTM**

---

##  Dataset Description

Each entry in the dataset contains:
- **tweet**: Text of the tweet.
- **label**:
  - `0`: Hate Speech
  - `1`: Offensive Language
  - `2`: Neither

---

##  Methodologies

### 🔸 Traditional Classifier: TF-IDF + Logistic Regression
- Tweets are converted to numerical feature vectors using **TF-IDF**.
- A **Logistic Regression** model is trained for classification.
- Efficient and interpretable but may miss deep contextual patterns.

### 🔹 Deep Learning Model: GloVe + LSTM
- **GloVe Embeddings** provide semantically rich vector representations.
- Passed through an **LSTM** network to capture context and dependencies in the tweet.
- Better suited for understanding nuanced language patterns.

---

##  Data Splitting Strategy
- Used **Random Sampling** to split the data into training and testing sets while maintaining class distribution.
- Helps in generalization and avoids overfitting.

---

##  Performance Evaluation

### ➤ Before Balancing
- LSTM model showed **low accuracy** due to class imbalance.

### ➤ After Balancing
- Accuracy improved from **78% to 88%**.
- Traditional model achieved **84% accuracy**.

---

##  ROC Curve
- ROC curve was plotted for external test evaluation (details in notebook).

---

##  Conclusion

- **TF-IDF + Logistic Regression**:
  - Easy to implement and fast.
  - Accuracy: **84%**
- **GloVe + LSTM**:
  - More complex and powerful.
  - Accuracy: **88%** (after addressing class imbalance)
- Deep learning models outperform traditional ones when provided with balanced and well-preprocessed data.

---

##  Source Code

You can access the full implementation here:  
🔗 [Google Colab Notebook](https://colab.research.google.com/drive/123DngHBj80vTEU5tu0Y7gS8ZOj_PcN42?usp=sharing)
🔗 [Dataset]([text](https://www.kaggle.com/datasets/mrmorj/hate-speech-and-offensive-language-dataset))
