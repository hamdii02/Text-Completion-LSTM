Text Generation App

This Flask application allows users to generate text completions using two different models: an N-gram model and an LSTM (Long Short-Term Memory) model. Users can enter raw text and select the model they want to use for generating predictions.

Prerequisites

    Python 
    Flask
    Keras
    NLTK
    TensorFlow


Create Environment: Use the provided environment.yaml file to create a virtual environment:


conda env create -f environment.yaml

Activate the Environment:

conda activate <environment-name>

Prepare the Models:

    Ensure you have the LSTM model saved as lstm_model.json and the tokenizer as tokenizer.json.
    Place the N-gram model in a file named ngram_counts.pkl.

Project Structure: Your project directory should look like this:

graphql

    /project-directory
    ├── app.py                   # Main Flask application with model selection
    ├── Run_Server_LSTM.py       # Flask application to run LSTM model
    ├── Run_Server_Ngram.py      # Flask application to run N-gram model
    ├── Run_Server_with_Choice.py # Flask application to run both models
    ├── lstm_model.json          # LSTM model JSON
    ├── tokenizer.json            # Tokenizer for LSTM model
    ├── ngram_counts.pkl         # Pickle file for N-gram model
    ├── templates/               # Folder containing HTML templates
    │   ├── home_page.html       # Home page HTML
    │   └── response_page.html   # Response page HTML
    └── static/                  # Folder for static files (images, CSS)
        └── Kraken-Logo.png      # Logo image

Running the Models
Run LSTM Model

To run the LSTM model separately, execute:

python Run_Server_LSTM.py

Run N-gram Model

To run the N-gram model separately, execute:

python Run_Server_Ngram.py

Run Both Models

To run both models in the same Flask app, execute:

python Run_Server_with_Choice.py

Usage

    Input Text: Enter the raw text in the provided textarea.
    Select Model: Choose either the LSTM or N-gram model from the dropdown menu.
    Submit: Click the "Check" button to generate text completions.
    View Results: The response page will display the original text and the generated text. Click "Go Back" to return to the input page.
