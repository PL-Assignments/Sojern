## Kubernetes Deployment

- Write a Kubernetes deployment manifest that has each of the following elements:
    - a config map with a simple key value pair that sets ENV to PROD
    - a deployment that consists of the following
    - 3 replicas at launch
    - an nginx pod that listens on port 80
    - an environment variable that reads the configmap value
    - a service that listens on port 80 and balances to all replicas of the above deployment
    - a horizontal autoscaler that will scale up if CPU usage is above 50%

- Its safe to assume that the nginx pod knows what to do with the environment variable already

- Your manifest should be able to pass a yaml linter

## Jenkins Pipeline

- Write a Jenkins pipeline that has one parameter which is: `"RUNNING_ENVIRONMENT"` and it is drop-down list of `"Development"`, `"Staging"` and `"Live"`.

    - According to that parameter, Jenkins will provide us another parameter to choose which is `"PROJECT"` as follows:
        - If `RUNNING_ENVIRONMENT` is `Development` then `PROJECT` needs to be a drop-down list of `"language1"`, `"language2"`
        - If `RUNNING_ENVIRONMENT` is `Staging` then `PROJECT` needs to be a drop-down list of `"languageA"`, `"languageB"`, `"languageC"`
        - If `RUNNING_ENVIRONMENT` is `Live` then `PROJECT` needs to be a drop-down list of `"languageP1"`, `"languageP2"`, `"languageP3"`

    - Then after choosing RUNNING_ENVIRONMENT and corresponding PROJECT, Jenkins will print them on screen as below:

        - Your selected `RUNNING_ENVIRONMENT` was : `Chosen Environment`
        - Your selected `Project` was: `Chosen Project`
  
  - In addition to the above output, if the selected Environment is `Live` and Selected PROJECT is `languageP3`, it will:
  
    ```$ echo "You need to get your manager's confirmation"```

- HINT: USE ACTIVE CHOICE IN YOUR PIPELINE.