
## Hooks Directory

The `hooks` directory is a specialized section of the codebase dedicated to housing custom React hooks. These hooks are integral to the project's state management and HTTP request handling. The directory contains two TypeScript files: `useCreateReducer.ts` and `useFetch.ts`. Each of these files defines a custom hook that encapsulates a specific functionality, providing a reusable and efficient way to manage state and perform HTTP requests within the codebase.

### Contents

The `hooks` directory contains the following TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook named `useCreateReducer`. The hook is designed to create a reducer with typed dispatch and state, taking an object with an `initialState` property as an argument. The file also defines two TypeScript types: `FieldNames` and `ActionType`. `FieldNames` extracts property names from the initial state of the reducer, while `ActionType` defines the action type for the dispatch object.
- `useFetch.ts`: This file exports a custom React hook for making HTTP requests named `useFetch`. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The `useFetch` hook returns an object with methods for each HTTP verb (get, post, put, patch, delete). Each method uses a helper function `handleFetch` to perform the actual fetch operation.

### Key Components

The `hooks` directory contains two key components:

- `useCreateReducer` Hook: This hook is a critical part of the state management in the codebase. It provides a typed reducer with dispatch and state, ensuring type safety and reducing potential errors during development. The `FieldNames` and `ActionType` types defined in the same file further enhance the type safety by providing specific types for the reducer's initial state and dispatch action.
- `useFetch` Hook: This hook is central to the HTTP request handling in the codebase. It provides a structured and reusable way to make HTTP requests, with methods for each HTTP verb. The `RequestModel` and `RequestWithBodyModel` types defined in the same file provide a structured way to define request parameters, ensuring consistency across different parts of the codebase.

### Usage & Examples

The hooks defined in the `hooks` directory are used throughout the codebase to manage state and perform HTTP requests.

- `useCreateReducer` Hook: This hook is used to create a reducer with typed dispatch and state. For example, it can be used to manage the state of a form, with the `initialState` object defining the initial state of the form fields, and the dispatch actions updating the state based on user input.
- `useFetch` Hook: This hook is used to make HTTP requests. For example, it can be used to fetch data from an API, with the `get` method making a GET request to the API endpoint, and the response being used to update the state of the application.

Please note that the above examples are illustrative and may not represent the exact usage patterns in the codebase.
