
# `k8s` Directory Documentation

The `k8s` directory is a critical part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations that orchestrate the deployment and operation of the chatbot UI application. This directory contains a single file, `chatbot-ui.yaml`, which defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. These resources work together to ensure the secure, scalable, and efficient operation of the chatbot UI application within a Kubernetes environment.

## Contents

The `k8s` directory is straightforward in its structure, containing a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the Namespace, Secret, Deployment, and Service resources necessary for the chatbot UI application's operation within a Kubernetes environment.

## Key Components

The `chatbot-ui.yaml` file is the key component of the `k8s` directory. It defines four Kubernetes resources that are integral to the operation of the chatbot UI application:

- **Namespace 'chatbot-ui'**: This resource isolates the chatbot UI application's resources within the Kubernetes environment, ensuring that they do not interfere with other applications' resources.

- **Secret**: This resource securely stores the OpenAI API key, which is necessary for the chatbot UI application's operation. The key is stored in a base64 encoded format to ensure its security.

- **Deployment**: This resource specifies the Docker image to be used for the chatbot UI application, the number of replicas to be created for scalability, and the container port to be used for communication. It also retrieves the OpenAI API key from the Secret resource.

- **Service**: This resource exposes the Deployment on port 80, routing traffic to the container port 3000. This allows the chatbot UI application to communicate with other applications and services.

## Usage & Examples

The `k8s` directory and its `chatbot-ui.yaml` file are used to deploy and manage the chatbot UI application within a Kubernetes environment. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster using the `kubectl apply` command, which creates or updates the defined resources.

For example, to deploy the chatbot UI application, a developer or operations engineer would navigate to the directory containing the `chatbot-ui.yaml` file and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the Namespace, Secret, Deployment, and Service resources as defined in the `chatbot-ui.yaml` file. Once these resources are created or updated, the chatbot UI application is operational and ready to serve user requests.

The `k8s` directory and its `chatbot-ui.yaml` file are integral to the operation of the chatbot UI application, providing the necessary configurations for its deployment and operation within a Kubernetes environment.
