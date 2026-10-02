# Simple API

A minimal [FastAPI](https://fastapi.tiangolo.com/) application with tests and a Dockerfile.

## Endpoints

| Method | Path     | Response                               |
| ------ | -------- | -------------------------------------- |
| GET    | `/hello` | `{"message": "Hello from CI/CD"}`      |

Interactive API docs are available at `/docs` once the server is running.

## Run locally

Requires Python 3.10+.

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
uvicorn app:app --reload
```

Then open http://127.0.0.1:8000/hello

## Run tests

```bash
pytest
```

## Run with Docker

```bash
docker build -t simple-api .
docker run -p 8000:8000 simple-api
```

Then open http://127.0.0.1:8000/hello

## Project structure

```
.
├── app.py             # FastAPI application
├── test_app.py        # Tests
├── requirements.txt   # Python dependencies
└── Dockerfile         # Container image
```
