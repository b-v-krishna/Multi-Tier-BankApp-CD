# Multi-Tier-BankApp-CD

This repository is used for the **Continuous Deployment (CD)** pipeline for the Multi-Tier Bank Application.

It is used to update the Kubernetes deployment YAML file with the latest Docker image tag and push the updated manifest to the GitHub repo.

## Jenkins CD Stage

The Jenkins pipeline performs the following actions in the **CD stage**:

1. **Clone this repository** into the Jenkins workspace.
2. **Update the image tag** in the `bankapp-ds.yml` file using `sed`.
3. **Confirm the update** by printing the modified YAML.
4. **Configure Git** with user credentials.
5. **Commit and push** the changes back to the `main` branch of this repository.

   
##  bankapp-ds.yml

This file contains the Kubernetes Deployment for the `bankapp` service.

Jenkins dynamically updates the Docker image tag in the following line during CD


# 🛠️ Prerequisites
Ensure your Jenkins instance has the following:

Git credentials (git-cred) configured.

Access to this repository.

Pipeline configured with DOCKER_TAG as a parameter.

Docker image built and pushed with the given DOCKER_TAG.

📃 License
This project is licensed under the MIT License

