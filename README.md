# MLflow exaple
This repository demonstrate simple logging of mlflow of a basic model

![image](https://github.com/saikat-kolkata/mlflow1/assets/14269309/49da81b6-a81e-462a-8975-9c3a0d9956f9)

![image](https://github.com/saikat-kolkata/mlflow1/assets/14269309/1a8402ec-5f57-466a-95ec-1211e5cdff0b)

# MLflow on AWS
MLflow on AWS Setup:
Login to AWS console.
Create IAM user with AdministratorAccess
Export the credentials in your AWS CLI by running "aws configure"
Create a s3 bucket
Create EC2 machine (Ubuntu) & add Security groups 5000 port

## Run the following command on EC2 machine

```sudo apt update

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
