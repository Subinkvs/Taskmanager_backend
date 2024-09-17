#Task Manager Backend

##Overview
This is a backend application for a task manager, built with Django and Django REST Framework. It provides CRUD operations for tasks, secure API access using JWT authentication, and includes features such as search functionality and pagination.

Prerequisites
Python 3.12.5 or higher
pip (Python package installer)
Django 5.1 or higher
Django REST Framework

##installations

#Clone the Repository

git clone https://github.com/your-repo/task-manager-backend.git
cd task-manager-backend


#Create and Activate a Virtual Environment

python -m venv myenv
source myenv/bin/activate  # On Windows use `myenv\Scripts\activate`

#Install Dependencies

pip install -r requirements.txt

#Apply Migrations

python manage.py migrate

#Create a Superuser (for accessing the Django admin)

python manage.py createsuperuser

#Run the Development Server

python manage.py runserver

The server will be running at http://localhost:8000/.


##API Endpoints

#List All Tasks

Endpoint: /api/tasks/
Method: GET
Description: Retrieve a list of all tasks with search functionality and pagination.
Query Parameters:
search: Search for tasks by title or description.
page: Page number for pagination.

#Retrieve a Single Task

Endpoint: /api/tasks/<id>/
Method: GET
Description: Retrieve details of a specific task by its ID.

#Create a New Task

Endpoint: /api/tasks/
Method: POST
Description: Create a new task with a title and optional description.

#Update a Task

Endpoint: /api/tasks/<id>/
Method: PUT
Description: Update an existing task's title, description, or status.

#Delete a Task

Endpoint: /api/tasks/<id>/
Method: DELETE
Description: Delete a task by its ID.

#Filter Tasks by Status

Endpoint: /api/tasks/
Method: GET
Description: Filter tasks by their completion status (completed or pending).
Query Parameters:
status: true for completed tasks, false for pending tasks.
