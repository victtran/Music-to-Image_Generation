# Music-to-Image Generation Project README

## Introduction

The goal of this project is to enhance the visual representation of songs by generating images based on key phrases from song lyrics and associated audio sentiments. Below is an overview of the project's objectives, approach, and key components.

## Project Overview

- **Objective:** Transform songs into informative visual representations by combining sentiment analysis, text preprocessing, and image generation techniques.
- **Datasets:** Utilized the MuSe dataset, which contains sentiment information for 90,001 songs derived from Last.fm social tags, and incorporated audio features from the Spotify API.
- **Technologies:** Python, machine learning libraries, text analysis tools, and pre-trained text-to-image models.

## Approach

### Data Preprocessing

- Extracted audio features from the Spotify API.
- Scraped lyrics from Genius.com and preprocessed them by removing punctuation, tokenizing, removing stop words, lemmatizing, and filtering out profanity.
- Reduced the dimensionality of text features to the top 5,000 most frequent words.

### Multi-Label Classification

- Developed Multi-Label Random Forest models, experimenting with Binary Relevance and Classifier Chains techniques.
- Predicted audio sentiments for associated words and lyrics, ROC Score of 0.74.

### Image Generation

- Extracted 5 key phrases from lyrics using KeyBERT.
- Predicted the top 3 emotions behind the music using Multi-Label Audio Sentiment Classifiers.
- Merged sentiment and key phrases to generate images using both Open DallE and MidJourney and compared the results.
