
## k8s Directory

The `k8s` directory is a dedicated space for Kubernetes configurations that are integral to the deployment of the chatbot UI application. It contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. The Namespace, labeled 'chatbot-ui', serves to isolate the resources specific to the chatbot UI. The Secret is used to securely store the OpenAI API key in a base64 encoded format. The Deployment details the Docker image, the number of replicas, and the container port, and retrieves the OpenAI API key from the Secret. Lastly, the Service exposes the Deployment on port 80, routing traffic to the container port 3000.

### Contents

The `k8s` directory contains a single file:

- `chatbot-ui.yaml`: This Kubernetes configuration file outlines the necessary resources for the chatbot UI application. It defines a Namespace, a Secret, a Deployment, and a Service. The Namespace, 'chatbot-ui', isolates the resources of the chatbot UI. The Secret stores the OpenAI API key in a base64 encoded format. The Deployment specifies the Docker image, the number of replicas, and the container port, and retrieves the OpenAI API key from the Secret. The Service exposes the Deployment on port 80, routing traffic to the container port 3000.

### Key Components

The key component in this directory is the `chatbot-ui.yaml` file. This file is crucial as it outlines the Kubernetes resources necessary for the deployment of the chatbot UI application. It defines the Namespace, Secret, Deployment, and Service, each of which plays a critical role in the deployment process. The Namespace isolates the resources of the chatbot UI, the Secret securely stores the OpenAI API key, the Deployment specifies the Docker image and other details, and the Service exposes the Deployment on port 80.

### Usage & Examples

The `k8s` directory and its contents are used during the deployment process of the chatbot UI application. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster to create the necessary resources for the application. For example, during the deployment process, the `kubectl apply -f chatbot-ui.yaml` command would be used to apply the configurations outlined in the `chatbot-ui.yaml` file to the Kubernetes cluster. This would create the Namespace, Secret, Deployment, and Service as defined in the file, setting up the necessary environment for the chatbot UI application.
