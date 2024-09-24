# MLOps-Driven Titanic Survival Prediction Pipeline

## Overview

The Titanic Survival Prediction project aims to predict passenger survival on the Titanic using machine learning. This project leverages Scikit-Learn's powerful pipeline functionality to streamline the model development process and wraps the model into a Flask application for user-friendly predictions.

## Project Structure

- **`data/`**: Contains dataset files (e.g., training and test data).
- **`notebooks/`**: Jupyter notebooks for data exploration and preprocessing.
- **`src/`**: Source code for data processing, model training, and Flask application.
  - **`pipeline.py`**: Contains Scikit-Learn pipeline configuration for preprocessing and model training.
  - **`app.py`**: Flask application code for serving the model and handling user requests.
- **`requirements.txt`**: List of dependencies needed to run the project.
- **`README.md`**: Project overview and setup instructions.

## Installation

To set up the project, clone the repository and install the required dependencies:

git clone https://github.com/yourusername/titanic-survival.git
cd titanic-survival
pip install -r requirements.txt

## Usage
#Training the Model
1. Prepare the Data: Ensure the dataset files are located in the data/ directory.
2. Run the Pipeline: Execute the pipeline script to train the model. This will handle data preprocessing and model training.

```bash
python src/pipeline.py
```
This will save the trained model and preprocessing pipeline to disk.

#Running the Flask App
1. Start the Flask Server: Run the Flask application to serve the trained model and handle prediction requests.

```bash
python src/app.py
```
2. Access the App: Open your web browser and navigate to http://127.0.0.1:5000. You can use the web interface to input passenger details and get survival predictions.

#API Endpoints
1. POST /predict: Predict survival for a given passenger. Send a JSON payload with passenger data.

Example Request:
```bash
json
{
  "Pclass": 1,
  "Sex": "female",
  "Age": 29,
  "SibSp": 0,
  "Parch": 0,
  "Fare": 71.2833,
  "Embarked": "C"
}
```
Example Response:
```bash
json
{
  "survival": 1
}
```
#Requirements
- Python 3.x
- Flask
- Scikit-Learn
- Pandas
- NumPy

You can install the required packages using:

```bash
pip install -r requirements.txt
```
#Contributing
Feel free to open issues or submit pull requests if you have suggestions or improvements.

#License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgements
Scikit-Learn for the machine learning pipeline.
Flask for the web application framework.


Feel free to modify the content as needed, especially the placeholder URLs and paths. Let me know if there’s anything else you need!
