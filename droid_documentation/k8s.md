
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations. Kubernetes, a popular open-source platform for managing containerized workloads and services, is used in this project to orchestrate the deployment, scaling, and management of the chatbot UI application. The configurations within this directory are specifically tailored for the chatbot UI application, defining the necessary resources and settings for its deployment on a Kubernetes cluster.

### Contents

The `k8s` directory is straightforward and contains a single file, `chatbot-ui.yaml`. This file is a Kubernetes configuration file that outlines the necessary resources for deploying the chatbot UI application. 

- `k8s/chatbot-ui.yaml`: This file defines four Kubernetes resources - a Namespace, a Secret, a Deployment, and a Service. The Namespace 'chatbot-ui' is created to isolate the resources of the chatbot UI. The Secret stores the OpenAI API key in a base64 encoded format, providing a secure way to handle sensitive data. The Deployment specifies the Docker image to be used, the number of replicas, and the container port, while also retrieving the OpenAI API key from the Secret. The Service exposes the Deployment on port 80 and routes traffic to the container port 3000.

### Key Components

The `k8s/chatbot-ui.yaml` file is the key component of this directory. It is a comprehensive Kubernetes configuration file that encapsulates the deployment strategy for the chatbot UI application. 

- Namespace: The 'chatbot-ui' Namespace is created to provide a scope for the resources of the chatbot UI, ensuring isolation and management ease.
- Secret: The Secret resource is used to store the OpenAI API key in a secure, base64 encoded format, protecting sensitive data.
- Deployment: The Deployment resource details the Docker image, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret, ensuring the application has access to the necessary API key.
- Service: The Service resource exposes the Deployment on port 80, routing traffic to the container port 3000. This ensures the application is accessible to users.

### Usage & Examples

The `k8s` directory is used during the deployment phase of the chatbot UI application. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster, which creates the defined resources and sets up the application for use.

For example, to deploy the chatbot UI application to a Kubernetes cluster, one would use the `kubectl apply` command with the `chatbot-ui.yaml` file:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command instructs Kubernetes to create the resources defined in the `chatbot-ui.yaml` file, setting up the chatbot UI application as per the configurations. Note that this is a simplified example and actual deployment may require additional steps or configurations based on the specific Kubernetes environment.
