# meep-backend

## Setup

### Docker
  1. Install Docker
  2. Build docker image from dockerfile:
    ```
    docker build -t meep-backend:gunicorn
    ```
  3. Create and run a container from the image:
    ```
    docker run -p 8000:8000 meep-backend:gunicorn
    ```
  4. In a browser, try typing ```http://localhost:8000/locations``` to see
    if it worked.

### Unix
  1. Install python
     ```
     sudo apt-get install python3
     ```
  2. clone the master branch
  3. create a virtual environment in the project root directory
  4. activate the virtual environment ```source venv/bin/activate```
  5. pip install requiremnets ```pip install -r requirements.txt```
  6. create a sqlite database ```touch dev.db```
  7. set dev database environment variable ```export DEV_DATABASE_URL=sqlite:///dev.db```
  8. Open the database in sqlite with ```sqlite3 dev.db;``` check to see if it created the tables with ```.tables```
  9. try to display data from a table ```select * from projects;``` you should see a list of projects display

  10. set flask environment variable to development
    ```
    export FLASK_ENV=development
    ```
  11. run the app
    ```
    flask run
    ```
  12. test to see if it worked: in a browser, type ```localhost:5000/projects``` you should see some json containing project data




### Windows
  1. Install python
  2. Install pip
  3. Install virtualenv
  4. clone the master branch
  5. create a virtual environment in the project root directory
  6. activate the virtual environment ```venv\Scripts\activate```
  7. pip install requirements ```pip install -r requirements.txt```
  8. set dev database environment variable ```set DEV_DATABASE_URL=sqlite:///dev.db```
  9. set flask environment variable to development
    ```
    set FLASK_ENV=development
    ```
  10. run the app
    ```
    flask run
    ```
  11. test to see if it worked: in a browser, type ```localhost:5000/projects``` you should see some json containing project data
