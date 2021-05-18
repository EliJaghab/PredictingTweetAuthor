# Predicting the Author of a Tweet

This R Notebook uses a Naive Bayes model to predict the author of a tweet.

First I read in and analyzed the raw data. I create a variable to compare to the prediction values I get from the test set. Then I examine the distribution of the data which was equal for each author. 

I then build and examine a Vcorpus which is a body of docs to hold the all of the tweets. I examine the first tweet in the corpus to see the format of the tweet. I decide to remove any data that will not contribute to identifying the author. This includes urls, punctuation, white space, numbers and the word ‘amp.’ I also lower case all the letters of each tweet. After cleaning the data, I compare the cleaned tweet to the original and am satisfied with the changes.

Then I create a document matrix which uses all of the words tweeted and uses these as headers on the x axis and on the y axis are the tweet numbers and whether or not the word is included in the tweet. I build a training and test data set out of this document matrix and create a vector of frequently occurring words. After this, I convert each value to either yes or no depending on whether the word is included in the tweet. 

Finally, I run the Naive Bayes Model on the training set and run a prediction on the test set to get the matrix of the model. After running the model, I receive a score of 84% accuracy. This model did the best job in precision for Donald Trump with 90%. This means that the model had a small number of false positives for him. This makes sense because Trump’s tweets are typically distinct and most likely stood out against the other authors. On the other hand, Barry had the highest Recall score with 92%. This means that the model identified a small number of false negatives associated with Barry.
