
## Services Directory

The `services` directory is a critical part of the Factory-Crucible/chatbot-ui-documentation repository. It houses two TypeScript files that define custom React hooks, `useErrorService` and `useApiService`. These hooks play a significant role in the application's data flow and interactions, providing localized error messages and making API calls respectively. The `services` directory does not contain any subdirectories.

### Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages using the `useTranslation` hook. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.

- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses `useFetch` to make API calls. It provides a function `getModels` that makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal`.

### Key Components

The `services` directory contains two key TypeScript files:

- `errorService.ts`: The `useErrorService` hook in this file is crucial for providing localized error messages. The `getModelsError` function it returns is used throughout the application to handle errors and provide user-friendly messages.

- `useApiService.ts`: The `useApiService` hook in this file is essential for making API calls. The `getModels` function it provides is used to make a POST request to the `/api/models` endpoint, which is a critical part of the application's data flow.

### Usage & Examples

The `useErrorService` and `useApiService` hooks defined in the `services` directory are used throughout the application to handle errors and make API calls respectively.

For instance, the `useErrorService` hook might be used in a component like this:

```typescript
import useErrorService from '../services/errorService';

const Component = () => {
  const { getModelsError } = useErrorService();
  // ... component logic
  // ... handle error using getModelsError
};
```

Similarly, the `useApiService` hook might be used in a component like this:

```typescript
import useApiService from '../services/useApiService';

const Component = () => {
  const { getModels } = useApiService();
  // ... component logic
  // ... make API call using getModels
};
```

These examples are representative of typical usage patterns, but the actual usage may vary depending on the specific requirements of the component or module.
