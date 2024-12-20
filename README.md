# Data Mining Project: Movie Recommendation System

## Overview

In today's digital age, numerous platforms allow users to rate and review movies, providing valuable insights into audience preferences. Websites like MovieLens aggregate these ratings, enabling the analysis of user behavior and movie popularity. This project leverages the MovieLens 100K Dataset to build a Movie Recommendation System using clustering techniques. By analyzing user demographics and movie genres, the system aims to provide personalized movie recommendations, enhancing the user experience on streaming platforms and aiding in content curation.

## Motivation

Understanding user preferences is crucial for delivering personalized content in the entertainment industry. By analyzing patterns in user ratings and demographic information, we can develop recommendation systems that not only enhance user satisfaction but also drive engagement and retention. Clustering allows us to group similar users or movies, facilitating more accurate and relevant recommendations.

## Problem to Solve

The primary objective is to develop a recommendation system that suggests movies to users based on their preferences and similarities with other users. Utilizing the MovieLens 100K Dataset, which includes 100,000 ratings from 943 users on 1,682 movies, the system will:

- **Cluster Users:** Group users with similar rating behaviors and demographic profiles.
- **Cluster Movies:** Group movies based on genres and user ratings.
- **Generate Recommendations:** Provide personalized movie suggestions by leveraging the clusters.

By addressing this, we aim to enhance the recommendation accuracy and provide insights into user and movie clustering dynamics

## Data Description

This project utilizes the MovieLens 100K Dataset, a stable benchmark dataset widely used for evaluating recommendation algorithms. The dataset comprises:

- Ratings Data (`u.data`):
    - 100,000 ratings from 943 users on 1,682 movies.
    - Each rating is an integer from 1 to 5.
    - Each user has rated at least 20 movies.
- User Data (`u.user`):
    - Demographic information for 943 users, including:
    - User ID
    - Age
    - Gender
    - Occupation
    - Zip Code
- Movie Data (`u.item`):
    - Information for 1,682 movies, including:
    - Movie ID
    - Movie Title
    - Release Date
    - IMDb URL
    - Genres (19 binary fields indicating genre membership)
- Additional Files:
    - `u.genre`: List of genres.
    - `u.occupation`: List of occupations.
    - `ua.base`, `ua.test`, etc.: Predefined training and test splits for cross-validation.

**Note:** The dataset has been cleaned to include only users with at least 20 ratings and complete demographic information.


## Features

- **User Clustering:** Group users based on demographic information and rating patterns to identify similar user segments.
- **Movie Clustering:** Group movies based on genres and user ratings to identify similar movie categories.
- **Recommendation Engine:** Generate personalized movie recommendations by analyzing user clusters and movie clusters.
- **Data Visualization:** Visualize user demographics, movie genres, and clustering results to gain insights into data distributions and cluster characteristics.
- **Evaluation Metrics:** Assess the performance of the recommendation system using metrics like Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

## Installation

### Prerequisites

Ensure you have Python 3.x installed on your machine. You can download it from [python.org](https://www.python.org/downloads/).

### Setting Up a Virtual Environment (Recommended)

It's recommended to use a virtual environment to avoid conflicts with other projects.

1. Create a virtual environment:
    - **Windows**
        ```bash
        py -m venv venv\
        ```
    - **Linux or Mac**
        ```bash
        python3 -m venv venv/
        ```
2. Activate the environment:
    - **Windows**
        ```bash
        PS> venv\Scripts\activate
        (venv) PS>
        ```
    - **Linux or Mac**
        ```bash
        $ source venv/bin/activate
        (venv) $
        ```

### Installing Dependencies

Install the required packages:
```bash
pip install -r requirements.txt

```

If installed packages add them to requirements.txt. To add all pip packages:
```bash
pip freeze > requirements.txt
```

## Usage

### Running the Recommendation System

1. **Navigate to the Project Directory:**
```bash
cd movie-recommendation-system
```
2. **Ensure the Virtual Environment is Activated:**
    - **Windows**
        ```bash
        PS> venv\Scripts\activate
        (venv) PS>
        ```
    - **Linux or Mac**
        ```bash
        $ source venv/bin/activate
        (venv) $
        ```
3. **Run the Main Script:** The main script orchestrates the data loading, preprocessing, clustering, and recommendation processes.
```bash
python main.py
```
4. **Interact with the System:** Follow the on-screen instructions to:
    - View user and movie clusters.
    - Input a user ID to receive personalized movie recommendations.
    - Explore data visualizations and insights.

## Example Usage
```bash
python main.py
```
Upon running, you might see prompts like:
```bash
Welcome to the Movie Recommendation System!

Please enter User ID to get recommendations (or 'exit' to quit): 

Top 5 movie recommendations for you:
1. Toy Story (1995) - Average Rating: 4.5
2. Star Wars (1977) - Average Rating: 4.4
3. ...
```

## Project Structure

```bash
movie-recommendation-system/
│
├── data/
│   ├── clustering/
│   │   ├── Movie-Clusters.png
│   │   ├── User-Clusters.png
│   ├── processed/
│   │   ├── movies_clustered.csv
│   │   ├── movies.csv
│   │   ├── ratings.csv
│   │   ├── users_clustered.csv
│   │   └── users.csv
│   └── raw/
│       ├── allbut.pl
│       ├── mksu.sh
│       ├── README.md
│       ├── u.data
│       ├── u.genre
│       ├── u.item
│       ├── u.occupation
│       ├── u.user
│       ├── u1.base
│       ├── u1.test
│       ├── u2.base
│       ├── u3.base
│       ├── u3.test
│       ├── u4.base
│       ├── u4.test
│       ├── u5.base
│       ├── u5.test
│       ├── ua.base
│       ├── ua.test
│       ├── ub.base
│       └── ub.test
│
├── notebooks/
│   ├── EDA.ipynb
│   └── Clustering.ipynb
│
├── src/
│   ├── __init__.py
│   ├── data_preprocessing.py
│   ├── clustering.py
│   └── recommendation.py
│
├── tests/
│   ├── __init__.py
│   ├── test_data_preprocessing.py
│   └── test_clustering.py
│
├── .gitignore
├── LICENSE
├── main.py
├── README.md
└── requirements.txt
```

## Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit changes (`git commit -m 'Add YourFeature`').
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

## Authors
- Fernando Villalobos Betancourt [@Villalobos4113](https://www.github.com/Villalobos4113)

## License
This project is under the MIT License - see [LICENSE](https://choosealicense.com/licenses/mit/) for details.