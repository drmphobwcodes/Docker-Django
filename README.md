# Docker-Django
Features:
User Authentication:
Allow users to register, login, and logout.
Ensure secure password storage.
CRUD Operations on a Resource:
Users can perform CRUD operations (Create, Read, Update, Delete) on a specific resource. For example, let's use a "Task" resource for demonstration purposes.
API Endpoints:
User Authentication:
POST /api/auth/register: Register a new user.
POST /api/auth/login: Login with username and password.
POST /api/auth/logout: Logout the currently authenticated user.
CRUD Operations on Tasks:
GET /api/tasks/: Retrieve all tasks.
POST /api/tasks/: Create a new task.
GET /api/tasks/<task_id>/: Retrieve a specific task by ID.
PUT /api/tasks/<task_id>/: Update a specific task by ID.
DELETE /api/tasks/<task_id>/: Delete a specific task by ID.
Database Tables:
Database Name: task_manager

User Table:
Columns:
id: Primary Key, Integer
username: Unique, String
password: String (hashed)
Constraints:
Primary Key: id
Task Table:
Columns:
id: Primary Key, Integer
title: String
description: Text
completed: Boolean
created_at: DateTime
updated_at: DateTime
user_id: Foreign Key (references User Table)
Constraints:
Primary Key: id
Foreign Key: user_id references User.id
