## Netflix Recommendation System

## Overview
This project explores the Netflix dataset and builds a **content-based recommendation system** using different approaches.

Currently, the project includes:
- Data cleaning and analysis
- A TF-IDF based recommendation system
- An embedding-based recommendation system

The goal is to progressively improve recommendation quality by experimenting with different techniques.

---

## Objectives
- Clean and prepare the Netflix dataset
- Perform exploratory data analysis (EDA)
- Build a recommendation system
- Understand how different methods impact recommendation quality

---

## Dataset
The dataset contains information about Netflix titles, including:
- Title
- Type (Movie / TV Show)
- Genres (`listed_in`)
- Description
- Director
- Cast
- Release year

---

## Recommendation Approaches

### 1️⃣ TF-IDF Based System
- Uses text vectorization
- Measures similarity based on word overlap
- Serves as a baseline model

📁 `03_recommendation_tfidf.ipynb`

---

### 2️⃣ Embedding-Based System
- Uses Sentence Transformers (`all-MiniLM-L6-v2`)
- Captures semantic meaning of text
- Produces more context-aware recommendations

📁 `04_recommendation_embeddings.ipynb`

---

## Methodology

### Feature Engineering
We combine multiple columns into a single text representation:

- Genres (`listed_in`)
- Description
- Director
- Cast
- Type

This allows the model to compare titles using richer context.

---

### Similarity Computation

#### TF-IDF
- Vectorization using `TfidfVectorizer`
- Similarity using cosine similarity

#### Embeddings
- Pretrained model from `sentence-transformers`
- Dense vector representation of text

----

## Project Structure
Netflix-data-analysis/
│
├── data/
│ └── netflix.csv
│
├── notebooks/
│ ├── 01_data_cleaning.ipynb
│ ├── 02_data_analysis.ipynb
│ ├── 03_recommendation_tfidf.ipynb
│ └── 04_recommendation_embeddings.ipynb
│
├── README.md
└── requirements.txt

---

## 🧪 Tools Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Sentence Transformers
- JupyterLab