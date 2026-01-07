# 🧠 Universal Customer Feedback Analyst

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://huggingface.co/spaces/mahaan-4/Universal-Customer-Feedback-Analyst)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An **End-to-End Machine Learning Platform** that turns unstructured customer reviews into actionable strategic insights. Unlike generic sentiment tools, this system uses a **custom-trained Logistic Regression model** and **Adaptive Unsupervised Learning (LDA)** to discover hidden product issues in real-time.

---

## 🚀 Live Demo
**Try the App here:** [Universal Feedback Analyst on Hugging Face](https://huggingface.co/spaces/mahaan-4/Universal-Customer-Feedback-Analyst)

*(Upload the `test_data.csv` provided in this repo to test the features)*

---

## 💼 Business Value
This dashboard is designed for **Product Managers** and **Strategy Teams** to eliminate manual review reading.
* **Instant Sentiment Audit:** Classifies thousands of reviews in seconds.
* **Pain Point Detection:** Automatically isolates specific keywords driving negative feedback (e.g., "Battery", "Delivery").
* **Universal Adaptability:** The topic model retrains itself on every upload, making it compatible with **any domain** (Electronics, Food, SaaS, Fashion).

---

## 🛠️ Tech Stack & Architecture

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | Streamlit | Professional, responsive dashboard with tabbed UI. |
| **Sentiment Engine** | Scikit-Learn | Custom **Logistic Regression** model (Trained on 174k Flipkart reviews). |
| **Topic Modeling** | LDA (Latent Dirichlet Allocation) | **Unsupervised Learning** to discover hidden themes without labeling. |
| **Visualization** | Plotly Express | Interactive charts (Donut charts, Bar graphs). |
| **Processing** | Pandas & NumPy | Batch processing and vectorization for high-speed inference. |
| **Deployment** | Hugging Face Spaces | Cloud deployment with CI/CD via Git. |

---

## 📊 Key Features

### 1. 🧠 Custom Sentiment Brain (Supervised Learning)
* Trained a custom classifier on 174,000+ labeled reviews.
* Achieved **~95% Accuracy** on the test set.
* Uses **TF-IDF Vectorization** to understand context better than simple dictionary-based tools.

### 2. 🧩 Adaptive Topic Modeling (Unsupervised Learning)
* Implements **Latent Dirichlet Allocation (LDA)** to cluster words into topics.
* **Smart Sampling:** Dynamically adjusts sampling rates based on file size (Small vs. Large datasets) for optimal performance.
* **Sentiment Separation:** Splits topics into "What People Love" (Positive) vs. "What People Hate" (Negative).

### 3. ⚡ High-Performance Engineering
* **Batch Inference:** Optimized prediction pipeline processes 10,000+ rows in <2 seconds.
* **Caching Strategy:** Uses `@st.cache_data` to eliminate redundant computations.

---

## 📂 Project Structure

```bash
├── app.py                   # Main Streamlit Dashboard application
├── requirements.txt         # Dependencies
├── src/
│   ├── data_loader.py       # Data cleaning & preprocessing logic
│   ├── sentiment_engine.py  # Inference logic for the ML models
│   ├── my_custom_model.pkl  # Serialized Sentiment Classifier
│   └── my_vectorizer.pkl    # Serialized TF-IDF Vectorizer
├── data/
│   └── test_data.csv        # Sample dataset for testing
└── README.md                # Documentation
```
## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
