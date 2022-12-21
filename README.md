# DMML2021

Team name: UNIL_Microsoft

Participants: Katelyn Bonner, Ahmed Farhat

Description: 
Finding text close to someone's knowledge level is quite hard. 
This issue raises the need to create a software tool that predicts a user's academic level in a certain language and recommends articles/readings based on it. 
In order to solve this problem, we decided to build a model that tries to predict the difficulty (from A1 to C2) of a French written text.
At the end, the deliverable will be a Github project repository, where one can find the code for different models we tried.

Our approach:
First, we have tested the models presented in the guidlines. The logistic regression model proved to be the hughest performing one.
We then proceeded by applying some data augmenatation (stop words, ...) <Consequence (better/worse)>
Finally, we decided to go with a pretrained model called CamemBert found on huggingface, which finally gave us our best score.

Results table summary:

|           | Logistic Regression | KNN        | Decision Tree | Random Forests | Logistic Regression + Data Augmentation | CamemBert Model |
|-----------|---------------------|:----------:|---------------|----------------|-----------------------------------------|-----------------|
| Precision | 0.4863              | 0.4461     | 0.3241        | 0.3655         |                                         |                 |
| Recall    | 0.4854              | 0.4292     | 0.3208        | 0.3740         |                                         |                 |
| F1-Score  | 0.4832              | 0.4117     | 0.3161        | 0.3334         |                                         |                 |
| Accuracy  | 0.4854              | 0.4292     | 0.3208        | 0.3740         |                                         |                 |

Explainatory video link:
