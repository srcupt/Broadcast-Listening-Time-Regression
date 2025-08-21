# Broadcast-Listening-Time-Regression
The goal is to predict how long it will take to listen to a podcast episode based on data from kaggle.

# Dataset Description
+ Link:"https://www.kaggle.com/competitions/playground-series-s5e4/data"

The dataset for this competition (both train and test) was generated from a deep learning model trained on the Podcast Listening Time Prediction dataset. Feature distributions are close to, but not exactly the same, as the original. Feel free to use the original dataset as part of this competition, both to explore differences as well as to see whether incorporating the original in training improves model performance.

Files
- train.csv - the training dataset; Listening_Time_minutes is the target
- test.csv - the test dataset; your objective is to predict the Listening_Time_minutes for each row
- sample_submission.csv - a sample submission file in the correct format.

# Podcast Listening Time Prediction Using XGBoost
This notebook focuses on modeling and predicting the duration listeners spend on podcast episodes. The Kaggle competition challenges participants to accurately forecast listening times based on features like episode length, popularity metrics, sentiment, and advertising data.

Predicting listening time is important for broadcasters and advertisers to optimize content delivery, improve user engagement, and maximize ad effectiveness. By leveraging XGBoost with careful data preprocessing and hyperparameter tuning, this notebook aims to build a robust regression model that captures complex relationships in the data and achieves strong predictive performance.

Overall, this project demonstrates practical machine learning techniques applied to real-world audio consumption behavior, providing valuable insights for the podcast industry.

# Library Imports and Setup
This block imports essential Python libraries for data analysis and visualization:

numpy – for numerical operations
pandas – for data manipulation
matplotlib & seaborn – for data visualization
warnings – to suppress unnecessary warnings
os – for interacting with the operating system

# Data Loading and Initial Preprocessing
This section loads the training, test, and sample submission CSV files from the Kaggle dataset. Then it removes the 'id' column from the training data as it's not useful for modeling.

# Train Data Overview
This command displays the contents of the train DataFrame, allowing us to inspect the loaded dataset. It helps verify the structure, column names, and sample values after loading and preprocessing.

| Podcast_Name    | Episode_Title | Episode_Length_minutes | Genre       | Host_Popularity_percentage | Publication_Day | Publication_Time |
|-----------------|---------------|-------------------------|-------------|----------------------------|-----------------|------------------|
| Mystery Matters | Episode 98    | NaN                     | True Crime  | 74.81                      | Thursday        | Night            |
| Joke Junction   | Episode 26    | 19.80                   | Comedy      | 66.95                      | Saturday        | Afternoon        |
| Study Sessions  | Episode 16    | 73.90                   | Education   | 69.97                      | Tuesday         | Evening          |
| Digital Digest  | Episode 45    | 67.17                   | Technology  | 57.22                      | Monday          | Morning          |
| Mind & Body     | Episode 86    | 10.51                   | Health      | 80.07                      | Monday          | Afternoon        |

