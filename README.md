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


Step 4: Setup a python virtual environment

run the following commands to configure a python virtual environment. udacity-ml-azure can be replaced with a name of your choice

'python3 -m venv ~/.udacity-ml-azure'
'source ~/.udacity-ml-azure/bin/activate'


![Python Virtual Environment](src/step4_python_virt.jpeg?raw=true "Python Virtual Environment")

Step 5
* Project running on Azure App Service



* Passing tests that are displayed after running the `make all` command from the `Makefile`

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


