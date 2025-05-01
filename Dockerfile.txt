# Use Python base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy application code
COPY . .

# Install dependencies
RUN pip install flask

# Expose the port Flask runs on
EXPOSE 80

# Run the application
CMD ["python", "app.py"]
