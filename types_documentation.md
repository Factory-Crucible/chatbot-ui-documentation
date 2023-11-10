
## Types Directory

The `types` directory is a crucial part of the `integration-chatbot-ui` project. It contains TypeScript files that define various interfaces, types, and constants used throughout the codebase. These definitions provide a clear and consistent structure for the data used in the application, ensuring type safety and reducing the likelihood of runtime errors.

### Contents

The `types` directory contains the following files:

- `index.ts`: This file is currently empty and does not contain any code or comments.
- `data.ts`: Defines a `KeyValuePair` interface, representing a key-value pair.
- `settings.ts`: Exports a `Settings` interface for application theme settings.
- `error.ts`: Defines an `ErrorMessage` interface for error messages.
- `prompt.ts`: Outlines a `Prompt` interface for prompt objects.
- `storage.ts`: Defines a `LocalStorage` interface for the application's local storage schema.
- `chat.ts`: Contains interfaces and types for a chat system.
- `google.ts`: Defines interfaces for Google services in a chat application.
- `folder.ts`: Defines a `FolderInterface` and a `FolderType` type.
- `openai.ts`: Outlines structures and constants related to OpenAI models.
- `plugin.ts`: Defines structures and types for plugins.
- `export.ts`: Defines types and interfaces for exporting data.
- `env.ts`: Defines a `ProcessEnv` interface for environment variables.

The directory does not contain any subdirectories.

### Folder Structure Overview

The `types` directory is organized in a flat structure, with all TypeScript files residing at the root level. Each file is named according to the type or interface it defines, making it easy to locate the definitions. The `index.ts` file, although currently empty, can be used in the future to export types and interfaces from the directory.

### Key Components

Some of the key components in the `types` directory include:

- `chat.ts`: This file contains critical interfaces and types for the chat system, including the `Message`, `Role`, `ChatBody`, and `Conversation` definitions. [Link to documentation](./chat.md)
- `openai.ts`: This file outlines important structures and constants related to OpenAI models, including the `OpenAIModel` interface and `OpenAIModelID` enumeration. [Link to documentation](./openai.md)
- `storage.ts`: This file defines the `LocalStorage` interface, which represents the schema for local storage in the application. [Link to documentation](./storage.md)

### Usage & Examples

The types and interfaces defined in the `types` directory are used throughout the `integration-chatbot-ui` codebase. For example, the `Prompt` interface defined in `prompt.ts` is used to structure the prompts sent to the AI model:

```typescript
import { Prompt } from '../types/prompt';

const examplePrompt: Prompt = {
  id: '1',
  name: 'Example Prompt',
  description: 'This is an example prompt.',
  content: 'Hello, world!',
  model: 'gpt-3.5-turbo',
  folderId: null,
};
```

Similarly, the `LocalStorage` interface defined in `storage.ts` is used to structure the data stored in the application's local storage:

```typescript
import { LocalStorage } from '../types/storage';

const exampleStorage: LocalStorage = {
  apiKey: 'example-api-key',
  conversationHistory: [],
  selectedConversation: null,
  theme: 'light',
  folders: [],
  prompts: [],
  showChatbar: true,
  showPromptbar: true,
  pluginKeys: [],
};
```
