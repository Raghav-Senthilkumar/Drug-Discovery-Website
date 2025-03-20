COX-2 Inhibition Drug Discovery Website

Overview

This project is a drug discovery web application designed to predict the effectiveness of new drugs for COX-2 inhibition. It consists of a React frontend and a Flask backend. The backend trains a machine-learning model using data from the ChEMBL website, leveraging PaDEL descriptors to calculate molecular properties and make predictions.

Project Structure

Getting Started

Prerequisites

Ensure you have the following installed:

Node.js (for the React frontend)

Python 3 (for the Flask backend)

pip (Python package manager)

Java (for PaDEL descriptor calculations)

Backend (Flask) Setup

1. Navigate to the backend folder

2. Create a virtual environment (optional)

3. Install dependencies

4. Run the Flask server

By default, the Flask API should be available at http://127.0.0.1:5000.

Frontend (React) Setup

1. Navigate to the frontend folder

2. Install dependencies

3. Start the React development server

By default, the React app should be available at http://localhost:3000.

API Endpoints

Method

Endpoint

Description

POST

/upload

Accepts a CSV file, calculates descriptors, and predicts drug effectiveness.

Example Request

To test the API, send a file using Postman or cURL:

Response Example:

Machine Learning Pipeline

Upload CSV File: The user uploads a CSV containing SMILES representations of molecules.

Descriptor Calculation: The system uses PaDEL-Descriptor to extract molecular properties.

Feature Selection: The model selects relevant descriptors from descriptor_list.csv.

Prediction: The trained Histogram Gradient Boosting model predicts drug effectiveness.

Molecule Visualization: The system generates molecular images using RDKit.

Common Issues & Troubleshooting

1. PaDEL Descriptor Calculation Fails?

Ensure Java is installed and available in the system path.

Try running the descriptor calculation manually:

2. CORS Errors in React?

Install and enable Flask-CORS in app.py:

Then add:

Deployment

Backend Deployment (Flask API)

Deploy on Heroku, AWS, or DigitalOcean.

Use Gunicorn for production:

Frontend Deployment (React App)

Deploy on Vercel, Netlify, or AWS S3.

Example Netlify deployment:

Contributing

Feel free to submit issues and pull requests:

Fork the repo

Create a new branch (git checkout -b feature-name)

Commit your changes (git commit -m "Added new feature")

Push to the branch (git push origin feature-name)

Open a Pull Request

License

This project is licensed under the MIT License.

