# Use a lightweight, updated Python base image
FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Copy all project files
COPY . /app

# Update system packages and install dependencies securely
RUN apt-get update && apt-get upgrade -y && \
    pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir flask && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Expose Flask default port
EXPOSE 5000

# Command to run the app
CMD ["python", "app.py"]
