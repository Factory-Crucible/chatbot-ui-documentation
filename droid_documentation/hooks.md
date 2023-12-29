
## Hooks Directory

The `hooks` directory is a dedicated space for custom React hooks that are used across the `chatbot-ui` project. These hooks encapsulate shared logic that can be reused across multiple components, promoting code reusability and maintainability. The directory contains two TypeScript files: `useCreateReducer.ts` and `useFetch.ts`. These files define hooks that manage state and handle HTTP requests, respectively.

### Contents

The `hooks` directory contains the following TypeScript files:

- `useCreateReducer.ts`: This file defines a custom React hook named `useCreateReducer` that creates a reducer with typed dispatch and state. It also defines two TypeScript types: `FieldNames` and `ActionType` that are used to manage the reducer's initial state and dispatch action.

- `useFetch.ts`: This file exports a custom React hook named `useFetch` for making HTTP requests. It defines two types, `RequestModel` and `RequestWithBodyModel`, to structure the request parameters. The `useFetch` hook provides methods for each HTTP verb (get, post, put, patch, delete), and uses a helper function `handleFetch` to perform the actual fetch operation.

### Key Components

The `hooks` directory contains two key TypeScript files:

- `useCreateReducer.ts`: The `useCreateReducer` hook is a critical part of the state management strategy in the `chatbot-ui` project. It provides a typed interface for creating reducers, which are used to manage complex state in the application. The `FieldNames` and `ActionType` types defined in this file are used to ensure type safety when defining the initial state and dispatch actions for the reducer.

- `useFetch.ts`: The `useFetch` hook is a central part of the HTTP request handling in the `chatbot-ui` project. It provides a unified interface for making HTTP requests, with methods for each HTTP verb. The `RequestModel` and `RequestWithBodyModel` types defined in this file are used to structure the request parameters, ensuring type safety and consistency across all HTTP requests made in the application.

### Usage & Examples

The hooks defined in the `hooks` directory are used throughout the `chatbot-ui` project to manage state and handle HTTP requests.

For example, the `useCreateReducer` hook might be used in a component to manage its local state. The hook would be invoked with an object containing the initial state, and it would return a state object and a dispatch function. The dispatch function could then be used to update the state in response to user interactions or other events.

The `useFetch` hook might be used in a component to fetch data from an API. The hook would be invoked without any arguments, and it would return an object with methods for each HTTP verb. These methods could then be used to make HTTP requests to the API, with the request parameters structured according to the `RequestModel` or `RequestWithBodyModel` types.
