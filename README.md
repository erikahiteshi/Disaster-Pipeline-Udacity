# Disaster Response Pipeline Project
In this project, I'll apply data engineering and a Machine Learning Model to analyze disaster data from Figure Eight to classify disaster messages.

This directory contains a data set which are real messages that were sent during disaster events. I will be creating a Machine Learning Pipeline which uses NLP to classify a message of one of 36 outputs. These outputs will indicate whether that person may or may not need aid.

This project will include a web app where a worker could input a new message and receive classification results in the output categories. The web app will also display visualizations of the data.


### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

# Key Files
- data/process_data : The ETL pipeline which processes the data in a format suitable to run our Machine Learning model on
- models/train_classifier.py : The Machine Learning pipeline which trains the model based on data given to us by Figure Eight. Using this data, the model is now ready to predict future messages.
- run.py : This file starts the Python server for the web app and prepare visualizations.
- app/templates/.html : These are the HTML template files for the app