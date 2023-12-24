
# Hooks Directory Documentation

The `hooks` directory is a specialized section of the codebase that houses custom React hooks. These hooks are designed to provide reusable stateful logic and side effects, which can be used across different components in the project. The hooks in this directory are written in TypeScript, providing static typing and enhancing code quality and maintainability. The directory contains two files: `useCreateReducer.ts` and `useFetch.ts`. These files define the `useCreateReducer` and `useFetch` hooks respectively, each serving a unique purpose in the codebase.

## Contents

The `hooks` directory contains two TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook named `useCreateReducer`. This hook is designed to create a reducer with typed dispatch and state. It also defines two TypeScript types: `FieldNames` and `ActionType`.
- `useFetch.ts`: This file exports a custom React hook for making HTTP requests named `useFetch`. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The `useFetch` hook returns an object with methods for each HTTP verb.

## Key Components

The `hooks` directory contains two key components:

- `useCreateReducer` Hook: This hook is designed to create a reducer with typed dispatch and state. It takes an object with an `initialState` property as an argument. The hook uses `useReducer` and `useMemo` from React to manage state and optimize performance. The `FieldNames` and `ActionType` types defined in this file are used to extract property names from the initial state of the reducer and define the action type for the dispatch object respectively.
- `useFetch` Hook: This hook is designed to make HTTP requests. It defines `RequestModel` and `RequestWithBodyModel` types to structure the request parameters. The hook returns an object with methods for each HTTP verb (get, post, put, patch, delete). Each method uses a helper function `handleFetch` to perform the actual fetch operation. The `handleFetch` function takes care of constructing the request URL, body, and headers, and handles the response based on its content type. It also handles errors and throws them for further handling.

## Usage & Examples

The hooks defined in this directory are used across the codebase to manage state and side effects in a reusable manner.

- `useCreateReducer` Hook: This hook is used when there is a need to manage complex state logic that involves multiple sub-values or when the next state depends on the previous one. It provides a more flexible alternative to `useState` that is more suited to complex state logic.
- `useFetch` Hook: This hook is used to make HTTP requests throughout the application. It provides a clean and reusable way to handle API calls, taking care of request construction, response handling, and error handling. It can be used in any component that needs to fetch data from an API.

Please note that the skeleton code provided in the DIRECTORY_STRUCTURE is not representative of typical usage patterns. For actual usage examples, refer to the specific components where these hooks are used.
