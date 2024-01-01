
## k8s Directory

The `k8s` directory is the home for Kubernetes configurations that are essential for the deployment of the chatbot UI application. It contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. 

### Contents

The `k8s` directory contains only one file:

- `chatbot-ui.yaml`: This file holds the Kubernetes configuration for the chatbot UI application. It defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service.

### Key Components

The `chatbot-ui.yaml` file is the key component in this directory. It outlines the Kubernetes resources required for the chatbot UI application:

- **Namespace 'chatbot-ui'**: This Namespace is created to isolate the resources of the chatbot UI, ensuring that they do not interfere with other resources in the Kubernetes cluster.
- **Secret**: This resource stores the OpenAI API key in a secure, base64 encoded format. This key is necessary for the chatbot UI application to interact with the OpenAI API.
- **Deployment**: This resource specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This Deployment resource is responsible for creating and managing the Pods that run the chatbot UI application.
- **Service**: This resource exposes the Deployment on port 80 and routes traffic to the container port 3000. This Service resource allows the chatbot UI application to be accessed from outside the Kubernetes cluster.

### Usage & Examples

The `k8s` directory is used during the deployment process of the chatbot UI application. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster, creating the defined resources and deploying the application.

For example, to deploy the chatbot UI application to a Kubernetes cluster, the following command would be used:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command applies the `chatbot-ui.yaml` file to the Kubernetes cluster, creating the Namespace, Secret, Deployment, and Service resources as defined in the file. The chatbot UI application is then accessible at the IP address provided by the Service resource.
