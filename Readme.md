# MiniTask API – Docker and CI/CD Assessment

## Project Overview
MiniTask API is a simple REST API developed using Python and FastAPI. It supports basic task management operations and provides a health-check endpoint.

## Technologies Used
- Python 3.12
- FastAPI
- Uvicorn
- Pytest
- Docker
- Docker Compose
- GitHub Actions

## Project Structure
```text
MiniTask_Student_Starter/
├── app/
│   └── main.py
├── tests/
│   └── test_api.py
├── .github/
│   └── workflows/
│       └── ci.yml
├── Dockerfile
├── compose.yaml
├── requirements.txt
└── requirements-dev.txt
```

## Run the Project Locally

Install dependencies:

```bash
python -m pip install -r requirements-dev.txt
```

Start the API:

```bash
python -m uvicorn app.main:app --reload
```

Open http://localhost:8000/docs to access Swagger UI.

## Run Tests

```bash
python -m pytest -q
```

## Build Docker Image

```bash
docker build -t minitask-api .
```

## Run with Docker Compose

```bash
docker compose up --build -d
```

Check running containers:

```bash
docker compose ps
```

Stop the application:

```bash
docker compose down
```

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/health` | Health check |
| GET | `/tasks` | Retrieve tasks |
| POST | `/tasks` | Create a task |

## CI/CD Pipeline

GitHub Actions automatically performs the following steps when code is pushed to the main branch:

1. Checks out the repository.
2. Sets up Python 3.12.
3. Installs dependencies.
4. Runs automated tests.
5. Builds the Docker image.

## Project Repository

https://github.com/pujitha-26/MiniTask-API
