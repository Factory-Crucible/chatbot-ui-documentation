
# Services Directory

The `services` directory is a crucial part of the chatbot-ui project, serving as a hub for the application's service layer. This directory contains TypeScript files that define custom React hooks for error handling and API calls. These hooks are integral to the application's functionality, providing a bridge between the user interface and the backend. They are responsible for making HTTP requests, handling errors, and managing state, thereby ensuring smooth data flow and user experience.

## Contents

The `services` directory is composed of two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.

- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses `useFetch` to make API calls. It provides a function `getModels` that makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal`.

## Key Components

The `services` directory houses two key TypeScript files:

- `errorService.ts`: This file is crucial as it provides a mechanism for handling errors in a user-friendly manner. The `useErrorService` hook it exports is used throughout the application to provide localized error messages, enhancing the user experience by providing clear and understandable error information.

- `useApiService.ts`: This file is vital for the application's interaction with the backend. The `useApiService` hook it defines is used to make API calls, specifically a POST request to the `/api/models` endpoint. This hook is integral to the application's functionality, enabling it to retrieve data from the backend and handle it appropriately.

## Usage & Examples

The files in the `services` directory are used throughout the chatbot-ui project to handle errors and make API calls. Here are some examples of how they might be used:

- `errorService.ts`: The `useErrorService` hook could be used in a component to handle errors from an API call. For example, if an API call fails, the component could call `getModelsError` with the error object to get a user-friendly error message.

- `useApiService.ts`: The `useApiService` hook could be used in a component to make a POST request to the `/api/models` endpoint. For example, a component could call `getModels` with an object containing a `key` property to make the request.

Please note that these examples are illustrative and may not represent the exact usage patterns in the chatbot-ui project.
