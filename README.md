# 🔐 Secure File Sharing System (Flask)

This project implements a secure file-sharing system between **Ops Users** and **Client Users** using Flask, SQLAlchemy, JWT, and encrypted download URLs.

---

## ✅ Features

### 👤 Ops User
- Login (JWT Token)
- Upload files (`.pptx`, `.docx`, `.xlsx` only)

### 👥 Client User
- Sign Up (Email Verification with Encrypted URL)
- Email Verification
- Login (JWT Token)
- List all uploaded files
- Generate secure download link
- Download file using encrypted, user-bound URL

---

## 🔐 Security
- JWT-based session management
- Encrypted download links using `cryptography.Fernet`
- Role-based access control
- File type validation
- Email confirmation before login

---

## 🏗️ Setup Instructions

### Prerequisites
- Python 3.7+
- A working email SMTP server for email verification

### Installation

```bash
git clone https://github.com/your-username/flask-secure-file-sharing.git
cd flask-secure-file-sharing
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

### Environment Variables

Set the following environment variables (e.g., via `.env` file or system config):

```bash
SECRET_KEY=your-secret-key
MAIL_USERNAME=your-email@example.com
MAIL_PASSWORD=your-email-password
MAIL_DEFAULT_SENDER=your-email@example.com
```

### Database Setup

```bash
flask shell
>>> from app import db
>>> db.create_all()
```

### Run the App

```bash
python app.py
```

---

## 🧪 Testing

- Ensure Ops cannot access download URLs
- Ensure only allowed file types can be uploaded
- Check expired/invalid token handling

---

## 🧠 Future Improvements

- One-time download tokens
- Token expiration with background cleanup
- File previews (non-download access)
- Cloud file storage (AWS S3)

---

## 🧑‍💻 Author

[Jey Sankar Sai Pinjala](https://github.com/Jey-Sankar-Sai-Pinjala)

---
