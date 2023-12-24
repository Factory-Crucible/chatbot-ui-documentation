
## Hooks Directory

The `hooks` directory is a specialized section of the codebase that houses custom React hooks. These hooks are designed to encapsulate specific functionalities that are reused across different components of the chatbot-ui project. The hooks are written in TypeScript, providing type safety and enhancing code maintainability. The directory contains two files: `useCreateReducer.ts` and `useFetch.ts`. These files define hooks that manage state with a reducer and handle HTTP requests, respectively.

### Contents

The `hooks` directory is composed of two TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook, `useCreateReducer`, which is designed to create a reducer with typed dispatch and state. It also defines two TypeScript types, `FieldNames` and `ActionType`, which are used to manage the reducer's initial state and dispatch action.

- `useFetch.ts`: This file exports a custom React hook, `useFetch`, which is used for making HTTP requests. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The hook provides methods for each HTTP verb and uses a helper function, `handleFetch`, to perform the actual fetch operation.

### Key Components

The `hooks` directory contains two key components:

- `useCreateReducer`: This hook is a critical part of the state management system in the chatbot-ui project. It provides a way to create a reducer with typed dispatch and state, enhancing type safety and reducing the likelihood of runtime errors. The `FieldNames` and `ActionType` types defined in this file are used to manage the reducer's initial state and dispatch action, providing a structured and predictable way to manage state.

- `useFetch`: This hook is a central part of the HTTP request handling system in the chatbot-ui project. It provides a way to make HTTP requests with structured parameters and handles the response, including error handling. The `RequestModel` and `RequestWithBodyModel` types defined in this file provide a structured way to specify request parameters, enhancing code readability and maintainability.

### Usage & Examples

The hooks defined in this directory are used throughout the chatbot-ui project to manage state and handle HTTP requests.

- `useCreateReducer`: This hook is used when a component needs to manage complex state with a reducer. The hook takes an object with an `initialState` property as an argument and returns a reducer with typed dispatch and state. The `FieldNames` and `ActionType` types are used to manage the reducer's initial state and dispatch action.

- `useFetch`: This hook is used when a component needs to make HTTP requests. The hook provides methods for each HTTP verb (get, post, put, patch, delete), and each method uses the `handleFetch` helper function to perform the actual fetch operation. The `RequestModel` and `RequestWithBodyModel` types are used to structure the request parameters.

For example, a component might use the `useFetch` hook to make a GET request to an API endpoint:

```typescript
const { get } = useFetch();
const response = await get('/api/endpoint', { params: { key: 'value' } });
```

This example shows how the `useFetch` hook can be used to make a GET request with structured parameters. The `get` method returns a promise that resolves with the response from the API endpoint.
