
## Services Directory

The `services` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation codebase. It houses two TypeScript files, `errorService.ts` and `useApiService.ts`, which define custom React hooks that are used throughout the project. These hooks provide functionality for handling errors and making API calls, respectively. The hooks are designed to be reusable and modular, allowing them to be easily integrated into various parts of the codebase.

### Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService`. The hook uses the `useTranslation` hook from `next-i18next` to provide localized error messages. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.

- `useApiService.ts`: This file defines a custom React hook named `useApiService`. The hook uses another custom hook `useFetch` to make API calls. It provides a function `getModels` which makes a POST request to the `/api/models` endpoint.

### Key Components

The `services` directory contains two key components:

- `useErrorService`: This custom React hook is a critical part of the error handling mechanism in the codebase. It provides a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages. The title and messages are translated using the `useTranslation` hook, providing localized error messages.

- `useApiService`: This custom React hook is used to make API calls throughout the codebase. It uses the `useFetch` hook to make these calls and provides a function `getModels` that makes a POST request to the `/api/models` endpoint.

### Usage & Examples

The hooks defined in the `services` directory are used throughout the codebase to handle errors and make API calls.

For example, the `useErrorService` hook might be used in a component like this:

```typescript
import useErrorService from '../services/errorService';

const MyComponent = () => {
  const { getModelsError } = useErrorService();
  // ...
  try {
    // Some code that might throw an error
  } catch (error) {
    const errorMessage = getModelsError(error);
    // Display the error message to the user
  }
  // ...
};
```

Similarly, the `useApiService` hook might be used in a component like this:

```typescript
import useApiService from '../services/useApiService';

const MyComponent = () => {
  const { getModels } = useApiService();
  // ...
  useEffect(() => {
    const fetchData = async () => {
      const data = await getModels({ key: 'myKey' });
      // Do something with the data
    };
    fetchData();
  }, []);
  // ...
};
```

These examples demonstrate how the hooks defined in the `services` directory can be used to handle errors and make API calls in a reusable and modular way.
