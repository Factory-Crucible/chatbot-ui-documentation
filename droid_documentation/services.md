
## Services Directory

The `services` directory is a critical part of the chatbot-ui project, serving as the hub for the application's service-related functionalities. It contains two TypeScript files, `errorService.ts` and `useApiService.ts`, which define custom React hooks that provide essential services for error handling and API calls. These services are integral to the application's data flow and interactions, as they are used throughout the codebase to handle errors, make API calls, and manage application state.

### Contents

The `services` directory is a flat structure with no subdirectories, containing only two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages using the `useTranslation` hook. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.

- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses `useFetch` to make API calls. It provides a function `getModels` that makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal`.

### Key Components

The `services` directory contains two key TypeScript files:

- `errorService.ts`: The `useErrorService` hook defined in this file is crucial for providing localized error messages throughout the application. The `getModelsError` function it returns is used to handle errors that occur when making a POST request to the `/api/models` endpoint.

- `useApiService.ts`: The `useApiService` hook defined in this file is essential for making API calls in the application. The `getModels` function it provides is used to make a POST request to the `/api/models` endpoint, which is a critical part of the application's data flow and interactions.

### Usage & Examples

The `services` directory is used throughout the chatbot-ui project to provide essential services for error handling and API calls.

- `errorService.ts`: The `useErrorService` hook is used wherever error handling is required in the application. For example, when making a POST request to the `/api/models` endpoint, the `getModelsError` function is used to handle any errors that occur and provide localized error messages.

- `useApiService.ts`: The `useApiService` hook is used wherever API calls are made in the application. For example, when making a POST request to the `/api/models` endpoint, the `getModels` function is used to make the request and handle the response.

Please note that the code snippets provided in the `DIRECTORY_STRUCTURE` are not representative of typical usage patterns. They are skeleton code and do not include the full implementation details.
