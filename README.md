# Movie Recommendation Systems

A portfolio project demonstrating two complementary movie recommendation approaches: content-based filtering with TF-IDF and cosine similarity, and ratings-based collaborative filtering with k-nearest neighbors.

## Overview

This repository preserves and curates recommendation-system work originally completed in **2022**.

Two approaches are presented:

1. **Content-Based Recommendation** — recommends movies using descriptive metadata such as genres, keywords, tagline, cast, and director.
2. **Ratings-Based Recommendation** — recommends movies from user-rating patterns using an item-based nearest-neighbors approach.

The repository was later organized and documented for portfolio presentation while preserving the original analytical concepts.

## Methods

### Content-Based Recommender

Movie metadata is combined into a text representation and transformed using **TF-IDF**. Pairwise movie similarity is then calculated with **cosine similarity**.

Key techniques:

- Text feature engineering
- TF-IDF vectorization
- Cosine similarity
- Approximate title matching

### Ratings-Based Recommender

User ratings are transformed into a sparse movie-user matrix. An item-based **k-nearest neighbors** model with cosine distance identifies movies with similar audience-rating patterns.

Key techniques:

- Collaborative filtering
- Sparse matrices
- k-nearest neighbors
- Cosine distance
- User-rating analysis

## Example Recommendations

For **Iron Man**, the content-based model identifies closely related superhero films such as *Iron Man 2*, *Iron Man 3*, *The Avengers*, and *Captain America: Civil War*.

The corrected ratings-based model for **Iron Man (2008)** identifies movies with similar audience-rating patterns, including *The Dark Knight (2008)*, *WALL·E (2008)*, *The Avengers (2012)*, *Iron Man 2 (2010)*, *Avatar (2009)*, and *Batman Begins (2005)*.

## Repository Structure

```text
Movie-Recommendation-Systems/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── 01_Content_Based_Movie_Recommender.ipynb
│   └── 02_Ratings_Based_Movie_Recommender.ipynb
└── data/
    └── README.md
```

## Data

The original project used movie metadata and movie-rating datasets. The raw data files are not included in the portfolio package until their original distribution sources and licensing terms are documented.

See [`data/README.md`](data/README.md).

## Technologies

- Python
- Pandas
- SciPy
- Scikit-learn
- Jupyter Notebook
- TF-IDF
- Cosine Similarity
- k-Nearest Neighbors

## Portfolio Note

The original recommendation-system work was completed in **2022**. This repository was later curated for portfolio presentation.

During curation, a movie-to-matrix row mapping issue in the original ratings-based notebook was corrected. The underlying collaborative-filtering approach remains the same, but the selected movie is now mapped through its `movieId` before nearest-neighbor lookup.
