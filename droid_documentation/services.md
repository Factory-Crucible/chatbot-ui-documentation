
## Services Directory

The `services` directory is a critical part of the Factory-Crucible/chatbot-ui-documentation codebase. It houses two TypeScript files, `errorService.ts` and `useApiService.ts`, which define custom React hooks that provide essential functionality to the application. These hooks are responsible for handling API calls and managing error messages, respectively. The hooks are designed to be reusable and are used throughout the codebase, making the `services` directory a key part of the application's architecture.

### Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages using the `useTranslation` hook from `next-i18next`. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.
- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint.

### Key Components

The `services` directory contains two key components:

- `useErrorService`: This custom React hook is a critical part of the application's error handling strategy. It provides localized error messages, which enhances the user experience by providing clear and understandable error messages. The hook is used throughout the codebase, making it a key part of the application's architecture.
- `useApiService`: This custom React hook is responsible for making API calls to the `/api/models` endpoint. It uses the `useFetch` hook to make these calls, and provides a function `getModels` that accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal`. This hook is used in various parts of the codebase, making it a key part of the application's data fetching strategy.

### Usage & Examples

The `useErrorService` hook is used throughout the codebase to provide localized error messages. It is typically used in components that need to handle errors from API calls. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object. The `ErrorMessage` object contains a title, a status code, and a list of messages, which are translated using the `useTranslation` hook.

The `useApiService` hook is used in components that need to make API calls to the `/api/models` endpoint. The hook provides a function `getModels` that accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal`. The `GetModelsRequestProps` interface expects a `key` of type string. The `getModels` function returns the result of the fetch operation, which can then be used by the component.
