## 🧠 Predictive Keyboard using LSTM

This project demonstrates how a predictive text system — similar to the ones found in mobile keyboards — can be built using a **Long Short-Term Memory (LSTM)** neural network. It learns from text data to suggest possible next words based on the previous few words in a sentence.

---

## 📖 Overview

The model is trained on **Sherlock Holmes stories** to learn language patterns and predict what word is most likely to follow a given sequence of words.
It combines concepts from **natural language processing (NLP)** and **sequence modeling** using deep learning.

This project provides a foundational understanding of:

* How words can be represented numerically for machine learning.
* How sequential context influences text prediction.
* How LSTM networks capture dependencies in language.

---

## 🧰 Key Steps

### 1. **Data Preparation**

The text data (Sherlock Holmes stories) was converted to lowercase and tokenized into individual words. This ensures uniformity and helps the model recognize patterns more efficiently.

### 2. **Vocabulary Building**

A vocabulary of all unique words in the dataset was created, assigning a unique index to each word. This mapping allowed the model to work with numerical representations instead of raw text.

### 3. **Sequence Creation**

The dataset was transformed into short word sequences. For each set of three input words, the fourth word was treated as the prediction target.
This is how the model learns to predict the “next word” based on context.

### 4. **Model Architecture**

A custom LSTM model was built using three key components:

* **Embedding Layer** to represent words as dense numerical vectors.
* **LSTM Layer** to learn relationships between consecutive words.
* **Fully Connected Layer** to output probabilities for every word in the vocabulary.

### 5. **Training**

The model was trained to minimize prediction error using **cross-entropy loss** and the **Adam optimizer**.
Although trained on a small subset for speed, it successfully captured basic patterns and could make reasonable predictions for simple phrases.

### 6. **Next Word Prediction**

After training, the model can take a short text prompt and predict the most likely next word.
For instance, given a phrase like *“So, are we really at”*, the model might suggest common next words such as *“the”*, *“my”*, or *“,”* based on learned patterns from the dataset.

---

## 📊 Results & Insights

* The model demonstrates the core principles of **language modeling** using neural networks.
* Even though it wasn’t trained on a massive dataset, it learns frequent word transitions and syntax structures.
* Predictions become more fluent and meaningful with longer training, a larger dataset, and optimized hyperparameters.

---

## 🚀 Future Improvements

* Introduce **mini-batch training** for efficiency.
* Increase the dataset size and training epochs for better accuracy.
* Add **regularization** techniques such as dropout layers to prevent overfitting.
* Experiment with **bidirectional LSTMs** or **transformer-based architectures** (like GPT).
* Deploy the model in a **Streamlit web app** to allow real-time word suggestions.

---

## 📚 Concepts Covered

* Text preprocessing and tokenization
* Vocabulary creation and word embeddings
* Sequence-to-one prediction using LSTM
* Probabilistic text generation
* Fundamentals of NLP language modeling

---

## 🏁 Conclusion

This project highlights the foundation of predictive text systems and demonstrates how LSTM models can capture word relationships in language.
While it’s a simplified version of what modern keyboards use, it offers valuable insight into **sequence prediction**, **text generation**, and **deep learning for NLP**.

---
