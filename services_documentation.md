
## Services Directory

The `services` directory plays a crucial role in the `integration-chatbot-ui` project. It contains service-related TypeScript files that provide functionalities such as API interactions and error handling. These services are encapsulated within custom React hooks, allowing them to be easily consumed by other parts of the application. The directory is a part of the service layer of the application, which is responsible for business logic and interactions with the backend.

### Contents

The `services` directory contains the following TypeScript files:

- `useApiService.ts`: This file exports a custom React hook that provides an API service for fetching data. It uses a custom `useFetch` hook for HTTP requests and defines a `getModels` function for making POST requests to the `/api/models` endpoint.

- `errorService.ts`: This file defines a custom React hook that provides localized error messages. It uses the `next-i18next` library for localization and returns a `getModelsError` method that takes an error object and returns a localized `ErrorMessage` object or null.

### Folder Structure Overview

The `services` directory is a flat structure with no subdirectories. It contains TypeScript files that define custom React hooks for various services. Each file is named after the service it provides and exports a default function that returns the service. The services are designed to be reusable and are optimized for performance using hooks like `useCallback` and `useMemo`.

### Key Components

The `services` directory contains two key TypeScript files:

- [`useApiService.ts`](https://github.com/Factory-Crucible/integration-chatbot-ui/blob/main/services/useApiService.ts): This file is a part of the service layer of the application. It provides an API service for fetching data, using a custom `useFetch` hook for HTTP requests. The `getModels` function it defines is critical for interacting with the backend.

- [`errorService.ts`](https://github.com/Factory-Crucible/integration-chatbot-ui/blob/main/services/errorService.ts): This file provides localized error messages using the `next-i18next` library. The `getModelsError` method it returns is essential for handling errors in a user-friendly manner.

### Usage & Examples

The services provided by the `services` directory are used throughout the `integration-chatbot-ui` project. For instance, the `useApiService` hook can be used in a React component to fetch data from the backend:

```typescript
import useApiService from '@/services/useApiService';

const MyComponent = () => {
  const { getModels } = useApiService();
  // Use getModels to fetch data
};
```

Similarly, the `useErrorService` hook can be used to handle errors and display localized error messages:

```typescript
import useErrorService from '@/services/errorService';

const MyComponent = () => {
  const { getModelsError } = useErrorService();
  // Use getModelsError to handle errors
};
```
