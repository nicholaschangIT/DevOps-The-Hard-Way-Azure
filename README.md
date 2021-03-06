[![CI](https://github.com/nicholaschangIT/DevOps-The-Hard-Way-Azure/actions/workflows/main.yml/badge.svg)](https://github.com/nicholaschangIT/DevOps-The-Hard-Way-Azure/actions/workflows/main.yml)

# DevOps-The-Hard-Way-Azure LAB 

In this lab I will be setting up a real world environemnt using Devops technologies and practices for deploying application in Microsoft Azure. 

The solution is to deploy the Uber API for the sign-up page. Currently this solution is sitting on a bunch of baremetal, but it's time to sprinkle a little DevOps on it.

![](images/uber.png) Thank you thomast1906 for creating this amazing guide :) 

Technologies consists: Azure, GitHub, Python, Terraform, Docker , Kubernetes, CI/CD and Automated Testing 

I did this by doing the following 

Prerequisites- Azure Account, Azure Cli, Terraform, Docker Desktop  and GitHub (store the source code)

1) Start Studio code and create a project called Devops-The-Hard-Way-Azure and initialize the folder by running git init command and publish the project to Github Repo. You also need to download the Github Extension in VBS before you publish it.  

2) Run the create-terraform-storage.sh in the azure folder to Create Storage Account and Resource Group for Terraform State file. I did this by running the script in bash cloud shell in visual studio code.

3) Create Azure AD Group  and AZ login details for AKS Admins by running the create azure-ad-group.sh in th azure folder which will create the cluster 

4) Terraform - Create all of the Azure cloud services you'll need for the Uber app 

  - [Set up terraform](https://github.com/nicholaschangIT/DevOps-The-Hard-Way-Azure/blob/main/Terraform-AZURE-Services-Creation/Readme.md)


5) Docker - create a Docker image from the app, containerise it, and store the container inside of a container repository

  - [Deploy Docker inside container](https://github.com/nicholaschangIT/DevOps-The-Hard-Way-Azure/blob/main/Docker/Readme.md)


6) Kubernetes - This section will connect to AKS locally and to write the Kubernetes manifest to deploy the Python Uber app

  - [Set up Kubernetes](https://github.com/nicholaschangIT/DevOps-The-Hard-Way-Azure/blob/main/Kubernetes/Readme.md)

7) Automated Test- This automated test ensures all the terraform code is performing as it should be from a policy, security, and static code analysis point of view. 

  - [Install And Run Checkov](https://github.com/nicholaschangIT/DevOps-The-Hard-Way-Azure/blob/main/Terraform-Static-Code-Analysis/Readme.md)

8) Run CI/CD - This section will create an Ci/CD using Github action 

  - [CI/CD using Github Actions](https://github.com/nicholaschangIT/DevOps-The-Hard-Way-Azure/blob/main/Terraform-AZURE-Services-Creation/Run-CI-CD-Readme.md)
