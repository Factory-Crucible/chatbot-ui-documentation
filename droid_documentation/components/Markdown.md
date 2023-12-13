
## components/Markdown

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot user interface. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the application's ability to display rich text content and code snippets in a user-friendly and efficient manner.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component that uses the `react-markdown` library to render markdown content. The component is optimized for performance by preventing unnecessary re-renders through the use of React's `memo` function.

- `CodeBlock.tsx`: This TypeScript component file exports a functional component that displays code blocks in markdown format. It uses the `react-syntax-highlighter` library for syntax highlighting and provides functionality to copy the code to the clipboard and download the code as a file. The component also uses `next-i18next` for internationalization.

### Key Components

The `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx` files are the key components in this directory. 

- `MemoizedReactMarkdown.tsx` is crucial for rendering markdown content within the chatbot UI. By using the `react-markdown` library, it ensures that markdown content is displayed correctly. Furthermore, its use of memoization optimizes performance by preventing unnecessary re-renders, which is particularly important for maintaining smooth user experience in scenarios where the markdown content updates frequently.

- `CodeBlock.tsx` is responsible for displaying code blocks in markdown format. This is essential for any instances where the chatbot needs to display code snippets to the user. The component's use of `react-syntax-highlighter` ensures that the code is displayed with syntax highlighting, making it easier for users to read and understand. Additionally, the component provides functionality to copy the code to the clipboard and download the code as a file, enhancing the user's ability to interact with and utilize the displayed code.

### Usage & Examples

The components in this directory are used throughout the codebase wherever markdown content or code blocks need to be displayed within the chatbot UI.

For instance, the `MemoizedReactMarkdown` component could be used to render user-generated markdown content in a chat message. Here's a simplified example of how it might be used:

```typescript
<MemoizedReactMarkdown>{userMessage}</MemoizedReactMarkdown>
```

In this example, `userMessage` is a string containing markdown content entered by the user.

Similarly, the `CodeBlock` component could be used to display a code snippet in a chat message. Here's a simplified example of how it might be used:

```typescript
<CodeBlock language="javascript" value={codeSnippet} />
```

In this example, `codeSnippet` is a string containing a code snippet, and `"javascript"` is the language of the code snippet.
