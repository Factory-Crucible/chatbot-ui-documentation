
# Services Directory

The `services` directory is a critical part of the chatbot-ui project, providing custom React hooks that facilitate API calls and error handling. It contains two TypeScript files, `errorService.ts` and `useApiService.ts`, each defining a custom hook that is used extensively throughout the codebase. These hooks encapsulate complex functionality, making it easier to maintain and understand the codebase.

## Contents

The `services` directory contains the following files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages. It uses the `useTranslation` hook from `next-i18next` to translate error messages. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.
- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.

## Key Components

The `services` directory contains two key components:

- `useErrorService`: This custom React hook is a critical part of the error handling mechanism in the chatbot-ui project. It provides a way to generate localized error messages, improving the user experience by providing clear and understandable error messages.
- `useApiService`: This custom React hook is a central part of the API interaction in the chatbot-ui project. It encapsulates the logic for making API calls, making it easier to manage and maintain the codebase.

## Usage & Examples

The hooks defined in the `services` directory are used throughout the chatbot-ui project. For example, the `useApiService` hook is used to make API calls, while the `useErrorService` hook is used to generate localized error messages.

The `useApiService` hook is typically used in the following way:

```typescript
const { getModels } = useApiService();
const models = getModels({ key: 'exampleKey' });
```

The `useErrorService` hook is typically used in the following way:

```typescript
const { getModelsError } = useErrorService();
const errorMessage = getModelsError(error);
```

These examples are representative of typical usage patterns, but the actual usage may vary depending on the specific requirements of the code.
