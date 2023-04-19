## Cinema Service API

___

### Installation using GitHub

<p>Before you begin, make sure you have Python and PostgreSQL installed on your computer. To do this, run the following commands:</p>

```shell
python3 --version
```

```shell
psql --version 
```

<p>The command output should be Python and PostgreSQL versions, respectively. If it is not, you need to install Python and PostgreSQL on your computer. If everything is ok, follow these steps:</p>

1. Clone the project repository to your computer using the following command:
    ```shell
    git clone https://github.com/bihunva/cinema-api.git
    ```

2. Create and activate a virtual environment (venv) by running the following commands:
    ```shell
    python3 -m venv venv
    source venv/bin/activate # for Unix-based systems
    venv\Scripts\activate # for Windows
    ```

3. Install the necessary dependencies by running the following command:
    ```shell
    pip install -r requirements.txt
    ```

4. Set the following environment variables in your shell or IDE to run the project:
   ```shell
   export DB_HOST=YOUR_DB_HOSTNAME
   export DB_NAME=YOUR_DB_NAME
   export DB_USER=YOUR_DB_USER
   export DB_PASSWORD=YOUR_DB_PASSWORD
   export DB_SECRET_KEY=YOUR_SECRET_KEY
   ```

5. Apply all required migrations by running the following command:
    ```shell
   python manage.py migrate
    ```

6. Start the local server by running the following command:
    ```shell
    python manage.py runserver
    ```

___

### Installation using Docker

<p>Before you begin, make sure you have Docker installed on your computer. To do this, run the following command:</p>

```shell
docker --version
```

<p>The result of the execution should be the docker version. If it is not, install docker on your computer, if everything is ok, follow these steps:</p>

1. Clone the project repository to your computer using the following command:
    ```shell
    git clone https://github.com/bihunva/cinema-api.git
    ```

2. Add the <strong>.env</strong> file to the root of the project. In this file you must specify the values of the
   environment variables, an example is in the file <strong>.env.sample</strong>.

3. Build Docker images by running the following command:
   ```shell
   docker-compose build
   ```

4. Run Docker containers by running the following command:
   ```shell
   docker-compose up
   ```

___

### Getting Access

To get access to Cinema Service API, you need to create a user account and
obtain an access token.

<p><strong>User creating</strong> - send a POST request to /api/user/register/ <br>
<strong>Obtain token</strong> - send a POST request to /api/user/token/</p>

___

### Features

<ul>
<li>JWT authenticated</li>
<li>Documentation is located at /api/doc/swagger/</li>
<li>Managing orders and tickets</li>
<li>Creating movies with genres, actors, cinema halls</li>
<li>Adding movie sessions</li>
<li>Filtering movies and movie sessions</li>
</ul>
