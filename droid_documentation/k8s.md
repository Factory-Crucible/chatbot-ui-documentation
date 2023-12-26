
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations. Kubernetes, a popular open-source platform for managing containerized workloads and services, is used in this project to orchestrate the deployment, scaling, and management of the chatbot UI application. The configurations within this directory are essential for defining the Kubernetes resources required for the chatbot UI application, including a Namespace, a Secret, a Deployment, and a Service.

### Contents

The `k8s` directory is straightforward and contains a single file, `chatbot-ui.yaml`. This file holds the Kubernetes configurations for the chatbot UI application.

- `k8s/chatbot-ui.yaml`: This is a Kubernetes configuration file that defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. These resources are integral to the functioning, security, and accessibility of the chatbot UI application.

### Key Components

The `k8s/chatbot-ui.yaml` file is the key component of this directory. It outlines the Kubernetes resources necessary for the chatbot UI application:

- Namespace: The Namespace, named 'chatbot-ui', is used to isolate the resources of the chatbot UI application. This isolation is beneficial for managing components in large projects, as it prevents conflicts between different parts of the project.
- Secret: The Secret resource is used to store the OpenAI API key in a secure, base64 encoded format. This ensures the sensitive API key is not exposed in plain text, enhancing the security of the application.
- Deployment: The Deployment resource specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This resource is responsible for the actual deployment of the chatbot UI application.
- Service: The Service resource exposes the Deployment on port 80 and routes traffic to the container port 3000. This makes the chatbot UI application accessible to users.

### Usage & Examples

The `k8s` directory is used during the deployment phase of the chatbot UI application. The Kubernetes configurations defined in the `chatbot-ui.yaml` file are applied to a Kubernetes cluster, which then creates the defined resources and manages the application.

For example, when deploying the chatbot UI application, the Kubernetes command-line tool `kubectl` is used to apply the configurations:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command instructs Kubernetes to create the resources defined in the `chatbot-ui.yaml` file. Once the resources are created, Kubernetes manages the deployment, scaling, and routing of the chatbot UI application based on the defined configurations.
