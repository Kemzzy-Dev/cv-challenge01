FROM python:3.11-slim

WORKDIR /app

COPY . .

RUN pip install poetry uvicorn

RUN poetry install

CMD poetry run bash ./prestart.sh; poetry run uvicorn app.main:app --host 0.0.0.0