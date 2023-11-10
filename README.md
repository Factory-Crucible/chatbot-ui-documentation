
# Integration Chatbot UI

Welcome to the documentation for the Integration Chatbot UI codebase. This document serves as the entry point for developers, providing a high-level overview of the codebase. The aim is to guide developers to have a better understanding of the context of the code as part of the whole puzzle.

## Overview

The Integration Chatbot UI is a project that provides a user interface for a chatbot. It is designed to be a comprehensive solution for managing chat conversations, prompts, and settings. The project is hosted on GitHub and can be found at [https://github.com/Factory-Crucible/integration-chatbot-ui](https://github.com/Factory-Crucible/integration-chatbot-ui).

### Purpose

The purpose of this repository is to provide a user-friendly interface for interacting with a chatbot. It includes features for managing chat conversations, prompts, and settings. The chatbot UI is designed to be flexible and customizable, allowing users to tailor the chat experience to their needs.

This repository is a standalone project, but it can also be integrated with other services to provide a more comprehensive solution. For example, it can be connected to a backend service that handles the chatbot's logic, or it can be integrated with a database to store chat history.

### Technologies used

The Integration Chatbot UI is built using several leading technologies:

- **ReactJS**: A JavaScript library for building user interfaces. It is used to create the various components of the chatbot UI.
- **Next.js**: A React framework that enables features like server-side rendering and static site generation.
- **TypeScript**: A statically typed superset of JavaScript that adds types to the language. It is used to ensure type safety and improve developer productivity.
- **Tailwind CSS**: A utility-first CSS framework for rapidly building custom designs.
- **Docker**: A platform used for developing, shipping, and running applications. It is used to containerize the application for easy deployment.
- **Kubernetes**: An open-source platform for automating deployment, scaling, and managing containerized applications. It is used to manage the application in a containerized environment.
- **GitHub Actions**: A CI/CD platform used for automating workflows. It is used to run tests and deploy the Docker image.

### Major Components

The Integration Chatbot UI codebase consists of several major components:

- **Components**: This is the heart of the application, containing all the React components that make up the UI. It includes components for buttons, chat, chatbar, folder, markdown, mobile, promptbar, search, settings, sidebar, and spinner.
- **Hooks**: This directory contains custom React hooks that encapsulate various functionalities used across the application.
- **Services**: This directory contains services that interact with APIs and handle data fetching.
- **Utils**: This directory contains utility functions and modules used throughout the application.

### Conventions

The codebase follows several conventions:

- **File Naming**: Files are named in camelCase. Test files have the `.test.ts` extension.
- **Directory Structure**: Each major component of the application has its own directory. Subcomponents are placed in a `components` subdirectory within their parent component's directory.
- **Testing**: Tests are placed in a `__tests__` directory at the root of the project. Each test file is named after the file it is testing, with the `.test.ts` extension.

## Structure

The Integration Chatbot UI codebase is organized into several directories, each serving a specific purpose. Here is a high-level overview of the structure:

```
.
├── .github
├── __tests__
├── components
├── docs
├── hooks
├── k8s
├── pages
├── public
├── services
├── styles
├── types
└── utils
```

- **.github**: Contains GitHub workflows for running tests and deploying Docker images.
- **__tests__**: Contains tests for the application's utility functions.
- **components**: Contains React components for the application.
- **docs**: Contains documentation for the project.
- **hooks**: Contains custom React hooks.
- **k8s**: Contains Kubernetes configurations for the application.
- **pages**: Contains Next.js pages and API routes.
- **public**: Contains public assets like favicon and screenshots.
- **services**: Contains services for API interactions.
- **styles**: Contains global CSS styles.
- **types**: Contains TypeScript types and interfaces.
- **utils**: Contains utility functions and modules.

For a more detailed overview of each directory, please refer to the respective documentation files linked in the following sections.

## Main Flows

The Integration Chatbot UI codebase is designed around several main flows that correspond to the core functionalities of the application. These flows include managing chat conversations, handling prompts, and managing settings.

### Overview Of Flows

- **Chat Conversations**: The chat conversation flow begins with the user interacting with the chat interface. The user's input is processed and sent to the backend service, which generates a response. The response is then displayed in the chat interface. This flow involves several components, including the Chat, Chatbar, and Sidebar components. For more details, refer to the [Chat documentation](./components/Chat_documentation.md) and [Chatbar documentation](./components/Chatbar/README.md).

- **Prompts**: The prompts flow involves the creation, management, and deletion of prompts. Prompts are created and managed through the Promptbar component, and they are displayed in the chat interface. For more details, refer to the [Promptbar documentation](./components/Promptbar_documentation.md).

- **Settings**: The settings flow involves the management of application settings. Settings are managed through the Settings component, and they affect various aspects of the application, such as the chat interface and the behavior of the chatbot. For more details, refer to the [Settings documentation](./components/Settings_documentation.md).

### System Connections

The Integration Chatbot UI interacts with several external systems:

- **Backend Service**: The application interacts with a backend service to process chat conversations. The user's input is sent to the backend service, which generates a response that is displayed in the chat interface.

- **OpenAI API**: The application interacts with the OpenAI API to fetch a list of models. The models are used in the chat conversation flow.

- **Google Custom Search API**: The application interacts with the Google Custom Search API to perform searches. The search results are displayed in the chat interface.

## Testing Principles

The Integration Chatbot UI codebase includes a suite of tests to ensure the correctness of the application. The tests are located in the `__tests__` directory at the root of the project. The tests are written using the Vitest testing framework.

The tests cover various aspects of the application, including utility functions and API interactions. For example, the `importExports.test.ts` file in the `__tests__/utils/app` directory contains tests for the import and export utility functions of the application.

For more details on the tests, refer to the [__tests__ documentation](./__tests___documentation.md).
