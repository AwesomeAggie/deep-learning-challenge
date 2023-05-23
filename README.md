## Deep Learning Challenge

## Overview

The purpose of this projecy was to develop a tool to help Alpphaabet Soup select applicants for funding with the best chance at success in their future ventures. The goal was to create a binary classifier based on the dataset provided to predict whether applicants would be successful or not. The objective provided was to create the model to have at least an accuracy score of 75% to be acceptable.

## Results

### Data Reprocessing

The model targets the "IS_SUCCESSFUL" column in the dataset as the target variable. The features would then by every other column that is not the target variable column. The "EIN" and "names" columns were dropped as they were not relevent to the rest of the dataset we used. Once removed the features can be used to predict the target variable inside the model.

### Compiling, Training, and Evaluating the Model

In my first model I used three layes, an input with 100 nuerons, a second hidden layer with 50 nuerons and an output layer with 1 nueron. I used these numbers because it seemed like a good starting point. With 43 input features used I wantged to get at least three times more neurons in the model and although its not exactly three times more I wanted to to be more venly split. I used relu as the activation function for the first two layers and sigmoid for the last layer since the goal was binary classification. I had the model trained with 100 epochs which resulted in an accuracy score of 72.99%. I did not seeing any indication of over or underfitting.

In my second model I tried to optimize the model to improve the accuracy score. I tried to up the neurons to get more results. I was afraid this may overfit the model so I also added two dropout layers with a rate of 0.5 to inhance the generalization. Using these changes I got an accuracy score of 73.00% which wasn't really an improvement at all.

In my third model I decided to get a bit more aggressive by trying to hyperparameter tune the model. I allowed Keras to choose the optimal hyperparameters. This resultes in using "relu" as the activation function for the input layer with 51 nuerons. The following layers were also "relu" and had 20, 7, and 1 nuerons respectively. Using this the model achieved an accuracy score of 73.25% which was the biggest improvemtn I got.

In my final attempt at optimizations I thought maybe the epochs was the problem and I just needed to run more to achieve my score. I set my layers back to their orignal nueron counts but kept the two dropout layers in because they did seem to ever so slightly increase the accuracy from before. I ran the model with 200 epochs instead of 100 epochs. This resulted in an accuracy rate of 73.11%.

## Summary

I was unable to achieve the accuracy score of 75%, so I would not be able to suggest any of my models. I would have to explore other approaches to solving this problem. Using Random Forest Classifier or other preprocessing modifications might result in better results. I could also continue to fiddle with the activations functions, dropout layers, number of layers, and number of nuerons per layer to try an optimize the model further as although my initial attempts did not get up to 75% they all did improve slightly over the initial model.
