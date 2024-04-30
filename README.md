# deep-learning-challenge

Overview of the analysis: Explain the purpose of this analysis:

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organisations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organisation, such as:

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?

    - "IS_SUCCESSFUL" is the target variable that we are tyring to predict 

What variable(s) are the features for your model?

    - APPLICATION_TYPE—Alphabet Soup application type
    - AFFILIATION—Affiliated sector of industry
    - CLASSIFICATION—Government organisation classification
    - USE_CASE—Use case for funding
    - ORGANIZATION—Organisation type
    - STATUS—Active status
    - INCOME_AMT—Income classification
    - SPECIAL_CONSIDERATIONS—Special considerations for application
    - ASK_AMT—Funding amount requested
    
What variable(s) should be removed from the input data because they are neither targets nor features?

    - EIN and NAME—Identification columns

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why? / What steps did you take in your attempts to increase model performance?

Initial attempt

    - layer 1 = 8 neurons, activation = relu
    - layer 2 = 5 neurons, activation = relu
    - output layer = sigmoid
    - accuracy = 72.5%
    - loss = 55.3%
    
Optimisation 1 

    - layer 1 = 8 neurons, activation = relu
    - layer 2 = 5 neurons, activation = relu
    - layer 3 = 3 neurons, activation = relu
    - output layer = sigmoid
    - accuracy = 72.4%
    - loss = 55.5%
    
Optimisation 2 

    - layer 1 = 100 neurons, activation = relu
    - layer 2 = 30 neurons, activation = tanh
    - layer 3 = 10 neurons, activation = sigmoid
    - output layer = sigmoid
    - accuracy = 72.7%
    - loss = 55.5%
    
Optimisation 3 Auto

    <img width="204" alt="Screenshot 2024-04-30 at 10 51 47 AM" src="https://github.com/patricb98/deep-learning-challenge/assets/145084886/8243ed8f-29b9-45cd-9413-a0119cc21e1b">
    - accuracy = 72.8%
    - loss = 57.4%

    - I took several steps to try and increase my models performance from the initial test 
    - I started the initial test with a basic model to with few neurons and layers using relu activation because I wanted a simple starting point to build on the non linear data. 
    - In the second model I added another layer to try and increase the accuracy but still kept the number of neurons in each layer relatively low. However the accuracy of the model did not really change. 
    - In the third model I tried increasing the number of neurons in each layer and changing the activation to Tanh and Sigmoid to increase accuracy
    - For the fourth model I used an auto optimisation function which suggested 2 layers with lower amounts of neurons in each layer than the third model and utilising relu activation. This model also only resulted in an accuracy of 72.8% which         is the highest out of all four attempts but still under the target accuracy of 75%. 
    
Were you able to achieve the target model performance?

    - Out of all four attempts I was not able to achieve the target model performance of 75%. The closest model to target was the auto optimisation model at 72.8% accuracy


Summary: Summarise the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

    - overall the modifications to the model did not result in a significant increase in accuracy from the initial model to the last attempt 
    - the final auto optimised model did not acheive the target accuracy of 75%
    - taking into account the modifications to each model (increasing neurons, layers and changing activation) did not have any impact on the accuracy I would suggest the next steps of modification would be to reduce the number of columns or creating bins in the columns before disregarding the model. This is because some variables or outliers in the data can cause confusion in models and result in decreased accuracy.  
    - If the additional modifications of reducing columns and adding bins didnot increase the accuracy I would suggest trying a different model to  achieve the target accuracy
    - A different model to use could be a disciion tree as thee are non-parametric learning method used for classification. A decision tree builds the model in the form of a tree strucuture. It breaks down a dataset into smaller and smaller subsets while at the same time an associated decision tree is incrementally developed. 

