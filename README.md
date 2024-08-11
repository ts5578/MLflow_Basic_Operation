# MLflow_Basic_Operation

import dagshub
dagshub.init(repo_owner='ts5578', repo_name='MLflow_Basic_Operation', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

export MLFLOW_TRACKING_URI=https://dagshub.com/ts5578/MLflow_Basic_Operation.mlflow

set MLFLOW_TRACKING_USERNAME = ts5578

set MLFLOW_TRACKING_PASSWORD = a4fdb2b615770584438afb314fa6994ea3786856

## AWS Setup

sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000/