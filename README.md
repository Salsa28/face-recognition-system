# Face-Recognition-System

<img src="assets/demo-app.png" alt="Database Schema" width="600">

## 📌 Overview

Face Recognition ini adalah Sistem pengenalan wajah untuk autentikasi dengan deteksi wajah real-time. Sistem ini menggunakan model deep learning untuk mendeteksi dan mencocokkan wajah berdasarkan fitur unik.

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
source venv/bin/activate   #for Linux/macos
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Database

Pastikan PostgreSQL sudah di install dan berjalan dan sesuaikan konfigurasi database di `.env`. Selanjutnya tes koneksi database di `koneksi.py` untuk memastikan apakah sudah terhubung ke PostgreSQL.

### 5. Membuat Database

- Buka terminal dan hubungkan ke PostgreSQL

```sql
psql -U your_username_postgreSQL
```

- Buat database:

```sql
CREATE DATABASE facerecognitiondb;
```

- Beralih ke database baru

```sql
\c facerecognitiondb
```

- Buat tabel users

```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(255) UNIQUE NOT NULL,
    password_hash TEXT NOT NULL,
    face_embedding BYTEA NOT NULL
);
```

### 6. Run the API

Jalankan API menggunakan FastAPI dengan perintah berikut:

```bash
uvicorn backend.main:app --reload
```

### 7. Run the Streamlit

Jika Anda memiliki antarmuka berbasis Streamlit, jalankan dengan:

```bash
cd frontend
streamlit run app.py
```

# API Documentation

Swagger UI = http://localhost:8000/docs

## Daftar endpoint bisa dilihat di folder including-API-endpoints
