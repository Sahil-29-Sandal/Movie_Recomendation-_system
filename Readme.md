## Content-Based Movie Recommender System (TMDB Dataset)####
 
* This project implements a content-based movie recommendation engine using the TMDB 5000 Movie Dataset. The system analyzes movie metadata (genres, keywords, cast, and crew) to find similarities and recommend movies via an interactive web application built with Streamlit.

*This project follows the machine learning and deployment pipeline often taught in guided projects.

### .. Project Highlights

1 : Recommender Type: Content-Based Filtering.

2  : Similarity Metric: Cosine Similarity (calculated from feature vectors).

3 : Feature Engineering: Combined movie metadata (overview, genres, keywords, cast, crew) into a single tag column, cleaning and stemming the text.

4 : Vectorization: Used CountVectorizer to transform the movie tags into numerical vectors.

5 : Web Application: Hosted using Streamlit, allowing users to select a movie and view the top 5 personalized recommendations along with their posters (fetched via the TMDB API).

## ....Technical Details.... ####

*** The recommendation model relies on the following processing steps:

1 : Data Preparation: Merged movie and credits datasets.

2 : Feature Engineering: Combined movie columns (overview, genres, keywords, cast, crew) into a single text-based tag field.

3 : Cast was limited to the top 3 actors.

4 : Only the director's name was kept from the crew list.

5 : All multi-word features (like "Science Fiction") were concatenated ("ScienceFiction") to ensure they are treated as single search terms.

6 : Vectorization: The tag text was converted into numerical vectors using the CountVectorizer technique (limited to the top 5,000 unique words).

7 : Model Calculation: The Cosine Similarity matrix was calculated across all movie vectors.

## ...How to Run Locally....##

****....You must first generate the model files (.pkl) and then run the Streamlit app.

1. Model Setup

Place your movie datasets (e.g., tmdb_5000_movies.csv) in the project directory.

Run the Jupyter Notebook  to execute the preprocessing steps, calculate the similarity matrix, and save the necessary model files (movie_list.pkl and similarity.pkl) inside a model/ folder.

2. Run the Web App

Install the required libraries (e.g., streamlit, pandas, scikit-learn, requests).

Open your terminal in the project's main directory.

Run the application:

streamlit run app.py


The application will open in your browser, ready for use!