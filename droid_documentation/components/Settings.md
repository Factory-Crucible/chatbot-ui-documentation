
## components/Settings

The `components/Settings` directory is responsible for managing the settings of the application. It contains three TypeScript React component files: `SettingDialog.tsx`, `Import.tsx`, and `Key.tsx`. These components handle the settings dialog, import functionality, and API key settings respectively. They work together to provide a user-friendly interface for managing application settings.

### Contents

The `components/Settings` directory contains the following files:

- `SettingDialog.tsx`: Manages a settings dialog, allowing users to change the application theme and handling outside clicks to close the dialog.
- `Import.tsx`: Provides an import functionality, rendering a file input and a button that triggers the file picker. It reads the selected file as text, parses it as JSON, and calls a function with the parsed data.
- `Key.tsx`: Manages the API key settings, maintaining a local state for the key and a flag indicating if the key is being changed. It handles key press events, updates the key when 'Enter' is pressed, and focuses on the input field when the key is being changed.

### Key Components

- `SettingDialog.tsx`: This component is crucial as it provides the interface for users to change the application theme. It fetches the current settings using the `getSettings` utility function and saves the new settings using the `saveSettings` utility function.
- `Import.tsx`: This component is responsible for importing data into the application. It reads the selected file as text, parses it as JSON, and calls a function with the parsed data.
- `Key.tsx`: This component is responsible for managing the API key settings. It maintains a local state for the key and updates the key when 'Enter' is pressed.

### Usage & Examples

- `SettingDialog.tsx`: This component is used to manage the settings dialog of the application. It is rendered when the settings button is clicked and is closed when an outside click is detected.
- `Import.tsx`: This component is used to import data into the application. It is rendered as a file input and a button. When the button is clicked, it triggers the file input click event to open the file picker.
- `Key.tsx`: This component is used to manage the API key settings. It is rendered as either an input field for changing the key or a button to initiate the change, depending on the state.
