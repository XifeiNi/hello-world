# How to run locally.

1. Install pip
2. Install Virtual environment using `pip3 install virtualenv` OR `sudo apt install virtual env`
3. Create a virtual environment using `virtualenv venv`
4. Activate the python environment using `source venv/bin/activate`
5. Install requirements using `pip3 install -r requirements.txt`
6. Run `python3 weather.py`
7. Deactivate virtual env using `deactivate`

# How to Deploy to Heroku

## Server
```
$ virtualenv -p python3 venv
$ pip install -r requirements.txt
$ gunicorn app:app
```
## Client
```
$ cd client
$ npm install
$ npm run build
```
To check the build directory on a static server :
```
$ cd build
$ python3 -m http.server
```

Deployment on Heroku
```
$ heroku login ...
$ heroku create <your-app-name>
$ heroku git:remote <your-app-name>
$ git push heroku master
```
