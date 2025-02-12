# deep-learning-challenge

## Report Analysis on Neural Network Model

### Overview

**Purpose**:
* Evaluating the features  in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.
* Evaluating the performance of the neural model to determine if the alphabet Soup can use the model.

#### Results:
 **Data Preprocessing**:
* The target variable for the model  in the given dataset is column:
* 'IS_SUCCESSFUL' column. which is " y" variable
   * y=application_df['IS_SUCCESSFUL'].values 

* The feature variable in our model is the following columns:

 * APPLICATION_TYPE
 * AFFILIATION
 * CLASSIFICATION
 * USE_CASE
 * ORGANIZATION
 * INCOME_AMT
 * SPECIAL_CONSIDERATIONS

* The column "EIN" and "NAME" are droped from the model.since they are neither targets nor features.


  ***first hiden layer***:
* units =80 the input layer takes 80 features to capture a broad range of the pattern in the data.
* activation ='relu' the relu activation function will accelerate the convergence.
* input_dim=43

 ***second hiden layer***:
* units=30
* activation='relu'

***output layer***:
* units=1
* activation ='sigmoid'

* The target model wasnt able to achieve its performance.the is accuracy of 72% .

**Steps taken to increase the performance**:
* Droped more columns.in order the model to capture pattern in data.
   ['EIN','NAME','INCOME_AMT']
* Reduced the input_dim from 43 to 34.

**Optimization method was used to prevent overfitting**
* Batch Normalization Layers:Stabilizes and accelerates training.
* Dropout: prevents overfitting.
* Early Stopping:Monitors validation loss and stops training to prevent overfitting.

* The result after attempting to increase the performance of the model is 73%

  **Summary**:
 * The performance of the model based on the binary classification this model maynot help on predicting that the applicant may or may not be successfull if it is funded.
 * I recommend using different model for this purpose.
 


