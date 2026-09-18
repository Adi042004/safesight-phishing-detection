Phishing Website Detection System

A machine learning-based Phishing Website Detection System built to classify website URLs as phishing or legitimate. The project combines Natural Language Processing, a transformer-based model, a FastAPI backend, and a web frontend to provide an end-to-end phishing detection workflow.

🚨 Project Overview

Phishing websites are designed to imitate legitimate websites and trick users into providing sensitive information such as passwords, payment details, or personal data.

This project uses the URL itself as an important source of information. The system processes a website URL, sends it through the trained NLP model, and returns a classification indicating whether the URL is likely to be phishing or legitimate.

The project was developed as a practical machine learning application rather than only as a model-training exercise. It includes model training, an API layer, database integration, and a user-facing web application.

✨ Features

Phishing vs. legitimate URL classification

Transformer-based NLP model using RoBERTa

Hugging Face tokenizer and training pipeline

FastAPI backend for model inference

Web-based interface for submitting URLs

QR-code functionality integrated into the application

Supabase database integration

Frontend and backend deployment support

Included phishing dataset for experimentation and reproduction

🧠 Machine Learning Approach

The core of the project is a RoBERTa-based text classification model.

Workflow

Website URL
    ↓
URL preprocessing
    ↓
Hugging Face tokenizer
    ↓
RoBERTa model
    ↓
Binary classification
    ↓
Phishing / Legitimate

The URL is treated as text and tokenized before being passed to the transformer model.

The training workflow uses the Hugging Face ecosystem, including the tokenizer and Trainer-based training pipeline.

📊 Dataset

The project dataset is included in this repository.

The dataset contains website/URL information along with a target label used for supervised classification.

At a high level:

URL / Website Features
        +
Classification Label
        ↓
Model Training
        ↓
Phishing / Legitimate Prediction

Dataset usage

The dataset can be used for:

Training the phishing detection model

Testing preprocessing and tokenization

Reproducing the project

Experimenting with different classification approaches

Further model improvement

Note: The repository contains the project dataset as provided for this case study. Check the dataset's source and license before redistributing it outside this repository.

🛠️ Technologies Used

Machine Learning / NLP

Python

PyTorch

Hugging Face Transformers

RoBERTa

Hugging Face Tokenizers

Scikit-learn

Backend

FastAPI

Uvicorn

Python

Database / Backend Services

Supabase

Frontend / Deployment

Web frontend

Netlify

Render

Other

QR-code generation / storage

GitHub

📁 Suggested Project Structure

Phishing-Website-Detection/
│
├── dataset/
│   └── <phishing-dataset-file>
│
├── model/
│   └── <trained-model-files>
│
├── backend/
│   ├── <FastAPI files>
│   └── ...
│
├── frontend/
│   ├── <frontend files>
│   └── ...
│
├── requirements.txt
├── README.md
└── ...

The exact file/folder names may differ depending on the version of the project stored in the repository.

⚙️ Installation

1. Clone the repository

git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_REPOSITORY_FOLDER>

2. Create a Python environment

python -m venv venv

Activate it on Windows:

venv\Scripts\activate

Or on macOS/Linux:

source venv/bin/activate

3. Install dependencies

pip install -r requirements.txt

🧪 Training the Model

The training process follows a standard Hugging Face sequence-classification workflow:

Dataset
   ↓
Data preparation
   ↓
Train / validation split
   ↓
RoBERTa tokenizer
   ↓
Tokenized dataset
   ↓
RoBERTa sequence classifier
   ↓
Hugging Face Trainer
   ↓
Trained model

The trained model can then be connected to the FastAPI application for real-time inference.

🚀 Running the Backend

The backend uses FastAPI.

A typical development command is:

uvicorn <backend_module>:app --reload

Once running, the API can be accessed through the local FastAPI server.

FastAPI also provides interactive API documentation, normally available at:

http://127.0.0.1:8000/docs

Use the actual module name and configuration present in the repository when starting the project.

🌐 Deployment

The project was designed with a separate frontend/backend architecture.

Backend

The FastAPI backend can be deployed through:

Render

Frontend

The web frontend can be deployed through:

Netlify

Database

Supabase is used for application data and QR-code-related storage.

This architecture allows the ML inference API and user interface to be deployed independently.

🔗 How the Application Works

A typical user flow is:

User enters a website URL
          ↓
Frontend sends URL to API
          ↓
FastAPI receives request
          ↓
URL is tokenized
          ↓
RoBERTa performs classification
          ↓
Prediction returned
          ↓
Frontend displays result

The application can then use the database layer for storing supported application data and QR-code information.

📌 Key Project Insights

1. URLs contain useful signals

Phishing URLs often contain unusual structures, misleading terms, excessive subdomains, suspicious paths, or other textual patterns. Treating URLs as text makes transformer-based NLP models applicable to the problem.

2. Transformer models can be used for cybersecurity classification

RoBERTa is primarily an NLP architecture, but URL strings can also be represented as token sequences. This makes the project an example of applying modern NLP techniques to a cybersecurity problem.

3. Model accuracy is only one part of a real application

A usable ML project also requires:

Data preparation

Model training

Inference

API integration

Frontend interaction

Database handling

Deployment

This project connects these components into one workflow.

4. False positives and false negatives matter

For a phishing detector, both error types are important.

A false negative can allow a phishing URL to be treated as legitimate, while a false positive can incorrectly flag a legitimate website.

Therefore, model evaluation should consider more than a single accuracy score.

🔍 What I Learned From This Project

This project helped me gain practical experience with:

Machine learning classification

Natural Language Processing

Transformer models

RoBERTa fine-tuning

Hugging Face Transformers

Dataset preprocessing

FastAPI API development

Backend/frontend integration

Supabase database usage

Model deployment

Building an end-to-end ML application

🔮 Future Improvements

Possible improvements for a future version include:

Add additional URL and domain-level features

Combine transformer predictions with traditional ML features

Add explainable AI for prediction reasoning

Detect newly registered or suspicious domains

Add real-time URL reputation checks

Improve handling of obfuscated URLs

Add stronger validation and security controls to the API

Add automated model evaluation and monitoring

Compare RoBERTa with models such as DistilBERT or traditional ML classifiers

🎯 Project Objective

The main objective of this project was to build an end-to-end system that demonstrates how machine learning and NLP can be applied to phishing URL detection and then integrated into a practical web application.

It combines:

Data → NLP → Model → API → Database → Frontend → Deployment

👤 Project Type

Final Year Machine Learning / Data Science Project

Built as an academic project to explore phishing detection, transformer-based NLP, and full-stack ML deployment.

📄 License

This repository is intended for educational and portfolio purposes. Please verify the licensing and redistribution permissions of any third-party dataset, pretrained model, or external resource included or referenced by the project.
