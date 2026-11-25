# 🌌 GoldLens — NASA Space Apps Challenge 2025

## 🪐 Introduction

**GoldLens** is a project developed for the **NASA Space Apps Challenge 2025**, under the challenge **“A World Away: Hunting for Exoplanets with AI.”**  
The project’s primary objective is to design and implement an artificial intelligence solution that supports the detection of **exoplanets** using **publicly available astronomical data**.

The solution integrates a **Python backend** with a **modern web frontend**, enabling users to evaluate and apply machine learning models through an accessible and interactive interface.  
GoldLens seeks to connect **advanced data science** with **astronomy** while promoting **open collaboration** and **scientific discovery**.


PITCH: https://youtu.be/szvgwXYw78o
---

## 🚀 Project Overview

GoldLens delivers an **end-to-end pipeline** for research in exoplanet detection.  
Users are able to:

- Ingest and preprocess astronomical datasets (e.g., telescope light curves)
- Evaluate performance using recognized statistical metrics

The system also provides a **web-based interface** where predictions can be tested, explored, and visualized in real time.

By combining **scientific rigor** with **accessibility**, GoldLens serves both as a **research tool** and an **educational platform**, designed to ensure **transparency**, **usability**, and **collaboration** — contributing to the **democratization of space research**.

---

## 📁 Repository Structure

```
├── artifacts # Trained ML artifacts
├── model.pkl # Serialized model ready for predictions
├── backend/ # Python server (training, prediction, API)
├── datasets/ # CSV datasets used for training and testing of the model
├── frontend/ # React + Vite web application
├── modelo.py # Model training and serialization
└── README.md # Documentation

Observation: We suggest the use of clean data for the analysis by the model (tests can be made with the "CANDIDATE" lines of the "clean_K2" and "clean_KOI" datasets). An improved version of the software was used applying Tansfer Learning on the TOI dataset, along with the former K2 and KOI datasets, and could deal with "dirty", unprocessed data, utilizing a robust preprocessing pipeline. However, due to problems on the integration of the model constructed with the web application, it could not be included on time for the project submiission for the NASA Space Apps Challenge 2025.

```

---

## 🧠 Technologies

### **Backend**
- **Language:** Python 3.10+
- **Libraries:**
  - `scikit-learn` — machine learning
  - `pandas`, `numpy` — data preprocessing
  - `Flask` — RESTful API
  - `joblib` — model serialization

### **Frontend**

- **Language:** JavaScript
- **Framework:** React + Vite
- **Styling:** TailwindCSS (responsive design)
- **Communication:** Fetch API
  
This stack ensures a **robust**, **scalable**, and **user-friendly** platform.

---

## ⚙️ Installation and Execution

### 🔧 Clone the repository

```bash
git clone https://github.com/gabriel-abreu542/NASA-Space-Apps-Challenge-GoldLens
cd NASA-Space-Apps-Challenge-GoldLens

```

### 🧩 Backend Setup

cd backend
python -m venv venv
source venv/bin/activate # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python modelo.py # Train and serialize the model
python app.py # Launch backend server

The backend will be available at: <b>The backend will be available at:</b>

```
https://localhost:5000
```

### 💻 Frontend Setup

```
cd frontend
npm install
npm run dev
```

The frontend interface will be available at:

```
https://localhost:5173
```

## 🔗 API Endpoints

| Endpoint      | Method    | Description                                           |
| ------------- | --------- | ----------------------------------------------------- |
| `/health`     | `GET`     | Returns service status                                |
| `/predict`    | `POST`    | Accepts CSV input and returns model predictions of multiple cases      |
| `/predict-individual` | `POST` | Accepts a JSON describing a single case and returns its prediction |

These endpoints complete the workflow of model training, validation, and inference.

# 📊 Model Evaluation

GoldLens evaluates trained models using standard metrics:

- Accuracy

- Precision

- Recall

- F1-score

- ROC-AUC

- Confusion Matrix

These metrics provide insights into model performance and help compare different algorithms for exoplanet detection.

# 👨‍🚀 Team

GoldLens is developed by Heart of Gold, a multidisciplinary team of five contributors:

- Pablo Calil

- Gabriel Abreu

- Breno Resende

- João Castelar

- Matheus Lopes

Each member brings expertise in data science, full stack development, and software engineering, working collaboratively to unite technological innovation and scientific exploration.

# 🤝 Contributing

Contributions are welcome!
To contribute:

1. Fork the repository

2. Create a new branch

3. Commit your changes with clear messages

4. Push to your fork

5. Open a Pull Request

All contributions — from bug fixes to new features — help strengthen the project and support its mission of collaborative science.

# 📜 License

GoldLens is licensed under the MIT License, allowing free use, modification, and distribution.
This ensures that the project’s resources can be reused and expanded by the community, promoting open science and innovation.

"Exploring worlds beyond — powered by data, driven by curiosity." 🌠
