# Chris McCarthy: Data Science Portfolio

**Portfolio site:** https://mccarthyleechris.github.io/data-science-portfolio/

Projects in regression, classification, NLP, deep learning, data engineering and data storytelling, mostly using public data on electric vehicles, public health and entertainment. Each project folder has its own README with the question, results, data source and steps to run the notebook.

| Project | Methods | Headline result | Folder |
|---|---|---|---|
| Predicting EV Driving Range | Simple and multiple linear regression, residual diagnostics | R² 0.93; error cut from 49 km to 26 km | [ev-range-prediction](ev-range-prediction/) |
| Washington EV Adoption and Manufacturer Classification | EDA, feature engineering, decision tree, random forest | 81% accuracy (random forest) vs. 64% baseline | [wa-ev-adoption-classification](wa-ev-adoption-classification/) |
| EV and Charging Station Data Pipeline | Web scraping, REST API, SQLite, merging | Three sources merged into one database | [ev-charging-data-pipeline](ev-charging-data-pipeline/) |
| Pitching an International Film to the Netflix Board | Data storytelling, seaborn | Six visuals for a board pitch | [netflix-international-film-pitch](netflix-international-film-pitch/) |
| Movie Review Sentiment Analysis | TF-IDF, TextBlob, VADER, logistic regression, Naive Bayes | 88% accuracy, AUC 0.95 | [movie-review-sentiment-nlp](movie-review-sentiment-nlp/) |
| Movie Recommendation System | Sparse matrix, k-nearest neighbors, cosine similarity | Top-10 similar films for any title | [movie-recommender](movie-recommender/) |
| Handwritten Digit Recognition | CNN, TensorFlow/Keras | 98.8% test accuracy | [mnist-digit-cnn](mnist-digit-cnn/) |
| Respiratory Illness Hospitalizations in Washington | Rate comparisons, rate ratios, linear regression | In progress | Coming soon |

## Data

Datasets are not stored in this repo; several are too large for GitHub. Each project's `data/README.md` links to the original source and says where to save the files.

## Tools

Python, pandas, NumPy, scikit-learn, TensorFlow/Keras, NLTK, matplotlib, seaborn, SQLite, Jupyter

## Contact

- Email: mccarthy.leechris@gmail.com
- GitHub: [mccarthyleechris](https://github.com/mccarthyleechris)
