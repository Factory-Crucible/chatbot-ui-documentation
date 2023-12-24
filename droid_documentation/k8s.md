
# `k8s` Directory Documentation

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It contains the Kubernetes configurations necessary for deploying and managing the chatbot UI application in a Kubernetes environment. The directory is named `k8s` as a shorthand for Kubernetes, following a common naming convention in the industry.

## Folder Purpose

The `k8s` directory's primary purpose is to provide the necessary Kubernetes configurations for the chatbot UI application. These configurations define the resources required to deploy and manage the application in a Kubernetes environment. The directory is essential for the deployment process, as it contains the definitions for the Namespace, Secret, Deployment, and Service resources used by the application.

The Namespace resource isolates the chatbot UI application's resources, ensuring that they do not interfere with other applications running in the same Kubernetes cluster. The Secret resource securely stores the OpenAI API key, which is used by the application to interact with the OpenAI API. The Deployment resource defines the Docker image to be used, the number of replicas, and the container port, and retrieves the OpenAI API key from the Secret. The Service resource exposes the Deployment on port 80, routing traffic to the container port 3000.

## Contents

The `k8s` directory contains a single file, `chatbot-ui.yaml`. This file is a Kubernetes configuration file that defines the Namespace, Secret, Deployment, and Service resources for the chatbot UI application.

### `chatbot-ui.yaml`

The `chatbot-ui.yaml` file is a Kubernetes configuration file that defines the resources necessary for deploying and managing the chatbot UI application in a Kubernetes environment. It defines a Namespace to isolate the application's resources, a Secret to securely store the OpenAI API key, a Deployment to specify the Docker image, the number of replicas, and the container port, and a Service to expose the Deployment on port 80 and route traffic to the container port 3000.

## Key Components

The key component in the `k8s` directory is the `chatbot-ui.yaml` file. This file is critical because it defines the Kubernetes resources necessary for deploying and managing the chatbot UI application. Without this file, the application could not be deployed in a Kubernetes environment.

The `chatbot-ui.yaml` file defines four resources:

- Namespace: The Namespace 'chatbot-ui' isolates the resources of the chatbot UI application, ensuring that they do not interfere with other applications running in the same Kubernetes cluster.

- Secret: The Secret stores the OpenAI API key in a secure, base64 encoded format. This key is used by the application to interact with the OpenAI API.

- Deployment: The Deployment specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret.

- Service: The Service exposes the Deployment on port 80 and routes traffic to the container port 3000. This allows the application to be accessed over the network.

## Usage & Examples

The `k8s` directory is used during the deployment process. When deploying the chatbot UI application in a Kubernetes environment, the `kubectl apply -f chatbot-ui.yaml` command is run in the `k8s` directory. This command applies the configurations defined in the `chatbot-ui.yaml` file, creating the Namespace, Secret, Deployment, and Service resources in the Kubernetes cluster.

For example, to deploy the chatbot UI application, a developer or DevOps engineer would navigate to the `k8s` directory and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command creates the Namespace, Secret, Deployment, and Service resources defined in the `chatbot-ui.yaml` file, deploying the chatbot UI application in the Kubernetes cluster.
