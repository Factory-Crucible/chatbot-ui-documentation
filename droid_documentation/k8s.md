
# k8s Directory Documentation

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It houses the Kubernetes configurations that are essential for deploying the chatbot UI application in a containerized environment. The directory contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. The Namespace isolates the chatbot UI resources, the Secret securely stores the OpenAI API key, the Deployment details the Docker image and its specifications, and the Service exposes the Deployment to the network.

## Contents

The `k8s` directory is straightforward and contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for deploying the chatbot UI application. It outlines a Namespace for isolating the chatbot UI resources, a Secret for securely storing the OpenAI API key, a Deployment for specifying the Docker image and its specifications, and a Service for exposing the Deployment to the network.

## Key Components

The `k8s` directory's key component is the `chatbot-ui.yaml` file. This file is the backbone of the Kubernetes deployment process for the chatbot UI application. It defines the following Kubernetes resources:

- **Namespace 'chatbot-ui'**: This Namespace isolates the resources of the chatbot UI, ensuring that they do not interfere with other resources in the Kubernetes cluster.
- **Secret**: This Kubernetes resource securely stores the OpenAI API key in a base64 encoded format. This ensures that the key is not exposed in plain text, enhancing the security of the application.
- **Deployment**: The Deployment specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This resource is responsible for managing the state of the application and ensuring that the desired number of instances are running at any given time.
- **Service**: The Service exposes the Deployment on port 80 and routes traffic to the container port 3000. This allows the chatbot UI application to be accessible over the network.

## Usage & Examples

The `k8s` directory is used during the deployment process of the chatbot UI application. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster, which creates the defined resources and deploys the application.

For example, to deploy the chatbot UI application, one would navigate to the `k8s` directory and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create the resources defined in the `chatbot-ui.yaml` file. Once the command is executed, Kubernetes creates the Namespace, Secret, Deployment, and Service, and the chatbot UI application is deployed and accessible over the network.

Please note that the above command assumes that you have `kubectl` installed and configured to interact with your Kubernetes cluster. Also, the OpenAI API key should be base64 encoded and replaced in the Secret resource in the `chatbot-ui.yaml` file before running the command.
