
## k8s Directory

The `k8s` directory is responsible for housing the Kubernetes configurations for the chatbot UI application. It contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. The Namespace, labeled 'chatbot-ui', is used to isolate the resources of the chatbot UI. The Secret is used to securely store the OpenAI API key in a base64 encoded format. The Deployment specifies the Docker image, the number of replicas, and the container port, while also retrieving the OpenAI API key from the Secret. Lastly, the Service exposes the Deployment on port 80 and routes traffic to the container port 3000.

### Contents

The `k8s` directory contains one file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for the chatbot UI application. It outlines the Namespace, Secret, Deployment, and Service required for the application.

### Key Components

The key component within this directory is the `chatbot-ui.yaml` file. This file is crucial as it outlines the Kubernetes resources necessary for the chatbot UI application. It defines the Namespace for isolating the application's resources, the Secret for securely storing the OpenAI API key, the Deployment for specifying the Docker image, the number of replicas, and the container port, and the Service for exposing the Deployment on port 80 and routing traffic to the container port 3000.

### Usage & Examples

The `chatbot-ui.yaml` file is used to define the Kubernetes resources for the chatbot UI application. It is used during the deployment process, where the Kubernetes configurations are applied to create the necessary resources for the application. For example, during deployment, the Namespace 'chatbot-ui' is created to isolate the application's resources, the Secret is created to securely store the OpenAI API key, the Deployment is created to specify the Docker image, the number of replicas, and the container port, and the Service is created to expose the Deployment on port 80 and route traffic to the container port 3000.
