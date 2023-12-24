
# `k8s` Directory Documentation

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It houses the Kubernetes configurations that are essential for deploying the chatbot UI application in a Kubernetes environment. The directory contains a single file, `chatbot-ui.yaml`, which outlines the necessary Kubernetes resources for the application. These resources include a Namespace, a Secret, a Deployment, and a Service. 

## Contents

The `k8s` directory is straightforward and contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for deploying the chatbot UI application in a Kubernetes environment.

There are no subdirectories within the `k8s` directory.

## Key Components

The `k8s` directory's primary component is the `chatbot-ui.yaml` file. This file is the blueprint for deploying the chatbot UI application in a Kubernetes environment. It defines four Kubernetes resources:

- **Namespace**: The Namespace, named 'chatbot-ui', is used to isolate the resources of the chatbot UI application from other applications running in the same Kubernetes cluster. This isolation is crucial for maintaining the integrity and security of the application.

- **Secret**: The Secret resource is used to store the OpenAI API key securely. The key is stored in a base64 encoded format, ensuring that it is not exposed in plain text.

- **Deployment**: The Deployment resource outlines the specifications for the chatbot UI application. It specifies the Docker image to be used, the number of replicas, and the container port. The Deployment also retrieves the OpenAI API key from the Secret resource.

- **Service**: The Service resource exposes the Deployment on port 80. It routes traffic from this port to the container port 3000, allowing users to access the chatbot UI application.

## Usage & Examples

The `k8s` directory is used during the deployment process of the chatbot UI application. When deploying the application in a Kubernetes environment, the `chatbot-ui.yaml` file is applied to create the necessary Kubernetes resources.

Here is a simplified example of how the `chatbot-ui.yaml` file might be used during deployment:

```bash
# Navigate to the directory containing the chatbot-ui.yaml file
cd k8s

# Apply the chatbot-ui.yaml file
kubectl apply -f chatbot-ui.yaml
```

This command creates the Namespace, Secret, Deployment, and Service defined in the `chatbot-ui.yaml` file. The chatbot UI application is then accessible via the Service's external IP address on port 80.

Please note that this is a simplified example. The actual deployment process may involve additional steps, such as setting up a Kubernetes cluster or configuring network policies.
