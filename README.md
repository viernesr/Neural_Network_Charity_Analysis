# Neural Network Charity Analysis

## Overview

A .csv file was received, containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. The dataset contains a number of columns that capture metadata about each organization. The data has to be preproccessed for a neural network model. The model has to be compiled, trained, and evaluated. Finally, if the model's accuracy does not hit at least 75%, ooptimizations will have to be made for the model, so that the the accuracy can hit the targetted percentage.

## Results

### Data Preprocessing

A couple of notes to keep in mind:
* The variable of interest for the model is: IS_SUCCESSFUL
* All variables were considered, excluding IS_SUCCESSFUL since it is the target variable
* EIN and NAME were dropped because they have no impact on the overall outcome

### Compiling, Training, and Evaluating the Model

The following information, including the number of hidden layers and their number of neurons, the activation functions, and the model performance are listed on the image below:

![alt text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image1.PNG?raw=true)

![alt_text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image2.PNG?raw=true)

Unfortunately, the model was not able to reach the targetted 75%. The accuracy of the model was 69%. So optimizations will have to be made.

#### Attempt 1

An additional feature was removed, more specifically the USE_CASE column. Otherwise, everything else remained the same. However, the model accuracy decreased to 67%.
![alt_text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image3.PNG?raw=true)

![alt_text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image4.PNG?raw=true)

#### Attempt 2

More neurons were added to the hidden layers, plus an additional hidden layer is included in the model. Unfortunately, the accuracy of the model decreased even further to 53%.

![alt_text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image5.PNG?raw=true)

![alt_text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image6.PNG?raw=true)

#### Final Attempt

The activation function of the output layer changed from "Sigmoid" to "tanh." This tanked the model's accuracy to 49%.

![alt_text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image7.PNG?raw=true)

![alt_text](https://github.com/viernesr/Neural_Network_Charity_Analysis/blob/main/Resources/images/image8.PNG?raw=true)

## Summary

The model concluded with an accuracy score of 49%, after three attempts of optimization, which was approximately 20% less than the initlal neural network model. This is because the model overfitted. Further optimizations could be made by removing more features or adding more data to the dataset, which would increase the accuracy. Alternatively, since the accuracy score was not particularly up to standard with neural networks, Random Forest Classifiers could have been used. 
