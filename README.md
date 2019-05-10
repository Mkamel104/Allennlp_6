# Training a Sentiment Analyzer using AllenNLP
We will be building and training a  sentiment Analyzer using AllenNLP. Sentiment analysis is a popular text analytic technique used in the automatic identification and categorization of subjective information within text. In this repo we used Bert to train and predict for sentiment, We need to build set of config files to tune different hyper-parameters.

# Training: 
1. We will run below command for three different config files. (replace (name) with the name of config file)

          allennlp train configs/name.json -s ./output/name --include-package classifires
          
          
# Evaluation: 
1. By runing below command and using test.txt file we can evaluate each model. (replace (name) with the correct name of the output folder)

          allennlp evaluate output/name/model.tar.gz  test.txt --include-package classifires
          
          
          
# Prediction:
          
          allennlp predict output/name/model.tar.gz test.txt --include-package model --predictor predictor
