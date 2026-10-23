# ToDo App — CI/CD with GitHub Actions

## Project Description

This project is a simple REST API for managing ToDo tasks, created as part of a CI/CD laboratory assignment.

The project uses **GitHub Actions** to automatically run tests whenever code is pushed to the `main` branch or a pull request is created.

## Technologies Used

- Python 3.12
- Flask
- Pytest
- Docker
- GitHub Actions

## Project Structure

```text
todo-app/
├── app/
│   ├── __init__.py
│   └── main.py
├── tests/
│   └── test_main.py
├── .github/
│   └── workflows/
│       └── ci.yml
├── Dockerfile
├── pytest.ini
├── requirements.txt
└── README.md
```

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/health` | Checks application health |
| GET | `/todos` | Returns all ToDo tasks |
| POST | `/todos` | Creates a new ToDo task |

### Example Request

Create a ToDo task:

```json
{
  "title": "Learn GitHub Actions"
}
```

## Installation and Local Setup

### 1. Clone the repository

```bash
git clone https://github.com/Mariyam777/todo-app.git
cd todo-app
```

### 2. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 3. Run tests

```bash
python -m pytest -v
```

### 4. Run the application

```bash
python -m app.main
```

The API will be available at `http://localhost:5000`.

Health check: `http://localhost:5000/health`

## CI/CD Workflow

The GitHub Actions workflow:

1. Checks out the repository.
2. Sets up Python 3.12.
3. Installs project dependencies.
4. Runs automated tests with Pytest.

The workflow runs automatically on pushes and pull requests targeting `main`. It can also be started manually through the GitHub Actions tab.

## Docker

A `Dockerfile` is included to package the application into a Docker image.

## Author

Mariyam Usubalieva
