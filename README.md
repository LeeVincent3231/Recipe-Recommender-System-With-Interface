## Table of Contents
1. [Recipe Recommender System With Interface](#recipe-recommender-system-with-interface)
2. [Key Features](#key-features)
3. [Tools and Frameworks](#tools-and-frameworks)
4. [Data Source](#data-source)
5. [Data Preprocessing](#data-preprocessing)
6. [Model Development](#model-development)
    - [TF-IDF Model](#tf-idf-model)
    - [Word2Vec Model](#word2vec-model)
7. [User Interface](#user-interface)
8. [Results](#results)
9. [Future Work](#future-work)

# Recipe-Recommender-System-With-Interface
This project showcases the development of a recipe recommender system that leverages Natural Language Processing (NLP) techniques, including TF-IDF, Word2Vec, and cosine similarity to deliver personalized recipe suggestions based on user preferences. The user-facing interface is built using Streamlit, providing an interactive and intuitive platform for users to explore recipe options that match their preferences.

The project involved aggregating data from over 300,000 recipes, applying thorough data preprocessing techniques such as noise removal and lemmatization to ensure the accuracy of the recommendations.

# Key Features
- **Personalized Recipe Recommendations**: Users receive tailored recipe suggestions based on their input preferences.
- **Interactive Web Interface**: Developed using Streamlit, allowing for easy interaction and intuitive exploration of recipes.
- **NLP Techniques**: Implemented TF-IDF, Word2Vec, and cosine similarity to analyze recipe data and improve recommendation accuracy.
- **Large-scale Dataset**: Aggregated and cleaned data from over 300,000 recipes, ensuring a robust recommendation system.
- **Data Preprocessing**: Applied preprocessing techniques such as noise removal, tokenization, and lemmatization to optimize the quality of the recommendations.

# Tools and Frameworks
- **Python**: pandas, NumPy
- **NLP**: TF-IDF, Word2Vec, cosine similarity
- **Machine Learning**: scikit-learn
- **Web Framework**: Streamlit.io
- **Data Cleaning & Preprocessing**: pandas, nltk (for lemmatization), regular expressions

# Data Source
I have included raw files in the repository. Below is a link to the original source of the datasets.

**Link**: https://eightportions.com/datasets/Recipes/

# Data Preprocessing
Preprocessing is a crucial step in applying NLP techniques and ensuring our final recipe recommender model will accurately read the data. Below are the preprocessing techniques applied.
- **Noise Removal**: Removed irrelevant characters and special symbols from recipe descriptions.
- **Tokenization**: Split recipe descriptions into tokens (words).
- **Lemmatization**: Converted words to their root forms for better generalization of terms.
- **Stopwords Removal**: Eliminated common words that do not contribute to the recommendation (e.g., "and", "the", etc.).

# Model Development
### TF-IDF Model
- **TF-IDF (Term Frequency-Inverse Document Frequency)** was used to represent the text in vector form. Each recipe is vectorized based on its ingredients and other descriptions.
- **Cosine Similarity** is then calculated to recommend recipes that are most similar to the user's preferences.

### Word2Vec Model
- **Word2Vec** is used to create word embeddings that capture the semantic meaning of the words in the recipes. This improves the recommendation accuracy by understanding context beyond just word frequency.
- The model calculates the similarity between user inputs and recipe vectors, returning the most relevant recipes.

# User Interface
The user interface is built using Streamlit, providing an interactive way for users to input their preferences and receive recipe suggestions.
- **User Inputs Preferences**: Users can enter ingredients or select from a list of preferences.
- **Recipe Recommendations**: The system processes these inputs through the trained NLP models and returns a list of recommended recipes.
- **Filters and Sorting**: Users can filter and sort recipes by relevance, rating, or ingredients.

# Results
After performing multiple testing rounds with benchmark questions, the TF-IDF model performed better, being able to suggest more ingredients that matched the user input. Below is a screenshot of how the model performed and what the interface looks like.

![image](https://github.com/user-attachments/assets/a8645eda-06ef-444b-9f6d-1d45e6780fd5)

# Future Work
- **More Rigorious Model Tuning**: Explore in-depth on optimization with regards to key metrics such as cosine similarity in determining the best model between TF-IDF, Word2Vec, or explore other models as well.
- **Deep Learning**: Explore using deep learning models, such as **Transformers**, for even more sophisticated recipe recommendations.
- **Expanded Dataset**: Incorporate additional recipe datasets to further improve the diversity and richness of recommendations.
- **User Ratings and Reviews**: Integrate a feedback loop where users can rate recipes, improving the recommendation system based on user preferences.
