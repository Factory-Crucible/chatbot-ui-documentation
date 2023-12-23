
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format respectively. These components are integral to the chatbot UI as they ensure the proper display of markdown content and code snippets, contributing to the overall user experience.

### Contents

The `components/Markdown` directory is a flat structure with no subdirectories. It contains two TypeScript files:

- `MemoizedReactMarkdown.tsx`: This file exports a memoized functional component that uses the 'react-markdown' library to render markdown content. The component is optimized for performance by preventing unnecessary re-renders.

- `CodeBlock.tsx`: This file exports a functional component that displays code blocks in markdown format. It uses 'react-syntax-highlighter' for syntax highlighting and provides functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two critical components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. It uses the 'react-markdown' library to convert markdown syntax into HTML, providing a rich text display for users. The component is memoized using React's 'memo' function, optimizing performance by preventing unnecessary re-renders when the markdown content remains unchanged.

- `CodeBlock`: This component is responsible for displaying code blocks within the markdown content. It uses 'react-syntax-highlighter' for syntax highlighting, enhancing readability of the code snippets. The component also provides functionality to copy the code to clipboard and download the code as a file, enhancing the user experience by providing easy access to the code snippets.

### Usage & Examples

The components in the `components/Markdown` directory are used throughout the chatbot UI to render markdown content and display code blocks.

For instance, the `MemoizedReactMarkdown` component could be used to render markdown content received from the chatbot. The component would take the markdown content as a prop and render it into HTML. Here is a simplified example of how it might be used:

```typescript
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>
```

The `CodeBlock` component could be used within the `MemoizedReactMarkdown` component to render code blocks within the markdown content. The component would take the programming language and the code snippet as props, and display the code snippet with syntax highlighting. Here is a simplified example of how it might be used:

```typescript
<CodeBlock language="javascript" value={codeSnippet} />
```

These examples are simplified and do not represent the full complexity of the actual usage within the codebase. However, they provide a basic understanding of how these components are used to render markdown content and display code blocks within the chatbot UI.
