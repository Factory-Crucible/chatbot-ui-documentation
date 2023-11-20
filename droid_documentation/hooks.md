
## Hooks Directory

The Hooks directory is a specialized section of the codebase dedicated to housing custom React hooks. These hooks, written in TypeScript, provide reusable logic that can be utilized across the application. The directory contains two key files: `useCreateReducer.ts` and `useFetch.ts`. The `useCreateReducer.ts` file defines a custom hook for creating a typed reducer with dispatch and state, while the `useFetch.ts` file exports a custom hook for making HTTP requests. These hooks are designed to streamline state management and HTTP requests, respectively, and are integral to the application's functionality.

### Contents

The Hooks directory is composed of two TypeScript files:

1. `useCreateReducer.ts`: This file defines a custom React hook, `useCreateReducer`, which is designed to create a reducer with typed dispatch and state. It also defines two TypeScript types, `FieldNames` and `ActionType`, which are used to manage the reducer's initial state and dispatch action.

2. `useFetch.ts`: This file exports a custom React hook, `useFetch`, which is used for making HTTP requests. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The hook provides methods for each HTTP verb and uses a helper function, `handleFetch`, to perform the actual fetch operation.

### Key Components

The Hooks directory contains two critical files that define custom hooks:

- `useCreateReducer.ts`: The `useCreateReducer` hook defined in this file is a key component in state management within the application. By creating a typed reducer with dispatch and state, it provides a robust and type-safe way to manage state changes. The `FieldNames` and `ActionType` types further enhance the type safety and predictability of the reducer.

- `useFetch.ts`: The `useFetch` hook defined in this file is crucial for making HTTP requests within the application. By providing methods for each HTTP verb and handling the construction of the request and response, it simplifies the process of making requests and handling responses. The `RequestModel` and `RequestWithBodyModel` types ensure that the request parameters are structured correctly.

### Usage & Examples

The hooks defined in the Hooks directory are used throughout the application to manage state and make HTTP requests.

- `useCreateReducer`: This hook is used when there is a need to manage complex state with a reducer. It provides a type-safe way to define the reducer's initial state and dispatch actions. For example, it could be used to manage the state of a form, with different actions for each form field.

- `useFetch`: This hook is used whenever an HTTP request needs to be made. It provides a simple and consistent way to make requests and handle responses. For example, it could be used to fetch data from an API, post data to an API, or delete data from an API.
