# Cholesterol Predictor & Health Chatbot

This project was developed during a summer internship at Emirates Aviation University to explore how machine learning and conversational interface can assist in early health screening and awareness.

## Problem Statement

Cardiovascular diseases are increasing worldwide, with high cholesterol levels being a common risk factor. Early detection through prediction of cholesterol levels can aid in preventive health care. Additionally, providing accessible health information via a conversational chatbot can enhance user engagement and awareness.

## Aim

- To develop a multiple linear regression model that predicts cholesterol levels based on age, blood pressire, and heart rate, enabling early health screening.
- To create an interactive health chatbot that provides users with factual health information, such as lifestyle advice related to conditions like high blood pressure.

## Overview

This project combines data-driven machine learning with conversational AI to support early health screening and awareness related to cardiovascular risks.

The first component is a multiple linear regression model that predicts an individual's cholesterol based on easily measurable health indicators such as age, blood pressure, and heart rate.

The second component is a health chatbot designed as an interactive conversational interface. It provides users with factual health information, such as recommended exercises for specific conditions like high blood pressure. Additionally, the chatbot includes a hospital locator feature that allows users to find and view hospitals on a map within a specified city.

By integrating these components, the project aims to empower users with accessible health information and resources, potentially aiding early detection and prevention of cholesterol-related diseases.

## Features

- *Cholesterol Prediction Model*: Uses multiple linear regression to estimate a user's cholesterol level based on age, blood pressure, and heart rate.
- *Interactive Health Chatbot*: Answers factual health-related questions (e.g., lifestyle changes for high blood pressure).
- *Hospital Locator*: When asked, the chatbot shows hospitals in any specified city plotted on a map.
- *User-Friendly Jupyter Notebooks*: Organized into separate notebooks for visualization and chatbot development.
- *Clean Data Visualizations*: Includes seaborn/matplotlib charts that explore correlations in the dataset.

## Tech Stack / Tools Used

-Languages:  
 -Python

-Data Analysis & Visualization:  
 -`numpy`, `pandas` - data manipulation and numerical operations  
 -`matplotlib`, `seaborn` -  plotting and visualization  

-Machine Learning & Modeling:  
 -`sklearn` - regression modeling, text vectorization (TF-IDF), Naive Bayes, Support Vector Classifier  
 -`TextBlob` - sentiment analysis (optional/fallback)

-Natural Language Processing (NLP):  
 -`nltk` - text tokenization, stopword removal, lemmatization  
 -Modules: `punkt`, `stopwords`, `wordnet`, `omw-1.4`

-Chatbot Functionality:  
 -`random` - randomized chatbot replies  
 -`cosine_similarity` (from sklearn) - matching user queries to known responses using vector similarity

-Location Mapping:  
 -`folium` - map visualization of hospitals  
 -`geopy` - geocoding cities to coordinates

-Development Environment:
 -Jupyter Notebook (local)
 -Visual Studio Code (editor)

## Model Details

- *Dataset Used*: The `base_data.csv` file contains anonymized patient data including age, heart rate, blood pressure, and total cholesterol.
- *Target Variable*: `TOTAL CHOLESTROL`
- *Input Features*: `AGE`, `HEART RATE`, `SYS BP`, `DIA BP`
- *Training Process*: The model was trained using multiple linear regression without normalization, assuming linearity between features and target.
- *Evaluation Metrics*: Performance was observed using regression summary statistics and visual correlation plots.

## Chatbot Features

- Responds to factual, health-related queries (e.g., “What is a normal blood pressure range?”).
- Designed using Python with simple logic to detect user intent based on keyword matching.
- Covers topics such as:
  - High blood pressure management
  - Cholesterol-friendly foods
  - Resting heart rate ranges
  - Exercise and hydration tips

## Hospital Locator Feature

- When prompted with queries like “show hospitals in Dubai,” the chatbot fetches geolocation data and plots nearby hospitals on a map.
- Uses the `geopy` library to convert city names into latitude/longitude coordinates.
- Uses the `folium` library to display hospital locations interactively on a map.
- Helps users quickly locate medical facilities in cities of their choice.

