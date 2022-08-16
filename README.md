[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Dzhud/ML-Microservice-With-Kubernetes/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Dzhud/ML-Microservice-With-Kubernetes/tree/master)

## Project Overview

The ML Microsrvice project contains is built on Scikit-Learn. It has a model that predicts house prices in the city of Boston according to features like average rooms in a home and information about highway access, teacher-to-pupil ratios, and etc. For more about the data, go on to [Kaggle](https://www.kaggle.com/c/boston-housing). 
This is all done by testing the ability to operationalize a Flask application which serves predictions based on API calls. It could be extended to any pre-trained machine learning model.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Tested code using linting
* Completed a Dockerfile to containerize the application
* Deployed the containerized application using Docker and make a prediction
* Improved the log statements in the source code for this application
* Configured Kubernetes and created a Kubernetes cluster
* Deployed a container using Kubernetes and made a prediction
* Uploaded a complete Github repo with CircleCI to indicate that the code has been tested

## Project Tasks
* Python 3.7

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
