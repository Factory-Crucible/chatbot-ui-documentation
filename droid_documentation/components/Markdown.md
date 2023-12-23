
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown content within the chatbot user interface. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the project as they enhance the user experience by providing a visually appealing and interactive way to display markdown and code content.

### Contents

The `components/Markdown` directory is composed of two TypeScript files:

- `MemoizedReactMarkdown.tsx`: This file exports a memoized functional component that uses the 'react-markdown' library to render markdown content. The component is optimized for performance by preventing unnecessary re-renders using React's 'memo' function.

- `CodeBlock.tsx`: This file exports a functional component that displays code blocks in markdown format. It uses 'react-syntax-highlighter' for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two critical components:

- `MemoizedReactMarkdown`: This component is crucial as it is responsible for rendering markdown content within the chatbot UI. By using the 'react-markdown' library, it ensures that markdown content is displayed correctly and consistently. Furthermore, the component is memoized, which optimizes performance by preventing unnecessary re-renders, especially when dealing with large markdown content.

- `CodeBlock`: This component is used to display code blocks within markdown content. It enhances the user experience by providing syntax highlighting for the code blocks using 'react-syntax-highlighter'. Additionally, it offers functionality to copy the code to clipboard and download the code as a file, providing users with more ways to interact with the code content.

### Usage & Examples

The components within the `components/Markdown` directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component can be used to render markdown content received from the chatbot. Here's a simplified example of how it might be used:

```typescript
<MemoizedReactMarkdown>{chatbotResponse}</MemoizedReactMarkdown>
```

The `CodeBlock` component, on the other hand, can be used within the `MemoizedReactMarkdown` component to display code blocks within the markdown content. Here's a simplified example of how it might be used:

```typescript
<CodeBlock language="javascript" value={codeSnippet} />
```

In this example, `codeSnippet` would be a string containing the code to be displayed, and "javascript" would be the programming language of the code. The `CodeBlock` component would then display the code with appropriate syntax highlighting, and provide options to copy the code to clipboard and download it as a file.
