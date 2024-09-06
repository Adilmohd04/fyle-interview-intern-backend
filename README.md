# Fyle Backend Challenge

## Who is this for?

This challenge is meant for candidates who wish to intern at Fyle and work with our engineering team. You should be able to commit to at least 6 months of dedicated time for internship.

## Why work at Fyle?

Fyle is a fast-growing Expense Management SaaS product. We are ~40 strong engineering team at the moment. 

We are an extremely transparent organization. Check out our [careers page](https://careers.fylehq.com) that will give you a glimpse of what it is like to work at Fyle. Also, check out our Glassdoor reviews [here](https://www.glassdoor.co.in/Reviews/Fyle-Reviews-E1723235.htm). You can read stories from our teammates [here](https://stories.fylehq.com).


## Challenge outline

**You are allowed to use any online/AI tool such as ChatGPT, Gemini, etc. to complete the challenge. However, we expect you to fully understand the code and logic involved.**

This challenge involves writing a backend service for a classroom. The challenge is described in detail [here](./Application.md)


## What happens next?

You will hear back within 48 hours from us via email. 



Here’s the modified documentation specifically for Windows, based on the instructions you provided:

---

# Documentation: Setup, Run, Test, and Dockerize the Backend Code (Windows)

## Installation

### 1. Fork and Clone the Repository
1. **Fork the repository** to your own GitHub account by clicking the "Fork" button on GitHub.
2. **Clone the forked repository** to your local machine:
    ```cmd
    git clone https://github.com/YourUsername/fyle-interview-intern-backend.git
    cd fyle-interview-intern-backend
    ```

### 2. Install Requirements
1. **Create and activate a virtual environment**:
    ```cmd
    python -m venv env
    env\Scripts\activate
    ```

2. **Install the required dependencies** from the `requirements.txt` file:
    ```cmd
    pip install -r requirements.txt
    ```

---

## Reset Database

To reset the database, follow these steps:

1. **Set the environment variable for Flask**:
    ```cmd
    set FLASK_APP=core/server.py
    ```

2. **Delete the SQLite database** (if it exists):
    ```cmd
    del core\store.sqlite3
    ```

3. **Run the database migration** to upgrade the database schema:
    ```cmd
    flask db upgrade -d core/migrations
    ```

---

## Start the Server

To start the server, you need to run the `run.sh` script. For Windows, you'll run the following command (assuming you have Git Bash or another Bash shell available):

1. **Start the server**:
    ```bash
    bash run.sh
    ```

If you do not have a Bash shell, you can copy the contents of `run.sh` and execute the commands manually in Command Prompt:
```cmd
set FLASK_APP=core/server.py
set FLASK_ENV=development
flask run
```

---

## Run Tests

To run the tests, follow these steps:

1. **Run unit tests**:
    ```cmd
    pytest -vvv -s tests/
    ```

2. **For test coverage report**:
    ```cmd
    pytest --cov
    ```

3. **To view the HTML coverage report**:
    1. Run the following command:
        ```cmd
        pytest --cov
        ```
    2. Open the HTML report by navigating to:
        ```
        htmlcov\index.html
        ```

---
Here’s an updated version of the documentation that includes Dockerization and testing for Docker on Windows:

---

# Documentation: Setup, Run, Test, and Dockerize the Backend Code (Windows)

## Installation

### 1. Fork and Clone the Repository
1. **Fork the repository** to your GitHub account.
2. **Clone the forked repository** to your local machine:
    ```cmd
    git clone https://github.com/YourUsername/fyle-interview-intern-backend.git
    cd fyle-interview-intern-backend
    ```

### 2. Install Requirements
1. **Create and activate a virtual environment**:
    ```cmd
    python -m venv env
    env\Scripts\activate
    ```

2. **Install the required dependencies**:
    ```cmd
    pip install -r requirements.txt
    ```

---

## Reset Database

1. **Set the Flask environment variable**:
    ```cmd
    set FLASK_APP=core/server.py
    ```

2. **Delete the SQLite database** (if it exists):
    ```cmd
    del core\store.sqlite3
    ```

3. **Run the database migrations**:
    ```cmd
    flask db upgrade -d core/migrations
    ```

---

## Start the Server

1. If using **Git Bash** or another Bash shell on Windows, start the server by running:
    ```bash
    bash run.sh
    ```

2. If using **Command Prompt**, manually run the commands from `run.sh`:
    ```cmd
    set FLASK_APP=core/server.py
    set FLASK_ENV=development
    flask run
    ```

---

## Run Tests

### 1. Run Unit Tests:
```cmd
pytest -vvv -s tests/
```

### 2. Generate Test Coverage Report:
```cmd
pytest --cov
```

### 3. View HTML Coverage Report:
After running the test coverage command, open the HTML report:
```cmd
start htmlcov\index.html
```


### 4. Build and Run the Docker Container

#### 4.1. Build the Docker Image
In Command Prompt, run the following to build the Docker image:
```cmd
docker-compose build
```

#### 4.2. Run the Docker Container
Once the image is built, start the container:
```cmd
docker-compose up
```
### 5. Testcases Passed 
![test completed](https://github.com/user-attachments/assets/af780ec9-ab9b-49c0-b5c0-9ecfab14e5d5)

