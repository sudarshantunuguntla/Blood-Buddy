# Blood Buddy

A Flask-based blood donation and request management web application for managing user accounts, blood requests, and hospital coordination.

## Features

- User signup and login
- Blood group request and donation tracking
- Hospital request and blood availability workflow
- Community blood request posting and viewing
- User dashboard and profile management
- Request history and personal request tracking

## Tech Stack

- Python 3
- Flask
- MongoDB
- HTML, CSS, JavaScript

## Project Structure

```text
blood-buddy/
├── .gitignore
├── README.md
├── requirements.txt
├── bloodbank_main/
│   ├── app.py
│   └── flaskapp/
│       ├── __init__.py
│       ├── static/
│       ├── templates/
│       └── user/
│           ├── __init__.py
│           ├── models.py
│           └── routes.py
└── .venv/   # optional local virtual environment
```

## Prerequisites

- Python 3.10+
- MongoDB running locally on port 27017
- Optional: virtual environment tool such as `venv` or `virtualenv`

## Setup

1. Open a terminal in the project root.
2. Create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows:

```powershell
.venv\Scripts\Activate.ps1
```

On macOS/Linux:

```bash
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Start MongoDB locally.

5. Run the application:

```bash
python bloodbank_main/app.py
```

6. Open the app in your browser:

```text
http://localhost:5000
```

## Configuration

This project connects to MongoDB using the default local setup in [bloodbank_main/flaskapp/__init__.py](bloodbank_main/flaskapp/__init__.py):

- Host: `localhost`
- Port: `27017`
- Databases: `sodabbs`, `hospitals`, `req`, `comm_req`

If your MongoDB server is configured differently, update the connection values in the Flask app initialization.

## Notes

- The app is designed for local development and testing.
- The login and dashboard flows depend on MongoDB collections being populated correctly.
- The project currently uses direct database access and is best suited for a dev environment rather than a production deployment.

