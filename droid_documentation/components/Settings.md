
## components/Settings

The `components/Settings` directory is a crucial part of the chatbot-ui project, housing three TypeScript React component files that manage various aspects of the application's settings. These components are `SettingDialog.tsx`, `Import.tsx`, and `Key.tsx`. Each of these components plays a unique role in the application, providing functionality for managing a settings dialog, importing data, and handling API key settings respectively. These components are integral to the application's functionality, allowing users to customize their experience and interact with the chatbot in a seamless and efficient manner.

### Contents

The `components/Settings` directory contains the following files:

- `SettingDialog.tsx`: This file exports a functional component that manages a settings dialog. The dialog allows users to change the application theme and handles outside clicks to close the dialog.
- `Import.tsx`: This file provides an import functionality, rendering a file input and a button that triggers the file picker. It reads the selected file as text, parses it as JSON, and calls a function with the parsed data.
- `Key.tsx`: This file manages the API key settings, maintaining a local state for the key and a flag indicating if the key is being changed. It handles key press events, updates the key when 'Enter' is pressed, and focuses on the input field when the key is being changed. It renders either an input field for changing the key or a button to initiate the change, depending on the state.

### Key Components

The key components in the `components/Settings` directory are the `SettingDialog.tsx`, `Import.tsx`, and `Key.tsx` files. These files are critical to the functionality of the chatbot-ui project, providing the necessary components for managing the application's settings.

- `SettingDialog.tsx`: This component is responsible for managing the settings dialog. It uses several hooks, including `useContext`, `useEffect`, `useReducer`, and `useRef`, to manage the dialog's state and handle user interactions. It also uses the `useTranslation` hook from `next-i18next` for internationalization. The component fetches the current settings using the `getSettings` utility function and allows the user to change the theme of the application. The new settings are saved using the `saveSettings` utility function.
- `Import.tsx`: This component provides an import functionality for the application. It uses the `next-i18next` library for internationalization and the `@tabler/icons-react` library for icons. The component accepts a prop `onImport` which is a function that takes a parameter of type `SupportedExportFormats`. When a file is selected, it reads the file as text and parses it as JSON, then calls the `onImport` function with the parsed data.
- `Key.tsx`: This component manages the API key settings for the application. It maintains a local state for the API key and a boolean flag to indicate whether the key is being changed. The component handles key press events and updates the API key when the 'Enter' key is pressed. It also uses an effect to focus on the input field when the key is being changed.

### Usage & Examples

The components in the `components/Settings` directory are used throughout the chatbot-ui project to manage the application's settings. They provide functionality for managing a settings dialog, importing data, and handling API key settings.

For example, the `SettingDialog.tsx` component is used to manage the settings dialog. It fetches the current settings using the `getSettings` utility function and allows the user to change the theme of the application. The new settings are saved using the `saveSettings` utility function.

The `Import.tsx` component provides an import functionality for the application. When a file is selected, it reads the file as text and parses it as JSON, then calls the `onImport` function with the parsed data.

The `Key.tsx` component manages the API key settings for the application. It maintains a local state for the API key and a boolean flag to indicate whether the key is being changed. The component handles key press events and updates the API key when the 'Enter' key is pressed.
