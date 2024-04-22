# Use the official Python image as a base
FROM python:3.9-slim

# Set environment variables
ENV FLASK_APP=app.py
ENV FLASK_ENV=development

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed dependencies specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port the app runs on
EXPOSE 5000

# Run the application
CMD ["flask", "run", "--host=0.0.0.0"]
