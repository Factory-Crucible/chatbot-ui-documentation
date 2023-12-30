
## Services Directory

The `services` directory is a container for two TypeScript files, `errorService.ts` and `useApiService.ts`. These files define custom React hooks that provide specific functionalities within the codebase. The hooks are used to handle API calls and error messages in a localized manner.

### Contents

The `services` directory contains the following files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService`. The hook uses the `useTranslation` hook from `next-i18next` to provide localized error messages. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.
- `useApiService.ts`: This file defines a custom React hook named `useApiService`. This hook uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint.

### Key Components

- `useErrorService` Hook: This hook provides a function `getModelsError` that takes an error object and returns an `ErrorMessage` object. The `ErrorMessage` object contains a title, a status code, and a list of messages. The title and messages are translated using the `useTranslation` hook.
- `useApiService` Hook: This hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.

### Usage & Examples

The `useErrorService` hook is used to provide localized error messages. It is used in components that need to handle and display error messages to the user. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object.

The `useApiService` hook is used to make API calls. It is used in components that need to fetch data from the `/api/models` endpoint. The hook provides a function `getModels` which makes a POST request to the endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.
