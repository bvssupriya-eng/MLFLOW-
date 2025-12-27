## MLflow

##### cmd
- mlflow ui

### For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/bvssupriya-eng/MLFLOW-.mlflow
MLFLOW_TRACKING_USERNAME=bvssupriya-eng
MLFLOW_TRACKING_PASSWORD=c63dbbbe329b52fa245148c0f09781bbb08f4559
 

Run this to set env variables:

**For Windows Command Prompt:**
```cmd
set MLFLOW_TRACKING_URI=https://dagshub.com/bvssupriya-eng/MLFLOW-.mlflow
set MLFLOW_TRACKING_USERNAME=bvssupriya-eng
set MLFLOW_TRACKING_PASSWORD=c63dbbbe329b52fa245148c0f09781bbb08f4559
```

**For PowerShell:**
```powershell
$env:MLFLOW_TRACKING_URI="https://dagshub.com/bvssupriya-eng/MLFLOW-.mlflow"
$env:MLFLOW_TRACKING_USERNAME="bvssupriya-eng"
$env:MLFLOW_TRACKING_PASSWORD="c63dbbbe329b52fa245148c0f09781bbb08f4559"
```
### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


## About MLflow & DVC

MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & taging your model


DVC 

 - Its very lite weight for POC only
 - lite weight expriements tracker
 - It can perform Orchestration (Creating Pipelines)



# MLFLOW ON AWS

## MLflow on AWS Setup:
    1. Login to AWS Console.
    2. Create IAM User with AdminsintratorAccess
    3. Export the credentials in your AWS CLI by running "aws configure"
    4. Create a s3 bucket.
    5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

    Run the following command on EC2 machine
    ```bash

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
	
    ##Then ask aws credentials
    aws configure

    #Finally
    mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23
	
 

    export 