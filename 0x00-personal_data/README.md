# ALX Backend User Data Project

## Curriculum

### Short Specializations
- **Back-end**
  - **Authentication**
    - *By:* Emmanuel Turlay, Staff Software Engineer at Cruise
    - *Weight:* 1
    - *Project Dates:* Feb 7, 2024, 6:00 AM - Feb 9, 2024, 6:00 AM
    - *Checker Release:* Feb 7, 2024, 6:00 PM
    - *QA Review:* Manual review required after project completion
    - *Auto Review:* Scheduled at the deadline

### Resources
Read or watch:
- [What Is PII, non-PII, and Personal Data?](#)
- [Logging Documentation](#)
- [Bcrypt Package](#)
- [Logging to Files, Setting Levels, and Formatting](#)

### Learning Objectives
By the end of this project, you should be able to explain to anyone:
- Examples of Personally Identifiable Information (PII)
- How to implement a log filter that obfuscates PII fields
- How to encrypt a password and validate an input password
- How to authenticate to a database using environment variables

### Requirements
- All files interpreted/compiled on Ubuntu 18.04 LTS using Python3 (version 3.7)
- All files should end with a new line
- The first line of all files should be exactly `#!/usr/bin/env python3`
- A `README.md` file at the root of the project folder is mandatory
- Code should follow the `pycodestyle` style (version 2.5)
- All files must be executable
- Code length will be tested using `wc`
- All modules, classes, and functions should have documentation
- Functions should be type-annotated

## Tasks

### 0. Regex-ing
- Write a function `filter_datum` that obfuscates log messages using regex.
- The function should be less than 5 lines long and use `re.sub` for substitution.
- Example usage:
  ```python
  filter_datum(["password", "date_of_birth"], 'xxx', "name=egg;email=eggmin@eggsample.com;password=eggcellent;date_of_birth=12/12/1986;", ';')
  ```

### 1. Log formatter
- Update the `RedactingFormatter` class to accept a list of fields as a constructor argument.
- Implement the `format` method to filter values in incoming log records using `filter_datum`.
- Example usage:
  ```python
  RedactingFormatter(fields=("email", "ssn", "password"))
  ```

### 2. Create logger
- Implement a `get_logger` function that returns a logging.Logger object named "user_data."
- Logger should log up to logging.INFO level and have a StreamHandler with `RedactingFormatter` as formatter.
- Use the `PII_FIELDS` constant to parameterize the formatter.

### 3. Connect to secure database
- Implement a `get_db` function to connect to a secure holberton database using environment variables.
- Use the `mysql-connector-python` module for database connection.

### 4. Read and filter data
- Implement a `main` function to obtain a database connection and retrieve all rows in the users table.
- Display each row under a filtered format using the logger.

### 5. Encrypting passwords
- Implement a `hash_password` function to hash passwords using the `bcrypt` package.

### 6. Check valid password
- Implement an `is_valid` function to validate passwords using `bcrypt`.

## Copyright
Copyright © 2024 ALX, All rights reserved.
