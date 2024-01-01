
# Services Directory

The `services` directory is a critical part of the Factory-Crucible/chatbot-ui-documentation repository. It houses two TypeScript files, `errorService.ts` and `useApiService.ts`, which define custom React hooks that provide essential functionalities to the chatbot-ui project. These hooks are responsible for handling API calls and managing error messages, respectively. 

## Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages using the `useTranslation` hook from `next-i18next`. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages. 
- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.

## Key Components

The `services` directory contains two key TypeScript files:

- `errorService.ts`: The `useErrorService` hook defined in this file is crucial for providing localized error messages. It uses the `useTranslation` hook from `next-i18next` to translate error messages, ensuring that users receive error messages in their preferred language. The `getModelsError` function, which is returned by the `useErrorService` hook, takes an error object and returns an `ErrorMessage` object. This object contains a title, a status code, and a list of messages, providing comprehensive information about the error.
- `useApiService.ts`: The `useApiService` hook defined in this file is responsible for making API calls. It uses the `useFetch` hook to make these calls, abstracting the complexity of fetch operations. The `getModels` function, which is provided by the `useApiService` hook, makes a POST request to the `/api/models` endpoint. This function is essential for fetching models from the API.

## Usage & Examples

The `services` directory is used to manage API calls and error messages in the chatbot-ui project. The `useErrorService` hook is used to provide localized error messages. For example, when an error occurs while fetching models from the API, the `getModelsError` function can be used to generate an `ErrorMessage` object with a title, status code, and list of messages.

The `useApiService` hook is used to make API calls. For instance, when the application needs to fetch models from the API, the `getModels` function can be used. This function makes a POST request to the `/api/models` endpoint, accepting an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.

```typescript
// Example usage of useErrorService hook
const { getModelsError } = useErrorService();
const error = getModelsError(someErrorObject);

// Example usage of useApiService hook
const { getModels } = useApiService();
const models = getModels({ key: 'someKey' });
```

Note: The above code snippets are examples and may not represent the actual usage in the codebase.
