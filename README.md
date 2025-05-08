# Django API Project

This project provides a RESTful API for authentication, user management, banks, and transactions using Django and Django REST Framework.

---

## 🚀 Getting Started (Local Development Setup)

### 1. Clone the Repository

```bash
git clone <repository_url>
cd <project_directory>
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply Migrations

```bash
python manage.py migrate
```

### 5. Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

### 6. Run the Server

```bash
python manage.py runserver
```

Now open your browser at: `http://127.0.0.1:8000`

---

## 📃 API Endpoints

### Authentication

* `POST /api/auth/change-password/` — Change password
* `POST /api/auth/login/` — Login
* `POST /api/auth/password-reset/` — Request password reset
* `POST /api/auth/password-reset-confirm/` — Confirm password reset
* `POST /api/auth/refresh/` — Refresh token

### Banks

* `GET /api/banks/` — List banks
* `POST /api/banks/` — Create bank
* `GET /api/banks/{id}/` — Retrieve bank
* `PUT /api/banks/{id}/` — Update bank
* `PATCH /api/banks/{id}/` — Partial update bank
* `DELETE /api/banks/{id}/` — Delete bank

### Transactions

* `GET /api/transactions/` — List transactions
* `POST /api/transactions/` — Create transaction
* `GET /api/transactions/{id}/` — Retrieve transaction
* `PUT /api/transactions/{id}/` — Update transaction
* `PATCH /api/transactions/{id}/` — Partial update transaction
* `DELETE /api/transactions/{id}/` — Delete transaction
* `POST /api/transactions/{id}/reconcile/` — Reconcile transaction
* `POST /api/transactions/{id}/verify/` — Verify transaction

### Users

* `GET /api/users/` — List users
* `POST /api/users/` — Create user
* `GET /api/users/me/` — Get current user profile
* `GET /api/users/{id}/` — Retrieve user
* `PUT /api/users/{id}/` — Update user
* `PATCH /api/users/{id}/` — Partial update user
* `DELETE /api/users/{id}/` — Delete user

---

## 🔧 API Testing Example

Example using `curl` to create a new user:

```bash
curl -X POST http://127.0.0.1:8000/api/users/ \
-H "Content-Type: application/json" \
-d '{"username": "testuser", "password": "password123"}'
```

---

## 📖 References

* [Django Documentation](https://docs.djangoproject.com/)
* [Django REST Framework](https://www.django-rest-framework.org/)

---

## 📅 License

MIT License — feel free to use and modify!
