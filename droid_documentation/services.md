
## The Services Directory

The `services` directory is a crucial part of the codebase, acting as a hub for the application's core functionalities. It houses two TypeScript files, `errorService.ts` and `useApiService.ts`, which define custom React hooks that provide localized error messages and make API calls respectively. These hooks are integral to the application's operation, facilitating communication with the API and handling errors in a user-friendly manner. The absence of subdirectories in this directory underscores the focused nature of its role in the codebase.

### Contents of the Services Directory

The `services` directory contains two TypeScript files:

1. `errorService.ts`: This file exports a custom React hook named `useErrorService`. It provides localized error messages using the `useTranslation` hook from `next-i18next`. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages. The title and messages are translated using the `useTranslation` hook.

2. `useApiService.ts`: This file defines a custom React hook named `useApiService`. This hook uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.

### Key Components in the Services Directory

The `services` directory is home to two key TypeScript files:

- `errorService.ts`: The `useErrorService` hook defined in this file is crucial for providing localized error messages. The `getModelsError` function it returns takes an error object and returns an `ErrorMessage` object, which includes a title, status code, and list of messages. This ensures that errors are handled gracefully and communicated to the user in a clear, localized manner.

- `useApiService.ts`: The `useApiService` hook defined in this file is responsible for making API calls using the `useFetch` hook. The `getModels` function it provides makes a POST request to the `/api/models` endpoint, accepting an object of type `GetModelsRequestProps` and an optional `AbortSignal`. This function is key to fetching data from the API, making it a critical part of the application's functionality.

### Usage & Examples

The files in the `services` directory are used to provide core functionalities to the application:

- `errorService.ts`: The `useErrorService` hook is used throughout the application to provide localized error messages. For example, when an API call fails, the `getModelsError` function can be used to generate a user-friendly error message.

- `useApiService.ts`: The `useApiService` hook is used to make API calls. For instance, when the application needs to fetch data from the `/api/models` endpoint, it can use the `getModels` function provided by this hook. The function accepts an object of type `GetModelsRequestProps`, which includes a `key` of type string, and an optional `AbortSignal`.
