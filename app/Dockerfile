FROM python:3.9-slim

# Install ping
RUN apt-get update && \
    apt-get install -y iputils-ping && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8080

CMD ["python3", "app.py"]
