
## k8s Directory

The `k8s` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It is responsible for the Kubernetes configurations of the chatbot UI application. Kubernetes, a popular open-source platform, is used for automating deployment, scaling, and managing containerized applications. The configurations in this directory are essential for the deployment and orchestration of the chatbot UI application in a Kubernetes environment.

### Contents

The `k8s` directory is straightforward and contains a single file, `chatbot-ui.yaml`. This file holds the Kubernetes configurations for the chatbot UI application. There are no subdirectories within the `k8s` directory.

- `chatbot-ui.yaml`: This is a Kubernetes configuration file. It defines four Kubernetes resources: a Namespace, a Secret, a Deployment, and a Service. These resources are essential for the deployment and operation of the chatbot UI application in a Kubernetes environment.

### Key Components

The `chatbot-ui.yaml` file is the key component of the `k8s` directory. It contains the following Kubernetes resources:

- Namespace: The Namespace, named 'chatbot-ui', is used to isolate the resources of the chatbot UI application. This isolation is beneficial for managing resources in a multi-tenant cluster environment.

- Secret: The Secret resource is used to store the OpenAI API key in a secure, base64 encoded format. This ensures the sensitive API key is not exposed in plain text.

- Deployment: The Deployment resource specifies the Docker image to be used, the number of replicas, and the container port. It also retrieves the OpenAI API key from the Secret. This resource is responsible for maintaining the desired state of the application.

- Service: The Service resource exposes the Deployment on port 80 and routes traffic to the container port 3000. This allows the chatbot UI application to be accessible over the network.

### Usage & Examples

The `k8s` directory is used during the deployment process of the chatbot UI application. When deploying the application in a Kubernetes environment, the `chatbot-ui.yaml` file is applied using the `kubectl apply` command. This command creates or updates the Kubernetes resources defined in the file.

For example, to deploy the chatbot UI application, a developer or DevOps engineer would navigate to the `k8s` directory and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create or update the Namespace, Secret, Deployment, and Service as defined in the `chatbot-ui.yaml` file. The `-f` flag specifies the file or directory that contains the configuration(s).

Please note that the actual usage of the `k8s` directory and the `chatbot-ui.yaml` file may vary depending on the specific deployment and orchestration requirements of the chatbot UI application.
