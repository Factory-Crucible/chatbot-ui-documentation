
## Hooks Directory

The `hooks` directory is a specialized section of the codebase that houses custom React hooks. These hooks are designed to encapsulate and manage specific aspects of state and side effects within the application. The directory contains two TypeScript files, `useCreateReducer.ts` and `useFetch.ts`, each defining a unique hook that is utilized across the application. These hooks are integral to the application's state management and HTTP request handling, providing a structured and reusable approach to these common tasks.

### Contents

The `hooks` directory is composed of two TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook named `useCreateReducer`. The hook is designed to create a reducer with typed dispatch and state, taking an object with an `initialState` property as an argument. The file also defines two TypeScript types, `FieldNames` and `ActionType`, which are used to manage the reducer's initial state and dispatch action.

- `useFetch.ts`: This file exports a custom React hook for making HTTP requests, named `useFetch`. The hook provides methods for each HTTP verb (get, post, put, patch, delete), and uses a helper function `handleFetch` to perform the actual fetch operation. The file also defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters.

### Key Components

The `hooks` directory contains two key components:

- `useCreateReducer`: This custom hook is a critical part of the application's state management strategy. It provides a typed reducer with dispatch and state, allowing for a structured and type-safe approach to managing state within the application. The hook uses `useReducer` and `useMemo` from React to manage state and optimize performance.

- `useFetch`: This custom hook is central to the application's HTTP request handling. It provides a structured and reusable approach to making HTTP requests, with methods for each HTTP verb. The hook uses a helper function `handleFetch` to construct the request and handle the response, including error handling.

### Usage & Examples

The hooks defined in this directory are used throughout the application to manage state and handle HTTP requests.

- `useCreateReducer`: This hook is used when a reducer with typed dispatch and state is required. It takes an object with an `initialState` property as an argument. The `FieldNames` and `ActionType` types are used to manage the reducer's initial state and dispatch action.

```typescript
const { state, dispatch } = useCreateReducer({ initialState: { count: 0 } });
```

- `useFetch`: This hook is used to make HTTP requests. It provides methods for each HTTP verb, and uses a helper function `handleFetch` to perform the actual fetch operation. The `RequestModel` and `RequestWithBodyModel` types are used to structure the request parameters.

```typescript
const { get, post } = useFetch();
const data = await get('/api/data');
const response = await post('/api/data', { body: { key: 'value' } });
```

Please note that these code snippets are simplified examples and may not represent the full complexity and usage patterns of the hooks in the actual application.
