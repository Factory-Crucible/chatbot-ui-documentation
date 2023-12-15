
# Services Directory

The `services` directory is a crucial part of the chatbot-ui project, serving as the home for two TypeScript files that define custom React hooks. These hooks, `useErrorService` and `useApiService`, play a significant role in the application's functionality. They handle error messaging and API calls, respectively, contributing to the overall data flow and interactions within the project.

## Contents

The `services` directory is straightforward in its structure, containing two TypeScript files and no subdirectories. The files are:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages using the `useTranslation` hook. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.

- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses `useFetch` to make API calls. It provides a function `getModels` that makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal`. The `useApiService` hook returns an object that exposes the `getModels` function.

## Key Components

The `services` directory houses two key TypeScript files, `errorService.ts` and `useApiService.ts`, each defining a custom React hook that contributes to the application's functionality.

- `errorService.ts`: The `useErrorService` hook defined in this file is responsible for providing localized error messages. It uses the `useTranslation` hook from `next-i18next` to translate error messages, ensuring that the application can cater to a diverse user base. The `getModelsError` function it returns is used throughout the application to handle errors, making it a critical part of the project's error management strategy.

- `useApiService.ts`: The `useApiService` hook defined in this file is central to the application's interaction with the API. It uses the `useFetch` hook to make API calls, providing a function `getModels` that makes a POST request to the `/api/models` endpoint. This function is used to fetch models from the API, playing a crucial role in the application's data flow.

## Usage & Examples

The files in the `services` directory are used throughout the chatbot-ui project to handle error messages and make API calls.

- `errorService.ts`: The `useErrorService` hook is used in components that need to handle errors. For example, a component might use it to get an error message when an API call fails. The `getModelsError` function it returns takes an error object and returns an `ErrorMessage` object, which can then be displayed to the user.

- `useApiService.ts`: The `useApiService` hook is used in components that need to make API calls. For example, a component might use it to fetch models from the API. The `getModels` function it provides takes an object of type `GetModelsRequestProps` and an optional `AbortSignal`, making a POST request to the `/api/models` endpoint and returning the result.

Please note that the code snippets provided in the `DIRECTORY_STRUCTURE` are not representative of typical usage patterns. They are skeleton code meant to give an idea of the structure and functionality of the hooks defined in the `services` directory.
