
## Services Directory

The `services` directory in the Factory-Crucible/chatbot-ui-documentation codebase is a crucial part of the project's architecture. It houses two TypeScript files that define custom React hooks, `useErrorService` and `useApiService`, which are integral to the application's error handling and API interaction respectively. These hooks encapsulate complex functionality, providing a clean and reusable interface for other parts of the codebase. The `services` directory does not contain any subdirectories, keeping its structure simple and focused.

### Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService`. The hook leverages the `useTranslation` hook from `next-i18next` to provide localized error messages. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages. The title and messages are translated using the `useTranslation` hook.

- `useApiService.ts`: This file defines a custom React hook named `useApiService`. The hook uses another custom hook `useFetch` to make API calls. It provides a function `getModels` which makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters. The `GetModelsRequestProps` interface is also defined in this file.

### Key Components

The `services` directory contains two key TypeScript files:

- `errorService.ts`: The `useErrorService` hook defined in this file is a critical part of the application's error handling mechanism. By providing localized error messages, it enhances the user experience and aids in debugging. The `getModelsError` function it returns is used throughout the codebase to handle errors from the `getModels` API call.

- `useApiService.ts`: The `useApiService` hook defined in this file is central to the application's interaction with the API. It encapsulates the logic for making a POST request to the `/api/models` endpoint, providing a clean and reusable interface for this operation. The `getModels` function it provides is used in various parts of the codebase to fetch model data from the API.

### Usage & Examples

The `useErrorService` and `useApiService` hooks defined in the `services` directory are used throughout the codebase to handle errors and interact with the API respectively.

For instance, the `useErrorService` hook might be used in a component as follows:

```typescript
import useErrorService from '../services/errorService';

const MyComponent = () => {
  const { getModelsError } = useErrorService();

  // ... code to make API call and handle error
  const error = // ... code to get error from API call
  const errorMessage = getModelsError(error);

  // ... code to display error message
};
```

Similarly, the `useApiService` hook might be used in a component like this:

```typescript
import useApiService from '../services/useApiService';

const MyComponent = () => {
  const { getModels } = useApiService();

  // ... code to make API call and handle response
  const response = getModels({ key: 'myKey' });

  // ... code to handle response
};
```

These examples illustrate typical usage patterns for the hooks defined in the `services` directory. They show how these hooks encapsulate complex functionality, providing a clean and reusable interface for other parts of the codebase.
