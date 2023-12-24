
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation codebase, serving as the home for Kubernetes configurations. Kubernetes, a popular open-source platform for managing containerized workloads and services, is used in this project to handle the deployment and scaling of the chatbot UI application. The configurations stored in this directory are essential for defining the Kubernetes resources required for the application, including a Namespace, a Secret, a Deployment, and a Service.

### Contents

The `k8s` directory is straightforward and contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that outlines the necessary resources for the chatbot UI application. It defines a Namespace for isolating the chatbot UI resources, a Secret for securely storing the OpenAI API key, a Deployment for detailing the Docker image, the number of replicas, and the container port, and a Service for exposing the Deployment on a specific port and routing traffic to the container port.

### Key Components

The key component in this directory is the `chatbot-ui.yaml` file. This file is the blueprint for the Kubernetes resources needed to deploy and manage the chatbot UI application. It's a critical part of the codebase as it directly influences the deployment and scaling of the application.

- Namespace: The 'chatbot-ui' Namespace is created to isolate the resources of the chatbot UI. This isolation is beneficial for managing resources in a multi-tenant cluster environment, providing a scope for names, and ensuring policies around resource quotas and service accounts.
- Secret: The Secret resource is used to store the OpenAI API key in a secure, base64 encoded format. This is a crucial security measure, ensuring that sensitive data is not exposed in the application code or Docker image.
- Deployment: The Deployment resource specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This resource is responsible for maintaining the desired state of the application, handling updates and rollbacks, and scaling the application as needed.
- Service: The Service resource exposes the Deployment on port 80 and routes traffic to the container port 3000. This resource abstracts the underlying Pods, providing a stable endpoint for the application.

### Usage & Examples

The `k8s` directory is used during the deployment process of the chatbot UI application. The Kubernetes configurations defined in the `chatbot-ui.yaml` file are applied to a Kubernetes cluster, creating the necessary resources for the application.

For example, to deploy the application to a Kubernetes cluster, one would typically use the `kubectl apply` command with the `chatbot-ui.yaml` file:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the resources defined in the `chatbot-ui.yaml` file. Once the command is executed, Kubernetes creates a Namespace, a Secret, a Deployment, and a Service based on the configurations in the file. The application is then accessible through the Service, which routes traffic to the Pods managed by the Deployment.
