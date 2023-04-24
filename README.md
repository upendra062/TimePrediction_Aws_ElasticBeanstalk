# End To End Machine Learning Project

# Create a environment

```
conda create -p venv python==3.8
```

# Install all necessary libraries
```
pip install -r requirements.txt
```



# Deployment WebApplication
```
Aws Elastic Bean Stack
```

# DATABASE
```
MongoDB
```    
# Project LifeCycle
# Process of Machine Learning Project
```
    [DATA CLEANING] 
        { 
            I/P :RAW DATA, 
            O/P : CLEAN DATA,
        }   
    [DATA INJESTION]
        {
            I/P: CLEAN DATA,
            O/P: TRAIN AND TEST DATA 
            TRAIN TEST SPLIT
            We get train and test data
        }
    [DATA TRANSFORMATION]
        {
            WHAT WE DO HERE
            WE DO FEATURE ENGINEERING
            I/P: TRAIN AND TEST DATA
            O/P: TRAIN AND TEST DATA
        }
    [MODEL TRAINING]
        {
            I/O: TRAIN AND TEST DATA
            O/P: PICKLE FILE
        }
    [MODEL EVALUATION]
        {
            I/O: PICKLE FILE
            O/P: ACCURACY
        }
    [DEPLOYMENT]
```
# Steps
```
1. EDA
2. Feature Engineering
3. Model Training
4. Model Evaluation
4. Web Application Deployment
```

# Components
```
1. Data Cleaning 
``` 
```
2. Data Ingestion 
``` 
```
3. Data Transformation 
```
```
4. Model Training 
```
```
5. Model Evaluation 
```
```
6. Deployment
```


# TRAINING PIPELINE

```
DATA CLEANING
```
```
DATA INJESTION
```
```
DATA TRANSFORMATION
```
```
CLUSTERING (grouping the data)
```
```
MODEL TRAINING FOR EACH GROUP DATA
```
```
MODEL EVALUTION
```
```
HYPERPARAMTER TUNNING
```
```
FINDING BEST MODEL
```
```
SAVING BEST MODEL
```


# PREDICTION PIPELINE
--------------------

```
DATA TRANSFORMATION
 (because for the feature engineering we will also do for new data)
```
```
FEATURE ENGINEERING
```
```
PREDICTION
    I/O: DATA
        DATA PASSING THROUGH THE MODEL
    O/P: PREDICTION
```


# Runn Docker
```
docker build -t timeprediction:latest .
```
### To Run Docker Image
```
docker run -p 5000:5000 timeprediction
```
```
docker run -p 8888:5000 timeprediction
```
### Port In which Docker Image is Running
```
http://127.0.0.1:5000/
```
```
http://127.0.0.1:8888/
```

# DeployMent Step


##  AWS Elastic Beanstalk

```
mkdir .ebextensions
```
```
touch .ebextensions/python.config
```
## Add Following Code In python.config
```
option_settings:
"aws:elasticbeanstalk:container:python":
    WSGIPath: application:application
```
## Rename app.py to application.py where your program will starts
```
application.py
```
## Object Reference Also Named as application
```
application = Flask(__name__)
```
```
mkdir .elasticbeanstalk
```
```
touch .elasticbeanstalk/config.yml
```
```
branch-defaults:
  main:
    environment: null
global:
  application_name: reviewflask
  branch: main
  default_ec2_keyname: null
  default_platform: Python 3.7
  default_region: us-east-1
  include_git_submodules: true
  instance_profile: null
  platform_name: null
  platform_version: null
  profile: eb-cli
  repository: origin
  sc: git
  workspace_type: Application
```
## Elastic Beanstalk
```
Create Application
```
```
```
```
```
```
```
```
```
```
```
```
```
```
```
```
```
```
```
```
```




















































