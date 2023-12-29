
## Services Directory

The `services` directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation codebase. It contains TypeScript files that define custom React hooks, which are used to handle API calls and error messages within the application. These hooks are integral to the functioning of the chatbot UI, as they facilitate communication with the backend and ensure that any errors encountered during this process are handled appropriately and communicated to the user in a clear, localized manner.

### Contents

The `services` directory contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService`. This hook uses the `useTranslation` hook from `next-i18next` to provide localized error messages. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.
- `useApiService.ts`: This file defines a custom React hook named `useApiService`. This hook uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint.

### Key Components

The `services` directory contains two key TypeScript files:

- `errorService.ts`: The `useErrorService` hook defined in this file is crucial for handling errors in the application. It provides a function `getModelsError` that takes an error object and returns an `ErrorMessage` object. This object contains a title, status code, and list of messages, which are translated using the `useTranslation` hook. This ensures that error messages are localized and user-friendly.
- `useApiService.ts`: The `useApiService` hook defined in this file is essential for making API calls within the application. It uses the `useFetch` hook to make these calls and provides a function `getModels` that makes a POST request to the `/api/models` endpoint. This function is used to fetch data from the backend, making it a key part of the data flow in the application.

### Usage & Examples

The `services` directory is used to handle API calls and error messages within the application. The hooks defined in this directory are used throughout the codebase, facilitating communication with the backend and ensuring that any errors encountered during this process are handled appropriately.

For instance, the `useApiService` hook might be used in a component to fetch data from the backend. The `getModels` function provided by this hook could be used to make a POST request to the `/api/models` endpoint, passing in an object of type `GetModelsRequestProps` as a parameter. The result of this fetch operation would then be used to update the state of the component.

Similarly, the `useErrorService` hook might be used in a component to handle errors. The `getModelsError` function provided by this hook could be used to process an error object, returning an `ErrorMessage` object with a title, status code, and list of messages. These messages would then be displayed to the user, providing them with clear, localized information about the error.
