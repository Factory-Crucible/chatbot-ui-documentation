
# Directory Overview: components

The `components` directory houses various subdirectories, each containing TypeScript files for different parts of the chatbot UI project. These components encapsulate specific styles, behaviors, and functionalities associated with different parts of the user interface and functionality of the chatbot.

## Contents

The `components` directory is a collection of components that together form the chatbot UI. These components handle various aspects of the chat, including message input, message display, error handling, model selection, temperature adjustment, system prompts, and variable handling. The directory also includes components for managing the settings of the chatbot UI, providing a search functionality, representing a folder in the file system, displaying a spinning animation to indicate a loading state, and managing the sidebar of the application.

## Structure

The directory's structure is as follows:

- [`components/Markdown`](Markdown.md): Houses two TypeScript components, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, responsible for rendering markdown content and displaying code blocks in markdown format, respectively.
- [`components/Buttons`](Buttons.md): A collection of button components used across the chatbot UI. These components encapsulate specific styles and behaviors associated with different types of buttons.
- [`components/Search`](Search.md): Home to the `Search` component of the chatbot-ui project. This component is a functional React component written in TypeScript, designed to handle user search input within the chatbot interface.
- [`components/Settings`](Settings.md): Houses three TypeScript React components that manage various settings of the chatbot UI. These components handle the settings dialog, import functionality, and API key settings.
- [`components/Chat`](Chat.md): Dedicated to the chat functionality of the application. It contains a collection of React components that together form the chat interface.
- [`components/Chatbar`](Chatbar.md): Contains the `Chatbar` component and its related files and subcomponents. The `Chatbar` component represents a sidebar in the user interface of the application, providing functions for managing prompts and folders.
- [`components/Spinner`](Spinner.md): Dedicated to the Spinner component, a React component that displays a spinning animation typically used to indicate a loading state.
- [`components/Sidebar`](Sidebar.md): Houses the Sidebar component and its functionalities. The Sidebar component is a functional component that renders different layouts based on its state and handles various actions.
- [`components/Promptbar`](Promptbar.md): Contains the `Promptbar` component and its related files and subcomponents. The `Promptbar` component represents a sidebar in the user interface of the application, providing functions for managing prompts and folders.
- [`components/Folder`](Folder.md): Dedicated to the representation and functionality of a folder within the file system of the chatbot UI.
- [`components/Mobile`](Mobile.md): Dedicated to the mobile version of the chatbot UI. It contains a single TypeScript file, `Navbar.tsx`, which defines a functional component for the mobile application's navigation bar.
