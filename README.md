# Data Mining & Machine Learning 2021

Team name: UNIL_Microsoft

Participants: Katelyn Bonner, Ahmed Farhat

Description: 
While learning a new language, reading is essential. However, it may be difficult to find texts to read that match a person's reading level. 
This issue raises the need to create a software tool that predicts a text's academic level in a certain language and recommends articles/readings based on it. 
In order to solve this problem, we decided to build a model that tries to predict the difficulty (from A1 to C2) of a French written text.
At the end, the deliverable will be a Github project repository, where one can find the code for different models we tried.

Our approach: 

Basic models: 

First, we have tested the models presented in the guidlines. The logistic regression model proved to be the hughest performing one.

Data Augmentation: 

We then proceeded by applying some data augmenatation including: entity recognition and count, part of speech recognition and count, the number of words per sentence, average word length, number of stop words per sentence, and the share of stop words in order to add features that may indicate the difficulty of the text. Additionally, we removed stop words and punctuation and converted all words to lowercase. We also tried lemmatizing the words but found that the model performed worse with this which made sense to us given a particular verb conjugation ending can provide evidence to the level of difficulty of the text. After augmenting the data, we then created a bag of words dataframe using the count vectorizer. Finally, we used an ensemble classifier with a decision tree, logistic, knn, and random forest model. 

Pre-trained Model: 

Finally, we decided to try a pretrained model. We searched hugging face’s database of pre-trained models and found the CamemBERT model which is a french version of the BERT model. We use the CamemBERT model with the sequence classification head. This model gave us the best results and so we trained the model on our full data set giving us an accuracy of 60.4% on the unseen data.

Results table summary:

|           | Logistic Regression | KNN        | Decision Tree | Random Forests | Ensemble + Data Augmentation | CamemBert Model |
|-----------|---------------------|:----------:|---------------|----------------|------------------------------|-----------------|
| Precision | 0.4865              | 0.4037     | 0.3464        | 0.3886         | 0.4215                       | 0.5985          |
| Recall    | 0.4854              | 0.3990     | 0.3396        | 0.3969         | 0.3000                       | 0.5948          |
| F1-Score  | 0.4823              | 0.3767     | 0.3305        | 0.3723         | 0.2770                       | 0.5952          |
| Accuracy  | 0.4854              | 0.3990     | 0.3396        | 0.3969         | 0.3000                       | 0.5948          |

Explainatory video link:
