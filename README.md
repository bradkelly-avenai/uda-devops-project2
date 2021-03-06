# Overview

This project is an example of building a CI/CD pipeline using GitHub, Azure Pipelines and Azure App service. The project uses a Github repository which contains scaffolding that will assist you in performing both Continuous Integration and Continuous Delivery. The project also enables linting, testing and installation byg using a Makefile, a requirements.txt and application code.

The project uses a pre-developed python machine learning application which leverages the python web framework Flask. 

## Project Plan


* [Trello Board](https://trello.com/b/vtFOlsZ3/udacity-project-2)
* [Excel Project Plan](src/devop-project2-management.xlsx)

## Instructions
### Architecture Plan
![Architecture Plan](src/architecture.jpeg?raw=true "Architecture Plan")

### Instructions
Step 1: Launch Cloud Shell

![Azure Portal](src/step1_azure_portal.jpeg?raw=true "Azure Portal")

![Azure Cloud Shell](src/step1_azure_cloud_shell.jpeg?raw=true "Azure Cloud Shell")

Step 2: Clone Repo

![Azure Clone Repo](src/step2_azure_clone.jpeg?raw=true "Azure Clone Repo")

Step 3

Make a new repository for this exercise and commit the downloaded files. Make sure you enable Azure Pipelines either now, or when you later integrate Azure Pipelines. You can see what this looks like in the screenshot below. If you need help you can refer to the official steps from Microsoft.

[Microsoft Documenation](https://docs.microsoft.com/en-us/azure/devops/pipelines/repos/github?view=azure-devops&tabs=yaml)

![Integrate Azure Pipeline](src/step3_github_enable_az_pipe.jpeg?raw=true "Integrate Azure Pipeline")


Step 4: Create Flask ML Service

run the following commands to configure a python virtual environment. udacity-ml-azure can be replaced with a name of your choice

    python3 -m venv ~/.udacity-ml-azure
    source ~/.udacity-ml-azure/bin/activate
    
![Python Virtual Environment](src/step4_python_virt.jpeg?raw=true "Python Virtual Environment")

Run 'make install'

    make install

![Make Install](src/step4_make_install.jpeg?raw=true "Make Install")

Create an app service and initially deploy your app by running the following command

    az webapp up -n <replace-with-your-app-name>


Step 5:

Change the line in make_predict_azure_app.sh to match the deployed prediction:

    -X POST https://<replace-with-your-app-name>.azurewebsites.net:$PORT/predict

![Make Prediction](src/step_5_make_prediction.jpeg?raw=true "Make Prediction")




Review Output of streamed log files from deployed application

    az webapp log tail --name <replace-with-your-app-name> --resource-group <replace-with-your-resource-group-name>

![Log Files](src/streaming_web_logs.jpeg?raw=true "Log Files")


## Configure Azure
![Step1_Azure](src/azure-step1-devops-dashboard.png?raw=true "Step1_Azure")
## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


