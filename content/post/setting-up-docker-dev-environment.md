---
title: "Setting Up Docker Dev Environment"
date: 2019-12-30T21:24:24-08:00
draft: false
image: "/uploads/docker-compose.jpg"
tags: ["development"]
---

This is a walkthrough to setup a new Python dev environment with Docker


## Requirements:

Docker Desktop installed

    https://docs.docker.com/docker-for-mac/install/


## Getting started

Let's create a new project

    mkdir docker-flask
    cd docker-flask

Create a directory for the flask app

    mkdir flask_app
    touch __init__.py

Create a docker and docker-compose file for the flask project

    touch flask_app/Dockerfile
    touch docker-compose.yml

Let's create a started flask project

    touch app.py
    touch requirements.txt

Open the `app.py` file and put the following content:

    from flask import Flask

    app = Flask(__name__)

    @app.route('/')
    def hello_world():
        return 'Hello world!'

    if __name__ == '__main__':
        app.run(host='0.0.0.0')

Open the `requirements.txt` file and put the following content:

    Flask==1.1.1
    yapf==0.29.0
    pylint==2.4.4



## Docker commands

Build a new docker image for our app

    docker build -t flaskapp:latest .

`docker build -t <new-image-name>` to name the new image, `.` to say where is the folder for the app

The Flask server will start, follow the link and you should be able to see the `Hello world` app in your brownser !!
