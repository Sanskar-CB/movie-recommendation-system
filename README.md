# 🎬 Movie Recommendation System

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange.svg)
![Surprise](https://img.shields.io/badge/Surprise-SVD-yellow.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

An **end-to-end Machine Learning project** combining **Content-Based Filtering (TF-IDF & Cosine Similarity)** and **Collaborative Filtering (Matrix Factorization using SVD)** to deliver accurate and personalized movie recommendations.

---

# 📌 Overview

Traditional recommendation systems often struggle with either the **cold-start problem** or the inability to effectively capture user preference dynamics. This project introduces a **hybrid recommendation framework** that combines:

- 🎥 Content-Based Filtering using movie metadata and plot descriptions
- ⭐ Collaborative Filtering based on user rating patterns
- 📄 TF-IDF Vectorization & Cosine Similarity
- 🤖 Matrix Factorization using Singular Value Decomposition (SVD)

By integrating content information with collaborative user behavior, the system provides personalized recommendations for both **movie titles** and **individual users**.

---

# 🚀 Features

- 🎥 Content-Based Recommendation using TF-IDF & Cosine Similarity
- ⭐ Collaborative Filtering using SVD Matrix Factorization
- ⚙️ Automated Metadata Combination & Feature Engineering
- 📈 Model Performance Evaluation (RMSE)
- 📊 Synthetic Dataset Support for Scalability
- 🤖 Hybrid Recommendation Capability
- 💾 Model Saving & Loading
- 📋 Clean Recommendation Output

---

# 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Language | Python |
| Machine Learning | Scikit-learn, Surprise |
| Data Processing | Pandas, NumPy |
| NLP | TF-IDF Vectorizer |
| Visualization | Matplotlib, Seaborn |
| Environment | Google Colab / Jupyter Notebook |

---

# 📂 Dataset

The project uses two datasets:

## 🎬 Movies Dataset

Contains movie metadata including:

- Movie ID
- Movie Title
- Genres
- Plot Description

## ⭐ Ratings Dataset

Contains user interaction data including:

- User ID
- Movie ID
- Explicit Rating (1–5)

### Features Used

- Genres (`Action`, `Drama`, `Sci-Fi`, `Comedy`, `Romance`, etc.)
- Plot Summaries
- User Rating History

---

# 🧠 Model Architecture

## 1️⃣ Content-Based Recommendation

A **TF-IDF + Cosine Similarity** pipeline consisting of:

- English Stop-word Removal
- TF-IDF Feature Extraction
- Cosine Similarity Matrix
- Top-N Similar Movie Ranking

---

## 2️⃣ Collaborative Recommendation

A **Singular Value Decomposition (SVD)** model is trained on the user–movie rating matrix to predict unseen ratings.

### Configuration

| Parameter | Value |
|-----------|-------|
| Algorithm | SVD |
| Latent Factors | 20 |
| Rating Scale | 1–5 |
| Evaluation | RMSE |

---

# 🔄 Workflow

```text
Input Query (Movie Title / User ID)
                 │
  ┌──────────────┴──────────────┐
  ▼                             ▼
Content-Based Engine     Collaborative Engine
(TF-IDF + Cosine)         (SVD Matrix Factorization)
  │                             │
  ▼                             ▼
Similar Movies List     Predicted User Ratings
  │                             │
  └──────────────┬──────────────┘
                 ▼
      Final Recommendation Output
```

---

# ⚙️ Methodology

## Step 1 – Data Collection

Movie metadata and user ratings are collected for model training and evaluation.

| Dataset | Purpose |
|---------|----------|
| Movies Metadata | Content-Based Filtering |
| User Ratings | Collaborative Filtering |

---

## Step 2 – Feature Engineering

Text preprocessing includes:

- Combining genres and descriptions
- Text cleaning
- Stop-word removal
- TF-IDF Vectorization

---

## Step 3 – Content-Based Similarity

```text
Movie Metadata
        │
        ▼
TF-IDF Vectorizer
        │
        ▼
Cosine Similarity Matrix
        │
        ▼
Top-N Similar Movies
```

---

## Step 4 – Collaborative Filtering

User rating records are transformed into the **Surprise** dataset format and trained using the **SVD algorithm** to estimate missing ratings.

---

## Step 5 – Recommendation Generation

### 🎬 Movie Title Query

Returns the **Top-N most similar movies** based on cosine similarity.

### 👤 User ID Query

Predicts ratings for unseen movies and recommends the highest-rated titles.

---

# 📈 Results

## Collaborative Filtering Performance

| Metric | Value |
|---------|-------|
| Algorithm | SVD |
| Train/Test Split | 80% / 20% |
| Evaluation Metric | RMSE |
| Test Score | **1.1909** |

The SVD model successfully predicts ratings for unseen movies and generates personalized recommendations based on user preferences.

---

## Content-Based Recommendation

The TF-IDF model effectively identifies movies with similar genres and narrative structures.

### Example Recommendations

| Input Movie | Similar Recommendations |
|-------------|------------------------|
| Inception | The Matrix |
| Inception | Interstellar |
| Avatar | Guardians of the Galaxy |
| Titanic | The Notebook |

---

# 📊 Generated Outputs

The project generates:

- 🎬 Top-N Movie Recommendations
- ⭐ Personalized User Recommendations
- 📊 RMSE Evaluation
- 📈 Similarity Score Matrix
- 💾 Trained SVD Model
- 📋 Recommendation Reports

---

# 📁 Project Structure

```text
movie-recommendation-system/
│
├── data/
│   ├── movies.csv
│   └── ratings.csv
│
├── notebooks/
│   └── Movie_Recommendation.ipynb
│
├── models/
│   └── svd_model.pkl
│
├── outputs/
│   ├── recommendation_results.csv
│   └── evaluation_report.txt
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

# ▶️ Installation

## Clone the Repository

```bash
git clone https://github.com/yourusername/movie-recommendation-system.git

cd movie-recommendation-system
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run the Notebook

```bash
jupyter notebook notebooks/Movie_Recommendation.ipynb
```

Or open the notebook directly in **Google Colab**.

---

# 💻 Usage

Run the notebook to:

- Load movie metadata and ratings
- Preprocess textual features
- Train the TF-IDF similarity model
- Train the SVD collaborative filtering model
- Generate movie recommendations
- Predict unseen ratings
- Evaluate model performance
- Save trained models

---

# 📚 Applications

- 🎥 Streaming Platforms (Netflix, Prime Video, Disney+)
- 🛒 E-commerce Product Recommendation Systems
- 📰 Content Personalization Platforms
- 🎵 Music Recommendation Systems
- 📚 Book Recommendation Engines
- 🛍️ Personalized Shopping Experiences

---

# 🔮 Future Improvements

- Hybrid Score Fusion (Content + Collaborative)
- Neural Collaborative Filtering (NCF)
- Deep Learning Recommendation Models
- Real-Time User Feedback Learning
- Movie Poster Embedding using Computer Vision
- Explainable Recommendations
- Transformer-based Recommendation Systems

---

# 📖 References

- MovieLens Dataset
- Scikit-learn Documentation
- Surprise (scikit-surprise) Documentation
- TF-IDF Vectorization
- Cosine Similarity
- Singular Value Decomposition (SVD)

---

# 👨‍💻 Author

**Sanskar Saxena**

**B.Tech – Information Technology**

**Harcourt Butler Technical University (HBTU), Kanpur**

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub!

---

## 📜 License

This project is licensed under the **MIT License**.
