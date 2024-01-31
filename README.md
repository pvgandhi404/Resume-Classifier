# Resume-Classifier
The repository contains a Machine Learning Resume Classifier, leveraging fine-tuned Hugging Face models for categorizing resumes into roles like data science, software engineering, and project management. It offers options for hyperparameter tuning, training, and TensorFlow-based evaluation.

The resume classifier will catagorize a resume into 3 different job catagories:
0: Software Engineer
1: Data Scientist
2: Project Manager

To run the machine learning model, simply scroll down to the "Model Testing" section and hit run on both code blocks. Should an error be caused, please instead select "run all".
To insert custom inputs for the ML mode, simply change the variable "text" with the desired input. The code will automatically process the data and print the corresponding job title.

Explanation:
- The project was implemented using the Transformers library from HuggingFace and TensorFlow.
- I was unable to find an appropriate dataset for project manager jobs. To ensure consistancy and prvent bias in the results, I decided to forgo using the datasets for software engineer and data scientist.
- Instead, I simply asked chatGPT to give me a list of common job descriptions for each role. I then used that list to fine-tune the model.
- Since the dataset is quite small, there is a likely chance of reduced accuracy due to both underfitting and overfitting data.

Strategies:
- To build the resume classifier, I used the "finbert" text classification model from Hugginface, mainly due to its popularity and ability to classify between 3 different labels. - - This allowed me to easily translate the model into classifying 3 different jobs.
- I used the natural language took kit (ntlk) to remove all stopwords from all test and validation data. The same is done for all data before being processed by the model, thus increasing accuracy.
