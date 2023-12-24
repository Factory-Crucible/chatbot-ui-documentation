
## `components/Markdown` Directory

The `components/Markdown` directory is a specialized section of the codebase dedicated to handling markdown rendering within the chatbot UI. It contains two TypeScript component files, `MemoizedReactMarkdown.tsx` and `CodeBlock.tsx`, which are responsible for rendering markdown content and displaying code blocks in markdown format, respectively. These components are integral to the chatbot UI, as they enable the display of rich text content and code snippets in a user-friendly and efficient manner.

### Contents

The `components/Markdown` directory contains the following files:

- `MemoizedReactMarkdown.tsx`: This TypeScript component file exports a memoized functional component named `MemoizedReactMarkdown`. The component uses the `react-markdown` library to render markdown content and optimizes performance by preventing unnecessary re-renders through memoization.
- `CodeBlock.tsx`: This TypeScript component file exports a functional component named `CodeBlock`. The component is used to display code blocks in markdown format, with syntax highlighting provided by the `react-syntax-highlighter` library. It also includes functionality to copy the code to clipboard and download the code as a file.

### Key Components

The `components/Markdown` directory houses two key components:

- `MemoizedReactMarkdown`: This component is crucial for rendering markdown content within the chatbot UI. By using memoization, it ensures that the rendering process is efficient and does not cause unnecessary re-renders, thereby improving the performance of the chatbot UI.
- `CodeBlock`: This component is responsible for displaying code blocks within the chatbot UI. It not only provides syntax highlighting for better readability but also offers user-friendly features such as copying the code to clipboard and downloading the code as a file. These features enhance the user experience when interacting with code snippets in the chatbot UI.

### Usage & Examples

The `MemoizedReactMarkdown` and `CodeBlock` components are used throughout the chatbot UI to render markdown content and display code blocks, respectively.

For instance, `MemoizedReactMarkdown` could be used to render a markdown string `markdownContent` as follows:

```typescript
<MemoizedReactMarkdown>{markdownContent}</MemoizedReactMarkdown>
```

Similarly, `CodeBlock` could be used to display a code block `code` in a specific `language` as follows:

```typescript
<CodeBlock language={language} value={code} />
```

These examples represent typical usage patterns of these components within the chatbot UI. They illustrate how these components contribute to the functionality and user experience of the chatbot UI.
