
## components/Sidebar

The `components/Sidebar` directory is a crucial part of the chatbot UI project. It houses the TypeScript files that define the Sidebar component and its functionalities. The Sidebar component is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization. The directory also includes a 'components' subdirectory, which contains additional component files for managing the sidebar. 

### Contents

The `components/Sidebar` directory contains the following files and subdirectories:

- `index.ts`: This file serves as an entry point, exporting the main Sidebar component from 'Sidebar.tsx'.
- `Sidebar.tsx`: This file defines the Sidebar component, which is a functional component that handles various actions and renders different layouts based on its state.
- `SidebarButton.tsx`: This file defines a SidebarButton component with specific styling and behavior. It accepts three props: 'text', 'icon', and 'onClick'.
- `components/Sidebar/components`: This subdirectory contains additional component files for managing the sidebar. Notably, it includes 'OpenCloseButton.tsx', which exports two components responsible for opening and closing the sidebar. These components change appearance based on the screen size.

### Key Components

The key components in the `components/Sidebar` directory are:

- `Sidebar.tsx`: This file defines the Sidebar component, which is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization.
- `SidebarButton.tsx`: This file defines a SidebarButton component with specific styling and behavior. It accepts three props: 'text', 'icon', and 'onClick'.
- `components/Sidebar/components/OpenCloseButton.tsx`: This file exports two components: 'CloseSidebarButton' and 'OpenSidebarButton'. These components are responsible for opening and closing the sidebar, respectively. They accept two props: 'onClick', a function triggered when the button is clicked, and 'side', a string indicating the side of the screen where the sidebar is located.

### Usage & Examples

The files and subdirectories in the `components/Sidebar` directory are used to manage the sidebar in the chatbot UI. The Sidebar component, defined in `Sidebar.tsx`, is a functional component that handles various actions and renders different layouts based on its state. It uses the 'react-i18next' library for internationalization. The SidebarButton component, defined in `SidebarButton.tsx`, is used in the sidebar and accepts three props: 'text', 'icon', and 'onClick'. The 'components/Sidebar/components/OpenCloseButton.tsx' file exports two components: 'CloseSidebarButton' and 'OpenSidebarButton'. These components are responsible for opening and closing the sidebar, respectively.

Here is an example of how the Sidebar component might be used:

```typescript
import Sidebar from 'components/Sidebar';

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

In this example, the Sidebar component is imported from 'components/Sidebar' and used with various props. The 'isOpen' prop determines whether the sidebar is open or not, the 'addItemButtonTitle' prop sets the title of the 'Add Item' button, and the 'side' prop sets the side of the screen where the sidebar is located. The 'items', 'itemComponent', and 'folderComponent' props are used to render items and folders in the sidebar. The 'searchTerm' and 'handleSearchTerm' props are used for handling search terms. The 'toggleOpen', 'handleCreateItem', 'handleCreateFolder', and 'handleDrop' props are used for handling various actions such as opening and closing the sidebar, creating items and folders, and handling drag and drop events.
