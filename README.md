# End-to-end-Machine-Learning-Project-with-MLflow [Wine Quality Prediction]

![wine](https://github.com/ganeshmore99/End-to-end-Machine-Learning-Project-with-MLflow/assets/85934803/ab8283c2-ebba-45b1-88f8-46ad0535e2d8)


This repository contains an end-to-end machine learning project with MLflow for experiment tracking, along with other MLOps tools for a complete CI/CD pipeline deployment on AWS.

## Table of Contents
#### Introduction
#### Repository Setup
#### Project Template Creation
#### Project Setup and Requirements Installation
#### Logging, Utils, and Exceptions Modules
#### Project Workflows
#### Modular Code Implementation
#### Training Pipeline
#### MLOps Tools Implementation
#### Prediction Pipeline and User App Creation
#### Docker
#### GitHub Actions
#### Final CI/CD Deployment on AWS Cloud

## Introduction
This project demonstrates an end-to-end machine learning pipeline from data preprocessing to deployment. It incorporates various MLOps tools and practices to ensure robust, scalable, and maintainable machine learning workflows.

## Repository Setup
Clone this repository to your local machine using the following command:

git clone https://github.com/ganeshmore99/End-to-End-ML-Project-with-MLflow.git


## Project Template Creation
A project template is set up to ensure a structured and organized codebase. The template includes directories for data, scripts, notebooks, models, and logs.

## Project Setup and Requirements Installation
Install the required packages using pip:

pip install -r requirements.txt
Ensure all dependencies are met for smooth execution of the project.

## Logging, Utils, and Exceptions Modules
Modules for logging, utility functions, and custom exceptions are created to handle various aspects of the project:

Logging: For tracking the execution flow and debugging.
Utils: Contains helper functions used throughout the project.
Exceptions: Custom exceptions for better error handling.
Project Workflows
Define the workflows for the project, including data ingestion, preprocessing, model training, evaluation, and deployment. Each workflow is modular and reusable.

##  Modular Code Implementation
Implement all components of the project in a modular fashion. This includes data preprocessing, feature engineering, model training, and evaluation.

## Training Pipeline
Set up the training pipeline, which includes data loading, preprocessing, model training, and evaluation. The pipeline ensures that all steps are executed sequentially and reproducibly.

## MLOps Tools Implementation
Incorporate MLOps tools such as MLflow for experiment tracking and model management. This ensures that all experiments are logged, and models can be easily tracked and retrieved.

## Prediction Pipeline and User App Creation
Develop a prediction pipeline to generate predictions from the trained model. Additionally, create a user application (e.g., a web app) to allow users to interact with the model and get predictions.

## Docker
Create Docker containers for the project to ensure consistency across different environments. This includes Dockerfiles for the training and prediction pipelines.

## GitHub Actions
Set up GitHub Actions for CI/CD to automate testing, building, and deployment processes. This ensures that any changes to the codebase are automatically tested and deployed.

## Final CI/CD Deployment on AWS Cloud
Deploy the final project on AWS Cloud using CI/CD pipelines. This includes setting up the necessary infrastructure on AWS and using GitHub Actions for automated deployment.


## Workflows

1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the app.py



# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/ganeshmore99/End-to-end-Machine-Learning-Project-with-MLflow.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n mlproj python=3.8 -y
```

```bash
conda activate mlproj
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```



## MLflow

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/ganeshmore5199/End-to-end-Machine-Learning-Project-with-MLflow.mlflow \
MLFLOW_TRACKING_USERNAME=ganeshmore5199 \
MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0 \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/ganeshmore5199/End-to-end-Machine-Learning-Project-with-MLflow.mlflow

export MLFLOW_TRACKING_USERNAME=ganeshmore519 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.ap-south-1.amazonaws.com/mlproj

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app




## About MLflow 
MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & tagging your model

## Contributing
Contributions are welcome! Please read the contributing guidelines before submitting a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
Thanks to the developers of the tools and libraries used in this project.

