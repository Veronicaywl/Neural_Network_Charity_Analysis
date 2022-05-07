# Neural_Network_Charity_Analysis
## Overview of the analysis
We will use TensorFlow along with deep-learning neuron network to perform analysis for the charity donation. The methods that we will be using in this project: 
- Preprocessing data, drop the columns that are not relevant to this analysis.
- Complie the dataset and create a train-test split model for evaluation. 
- Optimize the model by using different functions and layers.

## Result
- Data Preprocessing

    - The column `IS_SUCCESSFUL` considered as the target of this analysis. In this column, we can use binary classification to predict whether or not the charity donation was used effectively. 
    - We used columns `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT` as features of the analysis. 
    - We took out the columns of `EIN` and `NAME` from the dataframe because these two columns are not relevant to the deep-learning model. 
    

- Compiling, Training, and Evaluating the Model

    - In this project, we used 2 hidden layers with 80 and 30 neurons with `relu` activation function for the deep-learning model. After the train-test split, there are 25,724 samples and 43 features in this dataset. As we will use binary classification for output, we use `sigmoid` function for the output layer. For compilation, we use `adam` optimizer and `binary_crossentropy` loss function. 
    - Since all our model accuracy are below 75%. In this case, the performance is not capable to help us predict the outcomes of charity donations. 
    - In order to optimize the model accuracy, we also preprocession `IMCOME_AMT` and `ASK_AMT` for detail analysis. We bucketed the `ASK_AMT` feature and rearrage the interval. 
    When all other conditions are the same, we tried to increased the neurons with 2 hidden layers. We've also tried to increased to 3 hidden layers for the dataset, as well as change the activation function. We replaced `relu` function to `tanh` function. However, all methods that we used did not help us increase the model accuracy. 

## Summary
As we aiming the accuracy should be 75% and above, we concluded that the model that we are using is not outperforming. Since we are using binary classification in this project, we should consider using supervised machine learning model such as Random Forest Classifier and combining a decision tree to evaluation the charity donation outcomes. Compared both methods of machine learning to get the higher accuracy scores in this project.  
