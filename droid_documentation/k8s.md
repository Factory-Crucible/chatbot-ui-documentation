
# `k8s` Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations. Kubernetes, a popular open-source platform for managing containerized workloads and services, is used in this project to orchestrate the deployment, scaling, and management of the chatbot UI application. The configurations stored in this directory are instrumental in defining the behavior and properties of the Kubernetes resources associated with the chatbot UI.

## Contents

The `k8s` directory contains a single file, `chatbot-ui.yaml`. This file is a Kubernetes configuration file that outlines the specifications for various Kubernetes resources required for the chatbot UI application. The directory does not contain any subdirectories.

### `chatbot-ui.yaml`

The `chatbot-ui.yaml` file is a Kubernetes configuration file that defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. 

- The Namespace, named 'chatbot-ui', is used to create a distinct environment within the Kubernetes cluster where the resources of the chatbot UI are isolated from other resources in the cluster. 
- The Secret is used to securely store the OpenAI API key, which is essential for the chatbot UI to interact with the OpenAI API. The key is stored in a base64 encoded format to ensure its security.
- The Deployment outlines the specifications for the chatbot UI application, including the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret.
- The Service is responsible for exposing the Deployment on port 80 and routing traffic to the container port 3000. This allows the chatbot UI application to be accessible over the network.

## Key Components

The `chatbot-ui.yaml` file is the key component of the `k8s` directory. It encapsulates the entire Kubernetes configuration for the chatbot UI application. The file is instrumental in defining the behavior of the chatbot UI application within a Kubernetes environment, including how it interacts with the OpenAI API, how it scales to handle traffic, and how it is exposed to the network.

## Usage & Examples

The `k8s` directory and its contents are primarily used by Kubernetes to orchestrate the deployment and management of the chatbot UI application. When deploying the application to a Kubernetes cluster, the `chatbot-ui.yaml` file is applied to the cluster. This creates the defined Namespace, Secret, Deployment, and Service in the cluster, effectively deploying the chatbot UI application.

For example, to deploy the chatbot UI application to a Kubernetes cluster, the following command would be used:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command tells Kubernetes to create the resources defined in the `chatbot-ui.yaml` file. Once the command is executed, the chatbot UI application is deployed and accessible over the network via the defined Service.

Please note that the above command assumes that `kubectl`, the Kubernetes command-line tool, is installed and configured to interact with your Kubernetes cluster, and that the command is run from the `k8s` directory.
