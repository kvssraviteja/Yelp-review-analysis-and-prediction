A Machine Learning model to predict the actual user rating based on his review, by analyzing previous reviews and ratings. For this, two models are considered, one which has text-based features and other has numerical features which are extracted from the text. It analyze their performance to see which predicts better.
I have taken the database of Yelp reviews and analyzed the dataset. I used the upvotes(cool, funny and useful) to collect only the reviews that are meaningful and actually reflect the rating. Yelp mentioned that good reviews receive more number of upvotes, so used that as a metric in pre-processing.
I performed some other preprocessing steps like, removing stop words, stemming etc. For gathering numerical features out of text, I used AFINN score which is a list containing 2500 words with values from -5 to 5 to convey the valence of the word. Along with this I developed a similar list of words and values, based on the dataset, which gives all the words in all reviews, a value from 0 to 5. For the text-based analysis, I used NBClassifier model and for numerical features we used Logistic regression model.

File Structure:

filtered_yelp1.csv: filtered dataset, which we use in our project(original dataset obtained from: https://www.kaggle.com/yelp-dataset/yelp-dataset)
Dataset Filtering.ipynb: Contains the intial filtering of the dataset
NB_Classifier.ipynb: Contains the implementaion of NBClassifier model on the dataset
Logistic_regression.ipynb: Contains the implementaion of Logistic regression model on the dataset
avgVal.txt, weightSum.txt: files generated by the Logistic_regression.ipynb 