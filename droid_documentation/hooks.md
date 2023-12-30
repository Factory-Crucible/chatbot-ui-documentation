
## hooks

The `hooks` directory is dedicated to the creation and management of custom React hooks. These hooks are used throughout the codebase to encapsulate and manage state and side effects in a reusable manner. The directory contains two TypeScript files: `useCreateReducer.ts` and `useFetch.ts`.

### Contents

The `hooks` directory contains the following files:

- `useCreateReducer.ts`: This file defines a custom React hook, `useCreateReducer`, and two TypeScript types, `FieldNames` and `ActionType`. The hook is designed to create a reducer with typed dispatch and state.
- `useFetch.ts`: This file exports a custom React hook, `useFetch`, for making HTTP requests. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The hook provides methods for each HTTP verb.

### Key Components

- `useCreateReducer.ts`: The `useCreateReducer` hook is a key component in managing state within the application. It provides a typed reducer with dispatch and state, enhancing type safety and reducing potential errors. The `FieldNames` and `ActionType` types are used to manage the reducer's initial state and dispatch action.
- `useFetch.ts`: The `useFetch` hook is a critical component for making HTTP requests within the application. It provides a structured and reusable way to make requests and handle responses, including error handling.

### Usage & Examples

- `useCreateReducer.ts`: The `useCreateReducer` hook is used to create a reducer with typed dispatch and state. It takes an object with an `initialState` property as an argument. The `FieldNames` and `ActionType` types are used to extract property names from the initial state and define the action type for the dispatch object.
- `useFetch.ts`: The `useFetch` hook is used to make HTTP requests. It returns an object with methods for each HTTP verb (get, post, put, patch, delete). Each method uses a helper function `handleFetch` to perform the actual fetch operation. The `handleFetch` function constructs the request URL, body, and headers, and handles the response based on its content type. It also handles errors and throws them for further handling.
