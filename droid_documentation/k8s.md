
# `k8s` Directory Documentation

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It houses the Kubernetes configurations for the chatbot UI application. Kubernetes, a popular container orchestration platform, is used to manage the deployment and scaling of the chatbot UI application. The configurations in this directory are instrumental in defining the behavior of the application when it is deployed on a Kubernetes cluster.

## Contents

The `k8s` directory is straightforward and contains a single file, `chatbot-ui.yaml`. This file is the heart of the directory, containing the Kubernetes configurations for the chatbot UI application.

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. These resources are essential for the deployment and operation of the chatbot UI application on a Kubernetes cluster.

## Key Components

The `chatbot-ui.yaml` file is the key component of this directory. It defines the following Kubernetes resources:

- **Namespace**: The Namespace, named 'chatbot-ui', is used to isolate the resources of the chatbot UI application. This isolation is beneficial for managing resources in a multi-tenant environment and can help prevent potential conflicts between different parts of the system.

- **Secret**: The Secret resource is used to store the OpenAI API key in a secure, base64 encoded format. This is a critical security measure, ensuring that sensitive data is not exposed in plain text.

- **Deployment**: The Deployment resource specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This resource is responsible for the actual deployment of the chatbot UI application on the Kubernetes cluster.

- **Service**: The Service resource exposes the Deployment on port 80 and routes traffic to the container port 3000. This allows the chatbot UI application to be accessible over the network.

## Usage & Examples

The `k8s` directory is used during the deployment process of the chatbot UI application. When deploying the application on a Kubernetes cluster, the `chatbot-ui.yaml` file is applied using the `kubectl apply` command. This command creates or updates the Kubernetes resources defined in the file.

For example, to deploy the chatbot UI application, one would navigate to the directory containing the `chatbot-ui.yaml` file and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the Namespace, Secret, Deployment, and Service as defined in the `chatbot-ui.yaml` file. Once the command is executed successfully, the chatbot UI application is deployed and accessible on the specified port.

Please note that the actual usage may vary depending on the specific deployment environment and configuration. Always refer to the most up-to-date deployment instructions for the chatbot UI application.
