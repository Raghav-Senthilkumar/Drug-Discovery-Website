# COX-2 Inhibition Drug Discovery Website

## Overview
This project is a drug discovery web application designed to predict the effectiveness of new drugs for COX-2 inhibition. It consists of a **React frontend** and a **Flask backend**. The backend trains a machine-learning model using data from the **ChEMBL website**, leveraging **PaDEL descriptors** to calculate molecular properties and make predictions.


## **Features**

1. **Drug Effectiveness Prediction**:
   - Predicts the effectiveness of new drugs for **COX-2 inhibition**.
   - Utilizes **SMILES representations** of molecules to calculate descriptors and predict drug effectiveness.
   - Relies on a **Histogram Gradient Boosting** machine learning model trained on data from **ChEMBL**.

2. **Descriptor Calculation**:
   - Extracts molecular descriptors using **PaDEL-Descriptor**.
   - Computes properties such as molecular weight, logP, and more, which are used as input features for the machine learning model.
   - The system uses **PaDEL** software, which requires **Java** to calculate descriptors.

3. **Molecule Visualization**:
   - Generates molecular images using **RDKit**.
   - Provides a graphical representation of molecules based on their SMILES strings.

4. **Frontend (React)**:
   - Features a user-friendly interface built with **React**.
   - Allows users to upload CSV files containing **SMILES** strings.
   - Displays the prediction results, including **drug effectiveness** and **confidence score**.

5. **Backend (Flask API)**:
   - The backend is powered by **Flask**, exposing an API for calculating descriptors, making predictions, and visualizing molecules.
   - Supports file uploads via **POST** requests and returns the prediction results in **JSON format**.

6. **Scientific Research Integration**:
   - Fetches relevant articles from **PubMed** using the **Entrez API**.
   - Provides links to articles related to the effects of COX-2 inhibitors on drug discovery and health.

7. **Deployment**:
   - The website can be deployed on cloud platforms like **Heroku**, **AWS**, or **DigitalOcean**.
   - The frontend can be deployed on platforms like **Vercel**, **Netlify**, or **AWS S3**.

## **Requirements**

To run this application, you need the following Python libraries and tools installed:

### **Python Libraries**:

- `paedldescriptors` – For calculating molecular descriptors using PaDEL software.
- `pandas` – For data manipulation and handling CSV files containing molecular data.
- `scikit-learn` – For machine learning, particularly for training and evaluating the **Histogram Gradient Boosting** model for drug effectiveness prediction.
- `flask` – For the backend API to serve predictions and handle file uploads.
- `biopython` – For interacting with biological data, especially to fetch PubMed articles using the Entrez API.
- `transformers` – For using **Hugging Face** models like GPT-2 to generate reports based on predictions.
- `torch` – For running **Hugging Face** models and performing deep learning tasks.

### **Frontend Tools**:

- `react` – For building the interactive user interface for the web application.
- `node.js` – For running the React development environment and managing dependencies.

### **Installing Dependencies**:

You can install the required Python libraries using `pip`:

```bash
pip install paedldescriptors pandas scikit-learn flask biopython transformers torch
