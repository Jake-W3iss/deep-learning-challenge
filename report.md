

1.  **Overview**  of the analysis: Explain the purpose of this analysis. The purpose of the analysis is to figure out through the use of neural network if we could accurately predict if a charity project would use funding successfully. 
    
2.  **Results**: Using bulleted lists and images to support your answers, address the following questions:
    
    -   **Data Preprocessing** 
        -   **What variable(s) are the target(s) for your model?** - The `IS_SUCCESSFUL` variable was our target for this model, which was a column filled with binary values '0' meaning unsuccessful, and '1' meaning successful.
        -   **What variable(s) are the features for your model? What variable(s) should be removed from the input data because they are neither targets nor features?** - All other features in the data set that weren't dropped due to being non-essential. `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, ASK_AMT` while 	`NAME, STATUS, and SPEACIAL_CONSIDERATIONS` where tested with keeping in and taking out, and finally `EIN` was removed from the features completely
           ****
    -   **Compiling, Training, and Evaluating the Model**
        
        -   **How many neurons, layers, and activation functions did you select for your neural network model, and why?** I used 4 layers, and two activation types 'relu' and 'sigmoid', Sigmoid is useful when dealing with binary classification tasks which our target was.
        -   **Were you able to achieve the target model performance?** - Yes I achieved 77% accuracy which is above the 75% target
        -   **What steps did you take in your attempts to increase model performance?**
        - I increased the number of epochs used when fitting the model from 100 to 200, I also included the `NAME` variable because its possible the organization has an impact on how consistently funding will be successful.  
3.  **Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
If your name appears 20 or mor times in the list of applications and your application type is either: T3, T4, T6, T5, T19, T8, T7, or T10. Plus, your classification falls under: C1000, C2000, C1200, C3000, or C2100. The model can predict with 77% accuracy that you'll be successful as an applicant. I tried a Random Forest model and trained it with the data as well and that model gave 75.64% accuracy. Which also falls within the accepted model performance, but since it is below my current 77% I wouldn't choose the random forest over my current model. 
