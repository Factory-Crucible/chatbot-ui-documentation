
# Chatbot UI Documentation

Welcome to the documentation for the Chatbot UI project. This document serves as the entry point for developers, providing a high-level overview of the codebase. The aim is to guide developers to have a better understanding of the context of the code as part of the whole puzzle.

## `Overview`

###Purpose

The Chatbot UI project is designed to create a user-friendly interface for interacting with a chatbot. The chatbot is powered by OpenAI and Google APIs, and the UI provides a platform for users to engage in conversations with the chatbot, manage prompts and folders, and adjust settings. The project is a microservice that interacts with other services, such as the OpenAI and Google APIs, to generate responses and search results.

### Technologies-:/'"Used

The Chatbot UI project is a Docker-based Node.js application that uses the Next.js framework for server-side rendering. It uses TypeScript for static typing, and React for building the user interface. The project also uses the Tailwind CSS framework for styling, and the i18next library for internationalization. For state management, it uses a custom hook that creates a typed reducer with dispatch and state. For making HTTP requests, it uses another custom hook that provides methods for each HTTP verb.

### Major Components

The codebase consists of several major components:

- The 'components' directory houses various parts of the project, each in its own subdirectory. These components handle functionalities such as managing the sidebar, settings, chat bar, chat messages, folders, and prompts.
- The 'pages' directory contains key files for the home page and an 'api' subdirectory for handling API requests.
- The 'utils' directory contains utility files and subdirectories for different aspects of the project, such as managing folders, chat conversations, and server-side operations.
- The 'hooks' directory defines custom React hooks for creating a typed reducer and making API calls.
- The 'services' directory contains services for error handling and API calls.
- The 'types' directory defines various interfaces, types, and constants used throughout the project.
- The '__tests__' directory is for testing, with a 'utils' subdirectory as a testing suite.

### Conventions

The project follows certain conventions for better understanding and consistency. File names are in camelCase, and directories are in lowercase. Each major component of the project has its own directory, and related files are grouped into subdirectories. TypeScript is used throughout the project for static typing, and React functional components are used for building the user interface.

## Structure

The structure of the codebase is organized into directories, each serving a specific purpose. Here is a high-level overview of the directories:

- '.' (root): Contains configuration files for the project, Docker, and various tools. It also includes the 'package.json' file that lists the project's dependencies and scripts.
- 'components': Houses various parts of the project, each in its own subdirectory.
- 'pages': Contains key files for the home page and an 'api' subdirectory for handling API requests.
- 'utils': Contains utility files and subdirectories for different aspects of the project.
- 'hooks': Defines custom React hooks.
- 'services': Contains services for error handling and API calls.
- 'types': Defines various interfaces, types, and constants.
- 'k8s': Contains Kubernetes configurations.
- '__tests__': Contains test files and a 'utils' subdirectory as a testing suite.
- 'public': Contains branding files and a 'screenshots' subdirectory.

Here is a visual representation of the directory structure:

```
.
├── __tests__
├── components
├── hooks
├── k8s
├── pages
├── public
├── services
├── styles
├── types
└── utils
```

## Main Flows

### Overview Of Flows

The main flows in the codebase revolve around the interaction between the user and the chatbot. The user can initiate a conversation with the chatbot, manage prompts and folders, and adjust settings. The chatbot generates responses based on the user's input and the selected AI model. The chatbot also interacts with the OpenAI and Google APIs to generate responses and search results.

For a more in-depth understanding of the flows, refer to the following documentation files:

- [Chat Component](#Technologies-used): Handles the chat functionality, including generating responses and managing chat messages.
- [Chatbar Component](#overview): Manages the chat bar, including initiating new conversations and managing prompts and folders.
- [API Pages](): Handles API requests and responses, interacting with the OpenAI and Google APIs.

### System Connections

The Chatbot UI project interacts with external systems, specifically the OpenAI and Google APIs. The 'api' subdirectory in the 'pages' directory contains files for handling these API requests and responses. The 'models.ts' file constructs URLs and fetches data from the OpenAI API. The 'chat.ts' file processes requests, encodes messages, and interacts with an OpenAI service. The 'google.ts' file interacts with the Google Custom Search API and the OpenAI API to generate prompts and send responses.

## Testing Principles

The project follows a testing approach that focuses on unit testing. The '__tests__' directory contains test files and a 'utils' subdirectory as a testing suite. The 'importExports.test.ts' file validates the import and export operations of the application. It ensures that the objects being exported conform to the expected format for each version. It also tests a function named 'cleanData', which is designed to update data from older export formats to the latest one. The test verifies that the updated data aligns with the expected structure of the current format.

For more information on testing, refer to the [Testing Documentation](./__tests__.md "I wonder how this is rendered").
