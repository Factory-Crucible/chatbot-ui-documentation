
# `k8s` Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It houses the Kubernetes configurations for the chatbot UI application. Kubernetes, a popular open-source platform, is used for automating deployment, scaling, and management of containerized applications. In the context of this project, Kubernetes is used to manage the deployment of the Docker-based Node.js project named 'chatbot-ui'. 

The `k8s` directory contains a single file, `chatbot-ui.yaml`, which defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. These resources are essential for the deployment and operation of the chatbot UI application in a Kubernetes environment.

## Contents

The `k8s` directory is straightforward and contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for deploying and managing the chatbot UI application in a Kubernetes environment.

## Key Components

The `chatbot-ui.yaml` file is the key component of this directory. It defines four Kubernetes resources:

- **Namespace**: The Namespace 'chatbot-ui' is created to isolate the resources of the chatbot UI. This isolation is beneficial for managing resources in a multi-tenant environment and provides a scope for names.

- **Secret**: The Secret stores the OpenAI API key in a secure, base64 encoded format. Secrets are used in Kubernetes to store sensitive information like passwords, OAuth tokens, and ssh keys.

- **Deployment**: The Deployment specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. Deployments in Kubernetes describe the desired state for your applications and can automatically roll out changes to ensure the actual state matches the desired state.

- **Service**: The Service exposes the Deployment on port 80 and routes traffic to the container port 3000. Services in Kubernetes are an abstract way to expose applications running on a set of Pods as a network service.

## Usage & Examples

The `k8s` directory is used during the deployment phase of the chatbot UI application. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster to create the defined resources. This is typically done using the `kubectl apply` command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the resources defined in the `chatbot-ui.yaml` file. Once the resources are created, the chatbot UI application is deployed and managed by Kubernetes according to the specifications in the `chatbot-ui.yaml` file.

The `chatbot-ui.yaml` file can also be used as a template for creating similar applications. Developers can modify the file to suit their needs, changing the Docker image, the number of replicas, the container port, and other parameters as necessary.
