# Project Title :Inventory Monitoring at Distribution Centers

# Introduction

The project aims to build a model that can accurately classify the number of objects in a bin. This system uses the power of deep learning to track inventory and ensure delivery consignment has the correct number of items. In extensive retail facilities such as Walmart and Amazon, inventory and monitoring are very labour intensive, involve high risk, require multiple people, and are prone to error. The process will improve significantly by automation whereby a vision-based method using deep learning to count the number of items in a bin before delivery

## Project Set Up and Installation
### AWS SageMaker Setup and installation

To build this project, you wlll have to use AWS through your classroom. Below are your main steps:
- Open AWS through the classroom on the left panel (**Open AWS Gateway**)
- Open SageMaker Studio and create a folder for your project

Create and open a Sagemaker instance, I have chosen 'ml.t2.medium' instance type. This instance comes with 2vCPUs and 4GiB memory. This configuration is good enough for running the project jupyter notebook and the price is also one of the least.
Then create or load the project files required to your workspace.

#### Download the Starter Files

You can clone this Github Repo or download the project files from Github and upload starter files to your workspace.

## Dataset

### Overview
The Dataset are amazon bin images dataset available in an S3 bucket named (aft-vbi-pds) in the US-east-1 AWS region. 

### Access
The Dataset was uploaded using AWS CLI

## Model Training( train.py, hpo.py, endpoint.py)
The training script takes the hyperparameters as arguments and reads, loads and preprocesses the train, test and validation datasets. Then after creating and loading the pretrained ‘resnet34’ model it trains the model using the given parameters.

hpo1.py:  used for hyperparameter tuning job.

train1.py: used for fine tuning the model with best hyperparameters.

inference1.py: used for deploying the trained model.

## Machine Learning Pipeline

- Install necessary dependencies and import the libraries required

- Data download and preparation

- Upload the downloaded data to the required S3 bucket

- Setup the training estimator

- Submit the job

- Setup the Hyperparameter search space
    
- Setup the model debugging and profiling rules
    
- Create the model estimator for Hyperparameter tuning job

- Create the tuner for Hyperparameter tuning job
- Submit the tuning job
    
- Fetch the best training job and the hyperparameters

- Finetune the model with the best hyperparameters
    
- Deploy the model
    
- Query the model with a bin image and get prediction

