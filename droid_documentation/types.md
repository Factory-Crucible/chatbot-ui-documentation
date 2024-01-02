
# `types` Directory

The `types` directory is a crucial part of the codebase, serving as the central location for TypeScript type definitions, interfaces, and constants that are used throughout the project. The directory contains a collection of TypeScript files, each defining a specific set of types or interfaces that are related to a particular aspect of the project. These types and interfaces provide a consistent structure for data and ensure type safety across the codebase.

## Contents

The `types` directory contains the following TypeScript files:

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
- `env.ts`: Defines an interface representing the environment variables related to the OpenAI API.
- `error.ts`: Defines an interface used to structure the error messages in the application.

## Key Components

The `types` directory contains several key components that are critical to the functioning of the project. These include:

- `data.ts`: This file is used wherever a key-value pair structure is needed, providing a consistent structure for such data.
- `prompt.ts`: This file provides a consistent structure for prompt objects throughout the codebase.
- `plugin.ts`: This file is used to define the structure of plugins and their keys, and to list the identifiers and names for different plugins.
- `settings.ts`: This file is used across the application to ensure consistent usage of the theme settings.
- `storage.ts`: This file defines the structure of the local storage schema for a chatbot UI, including properties for an API key, conversation history, selected conversation, theme, folders, prompts, visibility of chat and prompt bars, and plugin keys.
- `openai.ts`: This file primarily defines the structure of OpenAI models and their identifiers, and is used to interact with the OpenAI API.
- `chat.ts`: This file defines various interfaces and types related to a chat system, including a chat message, a chat body, and a conversation.
- `export.ts`: This file defines various types and interfaces related to the export functionality of the application, including different versions of the export format.
- `google.ts`: This file is used to interact with Google's APIs and structure the data returned from these services.
- `folder.ts`: This file is used throughout the project whenever a 'Folder' object is required.
- `env.ts`: This file is used to ensure that the correct types are used for the environment variables related to the OpenAI API throughout the application.
- `error.ts`: This file is used to structure the error messages in the application.

## Usage & Examples

The types and interfaces defined in the `types` directory are used throughout the codebase to ensure type safety and provide a consistent structure for data. For example, the `KeyValuePair` interface defined in `data.ts` is likely used wherever a key-value pair structure is needed. Similarly, the `Prompt` interface defined in `prompt.ts` is likely used to provide a consistent structure for prompt objects throughout the codebase.

The `settings.ts` file defines the `Settings` interface, which is used across the application to ensure consistent usage of the theme settings. The `theme` property of the `Settings` interface can take two possible string values: 'light' or 'dark'.

The `storage.ts` file defines the structure of the local storage schema for a chatbot UI. The `LocalStorage` interface includes properties for an API key, conversation history, selected conversation, theme, folders, prompts, visibility of chat and prompt bars, and plugin keys.

The `openai.ts` file primarily defines the structure of OpenAI models and their identifiers. The `OpenAIModel` interface describes the properties of an OpenAI model, including its 'id', 'name', 'maxLength' (maximum length of a message), and 'tokenLimit'. The file also exports a record 'OpenAIModels' that maps the model identifiers to their respective model details.

The `chat.ts` file defines various interfaces and types related to a chat system. The `Message` interface represents a chat message with a role and content. The `Role` type can be either 'assistant' or 'user'. The `ChatBody` interface represents the body of a chat, including the model used, an array of messages, a key, a prompt, and a temperature. The `Conversation` interface represents a conversation, including an id, name, an array of messages, a model, a prompt, a temperature, and a folderId which can be null.

The `export.ts` file defines various types and interfaces related to the export functionality of the application. It defines a type 'SupportedExportFormats' which is a union of four different types: 'ExportFormatV1', 'ExportFormatV2', 'ExportFormatV3', and 'ExportFormatV4'. It also defines a type 'LatestExportFormat' which is equivalent to 'ExportFormatV4'. The file then defines four interfaces: 'ConversationV1', 'ChatFolder', 'ExportFormatV2', 'ExportFormatV3', and 'ExportFormatV4'. Each of these interfaces represents a different version of the export format, with each subsequent version adding more fields to the previous one.

The `google.ts` file defines several interfaces related to Google's services. The 'GoogleBody' interface extends 'ChatBody' and includes Google-specific keys. The 'GoogleResponse' interface is designed to structure the response from Google's services, containing a 'Message'. The 'GoogleSource' interface describes the source of information from Google's services, including title, link, display link, snippet, image, and text.

The `folder.ts` file defines the structure of a 'Folder' object within the project. The 'FolderInterface' outlines the properties of a 'Folder' object, including an 'id' of type string, a 'name' of type string, and a 'type' of type 'FolderType'. The 'FolderType' can be either 'chat' or 'prompt'.

The `env.ts` file defines an interface named 'ProcessEnv'. This interface represents the environment variables related to the OpenAI API that the application uses. The variables include the API key, host, type, version, and organization. The API key is mandatory, while the host, type, version, and organization are optional. The type can be either 'openai' or 'azure'.

The `error.ts` file defines an interface named 'ErrorMessage'. This interface is used to structure the error messages in the application. It contains three properties: 'code', 'title', and 'messageLines'. The 'code' property can be a string or null, representing the error code. The 'title' property is a string that represents the title of the error. The 'messageLines' property is an array of strings, each string representing a line in the error message.
