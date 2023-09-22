#### CircleCI status badge:

[![CircleCI](https://dl.circleci.com/status-badge/img/gh/nickyallien6644/uda-Project-4/tree/master.svg?style=svg&circle-token=45eb86d8d25f505edc3f4c857c0c57efeb8c5c6c)](https://dl.circleci.com/status-badge/redirect/gh/nickyallien6644/uda-Project-4/tree/master)

## Project Overview

In this project, I will apply the skills I have acquired in this course to operationalize a Machine Learning Microservice API. 

It provided a pre-trained, pre-'sklearn' model that has been taught to forecast housing costs in Boston based on a number of parameters, including the average number of rooms in a home and information on highway accessibility, teacher-to-student ratios, and other factors. I may read more about the data on [the data source site] (https://www.kaggle.com/c/boston-housing), which was where the original Kaggle data came from. This project examines my ability to operationalize a Python flask app that uses API calls to deliver out predictions (inference) about house prices in a file called "app.py" that is provided. Any pre-trained machine learning model, such as those for image recognition and data labeling, might be included in this project.

### Project Tasks

my project's objective is to operationalize this functional machine learning microservice utilizing [kubernetes], an open-source solution for automating the administration of containerized applications (https://kubernetes.io/). I will perform the following tasks as part of this project: 
* Test my project code using linting 
* Create a Dockerfile to containerize this application 
* Deploy my containerized application using Docker and make a prediction 
* Enhance the logging in the source code for this application 
* Configure Kubernetes and create a Kubernetes cluster 
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repository with CircleCI to show

**The final implementation of the project will showcase my abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv and activate virtualenv
* Run `python -m venv ~/.devops` to install virtualenv ~/.devops
* Run `source ~/.devops/bin/activate` to active virtualenv
* Run `make install` to install the necessary dependencies
* Run `make lint`  (pylint app.py files and hadolint Dockerfile) to detect errors in the code.  

### Running `app.py`

1. Standalone: `python app.py`
2. Run in Docker: `./run_docker.sh`
3. Run in Kubernetes: `./run_kubernetes.sh`

### Kubernetes Steps

1. Setup and Configure Docker locally
    * install docker as described in the [link](https://docs.docker.com/engine/install/ubuntu/).
    * Run `./run_docker.sh`
    * Run `docker ps` to check if docker is running.
    * Run `./make_prediction.sh` to make prediction and copy/paste the logging info at terminal to `output_txt_files/docker_out.txt`
2. Setup and Configure Kubernetes locally
    * Run `curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64`
    * Run `sudo install minikube-linux-amd64 /usr/local/bin/minikube`
    * Run `minikube start` to start minikube
    * Run `kubectl get pods` to see which pods are running.
    * Run `./run_kubernetes.sh`
    * Run `./make_prediction.sh` to make prediction and copy/paste the logging info at terminal to `output_txt_files/kubernetes_out.txt`
3. Create Flask app in Container
    * Run `./run_docker.sh` to build and start the Flask app container. 
    * Run `./upload_docker.sh` to upload the container to docker hub.
* Run via kubectl
