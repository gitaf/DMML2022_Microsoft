# DMML2021_Microsoft

Team name: UNIL_Microsoft

Participants: Katelyn Bonner, Ahmed Farhat

Description: 
Finding text close to someone's knowledge level is quite hard. This issue raises the need to create a software tool that
predicts a user's academic level in a certain language and recommends articles/readings based on it.  
In order to solve this problem, we decided to build a model that tries to predict the difficulty (from A1 to C2) of a French written text.

Our approach:
First, we have tested the models presented in the guidlines. The logistic regression model proved to be the hughest performing one.
We then proceeded by applying some data augmenatation (stop words, ...) <Consequence (better/worse)>
Finally, we decided to go with a pretrained model called CamemBert found on huggingface, which finally gave us our best score.

Results table summary:

Explainatory video link:
