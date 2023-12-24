
## Services Directory

The `services` directory is a critical part of the Factory-Crucible/chatbot-ui-documentation codebase. It houses two TypeScript files that define custom React hooks, `useErrorService` and `useApiService`, which are integral to the application's error handling and API interaction respectively. These hooks encapsulate complex functionalities, providing a clean and reusable interface for other parts of the codebase.

### Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages. It leverages the `useTranslation` hook from `next-i18next` to ensure the error messages are appropriate for the user's locale. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.

- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint. The `getModels` function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.

### Key Components

The `services` directory contains two key TypeScript files:

- `errorService.ts`: The `useErrorService` hook defined in this file is crucial for providing localized error messages to the user. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object. This object contains a title, a status code, and a list of messages, all of which are translated using the `useTranslation` hook. This ensures that the error messages are understandable to the user, regardless of their locale.

- `useApiService.ts`: The `useApiService` hook defined in this file is essential for making API calls within the application. It uses the `useFetch` hook to make these calls and provides a function `getModels` that makes a POST request to the `/api/models` endpoint. This function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters. The `GetModelsRequestProps` interface is also defined in this file, which expects a `key` of type string.

### Usage & Examples

The `services` directory is used to encapsulate complex functionalities related to error handling and API interaction. The hooks defined in this directory are used throughout the codebase, providing a clean and reusable interface for these functionalities.

For instance, the `useErrorService` hook can be used in a component to provide localized error messages. Here's a simplified example of how it might be used:

```typescript
import useErrorService from '../services/errorService';

const MyComponent = () => {
  const { getModelsError } = useErrorService();
  // ... other code
  const error = getModelsError(someErrorObject);
  // ... handle error
};
```

Similarly, the `useApiService` hook can be used to make API calls. Here's a simplified example of how it might be used:

```typescript
import useApiService from '../services/useApiService';

const MyComponent = () => {
  const { getModels } = useApiService();
  // ... other code
  const models = getModels({ key: 'someKey' });
  // ... handle models
};
```

Please note that these examples are simplified and may not represent the actual usage in the codebase. Always refer to the actual code for accurate usage patterns.
