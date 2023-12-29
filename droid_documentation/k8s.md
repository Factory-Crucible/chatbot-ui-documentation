
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation codebase, serving as the home for Kubernetes configurations. Kubernetes, a popular open-source platform for managing containerized workloads and services, is used in this project to orchestrate the deployment, scaling, and management of the chatbot UI application. The configurations within this directory are specifically tailored for the chatbot UI application, defining the necessary resources and settings for its deployment on a Kubernetes cluster.

### Contents

The `k8s` directory is straightforward and contains a single file, `chatbot-ui.yaml`. This file is a Kubernetes configuration file that outlines the necessary resources for the chatbot UI application.

- `k8s/chatbot-ui.yaml`: This file defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. These resources are essential for the deployment and operation of the chatbot UI application in a Kubernetes environment.

### Key Components

The `chatbot-ui.yaml` file is the key component in this directory. It is a Kubernetes configuration file that outlines the necessary resources for deploying the chatbot UI application. Here's a brief overview of the resources defined in this file:

- Namespace: The Namespace, named 'chatbot-ui', is used to isolate the resources of the chatbot UI application. This isolation is beneficial for managing resources in a multi-tenant environment and providing a scope for names.
- Secret: The Secret resource is used to store sensitive data, in this case, the OpenAI API key. It stores this key in a secure, base64 encoded format, protecting it from exposure.
- Deployment: The Deployment resource describes the desired state for the chatbot UI application. It specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret resource.
- Service: The Service resource is used to expose the Deployment on port 80. It routes traffic to the container port 3000, allowing the chatbot UI application to be accessed.

### Usage & Examples

The `k8s` directory and its contents are used during the deployment process of the chatbot UI application. When deploying the application to a Kubernetes cluster, the `chatbot-ui.yaml` file is applied using the `kubectl apply` command. This command creates or updates the resources defined in the file on the Kubernetes cluster.

For example, to deploy the chatbot UI application, one would navigate to the directory containing the `chatbot-ui.yaml` file and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the Namespace, Secret, Deployment, and Service as defined in the `chatbot-ui.yaml` file. Once the command is executed, the chatbot UI application is deployed and accessible on the specified port.
