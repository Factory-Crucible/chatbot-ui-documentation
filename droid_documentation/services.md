
## Services Directory

The `services` directory houses two TypeScript files, `errorService.ts` and `useApiService.ts`. These files define custom React hooks that provide functionality for error handling and API service respectively. The hooks are designed to be reusable across the codebase, encapsulating specific functionalities related to error messages and API calls.

### Contents

The `services` directory contains the following files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService`. The hook uses the `useTranslation` hook from `next-i18next` to provide localized error messages. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.
- `useApiService.ts`: This file defines a custom React hook named `useApiService`. The hook uses another custom hook `useFetch` to make API calls. It provides a function `getModels` which makes a POST request to the `/api/models` endpoint.

### Key Components

- `useErrorService` Hook: This hook is crucial for providing localized error messages throughout the application. It returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object. This allows for consistent error handling across the application.
- `useApiService` Hook: This hook is responsible for making API calls within the application. It provides a function `getModels` that makes a POST request to the `/api/models` endpoint. This encapsulates the API call logic, making it reusable and maintainable.

### Usage & Examples

The hooks defined in the `services` directory are used throughout the application to handle errors and make API calls.

For instance, the `useErrorService` hook can be used in a component to handle errors from an API call:

```typescript
const { getModelsError } = useErrorService();
const error = getModelsError(apiError);
```

Similarly, the `useApiService` hook can be used to make API calls:

```typescript
const { getModels } = useApiService();
const models = getModels({ key: 'example' });
```

These examples demonstrate typical usage patterns of the hooks defined in the `services` directory.
