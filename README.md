🧾 Fake Receipt Detection Web App
A Machine Learning + FastAPI + Frontend Project

📌 Overview
Fake receipts are often used for fraud, reimbursements, and manipulation. This project provides a fast, lightweight web application that detects Real vs. Fake receipts using a CNN-based machine learning model served through FastAPI.
The frontend offers a responsive drag‑and‑drop upload UI, real‑time image preview, and instant prediction results.

🚀 Features

📂 Upload or drag‑and‑drop receipt images

🖼 Real‑time image preview before prediction

⚡ Instant classification through FastAPI backend

🧠 PyTorch CNN model trained to detect fake vs. real receipts

🔍 Confidence score display for transparency

💻 Fully responsive UI built with HTML, CSS & JavaScript

🔗 Smooth frontend ↔ backend communication via Fetch API

🧠 Machine Learning Model
Framework: PyTorch

Model Type: Custom CNN / ResNet18 fine‑tuned

Input: Receipt images

Output:

REAL

FAKE

confidence score (0 to 1)


⚙️ Installation & Setup

1️⃣ Clone the Repository
git clone https://github.com/<your-username>/Fake-Receipt-Detection.git
cd Fake-Receipt-Detection

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Run the Backend
cd backend
uvicorn app:app --reload
Backend runs at:
👉 http://127.0.0.1:8000

5️⃣ Open the Frontend
Just double‑click:

frontend/index.html

🎯 How It Works
User uploads a receipt image

Frontend sends the image to FastAPI

Backend loads the CNN model and classifies the image

Frontend displays:

Result → REAL / FAKE

Confidence value

Uploaded image preview

📬 API Endpoint
POST /predict
Accepts: multipart/form-data image file

Returns JSON:

{
  "prediction": "REAL",
  "confidence": 0.9444
}

📸 UI Preview
Clean, responsive layout

Drag‑and‑drop zone

Instant image preview

Smooth animations and results display
