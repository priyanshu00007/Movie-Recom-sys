# Movie Recommendation System

This project implements a simple movie recommendation system based on content-based filtering. It uses movie overview, genre, keywords, cast, and crew information to suggest similar movies.

## Features

-   **Data Merging**: Combines movie metadata and credit information from two separate datasets.
-   **Data Preprocessing**: Cleans and transforms text-based features (genres, keywords, cast, crew, overview) into a suitable format for machine learning.
-   **Text Vectorization**: Uses CountVectorizer to convert text data into numerical vectors.
-   **Similarity Calculation**: Employs cosine similarity to measure the likeness between movie vectors.
-   **Recommendation Engine**: Provides a function to recommend movies based on a given movie title.

## Technologies Used

-   Python
-   Pandas (for data manipulation)
-   scikit-learn (for CountVectorizer and cosine_similarity)
-   NLTK (for stemming)
-   `ast` (for safe evaluation of string literals)

## Setup

To run this project, you will need the following:

1.  **Python Environment**: Ensure you have Python (3.7+) installed.
2.  **Install Dependencies**: Install the required Python libraries using pip:
    ```bash
    pip install pandas scikit-learn nltk
    ```
3.  **Download Data**: Obtain the `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` datasets. These files are typically available from platforms like Kaggle. Place them in the same directory as your notebook or script.

## Usage

1.  **Load the Notebook**: Open and run the provided Jupyter/Colab notebook (`movie_recommendation.ipynb`).
2.  **Generate Recommendation Files**: The notebook will process the data and generate two pickle files:
    -   `movienew.pkl`: A dictionary containing movie IDs, titles, and processed tags.
    -   `similarity.pkl`: A matrix storing cosine similarity scores between all movies.
3.  **Use the `recommend` function**: Once the notebook cells are executed, you can use the `recommend` function to get movie suggestions:

    ```python
    # Example usage:
    recommend("Avatar")
    ```
    This will output a list of the top 5 most similar movies to 'Avatar'.

## Example

```python
# After running all the cells in the notebook:
recommend("Batman Begins")
```

**Output (example)**:
```
The Dark Knight Rises
Raising Helen
The Dark Knight
Batman Forever
Synecdoche, New York
```
