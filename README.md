# Flask-React Full Stack Contact Management App

A modern full-stack web application for managing contacts, built with Flask (backend) and React (frontend).

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)

## ✨ Features

- **Create Contacts**: Add new contacts with first name, last name, and email
- **View Contacts**: Display all contacts in a user-friendly list interface
- **Update Contacts**: Edit existing contact information
- **Delete Contacts**: Remove contacts from the database
- **Responsive UI**: Clean and intuitive React-based frontend
- **Input Validation**: Server-side validation for data integrity

## 🛠️ Tech Stack

### Backend
- **Flask**: Lightweight Python web framework
- **Flask-SQLAlchemy**: ORM for database operations
- **Flask-CORS**: Cross-Origin Resource Sharing support
- **SQLite**: Lightweight database (default)

### Frontend
- **React 18**: JavaScript library for building user interfaces
- **Vite**: Fast build tool and development server
- **CSS**: Custom styling

## 📁 Project Structure

```
Flask-React-Full-Stack-App/
│
├── backend/
│   ├── config.py          # Flask app configuration and database setup
│   ├── main.py            # Flask API routes and endpoints
│   ├── models.py          # Database models (Contact model)
│   ├── requirements.txt    # Python dependencies
│   └── instance/           # Database instances folder
│
├── frontend/
│   ├── index.html         # HTML entry point
│   ├── package.json       # Node.js dependencies and scripts
│   ├── vite.config.js     # Vite configuration
│   ├── src/
│   │   ├── main.jsx       # React app entry point
│   │   ├── App.jsx        # Main App component
│   │   ├── App.css        # App styles
│   │   ├── ContactForm.jsx # Contact form component
│   │   ├── ContactList.jsx # Contact list display component
│   │   ├── index.css      # Global styles
│   │   └── README.md      # Frontend-specific documentation
│   └── public/            # Static assets
│
└── README.md              # This file
```

## 📦 Prerequisites

- **Python 3.8+** for the backend
- **Node.js 16+** and **npm** for the frontend
- **Git** for version control

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone <repository-url>
cd Flask-React-Full-Stack-App-main
```

### 2. Backend Setup

Navigate to the backend folder and install Python dependencies:

```bash
cd backend
pip install -r requirements.txt
```

### 3. Frontend Setup

Navigate to the frontend folder and install Node.js dependencies:

```bash
cd ../frontend
npm install
```

## ▶️ Running the Application

### Start the Backend Server

```bash
cd backend
python main.py
```

The Flask server will run on `http://127.0.0.1:5000`

### Start the Frontend Development Server

In a new terminal:

```bash
cd frontend
npm run dev
```

The React app will typically run on `http://localhost:5173`

## 📡 API Endpoints

### GET `/contacts`
Retrieve all contacts from the database.

**Response:**
```json
{
  "contacts": [
    {
      "id": 1,
      "firstName": "John",
      "lastName": "Doe",
      "email": "john@example.com"
    }
  ]
}
```

### POST `/create_contact`
Create a new contact.

**Request Body:**
```json
{
  "firstName": "Jane",
  "lastName": "Smith",
  "email": "jane@example.com"
}
```

**Response:** 201 Created

### PATCH `/update_contact/<id>`
Update an existing contact by ID.

**Request Body:**
```json
{
  "firstName": "Jane",
  "lastName": "Smith",
  "email": "jane.smith@example.com"
}
```

**Response:** 200 OK

### DELETE `/delete_contact/<id>`
Delete a contact by ID.

**Response:** 200 OK

## 🔧 Configuration

- Backend configuration is managed in `backend/config.py`
- Frontend configuration is available in `frontend/vite.config.js`
- Ensure the frontend is pointing to the correct backend URL (currently `http://127.0.0.1:5000`)

## 📝 Contributing

Contributions are welcome! Feel free to submit issues or pull requests to improve the application.

## � Author

- **GitHub Username:** dev-kelz
- **Email:** kelz.codesgmail.com

## �📄 License

This project is open source and available under the MIT License.

---

**Happy coding!** 🎉
