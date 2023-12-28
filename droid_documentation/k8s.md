
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It houses the Kubernetes configurations for the chatbot UI application. Kubernetes, a popular open-source platform, is used for automating deployment, scaling, and managing containerized applications. The configurations in this directory are essential for deploying the chatbot UI application in a Kubernetes environment.

### Contents

The `k8s` directory is straightforward and contains a single file, `chatbot-ui.yaml`. This file holds the Kubernetes configurations for the chatbot UI application. There are no subdirectories in this directory.

- `k8s/chatbot-ui.yaml`: This is a Kubernetes configuration file. It defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. These resources are used to deploy and manage the chatbot UI application in a Kubernetes environment.

### Key Components

The `k8s/chatbot-ui.yaml` file is the key component in this directory. It outlines the Kubernetes resources required to deploy and manage the chatbot UI application. Here's a brief overview of the resources defined in this file:

- Namespace: The Namespace 'chatbot-ui' is created to isolate the resources of the chatbot UI. This isolation helps in managing resources related to the chatbot UI application separately from other applications in the Kubernetes environment.

- Secret: The Secret resource stores the OpenAI API key in a secure, base64 encoded format. This key is used to interact with the OpenAI API, which is a crucial part of the chatbot UI application.

- Deployment: The Deployment resource specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This resource is responsible for deploying the chatbot UI application and managing its instances in the Kubernetes environment.

- Service: The Service resource exposes the Deployment on port 80 and routes traffic to the container port 3000. This resource is responsible for managing network traffic to and from the chatbot UI application.

### Usage & Examples

The `k8s` directory is used during the deployment phase of the chatbot UI application. The Kubernetes configurations defined in the `chatbot-ui.yaml` file are applied to a Kubernetes environment to deploy the application.

For example, to deploy the chatbot UI application to a Kubernetes environment, one would typically use the `kubectl apply` command with the `chatbot-ui.yaml` file:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the resources defined in the `chatbot-ui.yaml` file, effectively deploying or updating the chatbot UI application in the Kubernetes environment.

Please note that this is a typical usage example and the actual deployment process may vary based on the specific Kubernetes environment and deployment strategy used.
