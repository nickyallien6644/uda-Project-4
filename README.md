[CircleCI URL]https://app.circleci.com/pipelines/github/nickyallien6644/uda-Project-4

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are provided a pre-trained, pre-'sklearn' model that has been taught to forecast housing costs in Boston based on a number of parameters, including the average number of rooms in a home and information on highway accessibility, teacher-to-student ratios, and other factors. You may read more about the data on [the data source site] (https://www.kaggle.com/c/boston-housing), which was where the original Kaggle data came from. This project examines your ability to operationalize a Python flask app that uses API calls to deliver out predictions (inference) about house prices in a file called "app.py" that is provided. Any pre-trained machine learning model, such as those for image recognition and data labeling, might be included in this project.

### Project Tasks

Your project's objective is to operationalize this functional machine learning microservice utilizing [kubernetes], an open-source solution for automating the administration of containerized applications (https://kubernetes.io/). You will perform the following tasks as part of this project: 
* Test your project code using linting 
* Create a Dockerfile to containerize this application 
* Deploy your containerized application using Docker and make a prediction 
* Enhance the logging in the source code for this application 
* Configure Kubernetes and create a Kubernetes cluster 
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repository with CircleCI to show

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtual env with Python and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python -m pip install --user virtualenv
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
