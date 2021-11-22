# Creating a Sentiment Analysis Web App
## Using PyTorch and SageMaker

The deployment project is intended to be done using Amazon's SageMaker platform. In this project there is a working notebook instance which presents Sentiment analysis of IMDB movie reviews dataset using LSTM model which we are going to deploy on high level and low level, and test it using a web app service (HTTP POST) via an endpoint (LAMBDA function + API gateway)
This project is the fifth requirement to graduate from Udacity's Deep learning Nano-degree.

### General Outline
Recall the general outline for SageMaker projects using a notebook instance.

* Download or otherwise retrieve the data.
* Process / Prepare the data.
* Upload the processed data to S3.
* Train a chosen model.
* Test the trained model (typically using a batch transform job).
* Deploy the trained model.
* Use the deployed model.

For this project, you will be following the steps in the general outline with some modifications.

First, you will not be testing the model in its own step. You will still be testing the model, however, you will do it by deploying your model and then using the deployed model by sending the test data to it. One of the reasons for doing this is so that you can make sure that your deployed model is working correctly before moving forward.

In addition, you will deploy and use your trained model a second time. In the second iteration you will customize the way that your trained model is deployed by including some of your own code. In addition, your newly deployed model will be used in the sentiment analysis web app.

## This repo contains:
* `SageMaker Project.ipynb` leads you through each of the steps and contains coding tasks and questions for you to complete
* `train folder` has the code for training the model
* `train.py` is the training script to which you will make some modification
* `serve folder` has the code for the deployed the model
* `predict.py` is the predicting script to which you will make some changes
* `website folder` has the code for interacting with the endpoint
* `index.html` needs to be set up to work with your own endpoint
