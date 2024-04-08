# deep-learning-challenge

## Overview
This analysis was performed on behalf of Alphabet Soup, a nonprofit foundation that provides funding for other ventures. The purpose of this analysis is to create a model that can select the applicants that have the best chance of succeeding in their ventures. 

The data used to train this model is soucred from 34,000 organizations that have previously received funding from Alphabet Soup. Each organization is catagorized as having been successful or not. 

## Results

### Data Preprocessing
The target variable for the model is encoded as 'IS_SUCCESSFUL' in the dataset, and indicates if the organization was successful in their ventures or not

The dataset contains the following features: 
- Entity's EIN
- Name
- Affiliation : Affiliated sector of industry
- Classification : Government organization classification
- Use Case : Use case for funding
- Organization : Organization type
- Status : Active status
- Income amount : Income classification
- Special considerations : If the application should receive special considerations
- Ask amount : Funding amount requested

The features 'EIN' and 'Name' were removed from the data as they have no bearing on the success of an entity and are unique identifiers. 

### Compiling, Training, and Evaluating the Model
The first iteration of the model had 111 neurons and 3 layers. 

The activation function for the first two layers was relu, and for the output layer was sigmoid. This first model achieved 72% accuracy so was rejected.

In attempts to increase model performance the number of neurons was increased on the second hidden layer from 30 to 80. In addition a hidden layer with 30 neurons and a relu activation function was added. These changes decreased the performance of the model.

The activation functions were all changed to sigmoid, which also decreased model performance.

Finally, the original dataset was modified to exclude the following features : 'AFFILIATION', 'STATUS', 'SPECIAL_CONSIDERATIONS.' These modifications decreased model performance

Ultimately none of these efforts succeeded in prediciting an origanization's success at higher than 75% accuracy and so this model was abandoned. 

## Summary
Ultimately, despite numerous attempts to improve the effectiveness of this model, it was unable to predict an organizations success at the required rate. 

Continued efforts to create a model might consider using a Logistic Regression model or a Random Forest Model. Random Forest would allow the programmer to identify the most important variables to the model, which may increase the change of obtaining the required accuracy rate. 