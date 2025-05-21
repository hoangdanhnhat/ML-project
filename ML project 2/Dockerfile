# Use an official Python runtime as the base image
FROM python:3.10-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file to install dependencies
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code and .joblib files
COPY app.py .
COPY *.joblib .

# Expose the port that Gradio uses (default is 7860)
EXPOSE 7860

# Command to run the Gradio app
CMD ["python", "app.py"]