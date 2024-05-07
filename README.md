# Loan Prediction Application

This is a Flask-based Loan Prediction Application that uses a machine learning model to predict loan eligibility based on user provided data.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.7 or higher installed.
- Pip for installing Python packages.

## Installation

Clone the repository to your local machine:

git clone https://github.com/yourusername/loan-prediction-app.git
cd loan-prediction-app
Install the necessary Python packages:

pip install -r requirements.txt
Running the Application
To start the application locally, run the following command in the root directory of the project:

python app.py
This will start the Flask server on localhost with the default port 5000.

Accessing the Application
Once the server is running, you can access the application by navigating to:

http://localhost:5000/
Using the API
The application provides an API endpoint for making predictions. Below are the details on how to use this endpoint:

/predict
Method: POST
Description: This endpoint accepts user data in JSON format and returns a loan eligibility prediction.
Data Format: JSON
Data Example:
{
  "First_Name": "John",
  "Last_Name": "Doe",
  "Gender": 1,
  "Married": 1,
  "Dependents": 1,
  "Education": 1,
  "Self_Employed": 1,
  "ApplicantIncome": 5000,
  "CoapplicantIncome": 2000,
  "LoanAmount": 200,
  "Loan_Amount_Term": 360,
  "Credit_History": 1,
  "Property_Area": 2
}

Usage Example:Use curl or any HTTP client to send a POST request:
curl -X POST http://localhost:5000/predict -H "Content-Type: application/json" -d '