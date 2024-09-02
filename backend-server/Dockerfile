# Base image
FROM python:3.10-slim

# Set the working directory
WORKDIR /app

# Copy the requirements file
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY . .

# Expose the port the app runs on
EXPOSE 5000

# Set the environment variables (ensure .env is copied)
ENV FLASK_ENV=production

# Command to run the app
CMD ["python", "app.py"]
