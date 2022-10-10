# Neural Network Charity Analysis

## Overview
In this analysis, I used the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results
### Data Preprocessing
![features](https://user-images.githubusercontent.com/106292020/194840483-9628523a-7176-4e81-995e-506cf0114474.PNG)
* The target variable for our model is IS_SUCCESSFUL.
* The features of our model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
![removed](https://user-images.githubusercontent.com/106292020/194840142-96ff811c-6913-45ed-9052-5f10577bb710.PNG)
* The variables that are neither target nor features are EIN and NAME.

### Compiling, Training, and Evaluating the Model
![model](https://user-images.githubusercontent.com/106292020/194840985-414489d1-28e5-475d-a7f5-43fc4d1cced5.PNG)
* In the final model, there were three hidden layers and one output layer. In the first layer, I had 60 neurons then 40 neurons in the second, and 20 neurons in the third layer. For the activation functions, I used relu (first hidden layer), tanh (second hidden layer), relu (third hidden layer), and sigmond (output layer). The activation functions are commonly used in binary classification so I chose them.
![answer](https://user-images.githubusercontent.com/106292020/194841763-3d956f34-e815-465b-94c0-75c837543656.PNG)
* After three optimizations, I was not able to reach the target performance of 75%. 
![change](https://user-images.githubusercontent.com/106292020/194841649-825647d7-a955-4a98-b20c-907a8d5b8e36.PNG)
* To increase model performance, I increased the bin size of OTHER in APPLICATION_TYPE from 200 to 700 then added a third hidden layer and adjusted neurons in each of the layers. Finally, I replaced the second activation function from relu to tanh and increased the epoch time from 100 to 200.

## Summary
The performance of our final optimized model was very similar to that of the first model. Performance decreased slightly, but the difference is negligible. To solve this classification problem, a supervised machine learning model such as a random forest or decision tree model because interpretability is not necessary here. The classifier can decide which applicant will be successful based on the outputs.
