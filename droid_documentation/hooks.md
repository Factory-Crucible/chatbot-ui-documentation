
## Hooks Directory

The Hooks directory is a critical part of the Factory-Crucible/chatbot-ui-documentation repository, serving as the home for custom React hooks used throughout the project. These hooks, defined in TypeScript, provide reusable logic that can be used across multiple components, enhancing the modularity and maintainability of the codebase. The hooks defined in this directory are `useCreateReducer` and `useFetch`, each encapsulating distinct functionalities that are integral to the application's data management and HTTP communication.

### Contents

The Hooks directory contains two TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook, `useCreateReducer`, which is used to create a typed reducer with dispatch and state. It also defines two types, `FieldNames` and `ActionType`, which are used to manage the reducer's initial state and dispatch action.

- `useFetch.ts`: This file exports a custom React hook, `useFetch`, which is used for making HTTP requests. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters and provides methods for each HTTP verb.

### Key Components

The Hooks directory contains two key components:

- `useCreateReducer`: This hook is a critical part of the state management in the application. It creates a typed reducer with dispatch and state, enhancing the type safety and predictability of the state changes. The `FieldNames` and `ActionType` types defined in this file are used to manage the reducer's initial state and dispatch action, providing a structured and type-safe way to handle state changes.

- `useFetch`: This hook is central to the application's communication with external APIs. It provides a structured and reusable way to make HTTP requests, with methods for each HTTP verb. The `RequestModel` and `RequestWithBodyModel` types defined in this file structure the request parameters, ensuring that all requests adhere to a consistent format. The `handleFetch` helper function within `useFetch` constructs the request and handles the response, including error handling, providing a centralized location for HTTP communication logic.

### Usage & Examples

The hooks defined in this directory are used throughout the application to manage state and make HTTP requests.

- `useCreateReducer` is used in components that need to manage complex state. For example, it could be used in a component that manages a form with multiple fields. The `FieldNames` type can be used to extract the property names from the initial state of the reducer, and the `ActionType` type can be used to define the action type for the dispatch object.

- `useFetch` is used in components that need to communicate with external APIs. For example, it could be used in a component that fetches data from an API when the component mounts. The `get`, `post`, `put`, `patch`, and `delete` methods provided by `useFetch` can be used to make HTTP requests of the corresponding type. The `RequestModel` and `RequestWithBodyModel` types can be used to structure the request parameters.

Please note that the above examples are illustrative and not representative of actual usage in the codebase. The actual usage of these hooks depends on the specific requirements of the components in which they are used.
