#  We Rent! Backend 

This branch adds full unit testing support for the `AuthService` logic, complete with isolated test configuration and mocks. These tests are safe to run and will not interfere with the local PostgreSQL or production data.

<br><br>

## 🛠️ Project Overview

The We Rent! backend is a RESTful API service built with Flask, designed to support the core functionalities of the We Rent! application. It manages user authentication, product listings, product details, reviews, and other business logic required for the rental platform.

<br><br>

## 🔗 Project Links

- **Backend Repository:** [Backend GitHub Repository](https://github.com/rizalandyyy/backend-team-two)
- **Backend Deployment (Koyeb):** [Koyeb Deployment Link](https://indirect-yasmin-ananana-483e9951.koyeb.app/)
- **Postman API Documentation:** [Postman API Documentation](https://documenter.getpostman.com/view/44239234/2sB3B8st5c#1dff3df8-6ee7-4ed8-a064-0ea0660e3472)
- **Frontend Repository:** [Frontend GitHub Repository](https://github.com/rizalandyyy/frontend-team-two)
- **Frontend Deployment (Netlify):** [Netlify Deployment Link](https://your-frontend-site.netlify.app)

<br><br>

## 🗂 Codebase Structure

- `app.py`: The main application entry point where the Flask app is initialized.
- `config/`: Configuration files for different environments and settings.
- `models/`: Database models representing the core entities such as users, products, and reviews.
- `repo/`: Repository layer handling database operations and queries.
- `route/`: Flask route definitions organizing API endpoints by feature.
- `services/`: Business logic and service layer implementing core application functionality.
- `shared/`: Shared utilities and helper modules used across the codebase.
- `migrations/`: Database migration scripts managed by Flask-Migrate.
- `tests/`: Unit and integration tests to ensure code quality and correctness.
- `instance/`: Contains instance-specific files such as the database initialization.

<br><br>

##  Summary of Changes

- Added unit tests for `AuthService` including:
  - `register_user`: success, username taken, email taken
  - `login_user`: success, wrong password, user not found
- Configured test environment in `conftest.py` using:
  - In-memory SQLite
  - Flask-JWT-Extended
  - Flask-Bcrypt
  - Proper app context injection
- Used `pytest` and `pytest-mock` for full mocking
- Ensured that real DB or token behavior is not triggered

<br><br>

##  How to Run Tests

```bash
pip install -r requirements.txt
pytest -v
```

---

