
## components/Mobile

The `components/Mobile` directory is dedicated to the mobile version of the chatbot UI application. It contains TypeScript files that define components specifically designed for mobile interfaces. Currently, it houses a single file, `Navbar.tsx`, which defines a functional component for the mobile application's navigation bar. This component is a critical part of the mobile chat application, as it manages the display of the active chat and the initiation of new conversations.

### Contents

The `components/Mobile` directory contains the following file:

- `Navbar.tsx`: This TypeScript file defines the `Navbar` functional component for the mobile application's navigation bar. It is responsible for displaying the active chat and managing the initiation of new conversations.

### Key Components

The `Navbar.tsx` file is a critical component in this directory. It defines the `Navbar` functional component, which is a key part of the mobile chat application's user interface. This component manages the display of the active chat and the initiation of new conversations, contributing to the overall functionality and user experience of the mobile application.

### Usage & Examples

The `Navbar` component is used in the mobile chat application. It accepts two props: `selectedConversation` and `onNewConversation`. The `selectedConversation` prop is an object of type `Conversation` that represents the currently active chat. The `onNewConversation` prop is a function that is triggered when a new conversation is initiated.

Here is a simplified example of how the `Navbar` component might be used:

```typescript
<Navbar
  selectedConversation={currentConversation}
  onNewConversation={handleNewConversation}
/>
```

In this example, `currentConversation` is the currently active chat, and `handleNewConversation` is a function that initiates a new conversation when the 'IconPlus' button in the `Navbar` component is clicked.
