# Movie Recommendation System

A content-based movie recommendation system built with Python, Natural Language Processing (NLP), and cosine similarity. The system analyzes movie metadata to recommend titles similar to a movie selected by the user.

## 📌 Business Problem

Discovering relevant movies in a large entertainment catalog can be time-consuming. Users may want to find films with similar genres, storylines, keywords, cast members, or directors without manually searching through hundreds of titles.

The objective is to develop a recommendation engine that simplifies movie discovery by identifying films with similar content.

## 💡 Analytical Solution

The project uses the TMDB 5000 Movies and Credits datasets to build a content-based recommendation workflow:

- **Data Preparation:** Combined movie and credits datasets, handled missing values, and extracted relevant information from genres, keywords, cast, and crew data.
- **Feature Engineering:** Combined plot overviews, genres, keywords, cast members, and directors into a consolidated text representation for each movie.
- **Text Processing:** Cleaned and prepared movie metadata for vectorization and explored stemming using NLTK.
- **Text Vectorization:** Used Scikit-learn's CountVectorizer to transform movie tags into numerical feature vectors, with a maximum vocabulary size of 5,000 features.
- **Similarity Calculation:** Applied cosine similarity to compare movies based on their feature vectors.
- **Recommendation Generation:** Implemented a recommendation function that retrieves and ranks the five most similar movies for a selected title.
- **Artifact Persistence:** Saved processed movie data and the similarity matrix using Pickle for reuse.

## 🛠️ Technologies Used

- Python
- Pandas and NumPy
- Scikit-learn
- NLTK
- CountVectorizer
- Cosine Similarity
- Jupyter Notebook
- Pickle

## ⚙️ How It Works

1. Load the TMDB 5000 Movies and Credits datasets.
2. Merge the datasets using the movie identifier.
3. Extract genres, keywords, cast members, directors, and plot overviews.
4. Clean and combine the selected attributes into movie tags.
5. Convert the text tags into numerical vectors using CountVectorizer.
6. Calculate cosine similarity between movie feature vectors.
7. Retrieve the five most similar movies for a selected title.

## 🎬 Example

For a selected movie such as *Batman Begins*, the system calculates similarity scores against other movies and returns the five highest-ranked alternatives, excluding the selected title itself.

Recommendations are based on movie metadata similarity rather than user ratings, viewing history, or collaborative filtering.

## 📈 Business Value

The recommendation engine demonstrates how content-based filtering can support digital entertainment platforms by:

- Helping users discover movies with similar themes, genres, or casts.
- Simplifying navigation across large movie catalogs.
- Supporting personalized content discovery features.
- Providing a foundation for more advanced recommendation systems.

These are potential applications; improvements in engagement, watch time, or user retention have not been measured by this project.

## 📁 Saved Artifacts

The notebook saves the following artifacts:

| File | Purpose |
|---|---|
| `movies.pkl` | Processed movie data |
| `movies_dict.pkl` | Dictionary representation of the processed movie dataset |
| `similarity.pkl` | Calculated movie similarity matrix |

## 🚀 Future Improvements

- Apply stemming before vectorization and similarity calculation so it influences the resulting recommendations.
- Use `get_feature_names_out()` for compatibility with newer Scikit-learn versions.
- Build an interactive interface using Streamlit.
- Integrate movie posters, ratings, and additional metadata through a movie database API.
- Evaluate recommendation quality using ranking metrics and user feedback.
- Explore hybrid recommendation methods combining content similarity with ratings or viewing history.

## ⚠️ Disclaimer

This project is intended for educational and portfolio purposes. Recommendations are based on metadata similarity and may not reflect individual user preferences.

## 🔗 Repository

[View the project on GitHub](https://github.com/jaythecool/MovieRecommendationSystem)
