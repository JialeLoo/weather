
# Thedatafoundry_weatherAPI

* The project is done in AWS Cloud9, t3.small has been selected for the EC2 enviroment.
  
To manually create a virtualenv on MacOS and Linux:
```
$ python3 -m venv .venv
```

After the init process completes and the virtualenv is created, you can use the following
step to activate your virtualenv.
```
$ source .venv/bin/activate
```

Once the virtualenv is activated, you can install the required dependencies.
```
$ pip install -r requirements.txt
```

For external library to be used in lambda, go to the requirements.txt under the folder 'lambda' to add the library package name

# GitHub repo

weather/weather_stack.py is the file that contains the AWS resources.
It contains resources: S3, EventBridge, Lambda function

lambda/lambda_handler.py is the file for lambda function. 
It will perform the API requesting and ETL process and store the result in S3 bucket.

# S3 bucket

2 directories will be generated.
Raw_weather/: This directory contains raw json data of the weather information.
Melbourne_weather/: This directory contains wrangled json data (processed ETL) for further use.

# Feel free to add on your idea to the project!
Run the command line whenever you want to deploy your changes. This will modify the resources in your AWS account.
```
$ cdk deploy
```
