
# `k8s` Directory Documentation

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It houses the Kubernetes configurations that are essential for deploying and managing the chatbot UI application in a Kubernetes environment. The directory contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service.

## Contents

The `k8s` directory is straightforward and contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for deploying and managing the chatbot UI application in a Kubernetes environment.

## Key Components

The `chatbot-ui.yaml` file is the key component of this directory. It outlines four Kubernetes resources that are integral to the deployment and management of the chatbot UI application:

- **Namespace**: The Namespace, named 'chatbot-ui', is used to isolate the resources of the chatbot UI application. This isolation ensures that the resources do not interfere with other applications running in the same Kubernetes cluster.
- **Secret**: The Secret resource is used to securely store the OpenAI API key. The key is stored in a base64 encoded format, ensuring that it is not exposed in plain text.
- **Deployment**: The Deployment resource specifies the Docker image to be used for the chatbot UI application, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret resource, ensuring that the key is available to the application.
- **Service**: The Service resource exposes the Deployment on port 80. It routes traffic to the container port 3000, ensuring that the chatbot UI application is accessible to users.

## Usage & Examples

The `k8s` directory is used during the deployment process of the chatbot UI application. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster, which creates the defined resources and deploys the application.

Here is a simplified example of how the `chatbot-ui.yaml` file might be used:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command applies the `chatbot-ui.yaml` file to the Kubernetes cluster, creating the Namespace, Secret, Deployment, and Service resources. The chatbot UI application is then deployed and made accessible to users.

Please note that this is a simplified example and the actual usage may vary depending on the specific deployment process and Kubernetes configuration.
