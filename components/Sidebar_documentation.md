
## components/Sidebar

The `components/Sidebar` directory is a crucial part of the `integration-chatbot-ui` project. It contains TypeScript files that define the Sidebar component and its subcomponents. The Sidebar component is a key part of the user interface, providing a navigational element that can be opened and closed by the user. It is designed to be flexible and reusable, accepting a variety of props for functionality and using the `react-i18next` library for translation.

### Contents

The `components/Sidebar` directory contains the following files and subdirectories:

- `index.ts`: A simple TypeScript index file that exports the Sidebar component.
- `Sidebar.tsx`: Defines the Sidebar component, which accepts various props for functionality.
- `SidebarButton.tsx`: Defines a functional component that returns a styled button element.
- `components`: A subdirectory that contains additional components used in the Sidebar.

### Folder Structure Overview

The `components/Sidebar` directory is organized into two main parts. The root of the directory contains the main Sidebar component and a SidebarButton component. The Sidebar component is a complex component that accepts a variety of props for functionality, including handlers for various events and components for rendering items and folders. The SidebarButton component is a simpler component that renders a button with specific styling and behavior.

The `components` subdirectory contains additional components used in the Sidebar. These components are more specific and are used to control the opening and closing of the Sidebar.

### Key Components

The key components in the `components/Sidebar` directory are:

- `Sidebar.tsx`: This is the main Sidebar component. It is a complex component that accepts a variety of props for functionality. It contains logic for drag and drop events and renders different UI elements based on whether it's open and if there are items present. [Link to Sidebar.tsx documentation](./Sidebar.tsx.md)
- `SidebarButton.tsx`: This is a functional component that returns a styled button element. It takes three props: 'text' which is a string, 'icon' which is a JSX element, and 'onClick' which is a function. [Link to SidebarButton.tsx documentation](./SidebarButton.tsx.md)
- `components/OpenCloseButton.tsx`: This file defines two components, 'CloseSidebarButton' and 'OpenSidebarButton', which are used to open and close a sidebar in a user interface. [Link to OpenCloseButton.tsx documentation](./components/OpenCloseButton.tsx.md)

### Usage & Examples

The Sidebar component is used throughout the `integration-chatbot-ui` project as a navigational element. It can be opened and closed by the user, and it contains items and folders that the user can interact with.

For example, the Sidebar component might be used like this:

```jsx
<Sidebar
  isOpen={isOpen}
  addItemButtonTitle="Add Item"
  side="left"
  items={items}
  itemComponent={ItemComponent}
  folderComponent={FolderComponent}
  searchTerm={searchTerm}
  handleSearchTerm={handleSearchTerm}
  toggleOpen={toggleOpen}
  handleCreateItem={handleCreateItem}
  handleCreateFolder={handleCreateFolder}
  handleDrop={handleDrop}
/>
```

The SidebarButton component is used within the Sidebar component to render buttons. It might be used like this:

```jsx
<SidebarButton
  text="Button Text"
  icon={<Icon />}
  onClick={handleClick}
/>
```

The 'CloseSidebarButton' and 'OpenSidebarButton' components are used to control the opening and closing of the Sidebar. They might be used like this:

```jsx
<CloseSidebarButton onClick={handleClose} side="left" />
<OpenSidebarButton onClick={handleOpen} side="right" />
```
