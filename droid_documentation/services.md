
## Services Directory

The `services` directory is a crucial part of the chatbot-ui project, housing two TypeScript files that define custom React hooks. These hooks, `useErrorService` and `useApiService`, play a significant role in the project's functionality. The `useErrorService` hook provides localized error messages, while the `useApiService` hook is used for making API calls. These hooks are integral to the project's functionality, contributing to the user interface's responsiveness and the chatbot's interaction with the user.

### Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages using the `useTranslation` hook. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.
- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses `useFetch` to make API calls. It provides a function `getModels` that makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal`. The `useApiService` hook returns an object that exposes the `getModels` function.

### Key Components

The `services` directory contains two key components:

- `useErrorService`: This custom React hook is crucial for providing localized error messages. It uses the `useTranslation` hook from `next-i18next` to translate error messages, enhancing the user experience by providing error messages in the user's preferred language.
- `useApiService`: This custom React hook is essential for making API calls. It uses another custom hook `useFetch` to make these calls, providing a function `getModels` which makes a POST request to the `/api/models` endpoint. This function is used extensively throughout the project to fetch models from the API.

### Usage & Examples

The `useErrorService` hook is used throughout the project to provide localized error messages. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object. This function is used in various parts of the project to handle errors and provide user-friendly error messages.

The `useApiService` hook is used to make API calls. It provides a function `getModels` that makes a POST request to the `/api/models` endpoint. This function is used in various parts of the project to fetch models from the API.

For example, the `getModels` function could be used as follows:

```typescript
const { getModels } = useApiService();
const models = getModels({ key: 'exampleKey' });
```

This would make a POST request to the `/api/models` endpoint with the `key` parameter set to `'exampleKey'`, and store the result in the `models` variable.
