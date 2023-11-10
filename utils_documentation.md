
## Utils Directory

The `utils` directory is a collection of utility modules and functions that contribute to the overall functionality of the `integration-chatbot-ui` project. It is organized into three subdirectories: `app`, `data`, and `server`. Each subdirectory contains specific utility modules that handle various aspects of the application.

### Contents

The `utils` directory contains the following subdirectories:

- `app`: This subdirectory contains modules for various application tasks like managing settings, handling data import/export, and managing chat conversations.
- `data`: This subdirectory contains a `throttle` function that controls the execution frequency of any given function.
- `server`: This subdirectory has two modules: `google.ts` for cleaning up text input and `index.ts` for handling OpenAI API requests.

### Folder Structure Overview

The `utils` directory is structured to categorize utility functions based on their usage within the application. The `app` subdirectory contains utility modules that are used throughout the application for tasks like managing settings and handling data import/export. The `data` subdirectory contains a utility function for throttling function execution. The `server` subdirectory contains utility modules for server-side tasks like cleaning up text input and handling OpenAI API requests.

### Key Components

Some of the key components in the `utils` directory include:

- `app/settings.ts`: This file manages application settings. It provides functions to retrieve and save settings from and to the local storage. [Link to documentation](./app/settings.md)
- `app/importExport.ts`: This file handles data import and export in different formats. It provides functions to export data as a JSON file and import data from a JSON file. [Link to documentation](./app/importExport.md)
- `data/throttle.ts`: This file exports a `throttle` function that controls the execution frequency of any given function. [Link to documentation](./data/throttle.md)
- `server/index.ts`: This file handles OpenAI API requests. It provides a function to send a POST request to the OpenAI API and handle the response. [Link to documentation](./server/index.md)

### Usage & Examples

The utility modules in the `utils` directory are used throughout the `integration-chatbot-ui` project. For example, the `app/settings.ts` module is used to manage application settings. It provides functions to retrieve and save settings from and to the local storage. Here is an example of how it can be used:

```typescript
import { getSettings, saveSettings } from '@/utils/app/settings';

// Retrieve settings
const settings = getSettings();

// Update a setting
settings.theme = 'dark';

// Save settings
saveSettings(settings);
```

The `app/importExport.ts` module is used to handle data import and export. It provides functions to export data as a JSON file and import data from a JSON file. Here is an example of how it can be used:

```typescript
import { exportData, importData } from '@/utils/app/importExport';

// Export data
const data = exportData();

// Import data
const importedData = importData(data);
```

The `data/throttle.ts` module provides a `throttle` function that controls the execution frequency of any given function. Here is an example of how it can be used:

```typescript
import { throttle } from '@/utils/data/throttle';

// Function to be throttled
const log = () => console.log('Hello, world!');

// Throttle function
const throttledLog = throttle(log, 1000);

// Call throttled function
throttledLog();
```

The `server/index.ts` module handles OpenAI API requests. It provides a function to send a POST request to the OpenAI API and handle the response. Here is an example of how it can be used:

```typescript
import { OpenAIStream } from '@/utils/server';

// Send a request to the OpenAI API
const response = await OpenAIStream(model, systemPrompt, temperature, key, messages);
```
