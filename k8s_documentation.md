
## k8s Directory

The `k8s` directory is a crucial part of the `integration-chatbot-ui` project. It contains Kubernetes configurations for the chatbot user interface. Kubernetes, a popular open-source platform, is used for automating deployment, scaling, and management of containerized applications. In the context of this project, Kubernetes is used to orchestrate the deployment of the chatbot UI, ensuring its consistent behavior across different environments.

### Contents

The `k8s` directory contains a single file:

- `chatbot-ui.yaml`: This is a Kubernetes configuration file for the chatbot user interface. It defines four resources: a Namespace, a Secret, a Deployment, and a Service.

### Folder Structure Overview

The `k8s` directory is straightforward and contains no subdirectories. It houses a single configuration file, `chatbot-ui.yaml`, which holds all the necessary Kubernetes configurations for the chatbot UI.

### Key Components

The key component in this directory is the `chatbot-ui.yaml` file. This file defines the following Kubernetes resources:

- **Namespace 'chatbot-ui'**: This namespace is created to isolate resources related to the chatbot UI. Namespaces are a way to divide cluster resources between multiple users or applications.

- **Secret**: This Kubernetes object stores the OpenAI API key in base64 encoded format. Secrets are used to store sensitive information like API keys, passwords, or certificates.

- **Deployment**: This specifies a single replica of the 'chatbot-ui' container, which is built from a Docker image. The container exposes port 3000 and uses the OpenAI API key from the Secret. Deployments are used to manage stateless applications, ensuring they are always available and up-to-date.

- **Service**: This exposes the Deployment on port 80 within the cluster, routing traffic to the container's port 3000. Services are an abstract way to expose an application running on a set of Pods as a network service.

### Usage & Examples

The `k8s` directory is used during the deployment phase of the `integration-chatbot-ui` project. The `chatbot-ui.yaml` file is applied to a Kubernetes cluster to create the necessary resources for the chatbot UI.

Here is an example of how to use the `chatbot-ui.yaml` file to deploy the chatbot UI to a Kubernetes cluster:

```bash
kubectl apply -f k8s/chatbot-ui.yaml
```

This command will create the Namespace, Secret, Deployment, and Service defined in the `chatbot-ui.yaml` file. The chatbot UI will then be accessible within the Kubernetes cluster.
