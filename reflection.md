# Lab 5: Static Code Analysis — Reflection

## 1. What is static code analysis?

Static code analysis examines source code without executing it to identify potential bugs, security vulnerabilities, maintainability problems, and style violations.

## 2. What are the purposes of Pylint, Bandit, and Flake8?

- **Pylint:** Checks code quality, naming conventions, missing documentation, and potential programming problems.
- **Bandit:** Identifies common security vulnerabilities and unsafe coding practices in Python programs.
- **Flake8:** Checks Python formatting and compliance with style guidelines, including whitespace and line length.

## 3. What issues were identified and fixed?

The analysis identified issues involving mutable default arguments, insecure hashing, temporary-file creation, OTP generation, credential handling, naming conventions, missing docstrings, and formatting.

## 4. Why should mutable default arguments be avoided?

Mutable default arguments, such as lists, are created once when the function is defined and can be shared between calls. Using `None` as the default and creating a new list inside the function prevents unintended sharing.

## 5. How does static analysis improve software quality?

Static analysis detects potential problems early, improves readability and maintainability, encourages consistent coding practices, and helps developers identify security risks before deployment.

## 6. What did you learn from this lab?

I learned how to create a Python virtual environment, install and run Pylint, Bandit, and Flake8, interpret their reports, correct code issues, and rerun the tools to verify the fixes.

## 7. What were the final analysis results?

Pylint reported a score of 10.00/10, Bandit identified no security issues, and Flake8 reported no style violations. The Python file also compiled and executed successfully.
