[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Dzhud/ML-Microservice-With-Kubernetes/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Dzhud/ML-Microservice-With-Kubernetes/tree/master)

## Project Overview

The ML Microsrvice project contains is built on Scikit-Learn. It has a model that predicts house prices in the city of Boston according to features like average rooms in a home and information about highway access, teacher-to-pupil ratios, and etc. For more about the data, go on to [Kaggle](https://www.kaggle.com/c/boston-housing). 
This is all done by testing the ability to operationalize a Flask application which serves predictions based on API calls. It could be extended to any pre-trained machine learning model.

### Project Tasks

The project goal is to operationalize a working, machine learning microservice using [kubernetes](https://kubernetes.io/). These are some of the completed actions:
* Tested code using linting
* Completed a Dockerfile to containerize the application
* Deployed the containerized application using Docker and make a prediction
* Improved the log statements in the source code for this application
* Configured Kubernetes and created a Kubernetes cluster
* Deployed a container using Kubernetes and made a prediction
* Uploaded a complete Github repo with CircleCI to indicate that the code has been tested

## Requirement
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
* Run minikube: `minikube start`


### Project Files
* `docker_out.txt`: terminal output containing log info after running prediction to docker container
* `kubernetes_out.txt`: terminal output containing log info after running prediction to kubernetes cluster
* `config.yml`: Circeci configuration file
* `app.py`: Flask script
* `Dockerfile`: contains every command used in the building and running of a docker image
* `make_prediction.sh`: source code is responsible for passing data through a trained, machine learning model, and responding with a predicted value for the house price.
* `Makefile`: used to test and install software, build scripts, and collect and run task
* `requirements.txt`: has the libraries of installed dependencies
* `run_docker.sh`: to run and build a docker image
* `run_kubernetes.sh`: to deploy application using kubectl
* upload_docker.sh: upload your built image to docker
