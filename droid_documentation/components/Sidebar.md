
## components/Sidebar

The `components/Sidebar` directory is a crucial part of the chatbot UI project. It houses the TypeScript files that define the Sidebar component and its functionalities. The Sidebar component is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization. The directory also includes a subdirectory, `components/Sidebar/components`, which contains additional component files for managing the sidebar.

### Contents

The `components/Sidebar` directory contains the following files and subdirectories:

- `index.ts`: This file serves as an entry point, exporting the main Sidebar component from 'Sidebar.tsx'.
- `Sidebar.tsx`: This file defines the Sidebar component, a functional component that handles various actions and renders different layouts based on its state.
- `SidebarButton.tsx`: This file defines a SidebarButton component with specific styling and behavior. It accepts three props: 'text', 'icon', and 'onClick'.
- `components/Sidebar/components`: This subdirectory contains additional component files for managing the sidebar. Notably, it includes 'OpenCloseButton.tsx', which exports two components responsible for opening and closing the sidebar.

### Key Components

- `Sidebar.tsx`: This file defines the Sidebar component, which is a key part of the user interface. It handles various actions and renders different layouts based on its state. It also uses the 'react-i18next' library for internationalization.
- `SidebarButton.tsx`: This file defines the SidebarButton component, which is used extensively in the Sidebar component. It has specific styling and behavior and accepts three props: 'text', 'icon', and 'onClick'.
- `components/Sidebar/components/OpenCloseButton.tsx`: This file exports two components, 'CloseSidebarButton' and 'OpenSidebarButton', which are responsible for opening and closing the sidebar. These components change appearance based on the screen size.

### Usage & Examples

The files and subfolders within the `components/Sidebar` directory are used to manage the sidebar in the chatbot UI. The Sidebar component, defined in `Sidebar.tsx`, is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization.

The `SidebarButton.tsx` file defines a SidebarButton component with specific styling and behavior. It accepts three props: 'text', 'icon', and 'onClick'. This component is used extensively within the Sidebar component to create buttons with specific actions.

The `components/Sidebar/components/OpenCloseButton.tsx` file exports two components, 'CloseSidebarButton' and 'OpenSidebarButton', which are responsible for opening and closing the sidebar. These components change appearance based on the screen size and are used within the Sidebar component to manage its open and closed states.

For example, the Sidebar component might be used in the following way:

```typescript
<Sidebar
  isOpen={isOpen}
  addItemButtonTitle="Add Item"
  side="left"
  items={items}
  itemComponent={<ItemComponent />}
  folderComponent={<FolderComponent />}
  footerComponent={<FooterComponent />}
  searchTerm={searchTerm}
  handleSearchTerm={handleSearchTerm}
  toggleOpen={toggleOpen}
  handleCreateItem={handleCreateItem}
  handleCreateFolder={handleCreateFolder}
  handleDrop={handleDrop}
/>
```

In this example, the Sidebar component is rendered with various props that control its behavior and appearance. The `isOpen` prop controls whether the sidebar is open or not, the `addItemButtonTitle` prop sets the title of the "Add Item" button, and the `side` prop determines which side of the screen the sidebar appears on. The `items`, `itemComponent`, `folderComponent`, and `footerComponent` props control the items displayed in the sidebar and their appearance. The `searchTerm`, `handleSearchTerm`, `toggleOpen`, `handleCreateItem`, `handleCreateFolder`, and `handleDrop` props provide handlers for various actions such as searching, opening and closing the sidebar, creating items and folders, and handling drag and drop events.
