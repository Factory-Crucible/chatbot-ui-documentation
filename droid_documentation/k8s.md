
## k8s Directory

The `k8s` directory is dedicated to the Kubernetes configurations required for the chatbot UI application. It contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. 

### Contents

The `k8s` directory contains one file:

- `chatbot-ui.yaml`: A Kubernetes configuration file that defines the Namespace, Secret, Deployment, and Service required for the chatbot UI application.

### Key Components

The `chatbot-ui.yaml` file is the sole component of this directory. It outlines four Kubernetes resources:

- Namespace: The `chatbot-ui` Namespace is created to isolate the resources of the chatbot UI application.
- Secret: This resource securely stores the OpenAI API key in a base64 encoded format.
- Deployment: This resource specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret.
- Service: This resource exposes the Deployment on port 80 and routes traffic to the container port 3000.

### Usage & Examples

The `chatbot-ui.yaml` file is used to configure the Kubernetes resources for the chatbot UI application. It is applied to a Kubernetes cluster to create the necessary resources for the application. 

For example, to apply the configuration to a Kubernetes cluster, the following command would be used:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command creates the Namespace, Secret, Deployment, and Service as defined in the `chatbot-ui.yaml` file.
