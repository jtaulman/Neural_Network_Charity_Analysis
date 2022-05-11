# Neural_Network_Charity_Analysis

## Project Overview

I was tasked with using machine learning and neural networks to determine if applicants will be successfull if funded by Alphabet Soup. I was given a csv file containing approximetly 34,000 organizations that already receive funding from Alphabet Soup. There are three parts to this project,

1. Prerocessing the data
2. Compile, Train and Evaluate the Model
3. Optimize the Model

## Results

### Preprocessing

- Target Variable = IS_SUCCESSFUL because the model is attempting to predict which applicants will be successful with funding from Alphabet Soup.

- Feature Variable = APPLICATION_TYPE and CLASSIFICATION are the two featured variables. They are used the most throughout the remainder of the analysis.

- Neither Target nor Feature Variable = EIN and NAME are neither target nor featured variables and therefore were dropped from the data.

### Compile, Train and Evaluate

1. There were 2 hidden layers in this model, with the first containing 80 neurons and the second containing 30 neurons. Both layers used the "relu" activation function, while the ouput layer used the "sigmoid" function.

![Written Analysis 1](https://user-images.githubusercontent.com/95730434/167952479-36f2bc73-ca1c-47aa-87d9-4cf48dc36288.png)

### Optimize

2. The optimal target was 75% for accuracy, which was not obtained. The highest level of accuracy reached was 69% during the first attempt.

![Accuracy 1](https://user-images.githubusercontent.com/95730434/167952936-a74ab57b-6492-461d-9cfb-c3f687c2ba01.png)

3. In an attempt to meet the target of 75% for accuracy, there were a few changed made to the model. First, there was removing an additional column 'USE_CASE', which resulted in a decrease to 55%.

![Attempt 1](https://user-images.githubusercontent.com/95730434/167954191-4be20e1b-7886-4fe5-ab3e-de292e4b7dc1.png)
![Accuracy 4](https://user-images.githubusercontent.com/95730434/167954203-e7b4d3ba-cad9-405a-92ec-34f38e72f3c8.png)

Next, an additional hidden layer added, as well as additional neurons. That decreased the accuracy to 53%.

![Attempt 2](https://user-images.githubusercontent.com/95730434/167953574-d1bd96ef-bddd-49a1-aa31-612207a6f3db.png)
![Accuracy 2](https://user-images.githubusercontent.com/95730434/167953584-0a8d2507-9677-4870-b042-b969ae692ba2.png)

The final attempt consisted of changing the activation function for the ouput layer to "tanh", and the accuracy ended up going down to 47%.

![Attempt 3](https://user-images.githubusercontent.com/95730434/167953634-04e43e4a-d01e-4a59-9515-2eeaefdd2196.png)
![Accuracy 3](https://user-images.githubusercontent.com/95730434/167953641-17e11b6d-320e-4a10-ab6b-fda72da40e7a.png)

## Summary

The model was never able to reach the target accuracy of 75%, but was close with a max of 69%. The accuracy might have increased if more features were removed or if more data was provided in the dataset. Another way the model could be run is with the Random Forest Classifiers because it uses a sufficient amount of estimators. The Random Forest Classifier method is extremely accurate and processes faster, which could solve the issues seen in the neural network model.