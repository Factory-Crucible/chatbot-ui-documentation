
# `k8s` Directory

The `k8s` directory is a critical part of the Factory-Crucible/chatbot-ui-documentation repository. It houses the Kubernetes configurations for the chatbot UI application. The directory contains a single file, `chatbot-ui.yaml`, which outlines the Kubernetes resources required for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. The Namespace isolates the resources of the chatbot UI, while the Secret securely stores the OpenAI API key. The Deployment details the Docker image, the number of replicas, and the container port, and retrieves the OpenAI API key from the Secret. The Service exposes the Deployment on port 80, routing traffic to the container port 3000.

## Contents

The `k8s` directory contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for the chatbot UI application. It creates a Namespace to isolate the resources of the chatbot UI, stores the OpenAI API key in a Secret, specifies the Docker image, the number of replicas, and the container port in a Deployment, and exposes the Deployment on port 80 via a Service.

## Key Components

The `k8s` directory's key component is the `chatbot-ui.yaml` file. This file is crucial as it outlines the Kubernetes resources required for the chatbot UI application. It defines a Namespace for resource isolation, a Secret for secure storage of the OpenAI API key, a Deployment for specifying the Docker image, the number of replicas, and the container port, and a Service for exposing the Deployment on port 80 and routing traffic to the container port 3000.

## Usage & Examples

The `k8s` directory is used to manage the Kubernetes configurations for the chatbot UI application. The `chatbot-ui.yaml` file within this directory is applied to a Kubernetes cluster to deploy the chatbot UI application.

For example, to deploy the chatbot UI application to a Kubernetes cluster, one would use the `kubectl apply` command with the `chatbot-ui.yaml` file:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command creates or updates the Kubernetes resources defined in the `chatbot-ui.yaml` file, effectively deploying or updating the chatbot UI application on the Kubernetes cluster.
