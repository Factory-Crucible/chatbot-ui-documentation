
## Hooks Directory

The `hooks` directory is a specialized section of the codebase that houses two TypeScript files, each defining a custom React hook. These hooks, `useCreateReducer` and `useFetch`, play a crucial role in state management and HTTP request handling respectively. The hooks are designed to be reusable across the codebase, providing a standardized way to manage state and perform HTTP operations.

### Contents

The `hooks` directory contains two files:

- `useCreateReducer.ts`: This TypeScript file defines a custom React hook named `useCreateReducer`. It is designed to create a reducer with typed dispatch and state, providing a structured way to manage state in the application.
- `useFetch.ts`: This TypeScript file exports a custom React hook for making HTTP requests. It provides a structured way to perform HTTP operations, including GET, POST, PUT, PATCH, and DELETE requests.

### Key Components

The `hooks` directory houses two key components:

- `useCreateReducer`: This hook is designed to create a reducer with typed dispatch and state. It takes an object with an 'initialState' property as an argument. The file also defines two TypeScript types: 'FieldNames' and 'ActionType'. 'FieldNames' extracts property names from the initial state of the reducer, while 'ActionType' defines the action type for the dispatch object. The hook uses 'useReducer' and 'useMemo' from React to manage state and optimize performance.
- `useFetch`: This hook provides a structured way to perform HTTP operations. It defines two types, 'RequestModel' and 'RequestWithBodyModel', to structure the request parameters. The hook returns an object with methods for each HTTP verb (get, post, put, patch, delete). Each method uses a helper function 'handleFetch' to perform the actual fetch operation. The 'handleFetch' function takes care of constructing the request URL, body, and headers, and handles the response based on its content type. It also handles errors and throws them for further handling.

### Usage & Examples

The hooks defined in this directory are used throughout the codebase to manage state and perform HTTP operations.

- `useCreateReducer`: This hook is used to create a reducer with typed dispatch and state. It is typically used in components that require state management. For example, a component that manages user input might use this hook to create a reducer for the input state.
- `useFetch`: This hook is used to perform HTTP operations. It is typically used in components that need to fetch data from an API. For example, a component that displays user data might use this hook to fetch the data from a user API.

Please note that the code snippets provided in the DIRECTORY_STRUCTURE are not representative of typical usage patterns. They are provided to give a sense of the structure and functionality of the hooks, but they may not reflect the actual usage in the codebase.
