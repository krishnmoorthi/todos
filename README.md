# FastAPI Todos Application

A lightweight RESTful Todo API built with **FastAPI**, **SQLAlchemy**, and **SQLite**.

---

## Tech Stack

| Library | Purpose |
|---|---|
| FastAPI | Web framework & routing |
| Uvicorn | ASGI server |
| SQLAlchemy | ORM & database toolkit |
| Pydantic v2 | Data validation & schemas |
| SQLite | Lightweight database |

---

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/todos.git
cd todos
```

### 2. Create & Activate Virtual Environment
```bash
python -m venv .venv
source .venv/Scripts/activate   # Git Bash on Windows
source .venv/bin/activate       # macOS / Linux
```

### 3. Install Dependencies
```bash
pip install fastapi uvicorn sqlalchemy
```

### 4. Run the Application
```bash
uvicorn app:app --reload --port 8010
```

| URL | Description |
|---|---|
| http://127.0.0.1:8010 | API Base URL |
| http://127.0.0.1:8010/docs | Swagger UI |
| http://127.0.0.1:8010/redoc | ReDoc |

---

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/todos` | Retrieve all todos |
| `GET` | `/todos/{id}` | Retrieve a single todo by ID |
| `POST` | `/todos` | Create a new todo |
| `PUT` | `/todos/{id}` | Update an existing todo by ID |
| `DELETE` | `/todos/{id}` | Delete a todo by ID |

---

## Request & Response Examples

### Create a Todo — `POST /todos`

**Request Body**
```json
{
  "title": "Buy groceries",
  "description": "Milk, eggs, bread"
}
```

**Response — 201 Created**
```json
{
  "id": 1,
  "title": "Buy groceries",
  "description": "Milk, eggs, bread",
  "completed": false
}
```

### Update a Todo — `PUT /todos/{id}`

**Request Body**
```json
{
  "completed": true
}
```

---

## Project Structure

```
todos/
├── app.py        # Main application — routes, models, schemas
├── todos.db      # SQLite database (auto-created on first run)
├── .venv/        # Virtual environment
└── README.md     # This file
```

---

> Built with FastAPI • Happy Coding! 🚀
