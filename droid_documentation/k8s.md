
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations. Kubernetes, a popular open-source platform for managing containerized workloads and services, is used in this project to handle the deployment and scaling of the chatbot UI application. The configurations stored in this directory are essential for defining the behavior and properties of the Kubernetes resources associated with the chatbot UI.

### Contents

The `k8s` directory is straightforward in its structure, containing a single file named `chatbot-ui.yaml`. This file is a Kubernetes configuration file that outlines the necessary resources for the chatbot UI application.

- `k8s/chatbot-ui.yaml`: This file defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. The Namespace, labeled 'chatbot-ui', is used to isolate the resources of the chatbot UI. The Secret is employed to securely store the OpenAI API key in a base64 encoded format. The Deployment outlines the Docker image to be used, the number of replicas, and the container port, and it retrieves the OpenAI API key from the Secret. Lastly, the Service exposes the Deployment on port 80 and routes traffic to the container port 3000.

### Key Components

The `k8s/chatbot-ui.yaml` file is the key component of this directory. It is through this file that the Kubernetes resources for the chatbot UI application are defined and managed. The file's structure and the resources it outlines are integral to the deployment and operation of the chatbot UI application.

### Usage & Examples

The `k8s` directory and its contents are primarily used during the deployment process of the chatbot UI application. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster, which then creates the defined resources and manages the application accordingly.

For example, when deploying the chatbot UI application, a command similar to `kubectl apply -f k8s/chatbot-ui.yaml` would be used. This command instructs Kubernetes to create or update the resources defined in the `chatbot-ui.yaml` file.

It's important to note that the actual usage may vary based on the specific deployment process and Kubernetes setup. The example provided is a typical usage pattern and may not represent all possible scenarios.
