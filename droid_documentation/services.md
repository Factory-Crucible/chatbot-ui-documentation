
## Services Directory

The Services directory is a crucial part of the Factory-Crucible/chatbot-ui-documentation repository. It houses two TypeScript files, `errorService.ts` and `useApiService.ts`, which define custom React hooks that are integral to the functioning of the chatbot UI. These hooks are responsible for handling errors and making API calls respectively, thus playing a significant role in the user interface and functionality of the chatbot.

### Contents

The Services directory is a simple, flat structure with no subdirectories. It contains two TypeScript files:

- `errorService.ts`: This file exports a custom React hook named `useErrorService` that provides localized error messages. It uses the `useTranslation` hook from `next-i18next` to translate error messages based on the user's locale. The hook returns a function `getModelsError` that takes an error object and returns an `ErrorMessage` object with a title, status code, and list of messages.
- `useApiService.ts`: This file defines a custom React hook named `useApiService` that uses another custom hook `useFetch` to make API calls. The hook provides a function `getModels` which makes a POST request to the `/api/models` endpoint. The function accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters.

### Key Components

The key components of the Services directory are the two TypeScript files, `errorService.ts` and `useApiService.ts`. These files define custom React hooks that are used throughout the codebase.

- `errorService.ts`: The `useErrorService` hook defined in this file is crucial for providing localized error messages to the user. It uses the `useTranslation` hook from `next-i18next` to translate error messages based on the user's locale. This ensures that the user interface is accessible and user-friendly, regardless of the user's language.
- `useApiService.ts`: The `useApiService` hook defined in this file is responsible for making API calls. It uses another custom hook `useFetch` to make these calls. This hook is integral to the functioning of the chatbot UI, as it enables the application to communicate with the backend and retrieve necessary data.

### Usage & Examples

The files in the Services directory are used throughout the codebase to handle errors and make API calls.

- `errorService.ts`: The `useErrorService` hook is used whenever an error occurs in the application. It takes an error object as a parameter and returns an `ErrorMessage` object with a title, status code, and list of messages. The title and messages are translated using the `useTranslation` hook, ensuring that the error messages are displayed in the user's locale.
- `useApiService.ts`: The `useApiService` hook is used to make API calls. It provides a function `getModels` which makes a POST request to the `/api/models` endpoint. This function is used whenever the application needs to retrieve data from the backend. It accepts an object of type `GetModelsRequestProps` and an optional `AbortSignal` as parameters, and returns the result of the fetch operation.
