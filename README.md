# Skin Cancer Classification (CNN + FastAPI + React)

This project demonstrates an end-to-end pipeline for **skin cancer classification** using a **Convolutional Neural Network (CNN)**.  
The workflow includes:

- **Model Training**: A CNN model was trained on a skin cancer image dataset.  
- **Model Export**: The trained model + architecture was saved in `.keras` format.  
- **Backend (FastAPI)**: A FastAPI server loads the model and exposes REST APIs for predictions.  
- **Frontend (React)**: A React web app allows users to upload an image, sends it to the FastAPI backend, and displays the predicted cancer class + confidence score.

---

## Features
- Upload an image (skin lesion photo).  
- Model performs inference using CNN.  
- Predicts **9 possible skin conditions**:  
  1. Actinic keratosis  
  2. Basal cell carcinoma  
  3. Dermatofibroma  
  4. Melanoma  
  5. Nevus  
  6. Pigmented benign keratosis  
  7. Seborrheic keratosis  
  8. Squamous cell carcinoma  
  9. Vascular lesion  

---

##  Tech Stack
- **Python 3.10+**
- **TensorFlow / Keras 3.x** → Model training & saving  
- **FastAPI** → Backend API for serving the model  
- **Uvicorn** → ASGI server for FastAPI  
- **NumPy, Pillow** → Image preprocessing  
- **React.js** → Frontend UI  

---

## Project Structure
skin_cancer/
│── models/ # Saved .keras model
│── api/ # FastAPI backend
│ ├── main.py # FastAPI app
│── frontend/ # React app
│ ├── src/ # React components
│ └── package.json
│── Train/ # Training dataset
│── Test/ # Testing dataset
│── classification.ipynb # Jupyter notebook (model training)
│── README.md



## Prerequisites

Python 3.10+

Node.js 18+ and npm

## Run Fast API Server

uvicorn api.main:app --reload --host 0.0.0.0 --port 8000
Swagger Docs → http://localhost:8000/docs


## Test API Endpoint

POST -F "file=@Test/sample.jpg" http://localhost:8000/predict

## FrontEnd
localhost:3000
