# Ansible Playbook for Deploying Code on Docker

This Ansible playbook can be used to deploy code on a Docker container. Follow the steps below to use this playbook.
### Prerequisites

1. Ansible installed on the deployment machine
2. A host with Docker installed and running
3. A Docker image to deploy
4. A container name and port to publish

## Instructions

1. Clone this repository to your deployment machine.
2. Open the deploy.yml file in a text editor.
3. Edit the hosts field to specify the target host for deployment.
4. Edit the vars section to specify the name and tag of the Docker image, as well as the container name and port.
5. Save the deploy.yml file.
6. Run the playbook using the command ansible-playbook deploy.yml.

The playbook will perform the following steps:

1. Ensure that Docker is installed on the target host.
2. Add Docker's official GPG key.
3. Add Docker's APT repository to the package manager.
4. Install Docker.
5. Pull the specified Docker image.
6. Start a Docker container with the specified name and port.

You should now be able to access your deployed code at http://<target_host>:<container_port>.
