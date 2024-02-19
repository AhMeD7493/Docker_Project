# Base image
FROM python:3.12

# Set environment variables
ENV PYTHONUNBUFFERED 1

# Set the working directory in the container
WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --upgrade pip
RUN pip install -r requirements.txt


COPY . .

# Expose the port the app runs on
EXPOSE 8000

# Run the Django app
CMD ["python", "manage.py", "runserver"]
