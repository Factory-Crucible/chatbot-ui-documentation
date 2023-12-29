
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It is dedicated to the Kubernetes configurations necessary for deploying and managing the chatbot UI application in a Kubernetes environment. The directory contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. 

The Namespace, labeled 'chatbot-ui', is designed to provide a dedicated space within the Kubernetes cluster for the chatbot UI application. This isolation ensures that the resources of the chatbot UI are managed separately from other applications within the same cluster.

The Secret is a Kubernetes resource that stores sensitive data, such as the OpenAI API key, in a secure, base64 encoded format. This ensures that the key is not exposed in plain text within the Kubernetes configurations or the application code.

The Deployment resource outlines the specifications for the chatbot UI application pods. It details the Docker image to be used, the number of replicas for scaling, and the container port for network access. The Deployment also retrieves the OpenAI API key from the Secret, ensuring that the application has access to the necessary API credentials.

The Service resource is responsible for exposing the chatbot UI application to network traffic. It routes external traffic on port 80 to the container port 3000, allowing users to access the chatbot UI.

### Contents

The `k8s` directory contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for deploying and managing the chatbot UI application in a Kubernetes environment.

### Key Components

The key component in the `k8s` directory is the `chatbot-ui.yaml` file. This file is critical because it outlines the Kubernetes resources necessary for deploying and managing the chatbot UI application. It defines a Namespace for isolating the application's resources, a Secret for securely storing the OpenAI API key, a Deployment for specifying the application's specifications, and a Service for exposing the application to network traffic.

### Usage & Examples

The `k8s` directory and its `chatbot-ui.yaml` file are used during the deployment process of the chatbot UI application. When deploying the application to a Kubernetes cluster, the `kubectl apply -f chatbot-ui.yaml` command is used. This command instructs Kubernetes to create or update the resources defined in the `chatbot-ui.yaml` file.

For example, to deploy the chatbot UI application to a Kubernetes cluster, the following command would be used from the root directory of the project:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the Namespace, Secret, Deployment, and Service defined in the `chatbot-ui.yaml` file, deploying the chatbot UI application to the Kubernetes cluster.
