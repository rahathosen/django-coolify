# Django Coolify Template

## Project Overview

This project demonstrates how to set up a Django application with Docker, using best practices for deployment and development. It includes configurations for using PostgreSQL as the database, Gunicorn as the WSGI HTTP server, and Whitenoise for serving static files.

## Prerequisites

- Python 3.12

## Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/rahathosen/django-coolify
   cd django-coolify
   ```

2. **Create a `.env` file:**

   Copy the `.env.example` to `.env` and fill in the necessary environment variables.

3. **Set up the environment using Poetry:**

   - Install the dependencies:
     ```bash
     poetry install
     ```
   - Activate the virtual environment:
     ```bash
     poetry shell
     ```

4. **Apply database migrations:**

   ```bash
   python manage.py migrate
   ```

5. **Run the Django development server:**

   ```bash
   python manage.py runserver
   ```

6. **Access the application:**

   The application will be available at `http://localhost:8000`.

## Alternative Setup Using pip

1. **Create a virtual environment:**

   ```bash
   python -m venv venv
   ```

2. **Activate the virtual environment:**

   - On macOS and Linux:
     ```bash
     source venv/bin/activate
     ```
   - On Windows:
     ```bash
     .\venv\Scripts\activate
     ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply database migrations:**

   ```bash
   python manage.py migrate
   ```

5. **Run the Django development server:**

   ```bash
   python manage.py runserver
   ```

## Project Structure

- `Dockerfile`: Contains the instructions to build the Docker image in coolify.
- `docker-compose.yaml`: Defines the services and configurations for deployment in production.
- `pyproject.toml`: Manages the project dependencies using Poetry.

## Dependencies

- Django 5.1.5
- Whitenoise 6.8.2
- dj-database-url 2.3.0
- psycopg2-binary 2.9.10
- Gunicorn 23.0.0
- Python Decouple 3.8
