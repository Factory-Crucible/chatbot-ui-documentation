
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations that are essential for the deployment and orchestration of the chatbot UI application. The directory contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. The Namespace isolates the resources of the chatbot UI, ensuring that they are logically grouped and can operate independently of other resources in the Kubernetes cluster. The Secret provides a secure storage mechanism for sensitive data, in this case, the OpenAI API key. The Deployment defines the specifications for the application, such as the Docker image to be used, the number of replicas, and the container port. The Service, on the other hand, is responsible for exposing the Deployment on port 80 and routing traffic to the container port 3000.

### Contents

The `k8s` directory is straightforward and contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that outlines the necessary resources for the chatbot UI application. It defines a Namespace, a Secret, a Deployment, and a Service, each serving a specific purpose in the deployment and orchestration of the application.

### Key Components

The `k8s` directory's key component is the `chatbot-ui.yaml` file. This file is critical because it outlines the necessary Kubernetes resources for the chatbot UI application. It defines a Namespace for isolating the resources of the application, a Secret for securely storing the OpenAI API key, a Deployment for specifying the application's specifications, and a Service for exposing the Deployment and routing traffic.

### Usage & Examples

The `k8s` directory and its `chatbot-ui.yaml` file are used during the deployment process of the chatbot UI application. When deploying the application to a Kubernetes cluster, the `kubectl apply -f chatbot-ui.yaml` command is executed. This command instructs Kubernetes to create or update the resources defined in the `chatbot-ui.yaml` file.

The `chatbot-ui.yaml` file defines four resources:

- The Namespace 'chatbot-ui' is created to isolate the resources of the chatbot UI. This ensures that the resources of the application are logically grouped and can operate independently of other resources in the Kubernetes cluster.
- The Secret stores the OpenAI API key in a base64 encoded format. This provides a secure storage mechanism for sensitive data.
- The Deployment specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This defines the specifications for the application.
- The Service exposes the Deployment on port 80 and routes traffic to the container port 3000. This ensures that the application is accessible to users.

Please note that the actual usage of the `k8s` directory and the `chatbot-ui.yaml` file may vary depending on the specific deployment and orchestration requirements of the chatbot UI application.
