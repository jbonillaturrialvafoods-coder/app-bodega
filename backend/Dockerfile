# Backend Dockerfile - FastAPI
FROM python:3.11-slim

WORKDIR /app
COPY src/backend/app ./app
COPY src/backend/requirements.txt ./requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

# Opcional: permitir pasar DATABASE_URL como build-arg (no recomendado para secretos)
ARG DATABASE_URL
ENV DATABASE_URL=${DATABASE_URL}

EXPOSE 8000
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
