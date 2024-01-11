# CheerBot
The Cheerbot project is a chatbot designed to assist users in conversation while being sensitive to their emotions. The chatbot operates by processing user input, classifying it into one of five emotion categories, generating a tailored response, and delivering it to the user.

The chatbot starts with a greeting message, "Hey user! How may I assist you?". The user provides input speech signals, which are then converted into text by the speech recognizer module. The autocorrector module checks for any spelling or grammatical errors in the input text.

Upon receiving a stop keyword such as 'stop', 'quit', 'exit', 'end', 'bye', 'goodbye', or 'close', the chatbot exits gracefully by saying, "Thank you for using the chatbot. Exiting program...".

The corrected input text is then passed to the Emotion Classification Module, which utilizes a fine-tuned Roberta Classifier to identify the emotion of the input text. The classifier categorizes the input text into one of five emotion categories: Surprise, Happy, Sad, Anger, and Fear.

The Response Generation Module takes the emotion category and input text as inputs and passes them to a generator (GPT-3.5 Davinci 002), which produces a tailored response based on the input text and the emotion category. The generator produces a response that is appropriate to the identified emotion of the input text.

Finally, the Output Module delivers the tailored response to the user. The process continues until the chatbot receives one of the stop keywords.

UPDATE: GPT3.5 API has been replaced with PALM2 API for response generation as the former API has been closed-sourced.
