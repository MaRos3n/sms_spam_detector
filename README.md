# SMS Text Classification Project

Instructions taken from UNC AI Bootcampspot 

## Background

This project involves refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, a Gradio app will be created to host the application, enabling users to test text messages. The application will provide feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.

## Challenge Instructions

### Starter Files

The starter files consist of the following:
- `gradio_sms_text_classification.ipynb`
- `sms_text_classification_solution.ipynb`
- `SMSSpamCollection.csv`

### Create the SMS Classification Function

Using the code in the `sms_text_classification_solution.ipynb` file, create the `sms_classification` function in the `gradio_sms_text_classification.ipynb` by performing the following steps:

1. Set the `features` variable to the text message column of the DataFrame.
2. Set the `target` variable to the "label" column of the DataFrame.
3. Split data into training and testing sets, setting `test_size` to 33%.
4. Build a pipeline to transform the test set to compare to the training set.
5. Fit the model to the transformed training data and return the model.
6. Load the `SMSSpamCollection.csv` into a DataFrame and call the `sms_classification` function with the DataFrame, setting the result to the `text_clf` variable.

### Create the SMS Prediction Function

Use the `sms_prediction` function to predict the classification of a new text by performing the following steps:

1. Create a variable that will hold the prediction of a new text.
2. Use a conditional statement to determine if the text message is "ham" or “spam”.
3. 
    - If the message is “ham”, the function should return the following message: "f'The text message: "{text}", is not spam.'"
    - If the message is spam, the function should return the following message: f'The text message: "{text}", is spam.'


### Create the Gradio Interface Application

Create a Gradio Interface application that includes:
1. A textbox for input.
2. A textbox for output.
3. Labels that describe what each textbox contains.

Launch the application and provide the URL to share the application.

#### Test Messages

Use the following text messages to test your application:
1. You are a lucky winner of $5000!
2. You won 2 free tickets to the Super Bowl.
3. You won 2 free tickets to the Super Bowl. Text us to claim your prize.
4. Thanks for registering. Text 4343 to receive free updates on medicare.

## References

- "ChatGPT-4o." OpenAI, OpenAI, 2024, chat.openai.com.
- Norman, Ryan. Instructor at UNC AI Bootcamp. UNC AI Bootcamp, 2024.
