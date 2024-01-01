
# `types` Directory

The `types` directory is a critical part of the codebase, serving as the central location for TypeScript type definitions, interfaces, and constants that are used throughout the project. This directory provides a consistent structure for various parts of the project, including theme settings, key-value pair structures, prompt objects, Google's services, plugins, chat systems, environment variables for the OpenAI API, and the local storage schema for a chatbot UI. The types defined in this directory are integral to the static typing feature of TypeScript, which enhances code quality and maintainability.

## Contents

The `types` directory contains several TypeScript files, each defining specific types, interfaces, or constants that are used in different parts of the project. There are no subdirectories within this directory. The files in this directory include:

- `data.ts`: Defines the `KeyValuePair` interface, representing a key-value pair structure.
- `prompt.ts`: Defines the `Prompt` interface, representing a prompt object.
- `plugin.ts`: Defines the structure and data for plugins in the application.
- `settings.ts`: Defines the `Settings` interface, specifying the theme settings for the application.
- `storage.ts`: Defines the structure of the local storage schema for a chatbot UI.
- `openai.ts`: Defines the structure of OpenAI models and their identifiers.
- `chat.ts`: Defines various interfaces and types related to a chat system.
- `export.ts`: Defines various types and interfaces related to the export functionality of the application.
- `google.ts`: Defines several interfaces related to Google's services.
- `folder.ts`: Defines the structure of a 'Folder' object within the project.
- `index.ts`: An empty placeholder file.
- `env.ts`: Defines the `ProcessEnv` interface, representing the environment variables related to the OpenAI API.
- `error.ts`: Defines the `ErrorMessage` interface, used to structure the error messages in the application.

## Key Components

Several files in the `types` directory are particularly noteworthy due to their extensive use throughout the codebase:

- `data.ts`: The `KeyValuePair` interface defined in this file is likely used throughout the project wherever a key-value pair structure is needed, providing a consistent structure for such data.
- `prompt.ts`: The `Prompt` interface defined in this file is likely used to provide a consistent structure for prompt objects throughout the codebase.
- `plugin.ts`: The interfaces and enums defined in this file are likely used to manage plugins in the application.
- `storage.ts`: The `LocalStorage` interface defined in this file is likely used to manage the local storage schema for the chatbot UI.
- `openai.ts`: The interfaces and enums defined in this file are likely used to manage interactions with OpenAI models.

## Usage & Examples

The types, interfaces, and constants defined in the `types` directory are used throughout the codebase to provide a consistent structure for various parts of the project. For example, the `KeyValuePair` interface defined in `data.ts` is likely used wherever a key-value pair structure is needed. Similarly, the `Prompt` interface defined in `prompt.ts` is likely used to provide a consistent structure for prompt objects throughout the codebase.

The `plugin.ts` file defines the structure and data for plugins in the application. It contains interfaces `Plugin` and `PluginKey` that define the structure of a plugin and its key respectively. It also defines two enums `PluginID` and `PluginName` for plugin identification and naming. The file exports a constant `Plugins` which is a record of all plugins, each with its ID, name, and required keys. Another constant `PluginList` is exported which is an array of all plugins.

The `storage.ts` file defines the structure of the local storage schema for a chatbot UI. It imports several interfaces and types from other files in the same directory. The `LocalStorage` interface defined in this file includes properties for an API key, conversation history, selected conversation, theme, folders, prompts, visibility of chat and prompt bars, and plugin keys. The theme can be either 'light' or 'dark'. The conversation history and selected conversation are of type `Conversation`, folders are of type `FolderInterface`, prompts are of type `Prompt`, and plugin keys are of type `PluginKey`. The `showChatbar` and `showPromptbar` are boolean values indicating the visibility of the chat and prompt bars respectively.

The `openai.ts` file defines the structure of OpenAI models and their identifiers. The file exports an interface `OpenAIModel` that describes the properties of an OpenAI model, including its `id`, `name`, `maxLength` (maximum length of a message), and `tokenLimit`. It also exports an enumeration `OpenAIModelID` that lists the identifiers for different OpenAI models. A constant `fallbackModelID` is defined as a default model identifier. Lastly, the file exports a record `OpenAIModels` that maps the model identifiers to their respective model details.
