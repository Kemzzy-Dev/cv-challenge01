FROM python:3.11-slim

WORKDIR /app

COPY . .

RUN pip install poetry uvicorn

RUN poetry install

RUN poetry run bash ./prestart.sh

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]