[Back to portfolio site](https://mccarthyleechris.github.io/data-science-portfolio/) · [All projects](../README.md)

# Movie Recommendation System with Collaborative Filtering

If someone liked a movie, which other movies would they probably like too?

This project builds an item-based recommender on the MovieLens ratings data. It finds movies that the same users rated in similar ways, so it needs no information about genre, cast or plot.

## Example output

```
Because you liked: Toy Story (1995)

Recommended movies:
1. Toy Story 2 (1999)
2. Jurassic Park (1993)
3. Independence Day (a.k.a. ID4) (1996)
4. Star Wars: Episode IV - A New Hope (1977)
5. Forrest Gump (1994)
6. Lion King, The (1994)
...
```

A second test with Jumanji (1995) returns The Lion King, Mrs. Doubtfire, The Mask, Jurassic Park and Home Alone: other family movies from the same years.

## Data

- Source: [MovieLens Latest Small dataset (GroupLens)](https://grouplens.org/datasets/movielens/latest/), `ml-latest-small.zip`
- Size: 9,724 movies rated by 610 users
- Files used: `movies.csv` and `ratings.csv` (`links.csv` and `tags.csv` are loaded for reference)

## Approach

1. Merged movies with ratings so each rating has a title.
2. Built a movie-by-user matrix (9,724 × 610) stored as a sparse matrix (`scipy.sparse.csr_matrix`) because most users have rated only a few movies. Unrated movies count as 0.
3. Fit a k-nearest-neighbors model with cosine similarity (scikit-learn `NearestNeighbors`, brute-force search).
4. Wrote a function that takes a movie title and returns the 10 closest movies.

## Repository contents

```
movie-recommender/
├── README.md
├── movie_recommender.ipynb   # full notebook
└── data/                     # MovieLens CSV files (see data/README.md)
```

## How to run

```
pip install pandas numpy scipy scikit-learn jupyter
jupyter notebook movie_recommender.ipynb
```

## Limitations and next steps

Item-based filtering favors popular movies, because they have the most ratings to compare, and it can't recommend a new movie nobody has rated yet. Next, I'd add a minimum-ratings threshold, test matrix factorization (SVD) and measure quality with a held-out set of ratings.

## Tools

Python, pandas, SciPy, scikit-learn, Jupyter

## Citation

F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems 5, 4.
