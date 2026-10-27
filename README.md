# blogApp-api 🚀

A robust API built with FastAPI, designed for managing blog content. It features complete CRUD operations for blogs, secure JWT-based authentication, and user authorization. The API is integrated with SQLAlchemy for efficient database interactions and provides a clear structure for managing blog posts and users.

## Features ✨

- **CRUD Operations:** Full Create, Read, Update, and Delete functionality for blog posts.
- **JWT Authentication:** Secure user authentication using JSON Web Tokens.
- **User Authorization:** Implements mechanisms to control access to resources.
- **Database Integration:** Utilizes SQLAlchemy for interacting with a SQLite database.
- **Dynamic Routing:** Organizes API endpoints for blogs, users, and authentication.
- **Password Hashing:** Securely stores passwords using bcrypt hashing.
- **API Documentation:** Auto-generated interactive API documentation via Swagger UI.

## Tech Stack 🛠️

- **Framework:** FastAPI
- **Language:** Python
- **Database:** SQLAlchemy (SQLite)
- **Authentication:** JWT (HS256), Passlib (bcrypt)
- **Dependencies:** Uvicorn, Python-multipart, python-jose

## Usage 💡

This API provides endpoints for managing blogs and users, secured with JWT authentication.


### Blog Operations

*   **Create Blog:** `POST /blog/`
*   **Get All Blogs:** `GET /blog/`
*   **Get Specific Blog:** `GET /blog/{id}`
*   **Update Blog:** `PUT /blog/{id}`
*   **Delete Blog:** `DELETE /blog/{id}`

### User Operations

*   **Create User:** `POST /user/`
*   **Get User:** `GET /user/{id}`


**Example Workflow:**

1.  Register a new user via `POST /user/`.
2.  Log in with the user's credentials via `POST /login` to get an access token.
3.  Use the access token to create new blog posts via `POST /blog/`.
4.  Retrieve, update, or delete blog posts using their respective endpoints and the access token.

## Project Structure 📁

The project follows a modular structure typical for FastAPI applications:

```
blogApp-api/
├── blog/
│   ├── __init__.py
│   ├── database.py       # Database connection and session management
│   ├── hashing.py        # Password hashing utilities
│   ├── main.py           # FastAPI application setup and router inclusion
│   ├── models.py         # SQLAlchemy database models (Blog, User)
│   ├── oauth2.py         # OAuth2 dependency for JWT authentication
│   ├── schemas.py        # Pydantic schemas for request/response validation
│   ├── token.py          # JWT token creation and verification functions
│   ├── repository/
│   │   ├── blog.py       # Repository functions for blog operations
│   │   └── user.py       # Repository functions for user operations
│   └── routes/
│       ├── __init__.py
│       ├── authentication.py # Authentication routes (login)
│       ├── blog.py       # Blog-related API routes
│       └── user.py       # User-related API routes
├── requirements.txt      # Project dependencies
├── main.py               # Alternative FastAPI app entry point (simplified)
└── blog.db               # SQLite database file (generated)
```

---
*Feel free to star ⭐, fork 🍴, and create issues 💡 for this project.*
