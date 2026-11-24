# fastapi-example [![CircleCI](https://circleci.com/gh/marciovrl/fastapi-example.svg?style=svg)](https://circleci.com/gh/marciovrl/fastapi-example)

A simple example of using Fast API in Python.

## Preconditions:

- Python 3

## Clone the project

```
git clone https://github.com/marciovrl/fastapi-example.git
```

## Run local

### Install dependencies

```
py -m pip install -r requirements.txt
```

### Run server

```
uvicorn app.main:app --reload
```

### Run test

```
pytest app/test.py
```

## Code quality with Ruff

Install the project dependencies, including Ruff:

```
pip install -r requirements.txt
```

Check lint rules across the application and tests:

```
py -m ruff check .
```

Check formatting without modifying files:

```
py -m ruff format --check .
```

The Ruff configuration is in `pyproject.toml`. It enables broad checks for
correctness, imports, naming, type annotations, docstrings, maintainability,
and Python style so the example can be used to exercise code-quality reviews.

## Run with docker

### Run server

```
docker-compose up -d --build
```

### Run test

```
docker-compose exec app pytest test/test.py
```

## API documentation (provided by Swagger UI)

```
http://127.0.0.1:8000/docs
```

### Run server

```
docker-compose exec db psql --username=fastapi --dbname=fastapi_dev
```
