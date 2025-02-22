# Content-Based Movie Recommendation System

## Overview
This project implements a simple content-based movie recommendation system. Given a user’s input query, the system returns the top matching movies based on textual similarity. The recommendation system utilizes TF-IDF vectorization and cosine similarity to measure the relevance of movies in the dataset.

## Dataset
- **Download Dataset**: [IMDB Movies Dataset](https://www.kaggle.com/datasets/amanbarthwal/imdb-movies-data)
- **movies.csv**: Contains ~100–500 movies with various attributes such as `Title`, `Genre`, `Director`, `Cast`, and `Description`.
- These attributes are used to construct a meaningful representation of each movie.

## Setup
### Prerequisites
- **Python**: 3.8+
- **Dependencies**:
  ```bash
  pip install -r requirements.txt
  ```
  Ensure `pandas` and `scikit-learn` are installed.

## Implementation
### 1. Load and Preprocess Data
- Reads the `imdb-movies-dataset.csv.csv` file.
- Extracts relevant textual fields: `Title`, `Genre`, `Director`, `Cast`, and `Description`.
- Fills missing values with empty strings.
- Creates a `combined_features` column by merging the selected text fields.

### 2. Build the TF-IDF Matrix
- Uses TF-IDF vectorization to convert text data into numerical format.
- Removes common stop words to improve accuracy.

### 3. Define the Recommendation Function
- Transforms user input into a TF-IDF vector.
- Computes cosine similarity with all movies in the dataset.
- Retrieves the top `n` most similar movies based on similarity scores.

## Running the Recommendation System
### Steps:
1. Clone or download this repository.
2. Ensure dependencies are installed.
3. Open and run the Jupyter Notebook (`content_recommender.ipynb`).
4. Test with different user queries.

### Example Queries:
```python
query1 = "I love thrilling action movies set in space, with a comedic twist."
query2 = "Show me some romantic comedies with famous actors."
query3 = "A mystery thriller featuring detectives and mind-bending twists."
query4 = "Recommend horror movies with supernatural elements."
query5 = "Sci-fi movie with AI and futuristic technology."
```

### Example Output:
```
Top Recommendations:
            Title        Genre   Director  ...
1  Guardians ...  Action, Sci-Fi James Gunn ...
2  Spaceballs     Sci-Fi,Comedy Mel Brooks ...
...
```

## Short Video Demo
Check `demo.md` for a quick walkthrough.

## Evaluation Criteria
- **Functionality**: Produces relevant movie recommendations.
- **Code Quality**: Clear workflow and well-commented code.
- **Clarity**: README provides a simple and understandable guide.
- **Recommendation Logic**: Uses TF-IDF and cosine similarity.

**Enjoy building and experimenting with movie recommendations!**
