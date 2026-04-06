## Experiment-13: Flask MySQL Students CRUD API
This is a Flask-based REST API for performing CRUD operations on a Students database using MySQL. It includes data validation with Marshmallow and uses environment variables for database configuration.

## Features
Create: Add new students via POST /students
Read: Retrieve all students via GET /students or a specific student via GET /students/<id>
Update: Modify student details via PUT /students/<id>
Delete: Remove a student via DELETE /students/<id>
Data validation for name (min 2 chars), age (1-120), and unique UID
SSL connection to MySQL using ca.pem

# Prerequisites
Python 3.x
MySQL database
Virtual environment (vir5/)

# API Endpoints
GET /: Health check message
POST /students: Create a student (JSON body: {"name": "string", "age": int, "uid": "string"})
GET /students: Get all students
GET /students/<id>: Get a specific student by ID
PUT /students/<id>: Update a student (partial JSON body allowed)
DELETE /students/<id>: Delete a student

# Error Handling
Validation errors return 400 with details.
Not found errors return 404.
# Dependencies
Flask: Web framework
Flask-SQLAlchemy: ORM for database interactions
Marshmallow: Data validation
PyMySQL: MySQL driver
python-dotenv: Environment variable loading
