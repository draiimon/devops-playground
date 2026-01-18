FROM python:3.11-slim

# Set working directory inside container
WORKDIR /app

# Copy requirements and install
COPY backend/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the backend folder contents into /app
COPY backend/ ./

# Expose FastAPI port
EXPOSE 8000

# Run FastAPI using uvicorn
# Note: main.py is directly under /app, app object should be 'app'
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
