
## k8s Directory

The `k8s` directory is a critical part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for Kubernetes configurations. Kubernetes, a powerful container orchestration system, is used to manage the deployment of the chatbot UI application. The configurations within this directory are essential for defining the resources required for the application's deployment and operation.

### Contents

The `k8s` directory is straightforward in its structure, containing a single file, `chatbot-ui.yaml`. This file holds the Kubernetes configurations for the chatbot UI application. There are no subdirectories within the `k8s` directory.

- `k8s/chatbot-ui.yaml`: This is a Kubernetes configuration file that defines the necessary resources for the chatbot UI application. These resources include a Namespace, a Secret, a Deployment, and a Service.

### Key Components

The `k8s/chatbot-ui.yaml` file is the key component within this directory. It outlines the Kubernetes resources required for the chatbot UI application.

- Namespace: The Namespace, named 'chatbot-ui', is used to isolate the resources of the chatbot UI application. This isolation ensures that the resources do not interfere with those of other applications within the same Kubernetes cluster.
- Secret: The Secret resource is used to securely store the OpenAI API key. This key is base64 encoded to ensure its security.
- Deployment: The Deployment resource outlines the specifics of the chatbot UI application. It specifies the Docker image to be used, the number of replicas, and the container port. The OpenAI API key, stored in the Secret, is also retrieved by the Deployment.
- Service: The Service resource is used to expose the Deployment on port 80. It routes traffic to the container port 3000, allowing users to interact with the chatbot UI application.

### Usage & Examples

The `k8s` directory and its contents are used during the deployment process of the chatbot UI application. When deploying the application to a Kubernetes cluster, the `chatbot-ui.yaml` file is applied using the `kubectl apply` command. This command creates the resources defined in the file within the Kubernetes cluster.

For example, to deploy the chatbot UI application, one would navigate to the directory containing the `chatbot-ui.yaml` file and run the following command:

```bash
kubectl apply -f chatbot-ui.yaml
```

This command instructs Kubernetes to create the Namespace, Secret, Deployment, and Service as defined in the `chatbot-ui.yaml` file. Once these resources are created, the chatbot UI application is deployed and operational within the Kubernetes cluster.
