
## Hooks Directory

The `hooks` directory is a specialized section of the codebase dedicated to housing custom React hooks. These hooks, defined in TypeScript, are designed to provide reusable stateful logic and side effects that can be shared across multiple components in the project. The directory contains two files, `useCreateReducer.ts` and `useFetch.ts`, each defining a unique hook that serves a specific purpose in the application.

### Contents

The `hooks` directory is composed of two TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook named `useCreateReducer`. The hook is designed to create a reducer with typed dispatch and state, taking an object with an `initialState` property as an argument. The file also defines two TypeScript types: `FieldNames` and `ActionType`. `FieldNames` extracts property names from the initial state of the reducer, while `ActionType` defines the action type for the dispatch object. The hook uses `useReducer` and `useMemo` from React to manage state and optimize performance.

- `useFetch.ts`: This file exports a custom React hook for making HTTP requests named `useFetch`. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The `useFetch` hook returns an object with methods for each HTTP verb (get, post, put, patch, delete). Each method uses a helper function `handleFetch` to perform the actual fetch operation. The `handleFetch` function takes care of constructing the request URL, body, and headers, and handles the response based on its content type. It also handles errors and throws them for further handling.

### Key Components

The `hooks` directory contains two key components:

- `useCreateReducer`: This custom hook is a critical part of the state management strategy in the application. By providing a typed reducer with dispatch and state, it ensures type safety and predictability in state updates. The `FieldNames` and `ActionType` types defined in this file are integral to the functioning of the `useCreateReducer` hook, providing the necessary structure for the reducer's initial state and dispatch action.

- `useFetch`: This custom hook is central to the application's interaction with external APIs. It provides a structured and reusable way to make HTTP requests, handling the construction of the request and the processing of the response. The `RequestModel` and `RequestWithBodyModel` types defined in this file provide a structured way to specify request parameters, ensuring consistency and predictability in the application's interactions with external APIs.

### Usage & Examples

The hooks defined in the `hooks` directory are used throughout the codebase to manage state and interact with external APIs.

- `useCreateReducer` is used in components that require state management. For example, a component that manages a list of items might use `useCreateReducer` to manage the list's state, providing an `initialState` that includes the list and actions for adding, removing, and updating items.

- `useFetch` is used in components that need to interact with external APIs. For example, a component that displays data from an external API might use `useFetch` to make the API request, using the `get` method to retrieve the data and handling the response in the component.

These examples are representative of typical usage patterns, but the actual usage of these hooks will depend on the specific requirements of the components in which they are used.
