

# Dockerized Development Environment

This project was created to develop Docker images that provides a pre-installed development environment for students to use during coding workshops.  It includes all the necessary tools and dependencies for students to be able to develop and run code on their own machines without any additional setup required.

## Prerequisites

Before you can use this Docker image, you will need to have those programs:

1. Docker Desktop: [Docker website](https://www.docker.com/get-started)
2. Vscode: [Visual Studio](https://code.visualstudio.com/)
3. Vscode plugin: [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

## Getting Started

To get started using this Docker image, follow these steps:

1. Clone this repository to your local machine.
2. Open a terminal window and navigate to the directory where you cloned the repository.
3. find the right image to your workshop
4. Run the following command to build the Docker image:

   ```
   docker build -t workshop-name -f Dockerfile .
   ```

4. Once the Docker image has finished building, run the following command to start a container:

   ```
   docker run -it workshop-name
   ```

   This will start a container with the Docker image

5. Open Vscode and select the Remote Development plugin then right click on the docker image that was created and click "attach to container"

6. This will open a new vscode window, after connect with success click on open folder

7. navigate to this folder: /usr/workshop/


## Troubleshooting

If you run into any issues while using this Docker image, please check the following:

- Make sure Docker is installed and running correctly on your machine.
- Make sure you are using the correct Docker commands to build and run the image.
- Make sure you have permissions to access the directory where you cloned the repository.
- Make sure the ports used by the Docker image are not already in use by other applications on your machine.

## Credits

I want to give some credits to my friend [Rodrigo Sasaki](https://github.com/rodrigopsasaki) that helped me to create the first Docker image to this project.
