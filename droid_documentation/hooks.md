
## Hooks Directory

The `hooks` directory is a collection of custom React hooks, specifically designed to handle state management and HTTP requests within the codebase. It contains two TypeScript files: `useCreateReducer.ts` and `useFetch.ts`. These hooks are integral to the application's state management and data fetching capabilities, respectively.

### Contents

The `hooks` directory contains the following files:

- `useCreateReducer.ts`: This file defines a custom React hook, `useCreateReducer`, and two TypeScript types, `FieldNames` and `ActionType`. The hook is designed to create a reducer with typed dispatch and state, taking an object with an `initialState` property as an argument. The `FieldNames` type extracts property names from the initial state of the reducer, while `ActionType` defines the action type for the dispatch object.
- `useFetch.ts`: This file exports a custom React hook, `useFetch`, for making HTTP requests. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The `useFetch` hook returns an object with methods for each HTTP verb (get, post, put, patch, delete). Each method uses a helper function `handleFetch` to perform the actual fetch operation.

### Key Components

- `useCreateReducer`: This hook is a key component in managing state within the application. It provides a typed reducer with dispatch and state, optimizing performance with `useReducer` and `useMemo` from React.
- `useFetch`: This hook is crucial for data fetching within the application. It provides methods for each HTTP verb, handling the construction of the request URL, body, and headers, and the response based on its content type. It also handles errors and throws them for further handling.

### Usage & Examples

- `useCreateReducer`: This hook is used to create a reducer with typed dispatch and state. It takes an object with an `initialState` property as an argument. The `FieldNames` and `ActionType` types are used to manage the reducer's initial state and dispatch action.
- `useFetch`: This hook is used for making HTTP requests. It returns an object with methods for each HTTP verb. Each method uses the `handleFetch` helper function to perform the actual fetch operation, handling the construction of the request URL, body, and headers, and the response based on its content type.
