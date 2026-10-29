# Start with Python installed
FROM python:3.12-slim

# Work inside /app in the container
WORKDIR /app

# Copy and install Python dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY . .

# Document the application's port
EXPOSE 5003

# Start the Python application
CMD ["python", "app.py"]