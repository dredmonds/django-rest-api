# django-rest-api project

Django REST API provides endpoint services to all web clients. It provides access into authenticated users to GET, POST, PULL, PATCH and DELETE all available resources.

To configure the development environment, please follow either one of following sets of instructions depending on your use case:

## Installation/Development with Docker

Dependencies:

- Docker Desktop (preferably latest version)
- Docker Hub account (optional)

This project uses Docker compose to setup and run all the necessary components. The docker-compose.yml file provided is meant to be used for running tests and development.

**Note for Mac Users:** By default, docker on Mac will restrict itself to using just 2GB of memory. This [should be increased](https://docs.docker.com/docker-for-mac/#resources) to at least 4GB to avoid running in to unexpected problems.

1.  Clone the repository:

    ```shell
    git clone https://github.com/dredmonds/django-rest-api
    cd django-rest-api
    ```
2.  Build and run the necessary containers for the required environment:

    ```shell
    docker-compose up
    ```

## Native installation (without Docker)

Dependencies:

- Python 3.10.x
- PostgreSQL 12

1.  Clone the repository:

    ```shell
    git clone https://github.com/dredmonds/django-rest-api
    cd django-rest-api
    ```

2.  Install Python 3.10.

    [See this guide](https://docs.python-guide.org/starting/installation/) for detailed instructions for different platforms.

3.  Install system dependencies:

    On Ubuntu:

    ```shell
    sudo apt install build-essential libpq-dev python3.10-dev python3.10-venv
    ```

    On macOS:

    ```shell
    brew install libpq
    ```

4. Install _postgres_, if not done already, as this is required by **psycopg2** in the requirements below

    On Ubuntu:

    ```shell
    sudo apt install postgresql postgresql-contrib
    ```

    On macOS:

    ```shell
    brew install postgresql
    ```

5.  Create and activate the virtualenv:

    ```shell
    python3.10 -m venv env
    source env/bin/activate
    pip install -U pip
    ```

6.  Install the dependencies:

    ```shell
    pip install -r requirements-dev.txt
    ```