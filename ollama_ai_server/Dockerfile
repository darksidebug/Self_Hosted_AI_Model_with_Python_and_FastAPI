FROM python:3.10-slim

WORKDIR /app

# Install curl (and other dependencies if needed)
RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

ENV OLLAMA_URL=http://ollama:11434/api/generate

EXPOSE 8000
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000", "--loop", "uvloop"]
