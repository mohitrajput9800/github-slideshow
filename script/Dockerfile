# Use an official lightweight Python image.
FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Copy requirements and install them
COPY requirements.txt ./
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Copy all files
COPY . .

# Expose port 8080
EXPOSE 8080

# Run with gunicorn for production
CMD ["gunicorn", "app:app", "-b", "0.0.0.0:8080"]
