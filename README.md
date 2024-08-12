# FakeNews-Prediction

This project demonstrates the use of a Logistic Regression model for detecting whether a news article is real or fake based on its content. The dataset used is from a Kaggle competition.

https://www.kaggle.com/competitions/fake-news/data

Table of Contents
Installation
Usage
Project Structure
Data Collection and Processing
Model Training and Evaluation
Making Predictions
Contributing
License
Installation
To run this project, you need to have Python installed. Clone this repository and install the required dependencies using pip:

bash
Copy code
git clone https://github.com/yourusername/fake-news-detection.git
cd fake-news-detection
pip install -r requirements.txt
Usage
Ensure the dataset train.csv is in the root directory of the project.
Run the main.py script to train the model and make predictions.
bash
Copy code
python main.py
Project Structure
css
Copy code
fake-news-detection/
├── main.py
├── train.csv
├── requirements.txt
└── README.md
main.py: Contains the code for data processing, model training, evaluation, and prediction.
train.csv: The dataset used for training and testing the model.
requirements.txt: Lists the Python dependencies required for the project.
README.md: This file.
Data Collection and Processing
The dataset used for this project is sourced from a Kaggle competition. Each instance contains the following attributes:

id: Unique id for a news article
title: The title of a news article
author: Author of the news article
text: The text of the article; could be incomplete
label: A label that marks whether the news article is real or fake:
1: Fake news
0: Real news
Key steps in data processing:

Load the dataset using pandas.
Replace null values with empty strings.
Merge the author name and news title into a single column.
Separate the features (X) and labels (Y).
Apply stemming to the text data.
Convert the text data to numerical data using TfidfVectorizer.
