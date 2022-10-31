# Neural_Network_Charity_Analysis

## Overview of the analysis: 
- Our objectives were to use the features in the provided dataset to help Beks create a binary classifier capable of predicting whether applicants will be successful if funded by Alphabet Soup.
- Our tasks were:
  - Deliverable 1: Preprocessing Data for a Neural Network Model
  - Deliverable 2: Compile, Train, and Evaluate the Model
  - Deliverable 3: Optimize the Model
  - Deliverable 4: A Written Report on the Neural Network Model


## Results:
- Data Preprocessing
  - What variable(s) are considered the target(s) for your model?
    - In my model "IS_SUCCESSFUL" column was the target.
  - What variable(s) are considered to be the features of your model?
    - Features in my model were:  NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT. I included NAME columns as they significantly helped to reach the target of 75percent accuracy. 
  - What variable(s) are neither targets nor features and should be removed from the input data?
    - I removed only the EIN column from the dataset. 
- Compiling, Training, and Evaluating the Model
  - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - I attempted three times to improve the accuracy to the best outcome. 
    
    - During my first attempt, I used 141 neurons and distributed them between 4 hidden layers with two different activation functions(relu,relu,sigmoid,sigmoid). 
    - <img width="929" alt="Attempt1" src="https://user-images.githubusercontent.com/89552059/198910131-95a98684-4947-4785-9884-9d804f2711ae.png">
    
    - For my second attempt, I used 151 neurons distributed in 4 hidden layers with two activation functions used twice(relu,sigmoid,relu,sigmoid).
    - <img width="923" alt="Attempt2" src="https://user-images.githubusercontent.com/89552059/198910202-0fe7fdd1-d93d-4391-bef5-e335ca803fe1.png">
    
    - For my final attempt, I used 141 neurons, four hidden layers, and two activation functions(relu,sigmoid,sigmoid,sigmoid).
    - <img width="919" alt="Attempt3" src="https://user-images.githubusercontent.com/89552059/198910222-a3613fde-b392-4530-84ac-c490eac7fdd3.png">
  - Were you able to achieve the target model performance?
  - <img width="759" alt="Attempt1_result" src="https://user-images.githubusercontent.com/89552059/198910242-4e3679cb-3eef-4c15-b945-deb8b4941f06.png">
  - <img width="753" alt="Attempt2_result" src="https://user-images.githubusercontent.com/89552059/198910244-b42c8694-e503-4a2e-82a8-5230b1176426.png">
  - <img width="757" alt="Attempt3_result" src="https://user-images.githubusercontent.com/89552059/198910247-aa70534c-f79f-4abe-a857-eaec1a579077.png">
  - I achieved the target model performance on all attempts. Attempt 1 resulted in about 77 percent accuracy, and attempts 2 and 3 both had about 78 percent accuracy. 
  - What steps did you take to try and increase model performance?
    - Firstly, I tried binning the ASK_AMT column as it had 8747 unique values, but I had a type error that said I could not include string and integer in the same columns. I could not develop a perfect defying name to explain the binning data. Then I tried including the NAME column in the module, which proved successful. 

## Summary: 
- Including the NAME columns and having four hidden layers helped to achieve a target model performance. 
- I would recommend using Random Forest Classifier as it achieved a target only in a few seconds, while other neural models took minutes.
- <img width="737" alt="suggestion" src="https://user-images.githubusercontent.com/89552059/198910889-a736d7b5-70f3-4739-a3af-637cfd62e984.png">
