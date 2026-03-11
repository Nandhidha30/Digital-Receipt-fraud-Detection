Fake Receipt Detection Web App
A Machine Learning + FastAPI + Frontend Project

Overview
Fake receipts are often used for fraud, reimbursements, and manipulation. This project provides a fast, lightweight web application that detects Real vs. Fake receipts using a CNN-based machine learning model served through FastAPI.

The frontend offers a responsive drag-and-drop upload UI, real-time image preview, and instant prediction results.

Features
- Upload or drag-and-drop receipt images
- Real-time image preview before prediction
- Instant classification through FastAPI backend
- PyTorch CNN model trained to detect fake vs real receipts
- Confidence score display
- Fully responsive UI built with HTML, CSS & JavaScript
- Smooth frontend ↔ backend communication via Fetch API

Machine Learning Model
Framework: PyTorch  
Model Type: Custom CNN / ResNet18 fine-tuned  
Input: Receipt images  

Output:
REAL  
FAKE  
confidence score (0 to 1)

Installation & Setup

Clone the Repository
git clone https://github.com/nandhidha30/Fake-Receipt-Detection.git
cd Fake-Receipt-Detection

Create Virtual Environment
python -m venv venv
venv\Scripts\activate

Install Dependencies
pip install -r requirements.txt

Run the Backend
uvicorn app:app --reload

Backend runs at:
http://127.0.0.1:8000

How It Works
1. User uploads a receipt image  
2. Frontend sends the image to FastAPI  
3. Backend loads the CNN model and classifies the image  
4. Frontend displays result and confidence score

API Endpoint
POST /predict

Returns:

{
  "prediction": "REAL",
  "confidence": 0.9444
}