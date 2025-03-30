# Django-react-auth
# Django + React Authentication

## Overview
This project integrates **Django (backend)** and **React (frontend)** for a secure authentication system. It uses **JWT-based authentication** to handle user login, registration, and protected routes.

## Features
- User Registration & Login
- Token-based authentication (JWT)
- Protected API endpoints
- React Context API for state management
- Logout functionality

## Tech Stack
- **Backend**: Django, Django REST Framework (DRF), SimpleJWT
- **Frontend**: React.js, React Router, Axios, Context API
- **Database**: SQLite

---

## Installation & Setup

### 1. Clone the Repository
```sh
git clone https://github.com/your-username/django-react-auth.git
cd django-react-auth
```

### 2. Backend Setup (Django)
#### a) Create a Virtual Environment
```sh
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

#### b) Install Dependencies
```sh
pip install -r requirements.txt
```

#### c) Apply Migrations
```sh
python manage.py migrate
```

#### d) Create a Superuser (Optional)
```sh
python manage.py createsuperuser
```

#### e) Run the Backend Server
```sh
python manage.py runserver
```

---

### 3. Frontend Setup (React)
#### a) Navigate to Frontend Directory
```sh
cd frontend
```

#### b) Install Dependencies
```sh
npm install
```

#### c) Start the React Development Server
```sh
npm start
```

---

## API Endpoints
| Method | Endpoint           | Description          |
|--------|-------------------|----------------------|
| POST   | `/api/register/`  | User Registration   |
| POST   | `/api/login/`     | User Login          |
| POST   | `/api/logout/`    | User Logout         |
| GET    | `/api/user/`      | Get Authenticated User |


---

## Environment Variables
Create a `.env` file in the `backend/` and `frontend/` directories with the following variables:

**Backend (.env):**
```
SECRET_KEY=your_secret_key
DEBUG=True
ALLOWED_HOSTS=*
```

**Frontend (.env):**
```
REACT_APP_API_URL=http://localhost:8000/api
```

---

## Authentication Flow
1. User registers via `/api/register/`.
2. User logs in and receives a JWT token.
3. Token is stored in local storage or cookies.
4. Protected routes require authentication.
5. User logs out, and the token is removed.

---

## Contribution
Feel free to fork this project and submit pull requests!

---

## License
MIT License. Free to use and modify.

