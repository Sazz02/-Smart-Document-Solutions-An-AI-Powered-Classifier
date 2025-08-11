📁 Smart Document Solutions: An AI-Powered Classifier

A Machine Learning project to automatically categorize documents, built for the Smart Data Solutions AI Intern Selection.

Project Overview

In today's data-driven world, efficiently organizing and routing vast amounts of digital documents is a critical challenge. This project tackles that problem head-on by creating a machine learning model that can instantly classify a document based on its text content.

Think of it as teaching a computer to be a skilled archivist. Instead of manually sorting through financial reports, legal contracts, and user manuals, this AI-powered solution automates the process, saving time and preventing human error. This repository documents the complete journey: from raw data to a live, interactive web application.

💾 The Dataset: A Closer Look

The foundation of this project is a balanced document image dataset provided for the internship task. It's a well-structured collection of 2,500 documents, organized into five distinct classes, with 500 examples for each class.

The dataset is provided in a hierarchical structure:

    /data: The root directory.

        /images: Contains the raw document images in TIF format.

        /ocr: Contains the text data extracted from each image.

For this project, we primarily utilized the OCR text data from the /ocr directory to build our classification model, as it contains the most discriminative information for document categorization.

🚀 The Project Pipeline: From Raw Data to a Live App

Our solution follows a structured, end-to-end machine learning workflow.

1. Data Ingestion & Preprocessing

The project begins by unzipping the raw dataset. We then load the OCR text files, clean them by removing noise like punctuation and stop words, and organize them into a structured format for training.

2. Feature Engineering: The Secret Sauce 🧂

The core challenge of text classification is converting human language into a numerical format that a computer can understand. We used TF-IDF (Term Frequency-Inverse Document Frequency), a powerful technique that assigns a numerical value to words based on their importance within a document and across the entire dataset. This created a rich set of features for our models to learn from.

3. The Algorithm Bake-Off 📊

To ensure we built the best possible model, we didn't just pick one algorithm—we tested four of the most effective classifiers for this task. We trained each model on the same dataset and compared their performance based on accuracy.
Model	Accuracy
Logistic Regression	0.9576
Random Forest	0.9480
Support Vector Machine	0.9552
Naive Bayes	0.9400

Model Analysis:
As the results clearly show, Logistic Regression emerged as the top performer with an accuracy of 95.76%. While other models like SVC and Random Forest performed admirably, Logistic Regression offered the best balance of high accuracy and computational efficiency. This makes it a perfect choice for a real-world, production-ready application.

🌐 The Final Deliverable: A Live Web App

To showcase the winning model, we built a simple and interactive web application using Gradio. This app allows anyone to paste text from a document and receive an instant classification.

You can test the live application here:
🔗 https://huggingface.co/spaces/Sazzz02/Smart-Doc-Solutions

🛠️ How to Run This Project Locally

To replicate this project on your machine, follow these steps:

    Clone the Repository
    Bash

git clone [Your-GitHub-Repo-URL]
cd [Your-Repo-Name]

Set up the Python Environment
Install the required packages using the requirements.txt file.
Bash

pip install -r requirements.txt

Run the Jupyter Notebook
Open and run Doc_Classify_Solutions_.ipynb to see the entire analysis, model training, and evaluation. This will generate the best_model.joblib and tfidf_vectorizer.joblib files.

Launch the Web Application
Run the app.py file to start the Gradio app locally.
Bash

    python app.py

🚀 Conclusion & Future Work

This project demonstrates a robust and complete solution for document classification. By systematically comparing multiple algorithms, we were able to select the most effective model, and by deploying it as a web app, we made the technology accessible to everyone.

If given more time, future improvements could include:

    Integrating image features with text features for an even more robust hybrid model.

    Hyperparameter tuning of the best-performing model to squeeze out every last bit of performance.

This project was a great learning experience and a testament to the power of a data-driven approach to problem-solving.
