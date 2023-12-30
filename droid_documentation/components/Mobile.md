
## components/Mobile

The `components/Mobile` directory is dedicated to the mobile version of the chatbot UI. It contains a single TypeScript file, `Navbar.tsx`, which defines a functional component for the mobile application's navigation bar. This component is designed to be used in a chat application and is responsible for displaying the currently active chat and initiating new conversations.

### Contents

The `components/Mobile` directory contains the following file:

- `Navbar.tsx`: This TypeScript file defines a functional component named 'Navbar' for the mobile application's navigation bar. It accepts two props: 'selectedConversation', an object of type 'Conversation' representing the currently active chat, and 'onNewConversation', a function that is triggered when a new conversation is initiated. The component displays the name of the selected conversation and an 'IconPlus' button that, when clicked, triggers the 'onNewConversation' function.

### Key Components

The key component in this directory is the `Navbar` component defined in the `Navbar.tsx` file. This component is responsible for displaying the currently active chat and initiating new conversations in the mobile version of the chatbot UI.

### Usage & Examples

The `Navbar` component is used in the mobile version of the chatbot UI. It accepts two props: 'selectedConversation' and 'onNewConversation'. The 'selectedConversation' prop is an object of type 'Conversation' representing the currently active chat. The 'onNewConversation' prop is a function that is triggered when a new conversation is initiated.

Here is a simplified example of how the `Navbar` component might be used:

```typescript
<Navbar
  selectedConversation={currentConversation}
  onNewConversation={startNewConversation}
/>
```

In this example, `currentConversation` is an object of type 'Conversation' representing the currently active chat, and `startNewConversation` is a function that is triggered when a new conversation is initiated.
