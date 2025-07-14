

# 🏢 The Innovation Hub - Coworking Space Web App

This is a full-stack web application developed as part of a student group project for managing a coworking space. It enables users to register, log in, view available seating areas, book seats, and monitor real-time crowd levels via sensor simulation.

## 🚀 Features

* 🧑‍💼 Multi-role registration (Student, Professor, Guest)
* 📧 Email verification and 2FA code for login
* 📬 Password reset functionality
* 📊 Live crowd status based on sensor simulation
* 🪑 Seat availability and booking with time-slot control
* 📄 View and manage user bookings
* 💬 Contact form for inquiries

## 📽️ Website Preview

▶️ [Click here to watch the CWS demo video](cws-rec_S5WP6dHV.mp4)

## 🛠 Tech Stack

**Frontend:**

* React (Material UI + Material Kit 2)
* React Router DOM
* Fetch API
* Font Awesome Icons

**Backend:**

* Flask
* Flask-CORS, Flask-Bcrypt, Flask-Mail
* Flask-SQLAlchemy
* SQLite (for development)
* dotenv for environment config
* Pandas for CSV parsing (sensor simulation)

## 📁 Folder Structure

```
coworking-space-app/
├── backend/               # Flask backend
│   ├── app.py             # Main Flask app
│   ├── .env               # Environment variables
│   └── ...
├── frontend/              # React frontend
│   ├── src/
│   ├── .env
│   └── ...
└── README.md
```

## ⚙️ Setup Instructions

### Backend

1. Navigate to the backend folder:

```bash
cd backend
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Add a `.env` file with:

```
SECRET_KEY=your-secret-key
SQLALCHEMY_DATABASE_URI=sqlite:///app.db
MAIL_SERVER=smtp.gmail.com
MAIL_PORT=587
MAIL_USE_TLS=True
MAIL_USERNAME=your-email
MAIL_PASSWORD=your-password
MAIL_DEFAULT_SENDER=your-email
FRONTEND_BASE_URL=http://localhost:3000
```

5. Run the server:

```bash
python app.py
```

### Frontend

1. Navigate to the frontend folder:

```bash
cd frontend
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file:

```
REACT_APP_API_BASE_URL=http://localhost:5000
```

4. Start the frontend:

```bash
npm start
```

## 🧪 Testing CORS

A test route `/api/test-cors` is available to check if cross-origin requests are working. Ensure your `fetch` requests include `credentials: "include"` and your Flask backend has the correct `CORS` config matching your frontend origin.

## 🧠 Known Issues

* CORS errors can happen due to GitHub Codespaces proxying and authentication settings.
* Email sending may delay or fail if SMTP is not configured properly.
* Codespace deployment may not always reflect changes unless hard-reloaded.
* Deployment was impacted due to teammate delays and limited final hours for integration and error fixes.

## 🔗 Project Links

* GitHub Repo: [https://github.com/khadija-mahmoud-17/The\_Innovation\_Hub](https://github.com/khadija-mahmoud-17/The_Innovation_Hub)

## 📬 Contact

For any questions or feedback, please use the contact form in the application or open an issue on the GitHub repository.

---

