# Sentiment-Prediction

Project Description:
This project uses Deep Learning techniques to classify reviews(for various products) into five sentiment classes. 5 for most positive sentiment and 1 for worst sentiment.
All the DL models used are built and trained using Keras.

NOTE: 
1. All the data files and word embedding files that are used in this project have been uploaded to my google drive. For using these I mount the google drive in the colab 
session and download it from there. 
2. Data files can be found in data folder.
3. For pretrained embeddings use following link to download these or run the code without pretrained embedding.

## Links for downloading pretrained embeddings

* Glove:	https://www.kaggle.com/danielwillgeorge/glove6b100dtxt/download	  	
* Word2vec: 	https://www.kaggle.com/leadbest/googlenewsvectorsnegative300/download
* Fasttext: 	https://dl.fbaipublicfiles.com/fasttext/vectors-english/wiki-news-300d-1M.vec.zip

## Data Files
1. train.csv contains reviews and corresponding sentiments and is used for training models.
2. gold_test.csv is used for testing.

## Imabalanced data
Countplot of reviews present for different classes in training data showed that data is highly imbalanced with around 70% data for class 5 only. Oversampling for all the minority 
class has been used. After oversampling all classes have same number of training examples

## Preprocessing
1. conversion to lower case 
2. removal of punctuations

## Word Embeddnigs 
Different methods for word embeddings have been tried. To use any embedding comment out the code cells for other embeddings except the one to be used. In code.ipynb currently 
GloVe is used.
1. GloVe
2. Word2Vec
3. Fasttext
4. Without pretrained embeddings

Note: For using pretrained embeddings corresponding file I have uploaded the corresponding files in my google drive.

## Architectures tried
1. Feedforward Neural Networks (FFNN)
2. Recurrent Neural Networks (RNN)
3. Transformer Network

Any of the above three architechtures can be used by commenting out code cells for the other two only. By default Bi-GRU a type of RNN is used in code.ipynb file.

## Evaluation Metric
Accuracy, precision, recall and F1 score has been used for evaluating performance of the model. 
Confusion matrix has also been shown.

## LIME for explainability
LIME (Locally Interpretable Model-Agnostic Explanations), which is an algorithm that can explain the predictions of any classifier or regressor in a faithful way, by 
approximating it locally with an interpretable model.
Defintion source: https://www.analyticsvidhya.com/blog/2017/06/building-trust-in-machine-learning-models/

LIME adds explainability to the model by providing sensitivity scores for different words leading towards a particular prediction by the model.

## Deploying a web app using Anvil
A web app has been developed using Anvil which provides a GUI for interacting with the model. 
Link for using the GUI https://sentimentanalysiswithlime.anvil.app/
