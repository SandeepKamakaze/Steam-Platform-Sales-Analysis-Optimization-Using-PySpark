# Stream Platform Sales Analysis & Optimization Using PySpark

This project leverages **PySpark** to analyze the sales performance of games on the **Steam** platform and build a recommendation model based on game features and user engagement. By handling and processing large datasets with PySpark's distributed computing capabilities, the project explores insights into game success, popularity trends, and key performance factors to optimize recommendations and marketing strategies.

## Table of Contents
- [Overview](#overview)
- [Project Goals](#project-goals)
- [Dataset](#dataset)
- [Data Processing and Feature Engineering](#data-processing-and-feature-engineering)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Usage](#usage)
- [Future Work](#future-work)
- [Contributors](#contributors)

## Overview
The gaming industry is highly competitive, with many factors influencing a game's success. This project uses **PySpark** to process and analyze a large dataset of games from the Steam platform. By building classification models and clustering algorithms, it aims to predict game success, identify customer trends, and provide actionable insights for game development, marketing, and sales optimization.

## Project Goals
- Predict the probability of a game's commercial success based on its attributes.
- Analyze relationships between games to enhance recommendations and improve user experience.
- Segment games by their features and performance metrics to assist with targeted marketing and bundle sales strategies.

## Dataset
The **Steam Games Sales Dataset** is sourced from [Kaggle](https://www.kaggle.com/datasets/nikdavis/steam-store-games) and includes data on:
- Game characteristics: title, genre, publisher, developer, etc.
- User engagement: positive and negative ratings, average playtime, achievements.
- Sales metrics: estimated owners, price, release date, etc.

## Data Processing and Feature Engineering
### Key Steps:
1. **Data Cleaning:** Removed null values and standardized data types.
2. **Feature Engineering:** Applied string indexing, one-hot encoding, and min-max scaling for relevant columns.
3. **Vector Assembler:** Consolidated features for ML models by creating a single vector for easy analysis.
4. **Graph Models:** Used **graph frames** and PageRank to model relationships between games.

### Notable Features:
- **Genres, Platforms, and Categories** were expanded into binary columns to accommodate categorical data.
- **Date Engineering:** Processed release dates to analyze trends over different decades.

## Modeling
The project utilizes **Random Forest** and **Logistic Regression** models to classify games as successful or not based on specific features. These models predict the likelihood of a game's success, providing useful insights for the gaming industry.

### Classification Models:
- **Random Forest Classifier:** Selected for its robustness and ability to manage large datasets.
- **Logistic Regression:** Chosen for its interpretability in binary classification.

### Clustering:
- **KMeans Clustering:** Performed on attributes like ratings, achievements, and price to categorize games into clusters, aiding targeted recommendations and marketing.

## Evaluation
The models were evaluated using **ROC-AUC** and accuracy metrics:
- **Random Forest** achieved an accuracy of 80.94%.
- **Logistic Regression** showed an AUC of 0.82, demonstrating reliable prediction capabilities.
- **Silhouette Score** for KMeans clustering was used to identify optimal clusters for the game dataset.

## Usage
### Requirements
- **PySpark** (3.5.1)
- **Python** (3.10)
  
### Running the Project
1. Install dependencies:
   ```bash
   pip install pyspark
    ```

Execute the main notebook or script to process the data, train models, and evaluate results.

# Future Work
Frequent Pattern Mining for bundling insights to improve sales.
Expanded Graph Analytics for deeper insights into game relationships.
Additional Clustering and Segmentation for customer-specific recommendations.
