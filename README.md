# Deep Learning Homework: Charity Funding Predictor

## Background 🌎

- The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful
- Utilized the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup

![Charity Funding](/images/1.gif)

**The dataset contains the following columns:**

1. **EIN and NAME** — Identification columns
2. **APPLICATION_TYPE** — Alphabet Soup application type
3. **AFFILIATION** — Affiliated sector of industry
4. **CLASSIFICATION** — Government organization classification
5. **USE_CASE** — Use case for funding
6. **ORGANIZATION** — Organization type
7. **STATUS** — Active status
8. **INCOME_AMT** — Income classification
9. **SPECIAL_CONSIDERATIONS** — Special consideration for application
10. **ASK_AMT** — Funding amount requested
11. **IS_SUCCESSFUL** — Was the money used effectively

## Requirements 👩🏻‍💻

1. Notebook: *Jupyter Notebook*
2. Scripting: *Python Scripting*
3. Libraries Used: *sklearn, pandas, tensorflow, os*

![Coder](/images/2.gif)

## Accomplishments 🎯

### Step 1: Preprocess the data 

- Read in the [Charity Dataset](/Resources/charity_data.csv) to a *Pandas DataFrame* 
    - Target Variable: *IS_SUCCESSFUL*
    - Feature Variables: *Other columns*
- Dropped *EIN* and *NAME* columns
- Deteremined the number of unique values for each column
- Deteremined the number of data points for each unique value
- Performed Binning
- Used *pd.get_dummies()* to encode categorical variables

![DATA DATA](/images/3.gif)

### Step 2: Compile, Train and Evaluate the Model

- Created a neural network model by assigning the number of input features and nodes for each layer using TensorFlow Keras
- Created the first hidden layer and choose and appropriate activation function
- Added a second and third hidden layer with an appropriate activation function
- Created an output layer with an appropriate activation function
- Check the structure of the model
- Compile and train the model
- Create a callback that saves the model's weights every 5 epochs
- Evaluate the model using the test data to determine the loss and accuracy
- Save and export your results to an HDF5 file, and name it AlphabetSoupCharity.h5

![Starter](/images/1.jpg)

### Step 3: Optimize the model

- Optimized the model in order to achieve a target perdictive accuracy higher than 75%
- Adjusted the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as: 
* Dropped only *EIN* column
* Created 3 bins for rare occurrences in columns
* Increased/Decreased the number of values for each bin
* Used different activation functions for the hidden layers
* Reduced the number of epochs to the training regimen

**Results**

By doing the above tweaks, the accuracy of the model increased from *72% to 77%*

![Optimization](/images/2.jpg)

### Step 4: Report on the Neural Network Model 🗒️

**Overview of the Analysis**
- Create an algorithm to predict whether or not applicants for funding will be successful
- Create Binary Classifier using features provided in the dataset that is capable of predicting whether applicants will be successful if funded by Alphabet Soup

**Summary**

If an applicant possesses the following characteristics, they have about an 80% chance of getting accepted:

- The *NAME* of the applicant appears more than 10 times
- The *APPLICATION_TYPE* of the applicant is one of the given types: T3, T4, T6, T5, T19, T8, T7 and T10
- Lastly, the government organization classification is one of these: C1000, C2000, C1200, C3000, C2100

Classification models include logistic regression, decision tree, random forest, gradient-boosted tree, multilayer perceptron, one-vs-rest, and Naive Bayes.

For our classification purposes, the recommended model is *Random Forest Model* which produces about 77% accuracy

![Random Forest](/images/3.jpg)






