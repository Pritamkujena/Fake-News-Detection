# Fake-News-Detection
This project involves the implementation of a machine learning pipeline to detect fake news.
Data Loading and Preparation:

Two datasets are loaded: one containing fake news articles and the other containing true news articles.
Each dataset is labeled with a class column where 0 represents fake news and 1 represents true news.
Data Splitting for Manual Testing:

The last 10 rows from each dataset are separated for manual testing purposes.
These rows are removed from the main datasets to ensure the models are not trained on them.
Data Merging and Cleaning:

The remaining data from both datasets are merged into a single dataframe.
Unnecessary columns (title, subject, date) are dropped.
The data is shuffled to ensure random distribution and prevent any bias.
Text Preprocessing:

A preprocessing function (wordopt) is defined to clean the text by:
Converting to lowercase
Removing punctuation, numbers, and special characters
Removing URLs, HTML tags, and extra whitespace
Feature Extraction:

The cleaned text data is converted into numerical vectors using TF-IDF Vectorizer. This step transforms the text into a format suitable for machine learning algorithms.
Model Training and Evaluation:

The data is split into training and testing sets.
Four different machine learning models are trained on the training set:
Logistic Regression (LR)
Decision Tree (DT)
Gradient Boosting Classifier (GBC)
Random Forest Classifier (RFC)
Each model is evaluated on the testing set, and performance metrics such as accuracy and classification reports are generated.
Manual Testing Function:

A function is defined to test new, unseen news articles by predicting whether they are fake or true using the trained models.
The function cleans the input text, transforms it using the TF-IDF Vectorizer, and makes predictions using each of the four models.
Overall, this project demonstrates a comprehensive approach to detecting fake news by leveraging data preprocessing, feature extraction, and multiple machine learning models to achieve accurate classification.
