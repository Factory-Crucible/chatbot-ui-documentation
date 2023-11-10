
## Hooks Directory

The `hooks` directory is a crucial part of the `integration-chatbot-ui` project. It contains custom React hooks that are used throughout the application to manage state and handle HTTP requests. These hooks are written in TypeScript, providing type safety and enhancing code readability and maintainability.

### Contents

The `hooks` directory contains two TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook named `useCreateReducer` and exports two types, `FieldNames` and `ActionType`. The `useCreateReducer` hook is designed to create a type-safe reducer, while the `FieldNames` and `ActionType` types are used for extracting property names from the reducer's initial state and defining the action type for the dispatch object, respectively.

- `useFetch.ts`: This file exports a custom hook named `useFetch` that simplifies making HTTP requests. It defines two types, `RequestModel` and `RequestWithBodyModel`, for structuring the request parameters, headers, and body. The `useFetch` hook provides five methods: `get`, `post`, `put`, `patch`, and `delete`, each returning a Promise after accepting a URL and a request object.

### Folder Structure Overview

The `hooks` directory is straightforward and does not contain any subdirectories. It directly houses the TypeScript files that define the custom hooks. This structure makes it easy to locate and manage the hooks used in the application.

### Key Components

The `hooks` directory contains two key components:

- [`useCreateReducer.ts`](./hooks/useCreateReducer.ts): This file is crucial for managing state in the application. It exports a custom hook that creates a type-safe reducer, enhancing the robustness of state management.

- [`useFetch.ts`](./hooks/useFetch.ts): This file is essential for handling HTTP requests in the application. It exports a custom hook that provides a simplified interface for making HTTP requests, improving code readability and maintainability.

### Usage & Examples

The hooks defined in this directory are used throughout the application to manage state and handle HTTP requests.

For instance, the `useCreateReducer` hook can be used to create a type-safe reducer as follows:

```typescript
import { useCreateReducer } from './hooks/useCreateReducer';

const { state, dispatch } = useCreateReducer({ initialState: { count: 0 } });

dispatch({ type: 'increment', payload: 1 });
```

Similarly, the `useFetch` hook can be used to make HTTP requests as follows:

```typescript
import { useFetch } from './hooks/useFetch';

const { get, post } = useFetch();

// GET request
const response = await get('https://api.example.com/data');

// POST request
const response = await post('https://api.example.com/data', { body: { key: 'value' } });
```
