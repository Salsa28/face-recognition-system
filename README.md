# Face-Recognition-System

<img src="assets/demo-app.png" alt="Database Schema" width="800">

## 📌 Overview

face recognition system for authentication uses the FaceNet model based on InceptionResNetV1, which relies on the Convolutional Neural Network (CNN) algorithm to generate face embedding. The feature matching process is carried out with cosine similarity, so that the system can recognize faces based on the level of similarity of the resulting feature vectors.

## 🛠 Installation

### 1. Clone Repository

```bash
git clone https://github.com/your-repo/face-recognition-system.git
cd face-recognition-system
```

### 2. Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate      #for windows
source venv/bin/activate   #for Linux/macOS
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Database

🔗 Unduh PostgreSQL: https://www.postgresql.org/download/

Make sure PostgreSQL is installed and running and adjust the database configuration in `.env`. Next, test the database connection in `koneksi.py` to make sure it is connected to PostgreSQL

### 5. Create Database

- Open a terminal and connect to PostgreSQL

```sql
psql -U your_username_postgreSQL
```

- Create database

```sql
CREATE DATABASE facerecognitiondb;
```

- move to the new database that has been created

```sql
\c facerecognitiondb
```

- Create tabel users

```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(255) UNIQUE NOT NULL,
    password_hash TEXT NOT NULL,
    face_embedding BYTEA NOT NULL
);
```

### 6. Run the API

run the API using FastAPI with terminal

```bash
uvicorn backend.main:app --reload
```

### 7. Run the Streamlit

<<<<<<< HEAD
run streamlit in terminal 2
=======
<<<<<<< HEAD
jalankan dengan:
=======
run streamlit in terminal 2
>>>>>>> 75ecc64 (initial commit)
>>>>>>> feature-auth

```bash
cd frontend
streamlit run app.py
```

# API Documentation

Swagger UI = http://localhost:8000/docs

## The list of endpoints can be seen in the including-API-endpoints folder.
