# Session Authentication

## Overview
This repository contains the implementation of a Session Authentication system as part of a curriculum. The authentication system is designed for educational purposes, walking through the steps of creating a session-based authentication mechanism without using external modules or frameworks.

## Short Specialization: Session Authentication
- **Average Grade:** 73.99%
- **Instructor:** Guillaume, CTO at Holberton School
- **Project Dates:** Feb 14, 2024 - Feb 16, 2024
- **Project Weight:** 1

## Project Background
The project focuses on implementing Session Authentication, a mechanism used in the industry to manage user sessions securely. The implementation is done step by step, exploring the creation and validation of session IDs without using external modules.

## Learning Objectives
Upon completion of this project, students are expected to understand:
- General concepts of authentication
- Session authentication principles
- Cookie usage and manipulation
- Implementation details of session authentication without external modules

## Requirements
- Python 3.7 on Ubuntu 18.04 LTS
- Code follows PEP 8 style guide
- Documentation for all modules, classes, and functions
- Execution of scripts is validated
- Length of files checked with `wc`

## Tasks
1. **Et moi et moi et moi!**
   - Copy previous work from the Basic Authentication project and add a new endpoint.

2. **Empty session**
   - Create a SessionAuth class inheriting from Auth and validate the inheritance.

3. **Create a session**
   - Implement methods to generate and store session IDs.

4. **User ID for Session ID**
   - Implement a method to retrieve User IDs based on Session IDs.

5. **Session cookie**
   - Add a method to retrieve the session cookie from a request.

6. **Before request**
   - Update the before_request method to handle authentication.

7. **Use Session ID for identifying a User**
   - Implement a method to retrieve a User based on the session ID.

8. **New view for Session Authentication**
   - Create a new Flask view to handle session authentication routes.

9. **Logout**
   - Implement a method to destroy a session and log out the user.

## How to Run
1. Install dependencies: `pip install -r requirements.txt`
2. Set environment variables:
   - `API_HOST=0.0.0.0`
   - `API_PORT=5000`
   - `AUTH_TYPE=session_auth`
   - `SESSION_NAME=_my_session_id`
3. Run the main application: `python3 -m api.v1.app`

## Testing
Use curl commands to test various routes and authentication scenarios as described in the project tasks.

## Repository Structure
- `api/v1`: Contains the main application and authentication-related files.
- `tests`: Directory for testing scripts.
- `main_*.py`: Example scripts to demonstrate authentication processes.

