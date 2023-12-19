
# k8s Directory Documentation

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations that orchestrate the deployment and operation of the chatbot UI application. The directory contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service, each playing a unique role in the application's Kubernetes environment.

## Contents

The `k8s` directory is straightforward in its structure, containing a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for the chatbot UI application. It outlines a Namespace for isolating the application's resources, a Secret for securely storing the OpenAI API key, a Deployment for specifying the Docker image, the number of replicas, and the container port, and a Service for exposing the Deployment and routing traffic.

## Key Components

The `k8s` directory's primary component is the `chatbot-ui.yaml` file. This file is the blueprint for the Kubernetes environment in which the chatbot UI application operates. It defines four key Kubernetes resources:

- **Namespace**: The Namespace, named 'chatbot-ui', isolates the resources of the chatbot UI application, providing a scope for names and ensuring that the application does not interfere with other resources in the Kubernetes cluster.

- **Secret**: The Secret stores the OpenAI API key, which is necessary for the chatbot UI application to interact with the OpenAI API. The key is stored in a base64 encoded format, ensuring its security.

- **Deployment**: The Deployment specifies the Docker image to be used for the application, the number of replicas for scaling the application, and the container port for the application to listen on. It also retrieves the OpenAI API key from the Secret, making it available to the application.

- **Service**: The Service exposes the Deployment on port 80, allowing external traffic to reach the application. It routes this traffic to the container port 3000, where the application is listening.

## Usage & Examples

The `k8s` directory and its `chatbot-ui.yaml` file are used to deploy and manage the chatbot UI application in a Kubernetes environment. The file is applied to a Kubernetes cluster using the `kubectl apply` command, which creates or updates the resources defined in the file.

For example, to deploy the chatbot UI application, a developer or DevOps engineer would navigate to the directory containing the `chatbot-ui.yaml` file and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the Namespace, Secret, Deployment, and Service defined in the `chatbot-ui.yaml` file, setting up the environment for the chatbot UI application.

The `k8s` directory and its `chatbot-ui.yaml` file are integral to the deployment and operation of the chatbot UI application, providing the necessary Kubernetes configurations for the application's Kubernetes environment.
