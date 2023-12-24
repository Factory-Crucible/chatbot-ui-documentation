
## components/Sidebar

The `components/Sidebar` directory is a crucial part of the chatbot UI project. It houses the TypeScript files that define the Sidebar component and its functionalities. The Sidebar component is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization. The Sidebar component is not just a simple UI element; it is a complex component that interacts with other parts of the application, handling actions such as creating items and folders, and managing search terms.

### Contents

The `components/Sidebar` directory contains several TypeScript files and a subdirectory:

- `index.ts`: This file serves as an entry point, exporting the main Sidebar component from 'Sidebar.tsx'.
- `Sidebar.tsx`: This file defines the Sidebar component, which is a functional component that handles various actions and renders different layouts based on its state.
- `SidebarButton.tsx`: This file defines a SidebarButton component with specific styling and behavior. It accepts three props: 'text', 'icon', and 'onClick'.
- `components/Sidebar/components`: This subdirectory contains additional component files for managing the sidebar. Notably, it includes 'OpenCloseButton.tsx', which exports two components responsible for opening and closing the sidebar.

### Key Components

The `components/Sidebar` directory contains several key components:

- `Sidebar.tsx`: This file defines the Sidebar component, which is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization.
- `SidebarButton.tsx`: This file defines a SidebarButton component with specific styling and behavior. It accepts three props: 'text', 'icon', and 'onClick'.
- `components/Sidebar/components/OpenCloseButton.tsx`: This file exports two components: 'CloseSidebarButton' and 'OpenSidebarButton'. These components are responsible for opening and closing the sidebar, respectively.

### Usage & Examples

The files in the `components/Sidebar` directory are used to manage the sidebar in the chatbot UI. The Sidebar component, defined in `Sidebar.tsx`, is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization.

The SidebarButton component, defined in `SidebarButton.tsx`, is used in the Sidebar component. It accepts three props: 'text', 'icon', and 'onClick'. The 'text' prop is a string that represents the button's label, the 'icon' prop is a JSX.Element that represents the button's icon, and the 'onClick' prop is a function that is executed when the button is clicked.

The 'CloseSidebarButton' and 'OpenSidebarButton' components, defined in `components/Sidebar/components/OpenCloseButton.tsx`, are used to open and close the sidebar. They accept two props: 'onClick', a function that is triggered when the button is clicked, and 'side', a string that can be either 'left' or 'right', indicating the side of the screen where the sidebar is located.

Here is an example of how the Sidebar component might be used:

```typescript
<Sidebar
  isOpen={isOpen}
  addItemButtonTitle="Add Item"
  side="left"
  items={items}
  itemComponent={<ItemComponent />}
  folderComponent={<FolderComponent />}
  searchTerm={searchTerm}
  handleSearchTerm={handleSearchTerm}
  toggleOpen={toggleOpen}
  handleCreateItem={handleCreateItem}
  handleCreateFolder={handleCreateFolder}
  handleDrop={handleDrop}
/>
```

In this example, the Sidebar component is used with several props. The 'isOpen' prop is a boolean that indicates whether the sidebar is open. The 'addItemButtonTitle' prop is a string that represents the title of the 'Add Item' button. The 'side' prop is a string that can be either 'left' or 'right', indicating the side of the screen where the sidebar is located. The 'items' prop is an array of items that are displayed in the sidebar. The 'itemComponent' and 'folderComponent' props are React components that are used to render items and folders, respectively. The 'searchTerm' prop is a string that represents the current search term. The 'handleSearchTerm', 'toggleOpen', 'handleCreateItem', 'handleCreateFolder', and 'handleDrop' props are functions that handle various actions.
